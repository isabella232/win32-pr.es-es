---
title: Fases de teselación
description: El tiempo de ejecución de Direct3D 11 admite tres nuevas fases que implementan Teselación, que convierte las superficies de subdivisiones de bajo detalle en primitivas más detalladas en la GPU.
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aacb48ccc2c95ab93ba4f34212e654880d9a369
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "104359483"
---
# <a name="tessellation-stages"></a>Fases de teselación

El tiempo de ejecución de Direct3D 11 admite tres nuevas fases que implementan Teselación, que convierte las superficies de subdivisiones de bajo detalle en primitivas más detalladas en la GPU. Mosaicos de teselación (o rotura) de superficies de orden superior en estructuras adecuadas para la representación.

Mediante la implementación de teselación en hardware, una canalización de gráficos puede evaluar modelos de menor detalle (recuento de polígonos inferiores) y representar con mayor detalle. Aunque se puede hacer la teselación de software, la teselación implementada por el hardware puede generar una cantidad increíble de detalles visuales (incluida la compatibilidad con la asignación de desplazamiento) sin agregar los detalles visuales a los tamaños del modelo y las tasas de actualización de paralyzing.

-   [Ventajas de teselación](#tessellation-benefits)
-   [Nuevas fases de canalización](#new-pipeline-stages)
    -   [Fase del sombreador de casco](#hull-shader-stage)
    -   [Fase del teselador](#tessellator-stage)
    -   [Fase de sombreador de dominios](#domain-shader-stage)
-   [API para inicializar fases de teselación](#apis-for-initializing-tessellation-stages)
-   [Cómo:](#how-tos)
-   [Temas relacionados](#related-topics)

## <a name="tessellation-benefits"></a>Ventajas de teselación

Tesela

-   Ahorra gran cantidad de memoria y ancho de banda, lo que permite que una aplicación represente superficies más detalladas de modelos de baja resolución. La técnica de teselación implementada en la canalización de Direct3D 11 también admite la asignación de desplazamiento, que puede generar sorprendentes cantidades de detalles de la superficie.
-   Admite técnicas de representación escalables, como Continuous o View dependent Level-of-detail que se puede calcular sobre la marcha.
-   Mejora el rendimiento al realizar cálculos caros con una frecuencia menor (realizando cálculos en un modelo de detalles más bajo). Esto podría incluir los cálculos de mezcla mediante formas de mezcla o destinos de transformación para la animación realista o cálculos físicos para la detección de colisiones o la dinámica del cuerpo flexible.

La canalización de Direct3D 11 implementa la teselación en el hardware, que no carga el trabajo de la CPU a la GPU. Esto puede dar lugar a mejoras de rendimiento muy grandes si una aplicación implementa un gran número de destinos transformativos y/o modelos más sofisticados. Para tener acceso a las nuevas características de teselación, debe obtener información sobre algunas nuevas fases de canalización.

## <a name="new-pipeline-stages"></a>Nuevas fases de canalización

La teselación usa la GPU para calcular una superficie más detallada de una superficie construida a partir de las cuádruples revisiones, parches de triángulo o isolíneas. Para aproximar la superficie de orden superior, cada revisión se divide en triángulos, puntos o líneas mediante factores de teselación. La canalización de Direct3D 11 implementa la teselación mediante tres nuevas fases de canalización:

-   [Fase del sombreador de casco](#hull-shader-stage) : una fase de sombreador programable que genera una revisión de geometría (y constantes de revisión) que corresponden a cada revisión de entrada (cuádruple, triángulo o línea).
-   [Fase del teselador](#tessellator-stage) : una fase de canalización de función fija que crea un patrón de muestreo del dominio que representa la revisión de geometría y genera un conjunto de objetos más pequeños (triángulos, puntos o líneas) que conectan estos ejemplos.
-   [Fase de sombreador de dominio](#domain-shader-stage) : fase de sombreador programable que calcula la posición del vértice que corresponde a cada ejemplo de dominio.

En el diagrama siguiente se resaltan las nuevas fases de la canalización de Direct3D 11.

![diagrama de la canalización de Direct3D 11 que resalta las fases de sombreador de casco, del teselador y sombreador de dominio](images/d3d11-pipeline-stages-tessellation.png)

En el diagrama siguiente se muestra la progresión a través de las fases de teselación. La progresión comienza con la superficie de subdivisión de menor detalle. La progresión resalta la revisión de entrada con la revisión geométrica correspondiente, ejemplos de dominio y triángulos que conectan estos ejemplos. Finalmente, la progresión resalta los vértices que corresponden a estos ejemplos.

![diagrama de progresión de teselación](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Hull-Shader fase

Sombreador de casco (que se invoca una vez por revisión): transforma los puntos de control de entrada que definen una superficie de orden inferior en los puntos de control que componen una revisión. También realiza algunos cálculos por revisión para proporcionar datos para la fase de teselación y la fase de dominio. En el nivel de cuadro negro más sencillo, la fase del sombreador de casco tendría un aspecto similar al diagrama siguiente.

![diagrama de la fase del sombreador de casco](images/d3d11-hull-shader.png)

Un sombreador de casco se implementa con una función HLSL y tiene las siguientes propiedades:

-   La entrada del sombreador se encuentra entre 1 y 32 puntos de control.
-   La salida del sombreador se encuentra entre 1 y 32 puntos de control, independientemente del número de factores de teselación. La fase del sombreador de dominio puede consumir la salida de los puntos de control de un sombreador de casco. Un sombreador de dominio puede consumir los datos constantes de revisión; los factores de teselación pueden ser consumidos por el sombreador de dominios y la fase de teselación.
-   Los factores de teselación determinan la cantidad de subdividir cada revisión.
-   El sombreador declara el Estado requerido por la fase del teselador. Esto incluye información como el número de puntos de control, el tipo de revisión y el tipo de partición que se va a usar cuando se teselar. Esta información aparece como declaraciones normalmente al principio del código del sombreador.
-   Si la fase del sombreador de casco establece cualquier factor de teselación perimetral en = 0 o NaN, se seleccionará la revisión. Como resultado, la fase del teselador se puede ejecutar o no, el sombreador de dominios no se ejecutará y no se producirá ningún resultado visible para dicha revisión.

En un nivel más profundo, un sombreador de casco funciona en dos fases: una fase de punto de control y una fase de revisión constante, que se ejecutan en paralelo por el hardware. El compilador de HLSL extrae el paralelismo en un sombreador de casco y lo codifica en código de bytes que controla el hardware.

-   La fase de punto de control funciona una vez para cada punto de control, Lee los puntos de control de una revisión y genera un punto de control de salida (identificado por un ControlPointID).
-   La fase patch-Constant funciona una vez por revisión para generar factores de teselación perimetral y otras constantes por revisión. Internamente, muchas fases constantes de revisión se pueden ejecutar al mismo tiempo. La fase patch-Constant tiene acceso de solo lectura a todos los puntos de control de entrada y salida.

A continuación se muestra un ejemplo de un sombreador de casco:


```
[patchsize(12)]
[patchconstantfunc(MyPatchConstantFunc)]
MyOutPoint main(uint Id : SV_ControlPointID,
     InputPatch<MyInPoint, 12> InPts)
{
     MyOutPoint result;
     
     ...
     
     result = TransformControlPoint( InPts[Id] );

     return result;
}
```



Para obtener un ejemplo que crea un sombreador de casco, consulte [Cómo: crear un sombreador de casco](direct3d-11-advanced-stages-hull-shader-create.md).

### <a name="tessellator-stage"></a>Fase del teselador

Del teselador es una fase de función fija inicializada mediante el enlace de un sombreador de casco a la canalización (vea [Cómo: inicializar la fase del teselador](direct3d-11-advanced-stages-tessellator-initialize.md)). El propósito de la fase del teselador es subdividir un dominio (cuádruple, Tri o line) en muchos objetos más pequeños (triángulos, puntos o líneas). Del teselador coloca en mosaico un dominio canónico en un sistema de coordenadas normalizado (cero a uno). Por ejemplo, un dominio cuádruple se Tesela en un cuadrado de unidad.

Del teselador funciona una vez por revisión mediante los factores de teselación (que especifican el grado de teselación del dominio) y el tipo de creación de particiones (que especifica el algoritmo que se usa para segmentar una revisión) que se pasan desde la fase del sombreador de casco. Del teselador genera coordenadas UV (y, opcionalmente, w) y la topología de superficie en la etapa del sombreador de dominio.

Internamente, el del teselador funciona en dos fases:

-   En la primera fase se procesan los factores de teselación, se corrigen los problemas de redondeo, se controlan los factores muy pequeños, se reducen y se combinan los factores mediante la aritmética de punto flotante de 32 bits.
-   La segunda fase genera listas de puntos o topologías según el tipo de partición seleccionado. Esta es la tarea principal de la fase del teselador y usa fracciones de 16 bits con aritmética de punto fijo. La aritmética de punto fijo permite la aceleración de hardware manteniendo una precisión aceptable. Por ejemplo, dada una revisión de ancho de 64, esta precisión puede colocar puntos en una resolución de 2 mm.



| Tipo de creación de particiones | Intervalo                       |
|----------------------|-----------------------------|
| fraccionario \_ impar      | \[1... 63\]                  |
| Separadores fraccionarios \_     | Intervalo de TessFactor: \[ 2.. 64\] |
| integer              | Intervalo de TessFactor: \[ 1.. 64\] |
| pow2                 | Intervalo de TessFactor: \[ 1.. 64\] |



 

### <a name="domain-shader-stage"></a>Domain-Shader fase

Un sombreador de dominio calcula la posición del vértice de un punto subdividido en la revisión de salida. Un sombreador de dominio se ejecuta una vez por punto de salida de fase de del teselador y tiene acceso de solo lectura a las coordenadas UV de salida de del teselador Stage, la revisión de salida del sombreador de casco y las constantes de la revisión de salida del sombreador de casco, como se muestra en el diagrama siguiente.

![diagrama de la fase del sombreador de dominios](images/d3d11-domain-shader.png)

Las propiedades del sombreador de dominios incluyen:

-   Un sombreador de dominio se invoca una vez por cada coordenada de salida de la fase del teselador.
-   Un sombreador de dominios consume los puntos de control de salida de la fase del sombreador de casco.
-   Un sombreador de dominio genera la posición de un vértice.
-   Las entradas son las salidas del sombreador de casco, incluidos los puntos de control, los datos constantes de revisión y los factores de teselación. Los factores de teselación pueden incluir los valores usados por la función Fixed del teselador así como los valores sin formato (antes de redondear la teselación de enteros, por ejemplo), lo que facilita la geotransformación, por ejemplo.

Una vez finalizado el sombreador de dominios, se finaliza la teselación y los datos de canalización continúan hasta la siguiente fase de canalización (sombreador de geometría, sombreador de píxeles, etc.). Un sombreador de geometría que espera primitivas con adyacencias (por ejemplo, 6 vértices por triángulo) no es válido cuando la teselación está activa (esto produce un comportamiento indefinido, al que se queja la capa de depuración).

Este es un ejemplo de un sombreador de dominios:


```
void main( out    MyDSOutput result, 
           float2 myInputUV : SV_DomainPoint, 
           MyDSInput DSInputs,
           OutputPatch<MyOutPoint, 12> ControlPts, 
           MyTessFactors tessFactors)
{
     ...

     result.Position = EvaluateSurfaceUV(ControlPoints, myInputUV);
}
```



## <a name="apis-for-initializing-tessellation-stages"></a>API para inicializar fases de teselación

La teselación se implementa con dos nuevas fases del sombreador programable: un sombreador de casco y un sombreador de dominios. Estas nuevas fases del sombreador se programan con código HLSL que se define en el modelo de sombreador 5. Los nuevos destinos del sombreador son: HS \_ 5 \_ 0 y DS \_ 5 \_ 0. Al igual que todas las fases del sombreador programable, el código del hardware se extrae de los sombreadores compilados que se pasan al tiempo de ejecución cuando los sombreadores se enlazan a la canalización mediante las API como [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) y [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader). Pero en primer lugar, el sombreador se debe crear con las API como [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) y [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).

Habilite la teselación creando un sombreador de casco y enlazándolo a la fase del sombreador de casco (Esto configura automáticamente la fase del teselador). Para generar las posiciones finales del vértice a partir de las revisiones teselas, también debe crear un sombreador de dominios y enlazarlo a la fase del sombreador del dominio. Una vez que la teselación está habilitada, la entrada de datos en la etapa del ensamblador de entrada debe ser datos de revisión. Es decir, la topología del ensamblador de entrada debe ser una topología constante de revisión de la [**\_ \_ topología primitiva D3D11**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) establecida con [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology).

Para deshabilitar la teselación, establezca el sombreador de casco y el sombreador de dominios en **null**. Ni la fase de sombreador de geometría ni la fase de flujo de salida pueden leer puntos de control de salida del sombreador de casco o datos de revisión.

-   Nuevas topologías para la fase de ensamblador de entrada, que son extensiones de esta enumeración.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    La topología se establece en la fase del ensamblador de entrada mediante [ **IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   Por supuesto, las nuevas etapas del sombreador programable requieren que se establezca otro Estado, para enlazar búferes de constantes, muestras y recursos del sombreador a las fases de canalización apropiadas. Estos nuevos métodos de ID3D11Device se implementan para establecer este estado.
    -   [**DSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetconstantbuffers)
    -   [**DSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetsamplers)
    -   [**DSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshader)
    -   [**DSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dsgetshaderresources)
    -   [**DSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetconstantbuffers)
    -   [**DSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetsamplers)
    -   [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)
    -   [**DSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshaderresources)
    -   [**HSGetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetconstantbuffers)
    -   [**HSGetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshaderresources)
    -   [**HSGetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetsamplers)
    -   [**HSGetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hsgetshader)
    -   [**HSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetconstantbuffers)
    -   [**HSSetSamplers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetsamplers)
    -   [**HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)
    -   [**HSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshaderresources)

## <a name="how-tos"></a>Cómo:

La documentación también contiene ejemplos para inicializar las fases de teselación.



| Elemento                                                                                                                                                                                                                                                                                           | Descripción                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[Cómo: crear un sombreador de casco](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Cree un sombreador de casco.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[Cómo: diseñar un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Diseñar un sombreador de casco.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[Cómo: inicializar la fase del teselador](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Inicialice la fase de teselación.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[Cómo: crear un sombreador de dominios](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Cree un sombreador de dominios.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[Cómo: diseñar un sombreador de dominios](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Cree un sombreador de dominios.<br/>            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 


---
title: Fases de teselación
description: El entorno de ejecución de Direct3D 11 admite tres nuevas fases que implementan la teselación, que convierte las superficies de subdivisión de bajo detalle en primitivas de mayor detalle en la GPU.
ms.assetid: 4ad2fd3e-6e1a-4326-8469-3198acf931dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d272ad1db53c6e70a856255c1826f4867f069897b42da0219cd334d48226d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099237"
---
# <a name="tessellation-stages"></a>Fases de teselación

El entorno de ejecución de Direct3D 11 admite tres nuevas fases que implementan la teselación, que convierte las superficies de subdivisión de bajo detalle en primitivas de mayor detalle en la GPU. Los mosaicos de teselación (o se divide) superficies de alto orden en estructuras adecuadas para la representación.

Al implementar la teselación en hardware, una canalización de gráficos puede evaluar modelos de menor detalle (recuento inferior de polígonos) y representarlos con más detalle. Aunque se puede realizar la teselación de software, la teselación implementada por hardware puede generar una gran cantidad de detalles visuales (incluida la compatibilidad con la asignación de desplazamiento) sin agregar los detalles visuales a los tamaños de modelo y paralizar las tasas de actualización.

-   [Ventajas de teselación](#tessellation-benefits)
-   [Nuevas fases de canalización](#new-pipeline-stages)
    -   [Fase de sombreador de casco](#hull-shader-stage)
    -   [Fase de teselador](#tessellator-stage)
    -   [Fase sombreador de dominio](#domain-shader-stage)
-   [API para inicializar fases de teselación](#apis-for-initializing-tessellation-stages)
-   [Cómo:](#how-tos)
-   [Temas relacionados](#related-topics)

## <a name="tessellation-benefits"></a>Ventajas de teselación

Teselación:

-   Ahorra mucha memoria y ancho de banda, lo que permite que una aplicación represente superficies más detalladas a partir de modelos de baja resolución. La técnica de teselación implementada en la canalización de Direct3D 11 también admite la asignación de desplazamiento, que puede producir cantidades sorprendentes de detalles de la superficie.
-   Admite técnicas de representación escalable, como niveles de detalle continuos o dependientes de la vista que se pueden calcular sobre la marcha.
-   Mejora el rendimiento mediante la realización de cálculos costosos a una frecuencia inferior (realizando cálculos en un modelo de menor detalle). Esto podría incluir la combinación de cálculos mediante formas de mezcla o destinos de transformación para cálculos de animación realistas o físicos para la detección de colisiones o la dinámica del cuerpo suave.

La canalización de Direct3D 11 implementa la teselación en hardware, lo que permite cargar el trabajo desde la CPU a la GPU. Esto puede dar lugar a mejoras de rendimiento muy grandes si una aplicación implementa un gran número de destinos de transformación o modelos de desenfasado/desasociación más sofisticados. Para acceder a las nuevas características de teselación, debe obtener información sobre algunas fases de canalización nuevas.

## <a name="new-pipeline-stages"></a>Nuevas fases de canalización

La teselación usa la GPU para calcular una superficie más detallada a partir de una superficie construida a partir de revisiones de cuatro, revisiones de triángulo o isolíneas. Para aproximarse a la superficie ordenada, cada revisión se subdivide en triángulos, puntos o líneas mediante factores de teselación. La canalización de Direct3D 11 implementa la teselación mediante tres nuevas fases de canalización:

-   [Fase de sombreador](#hull-shader-stage) de casco: una fase programable del sombreador que genera una revisión de geometría (y constantes de revisión) que se corresponden con cada revisión de entrada (cuadrándulo, triángulo o línea).
-   [Fase de teselador:](#tessellator-stage) fase de canalización de función fija que crea un patrón de muestreo del dominio que representa la revisión de geometría y genera un conjunto de objetos más pequeños (triángulos, puntos o líneas) que conectan estos ejemplos.
-   [Fase sombreador de dominio:](#domain-shader-stage) una fase programable del sombreador que calcula la posición del vértice que corresponde a cada ejemplo de dominio.

En el diagrama siguiente se resaltan las nuevas fases de la canalización de Direct3D 11.

![diagrama de la canalización direct3d 11 que resalta las fases del sombreador de casco, el teselador y el sombreador de dominio](images/d3d11-pipeline-stages-tessellation.png)

En el diagrama siguiente se muestra la progresión a través de las fases de teselación. La progresión comienza con la superficie de subdivisión de bajo detalle. La progresión siguiente resalta la revisión de entrada con la revisión de geometría correspondiente, los ejemplos de dominio y los triángulos que conectan estos ejemplos. Por último, la progresión resalta los vértices que corresponden a estas muestras.

![diagrama de progresión de teselación](images/tess-prog.png)

### <a name="hull-shader-stage"></a>Hull-Shader fase

Un sombreador de casco, que se invoca una vez por revisión, transforma los puntos de control de entrada que definen una superficie de orden bajo en puntos de control que conste de una revisión. También realiza algunos cálculos por revisión para proporcionar datos para la fase de teselación y la fase de dominio. En el nivel de caja negra más simple, la fase del sombreador de casco tendría un aspecto parecido al del diagrama siguiente.

![diagrama de la fase de sombreador de casco](images/d3d11-hull-shader.png)

Un sombreador de casco se implementa con una función HLSL y tiene las siguientes propiedades:

-   La entrada del sombreador está entre 1 y 32 puntos de control.
-   La salida del sombreador está entre 1 y 32 puntos de control, independientemente del número de factores de teselación. La salida de los puntos de control de un sombreador de casco se puede usar en la fase del sombreador de dominio. Un sombreador de dominio puede consumir los datos constantes de revisión. El sombreador de dominio y la fase de teselación pueden consumir los factores de teselación.
-   Los factores de teselación determinan cuánto subdividir cada revisión.
-   El sombreador declara el estado requerido por la fase del teselador. Esto incluye información como el número de puntos de control, el tipo de cara de revisión y el tipo de partición que se va a usar al tessentar. Esta información aparece como declaraciones normalmente en la parte delantera del código del sombreador.
-   Si la fase del sombreador de casco establece cualquier factor de teselación del borde en = 0 o NaN, se realizará la selección de la revisión. Como resultado, la fase del teselador puede o no ejecutarse, el sombreador de dominio no se ejecutará y no se producirá ningún resultado visible para esa revisión.

En un nivel más profundo, un sombreador de casco funciona realmente en dos fases: una fase de punto de control y una fase de revisión constante, que el hardware ejecuta en paralelo. El compilador HLSL extrae el paralelismo en un sombreador de casco y lo codifica en un código de bytes que impulsa el hardware.

-   La fase de punto de control funciona una vez para cada punto de control, leyendo los puntos de control de una revisión y generando un punto de control de salida (identificado por un ControlPointID).
-   La fase patch-constant funciona una vez por revisión para generar factores de teselación perimetral y otras constantes por revisión. Internamente, muchas fases de revisión constante se pueden ejecutar al mismo tiempo. La fase patch-constant tiene acceso de solo lectura a todos los puntos de control de entrada y salida.

Este es un ejemplo de un sombreador de casco:


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



Para obtener un ejemplo en el que se crea un sombreador de casco, [vea Cómo: Crear un sombreador de casco.](direct3d-11-advanced-stages-hull-shader-create.md)

### <a name="tessellator-stage"></a>Fase de teselador

El teselador es una fase de función fija inicializada mediante el enlace de un sombreador de casco a la canalización (vea Cómo: Inicializar la [fase tessellator).](direct3d-11-advanced-stages-tessellator-initialize.md) El propósito de la fase del teselador es subdividir un dominio (quad, tri o line) en muchos objetos más pequeños (triángulos, puntos o líneas). El teselador mosaico un dominio canónico en un sistema de coordenadas normalizado (de cero a uno). Por ejemplo, un dominio de cuatro se tesela a un cuadrado de unidad.

El teselador funciona una vez por revisión mediante los factores de teselación (que especifican el nivel de teselación del dominio) y el tipo de creación de particiones (que especifica el algoritmo usado para segmentar una revisión) que se pasan desde la fase del sombreador de casco. El teselador genera las coordenadas uv (y, opcionalmente, w) y la topología de superficie a la fase del sombreador de dominio.

Internamente, el teselador funciona en dos fases:

-   La primera fase procesa los factores de teselación, corrige problemas de redondeo, administra factores muy pequeños, reduce y combina factores mediante aritmética de punto flotante de 32 bits.
-   La segunda fase genera listas de puntos o topologías en función del tipo de creación de particiones seleccionado. Esta es la tarea principal de la fase del teselador y usa fracciones de 16 bits con aritmética de punto fijo. La aritmética de punto fijo permite la aceleración de hardware mientras se mantiene una precisión aceptable. Por ejemplo, dada una revisión de 64 metros de ancho, esta precisión puede colocar puntos con una resolución de 2 mm.



| Tipo de creación de particiones | Intervalo                       |
|----------------------|-----------------------------|
| fraccionamiento \_ impar      | \[1...63\]                  |
| fractional \_ even     | Intervalo de TessFactor: \[ 2..64\] |
| integer              | Intervalo de TessFactor: \[ 1..64\] |
| pow2                 | Intervalo de TessFactor: \[ 1..64\] |



 

### <a name="domain-shader-stage"></a>Domain-Shader fase

Un sombreador de dominio calcula la posición del vértice de un punto subdividido en la revisión de salida. Un sombreador de dominio se ejecuta una vez por punto de salida de fase de teselador y tiene acceso de solo lectura a las coordenadas UV de salida de la fase del teselador, la revisión de salida del sombreador de casco y las constantes de revisión de salida del sombreador de casco, como se muestra en el diagrama siguiente.

![diagrama de la fase de sombreador de dominio](images/d3d11-domain-shader.png)

Las propiedades del sombreador de dominio incluyen:

-   Un sombreador de dominio se invoca una vez por coordenada de salida desde la fase del teselador.
-   Un sombreador de dominio consume puntos de control de salida de la fase de sombreador de casco.
-   Un sombreador de dominio genera la posición de un vértice.
-   Las entradas son las salidas del sombreador de casco, incluidos los puntos de control, los datos constantes de revisión y los factores de teselación. Los factores de teselación pueden incluir los valores utilizados por el teselador de función fija, así como los valores sin procesar (antes de redondear por teselación de enteros, por ejemplo), lo que facilita la geomorfización, por ejemplo.

Una vez completado el sombreador de dominio, la teselación finaliza y los datos de canalización continúan en la siguiente fase de canalización (sombreador de geometría, sombreador de píxeles, etc.). Un sombreador de geometría que espera primitivas con adyacencia (por ejemplo, 6 vértices por triángulo) no es válido cuando la teselación está activa (esto da como resultado un comportamiento indefinido del que se quejan la capa de depuración).

Este es un ejemplo de un sombreador de dominio:


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

La teselación se implementa con dos nuevas fases programables del sombreador: un sombreador de casco y un sombreador de dominio. Estas nuevas fases del sombreador se programan con código HLSL que se define en el modelo de sombreador 5. Los nuevos destinos del sombreador son: hs \_ 5 \_ 0 y ds \_ 5 \_ 0. Al igual que todas las fases programables del sombreador, el código del hardware se extrae de los sombreadores compilados que se pasan al tiempo de ejecución cuando los sombreadores se enlazan a la canalización mediante API como [**DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader) y [**HSSetShader.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader) Pero en primer lugar, el sombreador debe crearse mediante API como [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader) y [**CreateDomainShader.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)

Habilite la teselación mediante la creación de un sombreador de casco y su enlace a la fase del sombreador de casco (esto configura automáticamente la fase del teselador). Para generar las posiciones finales de los vértices a partir de las revisiones teseladas, también deberá crear un sombreador de dominio y enlazarlo a la fase del sombreador de dominio. Una vez habilitada la teselación, la entrada de datos en la fase de ensamblador de entrada debe ser datos de revisión. Es decir, la topología del ensamblador de entrada debe ser una topología de constante de revisión de [**LA \_ TOPOLOGÍA \_ PRIMITIVA D3D11**](/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)) establecida con [**IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology).

Para deshabilitar la teselación, establezca el sombreador de casco y el sombreador de dominio en **NULL.** Ni la fase geometry-shader ni la fase stream-output pueden leer los puntos de control de salida del sombreador de casco ni los datos de revisión.

-   Nuevas topologías para la fase de ensamblador de entrada, que son extensiones de esta enumeración.

    ```
    enum D3D11_PRIMITIVE_TOPOLOGY
    ```

    

    La topología se establece en la fase de ensamblador de entrada [ **mediante IASetPrimitiveTopology.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology)

-   Por supuesto, las nuevas fases de sombreador programables requieren que se establezca otro estado para enlazar búferes constantes, ejemplos y recursos de sombreador a las fases de canalización adecuadas. Estos nuevos métodos ID3D11Device se implementan para establecer este estado.
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
| <span id="How_To__Create_a_Hull_Shader"></span><span id="how_to__create_a_hull_shader"></span><span id="HOW_TO__CREATE_A_HULL_SHADER"></span>[Cómo: Crear un sombreador de casco](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                                     | Cree un sombreador de casco.<br/>              |
| <span id="How_To__Design_a_Hull_Shader"></span><span id="how_to__design_a_hull_shader"></span><span id="HOW_TO__DESIGN_A_HULL_SHADER"></span>[Cómo: Diseñar un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                                     | Diseñar un sombreador de casco.<br/>              |
| <span id="How_To__Initialize_the_Tessellator_Stage"></span><span id="how_to__initialize_the_tessellator_stage"></span><span id="HOW_TO__INITIALIZE_THE_TESSELLATOR_STAGE"></span>[Cómo: Inicializar la fase del teselador](direct3d-11-advanced-stages-tessellator-initialize.md)<br/> | Inicialice la fase de teselación.<br/> |
| <span id="How_To__Create_a_Domain_Shader"></span><span id="how_to__create_a_domain_shader"></span><span id="HOW_TO__CREATE_A_DOMAIN_SHADER"></span>[Cómo: Crear un sombreador de dominio](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                                           | Cree un sombreador de dominio.<br/>            |
| <span id="How_To__Design_a_Domain_Shader"></span><span id="how_to__design_a_domain_shader"></span><span id="HOW_TO__DESIGN_A_DOMAIN_SHADER"></span>[Cómo: Diseñar un sombreador de dominio](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                                           | Cree un sombreador de dominio.<br/>            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> </dl>

 


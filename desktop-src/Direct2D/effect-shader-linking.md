---
title: Vinculación del sombreador de efectos
description: Direct2D usa una optimización denominada vinculación del sombreador de efectos que combina varios pases de representación de gráfico de efecto en un solo paso.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608ae0b751840fc32b31e10012eb343c73ec3e0d941a26477a192b576204c247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431464"
---
# <a name="effect-shader-linking"></a>Vinculación del sombreador de efectos

Direct2D usa una optimización denominada vinculación del sombreador de efectos que combina varios pases de representación de gráfico de efecto en un solo paso.

-   [Información general sobre la vinculación del sombreador de efectos](#overview-of-effect-shader-linking)
-   [Usar la vinculación del sombreador de efectos](#using-effect-shader-linking)
-   [Creación de un efecto personalizado compatible con la vinculación de sombreador](#authoring-a-shader-linking-compatible-custom-effect)
-   [Sombreador de efectos compatible con la vinculación de ejemplo](#example-linking-compatible-effect-shader)
-   [Compilación de un sombreador compatible de vinculación](#compiling-a-linking-compatible-shader)
    -   [Paso 1: Compilación de la función de exportación](#step-1-compile-the-export-function)
    -   [Paso 2: Compilación del sombreador completo e inserción de la función de exportación](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [Exportar especificaciones de función](#export-function-specifications)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>Información general sobre la vinculación del sombreador de efectos

Las optimizaciones de vinculación del sombreador de efectos se basa en la vinculación del sombreador HLSL, una característica de Direct3D 11.2 que permite generar sombreadores de píxeles y vértices en tiempo de ejecución mediante la vinculación de funciones de sombreador compiladas previamente. Las siguientes figuras ilustran el concepto de vinculación del sombreador de efectos en un gráfico de efectos. En la primera ilustración se muestra un gráfico de efectos de Direct2D típico con cuatro transformaciones de representación. Sin la vinculación del sombreador, cada transformación consume un paso de representación y requiere una superficie intermedia; en total, este gráfico requiere 4 pases y 3 intermedios.

![transformar gráfico sin vinculación de sombreador: 4 pases y 3 intermedios.](images/shader-transform-graph.png)

En la segunda ilustración se muestra el mismo gráfico de efecto en el que cada transformación de representación se ha reemplazado por una versión de función enlazable. Direct2D puede vincular todo el gráfico y ejecutarlo en un solo paso sin necesidad de ningún intermedio. Esto puede proporcionar una disminución significativa en el tiempo de ejecución de GPU y una reducción en el consumo máximo de memoria de GPU.

![transformar gráfico con vinculación de sombreador: 1 paso, 0 intermedios.](images/shader-linking-graph.png)



 

La vinculación del sombreador de efectos funciona en transformaciones individuales dentro de un efecto; Esto significa que incluso un gráfico con un único efecto puede beneficiarse de la vinculación del sombreador si ese efecto tiene varias transformaciones válidas.

## <a name="using-effect-shader-linking"></a>Usar la vinculación del sombreador de efectos

Si va a compilar una aplicación de Direct2D que usa efectos, no es necesario hacer nada para aprovechar la vinculación del sombreador de efectos. Direct2D analiza automáticamente el gráfico de efectos para determinar la manera más óptima de vincular cada transformación.

Los autores de efectos son responsables de implementar su efecto de forma que admita la vinculación del sombreador de efectos. Para obtener más información, vea la sección Creación de un efecto personalizado compatible con [la vinculación](#authoring-a-shader-linking-compatible-custom-effect) de sombreador a continuación. Todos los efectos integrados admiten la vinculación del sombreador.

Direct2D solo vinculará transformaciones de representación adyacentes en situaciones en las que sea beneficioso. Tiene en cuenta varios factores a la hora de determinar si se vinculan dos transformaciones. Por ejemplo, la vinculación del sombreador no se realiza si una de las transformaciones usa sombreadores de vértices o de proceso, ya que solo se pueden vincular sombreadores de píxeles. Además, si no se ha creado un efecto para que sea compatible con la vinculación del sombreador, las transformaciones circundantes no se vincularán con él.

En caso de que exista un riesgo de vinculación de este tipo, Direct2D no vinculará ninguna transformación adyacente al peligro, sino que intentará vincular el resto del gráfico.

![transformar gráfico con un peligro de vinculación: 2 pases, 1 intermedio.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Creación de un efecto personalizado compatible con la vinculación de sombreador

Si va a crear su propio efecto personalizado de Direct2D, debe asegurarse de que sus transformaciones admiten la vinculación del sombreador de efectos. Esto requiere algunos cambios menores de la forma en que se implementaron los efectos personalizados anteriores. Si una transformación dentro del efecto personalizado no admite la vinculación del sombreador, Direct2D no la vinculará con ninguna transformación adyacente a ella en el gráfico de efectos.

Como autor de efectos personalizados, debe tener en cuenta varios conceptos y requisitos clave:

-   **No hay cambios en las implementaciones de interfaz de efecto**

    No es necesario modificar ningún código que implemente las distintas interfaces de efecto, [como ID2D1DrawTransform.](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)

-   **Proporcionar una versión de función completa y de exportación de sombreadores**

    Debe proporcionar una versión de función de exportación de los sombreadores del efecto que Direct2D puede vincular. Además, también debe seguir proporcionando el sombreador completo original; Esto se debe a que Direct2D selecciona en tiempo de ejecución la versión correcta del sombreador en función de si la vinculación del sombreador se va a aplicar a un vínculo determinado del gráfico.

    Si una transformación solo proporciona el blob de sombreador de píxeles completo (a través de [ID2D1EffectContext::LoadPixelShader),](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)no se vinculará a transformaciones adyacentes.

- **Funciones auxiliares**

    Direct2D proporciona macros y funciones auxiliares [HLSL](hlsl-helpers.md) que generarán automáticamente las versiones de función completa y de exportación de un sombreador. Estos asistentes se pueden encontrar en d2d1effecthelpers.hlsli. Además, el compilador HLSL (FXC) permite insertar el sombreador de funciones de exportación en un campo privado en el sombreador completo. De este modo, solo necesita crear un sombreador una vez y pasar ambas versiones a Direct2D simultáneamente. Tanto d2d1effecthelpers.hlsli como el compilador de FXC se incluyen como parte del SDK de Windows.

    Las funciones auxiliares:

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [D2D \_ PS \_ ENTRY](d2d-ps-entry.md)  

  También puede crear manualmente dos versiones de cada sombreador y compilarlas dos veces, siempre y cuando se cumplen las especificaciones descritas a continuación en [Exportar](#export-function-specifications) especificaciones de función.

-   **Solo sombreadores de píxeles**

    Direct2D no admite la vinculación de sombreadores de vértices o proceso. Sin embargo, si el efecto usa un sombreador de vértices y píxeles, la salida del sombreador de píxeles todavía se puede vincular.

-   **Muestreo simple frente a complejo**

    La vinculación de funciones de sombreador funciona conectando la salida de un paso de sombreador de píxeles a la entrada de un paso posterior del sombreador de píxeles. Esto solo es posible cuando el sombreador de píxeles de consumo solo requiere un valor de entrada único para realizar su cálculo; Este valor normalmente procedería del muestreo de una textura de entrada en la coordenada de textura emitida por el sombreador de vértices. Se dice que este sombreador de píxeles realiza un muestreo simple.

    ![La conversión de escala de grises es un ejemplo de muestreo simple. El valor de un píxel de salida determinado depende solo del valor del píxel de entrada correspondiente.](images/simple-sampling.png)

    Algunos sombreadores de píxeles, como un desenfoque gaussiano, calculan su salida a partir de varias muestras de entrada en lugar de una sola muestra. Se dice que este sombreador de píxeles realiza un muestreo complejo.

    

    ![El desenfoque gaussiano es un ejemplo de muestreo complejo. El valor del píxel de salida central depende de varios píxeles de entrada.](images/complex-sampling.png)

    
    Solo las funciones de sombreador con entradas simples pueden tener su entrada proporcionada por otra función de sombreador. Las funciones de sombreador con entradas complejas deben proporcionarse con una textura de entrada para muestrear. Esto significa que Direct2D no vinculará un sombreador con entradas complejas a su predecesor.

    Al usar los [asistentes HLSL de Direct2D,](hlsl-helpers.md)debe indicar en hlsl si un sombreador usa entradas complejas o sencillas.

## <a name="example-linking-compatible-effect-shader"></a>Sombreador de efecto compatible con la vinculación de ejemplo

Con los asistentes D2D, el siguiente fragmento de código representa un sombreador de efectos compatible con la vinculación simple:

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

En este breve ejemplo, tenga en cuenta que no se declara ningún parámetro de función, que el número de entradas y el tipo de cada entrada se declara antes que la función de entrada, la entrada se recupera mediante una llamada a [D2DGetInput](d2dgetinput.md)y que las directivas de preprocesador deben definirse antes de que se incluya el archivo auxiliar.

Un sombreador compatible con la vinculación debe proporcionar un sombreador de píxeles de un solo paso normal y una función de sombreador de exportación. La [macro D2D \_ PS \_ ENTRY](d2d-ps-entry.md) permite generar cada uno de ellos a partir del mismo código, cuando se usa junto con el script de compilación del sombreador.

Al compilar un sombreador completo, las macros se expanden en el código siguiente, que tiene una firma de entrada compatible con efectos D2D.

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

Al compilar una versión de función de exportación del mismo código, se genera el código siguiente:

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

Tenga en cuenta que la entrada de textura, recuperada normalmente mediante el muestreo de texture2D, se ha reemplazado por una entrada de función (input0).

Para ver una descripción completa paso a paso de lo que debe hacer para escribir un efecto compatible con la vinculación, consulte el [tutorial](custom-effects.md) de efectos personalizados y el ejemplo de efectos de imagen personalizados de [Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

## <a name="compiling-a-linking-compatible-shader"></a>Compilación de un sombreador compatible de vinculación

Para poder vincularse, el blob de sombreador de píxeles pasado a D2D debe contener las versiones de función completa y de exportación del sombreador. Esto se logra insertando la función de exportación compilada en el área D3D \_ BLOB \_ PRIVATE \_ DATA.

Cuando los sombreadores se han creado con las funciones auxiliares D2D, se debe definir un destino de compilación D2D en tiempo de compilación. Los tipos de destino de compilación son \_ D2D FULL SHADER y \_ D2D \_ FUNCTION.

La compilación de un sombreador de efectos compatible con la vinculación es un proceso de dos pasos:

-   [Compilación de la función de exportación](#step-1-compile-the-export-function)
-   [Compilación del sombreador completo e inserción de la función de exportación](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> Al compilar un efecto mediante Visual Studio, debe crear un archivo por lotes que ejecute ambos comandos FXC y ejecutar este archivo por lotes como un paso de compilación personalizado que se ejecuta antes del paso de compilación.

 

### <a name="step-1-compile-the-export-function"></a>Paso 1: Compilación de la función de exportación

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Para compilar la versión de la función de exportación del sombreador, debe pasar las marcas siguientes a FXC.



|    Marca                            |    Descripción                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /t <ShaderModel>         | Establezca <ShaderModel> en el perfil de sombreador de píxeles adecuado tal como se define en [Sintaxis de FXC.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) Debe ser uno de los perfiles enumerados en "Vinculación del sombreador HLSL". |
| <MyShaderFile>.hlsl      | Establezca <MyShaderFile> en el nombre del archivo HLSL.                                                                                                                                                                                                    |
| /D D D2D \_ (FUNCIÓN)               | Esta definición indica a FXC que compile la versión de la función de exportación del sombreador.                                                                                                                                                                       |
| /D D D2D \_ ENTRY=<entry>    | Establezca <entry> en el nombre del punto de entrada HLSL que definió dentro de la macro [ \_ D2D PS \_ ENTRY.](d2d-ps-entry.md)                                                                                                                                    |
| /Fl <MyShaderFile> .fxlib | Establezca <MyShaderfile> en donde desea almacenar la versión de la función de exportación del sombreador. Tenga en cuenta que la extensión .fxlib solo es para facilitar la identificación.                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Paso 2: Compilación del sombreador completo e inserción de la función de exportación

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Para compilar la versión completa del sombreador con la versión de exportación insertada, debe pasar las marcas siguientes a FXC.



|    Marca                                    |    Descripción                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /t <ShaderModel>                 | Establezca <ShaderModel> en el perfil de sombreador de píxeles adecuado tal como se define en [Sintaxis de FXC.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) Debe ser el perfil del sombreador de píxeles correspondiente al perfil de vinculación especificado en el paso 1. |
| <MyShaderFile>.hlsl              | Establezca <MyShaderFile> en el nombre del archivo HLSL.                                                                                                                                                                                                                               |
| SOMBREADOR COMPLETO /D \_ D2D \_                   | Esta definición indica a FXC que compile la versión completa del sombreador.                                                                                                                                                                                                             |
| /D D D2D \_ ENTRY=<entry>            | Establezca <entry> en el nombre del punto de entrada HLSL que definió dentro de la macro D2D PS \_ \_ ENTRY().                                                                                                                                                                                 |
| /e <entry>                       | Establezca <entry> en el nombre del punto de entrada HLSL que definió dentro de la macro D2D PS \_ \_ ENTRY().                                                                                                                                                                                 |
| /setprivate <MyShaderFile> .fxlib | Este argumento indica a FXC que inserte el sombreador de funciones de exportación generado en el paso 1 en el área D3D \_ BLOB \_ PRIVATE \_ DATA.                                                                                                                                                          |
| /Fo <MyShader> .cso               | Establezca <MyShader> en donde desea almacenar el sombreador compilado combinado final.                                                                                                                                                                                                 |
| /Fh <MyShader> .h                 | Establezca <MyShader> en donde desea almacenar el encabezado combinado final.                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a>Exportar especificaciones de función

Aunque no se recomienda, es posible crear un sombreador de efectos compatible sin usar los asistentes proporcionados por D2D. Debe tener cuidado para asegurarse de que tanto el sombreador completo como las firmas de entrada de la función de exportación se ajustan a las especificaciones de D2D.

Las especificaciones de los sombreadores completos son las mismas que las Windows anteriores. Brevemente, los parámetros de entrada del sombreador de píxeles deben ser SV POSITION, SCENE POSITION y \_ una entrada DE \_ TEXASCOORD por efecto.

Para la función de exportación, la función debe devolver float4 y sus entradas deben ser de uno de los tipos siguientes:

-   Entrada simple

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    Para entradas sencillas, D2D insertará una función Sample entre la textura de entrada y la función de sombreador, o bien la entrada la proporciona la salida de otra función de sombreador.

-   Entrada compleja

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    En el caso de las entradas complejas, D2D solo pasará una coordenada de textura como se describe en Windows 8 documentación.

-   Ubicación de salida

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    Solo se puede \_ definir una entrada SCENE POSITION. Este parámetro solo debe incluirse cuando sea necesario, ya que solo una función por sombreador vinculado puede utilizar este parámetro.

La semántica debe definirse como se ha indicado anteriormente, ya que D2D inspeccionará la semántica para decidir cómo vincular funciones entre sí. Si alguna entrada de función no coincide con uno de los tipos anteriores, la función se rechazará para la vinculación del sombreador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asistentes hlsl](hlsl-helpers.md)
</dt> <dt>

[Interfaz ID3D11Linker](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[Interfaz ID3D11FunctionLinkingGraph](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 
---
title: Vinculación del sombreador de efectos
description: Direct2D usa una optimización denominada vinculación de sombreador de efectos que combina varios pasos de representación de gráficos de efectos en un solo paso.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a17691346649b2ddcde7ca4f3e343be6a35a90
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361949"
---
# <a name="effect-shader-linking"></a>Vinculación del sombreador de efectos

Direct2D usa una optimización denominada vinculación de sombreador de efectos que combina varios pasos de representación de gráficos de efectos en un solo paso.

-   [Información general sobre la vinculación de sombreador de efectos](#overview-of-effect-shader-linking)
-   [Usar la vinculación del sombreador de efectos](#using-effect-shader-linking)
-   [Creación de un efecto personalizado compatible con la vinculación del sombreador](#authoring-a-shader-linking-compatible-custom-effect)
-   [Sombreador de efectos compatible con la vinculación de ejemplo](#example-linking-compatible-effect-shader)
-   [Compilar un sombreador compatible con vinculador](#compiling-a-linking-compatible-shader)
    -   [Paso 1: compilar la función de exportación](#step-1-compile-the-export-function)
    -   [Paso 2: compilar el sombreador completo e incrustar la función de exportación](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [Especificaciones de la función de exportación](#export-function-specifications)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>Información general sobre la vinculación de sombreador de efectos

Las optimizaciones de vinculación del sombreador de efectos se basan en la vinculación del sombreador de HLSL, una característica de Direct3D 11,2 que permite generar sombreadores de píxeles y vértices en tiempo de ejecución mediante la vinculación de funciones de sombreador previamente compiladas. Las siguientes figuras ilustran el concepto de vinculación de sombreador de efectos en un gráfico de efectos. En la primera ilustración se muestra un gráfico de efecto de Direct2D típico con cuatro transformaciones de representación. Sin la vinculación del sombreador, cada transformación consume un paso de representación y requiere una superficie intermedia; en total, este gráfico requiere 4 pasos y 3 intermedios.



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![transformar gráfico sin vinculación del sombreador: 4 pasos y 3 intermedios.](images/shader-transform-graph.png) |



 

En la segunda ilustración se muestra el mismo gráfico de efectos en el que cada transformación de representación se ha reemplazado por una versión de función vinculable. Direct2D es capaz de vincular todo el grafo y ejecutarlo en un solo paso sin necesidad de ningún medio. Esto puede proporcionar una disminución significativa en el tiempo de ejecución de la GPU y la reducción del consumo de memoria máxima de la GPU.



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![transformar gráfico con vinculación del sombreador: 1 paso, 0 intermedio.](images/shader-linking-graph.png) |



 

La vinculación de sombreador de efectos funciona en transformaciones individuales dentro de un efecto; Esto significa que incluso un gráfico con un solo efecto puede beneficiarse de la vinculación del sombreador si ese efecto tiene varias transformaciones válidas.

## <a name="using-effect-shader-linking"></a>Usar la vinculación del sombreador de efectos

Si va a compilar una aplicación de Direct2D que usa efectos, no es necesario hacer nada para aprovechar las ventajas de la vinculación del sombreador de efectos. Direct2D analiza automáticamente el gráfico de efectos para determinar la forma más óptima de vincular cada transformación.

Los autores de efectos son responsables de implementar su efecto de forma que admita la vinculación del sombreador de efectos; para obtener más información, consulte la sección [creación de un efecto personalizado compatible con la vinculación del sombreador](#authoring-a-shader-linking-compatible-custom-effect) a continuación. Todos los efectos integrados admiten la vinculación de sombreador.

Direct2D solo vinculará las transformaciones de representación adyacentes en situaciones en las que sea beneficioso. Tiene en cuenta varios factores a la hora de determinar si se deben vincular dos transformaciones. Por ejemplo, la vinculación del sombreador no se realiza si una de las transformaciones utiliza los sombreadores de vértices o de cálculo, ya que solo se pueden vincular los sombreadores de píxeles. Además, si no se ha creado un efecto para ser compatible con la vinculación del sombreador, las transformaciones circundantes no se vincularán con él.

En el caso de que exista un riesgo de vinculación de este tipo, Direct2D no vinculará las transformaciones adyacentes al riesgo, sino que seguirá intentando vincular el resto del gráfico.



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![transformar gráfico con un riesgo de vinculación: 2 pasos, 1 intermedio.](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Creación de un efecto personalizado compatible con la vinculación del sombreador

Si va a crear su propio efecto de Direct2D personalizado, debe asegurarse de que sus transformaciones admiten la vinculación del sombreador de efectos. Esto requiere algunos cambios menores de cómo se implementaron los efectos personalizados anteriores. Si una transformación dentro de su efecto personalizado no admite la vinculación del sombreador, Direct2D no lo vinculará con las transformaciones adyacentes a ella en el gráfico de efectos.

Como autor de un efecto personalizado, debe tener en cuenta varios conceptos y requisitos clave:

-   **No hay cambios en las implementaciones de interfaz de efecto**

    No es necesario modificar ningún código que implemente las diversas interfaces de efectos, como [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).

-   **Proporcionar una versión de función completa y de exportación de los sombreadores**

    Debe proporcionar una versión de función de exportación de los sombreadores de su efecto, que son vinculables por Direct2D. Además, también debe seguir proporcionando el sombreador completo original; Esto se debe a que Direct2D selecciona en tiempo de ejecución la versión correcta del sombreador, en función de si la vinculación del sombreador se va a aplicar a un vínculo determinado del gráfico.

    Si una transformación solo proporciona el BLOB del sombreador de píxeles completo (a través de [ID2D1EffectContext:: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), no se vinculará a las transformaciones adyacentes.

- **Funciones auxiliares**

    Direct2D proporciona [funciones](hlsl-helpers.md) y macros auxiliares de HLSL que generarán automáticamente las versiones de función completa y de exportación de un sombreador. Estas aplicaciones auxiliares se pueden encontrar en d2d1effecthelpers. hlsli. Además, el compilador de HLSL (FXC) permite insertar el sombreador de funciones de exportación en un campo privado en el sombreador completo. De esta manera, solo tiene que crear un sombreador una vez y pasar ambas versiones a Direct2D simultáneamente. Tanto d2d1effecthelpers. hlsli como el compilador FXC se incluyen como parte de la Windows SDK.

    Las funciones auxiliares:

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [Entrada de D2D \_ PS \_](d2d-ps-entry.md)  

  También puede crear manualmente dos versiones de cada sombreador y compilarlas dos veces, siempre y cuando se cumplan las especificaciones descritas a continuación en especificaciones de la [función de exportación](#export-function-specifications) .

-   **Solo sombreadores de píxeles**

    Direct2D no admite la vinculación de sombreadores de cálculo o de vértices. Sin embargo, si el efecto usa un sombreador de vértices y píxeles, la salida del sombreador de píxeles todavía se puede vincular.

-   **Muestreo simple frente a complejo**

    La vinculación de la función de sombreador funciona conectando la salida de un sombreador de píxeles pasando a la entrada de una fase del sombreador de píxeles subsiguiente. Esto solo es posible cuando el sombreador de píxeles de consumo requiere un solo valor de entrada para realizar su cálculo; Normalmente, este valor proviene del muestreo de una textura de entrada en la coordenada de textura emitida por el sombreador de vértices. Se dice que este sombreador de píxeles realiza un muestreo sencillo.

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![la conversión de escala de grises es un ejemplo de muestreo sencillo. el valor de un píxel de salida determinado depende solo del valor del píxel de entrada correspondiente.](images/simple-sampling.png) |

    

     

    Algunos sombreadores de píxeles, como un desenfoque gaussiano, calculan la salida de varios ejemplos de entrada en lugar de un solo ejemplo. Se dice que este sombreador de píxeles realiza un muestreo complejo.

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![Desenfoque gaussiano es un ejemplo de muestreo complejo. el valor del píxel de salida central depende de varios píxeles de entrada.](images/complex-sampling.png) |

    

     

    Solo las funciones de sombreador con entradas simples pueden tener su entrada proporcionada por otra función de sombreador. Las funciones de sombreador con entradas complejas se deben proporcionar con una textura de entrada para muestrear. Esto significa que Direct2D no vinculará un sombreador con entradas complejas a su predecesor.

    Al usar las [aplicaciones auxiliares de HLSL para Direct2D](hlsl-helpers.md), debe indicar en HLSL si un sombreador usa entradas simples o complejas.

## <a name="example-linking-compatible-effect-shader"></a>Sombreador de efectos compatible con la vinculación de ejemplo

Con las aplicaciones auxiliares de D2D, el siguiente fragmento de código representa un sombreador de efectos sencillo compatible con la vinculación:

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

En este breve ejemplo, observe que no se declara ningún parámetro de función, que el número de entradas y el tipo de cada entrada se declara antes que la función de entrada, la entrada se recupera llamando a [D2DGetInput](d2dgetinput.md)y que se deben definir las directivas de preprocesador antes de que se incluya el archivo auxiliar.

Un sombreador compatible con vinculación debe proporcionar un sombreador de píxeles de paso único normal y una función de sombreador de exportación. La macro [D2D \_ PS \_ entry](d2d-ps-entry.md) permite que cada una de ellas se genere a partir del mismo código, cuando se usa junto con el script de compilación del sombreador.

Al compilar un sombreador completo, las macros se expanden en el código siguiente, que tiene una firma de entrada compatible con efectos de D2D.

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

Tenga en cuenta que la entrada de textura, que normalmente se recupera mediante el muestreo de un Texture2D, se ha reemplazado por una entrada de función (input0).

Para ver una descripción completa y paso a paso de lo que debe hacer para escribir un efecto compatible con la vinculación, vea el [tutorial de efectos personalizados](custom-effects.md) y el [ejemplo de efectos de imagen personalizados de Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

## <a name="compiling-a-linking-compatible-shader"></a>Compilar un sombreador compatible con vinculador

Para que sea vinculable, el BLOB del sombreador de píxeles pasado a D2D debe contener las versiones de función Full y Export del sombreador. Esto se logra mediante la incrustación de la función de exportación compilada en el \_ área de datos privados del BLOB D3D \_ \_ .

Cuando los sombreadores se crean con las funciones auxiliares de D2D, se debe definir un destino de compilación D2D en el momento de la compilación. Los tipos de destino de compilación son D2D \_ Full \_ Shader y D2D \_ function.

La compilación de un sombreador de efectos compatible con la vinculación es un proceso de dos pasos:

-   [Compilar la función de exportación](#step-1-compile-the-export-function)
-   [Compilar el sombreador completo e incrustar la función de exportación](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> Al compilar un efecto con Visual Studio, debe crear un archivo por lotes que ejecute ambos comandos de FXC y ejecutar este archivo por lotes como un paso de compilación personalizado que se ejecuta antes del paso de compilación.

 

### <a name="step-1-compile-the-export-function"></a>Paso 1: compilar la función de exportación

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Para compilar la versión de la función de exportación del sombreador, debe pasar las siguientes marcas a FXC.



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Marca**                       | **Descripción**                                                                                                                                                                                                                                           |
| /T <ShaderModel>         | Establezca <ShaderModel> en el perfil de sombreador de píxeles adecuado tal y como se define en la [Sintaxis de FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Debe ser uno de los perfiles que aparecen en "vinculación del sombreador de HLSL". |
| <MyShaderFile>. HLSL      | Establezca <MyShaderFile> en el nombre del archivo HLSL.                                                                                                                                                                                                    |
| /D D2D \_ función)               | Esta definición indica a FXC que compile la versión de la función de exportación del sombreador.                                                                                                                                                                       |
| /D D2D \_ entry =<entry>    | Establezca <entry> en el nombre del punto de entrada de HLSL que ha definido en la macro [D2D \_ PS \_ entry](d2d-ps-entry.md) .                                                                                                                                    |
| /FL <MyShaderFile> . fxlib | Establezca <MyShaderfile> en dónde desea almacenar la versión de la función de exportación del sombreador. Tenga en cuenta que la extensión. fxlib solo es para facilitar la identificación.                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Paso 2: compilar el sombreador completo e incrustar la función de exportación

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Para compilar la versión completa del sombreador con la versión de exportación incrustada, debe pasar las siguientes marcas a FXC.



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Marca**                               | **Descripción**                                                                                                                                                                                                                                                                      |
| /T <ShaderModel>                 | Establezca <ShaderModel> en el perfil de sombreador de píxeles adecuado tal y como se define en la [Sintaxis de FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Debe ser el perfil de sombreador de píxeles correspondiente al perfil de vinculación especificado en el paso 1. |
| <MyShaderFile>. HLSL              | Establezca <MyShaderFile> en el nombre del archivo HLSL.                                                                                                                                                                                                                               |
| D2Dr/d ( \_ \_ sombreador completo)                   | Esta definición indica a FXC que compile la versión completa del sombreador.                                                                                                                                                                                                             |
| /D D2D \_ entry =<entry>            | Establezca <entry> en el nombre del punto de entrada de HLSL que ha definido dentro de la \_ macro D2D PS \_ entry ().                                                                                                                                                                                 |
| /E <entry>                       | Establezca <entry> en el nombre del punto de entrada de HLSL que ha definido dentro de la \_ macro D2D PS \_ entry ().                                                                                                                                                                                 |
| /setprivate <MyShaderFile> . fxlib | Este argumento indica a FXC que inserte el sombreador de la función de exportación generado en el paso 1 en el \_ área de datos privados del BLOB D3D \_ \_ .                                                                                                                                                          |
| /FO <MyShader> . CSO               | Establezca <MyShader> en dónde desea almacenar el sombreador compilado final combinado.                                                                                                                                                                                                 |
| /FH <MyShader> . h                 | Establezca <MyShader> en dónde desea almacenar el encabezado combinado final.                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a>Especificaciones de la función de exportación

Aunque no se recomienda, es posible crear un sombreador de efectos compatible sin usar las aplicaciones auxiliares proporcionadas por D2D. Se debe tener cuidado para asegurarse de que las firmas de entrada de la función de exportación y el sombreador completo cumplen con las especificaciones de D2D.

Las especificaciones de los sombreadores completos son las mismas que las versiones anteriores de Windows. Brevemente, los parámetros de entrada del sombreador de píxeles deben ser la \_ posición de la VP, la \_ posición de la escena y una TEXCOORD por entrada de efecto.

Para la función de exportación, la función debe devolver FLOAT4 y sus entradas deben ser de uno de los tipos siguientes:

-   Entrada simple

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    En el caso de las entradas simples, D2D insertará una función de ejemplo entre la textura de entrada y la función de sombreador, o bien la salida de otra función de sombreador proporcionará la entrada.

-   Entrada compleja

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    En el caso de las entradas complejas, D2D solo pasará una coordenada de textura, como se describe en la documentación de Windows 8.

-   Ubicación de salida

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    Solo \_ se puede definir una entrada de posición de la escena. Este parámetro solo debe incluirse cuando sea necesario, ya que solo una función por cada sombreador vinculado puede utilizar este parámetro.

La semántica debe definirse como se indicó anteriormente, ya que D2D inspeccionará la semántica para decidir cómo vincular las funciones entre sí. Si alguna entrada de función no coincide con uno de los tipos anteriores, se rechazará la función para la vinculación del sombreador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones auxiliares de HLSL](hlsl-helpers.md)
</dt> <dt>

[Interfaz ID3D11Linker](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[Interfaz ID3D11FunctionLinkingGraph](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 
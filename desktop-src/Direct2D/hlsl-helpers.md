---
title: Aplicaciones auxiliares de HLSL
description: Para ayudar a los autores de efectos a escribir sombreadores de píxeles vinculables, d2d1effecthelpers. hlsli define un conjunto de extensiones de lenguaje HLSL en forma de métodos auxiliares y macros.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993994"
---
# <a name="hlsl-helpers"></a>Aplicaciones auxiliares de HLSL

Para ayudar a los autores de efectos a escribir sombreadores de píxeles vinculables, d2d1effecthelpers. hlsli define un conjunto de extensiones de lenguaje HLSL en forma de métodos auxiliares y macros.

Para agregar d2d1effecthelpers. hlsli al proyecto, agregue una \# instrucción include en el archivo HLSL. d2d1effecthelpers. hlsli se encuentra en la misma ubicación que otros encabezados de Direct2D como d2d1. h; se puede hacer referencia a ella desde la página de propiedades del archivo HLSL agregando la macro $ (WindowsSDK \_ IncludePath) a la propiedad directorios de inclusión adicionales. Tenga en cuenta que la \# instrucción include debe aparecer después de que se hayan definido las directivas de preprocesador como \_ recuento de entrada D2D \_ .

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D no admite la vinculación de sombreadores de cálculo o de vértices. Sin embargo, si el efecto usa un sombreador de vértices y un sombreador de píxeles, la salida del sombreador de píxeles todavía se puede vincular.

## <a name="preprocessor-directives"></a>Directivas de preprocesador

Las directivas de preprocesador son necesarias para comunicar información sobre el efecto. Esto incluye el número de entradas y el tipo de muestreo de cada entrada. Los valores siguientes se deben definir en el código del sombreador de efectos sobre el punto de entrada del sombreador pertinente cuando sea aplicable.

-   `D2D_INPUT_COUNT <N>` : Declara el número de entradas de textura al efecto. Si el efecto tiene un número variable de entradas, este valor se debe limitar correctamente a cada punto de entrada del sombreador. La definición de este valor es obligatoria.
-   `D2D_INPUT<N>_SIMPLE` : Declara la entrada nth para usar el muestreo simple. Si no se define, la entrada nth tiene como valor predeterminado Complex. La definición de este valor es opcional.
-   `D2D_INPUT<N>_COMPLEX` : Declara la entrada nth para usar el muestreo complejo. Si no se define, la entrada nth tiene como valor predeterminado Complex. La definición de este valor es opcional.
-   `D2D_REQUIRES_SCENE_POSITION` : Indica que la función de sombreador llama a métodos auxiliares que usan el valor de posición de la escena (es decir, la función auxiliar [D2DGetScenePosition](d2dgetsceneposition.md) ). Este parámetro solo debe incluirse cuando sea necesario, ya que solo una función por cada sombreador vinculado puede utilizar este parámetro. La definición de este valor es opcional.
-   `D2D_CUSTOM_ENTRY` : Indica que la función de sombreador de píxeles consume la salida de un sombreador de vértices personalizado y, por lo tanto, declarará sus parámetros de entrada. Todas las entradas personalizadas del sombreador de vértices usan un muestreo complejo y no pueden consumir la salida de otra función de sombreador (es decir, solo se pueden vincular). La definición de este valor es opcional.

Por ejemplo:

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>Funciones del asistente

Las funciones auxiliares se usan como reemplazo para algunas funciones intrínsecas de HLSL nativas. En tiempo de compilación, las funciones auxiliares se redefinen mediante Direct2D en la versión adecuada según el tipo de destino de compilación (sombreador completo o función de exportación).

Las funciones auxiliares:

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[Entrada de D2D \_ PS \_](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vinculación del sombreador de efectos](effect-shader-linking.md)
</dt> </dl>

 

 





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
# <a name="hlsl-helpers"></a><span data-ttu-id="a460f-103">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="a460f-103">HLSL Helpers</span></span>

<span data-ttu-id="a460f-104">Para ayudar a los autores de efectos a escribir sombreadores de píxeles vinculables, d2d1effecthelpers. hlsli define un conjunto de extensiones de lenguaje HLSL en forma de métodos auxiliares y macros.</span><span class="sxs-lookup"><span data-stu-id="a460f-104">To assist effect authors in writing linkable pixel shaders, d2d1effecthelpers.hlsli defines a set of HLSL language extensions in the form of helper methods and macros.</span></span>

<span data-ttu-id="a460f-105">Para agregar d2d1effecthelpers. hlsli al proyecto, agregue una \# instrucción include en el archivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="a460f-105">To add d2d1effecthelpers.hlsli to your project, add an \#include statement in the HLSL file.</span></span> <span data-ttu-id="a460f-106">d2d1effecthelpers. hlsli se encuentra en la misma ubicación que otros encabezados de Direct2D como d2d1. h; se puede hacer referencia a ella desde la página de propiedades del archivo HLSL agregando la macro $ (WindowsSDK \_ IncludePath) a la propiedad directorios de inclusión adicionales.</span><span class="sxs-lookup"><span data-stu-id="a460f-106">d2d1effecthelpers.hlsli is located in the same location as other Direct2D headers such as d2d1.h; it can be referenced from the HLSL file's property page by adding the macro $(WindowsSDK\_IncludePath) to the Additional Include Directories property.</span></span> <span data-ttu-id="a460f-107">Tenga en cuenta que la \# instrucción include debe aparecer después de que se hayan definido las directivas de preprocesador como \_ recuento de entrada D2D \_ .</span><span class="sxs-lookup"><span data-stu-id="a460f-107">Note that the \#include statement must come after any preprocessor directives such D2D\_INPUT\_COUNT have been defined.</span></span>

``` syntax
#include <d2d1effecthelpers.hlsli>
```

<span data-ttu-id="a460f-108">Direct2D no admite la vinculación de sombreadores de cálculo o de vértices.</span><span class="sxs-lookup"><span data-stu-id="a460f-108">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="a460f-109">Sin embargo, si el efecto usa un sombreador de vértices y un sombreador de píxeles, la salida del sombreador de píxeles todavía se puede vincular.</span><span class="sxs-lookup"><span data-stu-id="a460f-109">However, if your effect uses both a vertex shader and pixel shader, the output of the pixel shader can still be linked.</span></span>

## <a name="preprocessor-directives"></a><span data-ttu-id="a460f-110">Directivas de preprocesador</span><span class="sxs-lookup"><span data-stu-id="a460f-110">Preprocessor Directives</span></span>

<span data-ttu-id="a460f-111">Las directivas de preprocesador son necesarias para comunicar información sobre el efecto.</span><span class="sxs-lookup"><span data-stu-id="a460f-111">Preprocessor directives are required to communicate information about the effect.</span></span> <span data-ttu-id="a460f-112">Esto incluye el número de entradas y el tipo de muestreo de cada entrada.</span><span class="sxs-lookup"><span data-stu-id="a460f-112">This includes the number of inputs and sampling type of each input.</span></span> <span data-ttu-id="a460f-113">Los valores siguientes se deben definir en el código del sombreador de efectos sobre el punto de entrada del sombreador pertinente cuando sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="a460f-113">The following values should be defined in the effect shader code above the relevant shader entry point when applicable.</span></span>

-   <span data-ttu-id="a460f-114">`D2D_INPUT_COUNT <N>` : Declara el número de entradas de textura al efecto.</span><span class="sxs-lookup"><span data-stu-id="a460f-114">`D2D_INPUT_COUNT <N>` : Declares the number of texture inputs to the effect.</span></span> <span data-ttu-id="a460f-115">Si el efecto tiene un número variable de entradas, este valor se debe limitar correctamente a cada punto de entrada del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a460f-115">If the effect has a variable number of inputs, this value must be scoped appropriately to each shader entry point.</span></span> <span data-ttu-id="a460f-116">La definición de este valor es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="a460f-116">Defining this value is mandatory.</span></span>
-   <span data-ttu-id="a460f-117">`D2D_INPUT<N>_SIMPLE` : Declara la entrada nth para usar el muestreo simple.</span><span class="sxs-lookup"><span data-stu-id="a460f-117">`D2D_INPUT<N>_SIMPLE` : Declares the Nth input to use simple sampling.</span></span> <span data-ttu-id="a460f-118">Si no se define, la entrada nth tiene como valor predeterminado Complex.</span><span class="sxs-lookup"><span data-stu-id="a460f-118">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="a460f-119">La definición de este valor es opcional.</span><span class="sxs-lookup"><span data-stu-id="a460f-119">Defining this value is optional.</span></span>
-   <span data-ttu-id="a460f-120">`D2D_INPUT<N>_COMPLEX` : Declara la entrada nth para usar el muestreo complejo.</span><span class="sxs-lookup"><span data-stu-id="a460f-120">`D2D_INPUT<N>_COMPLEX` : Declares the Nth input to use complex sampling.</span></span> <span data-ttu-id="a460f-121">Si no se define, la entrada nth tiene como valor predeterminado Complex.</span><span class="sxs-lookup"><span data-stu-id="a460f-121">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="a460f-122">La definición de este valor es opcional.</span><span class="sxs-lookup"><span data-stu-id="a460f-122">Defining this value is optional.</span></span>
-   <span data-ttu-id="a460f-123">`D2D_REQUIRES_SCENE_POSITION` : Indica que la función de sombreador llama a métodos auxiliares que usan el valor de posición de la escena (es decir, la función auxiliar [D2DGetScenePosition](d2dgetsceneposition.md) ).</span><span class="sxs-lookup"><span data-stu-id="a460f-123">`D2D_REQUIRES_SCENE_POSITION` : Indicates that the shader function calls helper methods that use the scene position value (namely, the [D2DGetScenePosition](d2dgetsceneposition.md) helper function).</span></span> <span data-ttu-id="a460f-124">Este parámetro solo debe incluirse cuando sea necesario, ya que solo una función por cada sombreador vinculado puede utilizar este parámetro.</span><span class="sxs-lookup"><span data-stu-id="a460f-124">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span> <span data-ttu-id="a460f-125">La definición de este valor es opcional.</span><span class="sxs-lookup"><span data-stu-id="a460f-125">Defining this value is optional.</span></span>
-   <span data-ttu-id="a460f-126">`D2D_CUSTOM_ENTRY` : Indica que la función de sombreador de píxeles consume la salida de un sombreador de vértices personalizado y, por lo tanto, declarará sus parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="a460f-126">`D2D_CUSTOM_ENTRY` : Indicates that the pixel shader function consumes the output of a custom vertex shader, and thus will declare its input parameters.</span></span> <span data-ttu-id="a460f-127">Todas las entradas personalizadas del sombreador de vértices usan un muestreo complejo y no pueden consumir la salida de otra función de sombreador (es decir, solo se pueden vincular).</span><span class="sxs-lookup"><span data-stu-id="a460f-127">All custom vertex shader inputs use complex sampling, and cannot consume the output of another shader function (i.e. they are only post-linkable).</span></span> <span data-ttu-id="a460f-128">La definición de este valor es opcional.</span><span class="sxs-lookup"><span data-stu-id="a460f-128">Defining this value is optional.</span></span>

<span data-ttu-id="a460f-129">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a460f-129">For example:</span></span>

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a><span data-ttu-id="a460f-130">Funciones del asistente</span><span class="sxs-lookup"><span data-stu-id="a460f-130">Helper Functions</span></span>

<span data-ttu-id="a460f-131">Las funciones auxiliares se usan como reemplazo para algunas funciones intrínsecas de HLSL nativas.</span><span class="sxs-lookup"><span data-stu-id="a460f-131">Helper functions are used as a replacement for some native HLSL intrinsic functions.</span></span> <span data-ttu-id="a460f-132">En tiempo de compilación, las funciones auxiliares se redefinen mediante Direct2D en la versión adecuada según el tipo de destino de compilación (sombreador completo o función de exportación).</span><span class="sxs-lookup"><span data-stu-id="a460f-132">At compile time, these helper functions are redefined by Direct2D into the appropriate version depending on the compilation target type (full shader or export function).</span></span>

<span data-ttu-id="a460f-133">Las funciones auxiliares:</span><span class="sxs-lookup"><span data-stu-id="a460f-133">The helper functions:</span></span>

<dl>

[<span data-ttu-id="a460f-134">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="a460f-134">D2DGetInput</span></span>](d2dgetinput.md)  
[<span data-ttu-id="a460f-135">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="a460f-135">D2DSampleInput</span></span>](d2dsampleinput.md)  
[<span data-ttu-id="a460f-136">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="a460f-136">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
[<span data-ttu-id="a460f-137">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="a460f-137">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
[<span data-ttu-id="a460f-138">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="a460f-138">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
[<span data-ttu-id="a460f-139">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="a460f-139">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
[<span data-ttu-id="a460f-140">Entrada de D2D \_ PS \_</span><span class="sxs-lookup"><span data-stu-id="a460f-140">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="a460f-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a460f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a460f-142">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="a460f-142">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> </dl>

 

 





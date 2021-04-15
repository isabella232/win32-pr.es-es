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
# <a name="effect-shader-linking"></a><span data-ttu-id="9ab22-103">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="9ab22-103">Effect Shader Linking</span></span>

<span data-ttu-id="9ab22-104">Direct2D usa una optimización denominada vinculación de sombreador de efectos que combina varios pasos de representación de gráficos de efectos en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="9ab22-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="9ab22-105">Información general sobre la vinculación de sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="9ab22-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="9ab22-106">Usar la vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="9ab22-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="9ab22-107">Creación de un efecto personalizado compatible con la vinculación del sombreador</span><span class="sxs-lookup"><span data-stu-id="9ab22-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="9ab22-108">Sombreador de efectos compatible con la vinculación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ab22-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="9ab22-109">Compilar un sombreador compatible con vinculador</span><span class="sxs-lookup"><span data-stu-id="9ab22-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="9ab22-110">Paso 1: compilar la función de exportación</span><span class="sxs-lookup"><span data-stu-id="9ab22-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="9ab22-111">Paso 2: compilar el sombreador completo e incrustar la función de exportación</span><span class="sxs-lookup"><span data-stu-id="9ab22-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="9ab22-112">Especificaciones de la función de exportación</span><span class="sxs-lookup"><span data-stu-id="9ab22-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="9ab22-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ab22-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="9ab22-114">Información general sobre la vinculación de sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="9ab22-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="9ab22-115">Las optimizaciones de vinculación del sombreador de efectos se basan en la vinculación del sombreador de HLSL, una característica de Direct3D 11,2 que permite generar sombreadores de píxeles y vértices en tiempo de ejecución mediante la vinculación de funciones de sombreador previamente compiladas.</span><span class="sxs-lookup"><span data-stu-id="9ab22-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="9ab22-116">Las siguientes figuras ilustran el concepto de vinculación de sombreador de efectos en un gráfico de efectos.</span><span class="sxs-lookup"><span data-stu-id="9ab22-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="9ab22-117">En la primera ilustración se muestra un gráfico de efecto de Direct2D típico con cuatro transformaciones de representación.</span><span class="sxs-lookup"><span data-stu-id="9ab22-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="9ab22-118">Sin la vinculación del sombreador, cada transformación consume un paso de representación y requiere una superficie intermedia; en total, este gráfico requiere 4 pasos y 3 intermedios.</span><span class="sxs-lookup"><span data-stu-id="9ab22-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![transformar gráfico sin vinculación del sombreador: 4 pasos y 3 intermedios.](images/shader-transform-graph.png) |



 

<span data-ttu-id="9ab22-120">En la segunda ilustración se muestra el mismo gráfico de efectos en el que cada transformación de representación se ha reemplazado por una versión de función vinculable.</span><span class="sxs-lookup"><span data-stu-id="9ab22-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="9ab22-121">Direct2D es capaz de vincular todo el grafo y ejecutarlo en un solo paso sin necesidad de ningún medio.</span><span class="sxs-lookup"><span data-stu-id="9ab22-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="9ab22-122">Esto puede proporcionar una disminución significativa en el tiempo de ejecución de la GPU y la reducción del consumo de memoria máxima de la GPU.</span><span class="sxs-lookup"><span data-stu-id="9ab22-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![transformar gráfico con vinculación del sombreador: 1 paso, 0 intermedio.](images/shader-linking-graph.png) |



 

<span data-ttu-id="9ab22-124">La vinculación de sombreador de efectos funciona en transformaciones individuales dentro de un efecto; Esto significa que incluso un gráfico con un solo efecto puede beneficiarse de la vinculación del sombreador si ese efecto tiene varias transformaciones válidas.</span><span class="sxs-lookup"><span data-stu-id="9ab22-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="9ab22-125">Usar la vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="9ab22-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="9ab22-126">Si va a compilar una aplicación de Direct2D que usa efectos, no es necesario hacer nada para aprovechar las ventajas de la vinculación del sombreador de efectos.</span><span class="sxs-lookup"><span data-stu-id="9ab22-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="9ab22-127">Direct2D analiza automáticamente el gráfico de efectos para determinar la forma más óptima de vincular cada transformación.</span><span class="sxs-lookup"><span data-stu-id="9ab22-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="9ab22-128">Los autores de efectos son responsables de implementar su efecto de forma que admita la vinculación del sombreador de efectos; para obtener más información, consulte la sección [creación de un efecto personalizado compatible con la vinculación del sombreador](#authoring-a-shader-linking-compatible-custom-effect) a continuación.</span><span class="sxs-lookup"><span data-stu-id="9ab22-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="9ab22-129">Todos los efectos integrados admiten la vinculación de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="9ab22-130">Direct2D solo vinculará las transformaciones de representación adyacentes en situaciones en las que sea beneficioso.</span><span class="sxs-lookup"><span data-stu-id="9ab22-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="9ab22-131">Tiene en cuenta varios factores a la hora de determinar si se deben vincular dos transformaciones.</span><span class="sxs-lookup"><span data-stu-id="9ab22-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="9ab22-132">Por ejemplo, la vinculación del sombreador no se realiza si una de las transformaciones utiliza los sombreadores de vértices o de cálculo, ya que solo se pueden vincular los sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="9ab22-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="9ab22-133">Además, si no se ha creado un efecto para ser compatible con la vinculación del sombreador, las transformaciones circundantes no se vincularán con él.</span><span class="sxs-lookup"><span data-stu-id="9ab22-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="9ab22-134">En el caso de que exista un riesgo de vinculación de este tipo, Direct2D no vinculará las transformaciones adyacentes al riesgo, sino que seguirá intentando vincular el resto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="9ab22-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![transformar gráfico con un riesgo de vinculación: 2 pasos, 1 intermedio.](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="9ab22-136">Creación de un efecto personalizado compatible con la vinculación del sombreador</span><span class="sxs-lookup"><span data-stu-id="9ab22-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="9ab22-137">Si va a crear su propio efecto de Direct2D personalizado, debe asegurarse de que sus transformaciones admiten la vinculación del sombreador de efectos.</span><span class="sxs-lookup"><span data-stu-id="9ab22-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="9ab22-138">Esto requiere algunos cambios menores de cómo se implementaron los efectos personalizados anteriores.</span><span class="sxs-lookup"><span data-stu-id="9ab22-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="9ab22-139">Si una transformación dentro de su efecto personalizado no admite la vinculación del sombreador, Direct2D no lo vinculará con las transformaciones adyacentes a ella en el gráfico de efectos.</span><span class="sxs-lookup"><span data-stu-id="9ab22-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="9ab22-140">Como autor de un efecto personalizado, debe tener en cuenta varios conceptos y requisitos clave:</span><span class="sxs-lookup"><span data-stu-id="9ab22-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="9ab22-141">**No hay cambios en las implementaciones de interfaz de efecto**</span><span class="sxs-lookup"><span data-stu-id="9ab22-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="9ab22-142">No es necesario modificar ningún código que implemente las diversas interfaces de efectos, como [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span><span class="sxs-lookup"><span data-stu-id="9ab22-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="9ab22-143">**Proporcionar una versión de función completa y de exportación de los sombreadores**</span><span class="sxs-lookup"><span data-stu-id="9ab22-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="9ab22-144">Debe proporcionar una versión de función de exportación de los sombreadores de su efecto, que son vinculables por Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9ab22-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="9ab22-145">Además, también debe seguir proporcionando el sombreador completo original; Esto se debe a que Direct2D selecciona en tiempo de ejecución la versión correcta del sombreador, en función de si la vinculación del sombreador se va a aplicar a un vínculo determinado del gráfico.</span><span class="sxs-lookup"><span data-stu-id="9ab22-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="9ab22-146">Si una transformación solo proporciona el BLOB del sombreador de píxeles completo (a través de [ID2D1EffectContext:: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), no se vinculará a las transformaciones adyacentes.</span><span class="sxs-lookup"><span data-stu-id="9ab22-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="9ab22-147">**Funciones auxiliares**</span><span class="sxs-lookup"><span data-stu-id="9ab22-147">**Helper functions**</span></span>

    <span data-ttu-id="9ab22-148">Direct2D proporciona [funciones](hlsl-helpers.md) y macros auxiliares de HLSL que generarán automáticamente las versiones de función completa y de exportación de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="9ab22-149">Estas aplicaciones auxiliares se pueden encontrar en d2d1effecthelpers. hlsli.</span><span class="sxs-lookup"><span data-stu-id="9ab22-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="9ab22-150">Además, el compilador de HLSL (FXC) permite insertar el sombreador de funciones de exportación en un campo privado en el sombreador completo.</span><span class="sxs-lookup"><span data-stu-id="9ab22-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="9ab22-151">De esta manera, solo tiene que crear un sombreador una vez y pasar ambas versiones a Direct2D simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="9ab22-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="9ab22-152">Tanto d2d1effecthelpers. hlsli como el compilador FXC se incluyen como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9ab22-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="9ab22-153">Las funciones auxiliares:</span><span class="sxs-lookup"><span data-stu-id="9ab22-153">The helper functions:</span></span>

  - [<span data-ttu-id="9ab22-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="9ab22-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="9ab22-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="9ab22-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="9ab22-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="9ab22-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="9ab22-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="9ab22-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="9ab22-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="9ab22-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="9ab22-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="9ab22-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="9ab22-160">Entrada de D2D \_ PS \_</span><span class="sxs-lookup"><span data-stu-id="9ab22-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="9ab22-161">También puede crear manualmente dos versiones de cada sombreador y compilarlas dos veces, siempre y cuando se cumplan las especificaciones descritas a continuación en especificaciones de la [función de exportación](#export-function-specifications) .</span><span class="sxs-lookup"><span data-stu-id="9ab22-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="9ab22-162">**Solo sombreadores de píxeles**</span><span class="sxs-lookup"><span data-stu-id="9ab22-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="9ab22-163">Direct2D no admite la vinculación de sombreadores de cálculo o de vértices.</span><span class="sxs-lookup"><span data-stu-id="9ab22-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="9ab22-164">Sin embargo, si el efecto usa un sombreador de vértices y píxeles, la salida del sombreador de píxeles todavía se puede vincular.</span><span class="sxs-lookup"><span data-stu-id="9ab22-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="9ab22-165">**Muestreo simple frente a complejo**</span><span class="sxs-lookup"><span data-stu-id="9ab22-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="9ab22-166">La vinculación de la función de sombreador funciona conectando la salida de un sombreador de píxeles pasando a la entrada de una fase del sombreador de píxeles subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="9ab22-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="9ab22-167">Esto solo es posible cuando el sombreador de píxeles de consumo requiere un solo valor de entrada para realizar su cálculo; Normalmente, este valor proviene del muestreo de una textura de entrada en la coordenada de textura emitida por el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="9ab22-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="9ab22-168">Se dice que este sombreador de píxeles realiza un muestreo sencillo.</span><span class="sxs-lookup"><span data-stu-id="9ab22-168">Such a pixel shader is said to perform simple sampling.</span></span>

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![la conversión de escala de grises es un ejemplo de muestreo sencillo.](images/simple-sampling.png) |

    

     

    <span data-ttu-id="9ab22-171">Algunos sombreadores de píxeles, como un desenfoque gaussiano, calculan la salida de varios ejemplos de entrada en lugar de un solo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9ab22-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="9ab22-172">Se dice que este sombreador de píxeles realiza un muestreo complejo.</span><span class="sxs-lookup"><span data-stu-id="9ab22-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![Desenfoque gaussiano es un ejemplo de muestreo complejo.](images/complex-sampling.png) |

    

     

    <span data-ttu-id="9ab22-175">Solo las funciones de sombreador con entradas simples pueden tener su entrada proporcionada por otra función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="9ab22-176">Las funciones de sombreador con entradas complejas se deben proporcionar con una textura de entrada para muestrear.</span><span class="sxs-lookup"><span data-stu-id="9ab22-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="9ab22-177">Esto significa que Direct2D no vinculará un sombreador con entradas complejas a su predecesor.</span><span class="sxs-lookup"><span data-stu-id="9ab22-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="9ab22-178">Al usar las [aplicaciones auxiliares de HLSL para Direct2D](hlsl-helpers.md), debe indicar en HLSL si un sombreador usa entradas simples o complejas.</span><span class="sxs-lookup"><span data-stu-id="9ab22-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="9ab22-179">Sombreador de efectos compatible con la vinculación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ab22-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="9ab22-180">Con las aplicaciones auxiliares de D2D, el siguiente fragmento de código representa un sombreador de efectos sencillo compatible con la vinculación:</span><span class="sxs-lookup"><span data-stu-id="9ab22-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

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

<span data-ttu-id="9ab22-181">En este breve ejemplo, observe que no se declara ningún parámetro de función, que el número de entradas y el tipo de cada entrada se declara antes que la función de entrada, la entrada se recupera llamando a [D2DGetInput](d2dgetinput.md)y que se deben definir las directivas de preprocesador antes de que se incluya el archivo auxiliar.</span><span class="sxs-lookup"><span data-stu-id="9ab22-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="9ab22-182">Un sombreador compatible con vinculación debe proporcionar un sombreador de píxeles de paso único normal y una función de sombreador de exportación.</span><span class="sxs-lookup"><span data-stu-id="9ab22-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="9ab22-183">La macro [D2D \_ PS \_ entry](d2d-ps-entry.md) permite que cada una de ellas se genere a partir del mismo código, cuando se usa junto con el script de compilación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="9ab22-184">Al compilar un sombreador completo, las macros se expanden en el código siguiente, que tiene una firma de entrada compatible con efectos de D2D.</span><span class="sxs-lookup"><span data-stu-id="9ab22-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

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

<span data-ttu-id="9ab22-185">Al compilar una versión de función de exportación del mismo código, se genera el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ab22-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="9ab22-186">Tenga en cuenta que la entrada de textura, que normalmente se recupera mediante el muestreo de un Texture2D, se ha reemplazado por una entrada de función (input0).</span><span class="sxs-lookup"><span data-stu-id="9ab22-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="9ab22-187">Para ver una descripción completa y paso a paso de lo que debe hacer para escribir un efecto compatible con la vinculación, vea el [tutorial de efectos personalizados](custom-effects.md) y el [ejemplo de efectos de imagen personalizados de Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="9ab22-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="9ab22-188">Compilar un sombreador compatible con vinculador</span><span class="sxs-lookup"><span data-stu-id="9ab22-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="9ab22-189">Para que sea vinculable, el BLOB del sombreador de píxeles pasado a D2D debe contener las versiones de función Full y Export del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="9ab22-190">Esto se logra mediante la incrustación de la función de exportación compilada en el \_ área de datos privados del BLOB D3D \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9ab22-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="9ab22-191">Cuando los sombreadores se crean con las funciones auxiliares de D2D, se debe definir un destino de compilación D2D en el momento de la compilación.</span><span class="sxs-lookup"><span data-stu-id="9ab22-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="9ab22-192">Los tipos de destino de compilación son D2D \_ Full \_ Shader y D2D \_ function.</span><span class="sxs-lookup"><span data-stu-id="9ab22-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="9ab22-193">La compilación de un sombreador de efectos compatible con la vinculación es un proceso de dos pasos:</span><span class="sxs-lookup"><span data-stu-id="9ab22-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="9ab22-194">Compilar la función de exportación</span><span class="sxs-lookup"><span data-stu-id="9ab22-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="9ab22-195">Compilar el sombreador completo e incrustar la función de exportación</span><span class="sxs-lookup"><span data-stu-id="9ab22-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="9ab22-196">Al compilar un efecto con Visual Studio, debe crear un archivo por lotes que ejecute ambos comandos de FXC y ejecutar este archivo por lotes como un paso de compilación personalizado que se ejecuta antes del paso de compilación.</span><span class="sxs-lookup"><span data-stu-id="9ab22-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="9ab22-197">Paso 1: compilar la función de exportación</span><span class="sxs-lookup"><span data-stu-id="9ab22-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="9ab22-198">Para compilar la versión de la función de exportación del sombreador, debe pasar las siguientes marcas a FXC.</span><span class="sxs-lookup"><span data-stu-id="9ab22-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab22-199">**Marca**</span><span class="sxs-lookup"><span data-stu-id="9ab22-199">**Flag**</span></span>                       | <span data-ttu-id="9ab22-200">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ab22-200">**Description**</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="9ab22-201">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="9ab22-201">/T <ShaderModel></span></span>         | <span data-ttu-id="9ab22-202">Establezca <ShaderModel> en el perfil de sombreador de píxeles adecuado tal y como se define en la [Sintaxis de FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="9ab22-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="9ab22-203">Debe ser uno de los perfiles que aparecen en "vinculación del sombreador de HLSL".</span><span class="sxs-lookup"><span data-stu-id="9ab22-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="9ab22-204"><MyShaderFile>. HLSL</span><span class="sxs-lookup"><span data-stu-id="9ab22-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="9ab22-205">Establezca <MyShaderFile> en el nombre del archivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="9ab22-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="9ab22-206">/D D2D \_ función)</span><span class="sxs-lookup"><span data-stu-id="9ab22-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="9ab22-207">Esta definición indica a FXC que compile la versión de la función de exportación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="9ab22-208">/D D2D \_ entry =<entry></span><span class="sxs-lookup"><span data-stu-id="9ab22-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="9ab22-209">Establezca <entry> en el nombre del punto de entrada de HLSL que ha definido en la macro [D2D \_ PS \_ entry](d2d-ps-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab22-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="9ab22-210">/FL <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="9ab22-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="9ab22-211">Establezca <MyShaderfile> en dónde desea almacenar la versión de la función de exportación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="9ab22-212">Tenga en cuenta que la extensión. fxlib solo es para facilitar la identificación.</span><span class="sxs-lookup"><span data-stu-id="9ab22-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="9ab22-213">Paso 2: compilar el sombreador completo e incrustar la función de exportación</span><span class="sxs-lookup"><span data-stu-id="9ab22-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="9ab22-214">Para compilar la versión completa del sombreador con la versión de exportación incrustada, debe pasar las siguientes marcas a FXC.</span><span class="sxs-lookup"><span data-stu-id="9ab22-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab22-215">**Marca**</span><span class="sxs-lookup"><span data-stu-id="9ab22-215">**Flag**</span></span>                               | <span data-ttu-id="9ab22-216">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ab22-216">**Description**</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9ab22-217">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="9ab22-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="9ab22-218">Establezca <ShaderModel> en el perfil de sombreador de píxeles adecuado tal y como se define en la [Sintaxis de FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="9ab22-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="9ab22-219">Debe ser el perfil de sombreador de píxeles correspondiente al perfil de vinculación especificado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="9ab22-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="9ab22-220"><MyShaderFile>. HLSL</span><span class="sxs-lookup"><span data-stu-id="9ab22-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="9ab22-221">Establezca <MyShaderFile> en el nombre del archivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="9ab22-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9ab22-222">D2Dr/d ( \_ \_ sombreador completo)</span><span class="sxs-lookup"><span data-stu-id="9ab22-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="9ab22-223">Esta definición indica a FXC que compile la versión completa del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="9ab22-224">/D D2D \_ entry =<entry></span><span class="sxs-lookup"><span data-stu-id="9ab22-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="9ab22-225">Establezca <entry> en el nombre del punto de entrada de HLSL que ha definido dentro de la \_ macro D2D PS \_ entry ().</span><span class="sxs-lookup"><span data-stu-id="9ab22-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="9ab22-226">/E <entry></span><span class="sxs-lookup"><span data-stu-id="9ab22-226">/E <entry></span></span>                       | <span data-ttu-id="9ab22-227">Establezca <entry> en el nombre del punto de entrada de HLSL que ha definido dentro de la \_ macro D2D PS \_ entry ().</span><span class="sxs-lookup"><span data-stu-id="9ab22-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="9ab22-228">/setprivate <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="9ab22-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="9ab22-229">Este argumento indica a FXC que inserte el sombreador de la función de exportación generado en el paso 1 en el \_ área de datos privados del BLOB D3D \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9ab22-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="9ab22-230">/FO <MyShader> . CSO</span><span class="sxs-lookup"><span data-stu-id="9ab22-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="9ab22-231">Establezca <MyShader> en dónde desea almacenar el sombreador compilado final combinado.</span><span class="sxs-lookup"><span data-stu-id="9ab22-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="9ab22-232">/FH <MyShader> . h</span><span class="sxs-lookup"><span data-stu-id="9ab22-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="9ab22-233">Establezca <MyShader> en dónde desea almacenar el encabezado combinado final.</span><span class="sxs-lookup"><span data-stu-id="9ab22-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a><span data-ttu-id="9ab22-234">Especificaciones de la función de exportación</span><span class="sxs-lookup"><span data-stu-id="9ab22-234">Export function specifications</span></span>

<span data-ttu-id="9ab22-235">Aunque no se recomienda, es posible crear un sombreador de efectos compatible sin usar las aplicaciones auxiliares proporcionadas por D2D.</span><span class="sxs-lookup"><span data-stu-id="9ab22-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="9ab22-236">Se debe tener cuidado para asegurarse de que las firmas de entrada de la función de exportación y el sombreador completo cumplen con las especificaciones de D2D.</span><span class="sxs-lookup"><span data-stu-id="9ab22-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="9ab22-237">Las especificaciones de los sombreadores completos son las mismas que las versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="9ab22-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="9ab22-238">Brevemente, los parámetros de entrada del sombreador de píxeles deben ser la \_ posición de la VP, la \_ posición de la escena y una TEXCOORD por entrada de efecto.</span><span class="sxs-lookup"><span data-stu-id="9ab22-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="9ab22-239">Para la función de exportación, la función debe devolver FLOAT4 y sus entradas deben ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9ab22-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="9ab22-240">Entrada simple</span><span class="sxs-lookup"><span data-stu-id="9ab22-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="9ab22-241">En el caso de las entradas simples, D2D insertará una función de ejemplo entre la textura de entrada y la función de sombreador, o bien la salida de otra función de sombreador proporcionará la entrada.</span><span class="sxs-lookup"><span data-stu-id="9ab22-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="9ab22-242">Entrada compleja</span><span class="sxs-lookup"><span data-stu-id="9ab22-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="9ab22-243">En el caso de las entradas complejas, D2D solo pasará una coordenada de textura, como se describe en la documentación de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9ab22-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="9ab22-244">Ubicación de salida</span><span class="sxs-lookup"><span data-stu-id="9ab22-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="9ab22-245">Solo \_ se puede definir una entrada de posición de la escena.</span><span class="sxs-lookup"><span data-stu-id="9ab22-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="9ab22-246">Este parámetro solo debe incluirse cuando sea necesario, ya que solo una función por cada sombreador vinculado puede utilizar este parámetro.</span><span class="sxs-lookup"><span data-stu-id="9ab22-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="9ab22-247">La semántica debe definirse como se indicó anteriormente, ya que D2D inspeccionará la semántica para decidir cómo vincular las funciones entre sí.</span><span class="sxs-lookup"><span data-stu-id="9ab22-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="9ab22-248">Si alguna entrada de función no coincide con uno de los tipos anteriores, se rechazará la función para la vinculación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9ab22-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ab22-249">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ab22-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ab22-250">Aplicaciones auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="9ab22-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="9ab22-251">Interfaz ID3D11Linker</span><span class="sxs-lookup"><span data-stu-id="9ab22-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="9ab22-252">Interfaz ID3D11FunctionLinkingGraph</span><span class="sxs-lookup"><span data-stu-id="9ab22-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 
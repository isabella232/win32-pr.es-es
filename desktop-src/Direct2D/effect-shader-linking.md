---
title: Vinculación del sombreador de efectos
description: Direct2D usa una optimización denominada vinculación del sombreador de efectos que combina varios pases de representación de gráfico de efecto en un solo paso.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6bad2170f2b897a5cf8ac3086a74945efa8bf
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549240"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="365ee-103">Vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="365ee-103">Effect Shader Linking</span></span>

<span data-ttu-id="365ee-104">Direct2D usa una optimización denominada vinculación del sombreador de efectos que combina varios pases de representación de gráfico de efecto en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="365ee-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="365ee-105">Información general sobre la vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="365ee-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="365ee-106">Usar la vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="365ee-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="365ee-107">Creación de un efecto personalizado compatible con la vinculación de sombreador</span><span class="sxs-lookup"><span data-stu-id="365ee-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="365ee-108">Sombreador de efecto compatible con la vinculación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="365ee-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="365ee-109">Compilación de un sombreador compatible de vinculación</span><span class="sxs-lookup"><span data-stu-id="365ee-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="365ee-110">Paso 1: Compilación de la función de exportación</span><span class="sxs-lookup"><span data-stu-id="365ee-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="365ee-111">Paso 2: Compilación del sombreador completo e inserción de la función de exportación</span><span class="sxs-lookup"><span data-stu-id="365ee-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="365ee-112">Exportar especificaciones de función</span><span class="sxs-lookup"><span data-stu-id="365ee-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="365ee-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="365ee-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="365ee-114">Información general sobre la vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="365ee-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="365ee-115">Las optimizaciones de vinculación del sombreador de efectos se basa en la vinculación del sombreador HLSL, una característica de Direct3D 11.2 que permite generar sombreadores de píxeles y vértices en tiempo de ejecución mediante la vinculación de funciones de sombreador compiladas previamente.</span><span class="sxs-lookup"><span data-stu-id="365ee-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="365ee-116">Las siguientes figuras ilustran el concepto de vinculación del sombreador de efectos en un gráfico de efectos.</span><span class="sxs-lookup"><span data-stu-id="365ee-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="365ee-117">En la primera ilustración se muestra un gráfico de efectos de Direct2D típico con cuatro transformaciones de representación.</span><span class="sxs-lookup"><span data-stu-id="365ee-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="365ee-118">Sin la vinculación del sombreador, cada transformación consume un paso de representación y requiere una superficie intermedia; en total, este gráfico requiere 4 pases y 3 intermedios.</span><span class="sxs-lookup"><span data-stu-id="365ee-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>

![transformar gráfico sin vinculación de sombreador: 4 pases y 3 intermedios.](images/shader-transform-graph.png)

<span data-ttu-id="365ee-120">En la segunda ilustración se muestra el mismo gráfico de efecto en el que cada transformación de representación se ha reemplazado por una versión de función enlazable.</span><span class="sxs-lookup"><span data-stu-id="365ee-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="365ee-121">Direct2D puede vincular todo el gráfico y ejecutarlo en un solo paso sin necesidad de ningún intermedio.</span><span class="sxs-lookup"><span data-stu-id="365ee-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="365ee-122">Esto puede proporcionar una disminución significativa en el tiempo de ejecución de GPU y una reducción en el consumo máximo de memoria de GPU.</span><span class="sxs-lookup"><span data-stu-id="365ee-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>

![transformar gráfico con vinculación de sombreador: 1 paso, 0 intermedios.](images/shader-linking-graph.png)



 

<span data-ttu-id="365ee-124">La vinculación del sombreador de efectos funciona en transformaciones individuales dentro de un efecto; Esto significa que incluso un gráfico con un único efecto puede beneficiarse de la vinculación del sombreador si ese efecto tiene varias transformaciones válidas.</span><span class="sxs-lookup"><span data-stu-id="365ee-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="365ee-125">Usar la vinculación del sombreador de efectos</span><span class="sxs-lookup"><span data-stu-id="365ee-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="365ee-126">Si va a crear una aplicación de Direct2D que usa efectos, no es necesario hacer nada para aprovechar las ventajas de la vinculación del sombreador de efectos.</span><span class="sxs-lookup"><span data-stu-id="365ee-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="365ee-127">Direct2D analiza automáticamente el gráfico de efectos para determinar la manera más óptima de vincular cada transformación.</span><span class="sxs-lookup"><span data-stu-id="365ee-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="365ee-128">Los autores de efectos son responsables de implementar su efecto de forma que admita la vinculación del sombreador de efectos. Para obtener más información, consulte la sección Creación de un efecto personalizado compatible con la vinculación de [sombreadores](#authoring-a-shader-linking-compatible-custom-effect) a continuación.</span><span class="sxs-lookup"><span data-stu-id="365ee-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="365ee-129">Todos los efectos integrados admiten la vinculación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="365ee-130">Direct2D solo vinculará transformaciones de representación adyacentes en situaciones en las que sea beneficioso.</span><span class="sxs-lookup"><span data-stu-id="365ee-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="365ee-131">Tiene en cuenta varios factores al determinar si se vinculan dos transformaciones.</span><span class="sxs-lookup"><span data-stu-id="365ee-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="365ee-132">Por ejemplo, la vinculación del sombreador no se realiza si una de las transformaciones usa sombreadores de vértices o de proceso, ya que solo se pueden vincular sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="365ee-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="365ee-133">Además, si no se ha creado un efecto para que sea compatible con la vinculación del sombreador, las transformaciones circundantes no se vincularán con él.</span><span class="sxs-lookup"><span data-stu-id="365ee-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="365ee-134">En el caso de que exista un peligro de vinculación de este tipo, Direct2D no vinculará ninguna transformación adyacente al peligro, sino que intentará vincular el resto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="365ee-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>

![transformar grafo con un peligro de vinculación: 2 pases, 1 intermedio.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="365ee-136">Creación de un efecto personalizado compatible con la vinculación de sombreadores</span><span class="sxs-lookup"><span data-stu-id="365ee-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="365ee-137">Si va a crear su propio efecto personalizado de Direct2D, debe asegurarse de que sus transformaciones admiten la vinculación del sombreador de efectos.</span><span class="sxs-lookup"><span data-stu-id="365ee-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="365ee-138">Esto requiere algunos cambios menores de la forma en que se implementaron los efectos personalizados anteriores.</span><span class="sxs-lookup"><span data-stu-id="365ee-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="365ee-139">Si una transformación dentro del efecto personalizado no admite la vinculación de sombreador, Direct2D no la vinculará con ninguna transformación adyacente a ella en el gráfico de efectos.</span><span class="sxs-lookup"><span data-stu-id="365ee-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="365ee-140">Como autor de efectos personalizados, debe tener en cuenta varios conceptos y requisitos clave:</span><span class="sxs-lookup"><span data-stu-id="365ee-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="365ee-141">**No hay cambios en las implementaciones de interfaz de efecto**</span><span class="sxs-lookup"><span data-stu-id="365ee-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="365ee-142">No es necesario modificar ningún código que implemente las distintas interfaces de efecto, [como ID2D1DrawTransform.](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)</span><span class="sxs-lookup"><span data-stu-id="365ee-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="365ee-143">**Proporcionar una versión de función completa y de exportación de sombreadores**</span><span class="sxs-lookup"><span data-stu-id="365ee-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="365ee-144">Debe proporcionar una versión de función de exportación de los sombreadores del efecto que Direct2D puede vincular.</span><span class="sxs-lookup"><span data-stu-id="365ee-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="365ee-145">Además, también debe seguir proporcionando el sombreador completo original; Esto se debe a que Direct2D selecciona en tiempo de ejecución la versión correcta del sombreador en función de si la vinculación del sombreador se va a aplicar a un vínculo determinado del gráfico.</span><span class="sxs-lookup"><span data-stu-id="365ee-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="365ee-146">Si una transformación solo proporciona el blob de sombreador de píxeles completo (a través de [ID2D1EffectContext::LoadPixelShader),](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)no se vinculará a transformaciones adyacentes.</span><span class="sxs-lookup"><span data-stu-id="365ee-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="365ee-147">**Funciones auxiliares**</span><span class="sxs-lookup"><span data-stu-id="365ee-147">**Helper functions**</span></span>

    <span data-ttu-id="365ee-148">Direct2D proporciona macros y funciones auxiliares [HLSL](hlsl-helpers.md) que generarán automáticamente las versiones completas y de exportación de funciones de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="365ee-149">Estos asistentes se pueden encontrar en d2d1effecthelpers.hlsli.</span><span class="sxs-lookup"><span data-stu-id="365ee-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="365ee-150">Además, el compilador HLSL (FXC) permite insertar el sombreador de funciones de exportación en un campo privado en el sombreador completo.</span><span class="sxs-lookup"><span data-stu-id="365ee-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="365ee-151">De este modo, solo necesita crear un sombreador una vez y pasar ambas versiones a Direct2D simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="365ee-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="365ee-152">Tanto d2d1effecthelpers.hlsli como el compilador FXC se incluyen como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="365ee-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="365ee-153">Las funciones auxiliares:</span><span class="sxs-lookup"><span data-stu-id="365ee-153">The helper functions:</span></span>

  - [<span data-ttu-id="365ee-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="365ee-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="365ee-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="365ee-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="365ee-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="365ee-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="365ee-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="365ee-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="365ee-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="365ee-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="365ee-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="365ee-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="365ee-160">D2D \_ PS \_ ENTRY</span><span class="sxs-lookup"><span data-stu-id="365ee-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="365ee-161">También puede crear manualmente dos versiones de cada sombreador y compilarlas dos veces, siempre y cuando se cumplen las especificaciones descritas a continuación en [Exportar](#export-function-specifications) especificaciones de función.</span><span class="sxs-lookup"><span data-stu-id="365ee-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="365ee-162">**Solo sombreadores de píxeles**</span><span class="sxs-lookup"><span data-stu-id="365ee-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="365ee-163">Direct2D no admite la vinculación de sombreadores de vértices o proceso.</span><span class="sxs-lookup"><span data-stu-id="365ee-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="365ee-164">Sin embargo, si el efecto usa un sombreador de vértices y píxeles, la salida del sombreador de píxeles todavía se puede vincular.</span><span class="sxs-lookup"><span data-stu-id="365ee-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="365ee-165">**Muestreo simple frente a complejo**</span><span class="sxs-lookup"><span data-stu-id="365ee-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="365ee-166">La vinculación de funciones de sombreador funciona conectando la salida de un paso de sombreador de píxeles a la entrada de un paso posterior del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="365ee-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="365ee-167">Esto solo es posible cuando el sombreador de píxeles de consumo solo requiere un valor de entrada único para realizar su cálculo; Este valor normalmente procedería del muestreo de una textura de entrada en la coordenada de textura emitida por el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="365ee-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="365ee-168">Se dice que este sombreador de píxeles realiza un muestreo simple.</span><span class="sxs-lookup"><span data-stu-id="365ee-168">Such a pixel shader is said to perform simple sampling.</span></span>

    ![La conversión de escala de grises es un ejemplo de muestreo simple.](images/simple-sampling.png)

    <span data-ttu-id="365ee-171">Algunos sombreadores de píxeles, como un desenfoque gaussiano, calculan su salida a partir de varias muestras de entrada en lugar de una sola muestra.</span><span class="sxs-lookup"><span data-stu-id="365ee-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="365ee-172">Se dice que este sombreador de píxeles realiza un muestreo complejo.</span><span class="sxs-lookup"><span data-stu-id="365ee-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    ![El desenfoque gaussiano es un ejemplo de muestreo complejo.](images/complex-sampling.png)

    
    <span data-ttu-id="365ee-175">Solo las funciones de sombreador con entradas simples pueden tener su entrada proporcionada por otra función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="365ee-176">Las funciones de sombreador con entradas complejas deben proporcionarse con una textura de entrada para muestrear.</span><span class="sxs-lookup"><span data-stu-id="365ee-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="365ee-177">Esto significa que Direct2D no vinculará un sombreador con entradas complejas a su predecesor.</span><span class="sxs-lookup"><span data-stu-id="365ee-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="365ee-178">Cuando se usan [los asistentes HLSL de Direct2D,](hlsl-helpers.md)debe indicar en HLSL si un sombreador usa entradas complejas o sencillas.</span><span class="sxs-lookup"><span data-stu-id="365ee-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="365ee-179">Sombreador de efectos compatible con la vinculación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="365ee-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="365ee-180">Con los asistentes de D2D, el siguiente fragmento de código representa un sombreador de efectos compatible con la vinculación simple:</span><span class="sxs-lookup"><span data-stu-id="365ee-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

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

<span data-ttu-id="365ee-181">En este breve ejemplo, tenga en cuenta que no se declara ningún parámetro de función, que el número de entradas y el tipo de cada entrada se declara antes de la función de entrada, que la entrada se recupera mediante una llamada a [D2DGetInput](d2dgetinput.md)y que las directivas de preprocesador deben definirse antes de incluir el archivo auxiliar.</span><span class="sxs-lookup"><span data-stu-id="365ee-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="365ee-182">Un sombreador compatible con la vinculación debe proporcionar un sombreador de píxeles de un solo paso normal y una función de sombreador de exportación.</span><span class="sxs-lookup"><span data-stu-id="365ee-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="365ee-183">La [macro D2D \_ PS \_ ENTRY](d2d-ps-entry.md) permite generar cada uno de ellos a partir del mismo código, cuando se usa junto con el script de compilación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="365ee-184">Al compilar un sombreador completo, las macros se expanden en el código siguiente, que tiene una firma de entrada compatible con efectos D2D.</span><span class="sxs-lookup"><span data-stu-id="365ee-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

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

<span data-ttu-id="365ee-185">Al compilar una versión de función de exportación del mismo código, se genera el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="365ee-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="365ee-186">Tenga en cuenta que la entrada de textura, recuperada normalmente mediante el muestreo de texture2D, se ha reemplazado por una entrada de función (input0).</span><span class="sxs-lookup"><span data-stu-id="365ee-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="365ee-187">Para ver una descripción completa paso a paso de lo que debe hacer para escribir un efecto compatible con la vinculación, consulte el [tutorial](custom-effects.md) de efectos personalizados y el ejemplo de efectos de imagen personalizada de [Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="365ee-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="365ee-188">Compilación de un sombreador compatible de vinculación</span><span class="sxs-lookup"><span data-stu-id="365ee-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="365ee-189">Para poder vincularse, el blob de sombreador de píxeles pasado a D2D debe contener las versiones de función completa y de exportación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="365ee-190">Para ello, inserte la función de exportación compilada en el área D3D \_ BLOB \_ PRIVATE \_ DATA.</span><span class="sxs-lookup"><span data-stu-id="365ee-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="365ee-191">Cuando los sombreadores se han creado con las funciones auxiliares D2D, se debe definir un destino de compilación D2D en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="365ee-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="365ee-192">Los tipos de destino de compilación son D2D \_ FULL \_ SHADER y D2D \_ FUNCTION.</span><span class="sxs-lookup"><span data-stu-id="365ee-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="365ee-193">La compilación de un sombreador de efectos compatible con la vinculación es un proceso de dos pasos:</span><span class="sxs-lookup"><span data-stu-id="365ee-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="365ee-194">Compilación de la función de exportación</span><span class="sxs-lookup"><span data-stu-id="365ee-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="365ee-195">Compilación del sombreador completo e inserción de la función de exportación</span><span class="sxs-lookup"><span data-stu-id="365ee-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="365ee-196">Al compilar un efecto mediante Visual Studio, debe crear un archivo por lotes que ejecute ambos comandos FXC y ejecutar este archivo por lotes como un paso de compilación personalizado que se ejecute antes del paso de compilación.</span><span class="sxs-lookup"><span data-stu-id="365ee-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="365ee-197">Paso 1: Compilación de la función de exportación</span><span class="sxs-lookup"><span data-stu-id="365ee-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="365ee-198">Para compilar la versión de la función de exportación del sombreador, debe pasar las marcas siguientes a FXC.</span><span class="sxs-lookup"><span data-stu-id="365ee-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|    <span data-ttu-id="365ee-199">Marca</span><span class="sxs-lookup"><span data-stu-id="365ee-199">Flag</span></span>                            |    <span data-ttu-id="365ee-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="365ee-200">Description</span></span>                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="365ee-201">/t <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="365ee-201">/T <ShaderModel></span></span>         | <span data-ttu-id="365ee-202">Establezca <ShaderModel> en el perfil de sombreador de píxeles adecuado, tal como se define en [Sintaxis de FXC.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)</span><span class="sxs-lookup"><span data-stu-id="365ee-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="365ee-203">Debe ser uno de los perfiles enumerados en "Vinculación de sombreador HLSL".</span><span class="sxs-lookup"><span data-stu-id="365ee-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="365ee-204"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="365ee-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="365ee-205">Establezca <MyShaderFile> en el nombre del archivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="365ee-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="365ee-206">/D D D2D \_ (FUNCIÓN)</span><span class="sxs-lookup"><span data-stu-id="365ee-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="365ee-207">Esta definición indica a FXC que compile la versión de la función de exportación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="365ee-208">/D D D2D \_ ENTRY=<entry></span><span class="sxs-lookup"><span data-stu-id="365ee-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="365ee-209">Establezca <entry> en el nombre del punto de entrada HLSL que definió dentro de la macro [ \_ D2D PS \_ ENTRY.](d2d-ps-entry.md)</span><span class="sxs-lookup"><span data-stu-id="365ee-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="365ee-210">/Fl <MyShaderFile> .fxlib</span><span class="sxs-lookup"><span data-stu-id="365ee-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="365ee-211">Establezca <MyShaderfile> en donde desea almacenar la versión de la función de exportación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="365ee-212">Tenga en cuenta que la extensión .fxlib solo es para facilitar la identificación.</span><span class="sxs-lookup"><span data-stu-id="365ee-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="365ee-213">Paso 2: Compilación del sombreador completo e inserción de la función de exportación</span><span class="sxs-lookup"><span data-stu-id="365ee-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="365ee-214">Para compilar la versión completa del sombreador con la versión de exportación incrustada, debe pasar las marcas siguientes a FXC.</span><span class="sxs-lookup"><span data-stu-id="365ee-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|    <span data-ttu-id="365ee-215">Marca</span><span class="sxs-lookup"><span data-stu-id="365ee-215">Flag</span></span>                                    |    <span data-ttu-id="365ee-216">Descripción</span><span class="sxs-lookup"><span data-stu-id="365ee-216">Description</span></span>                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="365ee-217">/t <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="365ee-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="365ee-218">Establezca <ShaderModel> en el perfil de sombreador de píxeles adecuado, tal como se define en [Sintaxis de FXC.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)</span><span class="sxs-lookup"><span data-stu-id="365ee-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="365ee-219">Debe ser el perfil de sombreador de píxeles correspondiente al perfil de vinculación especificado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="365ee-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="365ee-220"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="365ee-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="365ee-221">Establezca <MyShaderFile> en el nombre del archivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="365ee-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="365ee-222">SOMBREADOR COMPLETO /D \_ D2D \_</span><span class="sxs-lookup"><span data-stu-id="365ee-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="365ee-223">Esta definición indica a FXC que compile la versión completa del sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="365ee-224">/D D D2D \_ ENTRY=<entry></span><span class="sxs-lookup"><span data-stu-id="365ee-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="365ee-225">Establezca <entry> en el nombre del punto de entrada HLSL que definió dentro de la macro D2D PS \_ \_ ENTRY().</span><span class="sxs-lookup"><span data-stu-id="365ee-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="365ee-226">/e <entry></span><span class="sxs-lookup"><span data-stu-id="365ee-226">/E <entry></span></span>                       | <span data-ttu-id="365ee-227">Establezca <entry> en el nombre del punto de entrada HLSL que definió dentro de la macro D2D PS \_ \_ ENTRY().</span><span class="sxs-lookup"><span data-stu-id="365ee-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="365ee-228">/setprivate <MyShaderFile> .fxlib</span><span class="sxs-lookup"><span data-stu-id="365ee-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="365ee-229">Este argumento indica a FXC que inserte el sombreador de funciones de exportación generado en el paso 1 en el área D3D \_ BLOB \_ PRIVATE \_ DATA.</span><span class="sxs-lookup"><span data-stu-id="365ee-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="365ee-230">/Fo <MyShader> .cso</span><span class="sxs-lookup"><span data-stu-id="365ee-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="365ee-231">Establezca <MyShader> en donde desea almacenar el sombreador compilado combinado final.</span><span class="sxs-lookup"><span data-stu-id="365ee-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="365ee-232">/Fh <MyShader> .h</span><span class="sxs-lookup"><span data-stu-id="365ee-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="365ee-233">Establezca <MyShader> en donde desea almacenar el encabezado combinado final.</span><span class="sxs-lookup"><span data-stu-id="365ee-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a><span data-ttu-id="365ee-234">Exportar especificaciones de función</span><span class="sxs-lookup"><span data-stu-id="365ee-234">Export function specifications</span></span>

<span data-ttu-id="365ee-235">Aunque no se recomienda, es posible crear un sombreador de efectos compatible sin usar los asistentes proporcionados por D2D.</span><span class="sxs-lookup"><span data-stu-id="365ee-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="365ee-236">Se debe tener cuidado para asegurarse de que tanto el sombreador completo como las firmas de entrada de función de exportación se ajustan a las especificaciones de D2D.</span><span class="sxs-lookup"><span data-stu-id="365ee-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="365ee-237">Las especificaciones de los sombreadores completos son las mismas que las versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="365ee-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="365ee-238">Brevemente, los parámetros de entrada del sombreador de píxeles deben ser SV POSITION, SCENE POSITION y \_ \_ una entrada TEXCOORD por efecto.</span><span class="sxs-lookup"><span data-stu-id="365ee-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="365ee-239">Para la función de exportación, la función debe devolver float4 y sus entradas deben ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="365ee-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="365ee-240">Entrada simple</span><span class="sxs-lookup"><span data-stu-id="365ee-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="365ee-241">En el caso de las entradas simples, D2D insertará una función Sample entre la textura de entrada y la función de sombreador, o la entrada la proporciona la salida de otra función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="365ee-242">Entrada compleja</span><span class="sxs-lookup"><span data-stu-id="365ee-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="365ee-243">En el caso de las entradas complejas, D2D solo pasará una coordenada de textura como se describe en Windows 8 documentación.</span><span class="sxs-lookup"><span data-stu-id="365ee-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="365ee-244">Ubicación de salida</span><span class="sxs-lookup"><span data-stu-id="365ee-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="365ee-245">Solo se puede \_ definir una entrada SCENE POSITION.</span><span class="sxs-lookup"><span data-stu-id="365ee-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="365ee-246">Este parámetro solo debe incluirse cuando sea necesario, ya que solo una función por sombreador vinculado puede utilizar este parámetro.</span><span class="sxs-lookup"><span data-stu-id="365ee-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="365ee-247">La semántica debe definirse como se ha indicado anteriormente, ya que D2D inspeccionará la semántica para decidir cómo vincular funciones entre sí.</span><span class="sxs-lookup"><span data-stu-id="365ee-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="365ee-248">Si alguna entrada de función no coincide con uno de los tipos anteriores, la función se rechazará para la vinculación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="365ee-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="365ee-249">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="365ee-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="365ee-250">Asistentes hlsl</span><span class="sxs-lookup"><span data-stu-id="365ee-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="365ee-251">Interfaz ID3D11Linker</span><span class="sxs-lookup"><span data-stu-id="365ee-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="365ee-252">Interfaz ID3D11FunctionLinkingGraph</span><span class="sxs-lookup"><span data-stu-id="365ee-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 
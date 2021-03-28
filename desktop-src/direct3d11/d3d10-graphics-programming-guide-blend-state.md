---
title: Configuración de la funcionalidad de fusión
description: Las operaciones de combinación se realizan en cada salida del sombreador de píxeles (valor RGBA) antes de que el valor de salida se escriba en un destino de representación. Si el muestreo múltiple está habilitado, la combinación se realiza en cada muestreo múltiple; de lo contrario, se realiza la combinación en cada píxel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997064"
---
# <a name="configuring-blending-functionality"></a><span data-ttu-id="cf923-104">Configuración de la funcionalidad de fusión</span><span class="sxs-lookup"><span data-stu-id="cf923-104">Configuring Blending Functionality</span></span>

<span data-ttu-id="cf923-105">Las operaciones de combinación se realizan en cada salida del sombreador de píxeles (valor RGBA) antes de que el valor de salida se escriba en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="cf923-105">Blending operations are performed on every pixel shader output (RGBA value) before the output value is written to a render target.</span></span> <span data-ttu-id="cf923-106">Si el muestreo múltiple está habilitado, la combinación se realiza en cada muestreo múltiple; de lo contrario, se realiza la combinación en cada píxel.</span><span class="sxs-lookup"><span data-stu-id="cf923-106">If multisampling is enabled, blending is done on each multisample; otherwise, blending is performed on each pixel.</span></span>

-   [<span data-ttu-id="cf923-107">Crear el estado de Blend</span><span class="sxs-lookup"><span data-stu-id="cf923-107">Create the Blend State</span></span>](#create-the-blend-state)
-   [<span data-ttu-id="cf923-108">Enlazar el estado de Blend</span><span class="sxs-lookup"><span data-stu-id="cf923-108">Bind the Blend State</span></span>](#bind-the-blend-state)
-   [<span data-ttu-id="cf923-109">Temas de blending avanzado</span><span class="sxs-lookup"><span data-stu-id="cf923-109">Advanced Blending Topics</span></span>](#advanced-blending-topics)
    -   [<span data-ttu-id="cf923-110">Alfa a cobertura</span><span class="sxs-lookup"><span data-stu-id="cf923-110">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
    -   [<span data-ttu-id="cf923-111">Resultados del sombreador de píxeles de fusión</span><span class="sxs-lookup"><span data-stu-id="cf923-111">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)
-   [<span data-ttu-id="cf923-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf923-112">Related topics</span></span>](#related-topics)

## <a name="create-the-blend-state"></a><span data-ttu-id="cf923-113">Crear el estado de Blend</span><span class="sxs-lookup"><span data-stu-id="cf923-113">Create the Blend State</span></span>

<span data-ttu-id="cf923-114">El estado de blend es una colección de Estados que se usa para controlar la fusión.</span><span class="sxs-lookup"><span data-stu-id="cf923-114">The blend state is a collection of states used to control blending.</span></span> <span data-ttu-id="cf923-115">Estos Estados (definidos en [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) se usan para crear el objeto de estado de Blend llamando a [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span><span class="sxs-lookup"><span data-stu-id="cf923-115">These states (defined in [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) are used to create the blend state object by calling [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span></span>

<span data-ttu-id="cf923-116">Por ejemplo, a continuación se muestra un ejemplo muy sencillo de creación del estado de mezcla que deshabilita la combinación alfa y no utiliza el enmascaramiento de píxeles por componente.</span><span class="sxs-lookup"><span data-stu-id="cf923-116">For instance, here is a very simple example of blend-state creation that disables alpha blending and uses no per-component pixel masking.</span></span>


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



<span data-ttu-id="cf923-117">Este ejemplo es similar al [ejemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="cf923-117">This example is similar to the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="bind-the-blend-state"></a><span data-ttu-id="cf923-118">Enlazar el estado de Blend</span><span class="sxs-lookup"><span data-stu-id="cf923-118">Bind the Blend State</span></span>

<span data-ttu-id="cf923-119">Después de crear el objeto de estado de Blend, enlace el objeto de estado de mezcla a la fase de combinación de salida llamando a [**ID3D11DeviceContext:: OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="cf923-119">After you create the blend-state object, bind the blend-state object to the output-merger stage by calling [**ID3D11DeviceContext::OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span></span>


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



<span data-ttu-id="cf923-120">Esta API toma tres parámetros: el objeto de estado de mezcla, un factor de mezcla de cuatro componentes y una máscara de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cf923-120">This API takes three parameters: the blend-state object, a four-component blend factor, and a sample mask.</span></span> <span data-ttu-id="cf923-121">Puede pasar **null** para que el objeto de estado de mezcla especifique el estado de Blend predeterminado o pase un objeto de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="cf923-121">You can pass in **NULL** for the blend-state object to specify the default blend state or pass in a blend-state object.</span></span> <span data-ttu-id="cf923-122">Si creó el objeto de estado de Blend con el factor de mezcla de [**D3D11 \_ Blend \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) o el [**\_ factor de \_ \_ mezcla \_ de inv de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), puede pasar un factor de mezcla a los valores modulares para el sombreador de píxeles, el destino de representación o ambos.</span><span class="sxs-lookup"><span data-stu-id="cf923-122">If you created the blend-state object with [**D3D11\_BLEND\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) or [**D3D11\_BLEND\_INV\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), you can pass a blend factor to modulate values for the pixel shader, render target, or both.</span></span> <span data-ttu-id="cf923-123">Si no ha creado el objeto de estado de Blend con el factor de mezcla de **D3D11 \_ Blend \_ \_** o el **\_ \_ \_ \_ factor** de mezcla de inv de D3D11, puede pasar un factor de mezcla que no sea nulo, pero la fase de fusión no utiliza el factor de mezcla; el Runtime almacena el factor de mezcla y, posteriormente, puede llamar a [**ID3D11DeviceContext:: OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) para recuperar el factor de mezcla.</span><span class="sxs-lookup"><span data-stu-id="cf923-123">If you didn't create the blend-state object with **D3D11\_BLEND\_BLEND\_FACTOR** or **D3D11\_BLEND\_INV\_BLEND\_FACTOR**, you can still pass a non-NULL blend factor, but the blending stage does not use the blend factor; the runtime stores the blend factor, and you can later call [**ID3D11DeviceContext::OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) to retrieve the blend factor.</span></span> <span data-ttu-id="cf923-124">Si se pasa **null**, el motor en tiempo de ejecución usa o almacena un factor de mezcla igual a {1, 1, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="cf923-124">If you pass **NULL**, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.</span></span> <span data-ttu-id="cf923-125">La máscara de ejemplo es una máscara definida por el usuario que determina cómo se muestra el destino de representación existente antes de actualizarlo.</span><span class="sxs-lookup"><span data-stu-id="cf923-125">The sample mask is a user-defined mask that determines how to sample the existing render target before updating it.</span></span> <span data-ttu-id="cf923-126">La máscara de muestreo predeterminada es 0xFFFFFFFF, que designa el muestreo del punto.</span><span class="sxs-lookup"><span data-stu-id="cf923-126">The default sampling mask is 0xffffffff which designates point sampling.</span></span>

<span data-ttu-id="cf923-127">En la mayoría de los esquemas de almacenamiento en búfer, el píxel más cercano a la cámara es el que se dibuja.</span><span class="sxs-lookup"><span data-stu-id="cf923-127">In most depth buffering schemes, the pixel closest to the camera is the one that gets drawn.</span></span> <span data-ttu-id="cf923-128">Al [configurar el estado de la galería de símbolos de profundidad](d3d10-graphics-programming-guide-depth-stencil.md), el miembro **DepthFunc** de la [**Galería de \_ símbolos de profundidad \_ \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) puede ser cualquier función de [**\_ comparación \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="cf923-128">When [setting up the depth stencil state](d3d10-graphics-programming-guide-depth-stencil.md), the **DepthFunc** member of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) can be any [**D3D11\_COMPARISON\_FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span></span> <span data-ttu-id="cf923-129">Normalmente, desearía que **DepthFunc** se D3D11 de la **\_ comparación \_ menos**, de modo que los píxeles más cercanos a la cámara sobrescribirán los píxeles que se encuentran detrás.</span><span class="sxs-lookup"><span data-stu-id="cf923-129">Normally, you would want **DepthFunc** to be **D3D11\_COMPARISON\_LESS**, so that the pixels closest to the camera will overwrite the pixels behind them.</span></span> <span data-ttu-id="cf923-130">Sin embargo, en función de las necesidades de la aplicación, se puede usar cualquiera de las demás funciones de comparación para realizar la prueba de profundidad.</span><span class="sxs-lookup"><span data-stu-id="cf923-130">However, depending on the needs of your application, any of the other comparison functions may be used to do the depth test.</span></span>

## <a name="advanced-blending-topics"></a><span data-ttu-id="cf923-131">Temas de blending avanzado</span><span class="sxs-lookup"><span data-stu-id="cf923-131">Advanced Blending Topics</span></span>

-   [<span data-ttu-id="cf923-132">Alfa a cobertura</span><span class="sxs-lookup"><span data-stu-id="cf923-132">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
-   [<span data-ttu-id="cf923-133">Resultados del sombreador de píxeles de fusión</span><span class="sxs-lookup"><span data-stu-id="cf923-133">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a><span data-ttu-id="cf923-134">Alfa a cobertura</span><span class="sxs-lookup"><span data-stu-id="cf923-134">Alpha-To-Coverage</span></span>

<span data-ttu-id="cf923-135">Alpha-to-Coverage es una técnica de muestreo múltiple que es más útil para situaciones como el follaje denso, donde hay varios polígonos superpuestos que usan transparencia alfa para definir bordes dentro de la superficie.</span><span class="sxs-lookup"><span data-stu-id="cf923-135">Alpha-to-coverage is a multisampling technique that is most useful for situations such as dense foliage where there are several overlapping polygons that use alpha transparency to define edges within the surface.</span></span>

<span data-ttu-id="cf923-136">Puede usar el miembro **AlphaToCoverageEnable** de [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) o [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) para alternar si el Runtime convierte. un componente (alfa) del registro de salida VP de [ \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 del sombreador de píxeles a una máscara de cobertura de n pasos (dado un valor de **RenderTarget** de ejemplo n).</span><span class="sxs-lookup"><span data-stu-id="cf923-136">You can use the **AlphaToCoverageEnable** member of [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) or [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) to toggle whether the runtime converts the .a component (alpha) of output register [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 from the pixel shader to an n-step coverage mask (given an n-sample **RenderTarget**).</span></span> <span data-ttu-id="cf923-137">El motor en tiempo de ejecución realiza una operación **and** de esta máscara con la cobertura de ejemplo típica para el píxel de la primitiva (además de la máscara de ejemplo) para determinar qué ejemplos se deben actualizar en todas las **RenderTarget** activas.</span><span class="sxs-lookup"><span data-stu-id="cf923-137">The runtime performs an **AND** operation of this mask with the typical sample coverage for the pixel in the primitive (in addition to the sample mask) to determine which samples to update in all the active **RenderTarget** s.</span></span>

<span data-ttu-id="cf923-138">Si el sombreador de píxeles produce la [ \_ cobertura](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de la VP, el tiempo de ejecución deshabilita la de alfa a cobertura.</span><span class="sxs-lookup"><span data-stu-id="cf923-138">If the pixel shader outputs [SV\_Coverage](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), the runtime disables alpha-to-coverage.</span></span>

> [!Note]  
> <span data-ttu-id="cf923-139">En el muestreo múltiple, el Runtime solo comparte una cobertura para todos los objetos **RenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="cf923-139">In multisampling, the runtime shares only one coverage for all **RenderTarget** s.</span></span> <span data-ttu-id="cf923-140">El hecho de que el tiempo de ejecución de Lea y convierta. a del [ \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de la VP de salida 0 a la cobertura cuando **AlphaToCoverageEnable** es true no cambia. un valor que se dirige al mezclador en **RenderTarget** 0 (si se produce un error de **RenderTarget** ).</span><span class="sxs-lookup"><span data-stu-id="cf923-140">The fact that the runtime reads and converts .a from output [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 to coverage when **AlphaToCoverageEnable** is TRUE does not change the .a value that goes to the blender at **RenderTarget** 0 (if a **RenderTarget** happens to be set there).</span></span> <span data-ttu-id="cf923-141">En general, si habilita la operación de alfa a cobertura, no afecta al modo en que todas las salidas de color de los sombreadores de píxeles interactúan con **RenderTarget** s a través de la [fase de fusión de salida](d3d10-graphics-programming-guide-output-merger-stage.md) , salvo que el Runtime realiza una operación **and** de la máscara de cobertura con la máscara de alfa a cobertura.</span><span class="sxs-lookup"><span data-stu-id="cf923-141">In general, if you enable alpha-to-coverage, you don't affect how all color outputs from pixel shaders interact with **RenderTarget** s through the [output-merger stage](d3d10-graphics-programming-guide-output-merger-stage.md) except that the runtime performs an **AND** operation of the coverage mask with the alpha-to-coverage mask.</span></span> <span data-ttu-id="cf923-142">Alpha-to-Coverage funciona de forma independiente a si el runtime puede mezclar **RenderTarget** o si se usa la combinación en **RenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="cf923-142">Alpha-to-coverage works independently to whether the runtime can blend **RenderTarget** or whether you use blending on **RenderTarget**.</span></span>

 

<span data-ttu-id="cf923-143">El hardware de gráficos no especifica exactamente el modo en que convierte el [ \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de la VP del sombreador de píxeles 0. a (alfa) en una máscara de cobertura, salvo que el valor alfa de 0 (o menos) debe estar asignado a ninguna cobertura y el alfa de 1 (o superior) debe asignarse a la cobertura completa (antes de que el tiempo de ejecución realice una operación **and** con</span><span class="sxs-lookup"><span data-stu-id="cf923-143">Graphics hardware doesn't precisely specify exactly how it converts pixel shader [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0.a (alpha) to a coverage mask, except that alpha of 0 (or less) must map to no coverage and alpha of 1 (or greater) must map to full coverage (before the runtime performs an **AND** operation with actual primitive coverage).</span></span> <span data-ttu-id="cf923-144">Como el alfa va de 0 a 1, la cobertura resultante debería aumentar de forma continuada.</span><span class="sxs-lookup"><span data-stu-id="cf923-144">As alpha goes from 0 to 1, the resulting coverage should generally increase monotonically.</span></span> <span data-ttu-id="cf923-145">Sin embargo, el hardware puede realizar una interpolación de área para proporcionar una mejor cuantificación de los valores alfa a costa de la resolución espacial y el ruido.</span><span class="sxs-lookup"><span data-stu-id="cf923-145">However, hardware might perform area dithering to provide some better quantization of alpha values at the cost of spatial resolution and noise.</span></span> <span data-ttu-id="cf923-146">Un valor alfa de NaN (no un número) da como resultado una máscara sin cobertura (cero).</span><span class="sxs-lookup"><span data-stu-id="cf923-146">An alpha value of NaN (Not a Number) results in a no coverage (zero) mask.</span></span>

<span data-ttu-id="cf923-147">La utilización de Alpha-to-Coverage también se usa tradicionalmente para la transparencia de la puerta de pantalla o la definición de siluetas detalladas para sprites opacos de otro modo.</span><span class="sxs-lookup"><span data-stu-id="cf923-147">Alpha-to-coverage is also traditionally used for screen-door transparency or defining detailed silhouettes for otherwise opaque sprites.</span></span>

### <a name="blending-pixel-shader-outputs"></a><span data-ttu-id="cf923-148">Resultados del sombreador de píxeles de fusión</span><span class="sxs-lookup"><span data-stu-id="cf923-148">Blending Pixel Shader Outputs</span></span>

<span data-ttu-id="cf923-149">Esta característica permite que la fusión de salida Use las salidas del sombreador de píxeles simultáneamente como orígenes de entrada para una operación de combinación con el destino de representación único en la ranura 0.</span><span class="sxs-lookup"><span data-stu-id="cf923-149">This feature enables the output merger to use both the pixel shader outputs simultaneously as input sources to a blending operation with the single render target at slot 0.</span></span>

<span data-ttu-id="cf923-150">Este ejemplo toma dos resultados y los combina en un solo paso, mezclando uno en el destino con una multiplicación y el otro con un agregado:</span><span class="sxs-lookup"><span data-stu-id="cf923-150">This example takes two results and combines them in a single pass, blending one into the destination with a multiply and the other with an add:</span></span>


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



<span data-ttu-id="cf923-151">En este ejemplo se configura la salida del primer sombreador de píxeles como el color de origen y la segunda salida como factor de mezcla de componentes por color.</span><span class="sxs-lookup"><span data-stu-id="cf923-151">This example configures the first pixel shader output as the source color and the second output as a per-color component blend factor.</span></span>


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



<span data-ttu-id="cf923-152">En este ejemplo se muestra cómo los factores de mezcla deben coincidir con el sombreador swizzles:</span><span class="sxs-lookup"><span data-stu-id="cf923-152">This example illustrates how the blend factors must match the shader swizzles:</span></span>


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



<span data-ttu-id="cf923-153">Juntos, los factores de mezcla y el código del sombreador implican que el sombreador de píxeles es necesario para generar al menos O0. r y O1. a.</span><span class="sxs-lookup"><span data-stu-id="cf923-153">Together, the blend factors and the shader code imply that the pixel shader is required to output at least o0.r and o1.a.</span></span> <span data-ttu-id="cf923-154">Los componentes de salida adicionales pueden ser generados por el sombreador, pero se omitirán, menos componentes generarán resultados sin definir.</span><span class="sxs-lookup"><span data-stu-id="cf923-154">Extra output components can be output by the shader but would be ignored, fewer components would produce undefined results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf923-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf923-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf923-156">Fase de combinación de salida</span><span class="sxs-lookup"><span data-stu-id="cf923-156">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="cf923-157">Fases de canalización (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="cf923-157">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 
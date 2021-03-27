---
title: Configuración de la funcionalidad de Depth-Stencil
description: En esta sección se explican los pasos para configurar el búfer de estarcido de profundidad y el estado de la galería de símbolos de profundidad para la fase de combinación de salida.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792706"
---
# <a name="configuring-depth-stencil-functionality"></a><span data-ttu-id="c220d-103">Configuración de la funcionalidad de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="c220d-103">Configuring Depth-Stencil Functionality</span></span>

<span data-ttu-id="c220d-104">En esta sección se explican los pasos para configurar el búfer de estarcido de profundidad y el estado de la galería de símbolos de profundidad para la fase de combinación de salida.</span><span class="sxs-lookup"><span data-stu-id="c220d-104">This section covers the steps for setting up the depth-stencil buffer, and depth-stencil state for the output-merger stage.</span></span>

-   [<span data-ttu-id="c220d-105">Creación de un recurso de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="c220d-105">Create a Depth-Stencil Resource</span></span>](#create-a-depth-stencil-resource)
-   [<span data-ttu-id="c220d-106">Crear estado de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="c220d-106">Create Depth-Stencil State</span></span>](#create-depth-stencil-state)
-   [<span data-ttu-id="c220d-107">Enlazar datos de Depth-Stencil a la fase de OM</span><span class="sxs-lookup"><span data-stu-id="c220d-107">Bind Depth-Stencil Data to the OM Stage</span></span>](#bind-depth-stencil-data-to-the-om-stage)

<span data-ttu-id="c220d-108">Una vez que sepa cómo usar el búfer de estarcido de profundidad y el estado de la galería de símbolos de profundidad correspondiente, consulte [técnicas avanzadas de estarcido](#advanced-stencil-techniques).</span><span class="sxs-lookup"><span data-stu-id="c220d-108">Once you know how to use the depth-stencil buffer and the corresponding depth-stencil state, refer to [advanced-stencil techniques](#advanced-stencil-techniques).</span></span>

## <a name="create-a-depth-stencil-resource"></a><span data-ttu-id="c220d-109">Creación de un recurso de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="c220d-109">Create a Depth-Stencil Resource</span></span>

<span data-ttu-id="c220d-110">Cree el búfer de estarcido de profundidad con un recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="c220d-110">Create the depth-stencil buffer using a texture resource.</span></span>


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a><span data-ttu-id="c220d-111">Crear estado de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="c220d-111">Create Depth-Stencil State</span></span>

<span data-ttu-id="c220d-112">El estado de la galería de símbolos de profundidad indica a la fase de combinación de salida cómo realizar la [prueba de la galería de símbolos de profundidad](d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="c220d-112">The depth-stencil state tells the output-merger stage how to perform the [depth-stencil test](d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="c220d-113">La prueba de profundidad-estarcido determina si se debe dibujar un píxel determinado.</span><span class="sxs-lookup"><span data-stu-id="c220d-113">The depth-stencil test determines whether or not a given pixel should be drawn.</span></span>


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



<span data-ttu-id="c220d-114">DepthEnable y StencilEnable habilitan (y deshabilitan) las pruebas de profundidad y estarcido.</span><span class="sxs-lookup"><span data-stu-id="c220d-114">DepthEnable and StencilEnable enable (and disable) depth and stencil testing.</span></span> <span data-ttu-id="c220d-115">Establezca DepthEnable en **false** para deshabilitar las pruebas de profundidad y evitar la escritura en el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="c220d-115">Set DepthEnable to **FALSE** to disable depth testing and prevent writing to the depth buffer.</span></span> <span data-ttu-id="c220d-116">Establezca StencilEnable en **false** para deshabilitar las pruebas de estarcido y evitar la escritura en el búfer de estarcido (cuando DepthEnable es **false** y StencilEnable es **true**, la prueba de profundidad siempre pasa en la operación de estarcido).</span><span class="sxs-lookup"><span data-stu-id="c220d-116">Set StencilEnable to **FALSE** to disable stencil testing and prevent writing to the stencil buffer (when DepthEnable is **FALSE** and StencilEnable is **TRUE**, the depth test always passes in the stencil operation).</span></span>

<span data-ttu-id="c220d-117">DepthEnable solo afecta a la fase de combinación de salida, no afecta al recorte, a la diferencia de profundidad ni a la fijación de valores antes de que los datos se escriban en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c220d-117">DepthEnable only affects the output-merger stage - it does not affect clipping, depth bias, or clamping of values before the data is input to a pixel shader.</span></span>

## <a name="bind-depth-stencil-data-to-the-om-stage"></a><span data-ttu-id="c220d-118">Enlazar datos de Depth-Stencil a la fase de OM</span><span class="sxs-lookup"><span data-stu-id="c220d-118">Bind Depth-Stencil Data to the OM Stage</span></span>

<span data-ttu-id="c220d-119">Enlazar el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="c220d-119">Bind the depth-stencil state.</span></span>


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



<span data-ttu-id="c220d-120">Enlazar el recurso de la galería de símbolos de profundidad mediante una vista.</span><span class="sxs-lookup"><span data-stu-id="c220d-120">Bind the depth-stencil resource using a view.</span></span>


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



<span data-ttu-id="c220d-121">Se puede pasar una matriz de vistas de representación-destino a [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), pero todas esas vistas de destino de representación se corresponden con una vista de galería de símbolos de profundidad única.</span><span class="sxs-lookup"><span data-stu-id="c220d-121">An array of render-target views may be passed into [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), however all of those render-target views will correspond to a single depth stencil view.</span></span> <span data-ttu-id="c220d-122">La matriz de destino de representación en Direct3D 11 es una característica que permite que una aplicación se represente en varios destinos de representación simultáneamente en el nivel primitivo.</span><span class="sxs-lookup"><span data-stu-id="c220d-122">The render target array in Direct3D 11 is a feature that enables an application to render onto multiple render targets simultaneously at the primitive level.</span></span> <span data-ttu-id="c220d-123">Las matrices de destino de representación ofrecen mayor rendimiento que la configuración individual de destinos de representación con varias llamadas a **ID3D11DeviceContext:: OMSetRenderTargets** (esencialmente, el método empleado en Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="c220d-123">Render target arrays offer increased performance over individually setting render targets with multiple calls to **ID3D11DeviceContext::OMSetRenderTargets** (essentially the method employed in Direct3D 9).</span></span>

<span data-ttu-id="c220d-124">Todos los destinos de representación deben ser del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c220d-124">Render targets must all be the same type of resource.</span></span> <span data-ttu-id="c220d-125">Si se usa el suavizado de contorno Multimuestra, todos los destinos de representación enlazados y los búferes de profundidad deben tener el mismo número de muestras.</span><span class="sxs-lookup"><span data-stu-id="c220d-125">If multisample antialiasing is used, all bound render targets and depth buffers must have the same sample counts.</span></span>

<span data-ttu-id="c220d-126">Cuando se usa un búfer como destino de representación, no se admiten las pruebas de la galería de símbolos de profundidad y los diversos destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="c220d-126">When a buffer is used as a render target, depth-stencil testing and multiple render targets are not supported.</span></span>

-   <span data-ttu-id="c220d-127">Hasta 8 destinos de representación se pueden enlazar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="c220d-127">As many as 8 render targets can be bound simultaneously.</span></span>
-   <span data-ttu-id="c220d-128">Todos los destinos de representación deben tener el mismo tamaño en todas las dimensiones (ancho y alto, y profundidad para el tamaño 3D o de la matriz para los \* tipos de matriz).</span><span class="sxs-lookup"><span data-stu-id="c220d-128">All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for \*Array types).</span></span>
-   <span data-ttu-id="c220d-129">Cada destino de representación puede tener un formato de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="c220d-129">Each render target may have a different data format.</span></span>
-   <span data-ttu-id="c220d-130">Las máscaras de escritura controlan los datos que se escriben en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="c220d-130">Write masks control what data gets written to a render target.</span></span> <span data-ttu-id="c220d-131">El control de máscaras de escritura de salida controla el destino de cada representación y el nivel de cada componente de los datos que se escriben en los destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="c220d-131">The output write masks control on a per-render target, per-component level what data gets written to the render target(s).</span></span>

## <a name="advanced-stencil-techniques"></a><span data-ttu-id="c220d-132">Técnicas avanzadas de estarcido</span><span class="sxs-lookup"><span data-stu-id="c220d-132">Advanced Stencil Techniques</span></span>

<span data-ttu-id="c220d-133">La parte de la galería de símbolos del búfer de estarcido de profundidad se puede usar para crear efectos de representación como composición, alineación y esquematización.</span><span class="sxs-lookup"><span data-stu-id="c220d-133">The stencil portion of the depth-stencil buffer can be used for creating rendering effects such as compositing, decaling, and outlining.</span></span>

-   [<span data-ttu-id="c220d-134">Composición</span><span class="sxs-lookup"><span data-stu-id="c220d-134">Compositing</span></span>](#compositing)
-   [<span data-ttu-id="c220d-135">Marcas</span><span class="sxs-lookup"><span data-stu-id="c220d-135">Decaling</span></span>](#decaling)
-   [<span data-ttu-id="c220d-136">Contornos y siluetas</span><span class="sxs-lookup"><span data-stu-id="c220d-136">Outlines and Silhouettes</span></span>](#outlines-and-silhouettes)
-   [<span data-ttu-id="c220d-137">Galería de símbolos de dos caras</span><span class="sxs-lookup"><span data-stu-id="c220d-137">Two-Sided Stencil</span></span>](#two-sided-stencil)
-   [<span data-ttu-id="c220d-138">Leer el búfer de Depth-Stencil como una textura</span><span class="sxs-lookup"><span data-stu-id="c220d-138">Reading the Depth-Stencil Buffer as a Texture</span></span>](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a><span data-ttu-id="c220d-139">Composición</span><span class="sxs-lookup"><span data-stu-id="c220d-139">Compositing</span></span>

<span data-ttu-id="c220d-140">La aplicación puede usar el búfer de estarcido para componer imágenes 2D o 3D en una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="c220d-140">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="c220d-141">Se utiliza una máscara en el búfer de estarcido para tapabar un área de la superficie de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="c220d-141">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="c220d-142">La información de 2D almacenada, como texto o mapas de bits, se puede escribir en el área ocluidos.</span><span class="sxs-lookup"><span data-stu-id="c220d-142">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="c220d-143">Como alternativa, la aplicación puede representar primitivos 3D adicionales en la región enmascarada de estarcido de la superficie de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="c220d-143">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="c220d-144">Incluso puede representar una escena completa.</span><span class="sxs-lookup"><span data-stu-id="c220d-144">It can even render an entire scene.</span></span>

<span data-ttu-id="c220d-145">A menudo, los juegos componen varias escenas 3D juntas.</span><span class="sxs-lookup"><span data-stu-id="c220d-145">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="c220d-146">Por ejemplo, los juegos de conducción suelen mostrar un reflejo de la vista trasera.</span><span class="sxs-lookup"><span data-stu-id="c220d-146">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="c220d-147">El reflejo contiene la vista de la escena 3D detrás del controlador.</span><span class="sxs-lookup"><span data-stu-id="c220d-147">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="c220d-148">En esencia, es una segunda escena 3D compuesta con la vista hacia delante del controlador.</span><span class="sxs-lookup"><span data-stu-id="c220d-148">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

### <a name="decaling"></a><span data-ttu-id="c220d-149">Marcas</span><span class="sxs-lookup"><span data-stu-id="c220d-149">Decaling</span></span>

<span data-ttu-id="c220d-150">Las aplicaciones de Direct3D usan las marcas para controlar qué píxeles de una imagen primitiva determinada se dibujan en la superficie de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="c220d-150">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="c220d-151">Las aplicaciones aplican marcas a las imágenes de primitivas para permitir que los polígonos coplanoles se representen correctamente.</span><span class="sxs-lookup"><span data-stu-id="c220d-151">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="c220d-152">Por ejemplo, al aplicar las marcas de neumático y las líneas amarillas a un Roadway, las marcas deben aparecer directamente encima de la carretera.</span><span class="sxs-lookup"><span data-stu-id="c220d-152">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="c220d-153">Sin embargo, los valores z de las marcas y la carretera son los mismos.</span><span class="sxs-lookup"><span data-stu-id="c220d-153">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="c220d-154">Por lo tanto, es posible que el búfer de profundidad no produzca una separación limpia entre ambos.</span><span class="sxs-lookup"><span data-stu-id="c220d-154">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="c220d-155">Algunos píxeles de la primitiva inversa se pueden representar encima de la primitiva delantera y viceversa.</span><span class="sxs-lookup"><span data-stu-id="c220d-155">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="c220d-156">La imagen resultante parece Shimmer de fotograma a fotograma.</span><span class="sxs-lookup"><span data-stu-id="c220d-156">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="c220d-157">Este efecto se denomina lucha z o flimmering.</span><span class="sxs-lookup"><span data-stu-id="c220d-157">This effect is called z-fighting or flimmering.</span></span>

<span data-ttu-id="c220d-158">Para solucionar este problema, use una galería de símbolos para enmascarar la sección de la primitiva inversa en la que aparecerá la calcomanía.</span><span class="sxs-lookup"><span data-stu-id="c220d-158">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="c220d-159">Desactive el almacenamiento en búfer z y represente la imagen de la primitiva delantera en el área enmascarada de la superficie de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="c220d-159">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="c220d-160">Se puede usar la combinación de varias texturas para resolver este problema.</span><span class="sxs-lookup"><span data-stu-id="c220d-160">Multiple texture blending can be used to solve this problem.</span></span>

### <a name="outlines-and-silhouettes"></a><span data-ttu-id="c220d-161">Contornos y siluetas</span><span class="sxs-lookup"><span data-stu-id="c220d-161">Outlines and Silhouettes</span></span>

<span data-ttu-id="c220d-162">Puede usar el búfer de estarcido para efectos más abstractos, como la esquematización y la silhouetting.</span><span class="sxs-lookup"><span data-stu-id="c220d-162">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="c220d-163">Si la aplicación realiza dos fases de representación: una para generar la máscara de la galería de símbolos y la segunda para aplicar la máscara de la galería de símbolos a la imagen, pero con los primitivos ligeramente más pequeños en el segundo paso: la imagen resultante contendrá solo el contorno de la primitiva.</span><span class="sxs-lookup"><span data-stu-id="c220d-163">If your application does two render passes - one to generate the stencil mask and second to apply the stencil mask to the image, but with the primitives slightly smaller on the second pass - the resulting image will contain only the primitive's outline.</span></span> <span data-ttu-id="c220d-164">A continuación, la aplicación puede rellenar el área enmascarada de estarcido de la imagen con un color sólido, lo que proporciona al primitivo una apariencia en relieve.</span><span class="sxs-lookup"><span data-stu-id="c220d-164">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="c220d-165">Si la máscara de la galería de símbolos tiene el mismo tamaño y forma que la primitiva que se está representando, la imagen resultante contiene un hueco en el que el primitivo debe ser.</span><span class="sxs-lookup"><span data-stu-id="c220d-165">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="c220d-166">A continuación, la aplicación puede rellenar el hueco con negro para producir una silueta de la primitiva.</span><span class="sxs-lookup"><span data-stu-id="c220d-166">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

### <a name="two-sided-stencil"></a><span data-ttu-id="c220d-167">Two-Sided Galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="c220d-167">Two-Sided Stencil</span></span>

<span data-ttu-id="c220d-168">Los volúmenes de sombra se usan para dibujar sombras con el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="c220d-168">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="c220d-169">La aplicación calcula los volúmenes de sombra convertidos por geometría occluding, mediante el cálculo de los bordes de la silueta y la extrusión de la luz en un conjunto de volúmenes 3D.</span><span class="sxs-lookup"><span data-stu-id="c220d-169">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="c220d-170">A continuación, estos volúmenes se representan dos veces en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="c220d-170">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="c220d-171">La primera representación dibuja polígonos hacia delante e incrementa los valores del búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="c220d-171">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="c220d-172">La segunda representación dibuja los polígonos hacia delante del volumen de instantáneas y disminuye los valores de búfer de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="c220d-172">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="c220d-173">Normalmente, todos los valores incrementados y disminuidos se cancelan entre sí. Sin embargo, la escena ya se representó con geometría normal, lo que provoca que algunos píxeles no superen la prueba de búfer z mientras se representa el volumen de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="c220d-173">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="c220d-174">Los valores que quedan en el búfer de estarcido se corresponden con los píxeles que están en la sombra.</span><span class="sxs-lookup"><span data-stu-id="c220d-174">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="c220d-175">El resto del contenido del búfer de la galería de símbolos se usa como máscara, para que la combinación de alfa sea una gran cantidad de color negro que abarque a la escena.</span><span class="sxs-lookup"><span data-stu-id="c220d-175">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="c220d-176">Con el búfer de estarcido que actúa como máscara, el resultado es oscurecer los píxeles que se encuentran en las sombras.</span><span class="sxs-lookup"><span data-stu-id="c220d-176">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="c220d-177">Esto significa que la geometría de la sombra se dibuja dos veces por origen de la luz, por lo que se pone presión sobre el rendimiento de los vértices de la GPU.</span><span class="sxs-lookup"><span data-stu-id="c220d-177">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="c220d-178">La característica de galería de símbolos de dos caras se ha diseñado para mitigar esta situación.</span><span class="sxs-lookup"><span data-stu-id="c220d-178">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="c220d-179">En este enfoque, hay dos conjuntos de estado de la galería de símbolos (denominados a continuación), uno para cada uno de los triángulos orientados delante y otro para los triángulos de cara a la inversa.</span><span class="sxs-lookup"><span data-stu-id="c220d-179">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="c220d-180">De este modo, solo se dibuja un único paso por volumen de instantánea, por luz.</span><span class="sxs-lookup"><span data-stu-id="c220d-180">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="c220d-181">En el [ejemplo ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx)se puede encontrar un ejemplo de implementación de una galería de símbolos de dos caras.</span><span class="sxs-lookup"><span data-stu-id="c220d-181">An example of two-sided stencil implementation can be found in the [ShadowVolume10 Sample](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span></span>

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a><span data-ttu-id="c220d-182">Leer el búfer de Depth-Stencil como una textura</span><span class="sxs-lookup"><span data-stu-id="c220d-182">Reading the Depth-Stencil Buffer as a Texture</span></span>

<span data-ttu-id="c220d-183">Un sombreador puede leer un búfer de estarcido de profundidad inactivo como textura.</span><span class="sxs-lookup"><span data-stu-id="c220d-183">An inactive depth-stencil buffer can be read by a shader as a texture.</span></span> <span data-ttu-id="c220d-184">Una aplicación que lee un búfer de estarcido de profundidad como una textura se representa en dos fases, la primera pasada escribe en el búfer de la galería de símbolos de profundidad y el segundo paso Lee del búfer.</span><span class="sxs-lookup"><span data-stu-id="c220d-184">An application that reads a depth-stencil buffer as a texture renders in two passes, the first pass writes to the depth-stencil buffer and the second pass reads from the buffer.</span></span> <span data-ttu-id="c220d-185">Esto permite a un sombreador comparar los valores de profundidad o de estarcido previamente escritos en el búfer con el valor de la Currrently de píxeles que se está representando.</span><span class="sxs-lookup"><span data-stu-id="c220d-185">This allows a shader to compare depth or stencil values previously written to the buffer against the value for the pixel currrently being rendered.</span></span> <span data-ttu-id="c220d-186">El resultado de la comparación se puede usar para crear efectos como la asignación de sombras o las partículas flexibles en un sistema de partículas.</span><span class="sxs-lookup"><span data-stu-id="c220d-186">The result of the comparison can be used to create effects such as shadow mapping or soft particles in a particle system.</span></span>

<span data-ttu-id="c220d-187">Para crear un búfer de estarcido de profundidad que se pueda usar como un recurso de estarcido de profundidad y un recurso de sombreador, es necesario realizar algunos cambios en el código de ejemplo de la sección [crear un recurso de Depth-Stencil](#create-a-depth-stencil-resource) .</span><span class="sxs-lookup"><span data-stu-id="c220d-187">To create a depth-stencil buffer that can be used as both a depth-stencil resource and a shader resource a few changes need to be made to sample code in the [Create a Depth-Stencil Resource](#create-a-depth-stencil-resource) section.</span></span>

-   <span data-ttu-id="c220d-188">El recurso de la galería de símbolos de profundidad debe tener un formato sin tipo, como el formato de DXGI \_ \_ R32 \_ sin tipo.</span><span class="sxs-lookup"><span data-stu-id="c220d-188">The depth-stencil resource must have a typeless format such as DXGI\_FORMAT\_R32\_TYPELESS.</span></span>
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   <span data-ttu-id="c220d-189">El recurso de la galería de símbolos de profundidad debe usar tanto la galería de símbolos de \_ profundidad de enlace D3D10 como las marcas de enlace del \_ \_ \_ recurso de sombreador de enlace D3D10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c220d-189">The depth-stencil resource must use both the D3D10\_BIND\_DEPTH\_STENCIL and D3D10\_BIND\_SHADER\_RESOURCE bind flags.</span></span>
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

<span data-ttu-id="c220d-190">Además, es necesario crear una vista de recursos del sombreador para el búfer de profundidad mediante una estructura de DESC de la [**\_ vista de \_ recursos \_ \_ del sombreador D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) y [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="c220d-190">In addition a shader resource view needs to be created for the depth buffer using a [**D3D11\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) structure and [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span></span> <span data-ttu-id="c220d-191">La vista de recursos del sombreador usará un formato con tipo como **DXGI \_ format \_ R32 \_ float** equivalente al formato sin tipo especificado cuando se creó el recurso de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="c220d-191">The shader resource view will use a typed format such as **DXGI\_FORMAT\_R32\_FLOAT** that is the equivalent to the typeless format specified when the depth-stencil resource was created.</span></span>

<span data-ttu-id="c220d-192">En la primera fase de representación, el búfer de profundidad se enlaza tal y como se describe en la sección [enlazar Depth-Stencil datos a la fase de OM](#bind-depth-stencil-data-to-the-om-stage) .</span><span class="sxs-lookup"><span data-stu-id="c220d-192">In the first render pass the depth buffer is bound as described in the [Bind Depth-Stencil Data to the OM Stage](#bind-depth-stencil-data-to-the-om-stage) section.</span></span> <span data-ttu-id="c220d-193">Tenga en cuenta que el formato que se pasa a [**D3D11 \_ Depth \_ estarcido \_ View \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Format usará un formato con tipo como **DXGI \_ format \_ D32 \_ float**.</span><span class="sxs-lookup"><span data-stu-id="c220d-193">Note that the format passed to [**D3D11\_DEPTH\_STENCIL\_VIEW\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc).Format will use a typed format such as **DXGI\_FORMAT\_D32\_FLOAT**.</span></span> <span data-ttu-id="c220d-194">Después del primer paso de representación, el búfer de profundidad contendrá los valores de profundidad de la escena.</span><span class="sxs-lookup"><span data-stu-id="c220d-194">After the first render pass the depth buffer will contain the depth values for the scene.</span></span>

<span data-ttu-id="c220d-195">En el segundo paso de representación, la función [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) se usa para establecer la vista de la galería de símbolos de profundidad en **null** o en un recurso de estarcido de profundidad diferente y la vista de recursos del sombreador se pasa al sombreador mediante [**ID3D11EffectShaderResourceVariable:: SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span><span class="sxs-lookup"><span data-stu-id="c220d-195">In the second render pass the [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) function is used to set the depth-stencil view to **NULL** or a different depth-stencil resource and the shader resource view is passed to the shader using [**ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span></span> <span data-ttu-id="c220d-196">Esto permite al sombreador buscar los valores de profundidad calculados en la primera fase de representación.</span><span class="sxs-lookup"><span data-stu-id="c220d-196">This allows the shader to look up the depth values calculated in the first rendering pass.</span></span> <span data-ttu-id="c220d-197">Tenga en cuenta que se debe aplicar una transformación para recuperar los valores de profundidad si el punto de vista de la primera fase de representación es diferente de la segunda fase de representación.</span><span class="sxs-lookup"><span data-stu-id="c220d-197">Note that a transformation will need to be applied to retrieve depth values if the point of view of the first render pass is different from the second render pass.</span></span> <span data-ttu-id="c220d-198">Por ejemplo, si se usa una técnica de asignación de instantáneas, la primera fase de representación será desde la perspectiva de una fuente de luz, mientras que la segunda pasa desde la perspectiva del visor.</span><span class="sxs-lookup"><span data-stu-id="c220d-198">For example, if a shadow mapping technique is being used the first render pass will be from the perspective of a light source while the second render pass will from the viewer's perspective.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c220d-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c220d-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c220d-200">Fase de combinación de salida</span><span class="sxs-lookup"><span data-stu-id="c220d-200">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="c220d-201">Fases de canalización (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c220d-201">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 
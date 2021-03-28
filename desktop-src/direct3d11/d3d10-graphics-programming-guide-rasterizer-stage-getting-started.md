---
title: Introducción con la fase de rasterizador
description: En esta sección se describe la configuración de la ventanilla, el rectángulo de tijeras, el estado de rasterizador y el muestreo múltiple.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- muestreo múltiple, estado de rasterizador (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359000"
---
# <a name="getting-started-with-the-rasterizer-stage"></a><span data-ttu-id="9e57e-104">Introducción con la fase de rasterizador</span><span class="sxs-lookup"><span data-stu-id="9e57e-104">Getting Started with the Rasterizer Stage</span></span>

<span data-ttu-id="9e57e-105">En esta sección se describe la configuración de la ventanilla, el rectángulo de tijeras, el estado de rasterizador y el muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="9e57e-105">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span>

## <a name="set-the-viewport"></a><span data-ttu-id="9e57e-106">Establecer la ventanilla</span><span class="sxs-lookup"><span data-stu-id="9e57e-106">Set the Viewport</span></span>

<span data-ttu-id="9e57e-107">Una ventanilla asigna las posiciones de los vértices (en el espacio de recorte) en las posiciones de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="9e57e-107">A viewport maps vertex positions (in clip space) into render target positions.</span></span> <span data-ttu-id="9e57e-108">En este paso se escalan las posiciones 3D en el espacio 2D.</span><span class="sxs-lookup"><span data-stu-id="9e57e-108">This step scales the 3D positions into 2D space.</span></span> <span data-ttu-id="9e57e-109">Un destino de representación se orienta con los ejes Y que apuntan hacia abajo; Esto requiere que las coordenadas Y se invierten durante la escala de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="9e57e-109">A render target is oriented with the Y axes pointing down; this requires that the Y coordinates get flipped during the viewport scale.</span></span> <span data-ttu-id="9e57e-110">Además, las extensiones x e y (rango de los valores x e y) se escalan para ajustarse al tamaño de la ventanilla según las fórmulas siguientes:</span><span class="sxs-lookup"><span data-stu-id="9e57e-110">In addition, the x and y extents (range of the x and y values) are scaled to fit the viewport size according to the following formulas:</span></span>


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



<span data-ttu-id="9e57e-111">El tutorial 1 crea una ventanilla 640 × 480 con [**D3D11 \_ viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) y llamando a [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span><span class="sxs-lookup"><span data-stu-id="9e57e-111">Tutorial 1 creates a 640 × 480 viewport using [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) and by calling [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span></span>


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



<span data-ttu-id="9e57e-112">La descripción de la ventanilla especifica el tamaño de la ventanilla, el intervalo al que se va a asignar profundidad (mediante *MinDepth* y *maxdepth*), y la posición de la parte superior izquierda de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="9e57e-112">The viewport description specifies the size of the viewport, the range to map depth to (using *MinDepth* and *MaxDepth*), and the placement of the top left of the viewport.</span></span> <span data-ttu-id="9e57e-113">*MinDepth* debe ser menor o igual que *maxdepth*; el intervalo de *MinDepth* y *MaxDepth* está entre 0,0 y 1,0, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9e57e-113">*MinDepth* must be less than or equal to *MaxDepth*; the range for both *MinDepth* and *MaxDepth* is between 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="9e57e-114">Es habitual que la ventanilla se asigne a un destino de representación, pero no es necesario; Además, la ventanilla no tiene que tener el mismo tamaño o la misma posición que el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="9e57e-114">It is common for the viewport to map to a render target but it is not necessary; additionally, the viewport does not have to have the same size or position as the render target.</span></span>

<span data-ttu-id="9e57e-115">Puede crear una matriz de ventanillas, pero solo se puede aplicar una a una salida primitiva del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="9e57e-115">You can create an array of viewports, but only one can be applied to a primitive output from the geometry shader.</span></span> <span data-ttu-id="9e57e-116">Solo se puede establecer una ventanilla activa a la vez.</span><span class="sxs-lookup"><span data-stu-id="9e57e-116">Only one viewport can be set active at a time.</span></span> <span data-ttu-id="9e57e-117">La canalización usa una ventanilla predeterminada (y un rectángulo de tijeras, que se describe en la sección siguiente) durante la rasterización.</span><span class="sxs-lookup"><span data-stu-id="9e57e-117">The pipeline uses a default viewport (and scissor rectangle, discussed in the next section) during rasterization.</span></span> <span data-ttu-id="9e57e-118">El valor predeterminado es siempre la primera ventanilla (o rectángulo en tijera) de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9e57e-118">The default is always the first viewport (or scissor rectangle) in the array.</span></span> <span data-ttu-id="9e57e-119">Para realizar una selección por primitivo de la ventanilla en el sombreador de geometría, especifique la semántica ViewportArrayIndex en el componente de salida GS adecuado en la declaración de la firma de salida GS.</span><span class="sxs-lookup"><span data-stu-id="9e57e-119">To perform a per-primitive selection of the viewport in the geometry shader, specify the ViewportArrayIndex semantic on the appropriate GS output component in the GS output signature declaration.</span></span>

<span data-ttu-id="9e57e-120">El número máximo de ventanillas (y rectángulos en tijeras) que se pueden enlazar a la fase de rasterizador en cualquier momento es 16 (especificado por la **\_ ventanilla \_ de D3D11 y el \_ recuento de objetos de SCISSORRECT \_ \_ \_ por \_ canalización**).</span><span class="sxs-lookup"><span data-stu-id="9e57e-120">The maximum number of viewports (and scissor rectangles) that can be bound to the rasterizer stage at any one time is 16 (specified by **D3D11\_VIEWPORT\_AND\_SCISSORRECT\_OBJECT\_COUNT\_PER\_PIPELINE**).</span></span>

## <a name="set-the-scissor-rectangle"></a><span data-ttu-id="9e57e-121">Establecer el rectángulo en tijera</span><span class="sxs-lookup"><span data-stu-id="9e57e-121">Set the Scissor Rectangle</span></span>

<span data-ttu-id="9e57e-122">Un rectángulo en tijeras le ofrece otra oportunidad de reducir el número de píxeles que se enviarán a la fase de fusión de salida.</span><span class="sxs-lookup"><span data-stu-id="9e57e-122">A scissor rectangle gives you another opportunity to reduce the number of pixels that will be sent to the output merger stage.</span></span> <span data-ttu-id="9e57e-123">Los píxeles que se encuentran fuera del rectángulo de tijera se descartan.</span><span class="sxs-lookup"><span data-stu-id="9e57e-123">Pixels outside of the scissor rectangle are discarded.</span></span> <span data-ttu-id="9e57e-124">El tamaño del rectángulo en tijera se especifica en enteros.</span><span class="sxs-lookup"><span data-stu-id="9e57e-124">The size of the scissor rectangle is specified in integers.</span></span> <span data-ttu-id="9e57e-125">Solo se puede aplicar un rectángulo en tijera (basado en *ViewportArrayIndex* en la [semántica del valor del sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) a un triángulo durante la rasterización.</span><span class="sxs-lookup"><span data-stu-id="9e57e-125">Only one scissor rectangle (based on *ViewportArrayIndex* in [system value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) can be applied to a triangle during rasterization.</span></span>

<span data-ttu-id="9e57e-126">Para habilitar el rectángulo en tijeras, use el miembro *ScissorEnable* (en [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="9e57e-126">To enable the scissor rectangle, use the *ScissorEnable* member (in [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span> <span data-ttu-id="9e57e-127">El rectángulo entre tijeras predeterminado es un rectángulo vacío; es decir, todos los valores Rect son 0.</span><span class="sxs-lookup"><span data-stu-id="9e57e-127">The default scissor rectangle is an empty rectangle; that is, all rect values are 0.</span></span> <span data-ttu-id="9e57e-128">En otras palabras, si no configura el rectángulo en tijera y los tijeras están habilitados, no enviará ningún píxel a la fase de fusión de salida.</span><span class="sxs-lookup"><span data-stu-id="9e57e-128">In other words, if you do not set up the scissor rectangle and scissor is enabled, you will not send any pixels to the output-merger stage.</span></span> <span data-ttu-id="9e57e-129">La configuración más común consiste en inicializar el rectángulo de tijeras con el tamaño de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="9e57e-129">The most common setup is to initialize the scissor rectangle to the size of the viewport.</span></span>

<span data-ttu-id="9e57e-130">Para establecer una matriz de rectángulos con tijeras en el dispositivo, llame a [**ID3D11DeviceContext:: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) con [**D3D11 \_ Rect**](d3d11-rect.md).</span><span class="sxs-lookup"><span data-stu-id="9e57e-130">To set an array of scissor rectangles to the device, call [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) with [**D3D11\_RECT**](d3d11-rect.md).</span></span>


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



<span data-ttu-id="9e57e-131">Este método toma dos parámetros: (1) el número de rectángulos de la matriz y (2) una matriz de rectángulos.</span><span class="sxs-lookup"><span data-stu-id="9e57e-131">This method takes two parameters: (1) the number of rectangles in the array and (2) an array of rectangles.</span></span>

<span data-ttu-id="9e57e-132">La canalización utiliza un índice de rectángulo de tijeras predeterminado durante la rasterización (el valor predeterminado es un rectángulo de tamaño cero con el recorte deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="9e57e-132">The pipeline uses a default scissor rectangle index during rasterization (the default is a zero-size rectangle with clipping disabled).</span></span> <span data-ttu-id="9e57e-133">Para invalidar esto, especifique la \_ semántica de VP ViewportArrayIndex para un componente de salida GS en la declaración de la firma de salida GS.</span><span class="sxs-lookup"><span data-stu-id="9e57e-133">To override this, specify the SV\_ViewportArrayIndex semantic to a GS output component in the GS output signature declaration.</span></span> <span data-ttu-id="9e57e-134">Esto hará que la fase GS marque este componente de salida GS como un componente generado por el sistema con esta semántica.</span><span class="sxs-lookup"><span data-stu-id="9e57e-134">This will cause the GS stage to mark this GS output component as a system-generated component with this semantic.</span></span> <span data-ttu-id="9e57e-135">La fase de rasterizador reconoce esta semántica y usará el parámetro al que se adjunta como índice de rectángulo en tijera para tener acceso a la matriz de rectángulos con tijeras.</span><span class="sxs-lookup"><span data-stu-id="9e57e-135">The rasterizer stage recognizes this semantic and will use the parameter it is attached to as the scissor rectangle index to access the array of scissor rectangles.</span></span> <span data-ttu-id="9e57e-136">No se olvide de indicar a la fase de rasterizador que use el rectángulo de tijeras que define al habilitar el valor de *ScissorEnable* en la descripción de rasterizador antes de crear el objeto de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="9e57e-136">Don't forget to tell the rasterizer stage to use the scissor rectangle that you define by enabling the *ScissorEnable* value in the rasterizer description before creating the rasterizer object.</span></span>

## <a name="set-rasterizer-state"></a><span data-ttu-id="9e57e-137">Establecer estado de rasterizador</span><span class="sxs-lookup"><span data-stu-id="9e57e-137">Set Rasterizer State</span></span>

<span data-ttu-id="9e57e-138">A partir de Direct3D 10, el estado de rasterizador se encapsula en un objeto de estado de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="9e57e-138">Beginning with Direct3D 10, rasterizer state is encapsulated in a rasterizer state object.</span></span> <span data-ttu-id="9e57e-139">Puede crear hasta 4096 objetos de estado de rasterizador que se pueden establecer en el dispositivo pasando un identificador al objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="9e57e-139">You may create up to 4096 rasterizer state objects which can then be set to the device by passing a handle to the state object.</span></span>

<span data-ttu-id="9e57e-140">Use [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) para crear un objeto de estado de rasterizador a partir de una descripción de rasterizador (consulte [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="9e57e-140">Use [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) to create a rasterizer state object from a rasterizer description (see [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span>


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



<span data-ttu-id="9e57e-141">Este conjunto de estado de ejemplo lleva a cabo quizás la configuración de rasterizador más básica:</span><span class="sxs-lookup"><span data-stu-id="9e57e-141">This example set of state accomplishes perhaps the most basic rasterizer setup:</span></span>

-   <span data-ttu-id="9e57e-142">Modo de relleno sólido</span><span class="sxs-lookup"><span data-stu-id="9e57e-142">Solid fill mode</span></span>
-   <span data-ttu-id="9e57e-143">Desactivación o eliminación de caras atrás; asuma el orden de bobinado en sentido contrario a las agujas del reloj para primitivos</span><span class="sxs-lookup"><span data-stu-id="9e57e-143">Cull out or remove back faces; assume counter-clockwise winding order for primitives</span></span>
-   <span data-ttu-id="9e57e-144">Desactivar la diferencia de profundidad, habilitar el almacenamiento en búfer de profundidad y habilitar el rectángulo en tijera</span><span class="sxs-lookup"><span data-stu-id="9e57e-144">Turn off depth bias but enable depth buffering and enable the scissor rectangle</span></span>
-   <span data-ttu-id="9e57e-145">Desactivar el suavizado de contorno de línea y muestreo múltiple</span><span class="sxs-lookup"><span data-stu-id="9e57e-145">Turn off multisampling and line anti-aliasing</span></span>

<span data-ttu-id="9e57e-146">Además, las operaciones básicas de rasterizador siempre incluyen lo siguiente: recorte (al frustum de vista), División de perspectiva y escala de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="9e57e-146">In addition, basic rasterizer operations, always include the following: clipping (to the view frustum), perspective divide, and the viewport scale.</span></span> <span data-ttu-id="9e57e-147">Después de crear correctamente el objeto de estado de rasterizador, establézcalo en el dispositivo de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9e57e-147">After successfully creating the rasterizer state object, set it to the device like this:</span></span>


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a><span data-ttu-id="9e57e-148">Muestreo múltiple</span><span class="sxs-lookup"><span data-stu-id="9e57e-148">Multisampling</span></span>

<span data-ttu-id="9e57e-149">Muestreo múltiple muestrea algunos o todos los componentes de una imagen con una resolución superior (seguida de una disminución de nivel de la resolución original) para reducir el formato de alias más visible causado por los bordes de polígonos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="9e57e-149">Multisampling samples some or all of the components of an image at a higher resolution (followed by downsampling to the original resolution) to reduce the most visible form of aliasing caused by drawing polygon edges.</span></span> <span data-ttu-id="9e57e-150">Aunque el muestreo múltiple requiere muestras de subpíxeles, las GPU modernas implementan el multimuestreo para que un sombreador de píxeles se ejecute una vez por píxel.</span><span class="sxs-lookup"><span data-stu-id="9e57e-150">Even though multisampling requires sub-pixel samples, modern GPU's implement multisampling so that a pixel shader runs once per pixel.</span></span> <span data-ttu-id="9e57e-151">Esto proporciona un equilibrio aceptable entre el rendimiento (especialmente en una aplicación enlazada con GPU) y el suavizado de contorno de la imagen final.</span><span class="sxs-lookup"><span data-stu-id="9e57e-151">This provides an acceptable tradeoff between performance (especially in a GPU bound application) and anti-aliasing the final image.</span></span>

<span data-ttu-id="9e57e-152">Para usar el muestreo múltiple, establezca el campo habilitar en la descripción de la [**rasterización**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), cree un destino de representación de muestreo múltiple y lea el destino de representación con un sombreador para resolver los ejemplos en un color de un solo píxel o llame a [**ID3D11DeviceContext:: ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) para resolver los ejemplos mediante la tarjeta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9e57e-152">To use multisampling, set the enable field in the [**rasterization description**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), create a multisampled render target, and either read the render target with a shader to resolve the samples into a single pixel color or call [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) to resolve the samples using the video card.</span></span> <span data-ttu-id="9e57e-153">El escenario más común es dibujar en uno o varios destinos de representación multimuestreados.</span><span class="sxs-lookup"><span data-stu-id="9e57e-153">The most common scenario is to draw to one or more multisampled render targets.</span></span>

<span data-ttu-id="9e57e-154">El muestreo múltiple es independiente de si se usa o no una máscara de ejemplo, se habilita la opción [de alfa a cobertura](d3d10-graphics-programming-guide-blend-state.md) o las operaciones de estarcido (que siempre se realizan por muestra).</span><span class="sxs-lookup"><span data-stu-id="9e57e-154">Multisampling is independent of whether or not a sample mask is used, [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) is enabled, or stencil operations (which are always performed per-sample).</span></span>

<span data-ttu-id="9e57e-155">Las pruebas de profundidad se ven afectadas por el muestreo múltiple:</span><span class="sxs-lookup"><span data-stu-id="9e57e-155">Depth testing is affected by multisampling:</span></span>

-   <span data-ttu-id="9e57e-156">Cuando se habilita el muestreo múltiple, la profundidad se interpola por muestra y la prueba de profundidad/estarcido se realiza por ejemplo. el color de salida del sombreador de píxeles se duplica para todas las muestras de paso.</span><span class="sxs-lookup"><span data-stu-id="9e57e-156">When multisampling is enabled, depth is interpolated per sample and the depth/stencil test is done per sample; the pixel shader output color is duplicated for all passing samples.</span></span> <span data-ttu-id="9e57e-157">Si el sombreador de píxeles genera profundidad, el valor de profundidad se duplica para todos los ejemplos (aunque este escenario pierde la ventaja de la multimuestreo).</span><span class="sxs-lookup"><span data-stu-id="9e57e-157">If the pixel shader outputs depth, the depth value is duplicated for all samples (although this scenario loses the benefit of multisampling).</span></span>
-   <span data-ttu-id="9e57e-158">Cuando el muestreo múltiple está deshabilitado, las pruebas de profundidad y estarcido se siguen realizando por ejemplo, pero la profundidad no se interpola por muestra.</span><span class="sxs-lookup"><span data-stu-id="9e57e-158">When multisampling is disabled, depth/stencil testing is still done per-sample, but depth is not interpolated per-sample.</span></span>

<span data-ttu-id="9e57e-159">No hay restricciones para mezclar la representación multimuestreada y no multimuestreada en un único destino de representación.</span><span class="sxs-lookup"><span data-stu-id="9e57e-159">There are no restrictions for mixing multisampled and non-multisampled rendering within a single render target.</span></span> <span data-ttu-id="9e57e-160">Si habilita el muestreo múltiple y dibuja en un destino de representación no multimuestreado, se produce el mismo resultado que si no se hubiera habilitado el muestreo múltiple; el muestreo se realiza con una sola muestra por píxel.</span><span class="sxs-lookup"><span data-stu-id="9e57e-160">If you enable multisampling and draw to a non-multisampled render target, you produce the same result as if multisampling were not enabled; sampling is done with a single sample per-pixel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e57e-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e57e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e57e-162">Etapa del rasterizador</span><span class="sxs-lookup"><span data-stu-id="9e57e-162">Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 
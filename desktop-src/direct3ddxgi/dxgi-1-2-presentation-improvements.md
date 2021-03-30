---
title: Voltear modelo, rectángulos modificados, áreas desplazadas
description: DXGI 1,2 admite una nueva cadena de intercambio de modelo Flip, rectángulos modificados y áreas desplazadas. Se explican las ventajas de usar la nueva cadena de intercambio de modelo flip y de la presentación de optimización mediante la especificación de rectángulos modificados y áreas desplazadas.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104552376"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a><span data-ttu-id="9038a-104">Voltear modelo, rectángulos modificados, áreas desplazadas</span><span class="sxs-lookup"><span data-stu-id="9038a-104">Flip model, dirty rectangles, scrolled areas</span></span>

<span data-ttu-id="9038a-105">DXGI 1,2 admite una nueva cadena de intercambio de modelo Flip, rectángulos modificados y áreas desplazadas.</span><span class="sxs-lookup"><span data-stu-id="9038a-105">DXGI 1.2 supports a new flip-model swap chain, dirty rectangles, and scrolled areas.</span></span> <span data-ttu-id="9038a-106">Se explican las ventajas de usar la nueva cadena de intercambio de modelo flip y de la presentación de optimización mediante la especificación de rectángulos modificados y áreas desplazadas.</span><span class="sxs-lookup"><span data-stu-id="9038a-106">We explain the benefits of using the new flip-model swap chain and of optimizing presentation by specifying dirty rectangles and scrolled areas.</span></span>

## <a name="dxgi-flip-model-presentation"></a><span data-ttu-id="9038a-107">Presentación de modelo Flip de DXGI</span><span class="sxs-lookup"><span data-stu-id="9038a-107">DXGI flip-model presentation</span></span>

<span data-ttu-id="9038a-108">DXGI 1,2 agrega compatibilidad con el modelo de presentación de flip para las API de Direct3D 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9038a-108">DXGI 1.2 adds support for the flip presentation model for Direct3D 10 and later APIs.</span></span> <span data-ttu-id="9038a-109">En Windows 7, Direct3D 9EX ha adoptado primero la [presentación de Flip-Model](../direct3darticles/direct3d-9ex-improvements.md) para evitar la copia innecesaria del búfer de la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="9038a-109">In Windows 7, Direct3D 9EX first adopted [flip-model presentation](../direct3darticles/direct3d-9ex-improvements.md) to avoid unnecessarily copying the swap-chain buffer.</span></span> <span data-ttu-id="9038a-110">Mediante el uso de Flip Model, los búferes de reserva se voltean entre el tiempo de ejecución y el Administrador de ventanas de escritorio (DWM), por lo que DWM siempre se compone directamente del búfer de reserva en lugar de copiar el contenido del búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="9038a-110">By using flip model, back buffers are flipped between the runtime and Desktop Window Manager (DWM), so DWM always composes directly from the back buffer instead of copying the back buffer content.</span></span>

<span data-ttu-id="9038a-111">Las API de DXGI 1,2 incluyen una interfaz de cadena de intercambio de DXGI revisada, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="9038a-111">DXGI 1.2 APIs include a revised DXGI swap-chain interface, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="9038a-112">Puede usar varios métodos de interfaz [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) para crear el objeto **IDXGISwapChain1** adecuado para usarlo con un identificador [**hWnd**](../winprog/windows-data-types.md) , un objeto [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , un [DirectComposition](../directcomp/directcomposition-portal.md)o el marco [**Windows. UI. Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="9038a-112">You can use multiple [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) interface methods to create the appropriate **IDXGISwapChain1** object to use with an [**HWND**](../winprog/windows-data-types.md) handle, a [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) object, [DirectComposition](../directcomp/directcomposition-portal.md), or the [**Windows.UI.Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) framework.</span></span>

<span data-ttu-id="9038a-113">Para seleccionar el modelo de presentación de flip, especifique el valor de la enumeración [**\_ \_ \_ \_ Sequential del efecto de intercambio de dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) en el miembro **SwapEffect** de la estructura DESC1 de la [**\_ \_ cadena \_ de intercambio de dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) y establezca el miembro **BufferCount** de la cadena de **intercambio de dxgi \_ \_ \_ DESC1** en un mínimo de 2.</span><span class="sxs-lookup"><span data-stu-id="9038a-113">You select the flip presentation model by specifying the [**DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) enumeration value in the **SwapEffect** member of the [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and by setting the **BufferCount** member of **DXGI\_SWAP\_CHAIN\_DESC1** to a minimum of 2.</span></span> <span data-ttu-id="9038a-114">Para obtener más información sobre cómo usar DXGI Flip Model, consulte [modelo de volteo de dxgi](dxgi-flip-model.md).</span><span class="sxs-lookup"><span data-stu-id="9038a-114">For more info about how to use DXGI flip model, see [DXGI flip model](dxgi-flip-model.md).</span></span> <span data-ttu-id="9038a-115">Debido a la presentación más suave del modelo de presentación flip y a otras nuevas funcionalidades, se recomienda usar Flip Presentation Model para todas las aplicaciones nuevas que escriba con Direct3D 10 y las API posteriores.</span><span class="sxs-lookup"><span data-stu-id="9038a-115">Because of the flip presentation model's smoother presentation and other new functionality, we recommend that you use flip presentation model for all new apps that you write with Direct3D 10 and later APIs.</span></span>

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a><span data-ttu-id="9038a-116">Usar rectángulos modificados y el rectángulo de desplazamiento en la presentación de la cadena de intercambio</span><span class="sxs-lookup"><span data-stu-id="9038a-116">Using dirty rectangles and the scroll rectangle in swap chain presentation</span></span>

<span data-ttu-id="9038a-117">Mediante el uso de rectángulos modificados y el rectángulo de desplazamiento en la presentación de la cadena de intercambio, se ahorra el uso del ancho de banda de la memoria y el uso relacionado de la energía del sistema, ya que la cantidad de datos de píxeles que el sistema operativo necesita para dibujar el siguiente fotograma presentado se reduce si el sistema operativo no necesita dibujar todo el marco.</span><span class="sxs-lookup"><span data-stu-id="9038a-117">By using dirty rectangles and the scroll rectangle in swap chain presentation, you save on the usage of memory bandwidth and the related usage of system power because the amount of pixel data that the operating system needs to draw the next presented frame is reduced if the operating system doesn't need to draw the entire frame.</span></span> <span data-ttu-id="9038a-118">En el caso de las aplicaciones que se muestran a menudo a través de Conexión a Escritorio remoto y otras tecnologías de acceso remoto, el ahorro se percibe especialmente en la calidad de la pantalla, ya que estas tecnologías usan rectángulos modificados y metadatos de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9038a-118">For apps that are often displayed via Remote Desktop Connection and other remote-accessing technologies, the savings are particularly noticeable in the display quality because these technologies use dirty rectangles and scroll metadata.</span></span>

<span data-ttu-id="9038a-119">Solo se puede usar el desplazamiento con cadenas de intercambio de DXGI que se ejecuten en flip Presentation Model.</span><span class="sxs-lookup"><span data-stu-id="9038a-119">You can use scroll only with DXGI swap chains that run in flip presentation model.</span></span> <span data-ttu-id="9038a-120">Puede usar rectángulos modificados con cadenas de intercambio de DXGI que se ejecuten en el modelo de volteo y en el modelo de bitblt (establecido con el [**efecto de intercambio de dxgi \_ \_ \_ secuencial**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="9038a-120">You can use dirty rectangles with DXGI swap chains that run in both flip model and bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span>

<span data-ttu-id="9038a-121">En este escenario y en la ilustración se muestra la funcionalidad de usar rectángulos modificados y desplazarse.</span><span class="sxs-lookup"><span data-stu-id="9038a-121">In this scenario and illustration we show the functionality of using dirty rectangles and scroll.</span></span> <span data-ttu-id="9038a-122">Aquí, una aplicación desplazable contiene texto y animar vídeo.</span><span class="sxs-lookup"><span data-stu-id="9038a-122">Here, a scrollable app contains text and animating video.</span></span> <span data-ttu-id="9038a-123">La aplicación usa rectángulos modificados para actualizar el vídeo animado y la nueva línea para la ventana, en lugar de actualizar toda la ventana.</span><span class="sxs-lookup"><span data-stu-id="9038a-123">The app uses dirty rectangles to just update the animating video and new line for the window, instead of updating the entire window.</span></span> <span data-ttu-id="9038a-124">El rectángulo de desplazamiento permite que el sistema operativo copie y traduzca el contenido representado previamente en el nuevo marco y represente solo la nueva línea en el nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="9038a-124">The scroll rectangle allows the operating system to copy and translate the previously rendered content on the new frame and to render only the new line on the new frame.</span></span>

<span data-ttu-id="9038a-125">La aplicación realiza la presentación llamando al método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) .</span><span class="sxs-lookup"><span data-stu-id="9038a-125">The app performs presentation by calling the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method.</span></span> <span data-ttu-id="9038a-126">En esta llamada, la aplicación pasa un puntero a una estructura de [**\_ \_ parámetros presentes de DXGI**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) que incluye rectángulos modificados y el número de rectángulos modificados, o el rectángulo de desplazamiento y el desplazamiento de desplazamiento asociado, o ambos rectángulos modificados y el rectángulo de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9038a-126">In this call, the app passes a pointer to a [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) structure that includes dirty rectangles and the number of dirty rectangles, or the scroll rectangle and the associated scroll offset, or both dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="9038a-127">Nuestra aplicación pasa dos rectángulos modificados y el rectángulo de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9038a-127">Our app passes 2 dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="9038a-128">El rectángulo de desplazamiento es el área del fotograma anterior que el sistema operativo necesita para copiar en el fotograma actual antes de representar el fotograma actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-128">The scroll rectangle is the area of the previous frame that the operating system needs to copy to the current frame before it renders the current frame.</span></span> <span data-ttu-id="9038a-129">La aplicación especifica el vídeo de animación y la nueva línea como rectángulos modificados, y el sistema operativo los representa en el marco actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-129">The app specifies the animating video and new line as dirty rectangles, and the operating system renders them on the current frame.</span></span>

![Ilustración de los rectángulos de desplazamiento y modificados superpuestos](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

<span data-ttu-id="9038a-131">El rectángulo discontinuo muestra el rectángulo de desplazamiento en el marco actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-131">The dashed rectangle shows the scroll rectangle in the current frame.</span></span> <span data-ttu-id="9038a-132">El rectángulo de desplazamiento se especifica mediante el miembro **pScrollRect** de [**\_ \_ los parámetros presentes de DXGI**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span><span class="sxs-lookup"><span data-stu-id="9038a-132">The scroll rectangle is specified by the **pScrollRect** member of [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span></span> <span data-ttu-id="9038a-133">La flecha muestra el desplazamiento de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9038a-133">The arrow shows the scroll offset.</span></span> <span data-ttu-id="9038a-134">El desplazamiento de desplazamiento lo especifica el miembro **pScrollOffset** de **\_ \_ los parámetros presentes de DXGI**.</span><span class="sxs-lookup"><span data-stu-id="9038a-134">The scroll offset is specified by the **pScrollOffset** member of **DXGI\_PRESENT\_PARAMETERS**.</span></span> <span data-ttu-id="9038a-135">Los rectángulos rellenos muestran rectángulos modificados que la aplicación actualizó con contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="9038a-135">Filled rectangles show dirty rectangles that the app updated with new content.</span></span> <span data-ttu-id="9038a-136">Los rectángulos rellenos se especifican mediante los miembros **DirtyRectsCount** y **pDirtyRects** de los **\_ \_ parámetros presentes de DXGI**.</span><span class="sxs-lookup"><span data-stu-id="9038a-136">The filled rectangles are specified by the **DirtyRectsCount** and **pDirtyRects** members of **DXGI\_PRESENT\_PARAMETERS**.</span></span>

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a><span data-ttu-id="9038a-137">Ejemplo 2: cadena de intercambio del modelo de volteo de búfer con rectángulos modificados y rectángulo de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="9038a-137">Sample 2-buffer flip-model swap chain with dirty rectangles and scroll rectangle</span></span>

<span data-ttu-id="9038a-138">En la siguiente ilustración y secuencia se muestra un ejemplo de una operación de presentación de modelo de marcado de DXGI que usa rectángulos modificados y un rectángulo de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9038a-138">The next illustration and sequence shows an example of a DXGI flip-model presentation operation that uses dirty rectangles and a scroll rectangle.</span></span> <span data-ttu-id="9038a-139">En este ejemplo, se usa el número mínimo de búferes para la presentación de Flip-Model, que es un recuento de búferes de dos, un búfer frontal que contiene el contenido para mostrar la aplicación y un búfer de reserva que contiene el fotograma actual que la aplicación desea representar.</span><span class="sxs-lookup"><span data-stu-id="9038a-139">In this example we use the minimum number of buffers for flip-model presentation, which is a buffer count of two, one front buffer that contains the app display content and one back buffer that contains the current frame that the app wants to render.</span></span>

1.  <span data-ttu-id="9038a-140">Como se muestra en el búfer frontal al principio del fotograma, la aplicación desplazable muestra inicialmente un fotograma con algún texto y animar vídeo.</span><span class="sxs-lookup"><span data-stu-id="9038a-140">As shown in the front buffer at the beginning of the frame, the scrollable app initially shows a frame with some text and animating video.</span></span>
2.  <span data-ttu-id="9038a-141">Para representar el fotograma siguiente, la aplicación representa en el búfer de reserva los rectángulos modificados que actualizan el vídeo de animación y la nueva línea para la ventana.</span><span class="sxs-lookup"><span data-stu-id="9038a-141">To render the next frame, the app renders onto the back buffer the dirty rectangles that update the animating video and the new line for the window.</span></span>
3.  <span data-ttu-id="9038a-142">Cuando la aplicación llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), especifica los rectángulos modificados y el rectángulo de desplazamiento y el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9038a-142">When the app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), it specifies the dirty rectangles and the scroll rectangle and offset.</span></span> <span data-ttu-id="9038a-143">Después, el tiempo de ejecución copia el rectángulo de desplazamiento del fotograma anterior menos los rectángulos modificados actualizados en el búfer de reserva actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-143">The runtime next copies the scroll rectangle from the previous frame minus the updated dirty rectangles onto the current back buffer.</span></span>
4.  <span data-ttu-id="9038a-144">Finalmente, el tiempo de ejecución intercambia los búferes frontal y posterior.</span><span class="sxs-lookup"><span data-stu-id="9038a-144">The runtime finally swaps the front and back buffers.</span></span>

![ejemplo de cadena de intercambio de modelo Flip con rectángulos de desplazamiento y modificados](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a><span data-ttu-id="9038a-146">Seguimiento de rectángulos modificados y rectángulos de desplazamiento en varios marcos</span><span class="sxs-lookup"><span data-stu-id="9038a-146">Tracking dirty rectangles and scroll rectangles across multiple frames</span></span>

<span data-ttu-id="9038a-147">Al usar rectángulos modificados en la aplicación, debe realizar un seguimiento de los rectángulos modificados para admitir la representación incremental.</span><span class="sxs-lookup"><span data-stu-id="9038a-147">When you use dirty rectangles in your app, you must track the dirty rectangles to support incremental rendering.</span></span> <span data-ttu-id="9038a-148">Cuando la aplicación llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con rectángulos modificados, debe asegurarse de que todos los píxeles dentro de los rectángulos modificados estén actualizados.</span><span class="sxs-lookup"><span data-stu-id="9038a-148">When your app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) with dirty rectangles, you must ensure that every pixel within the dirty rectangles is up to date.</span></span> <span data-ttu-id="9038a-149">Si no va a volver a representar completamente todo el área del rectángulo sucio o si no sabe con certeza las áreas que han sido sucias, debe copiar algunos datos del búfer de reserva totalmente coherente en el búfer de reserva actual y obsoleto antes de comenzar la representación.</span><span class="sxs-lookup"><span data-stu-id="9038a-149">If you aren't completely re-rendering the whole area of the dirty rectangle or if you can’t know for certain the areas that are dirtied, you must copy some data from the previous fully coherent back buffer to the current, stale back buffer before you start rendering.</span></span>

<span data-ttu-id="9038a-150">El motor en tiempo de ejecución solo copia las diferencias entre las áreas actualizadas del marco anterior y las áreas actualizadas del marco actual en el búfer de retroceso actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-150">The runtime copies only the differences between updated areas of the previous frame and updated areas of the current frame onto the current back buffer.</span></span> <span data-ttu-id="9038a-151">Si estas áreas forman una intersección, el Runtime solo copia la diferencia entre ellas.</span><span class="sxs-lookup"><span data-stu-id="9038a-151">If these areas intersect, the runtime copies only the difference between them.</span></span> <span data-ttu-id="9038a-152">Como puede ver en el siguiente diagrama y secuencia, debe copiar la intersección entre el rectángulo sucio desde el fotograma 1 y el rectángulo sucio del fotograma 2 al rectángulo sucio del marco 2.</span><span class="sxs-lookup"><span data-stu-id="9038a-152">As you can see in the following diagram and sequence, you must copy the intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>

1.  <span data-ttu-id="9038a-153">Presente rectángulo sucio en el marco 1.</span><span class="sxs-lookup"><span data-stu-id="9038a-153">Present dirty rectangle in frame 1.</span></span>
2.  <span data-ttu-id="9038a-154">Copiar la intersección entre el rectángulo sucio desde el fotograma 1 y el rectángulo sucio desde el fotograma 2 al rectángulo sucio de la trama 2.</span><span class="sxs-lookup"><span data-stu-id="9038a-154">Copy intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>
3.  <span data-ttu-id="9038a-155">Presente rectángulo sucio en el marco 2.</span><span class="sxs-lookup"><span data-stu-id="9038a-155">Present dirty rectangle in frame 2.</span></span>

![seguimiento de rectángulos de desplazamiento y modificados en varios marcos](images/track-dirty-rects-scroll-rects.png)

<span data-ttu-id="9038a-157">Para generalizar, en una cadena de intercambio con N búferes, el área que el motor en tiempo de ejecución copia desde el último fotograma al fotograma actual en el marco actual está presente:</span><span class="sxs-lookup"><span data-stu-id="9038a-157">To generalize, for a swap chain with N buffers, the area that the runtime copies from the last frame to the current frame on the current frame’s present is:</span></span>

![ecuación para calcular el área en la que se copia en tiempo de ejecución](images/runtime-copy-equation.png)

<span data-ttu-id="9038a-159">donde buffer indica el índice de búfer en una cadena de intercambio, comenzando por el índice de búfer actual en cero.</span><span class="sxs-lookup"><span data-stu-id="9038a-159">where buffer indicates the buffer index in a swap chain, starting with current buffer index at zero.</span></span>

<span data-ttu-id="9038a-160">Puede realizar un seguimiento de las intersecciones entre el fotograma anterior y los rectángulos modificados del fotograma actual manteniendo una copia de los rectángulos modificados del fotograma anterior o volviendo a representar los rectángulos modificados del nuevo fotograma con el contenido adecuado del fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="9038a-160">You can keep track of any intersections between the previous frame and the current frame’s dirty rectangles by keeping a copy of the previous frame’s dirty rectangles or by re-rendering the new frame’s dirty rectangles with the appropriate content from the previous frame.</span></span>

<span data-ttu-id="9038a-161">Del mismo modo, en los casos en los que la cadena de intercambio tenga más de 2 búferes de reserva, debe asegurarse de que las áreas superpuestas entre los rectángulos modificados del búfer actual y los rectángulos modificados de todos los fotogramas anteriores se copian o se vuelven a representar.</span><span class="sxs-lookup"><span data-stu-id="9038a-161">Similarly, in the cases where the swap chain has more than 2 back buffers, you must ensure that overlapping areas between the current buffer’s dirty rectangles and the dirty rectangles of all previous frame’s are copied or re-rendered.</span></span>

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a><span data-ttu-id="9038a-162">Seguimiento de una sola intersección entre dos rectángulos modificados</span><span class="sxs-lookup"><span data-stu-id="9038a-162">Tracking a single intersection between 2 dirty rectangles</span></span>

<span data-ttu-id="9038a-163">En el caso más simple, cuando se actualiza un único rectángulo modificado por fotograma, los rectángulos modificados en dos fotogramas podrían intersectar.</span><span class="sxs-lookup"><span data-stu-id="9038a-163">In the simplest case, when you update a single dirty rectangle per frame, the dirty rectangles across two frames might intersect.</span></span> <span data-ttu-id="9038a-164">Para averiguar si el rectángulo sucio del fotograma anterior y el rectángulo sucio del marco actual se superponen, debe comprobar si el rectángulo sucio del fotograma anterior forma una intersección con el rectángulo sucio del fotograma actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-164">To find out whether the dirty rectangle of the previous frame and the dirty rectangle of the current frame overlap, you need to verify whether the dirty rectangle of the previous frame intersects with the dirty rectangle of the current frame.</span></span> <span data-ttu-id="9038a-165">Puede llamar a la función [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) de GDI para determinar si dos estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) que representan los dos rectángulos modificados forman una intersección.</span><span class="sxs-lookup"><span data-stu-id="9038a-165">You can call the GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) function to determine whether two [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that represent the two dirty rectangles intersect.</span></span>

<span data-ttu-id="9038a-166">En este fragmento de código, una llamada a [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) devuelve la intersección de dos rectángulos modificados en otro [**Rect**](/previous-versions//dd162897(v=vs.85)) denominado dirtyRectCopy.</span><span class="sxs-lookup"><span data-stu-id="9038a-166">In this code snippet, a call to [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) returns the intersection of two dirty rectangles in another [**RECT**](/previous-versions//dd162897(v=vs.85)) called dirtyRectCopy.</span></span> <span data-ttu-id="9038a-167">Después de que el fragmento de código determine que los dos rectángulos modificados forman una intersección, llama al método [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar la región de intersección en el marco actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-167">After the code snippet determines that the two dirty rectangles intersect, it calls the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy the region of intersection into the current frame.</span></span>

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

<span data-ttu-id="9038a-168">Si usa este fragmento de código en la aplicación, la aplicación estará lista para llamar a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para actualizar el marco actual con el rectángulo modificado actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-168">If you use this code snippet in your application, the app will then be ready to call [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) to update the current frame with the current dirty rectangle.</span></span>

### <a name="tracking-intersections-between-n-dirty-rectangles"></a><span data-ttu-id="9038a-169">Seguimiento de intersecciones entre N rectángulos modificados</span><span class="sxs-lookup"><span data-stu-id="9038a-169">Tracking intersections between N dirty rectangles</span></span>

<span data-ttu-id="9038a-170">Si especifica varios rectángulos modificados, que pueden incluir un rectángulo sucio para la línea de desplazamiento recién revelada, por fotograma, deberá comprobar y realizar el seguimiento de los superposiciones que puedan producirse entre todos los rectángulos modificados del fotograma anterior y todos los rectángulos modificados del fotograma actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-170">If you specify multiple dirty rectangles, which can include a dirty rectangle for the newly revealed scroll line, per frame, you need to verify and track any overlaps that might occur between all the dirty rectangles of the previous frame and all the dirty rectangles of the current frame.</span></span> <span data-ttu-id="9038a-171">Para calcular las intersecciones entre los rectángulos modificados del fotograma anterior y los rectángulos modificados del fotograma actual, puede agrupar los rectángulos modificados en regiones.</span><span class="sxs-lookup"><span data-stu-id="9038a-171">To calculate the intersections between the dirty rectangles of the previous frame and the dirty rectangles of the current frame, you can group the dirty rectangles into regions.</span></span>

<span data-ttu-id="9038a-172">En este fragmento de código, se llama a la función GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) para convertir cada rectángulo sucio en una región rectangular y, a continuación, se llama a la función GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) para combinar todas las regiones rectangulares desfasadas en un grupo.</span><span class="sxs-lookup"><span data-stu-id="9038a-172">In this code snippet, we call the GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) function to convert each dirty rectangle into a rectangular region and then we call the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to combine all the dirty rectangular regions into a group.</span></span>

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

<span data-ttu-id="9038a-173">Ahora puede usar la función [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) de GDI para determinar la intersección entre la región desfasada del fotograma anterior y la región desfasada del fotograma actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-173">You can now use the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to determine the intersection between the dirty region of the previous frame and the dirty region of the current frame.</span></span> <span data-ttu-id="9038a-174">Después de obtener la región de intersección, llame a la función [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) de GDI para obtener cada rectángulo individual de la región de intersección y, a continuación, llame al método [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar cada rectángulo intersectando en el búfer de retroceso actual.</span><span class="sxs-lookup"><span data-stu-id="9038a-174">After you obtain the intersecting region, call the GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) function to obtain each individual rectangle from the intersecting region and then call the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy each intersecting rectangle into the current back buffer.</span></span> <span data-ttu-id="9038a-175">En el fragmento de código siguiente se muestra cómo usar estas funciones GDI y Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9038a-175">The next code snippet shows how to use these GDI and Direct3D functions.</span></span>

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a><span data-ttu-id="9038a-176">Cadena de intercambio del modelo bitblt con rectángulos modificados</span><span class="sxs-lookup"><span data-stu-id="9038a-176">Bitblt model swap chain with dirty rectangles</span></span>

<span data-ttu-id="9038a-177">Puede usar rectángulos modificados con cadenas de intercambio de DXGI que se ejecutan en el modelo de bitblt (establecido con el [**efecto de intercambio de dxgi \_ \_ \_ secuencial**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="9038a-177">You can use dirty rectangles with DXGI swap chains that run in bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span> <span data-ttu-id="9038a-178">Las cadenas de intercambio del modelo bitblt que usan más de un búfer también deben realizar el seguimiento de los rectángulos modificados superpuestos en los fotogramas de la misma manera que se describe en [seguimiento de rectángulos modificados y rectángulos de desplazamiento en varios fotogramas](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) para las cadenas de intercambio de modelo</span><span class="sxs-lookup"><span data-stu-id="9038a-178">Bitblt model swap chains that use more than one buffer must also track overlapping dirty rectangles across frames in the same way as described in [Tracking dirty rectangles and scroll rectangles across multiple frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) for flip model swap chains.</span></span> <span data-ttu-id="9038a-179">Las cadenas de intercambio del modelo bitblt con un solo búfer no necesitan realizar un seguimiento de los rectángulos modificados superpuestos, ya que todo el búfer se vuelve a dibujar en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="9038a-179">Bitblt model swap chains with just one buffer need not track overlapping dirty rectangles because the entire buffer is redrawn every frame.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9038a-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9038a-180">Related topics</span></span>

[<span data-ttu-id="9038a-181">Mejoras en DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="9038a-181">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)

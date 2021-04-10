---
title: Introducción a la interoperabilidad de Direct2D y Direct3D
description: .
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D, interoperación de Direct3D
- Direct2D, interoperabilidad
- interoperabilidad, Direct2D
- interoperabilidad, Direct3D
- Direct3D, interoperabilidad
- Direct3D, interoperación de Direct2D
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6854481ec2a8d869467aa912252e3649e17f2501
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "104149709"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a><span data-ttu-id="1ad30-111">Introducción a la interoperabilidad de Direct2D y Direct3D</span><span class="sxs-lookup"><span data-stu-id="1ad30-111">Direct2D and Direct3D Interoperability Overview</span></span>

<span data-ttu-id="1ad30-112">Los gráficos con aceleración de hardware en 2D y 3D se convierten cada vez en una parte de las aplicaciones que no son de juegos y la mayoría de las aplicaciones de juegos usan gráficos 2D en forma de menús y pantallas de Heads-Up (HUDs).</span><span class="sxs-lookup"><span data-stu-id="1ad30-112">Hardware accelerated 2-D and 3-D graphics are increasingly becoming a part of non-gaming applications, and most gaming applications use 2-D graphics in the form of menus and Heads-Up Displays (HUDs).</span></span> <span data-ttu-id="1ad30-113">Hay un gran número de valores que se pueden agregar al permitir que la representación 2D tradicional se mezcle con la representación de Direct3D de una manera eficaz.</span><span class="sxs-lookup"><span data-stu-id="1ad30-113">There is lots of value that can be added by enabling traditional 2-D rendering to be mixed with Direct3D rendering in an efficient manner.</span></span>

<span data-ttu-id="1ad30-114">En este tema se describe cómo integrar gráficos 2D y 3D mediante Direct2D y [Direct3D](../graphics-and-multimedia.md).</span><span class="sxs-lookup"><span data-stu-id="1ad30-114">This topic describes how to integrate 2-D and 3-D graphics by using Direct2D and [Direct3D](../graphics-and-multimedia.md).</span></span>

<span data-ttu-id="1ad30-115">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="1ad30-115">It contains the following sections.</span></span>

-   [<span data-ttu-id="1ad30-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1ad30-116">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="1ad30-117">Versiones admitidas de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1ad30-117">Supported Direct3D Versions</span></span>](#supported-direct3d-versions)
-   [<span data-ttu-id="1ad30-118">Interoperabilidad a través de DXGI</span><span class="sxs-lookup"><span data-stu-id="1ad30-118">Interoperability Through DXGI</span></span>](#interoperability-through-dxgi)
-   [<span data-ttu-id="1ad30-119">Escribir en una superficie de Direct3D con un destino de representación de la superficie de DXGI</span><span class="sxs-lookup"><span data-stu-id="1ad30-119">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [<span data-ttu-id="1ad30-120">Crear una superficie de DXGI</span><span class="sxs-lookup"><span data-stu-id="1ad30-120">Creating a DXGI Surface</span></span>](#creating-a-dxgi-surface)
-   [<span data-ttu-id="1ad30-121">Escritura de contenido de Direct2D en un búfer de cadena de intercambio</span><span class="sxs-lookup"><span data-stu-id="1ad30-121">Writing Direct2D Content to a Swap Chain Buffer</span></span>](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [<span data-ttu-id="1ad30-122">Ejemplo: dibujar un fondo en 2D</span><span class="sxs-lookup"><span data-stu-id="1ad30-122">Example: Draw a 2-D Background</span></span>](#example-draw-a-2-d-background)
-   [<span data-ttu-id="1ad30-123">Usar contenido de Direct2D como textura</span><span class="sxs-lookup"><span data-stu-id="1ad30-123">Using Direct2D Content as a Texture</span></span>](#using-direct2d-content-as-a-texture)
    -   [<span data-ttu-id="1ad30-124">Ejemplo: uso de contenido de Direct2D como textura</span><span class="sxs-lookup"><span data-stu-id="1ad30-124">Example: Use Direct2D Content as a Texture</span></span>](#example-use-direct2d-content-as-a-texture)
-   [<span data-ttu-id="1ad30-125">Cambiar el tamaño de un destino de representación de la superficie de DXGI</span><span class="sxs-lookup"><span data-stu-id="1ad30-125">Resizing a DXGI Surface Render Target</span></span>](#resizing-a-dxgi-surface-render-target)
-   [<span data-ttu-id="1ad30-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ad30-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="1ad30-127">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1ad30-127">Prerequisites</span></span>

<span data-ttu-id="1ad30-128">En esta información general se supone que está familiarizado con las operaciones básicas de dibujo de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-128">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="1ad30-129">Para ver un tutorial, consulte la guía de [Inicio rápido de Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="1ad30-129">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="1ad30-130">También se supone que puede programar con [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="1ad30-130">It also assumes that you can program by using [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

## <a name="supported-direct3d-versions"></a><span data-ttu-id="1ad30-131">Versiones admitidas de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1ad30-131">Supported Direct3D Versions</span></span>

<span data-ttu-id="1ad30-132">Con DirectX 11,0, Direct2D solo admite la interoperabilidad con dispositivos Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="1ad30-132">With DirectX 11.0, Direct2D supports interoperability with Direct3D 10.1 devices only.</span></span> <span data-ttu-id="1ad30-133">Con DirectX 11,1 o posterior, Direct2D también admite la interoperabilidad con Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="1ad30-133">With DirectX 11.1 or later, Direct2D supports interoperability with Direct3D 11 as well.</span></span>

## <a name="interoperability-through-dxgi"></a><span data-ttu-id="1ad30-134">Interoperabilidad a través de DXGI</span><span class="sxs-lookup"><span data-stu-id="1ad30-134">Interoperability Through DXGI</span></span>

<span data-ttu-id="1ad30-135">A partir de Direct3D 10, el tiempo de ejecución de Direct3D usa [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) para la administración de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ad30-135">As of Direct3D 10, the Direct3D runtime uses [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) for resource management.</span></span> <span data-ttu-id="1ad30-136">La capa de tiempo de ejecución de DXGI proporciona el uso compartido entre procesos de superficies de memoria de vídeo y sirve como base para otras plataformas en tiempo de ejecución basadas en memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1ad30-136">The DXGI runtime layer provides cross-process sharing of video memory surfaces and serves as the foundation for other video memory-based runtime platforms.</span></span> <span data-ttu-id="1ad30-137">Direct2D usa DXGI para interoperar con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-137">Direct2D uses DXGI to interoperate with Direct3D.</span></span>

<span data-ttu-id="1ad30-138">Hay dos formas principales de usar Direct2D y Direct3D conjuntamente:</span><span class="sxs-lookup"><span data-stu-id="1ad30-138">There are two primary ways to use Direct2D and Direct3D together:</span></span>

-   <span data-ttu-id="1ad30-139">Puede escribir contenido de Direct2D en una superficie de Direct3D mediante la obtención de un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) y su uso con [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="1ad30-139">You can write Direct2D content to a Direct3D surface by obtaining an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and using it with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="1ad30-140">Después, puede usar el destino de representación para agregar una interfaz bidimensional o un fondo a gráficos tridimensionales, o bien usar un dibujo de Direct2D como textura para un objeto de tres dimensiones.</span><span class="sxs-lookup"><span data-stu-id="1ad30-140">You can then use the render target to add a two-dimensional interface or background to three-dimensional graphics, or use a Direct2D drawing as a texture for a three dimensional object.</span></span>
-   <span data-ttu-id="1ad30-141">Mediante el uso de [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) desde un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), puede escribir una escena de Direct3D en un mapa de bits y representarlo con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-141">By using [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) from an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), you can write a Direct3D scene to a bitmap and render it with Direct2D.</span></span>

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a><span data-ttu-id="1ad30-142">Escribir en una superficie de Direct3D con un destino de representación de la superficie de DXGI</span><span class="sxs-lookup"><span data-stu-id="1ad30-142">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>

<span data-ttu-id="1ad30-143">Para escribir en una superficie de Direct3D, obtenga un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) y páselo al método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un destino de representación de la superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-143">To write to a Direct3D surface, you obtain an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and pass it to the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create a DXGI surface render target.</span></span> <span data-ttu-id="1ad30-144">Después, puede usar el destino de representación de la superficie de DXGI para dibujar contenido 2D en la superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-144">You can then use the DXGI surface render target to draw 2-D content to the DXGI surface.</span></span>

<span data-ttu-id="1ad30-145">Un destino de representación de la superficie de DXGI es un tipo de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="1ad30-145">A DXGI surface render target is a kind of [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="1ad30-146">Al igual que otros destinos de representación de Direct2D, puede usarlo para crear recursos y emitir comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1ad30-146">Like other Direct2D render targets, you can use it to create resources and issue drawing commands.</span></span>

<span data-ttu-id="1ad30-147">El destino de representación de la superficie de DXGI y la superficie de DXGI deben usar el mismo formato de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-147">The DXGI surface render target and the DXGI surface must use the same DXGI format.</span></span> <span data-ttu-id="1ad30-148">Si especifica el formato de [**DXGI formato \_ \_ desconocido**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) al crear el destino de representación, usará automáticamente el formato de la superficie.</span><span class="sxs-lookup"><span data-stu-id="1ad30-148">If you specify the [**DXGI\_FORMAT\_UNKOWN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format when you create the render target, it will automatically use the surface's format.</span></span>

<span data-ttu-id="1ad30-149">El destino de representación de la superficie de DXGI no realiza la sincronización de la superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-149">The DXGI surface render target does not perform DXGI surface synchronization.</span></span>

### <a name="creating-a-dxgi-surface"></a><span data-ttu-id="1ad30-150">Crear una superficie de DXGI</span><span class="sxs-lookup"><span data-stu-id="1ad30-150">Creating a DXGI Surface</span></span>

<span data-ttu-id="1ad30-151">Con Direct3D 10, hay varias maneras de obtener una superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-151">With Direct3D 10, there are several ways to obtain a DXGI surface.</span></span> <span data-ttu-id="1ad30-152">Puede crear un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para un dispositivo y, a continuación, usar el método [**getBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la cadena de intercambio para obtener una superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-152">You can create an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) for a device, then use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span> <span data-ttu-id="1ad30-153">O bien, puede usar un dispositivo para crear una textura y, a continuación, usar esa textura como una superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-153">Or, you can use a device to create a texture, then use that texture as a DXGI surface.</span></span>

<span data-ttu-id="1ad30-154">Independientemente de cómo cree la superficie de DXGI, la superficie debe usar uno de los formatos de DXGI que admiten los objetivos de representación de la superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-154">Regardless of how you create the DXGI surface, the surface must use one of the DXGI formats supported by DXGI surface render targets.</span></span> <span data-ttu-id="1ad30-155">Para obtener una lista, vea [formatos de píxel admitidos y modos alfa](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="1ad30-155">For a list, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="1ad30-156">Además, el [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) asociado a la superficie de dxgi debe admitir formatos de BGRA DXGI para que la superficie funcione con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-156">Additionally, the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the DXGI surface must support BGRA DXGI formats for the surface to work with Direct2D.</span></span> <span data-ttu-id="1ad30-157">Para garantizar esta compatibilidad, use la marca de [**\_ soporte D3D10 Create \_ Device \_ BGRA \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) al llamar al método [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1ad30-157">To ensure this support, use the [**D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag when you call the [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) method to create the device.</span></span>

<span data-ttu-id="1ad30-158">En el código siguiente se define un método que crea un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span><span class="sxs-lookup"><span data-stu-id="1ad30-158">The following code defines a method that creates an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span></span> <span data-ttu-id="1ad30-159">Selecciona el mejor nivel de características disponible y recurre a [Windows Advanced rasterization Platform (warp)](./installing-the-direct2d-debug-layer.md) cuando no está disponible la representación de hardware.</span><span class="sxs-lookup"><span data-stu-id="1ad30-159">It selects the best feature level available and falls back to [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) when hardware rendering is not available.</span></span>


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



<span data-ttu-id="1ad30-160">En el ejemplo de código siguiente `CreateD3DDevice` se usa el método que se muestra en el ejemplo anterior para crear un dispositivo Direct3D que pueda crear superficies de DXGI para su uso con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-160">The next code example uses the `CreateD3DDevice` method shown in the previous example to create a Direct3D device that can create DXGI surfaces for use with Direct2D.</span></span>


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a><span data-ttu-id="1ad30-161">Escritura de contenido de Direct2D en un búfer de cadena de intercambio</span><span class="sxs-lookup"><span data-stu-id="1ad30-161">Writing Direct2D Content to a Swap Chain Buffer</span></span>

<span data-ttu-id="1ad30-162">La manera más sencilla de agregar contenido de Direct2D a una escena de Direct3D es usar el método [**getBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) para obtener una superficie de DXGI y luego usar la superficie con el método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para crear un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) con el que dibujar el contenido 2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-162">The simplest way to add Direct2D content to a Direct3D scene is to use the [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method of an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) to obtain a DXGI surface, then use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) with which to draw your 2-D content.</span></span>

<span data-ttu-id="1ad30-163">Este enfoque no representa el contenido en tres dimensiones. no tendrá perspectiva ni profundidad.</span><span class="sxs-lookup"><span data-stu-id="1ad30-163">This approach does not render your content in three dimensions; it will not have perspective or depth.</span></span> <span data-ttu-id="1ad30-164">Sin embargo, resulta útil para varias tareas comunes:</span><span class="sxs-lookup"><span data-stu-id="1ad30-164">However, it is useful for several common tasks:</span></span>

-   <span data-ttu-id="1ad30-165">Crear un fondo 2D para una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-165">Creating a 2-D background for a 3-D scene.</span></span>
-   <span data-ttu-id="1ad30-166">Creación de una interfaz 2D delante de una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-166">Creating a 2-D interface in front of a 3-D scene.</span></span>
-   <span data-ttu-id="1ad30-167">Usar el muestreo múltiple de Direct3D al representar contenido de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-167">Using Direct3D multisampling when rendering Direct2D content.</span></span>

<span data-ttu-id="1ad30-168">En la sección siguiente se muestra cómo crear un fondo 2D para una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-168">The next section shows how to create a 2-D background for a 3-D scene.</span></span>

### <a name="example-draw-a-2-d-background"></a><span data-ttu-id="1ad30-169">Ejemplo: dibujar un fondo en 2D</span><span class="sxs-lookup"><span data-stu-id="1ad30-169">Example: Draw a 2-D Background</span></span>

<span data-ttu-id="1ad30-170">En los pasos siguientes se describe cómo crear un destino de representación de la superficie de DXGI y cómo usarlo para dibujar un fondo degradado.</span><span class="sxs-lookup"><span data-stu-id="1ad30-170">The following steps describe how to create a DXGI surface render target and use it to draw a gradient background.</span></span>

1.  <span data-ttu-id="1ad30-171">Use el método [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) para crear una cadena de intercambio para una [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (la variable *\_ pDevice de m* ).</span><span class="sxs-lookup"><span data-stu-id="1ad30-171">Use the [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) method to create a swap chain for an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (the *m\_pDevice* variable).</span></span> <span data-ttu-id="1ad30-172">La cadena de intercambio usa el formato [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) dxgi Format, uno de los formatos de dxgi admitidos por Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-172">The swap chain uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  <span data-ttu-id="1ad30-173">Use el método [**getBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la cadena de intercambio para obtener una superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-173">Use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span>

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  <span data-ttu-id="1ad30-174">Use la superficie de DXGI para crear un destino de representación de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-174">Use the DXGI surface to create a DXGI render target.</span></span>
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  <span data-ttu-id="1ad30-175">Use el destino de representación para dibujar un fondo degradado.</span><span class="sxs-lookup"><span data-stu-id="1ad30-175">Use the render target to draw a gradient background.</span></span>

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

<span data-ttu-id="1ad30-176">El código se omite en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1ad30-176">Code is omitted from this sample.</span></span>

## <a name="using-direct2d-content-as-a-texture"></a><span data-ttu-id="1ad30-177">Usar contenido de Direct2D como textura</span><span class="sxs-lookup"><span data-stu-id="1ad30-177">Using Direct2D Content as a Texture</span></span>

<span data-ttu-id="1ad30-178">Otra forma de usar el contenido de Direct2D con Direct3D es usar Direct2D para generar una textura 2D y después aplicar esa textura a un modelo 3D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-178">Another way to use Direct2D content with Direct3D is to use Direct2D to generate a 2-D texture and then apply that texture to a 3-D model.</span></span> <span data-ttu-id="1ad30-179">Para ello, cree un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtenga una superficie de dxgi a partir de la textura y, a continuación, use la superficie para crear un destino de representación de la superficie de dxgi.</span><span class="sxs-lookup"><span data-stu-id="1ad30-179">You do this by creating an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtaining a DXGI surface from the texture, and then using the surface to create a DXGI surface render target.</span></span> <span data-ttu-id="1ad30-180">La superficie **ID3D10Texture2D** debe usar la marca de enlace de destino de [**representación de \_ enlace \_ \_ D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) y usar un formato de dxgi compatible con los destinos de representación de la superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-180">The **ID3D10Texture2D** surface must use the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) bind flag and use a DXGI format supported by DXGI surface render targets.</span></span> <span data-ttu-id="1ad30-181">Para obtener una lista de formatos de DXGI compatibles, vea [formatos de píxeles compatibles y modos alfa](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="1ad30-181">For a list of supported DXGI formats, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

### <a name="example-use-direct2d-content-as-a-texture"></a><span data-ttu-id="1ad30-182">Ejemplo: uso de contenido de Direct2D como textura</span><span class="sxs-lookup"><span data-stu-id="1ad30-182">Example: Use Direct2D Content as a Texture</span></span>

<span data-ttu-id="1ad30-183">En los siguientes ejemplos se muestra cómo crear un destino de representación de la superficie de DXGI que se representa en una textura 2D (representada por un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span><span class="sxs-lookup"><span data-stu-id="1ad30-183">The following examples show how to create a DXGI surface render target that renders to a 2-D texture (represented by an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span></span>

1.  <span data-ttu-id="1ad30-184">En primer lugar, use un dispositivo Direct3D para crear una textura 2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-184">First, use a Direct3D device to create a 2-D texture.</span></span> <span data-ttu-id="1ad30-185">La textura usa las marcas de enlace del recurso de destino de representación de enlace de D3D10 y del **\_ \_ sombreador \_ de enlace de D3D10** y usa el formato de [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) dxgi, uno de los formatos de dxgi admitidos por Direct2D. [**\_ \_ \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag)</span><span class="sxs-lookup"><span data-stu-id="1ad30-185">The texture uses the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) and **D3D10\_BIND\_SHADER\_RESOURCE** bind flags, and it uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  <span data-ttu-id="1ad30-186">Use la textura para obtener una superficie de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1ad30-186">Use the texture to obtain a DXGI surface.</span></span>

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  <span data-ttu-id="1ad30-187">Use la superficie con el método [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para obtener un destino de representación de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-187">Use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to obtain a Direct2D render target.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

<span data-ttu-id="1ad30-188">Ahora que ha obtenido un destino de representación de Direct2D y lo ha asociado con una textura de Direct3D, puede usar el destino de representación para dibujar el contenido de Direct2D en esa textura, y puede aplicar esa textura a los primitivos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-188">Now that you have obtained a Direct2D render target and associated it with a Direct3D texture, you can use the render target to draw Direct2D content to that texture, and you can apply that texture to Direct3D primitives.</span></span>

<span data-ttu-id="1ad30-189">El código se omite en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1ad30-189">Code is omitted from this sample.</span></span>

## <a name="resizing-a-dxgi-surface-render-target"></a><span data-ttu-id="1ad30-190">Cambiar el tamaño de un destino de representación de la superficie de DXGI</span><span class="sxs-lookup"><span data-stu-id="1ad30-190">Resizing a DXGI Surface Render Target</span></span>

<span data-ttu-id="1ad30-191">Los destinos de representación de la superficie de DXGI no admiten el método [**ID2D1RenderTarget:: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) .</span><span class="sxs-lookup"><span data-stu-id="1ad30-191">DXGI surface render targets do not support the [**ID2D1RenderTarget::Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) method.</span></span> <span data-ttu-id="1ad30-192">Para cambiar el tamaño de un destino de representación de la superficie de DXGI, la aplicación debe liberarla y volver a crearla.</span><span class="sxs-lookup"><span data-stu-id="1ad30-192">To resize a DXGI surface render target, the application must release and re-create it.</span></span>

<span data-ttu-id="1ad30-193">Esta operación puede crear problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1ad30-193">This operation can potentially create performance issues.</span></span> <span data-ttu-id="1ad30-194">El destino de representación podría ser el último recurso de Direct2D activo que mantiene una referencia al [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) asociado a la superficie de DXGI del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1ad30-194">The render target might be the last active Direct2D resource that keeps a reference to the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the render target's DXGI surface.</span></span> <span data-ttu-id="1ad30-195">Si la aplicación libera el destino de representación y se destruye la referencia **ID3D10Device1** , se debe volver a crear una nueva.</span><span class="sxs-lookup"><span data-stu-id="1ad30-195">If the application releases the render target and the **ID3D10Device1** reference is destroyed, a new one must be recreated.</span></span>

<span data-ttu-id="1ad30-196">Puede evitar esta operación potencialmente costosa manteniendo al menos un recurso de Direct2D creado por el destino de presentación mientras vuelve a crear ese destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1ad30-196">You can avoid this potentially expensive operation by keeping at least one Direct2D resource that was created by the render target while you re-create that render target.</span></span> <span data-ttu-id="1ad30-197">A continuación se muestran algunos recursos de Direct2D que funcionan para este enfoque:</span><span class="sxs-lookup"><span data-stu-id="1ad30-197">The following are some Direct2D resources that work for this approach:</span></span>

-   <span data-ttu-id="1ad30-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (que un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)puede mantener indirectamente)</span><span class="sxs-lookup"><span data-stu-id="1ad30-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (which may be held indirectly by an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span></span>
-   [<span data-ttu-id="1ad30-199">**ID2D1Layer**</span><span class="sxs-lookup"><span data-stu-id="1ad30-199">**ID2D1Layer**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [<span data-ttu-id="1ad30-200">**ID2D1Mesh**</span><span class="sxs-lookup"><span data-stu-id="1ad30-200">**ID2D1Mesh**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

<span data-ttu-id="1ad30-201">Para dar cabida a este enfoque, el método de cambiar tamaño debe probar para ver si el dispositivo Direct3D está disponible.</span><span class="sxs-lookup"><span data-stu-id="1ad30-201">To accommodate this approach, your resize method should test to see whether the Direct3D device is available.</span></span> <span data-ttu-id="1ad30-202">Si está disponible, libere y vuelva a crear los destinos de representación de la superficie de DXGI, pero Mantenga todos los recursos que crearon previamente y vuelva a usarlos.</span><span class="sxs-lookup"><span data-stu-id="1ad30-202">If it is available, release and re-create your DXGI surface render targets, but keep all the resources that they created previously and reuse them.</span></span> <span data-ttu-id="1ad30-203">Esto funciona porque, como se describe en la [información general](resources-and-resource-domains.md)de los recursos, los recursos creados por dos destinos de representación son compatibles cuando ambos destinos de representación están asociados al mismo dispositivo de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1ad30-203">This works because, as described in the [Resources Overview](resources-and-resource-domains.md), resources created by two render targets are compatible when both render targets are associated with the same Direct3D device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ad30-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ad30-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad30-205">Formatos de píxel admitidos y modos alfa</span><span class="sxs-lookup"><span data-stu-id="1ad30-205">Supported Pixel Formats and Alpha Modes</span></span>](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

<span data-ttu-id="1ad30-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="1ad30-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span></span>
</dt> <dt>

[<span data-ttu-id="1ad30-207">Gráficos de Windows DirectX</span><span class="sxs-lookup"><span data-stu-id="1ad30-207">Windows DirectX Graphics</span></span>](../graphics-and-multimedia.md)
</dt> </dl>

 

 
---
title: Uso compartido de la superficie entre las API de gráficos de Windows
description: En este tema se proporciona información general técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, como Direct3D 11, Direct2D, DirectWrite, Direct3D 10 y Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794223"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="508bb-103">Uso compartido de la superficie entre las API de gráficos de Windows</span><span class="sxs-lookup"><span data-stu-id="508bb-103">Surface Sharing Between Windows Graphics APIs</span></span>

<span data-ttu-id="508bb-104">En este tema se proporciona información general técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, como Direct3D 11, Direct2D, DirectWrite, Direct3D 10 y Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="508bb-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="508bb-105">Si ya tiene conocimientos prácticos de estas API, este documento puede ayudarle a usar varias API para representarlas en la misma superficie en una aplicación diseñada para los sistemas operativos Windows 7 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="508bb-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="508bb-106">En este tema también se proporcionan instrucciones de prácticas recomendadas y punteros a recursos adicionales.</span><span class="sxs-lookup"><span data-stu-id="508bb-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="508bb-107">Para la interoperabilidad de Direct2D y DirectWrite en el tiempo de ejecución de DirectX 11,1, puede usar [dispositivos y contextos de dispositivo de direct2d](/windows/desktop/Direct2D/devices-and-device-contexts) para representarlos directamente en dispositivos de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="508bb-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="508bb-108">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="508bb-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="508bb-109">Introducción</span><span class="sxs-lookup"><span data-stu-id="508bb-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="508bb-110">Información general sobre la interoperabilidad de API</span><span class="sxs-lookup"><span data-stu-id="508bb-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="508bb-111">Escenarios de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="508bb-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="508bb-112">Uso compartido de dispositivos de Direct3D 10,1 con Direct2D</span><span class="sxs-lookup"><span data-stu-id="508bb-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="508bb-113">Superficies compartidas de DXGI 1,1 sincronizadas</span><span class="sxs-lookup"><span data-stu-id="508bb-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="508bb-114">Interoperabilidad entre las API basadas en Direct3D 9Ex y DXGI</span><span class="sxs-lookup"><span data-stu-id="508bb-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="508bb-115">Conclusión</span><span class="sxs-lookup"><span data-stu-id="508bb-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="508bb-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="508bb-116">Introduction</span></span>

<span data-ttu-id="508bb-117">En este documento, la interoperabilidad de la API de gráficos de Windows hace referencia al uso compartido de la misma superficie de representación en distintas API.</span><span class="sxs-lookup"><span data-stu-id="508bb-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="508bb-118">Este tipo de interoperabilidad permite a las aplicaciones crear pantallas atractivas aprovechando varias API de gráficos de Windows y facilitar la migración a nuevas tecnologías manteniendo la compatibilidad con las API existentes.</span><span class="sxs-lookup"><span data-stu-id="508bb-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="508bb-119">En Windows 7 (y Windows Vista SP2 con Windows 7 Interop Pack, vista 7IP), las API de representación de gráficos son Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9C y las API de Direct3D anteriores, así como GDI y GDI+.</span><span class="sxs-lookup"><span data-stu-id="508bb-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="508bb-120">Windows Imaging Component (WIC) y DirectWrite son tecnologías relacionadas con el procesamiento de imágenes y Direct2D realiza la representación de texto.</span><span class="sxs-lookup"><span data-stu-id="508bb-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="508bb-121">DirectX video Acceleration API (DXVA), basado en Direct3D 9C y Direct3D 9Ex, se usa para el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="508bb-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="508bb-122">A medida que las API de gráficos de Windows evolucionan hasta estar basadas en Direct3D, Microsoft está invirtiendo más en garantizar la interoperabilidad entre las API.</span><span class="sxs-lookup"><span data-stu-id="508bb-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="508bb-123">Las API de Direct3D que se acaban de desarrollar y las API de nivel superior basadas en las API de Direct3D también proporcionan compatibilidad cuando es necesario para la compatibilidad de puente con las API anteriores.</span><span class="sxs-lookup"><span data-stu-id="508bb-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="508bb-124">Para ilustrar, las aplicaciones de Direct2D pueden usar Direct3D 10,1 compartiendo un dispositivo Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="508bb-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="508bb-125">Además, las API de Direct3D 11, Direct2D y Direct3D 10,1 pueden aprovechar las ventajas de la infraestructura de gráficos de DirectX (DXGI) 1,1, que permite que las superficies compartidas sincronizadas sean totalmente compatibles con la interoperabilidad entre estas API.</span><span class="sxs-lookup"><span data-stu-id="508bb-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="508bb-126">Las API basadas en DXGI 1,1 interoperan con GDI y con GDI+ por asociación mediante la obtención del contexto de dispositivo GDI desde una superficie de DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="508bb-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="508bb-127">Para obtener más información, consulte la documentación de interoperabilidad de DXGI y GDI disponible en MSDN.</span><span class="sxs-lookup"><span data-stu-id="508bb-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="508bb-128">El uso compartido de la superficie sin sincronizar es compatible con el tiempo de ejecución de Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="508bb-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="508bb-129">Las aplicaciones de vídeo basadas en DXVA pueden usar la aplicación auxiliar de interoperabilidad de Direct3D 9Ex y DXGI para la interoperabilidad de los DXVA basados en 9Ex de Direct3D con Direct3D 11 para el sombreador de cálculo, o pueden interoperar con Direct2D para controles 2D o representación de texto.</span><span class="sxs-lookup"><span data-stu-id="508bb-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="508bb-130">WIC y DirectWrite también interoperan con GDI, Direct2D y por asociación y otras API de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="508bb-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="508bb-131">Direct3D 10,0, Direct3D 9C y los tiempos de ejecución de Direct3D más antiguos no admiten superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="508bb-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="508bb-132">Las copias de memoria del sistema se seguirán usando para la interoperabilidad con las API basadas en GDI o en DXGI.</span><span class="sxs-lookup"><span data-stu-id="508bb-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="508bb-133">Tenga en cuenta que los escenarios de interoperabilidad de este documento hacen referencia a varias API de gráficos que se representan en una superficie de representación compartida, en lugar de en la misma ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="508bb-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="508bb-134">La sincronización de API independientes que tienen como destino diferentes superficies que se componen en la misma ventana está fuera del ámbito de este documento.</span><span class="sxs-lookup"><span data-stu-id="508bb-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="508bb-135">Información general sobre la interoperabilidad de API</span><span class="sxs-lookup"><span data-stu-id="508bb-135">API Interoperability Overview</span></span>

<span data-ttu-id="508bb-136">La interoperabilidad del uso compartido de Surface de las API de gráficos de Windows se puede describir en términos de escenarios de API a API y la funcionalidad de interoperabilidad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="508bb-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="508bb-137">A partir de Windows 7 y a partir de Windows Vista SP2 con 7IP, las nuevas API y los tiempos de ejecución asociados incluyen Direct2D y tecnologías relacionadas: Direct3D 11 y DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="508bb-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="508bb-138">También se ha mejorado el rendimiento de GDI en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="508bb-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="508bb-139">Direct3D 10,1 se presentó en Windows Vista SP1.</span><span class="sxs-lookup"><span data-stu-id="508bb-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="508bb-140">En el diagrama siguiente se muestra la compatibilidad de interoperabilidad entre las API.</span><span class="sxs-lookup"><span data-stu-id="508bb-140">The following diagram shows the interoperability support between APIs.</span></span>

![diagrama de compatibilidad de interoperabilidad entre las API de gráficos de Windows](images/surface-sharing-interoperability.png)

<span data-ttu-id="508bb-142">En este diagrama, las flechas muestran escenarios de interoperabilidad en los que las API conectadas pueden tener acceso a la misma superficie.</span><span class="sxs-lookup"><span data-stu-id="508bb-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="508bb-143">Las flechas azules indican mecanismos de interoperabilidad introducidos en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="508bb-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="508bb-144">Las flechas verdes indican compatibilidad de interoperabilidad con nuevas API o mejoras que ayudan a las API más antiguas a interoperar con las API más recientes.</span><span class="sxs-lookup"><span data-stu-id="508bb-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="508bb-145">Por ejemplo, las flechas verdes representan el uso compartido de dispositivos, la compatibilidad con superficies compartidas sincronizadas, la aplicación auxiliar de sincronización Direct3D 9Ex/DXGI y la obtención de un contexto de dispositivo GDI desde una superficie compatible.</span><span class="sxs-lookup"><span data-stu-id="508bb-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="508bb-146">Escenarios de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="508bb-146">Interoperability Scenarios</span></span>

<span data-ttu-id="508bb-147">A partir de Windows 7 y Windows Vista 7IP, las ofertas estándar de las API de gráficos de Windows admiten varias API que se representan en la misma superficie de DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="508bb-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="508bb-148">**Direct3D 11, Direct3D 10,1, Direct2D: interoperabilidad entre sí**</span><span class="sxs-lookup"><span data-stu-id="508bb-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="508bb-149">Las API de Direct3D 11, Direct3D 10,1 y Direct2D (y sus API relacionadas como DirectWrite y WIC) pueden interoperar entre sí mediante el uso compartido de dispositivos Direct3D 10,1 o las superficies compartidas sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="508bb-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="508bb-150">Uso compartido de dispositivos de Direct3D 10,1 con Direct2D</span><span class="sxs-lookup"><span data-stu-id="508bb-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="508bb-151">El uso compartido de dispositivos entre Direct2D y Direct3D 10,1 permite que una aplicación use ambas API para representar sin problemas y de forma eficaz en la misma superficie de DXGI 1,1, con el mismo objeto de dispositivo Direct3D subyacente.</span><span class="sxs-lookup"><span data-stu-id="508bb-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="508bb-152">Direct2D proporciona la capacidad de llamar a las API de Direct2D mediante un dispositivo Direct3D 10,1 existente, aprovechando el hecho de que Direct2D se basa en los tiempos de ejecución de Direct3D 10,1 y DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="508bb-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="508bb-153">En los fragmentos de código siguientes se muestra cómo Direct2D obtiene el destino de representación del dispositivo Direct3D 10,1 de una superficie de DXGI 1,1 asociada con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="508bb-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="508bb-154">El destino de representación del dispositivo Direct3D 10,1 puede ejecutar llamadas de dibujo de Direct2D entre las API BeginDraw y EndDraw.</span><span class="sxs-lookup"><span data-stu-id="508bb-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



<span data-ttu-id="508bb-155">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="508bb-155">**Remarks**</span></span>

-   <span data-ttu-id="508bb-156">El dispositivo Direct3D 10,1 asociado debe admitir el formato BGRA.</span><span class="sxs-lookup"><span data-stu-id="508bb-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="508bb-157">Dicho dispositivo se creó mediante una llamada a D3D10CreateDevice1 con el parámetro D3D10 \_ Create \_ Device \_ BGRA \_ support.</span><span class="sxs-lookup"><span data-stu-id="508bb-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="508bb-158">El formato BGRA se admite a partir del nivel de características 9,1 de Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="508bb-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="508bb-159">La aplicación no debe crear varios ID2D1RenderTargets que se asocien al mismo dispositivo de Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="508bb-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="508bb-160">Para obtener un rendimiento óptimo, mantenga al menos un recurso en todo momento, como texturas o superficies asociadas al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="508bb-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="508bb-161">El uso compartido de dispositivos es apto para el uso en proceso de un solo subproceso de un dispositivo de representación compartido por las API de representación de Direct3D 10,1 y Direct2D.</span><span class="sxs-lookup"><span data-stu-id="508bb-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="508bb-162">Las superficies compartidas sincronizadas habilitan el uso de varios subprocesos, en proceso y fuera de proceso de varios dispositivos de representación usados por las API de Direct3D 10,1, Direct2D y Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="508bb-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="508bb-163">Otro método de interoperabilidad de Direct3D 10,1 y Direct2D es mediante ID3D1RenderTarget:: CreateSharedBitmap, que crea un objeto ID2D1Bitmap a partir de IDXGISurface.</span><span class="sxs-lookup"><span data-stu-id="508bb-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="508bb-164">Puede escribir una escena de Direct3D 10.1 en el mapa de bits y representarla con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="508bb-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="508bb-165">Para obtener más información, vea [ID2D1RenderTarget:: CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span><span class="sxs-lookup"><span data-stu-id="508bb-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="508bb-166">Rasterización de software de Direct2D</span><span class="sxs-lookup"><span data-stu-id="508bb-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="508bb-167">El uso compartido de dispositivos con Direct3D 10,1 no se admite cuando se usa el representador de software de Direct2D, por ejemplo, mediante la especificación de D2D1 \_ presentación de \_ destino \_ \_ forzar representación \_ \_ de software en D2D1 \_ representar \_ el uso de destino \_ al crear un destino de representación de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="508bb-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="508bb-168">Direct2D puede usar el rasterizador de software WARP10 para compartir dispositivos con Direct3D 10 o Direct3D 11, pero el rendimiento disminuye considerablemente.</span><span class="sxs-lookup"><span data-stu-id="508bb-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="508bb-169">Superficies compartidas de DXGI 1,1 sincronizadas</span><span class="sxs-lookup"><span data-stu-id="508bb-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="508bb-170">Las API de Direct3D 11, Direct3D 10,1 y Direct2D usan DXGI 1,1, que proporciona la funcionalidad para sincronizar la lectura y la escritura en la misma superficie de memoria de vídeo (DXGISurface1) en dos o más dispositivos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="508bb-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="508bb-171">Los dispositivos de representación que usan superficies compartidas sincronizadas pueden ser dispositivos de Direct3D 10,1 o Direct3D 11, cada uno de los cuales se ejecuta en el mismo proceso o en procesos cruzados.</span><span class="sxs-lookup"><span data-stu-id="508bb-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="508bb-172">Las aplicaciones pueden usar superficies compartidas sincronizadas para interoperar entre cualquier dispositivo basado en DXGI 1,1, como Direct3D 11 y Direct3D 10,1, o entre Direct3D 11 y Direct2D, obteniendo el dispositivo Direct3D 10,1 del objeto de destino de representación de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="508bb-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="508bb-173">En Direct3D 10,1 y las API de versiones posteriores, para usar DXGI 1,1, asegúrese de que el dispositivo Direct3D se crea con un objeto de adaptador de DXGI 1,1, que se enumera desde el objeto de fábrica de DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="508bb-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="508bb-174">Llame a CreateDXGIFactory1 para crear el objeto IDXGIFactory1 y EnumAdapters1 para enumerar el objeto IDXGIAdapter1.</span><span class="sxs-lookup"><span data-stu-id="508bb-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="508bb-175">El objeto IDXGIAdapter1 debe pasarse como parte de la llamada a D3D10CreateDevice o D3D10CreateDeviceAndSwapChain.</span><span class="sxs-lookup"><span data-stu-id="508bb-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="508bb-176">Para obtener más información sobre las API de DXGI 1,1, consulte la [Guía de programación para dxgi](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="508bb-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="508bb-177">API existentes</span><span class="sxs-lookup"><span data-stu-id="508bb-177">APIs</span></span>

<span data-ttu-id="508bb-178">**\_Recurso \_ compartido D3D10 \_ varios \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="508bb-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="508bb-179">Al crear el recurso compartido Synchronized, establezca el \_ recurso D3D10 \_ \_ Shared \_ KEYEDMUTEX en la \_ marca D3D10 Resource \_ Misc \_ .</span><span class="sxs-lookup"><span data-stu-id="508bb-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="508bb-180">**\_Recurso \_ compartido D3D10 \_ varios \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="508bb-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="508bb-181">Permite que el recurso creado se sincronice con las API IDXGIKeyedMutex:: AcquireSync y ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="508bb-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="508bb-182">Las siguientes API de Direct3D 10,1 de creación de recursos que toman un \_ parámetro de marca de varios recursos D3D10 se han \_ \_ ampliado para admitir la nueva marca.</span><span class="sxs-lookup"><span data-stu-id="508bb-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="508bb-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="508bb-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="508bb-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="508bb-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="508bb-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="508bb-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="508bb-186">ID3D10Device1::CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="508bb-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="508bb-187">Si se llama a cualquiera de las funciones enumeradas con \_ el \_ \_ conjunto de indicadores compartidos de KEYEDMUTEX de recursos D3D10 \_ , se puede consultar la interfaz devuelta para una interfaz IDXGIKeyedMutex, que implementa las API AcquireSync y ReleaseSync para sincronizar el acceso a la superficie.</span><span class="sxs-lookup"><span data-stu-id="508bb-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="508bb-188">El dispositivo que crea la superficie y cualquier otro dispositivo que abra la superficie (mediante OpenSharedResource) es necesario para llamar a IDXGIKeyedMutex:: AcquireSync antes que cualquier comando de representación a la superficie y IDXGIKeyedMutex:: ReleaseSync cuando finaliza la representación.</span><span class="sxs-lookup"><span data-stu-id="508bb-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="508bb-189">Los dispositivos de ALABEo y de referencia no admiten recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="508bb-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="508bb-190">Si se intenta crear un recurso con esta marca en un dispositivo de ALABEo o de referencia, el método Create devolverá un \_ código de error E OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="508bb-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="508bb-191">**INTERFAZ IDXGIKEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="508bb-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="508bb-192">Una nueva interfaz en DXGI 1,1, IDXGIKeyedMutex, representa una exclusión mutua con clave, que permite el acceso exclusivo a un recurso compartido que usan varios dispositivos.</span><span class="sxs-lookup"><span data-stu-id="508bb-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="508bb-193">Para obtener documentación de referencia sobre esta interfaz y sus dos métodos, AcquireSync y ReleaseSync, consulte [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="508bb-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="508bb-194">Ejemplo: uso compartido de superficies sincronizadas entre dos dispositivos de Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="508bb-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="508bb-195">En el ejemplo siguiente se muestra cómo compartir una superficie entre dos dispositivos de Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="508bb-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="508bb-196">La superficie compartida sincronizada se crea mediante un dispositivo Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="508bb-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



<span data-ttu-id="508bb-197">El mismo dispositivo Direct3D 10.1 puede obtener la superficie compartida sincronizada para la representación llamando a AcquireSync y, a continuación, liberando la superficie de la representación de otro dispositivo llamando a ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="508bb-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="508bb-198">Cuando no se comparte la superficie compartida sincronizada con ningún otro dispositivo Direct3D, el creador puede obtener y liberar la superficie compartida sincronizada (para iniciar y finalizar la representación) adquiriendo y liberando con el mismo valor de clave.</span><span class="sxs-lookup"><span data-stu-id="508bb-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



<span data-ttu-id="508bb-199">El segundo dispositivo Direct3D 10.1 puede obtener la superficie compartida sincronizada para la representación llamando a AcquireSync y, a continuación, liberando la superficie de la representación del primer dispositivo mediante una llamada a ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="508bb-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="508bb-200">Tenga en cuenta que el dispositivo 2 puede adquirir la superficie compartida sincronizada con el mismo valor de clave que el especificado en la llamada de ReleaseSync por dispositivo 1.</span><span class="sxs-lookup"><span data-stu-id="508bb-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



<span data-ttu-id="508bb-201">Los dispositivos adicionales que comparten la misma superficie pueden tomar la adquisición y liberación de la superficie mediante claves adicionales, como se muestra en las siguientes llamadas.</span><span class="sxs-lookup"><span data-stu-id="508bb-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



<span data-ttu-id="508bb-202">Tenga en cuenta que una aplicación real siempre puede representarse en una superficie intermedia que luego se copia en la superficie compartida para evitar que un dispositivo espere en otro dispositivo que comparta la superficie.</span><span class="sxs-lookup"><span data-stu-id="508bb-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="508bb-203">Usar superficies compartidas sincronizadas con Direct2D y Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="508bb-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="508bb-204">Del mismo modo, para el uso compartido entre las API de Direct3D 11 y Direct3D 10,1, se puede crear una superficie compartida sincronizada desde cualquier dispositivo de API y compartirla con los otros dispositivos de la API, dentro o fuera del proceso.</span><span class="sxs-lookup"><span data-stu-id="508bb-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="508bb-205">Las aplicaciones que usan Direct2D pueden compartir un dispositivo Direct3D 10,1 y usar una superficie compartida sincronizada para interoperar con Direct3D 11 u otros dispositivos de Direct3D 10,1, tanto si pertenecen al mismo proceso como a procesos diferentes.</span><span class="sxs-lookup"><span data-stu-id="508bb-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="508bb-206">Sin embargo, para las aplicaciones de un solo proceso y de un solo subproceso, el uso compartido de dispositivos es el método de interoperabilidad más eficaz y de alto rendimiento entre Direct2D y Direct3D 10 o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="508bb-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="508bb-207">Rasterizador de software</span><span class="sxs-lookup"><span data-stu-id="508bb-207">Software Rasterizer</span></span>

<span data-ttu-id="508bb-208">Las superficies compartidas sincronizadas no se admiten cuando las aplicaciones usan los rasterizadores de software Direct3D o Direct2D, incluido el rasterizador de referencia y el ALABEo, en lugar de usar la aceleración de hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="508bb-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="508bb-209">Interoperabilidad entre las API basadas en Direct3D 9Ex y DXGI</span><span class="sxs-lookup"><span data-stu-id="508bb-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="508bb-210">Las API de Direct3D 9Ex incluyen la noción de uso compartido de la superficie para permitir que otras API lean desde la superficie compartida.</span><span class="sxs-lookup"><span data-stu-id="508bb-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="508bb-211">Para compartir la lectura y la escritura en una superficie compartida de Direct3D 9Ex, debe agregar la sincronización manual a la propia aplicación.</span><span class="sxs-lookup"><span data-stu-id="508bb-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="508bb-212">Superficies compartidas de Direct3D 9Ex más la aplicación auxiliar de sincronización manual</span><span class="sxs-lookup"><span data-stu-id="508bb-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="508bb-213">La tarea más fundamental de la interoperabilidad de Direct3D 9Ex y Direct3D 10 o 11 es pasar una sola superficie del primer dispositivo (dispositivo a) al segundo (dispositivo B), de modo que cuando el dispositivo B adquiera un identificador en la superficie, se garantice que la representación del dispositivo a se ha completado.</span><span class="sxs-lookup"><span data-stu-id="508bb-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="508bb-214">Por lo tanto, el dispositivo B puede usar esta superficie sin preocuparse.</span><span class="sxs-lookup"><span data-stu-id="508bb-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="508bb-215">Esto es muy similar al problema clásico productor-consumidor y este debate modela el problema de esa manera.</span><span class="sxs-lookup"><span data-stu-id="508bb-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="508bb-216">El primer dispositivo que usa la superficie y después lo cede es el productor (dispositivo A) y el dispositivo que está esperando inicialmente es el consumidor (dispositivo B).</span><span class="sxs-lookup"><span data-stu-id="508bb-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="508bb-217">Cualquier aplicación real es más sofisticada que esta y encadenará varios bloques de creación productor-consumidor para crear la funcionalidad deseada.</span><span class="sxs-lookup"><span data-stu-id="508bb-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="508bb-218">Los bloques de creación productor-consumidor se implementan en el ayudante mediante una cola de superficies.</span><span class="sxs-lookup"><span data-stu-id="508bb-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="508bb-219">El productor pone en cola las superficies y las pone en cola el consumidor.</span><span class="sxs-lookup"><span data-stu-id="508bb-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="508bb-220">La aplicación auxiliar presenta tres interfaces COM: ISurfaceQueue, ISurfaceProducer y ISurfaceConsumer.</span><span class="sxs-lookup"><span data-stu-id="508bb-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="508bb-221">Información general de High-Level de la aplicación auxiliar</span><span class="sxs-lookup"><span data-stu-id="508bb-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="508bb-222">El objeto ISurfaceQueue es el bloque de creación para usar las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="508bb-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="508bb-223">Se crea con un dispositivo Direct3D inicializado y una descripción para crear un número fijo de superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="508bb-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="508bb-224">El objeto Queue administra la creación de recursos y la apertura de código.</span><span class="sxs-lookup"><span data-stu-id="508bb-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="508bb-225">El número y tipo de superficies son fijos. una vez creadas las superficies, la aplicación no las puede agregar ni quitar.</span><span class="sxs-lookup"><span data-stu-id="508bb-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="508bb-226">Cada instancia del objeto ISurfaceQueue proporciona una especie de calle unidireccional que se puede usar para enviar superficies desde el dispositivo productor al dispositivo de consumo.</span><span class="sxs-lookup"><span data-stu-id="508bb-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="508bb-227">Se pueden usar varias calles unidireccionales para habilitar escenarios de uso compartido de superficie entre dispositivos de aplicaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="508bb-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="508bb-228">**Creación/duración del objeto**</span><span class="sxs-lookup"><span data-stu-id="508bb-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="508bb-229">Hay dos maneras de crear el objeto de cola: a través de CreateSurfaceQueue o mediante el método Clone de ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="508bb-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="508bb-230">Dado que las interfaces son objetos COM, se aplica la administración de la duración de COM estándar.</span><span class="sxs-lookup"><span data-stu-id="508bb-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="508bb-231">**Modelo productor/consumidor**</span><span class="sxs-lookup"><span data-stu-id="508bb-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="508bb-232">Enqueue (): el productor llama a esta función para indicar que se ha realizado con la superficie, que ahora puede estar disponible para otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="508bb-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="508bb-233">Al volver de esta función, el dispositivo productor ya no tiene derechos en la superficie y no es seguro seguir utilizándolo.</span><span class="sxs-lookup"><span data-stu-id="508bb-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="508bb-234">Quitar de la cola (): el dispositivo consumidor llama a esta función para obtener una superficie compartida.</span><span class="sxs-lookup"><span data-stu-id="508bb-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="508bb-235">La API garantiza que todas las superficies que se hayan quitado de la cola están listas para usarse.</span><span class="sxs-lookup"><span data-stu-id="508bb-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="508bb-236">**Metadatos**</span><span class="sxs-lookup"><span data-stu-id="508bb-236">**Metadata**</span></span>  
<span data-ttu-id="508bb-237">La API admite la Asociación de metadatos con las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="508bb-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="508bb-238">Enqueue () tiene la opción de especificar metadatos adicionales que se pasarán al dispositivo de consumo.</span><span class="sxs-lookup"><span data-stu-id="508bb-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="508bb-239">Los metadatos deben ser inferiores a un máximo conocido en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="508bb-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="508bb-240">La eliminación de la cola () puede pasar opcionalmente un búfer y un puntero al tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="508bb-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="508bb-241">La cola rellena el búfer con los metadatos de la llamada de puesta en cola correspondiente.</span><span class="sxs-lookup"><span data-stu-id="508bb-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="508bb-242">**Clonación**</span><span class="sxs-lookup"><span data-stu-id="508bb-242">**Cloning**</span></span>  
<span data-ttu-id="508bb-243">Cada objeto ISurfaceQueue resuelve una sincronización unidireccional.</span><span class="sxs-lookup"><span data-stu-id="508bb-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="508bb-244">Suponemos que la mayoría de las aplicaciones que usan esta API usarán un sistema cerrado.</span><span class="sxs-lookup"><span data-stu-id="508bb-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="508bb-245">El sistema cerrado más sencillo con dos dispositivos que envían superficies hacia atrás y hacia delante requiere dos colas.</span><span class="sxs-lookup"><span data-stu-id="508bb-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="508bb-246">El objeto ISurfaceQueue tiene un método Clone () para que sea posible crear varias colas que formen parte de la misma canalización mayor.</span><span class="sxs-lookup"><span data-stu-id="508bb-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="508bb-247">Clone crea un nuevo objeto ISurfaceQueue a partir de uno existente y comparte todos los recursos abiertos entre ellos.</span><span class="sxs-lookup"><span data-stu-id="508bb-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="508bb-248">El objeto resultante tiene exactamente las mismas superficies que la cola de origen.</span><span class="sxs-lookup"><span data-stu-id="508bb-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="508bb-249">Las colas clonadas pueden tener distintos tamaños de metadatos entre sí.</span><span class="sxs-lookup"><span data-stu-id="508bb-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="508bb-250">**Superficies**</span><span class="sxs-lookup"><span data-stu-id="508bb-250">**Surfaces**</span></span>  
<span data-ttu-id="508bb-251">ISurfaceQueue asume la responsabilidad de crear y administrar sus superficies.</span><span class="sxs-lookup"><span data-stu-id="508bb-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="508bb-252">No es válido poner en cola superficies arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="508bb-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="508bb-253">Además, una superficie solo debe tener un "propietario" activo.</span><span class="sxs-lookup"><span data-stu-id="508bb-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="508bb-254">Debe estar en una cola específica o ser utilizada por un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="508bb-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="508bb-255">No es válido tener en varias colas o para que los dispositivos continúen usando la superficie después de ponerla en cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="508bb-256">Detalles de la API</span><span class="sxs-lookup"><span data-stu-id="508bb-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="508bb-257">IsurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="508bb-257">IsurfaceQueue</span></span>

<span data-ttu-id="508bb-258">La cola es responsable de la creación y el mantenimiento de los recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="508bb-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="508bb-259">También proporciona la funcionalidad para encadenar varias colas mediante Clone.</span><span class="sxs-lookup"><span data-stu-id="508bb-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="508bb-260">La cola tiene métodos que abren el dispositivo productor y un dispositivo de consumo.</span><span class="sxs-lookup"><span data-stu-id="508bb-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="508bb-261">Solo una de ellas se puede abrir en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="508bb-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="508bb-262">La cola expone las siguientes API:</span><span class="sxs-lookup"><span data-stu-id="508bb-262">The queue exposes the following APIs:</span></span>



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="508bb-263">CreateSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="508bb-263">CreateSurfaceQueue</span></span>          | <span data-ttu-id="508bb-264">Crea un objeto ISurfaceQueue (la cola "raíz").</span><span class="sxs-lookup"><span data-stu-id="508bb-264">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="508bb-265">ISurfaceQueue::OpenConsumer</span><span class="sxs-lookup"><span data-stu-id="508bb-265">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="508bb-266">Devuelve una interfaz para el dispositivo de consumo que se va a quitar de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-266">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="508bb-267">ISurfaceQueue::OpenProducer</span><span class="sxs-lookup"><span data-stu-id="508bb-267">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="508bb-268">Devuelve una interfaz para el dispositivo de producción que se va a poner en cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-268">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="508bb-269">ISurfaceQueue:: Clone</span><span class="sxs-lookup"><span data-stu-id="508bb-269">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="508bb-270">Crea un objeto ISurfaceQueue que comparte superficies con el objeto de cola raíz.</span><span class="sxs-lookup"><span data-stu-id="508bb-270">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="508bb-271">**CreateSurfaceQueue**</span><span class="sxs-lookup"><span data-stu-id="508bb-271">**CreateSurfaceQueue**</span></span>  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



<span data-ttu-id="508bb-272">**Miembros**</span><span class="sxs-lookup"><span data-stu-id="508bb-272">**Members**</span></span>  

<span data-ttu-id="508bb-273">**Ancho**, **alto**  las dimensiones de las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="508bb-273">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="508bb-274">Todas las superficies compartidas deben tener las mismas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="508bb-274">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="508bb-275">**Formato** Formato de las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="508bb-275">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="508bb-276">Todas las superficies compartidas deben tener el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="508bb-276">All shared surfaces must have the same format.</span></span> <span data-ttu-id="508bb-277">Los formatos válidos dependen de los dispositivos que se vayan a usar, ya que los distintos pares de dispositivos pueden compartir distintos tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="508bb-277">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="508bb-278">**NumSurfaces**  El número de superficies que forman parte de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-278">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="508bb-279">Se trata de un número fijo.</span><span class="sxs-lookup"><span data-stu-id="508bb-279">This is a fixed number.</span></span>  
 <span data-ttu-id="508bb-280">**MetaDataSize**  Tamaño máximo del búfer de metadatos.</span><span class="sxs-lookup"><span data-stu-id="508bb-280">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="508bb-281">**Marcas**  de  Marcas para controlar el comportamiento de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-281">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="508bb-282">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="508bb-282">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="508bb-283">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="508bb-283">**Parameters**</span></span>

 <span data-ttu-id="508bb-284">*pDesc* \[ en \]  la descripción de la cola de superficie compartida que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="508bb-284">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="508bb-285">*pDevice* \[ en \]  el dispositivo que se debe usar para crear las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="508bb-285">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="508bb-286">Se trata de un parámetro explícito debido a una característica de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="508bb-286">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="508bb-287">En el caso de las superficies compartidas entre Direct3D 9 y Direct3D 10, las superficies deben crearse con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="508bb-287">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="508bb-288">*ppQueue* \[ fuera \]  de la devolución, contiene un puntero al objeto ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="508bb-288">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="508bb-289">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="508bb-289">**Return Values**</span></span>

<span data-ttu-id="508bb-290">Si *pDevice* no es capaz de compartir recursos, esta función devuelve una \_ \_ llamada no válida de DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="508bb-290">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="508bb-291">Esta función crea los recursos.</span><span class="sxs-lookup"><span data-stu-id="508bb-291">This function creates the resources.</span></span> <span data-ttu-id="508bb-292">Si se produce un error, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="508bb-292">If it fails, it returns an error.</span></span> <span data-ttu-id="508bb-293">Si se realiza correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="508bb-293">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="508bb-294">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="508bb-294">**Remarks**</span></span>

<span data-ttu-id="508bb-295">Al crear el objeto de cola, también se crean todas las superficies.</span><span class="sxs-lookup"><span data-stu-id="508bb-295">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="508bb-296">Se supone que todas las superficies son destinos de representación 2D y se crearán con el \_ destino de representación de enlace D3D10 y el conjunto de \_ \_ \_ \_ marcadores de recursos del sombreador de enlace D3D10 \_ (o las marcas equivalentes para los diferentes runtimes).</span><span class="sxs-lookup"><span data-stu-id="508bb-296">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="508bb-297">El desarrollador puede especificar una marca que indica si varios subprocesos tendrán acceso a la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-297">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="508bb-298">Si no se establece ningún marcador (**Flags** = = 0), varios subprocesos usarán la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-298">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="508bb-299">El desarrollador puede especificar el acceso de un solo subproceso, que desactiva el código de sincronización y proporciona una mejora del rendimiento para esos casos.</span><span class="sxs-lookup"><span data-stu-id="508bb-299">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="508bb-300">Cada cola clonada tiene su propia marca, por lo que es posible que las distintas colas del sistema tengan controles de sincronización diferentes.</span><span class="sxs-lookup"><span data-stu-id="508bb-300">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="508bb-301">**Apertura de un productor**</span><span class="sxs-lookup"><span data-stu-id="508bb-301">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="508bb-302">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="508bb-302">**Parameters**</span></span>  

<span data-ttu-id="508bb-303">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="508bb-303">*pDevice* \[in\]</span></span>  

<span data-ttu-id="508bb-304">El dispositivo productor que pone en cola las superficies en la cola de la superficie.</span><span class="sxs-lookup"><span data-stu-id="508bb-304">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="508bb-305">*ppProducer* \[ out \] devuelve un objeto a la interfaz del productor.</span><span class="sxs-lookup"><span data-stu-id="508bb-305">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="508bb-306">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="508bb-306">**Return Values**</span></span>

<span data-ttu-id="508bb-307">Si el dispositivo no es capaz de compartir superficies, devuelve un \_ error de DXGI \_ llamada no válida \_ .</span><span class="sxs-lookup"><span data-stu-id="508bb-307">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="508bb-308">**Apertura de un consumidor**</span><span class="sxs-lookup"><span data-stu-id="508bb-308">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="508bb-309">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="508bb-309">**Parameters**</span></span>  
 <span data-ttu-id="508bb-310">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="508bb-310">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="508bb-311">El dispositivo de consumidor que quita las superficies de la cola de Surface.</span><span class="sxs-lookup"><span data-stu-id="508bb-311">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="508bb-312">*ppConsumer* \[ out \]  devuelve un objeto a la interfaz del consumidor.</span><span class="sxs-lookup"><span data-stu-id="508bb-312">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="508bb-313">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="508bb-313">**Return Values**</span></span>

<span data-ttu-id="508bb-314">Si el dispositivo no es capaz de compartir superficies, devuelve un \_ error de DXGI \_ llamada no válida \_ .</span><span class="sxs-lookup"><span data-stu-id="508bb-314">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="508bb-315">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="508bb-315">**Remarks**</span></span>

<span data-ttu-id="508bb-316">Esta función abre todas las superficies en la cola del dispositivo de entrada y las almacena en caché.</span><span class="sxs-lookup"><span data-stu-id="508bb-316">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="508bb-317">Las llamadas subsiguientes a dequeue simplemente Irán a la memoria caché y no tendrán que volver a abrir las superficies cada vez.</span><span class="sxs-lookup"><span data-stu-id="508bb-317">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="508bb-318">Clonar un IDXGIXSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="508bb-318">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="508bb-319">**Los miembros** **MetaDataSize** y **Flags** tienen el mismo comportamiento que para CreateSurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="508bb-319">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="508bb-320">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="508bb-320">**Parameters**</span></span>

<span data-ttu-id="508bb-321">*pDesc* \[ en \] una estructura que proporciona una descripción del objeto clonado que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="508bb-321">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="508bb-322">Este parámetro debe inicializarse.</span><span class="sxs-lookup"><span data-stu-id="508bb-322">This parameter should be initialized.</span></span>  
<span data-ttu-id="508bb-323">*ppQueue* \[ out \] devuelve el objeto inicializado.</span><span class="sxs-lookup"><span data-stu-id="508bb-323">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="508bb-324">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="508bb-324">**Remarks**</span></span>

<span data-ttu-id="508bb-325">Puede clonar desde cualquier objeto de cola existente, incluso si no es la raíz.</span><span class="sxs-lookup"><span data-stu-id="508bb-325">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="508bb-326">IDXGIXSurfaceConsumer</span><span class="sxs-lookup"><span data-stu-id="508bb-326">IDXGIXSurfaceConsumer</span></span>

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



<span data-ttu-id="508bb-327">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="508bb-327">**Parameters**</span></span>  
<span data-ttu-id="508bb-328">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="508bb-328">*id* \[in\]</span></span>  
<span data-ttu-id="508bb-329">REFIID de una superficie 2D del dispositivo de consumo.</span><span class="sxs-lookup"><span data-stu-id="508bb-329">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="508bb-330">En el caso de una IDirect3DDevice9, REFIID debe ser \_ \_ Uuidof (IDirect3DTexture9).</span><span class="sxs-lookup"><span data-stu-id="508bb-330">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="508bb-331">En el caso de una ID3D10Device, REFIID debe ser \_ \_ Uuidof (ID3D10Texture2D).</span><span class="sxs-lookup"><span data-stu-id="508bb-331">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="508bb-332">En el caso de una ID3D11Device, REFIID debe ser \_ \_ Uuidof (ID3D11Texture2D).</span><span class="sxs-lookup"><span data-stu-id="508bb-332">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="508bb-333">*ppSurface* \[ out \] devuelve un puntero a la superficie.</span><span class="sxs-lookup"><span data-stu-id="508bb-333">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="508bb-334">*pBuffer* \[ en, \] un parámetro opcional y, si no **es null**, en la devolución, contiene los metadatos que se pasaron en la llamada de enqueue correspondiente.</span><span class="sxs-lookup"><span data-stu-id="508bb-334">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="508bb-335">*pBufferSize* \[ en, fuera \] del tamaño de *pBuffer*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="508bb-335">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="508bb-336">Devuelve el número de bytes devueltos en *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="508bb-336">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="508bb-337">Si la llamada de puesta en cola no proporcionó metadatos, *pBuffer* se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="508bb-337">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="508bb-338">*dwTimeout* \[ en \] especifica un valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="508bb-338">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="508bb-339">Vea los comentarios para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="508bb-339">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="508bb-340">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="508bb-340">**Return Values**</span></span>

<span data-ttu-id="508bb-341">Esta función puede devolver el tiempo \_ de espera si se especifica un valor de tiempo de espera y la función no devuelve antes del valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="508bb-341">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="508bb-342">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="508bb-342">See Remarks.</span></span> <span data-ttu-id="508bb-343">Si no hay superficies disponibles, la función devuelve con *ppSurface* establecido en **null**, *pBufferSize* establecido en 0 y el valor devuelto es 0x80070120 (Win32 \_ a \_ HRESULT ( \_ tiempo de espera de espera)).</span><span class="sxs-lookup"><span data-stu-id="508bb-343">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="508bb-344">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="508bb-344">**Remarks**</span></span>

<span data-ttu-id="508bb-345">Esta API se puede bloquear si la cola está vacía.</span><span class="sxs-lookup"><span data-stu-id="508bb-345">This API can block if the queue is empty.</span></span> <span data-ttu-id="508bb-346">El parámetro *dwTimeout* funciona de forma idéntica a las API de sincronización de Windows, como WaitForSingleObject.</span><span class="sxs-lookup"><span data-stu-id="508bb-346">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="508bb-347">En el caso de un comportamiento sin bloqueo, utilice un tiempo de espera de 0.</span><span class="sxs-lookup"><span data-stu-id="508bb-347">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="508bb-348">ISurfaceProducer</span><span class="sxs-lookup"><span data-stu-id="508bb-348">ISurfaceProducer</span></span>

<span data-ttu-id="508bb-349">Esta interfaz proporciona dos métodos que permiten a la aplicación poner en cola las superficies.</span><span class="sxs-lookup"><span data-stu-id="508bb-349">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="508bb-350">Después de poner en cola una superficie, el puntero de Surface ya no es válido y no es seguro usarlo.</span><span class="sxs-lookup"><span data-stu-id="508bb-350">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="508bb-351">La única acción que debe realizar la aplicación con el puntero es liberarla.</span><span class="sxs-lookup"><span data-stu-id="508bb-351">The only action that the application should perform with the pointer is to release it.</span></span>



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="508bb-352">ISurfaceProducer:: enqueue</span><span class="sxs-lookup"><span data-stu-id="508bb-352">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="508bb-353">Pone en cola una superficie en el objeto de cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-353">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="508bb-354">Una vez finalizada esta llamada, el productor se realiza con la superficie y la superficie está lista para otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="508bb-354">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="508bb-355">ISurfaceProducer:: Flush</span><span class="sxs-lookup"><span data-stu-id="508bb-355">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="508bb-356">Se usa si las aplicaciones deben tener un comportamiento sin bloqueo.</span><span class="sxs-lookup"><span data-stu-id="508bb-356">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="508bb-357">Para obtener información detallada, vea la sección Comentarios de.</span><span class="sxs-lookup"><span data-stu-id="508bb-357">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="508bb-358">**Poner en cola**</span><span class="sxs-lookup"><span data-stu-id="508bb-358">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="508bb-359">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="508bb-359">**Parameters**</span></span>  
<span data-ttu-id="508bb-360">*pSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="508bb-360">*pSurface* \[in\]</span></span>  
<span data-ttu-id="508bb-361">Superficie del dispositivo de producción que se debe poner en cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-361">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="508bb-362">Esta superficie debe ser una superficie quitada de la cola de la misma red de cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-362">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="508bb-363">*pBuffer* \[ en \] un parámetro opcional, que se usa para pasar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="508bb-363">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="508bb-364">Debe apuntar a los datos que se pasarán a la llamada de eliminación de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-364">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="508bb-365">*BufferSize* \[ en \] el tamaño de *pBuffer*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="508bb-365">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="508bb-366">*Marcas* \[ de en \] un parámetro opcional que controla el comportamiento de esta función.</span><span class="sxs-lookup"><span data-stu-id="508bb-366">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="508bb-367">La única marca es SURFACE \_ Queue \_ Flag \_ \_ no \_ espera.</span><span class="sxs-lookup"><span data-stu-id="508bb-367">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="508bb-368">Vea los comentarios para el vaciado.</span><span class="sxs-lookup"><span data-stu-id="508bb-368">See the Remarks for Flush.</span></span> <span data-ttu-id="508bb-369">Si no se pasa ninguna marca (*Flags* = = 0), se utiliza el comportamiento de bloqueo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="508bb-369">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="508bb-370">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="508bb-370">**Return Values**</span></span>

<span data-ttu-id="508bb-371">Esta función puede devolver el \_ error \_ \_ de DXGI todavía se \_ está dibujando si se usa una marca de cola de superficie \_ \_ \_ \_ no \_ esperada.</span><span class="sxs-lookup"><span data-stu-id="508bb-371">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="508bb-372">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="508bb-372">**Remarks**</span></span>

-   <span data-ttu-id="508bb-373">Esta función coloca la superficie en la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-373">This function puts the surface on the queue.</span></span> <span data-ttu-id="508bb-374">Si la aplicación no especifica que la \_ marca de la cola de Surface no \_ \_ \_ \_ espere, esta función está bloqueando y realizará una sincronización de CPU de GPU para asegurarse de que toda la representación en la superficie en cola está completa.</span><span class="sxs-lookup"><span data-stu-id="508bb-374">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="508bb-375">Si esta función se ejecuta correctamente, habrá una superficie disponible para quitar de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-375">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="508bb-376">Si desea un comportamiento sin bloqueo, use la marca no \_ \_ esperar.</span><span class="sxs-lookup"><span data-stu-id="508bb-376">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="508bb-377">Vea Flush () para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="508bb-377">See Flush() for details.</span></span>
-   <span data-ttu-id="508bb-378">Según las reglas de recuento de referencias COM, la superficie devuelta por dequeue será AddRef (), por lo que la aplicación no necesita hacer esto.</span><span class="sxs-lookup"><span data-stu-id="508bb-378">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="508bb-379">Después de llamar a enqueue, la aplicación debe liberar la superficie porque ya no la está usando.</span><span class="sxs-lookup"><span data-stu-id="508bb-379">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="508bb-380">**Vaciar**</span><span class="sxs-lookup"><span data-stu-id="508bb-380">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="508bb-381">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="508bb-381">**Parameters**</span></span>  
<span data-ttu-id="508bb-382">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="508bb-382">*Flags* \[in\]</span></span>  
<span data-ttu-id="508bb-383">La única marca es SURFACE \_ Queue \_ Flag \_ \_ no \_ espera.</span><span class="sxs-lookup"><span data-stu-id="508bb-383">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="508bb-384">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="508bb-384">See Remarks.</span></span> <span data-ttu-id="508bb-385">*nSurfaces* \[ out \] devuelve el número de superficies que todavía están pendientes y no se han vaciado.</span><span class="sxs-lookup"><span data-stu-id="508bb-385">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="508bb-386">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="508bb-386">**Return Values**</span></span>

<span data-ttu-id="508bb-387">Esta función puede devolver \_ el error \_ \_ de DXGI todavía se \_ está dibujando si se usa la marca de la cola de Surface \_ \_ \_ \_ no \_ esperada.</span><span class="sxs-lookup"><span data-stu-id="508bb-387">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="508bb-388">Esta función devuelve S \_ OK si alguna superficie se vació correctamente.</span><span class="sxs-lookup"><span data-stu-id="508bb-388">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="508bb-389">Esta función devuelve el \_ error de DXGI \_ todavía se está \_ \_ dibujando si no se ha vaciado ninguna superficie.</span><span class="sxs-lookup"><span data-stu-id="508bb-389">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="508bb-390">Juntos, el valor devuelto y *nSurfaces* indican a la aplicación qué trabajo se ha realizado y si queda algún trabajo.</span><span class="sxs-lookup"><span data-stu-id="508bb-390">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="508bb-391">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="508bb-391">**Remarks**</span></span>

<span data-ttu-id="508bb-392">El vaciado solo es significativo si la llamada anterior a enqueue usó la \_ \_ marca no wait; de lo contrario, será una operación no operativa.</span><span class="sxs-lookup"><span data-stu-id="508bb-392">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="508bb-393">Si la llamada a enqueue usó la \_ \_ marca no wait, enqueue se devuelve inmediatamente y no se garantiza la sincronización de la CPU de GPU.</span><span class="sxs-lookup"><span data-stu-id="508bb-393">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="508bb-394">La superficie se considera todavía en cola, el dispositivo productor no puede seguir utilizándola, pero no está disponible para quitar de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-394">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="508bb-395">Para intentar confirmar la superficie de la eliminación de la cola, se debe llamar a Flush.</span><span class="sxs-lookup"><span data-stu-id="508bb-395">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="508bb-396">Vaciar intenta confirmar todas las superficies que están actualmente en cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-396">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="508bb-397">Si no se pasa ninguna marca al vaciado, se bloqueará y se borrará toda la cola, y se prepararán todas las superficies en ella para quitar de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-397">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="508bb-398">Si \_ \_ se usa la marca no esperar, la cola comprobará las superficies para ver si alguna de ellas está lista; este paso no se bloquea.</span><span class="sxs-lookup"><span data-stu-id="508bb-398">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="508bb-399">Las superficies que han terminado la GPU: la sincronización de CPU estará lista para el dispositivo de consumidor.</span><span class="sxs-lookup"><span data-stu-id="508bb-399">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="508bb-400">Las superficies que siguen pendientes no se verán afectadas.</span><span class="sxs-lookup"><span data-stu-id="508bb-400">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="508bb-401">La función devuelve el número de superficies que todavía es necesario vaciar.</span><span class="sxs-lookup"><span data-stu-id="508bb-401">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="508bb-402">El vaciado no interrumpirá la semántica de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-402">Flush will not break the queue semantics.</span></span> <span data-ttu-id="508bb-403">La API garantiza que las superficies que se ponen en cola en primer lugar se confirmarán antes de que las superficies se ponen en cola más adelante, independientemente de Cuándo se produzca la sincronización de CPU-GPU.</span><span class="sxs-lookup"><span data-stu-id="508bb-403">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="508bb-404">Aplicación auxiliar de Direct3D 9Ex y DXGI Interop: Cómo usar</span><span class="sxs-lookup"><span data-stu-id="508bb-404">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="508bb-405">Esperamos que la mayoría de los casos de uso impliquen dos dispositivos que compartan varias superficies.</span><span class="sxs-lookup"><span data-stu-id="508bb-405">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="508bb-406">Dado que este también es el escenario más sencillo, en este documento se detalla cómo usar las API para lograr este objetivo, se describe una variación de no bloqueo y finaliza con una breve sección sobre la inicialización de tres dispositivos.</span><span class="sxs-lookup"><span data-stu-id="508bb-406">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="508bb-407">Dos dispositivos</span><span class="sxs-lookup"><span data-stu-id="508bb-407">Two Devices</span></span>

<span data-ttu-id="508bb-408">La aplicación de ejemplo que usa este ayudante puede usar Direct3D 9Ex y Direct3D 11 juntos.</span><span class="sxs-lookup"><span data-stu-id="508bb-408">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="508bb-409">La aplicación puede procesar el contenido con ambos dispositivos y presentar contenido mediante Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="508bb-409">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="508bb-410">El procesamiento podría significar la representación de contenido, la descodificación de vídeo, la ejecución de sombreadores de cálculo, etc.</span><span class="sxs-lookup"><span data-stu-id="508bb-410">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="508bb-411">En cada fotograma, la aplicación se procesará primero con Direct3D 11, después se procesará con Direct3D 9 y, por último, con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="508bb-411">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="508bb-412">Además, el procesamiento con Direct3D 11 generará algunos metadatos que debe consumir Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="508bb-412">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="508bb-413">En esta sección se trata el uso de la aplicación auxiliar en tres partes que corresponden a esta secuencia: inicialización, bucle principal y limpieza.</span><span class="sxs-lookup"><span data-stu-id="508bb-413">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="508bb-414">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="508bb-414">**Initialization**</span></span>  
<span data-ttu-id="508bb-415">La inicialización consta de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="508bb-415">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="508bb-416">Inicialice ambos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="508bb-416">Initialize both devices.</span></span>
2.  <span data-ttu-id="508bb-417">Cree la cola raíz: m \_ 11to9Queue.</span><span class="sxs-lookup"><span data-stu-id="508bb-417">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="508bb-418">Clone desde la cola raíz: m \_ 9to11Queue.</span><span class="sxs-lookup"><span data-stu-id="508bb-418">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="508bb-419">Llame a OpenProducer/OpenConsumer en ambas colas.</span><span class="sxs-lookup"><span data-stu-id="508bb-419">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="508bb-420">Los nombres de cola usan los números 9 y 11 para indicar qué API es el productor y cuál es el consumidor: \*\*m \_ ***productor*** a cola de \*\*\*consumidores\*\*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="508bb-420">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_\*\*\*producer**\* to ***consumer*** Queue\*\*.</span></span> <span data-ttu-id="508bb-421">En consecuencia, m \_ 11to9Queue indica una cola para la que el dispositivo Direct3D 11 genera superficies que el dispositivo de Direct3D 9 consume.</span><span class="sxs-lookup"><span data-stu-id="508bb-421">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="508bb-422">Del mismo modo, m \_ 9to11Queue indica una cola para la que Direct3D 9 produce superficies que usa Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="508bb-422">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="508bb-423">La cola raíz está inicialmente llena y todas las colas clonadas están inicialmente vacías.</span><span class="sxs-lookup"><span data-stu-id="508bb-423">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="508bb-424">Esto no debería ser un problema para la aplicación, salvo el primer ciclo de las colas y las decolas y la disponibilidad de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="508bb-424">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="508bb-425">Si una eliminación de cola solicita metadatos, pero no se estableció ninguno (ya sea porque no hay nada inicialmente o la puesta en cola no estableció nada), la eliminación de la cola observa que no se recibieron metadatos.</span><span class="sxs-lookup"><span data-stu-id="508bb-425">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="508bb-426">**Inicialice ambos dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="508bb-426">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="508bb-427">**Cree la cola raíz.**</span><span class="sxs-lookup"><span data-stu-id="508bb-427">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="508bb-428">En este paso también se crean las superficies.</span><span class="sxs-lookup"><span data-stu-id="508bb-428">This step also creates the surfaces.</span></span> <span data-ttu-id="508bb-429">Las restricciones de tamaño y formato son idénticas a la creación de cualquier recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="508bb-429">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="508bb-430">El tamaño del búfer de metadatos se fija en el momento de la creación y, en este caso, solo pasaremos un UINT.</span><span class="sxs-lookup"><span data-stu-id="508bb-430">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="508bb-431">La cola se debe crear con un número fijo de superficies.</span><span class="sxs-lookup"><span data-stu-id="508bb-431">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="508bb-432">El rendimiento variará en función del escenario.</span><span class="sxs-lookup"><span data-stu-id="508bb-432">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="508bb-433">Tener varias superficies aumenta la probabilidad de que los dispositivos estén ocupados.</span><span class="sxs-lookup"><span data-stu-id="508bb-433">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="508bb-434">Por ejemplo, si solo hay una superficie, no habrá ninguna paralelización entre los dos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="508bb-434">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="508bb-435">Por otro lado, el aumento del número de superficies aumenta la superficie de memoria, lo que puede reducir el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="508bb-435">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="508bb-436">En este ejemplo se usan dos superficies.</span><span class="sxs-lookup"><span data-stu-id="508bb-436">This example uses two surfaces.</span></span>  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  <span data-ttu-id="508bb-437">**Clone la cola raíz.**</span><span class="sxs-lookup"><span data-stu-id="508bb-437">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="508bb-438">Cada cola clonada debe usar las mismas superficies pero puede tener distintos tamaños de búfer de metadatos y marcas diferentes.</span><span class="sxs-lookup"><span data-stu-id="508bb-438">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="508bb-439">En este caso, no hay metadatos de Direct3D 9 a Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="508bb-439">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="508bb-440">**Abra el productor y los dispositivos de consumidor.**</span><span class="sxs-lookup"><span data-stu-id="508bb-440">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="508bb-441">La aplicación debe realizar este paso antes de llamar a poner en cola y quitar de la cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-441">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="508bb-442">Al abrir un productor y un consumidor, se devuelven interfaces que contienen las API enqueue y dequeue.</span><span class="sxs-lookup"><span data-stu-id="508bb-442">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="508bb-443">**Bucle principal**</span><span class="sxs-lookup"><span data-stu-id="508bb-443">**Main Loop**</span></span>  
<span data-ttu-id="508bb-444">El uso de la cola se modela después del problema de productor/consumidor clásico.</span><span class="sxs-lookup"><span data-stu-id="508bb-444">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="508bb-445">Piense en esto desde una perspectiva por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="508bb-445">Think of this from a per-device perspective.</span></span> <span data-ttu-id="508bb-446">Cada dispositivo debe realizar estos pasos: quitar de la cola para obtener una superficie de su cola de consumo, procesar en la superficie y, a continuación, poner en cola en su cola de producción.</span><span class="sxs-lookup"><span data-stu-id="508bb-446">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="508bb-447">En el caso del dispositivo Direct3D 11, el uso de Direct3D 9 es casi idéntico.</span><span class="sxs-lookup"><span data-stu-id="508bb-447">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



<span data-ttu-id="508bb-448">**Limpieza**</span><span class="sxs-lookup"><span data-stu-id="508bb-448">**Cleaning Up**</span></span>  
<span data-ttu-id="508bb-449">Este paso es muy sencillo.</span><span class="sxs-lookup"><span data-stu-id="508bb-449">This step is very straightforward.</span></span> <span data-ttu-id="508bb-450">Además de los pasos normales para limpiar las API de Direct3D, la aplicación debe liberar las interfaces COM devueltas.</span><span class="sxs-lookup"><span data-stu-id="508bb-450">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="508bb-451">Uso sin bloqueo</span><span class="sxs-lookup"><span data-stu-id="508bb-451">Non-Blocking Use</span></span>

<span data-ttu-id="508bb-452">El ejemplo anterior tiene sentido para un caso de uso multiproceso en el que cada dispositivo tiene su propio subproceso.</span><span class="sxs-lookup"><span data-stu-id="508bb-452">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="508bb-453">En el ejemplo se usan las versiones de bloqueo de las API: Infinite para el tiempo de espera y no hay ninguna marca para poner en cola.</span><span class="sxs-lookup"><span data-stu-id="508bb-453">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="508bb-454">Si desea usar el ayudante sin bloqueos, solo tiene que realizar algunos cambios en el proceso.</span><span class="sxs-lookup"><span data-stu-id="508bb-454">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="508bb-455">En esta sección se muestra el uso sin bloqueo con ambos dispositivos en un subproceso.</span><span class="sxs-lookup"><span data-stu-id="508bb-455">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="508bb-456">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="508bb-456">**Initialization**</span></span>  
<span data-ttu-id="508bb-457">La inicialización es idéntica salvo para las marcas.</span><span class="sxs-lookup"><span data-stu-id="508bb-457">Initialization is identical except for the flags.</span></span> <span data-ttu-id="508bb-458">Dado que la aplicación es de un solo subproceso, use esa marca para crearla.</span><span class="sxs-lookup"><span data-stu-id="508bb-458">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="508bb-459">Esto desactiva parte del código de sincronización, lo que puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="508bb-459">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



<span data-ttu-id="508bb-460">La apertura de los dispositivos de productor y consumidor son las mismas que en el ejemplo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="508bb-460">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="508bb-461">**Usar la cola**</span><span class="sxs-lookup"><span data-stu-id="508bb-461">**Using the Queue**</span></span>  
<span data-ttu-id="508bb-462">Hay muchas maneras de usar la cola en un modo de no bloqueo con diversas características de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="508bb-462">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="508bb-463">El siguiente ejemplo es sencillo, pero tiene un rendimiento deficiente debido al giro y el sondeo excesivos.</span><span class="sxs-lookup"><span data-stu-id="508bb-463">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="508bb-464">A pesar de estos problemas, en el ejemplo se muestra cómo usar el ayudante.</span><span class="sxs-lookup"><span data-stu-id="508bb-464">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="508bb-465">El enfoque consiste en permanecer constante en un bucle y quitar de la cola, procesar, poner en cola y vaciar.</span><span class="sxs-lookup"><span data-stu-id="508bb-465">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="508bb-466">Si se produce un error en cualquiera de los pasos porque el recurso no está disponible, la aplicación simplemente vuelve a intentar el siguiente bucle.</span><span class="sxs-lookup"><span data-stu-id="508bb-466">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



<span data-ttu-id="508bb-467">Una solución más compleja podría comprobar el valor devuelto de enqueue y de Flush para determinar si es necesario el vaciado.</span><span class="sxs-lookup"><span data-stu-id="508bb-467">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="508bb-468">Tres dispositivos</span><span class="sxs-lookup"><span data-stu-id="508bb-468">Three Devices</span></span>

<span data-ttu-id="508bb-469">La extensión de los ejemplos anteriores para abarcar varios dispositivos es sencilla.</span><span class="sxs-lookup"><span data-stu-id="508bb-469">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="508bb-470">En el código siguiente se realiza la inicialización.</span><span class="sxs-lookup"><span data-stu-id="508bb-470">The following code performs the initialization.</span></span> <span data-ttu-id="508bb-471">Una vez creados los objetos productor/consumidor, el código para usarlos es el mismo.</span><span class="sxs-lookup"><span data-stu-id="508bb-471">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="508bb-472">Este ejemplo tiene tres dispositivos y, por tanto, tres colas.</span><span class="sxs-lookup"><span data-stu-id="508bb-472">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="508bb-473">Las superficies fluyen de Direct3D 9 a Direct3D 10 a Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="508bb-473">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



<span data-ttu-id="508bb-474">Como se mencionó anteriormente, la clonación funciona de la misma manera, independientemente de la cola que se clona.</span><span class="sxs-lookup"><span data-stu-id="508bb-474">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="508bb-475">Por ejemplo, la segunda llamada de clonación podría haber estado fuera del \_ objeto m 9to10Queue.</span><span class="sxs-lookup"><span data-stu-id="508bb-475">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a><span data-ttu-id="508bb-476">Conclusión</span><span class="sxs-lookup"><span data-stu-id="508bb-476">Conclusion</span></span>

<span data-ttu-id="508bb-477">Puede crear soluciones que usen la interoperabilidad para emplear la eficacia de varias API de DirectX.</span><span class="sxs-lookup"><span data-stu-id="508bb-477">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="508bb-478">La interoperabilidad de la API de gráficos de Windows ahora ofrece un entorno de ejecución de Surface Management en Common 1,1.</span><span class="sxs-lookup"><span data-stu-id="508bb-478">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="508bb-479">Este Runtime habilita la compatibilidad con el uso compartido de superficies sincronizadas dentro de las API recién desarrolladas, como Direct3D 11, Direct3D 10,1 y Direct2D.</span><span class="sxs-lookup"><span data-stu-id="508bb-479">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="508bb-480">Mejoras de interoperabilidad entre nuevas API y API existentes ayuda a la migración de aplicaciones y compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="508bb-480">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="508bb-481">Las API de consumidor de Direct3D 9Ex y DXGI 1,1 pueden interoperar, como se muestra con el mecanismo de sincronización que se proporciona a través del código auxiliar de ejemplo en la galería de código de MSDN.</span><span class="sxs-lookup"><span data-stu-id="508bb-481">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 
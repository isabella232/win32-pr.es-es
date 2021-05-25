---
title: Uso compartido de surface entre las API de gráficos de Windows
description: En este tema se proporciona información técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, como Direct3D 11, Direct2D, DirectWrite, Direct3D 10 y Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1032cb1cf9b16280088f00e79e7e59bb7f1510b1
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343620"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="96b1e-103">Uso compartido de surface entre las API de gráficos de Windows</span><span class="sxs-lookup"><span data-stu-id="96b1e-103">Surface sharing between Windows graphics APIs</span></span>

<span data-ttu-id="96b1e-104">En este tema se proporciona información técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, como Direct3D 11, Direct2D, DirectWrite, Direct3D 10 y Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="96b1e-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="96b1e-105">Si ya tiene conocimientos prácticos de estas API, este documento puede ayudarle a usar varias API para representarse en la misma superficie en una aplicación diseñada para los sistemas operativos Windows 7 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="96b1e-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="96b1e-106">En este tema también se proporcionan instrucciones de procedimientos recomendados y punteros a recursos adicionales.</span><span class="sxs-lookup"><span data-stu-id="96b1e-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="96b1e-107">Para la interoperabilidad de Direct2D y DirectWrite en el entorno de ejecución de DirectX 11.1, puede usar [dispositivos y contextos](/windows/desktop/Direct2D/devices-and-device-contexts) de dispositivo de Direct2D para representar directamente en dispositivos Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="96b1e-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="96b1e-108">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="96b1e-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="96b1e-109">Introducción</span><span class="sxs-lookup"><span data-stu-id="96b1e-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="96b1e-110">Introducción a la interoperabilidad de API</span><span class="sxs-lookup"><span data-stu-id="96b1e-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="96b1e-111">Escenarios de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="96b1e-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="96b1e-112">Uso compartido de dispositivos direct3D 10.1 con Direct2D</span><span class="sxs-lookup"><span data-stu-id="96b1e-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="96b1e-113">Superficies compartidas sincronizadas de DXGI 1.1</span><span class="sxs-lookup"><span data-stu-id="96b1e-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="96b1e-114">Interoperabilidad entre las API basadas en Direct3D 9Ex y DXGI</span><span class="sxs-lookup"><span data-stu-id="96b1e-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="96b1e-115">Conclusión</span><span class="sxs-lookup"><span data-stu-id="96b1e-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="96b1e-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="96b1e-116">Introduction</span></span>

<span data-ttu-id="96b1e-117">En este documento, la interoperabilidad de la API de gráficos de Windows hace referencia al uso compartido de la misma superficie de representación por diferentes API.</span><span class="sxs-lookup"><span data-stu-id="96b1e-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="96b1e-118">Este tipo de interoperabilidad permite a las aplicaciones crear pantallas atractivas aprovechando varias API de gráficos de Windows y facilitar la migración a nuevas tecnologías manteniendo la compatibilidad con las API existentes.</span><span class="sxs-lookup"><span data-stu-id="96b1e-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="96b1e-119">En Windows 7 (y Windows Vista SP2 con El paquete de interoperabilidad de Windows 7, Vista 7IP), las API de representación de gráficos son Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c y anteriores API de Direct3D, así como GDI y GDI+.</span><span class="sxs-lookup"><span data-stu-id="96b1e-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="96b1e-120">Windows Imaging Component (WIC) y DirectWrite son tecnologías relacionadas para el procesamiento de imágenes, y Direct2D realiza la representación de texto.</span><span class="sxs-lookup"><span data-stu-id="96b1e-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="96b1e-121">DirectX Video Acceleration API (DXVA), basada en Direct3D 9c y Direct3D 9Ex, se usa para el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="96b1e-122">A medida que las API de gráficos de Windows evolucionan hacia la base de Direct3D, Microsoft invierte más esfuerzo en garantizar la interoperabilidad entre las API.</span><span class="sxs-lookup"><span data-stu-id="96b1e-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="96b1e-123">Las API de Direct3D recién desarrolladas y las API de nivel superior basadas en las API de Direct3D también proporcionan compatibilidad cuando sea necesario para puentear la compatibilidad con api anteriores.</span><span class="sxs-lookup"><span data-stu-id="96b1e-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="96b1e-124">Para ilustrar, las aplicaciones de Direct2D pueden usar Direct3D 10.1 mediante el uso compartido de un dispositivo Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="96b1e-125">Además, las API de Direct3D 11, Direct2D y Direct3D 10.1 pueden aprovechar las ventajas de Infraestructura de gráficos de DirectX (DXGI) 1.1, que permite superficies compartidas sincronizadas que admiten totalmente la interoperabilidad entre estas API.</span><span class="sxs-lookup"><span data-stu-id="96b1e-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="96b1e-126">Las API basadas en DXGI 1.1 interoperan con GDI y con GDI+ por asociación, obteniendo el contexto de dispositivo GDI de una superficie DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="96b1e-127">Para obtener más información, consulte la documentación de interoperabilidad de DXGI y GDI disponible en MSDN.</span><span class="sxs-lookup"><span data-stu-id="96b1e-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="96b1e-128">El entorno de ejecución de Direct3D 9Ex admite el uso compartido de superficies no sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="96b1e-129">Las aplicaciones de vídeo basadas en DXVA pueden usar el asistente de interoperabilidad direct3D 9Ex y DXGI para la interoperabilidad de DXVA basada en Direct3D 9Ex con Direct3D 11 para el sombreador de proceso, o bien pueden interoperar con Direct2D para controles 2D o representación de texto.</span><span class="sxs-lookup"><span data-stu-id="96b1e-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="96b1e-130">WIC y DirectWrite también interoperan con GDI, Direct2D y, por asociación, con otras API de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="96b1e-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="96b1e-131">Direct3D 10.0, Direct3D 9c y entornos de ejecución anteriores de Direct3D no admiten superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="96b1e-132">Las copias de memoria del sistema se seguirán usando para la interoperabilidad con las API basadas en GDI o DXGI.</span><span class="sxs-lookup"><span data-stu-id="96b1e-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="96b1e-133">Tenga en cuenta que los escenarios de interoperabilidad de este documento hacen referencia a varias API de gráficos que se representa en una superficie de representación compartida, en lugar de a la misma ventana de aplicación.</span><span class="sxs-lookup"><span data-stu-id="96b1e-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="96b1e-134">La sincronización de LAS API independientes que tienen como destino distintas superficies que luego se compone en la misma ventana está fuera del ámbito de este documento.</span><span class="sxs-lookup"><span data-stu-id="96b1e-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="96b1e-135">Introducción a la interoperabilidad de API</span><span class="sxs-lookup"><span data-stu-id="96b1e-135">API Interoperability Overview</span></span>

<span data-ttu-id="96b1e-136">La interoperabilidad del uso compartido de surface de las API de gráficos de Windows se puede describir en términos de escenarios de API a API y la funcionalidad de interoperabilidad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="96b1e-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="96b1e-137">A partir de Windows 7 y a partir de Windows Vista SP2 con 7IP, las nuevas API y los entornos de ejecución asociados incluyen Direct2D y tecnologías relacionadas: Direct3D 11 y DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="96b1e-138">El rendimiento de GDI también se mejoró en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="96b1e-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="96b1e-139">Direct3D 10.1 se introdujo en Windows Vista SP1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="96b1e-140">En el diagrama siguiente se muestra la compatibilidad de interoperabilidad entre las API.</span><span class="sxs-lookup"><span data-stu-id="96b1e-140">The following diagram shows the interoperability support between APIs.</span></span>

![diagrama de compatibilidad de interoperabilidad entre las API de gráficos de Windows](images/surface-sharing-interoperability.png)

<span data-ttu-id="96b1e-142">En este diagrama, las flechas muestran escenarios de interoperabilidad en los que las API conectadas pueden acceder a la misma superficie.</span><span class="sxs-lookup"><span data-stu-id="96b1e-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="96b1e-143">Las flechas azules indican mecanismos de interoperabilidad introducidos en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="96b1e-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="96b1e-144">Las flechas verdes indican compatibilidad de interoperabilidad con nuevas API o mejoras que ayudan a las API más antiguas a interoperar con api más recientes.</span><span class="sxs-lookup"><span data-stu-id="96b1e-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="96b1e-145">Por ejemplo, las flechas verdes representan el uso compartido de dispositivos, la compatibilidad con la superficie compartida sincronizada, el asistente de sincronización de Direct3D 9Ex/DXGI y la obtención de un contexto de dispositivo GDI desde una superficie compatible.</span><span class="sxs-lookup"><span data-stu-id="96b1e-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="96b1e-146">Escenarios de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="96b1e-146">Interoperability Scenarios</span></span>

<span data-ttu-id="96b1e-147">A partir de Windows 7 y Windows Vista 7IP, las ofertas estándar de las API de gráficos de Windows admiten la representación de varias API en la misma superficie DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="96b1e-148">**Direct3D 11, Direct3D 10.1, Direct2D: interoperabilidad entre sí**</span><span class="sxs-lookup"><span data-stu-id="96b1e-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="96b1e-149">Las API de Direct3D 11, Direct3D 10.1 y Direct2D (y sus API relacionadas, como DirectWrite y WIC) pueden interoperar entre sí mediante el uso compartido de dispositivos direct3D 10.1 o superficies compartidas sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="96b1e-150">Uso compartido de dispositivos direct3D 10.1 con Direct2D</span><span class="sxs-lookup"><span data-stu-id="96b1e-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="96b1e-151">El uso compartido de dispositivos entre Direct2D y Direct3D 10.1 permite que una aplicación use ambas API para representar de forma fluida y eficaz en la misma superficie DXGI 1.1, con el mismo objeto de dispositivo Direct3D subyacente.</span><span class="sxs-lookup"><span data-stu-id="96b1e-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="96b1e-152">Direct2D proporciona la capacidad de llamar a las API de Direct2D mediante un dispositivo Direct3D 10.1 existente, aprovechando el hecho de que Direct2D se basa en los entornos de ejecución de Direct3D 10.1 y DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="96b1e-153">Los fragmentos de código siguientes muestran cómo Direct2D obtiene el destino de representación del dispositivo Direct3D 10.1 desde una superficie DXGI 1.1 asociada al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="96b1e-154">El destino de representación del dispositivo Direct3D 10.1 puede ejecutar llamadas de dibujo de Direct2D entre las API BeginDraw y EndDraw.</span><span class="sxs-lookup"><span data-stu-id="96b1e-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


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



<span data-ttu-id="96b1e-155">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="96b1e-155">**Remarks**</span></span>

-   <span data-ttu-id="96b1e-156">El dispositivo Direct3D 10.1 asociado debe admitir el formato BGRA.</span><span class="sxs-lookup"><span data-stu-id="96b1e-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="96b1e-157">Ese dispositivo se creó mediante una llamada a D3D10CreateDevice1 con el parámetro D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="96b1e-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="96b1e-158">El formato BGRA se admite a partir del nivel de característica 9.1 de Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="96b1e-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="96b1e-159">La aplicación no debe crear varios ID2D1RenderTargets que se asocien al mismo dispositivo Direct3D10.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="96b1e-160">Para obtener un rendimiento óptimo, mantenga al menos un recurso en todo momento, como texturas o superficies asociadas al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="96b1e-161">El uso compartido de dispositivos es adecuado para el uso en proceso de un solo subproceso de un dispositivo de representación compartido por las API de representación de Direct3D 10.1 y Direct2D.</span><span class="sxs-lookup"><span data-stu-id="96b1e-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="96b1e-162">Las superficies compartidas sincronizadas permiten el uso multiproceso, en proceso y fuera de proceso de varios dispositivos de representación usados por las API de Direct3D 10.1, Direct2D y Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="96b1e-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="96b1e-163">Otro método de interoperabilidad de Direct3D 10.1 y Direct2D es mediante ID3D1RenderTarget::CreateSharedBitmap, que crea un objeto ID2D1Bitmap a partir de IDXGISurface.</span><span class="sxs-lookup"><span data-stu-id="96b1e-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="96b1e-164">Puede escribir una escena de Direct3D10.1 en el mapa de bits y representarla con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="96b1e-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="96b1e-165">Para obtener más información, [vea ID2D1RenderTarget::CreateSharedBitmap (Método).](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)</span><span class="sxs-lookup"><span data-stu-id="96b1e-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="96b1e-166">Rasterización de software de Direct2D</span><span class="sxs-lookup"><span data-stu-id="96b1e-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="96b1e-167">No se admite el uso compartido de dispositivos con Direct3D 10.1 cuando se usa el representador de software direct2D, por ejemplo, especificando D2D1 RENDER TARGET USAGE FORCE SOFTWARE RENDERING en D2D1 RENDER TARGET USAGE al crear un destino \_ \_ de representación de \_ \_ \_ \_ \_ \_ \_ Direct2D.</span><span class="sxs-lookup"><span data-stu-id="96b1e-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="96b1e-168">Direct2D puede usar el rasterizador de software WARP10 para compartir el dispositivo con Direct3D 10 o Direct3D 11, pero el rendimiento disminuye significativamente.</span><span class="sxs-lookup"><span data-stu-id="96b1e-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="96b1e-169">Superficies compartidas sincronizadas de DXGI 1.1</span><span class="sxs-lookup"><span data-stu-id="96b1e-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="96b1e-170">Las API de Direct3D 11, Direct3D 10.1 y Direct2D usan DXGI 1.1, que proporciona la funcionalidad para sincronizar la lectura y escritura en la misma superficie de memoria de vídeo (DXGISurface1) mediante dos o más dispositivos Direct3D.</span><span class="sxs-lookup"><span data-stu-id="96b1e-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="96b1e-171">Los dispositivos de representación que usan superficies compartidas sincronizadas pueden ser dispositivos Direct3D 10.1 o Direct3D 11, cada uno de los que se ejecutan en el mismo proceso o entre procesos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="96b1e-172">Las aplicaciones pueden usar superficies compartidas sincronizadas para interoperar entre cualquier dispositivo basado en DXGI 1.1, como Direct3D 11 y Direct3D 10.1, o entre Direct3D 11 y Direct2D, mediante la obtención del dispositivo Direct3D 10.1 del objeto de destino de representación de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="96b1e-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="96b1e-173">En las API de Direct3D 10.1 y versiones posteriores, para usar DXGI 1.1, asegúrese de que el dispositivo Direct3D se crea mediante un objeto de adaptador DXGI 1.1, que se enumera a partir del objeto de generador DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="96b1e-174">Llame a CreateDXGIFactory1 para crear el objeto IDXGIFactory1 y EnumAdapters1 para enumerar el objeto IDXGIAdapter1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="96b1e-175">El objeto IDXGIAdapter1 debe pasarse como parte de la llamada D3D10CreateDevice o D3D10CreateDeviceAndSwapChain.</span><span class="sxs-lookup"><span data-stu-id="96b1e-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="96b1e-176">Para obtener más información sobre las API de DXGI 1.1, consulte la Guía [de programación de DXGI.](https://msdn.microsoft.com/library/ee418147(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="96b1e-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="96b1e-177">API</span><span class="sxs-lookup"><span data-stu-id="96b1e-177">APIs</span></span>

<span data-ttu-id="96b1e-178">**RECURSO D3D10 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="96b1e-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="96b1e-179">Al crear el recurso compartido sincronizado, establezca D3D10 \_ RESOURCE \_ MISC SHARED KEYEDMUTEX en LA MARCA \_ \_ MISC RESOURCE DE D3D10. \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="96b1e-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="96b1e-180">**RECURSO D3D10 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="96b1e-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="96b1e-181">Permite sincronizar el recurso creado mediante las API IDXGIKeyedMutex::AcquireSync y ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="96b1e-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="96b1e-182">Las siguientes API de direct3D 10.1 de creación de recursos que toman un parámetro MISC FLAG DE RECURSOS D3D10 se han ampliado para admitir la \_ \_ nueva \_ marca.</span><span class="sxs-lookup"><span data-stu-id="96b1e-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="96b1e-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="96b1e-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="96b1e-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="96b1e-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="96b1e-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="96b1e-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="96b1e-186">ID3D10Device1::CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="96b1e-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="96b1e-187">Si se llama a cualquiera de las funciones enumeradas con la marca MISC SHARED KEYEDMUTEX de D3D10 RESOURCE, se puede consultar la interfaz devuelta para una interfaz \_ \_ \_ IDXGIKeyedMutex, que implementa las API AcquireSync y ReleaseSync para sincronizar el acceso a la \_ superficie.</span><span class="sxs-lookup"><span data-stu-id="96b1e-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="96b1e-188">El dispositivo que crea la superficie y cualquier otro dispositivo que abra la superficie (mediante OpenSharedResource) debe llamar a IDXGIKeyedMutex::AcquireSync antes de cualquier comando de representación en la superficie e IDXGIKeyedMutex::ReleaseSync cuando haya terminado la representación.</span><span class="sxs-lookup"><span data-stu-id="96b1e-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="96b1e-189">Los dispositivos WARP y REF no admiten recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="96b1e-190">Al intentar crear un recurso con esta marca en un dispositivo WARP o REF, el método create devolverá un código de \_ error E OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="96b1e-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="96b1e-191">**IDXGIKEYEDMUTEX (INTERFAZ)**</span><span class="sxs-lookup"><span data-stu-id="96b1e-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="96b1e-192">Una nueva interfaz de DXGI 1.1, IDXGIKeyedMutex, representa una exclusión mutua con clave, que permite el acceso exclusivo a un recurso compartido que usan varios dispositivos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="96b1e-193">Para obtener documentación de referencia sobre esta interfaz y sus dos métodos, AcquireSync y ReleaseSync, vea [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="96b1e-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="96b1e-194">Ejemplo: Uso compartido de superficie sincronizada entre dos dispositivos Direct3D 10.1</span><span class="sxs-lookup"><span data-stu-id="96b1e-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="96b1e-195">En el ejemplo siguiente se muestra cómo compartir una superficie entre dos dispositivos Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="96b1e-196">La superficie compartida sincronizada se crea mediante un dispositivo Direct3D10.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


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



<span data-ttu-id="96b1e-197">El mismo dispositivo Direct3D10.1 puede obtener la superficie compartida sincronizada para la representación mediante una llamada a AcquireSync y, a continuación, liberar la superficie para la representación del otro dispositivo mediante una llamada a ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="96b1e-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="96b1e-198">Cuando no se comparte la superficie compartida sincronizada con cualquier otro dispositivo Direct3D, el creador puede obtener y liberar la superficie compartida sincronizada (para iniciar y finalizar la representación) adquiriendo y liberando con el mismo valor de clave.</span><span class="sxs-lookup"><span data-stu-id="96b1e-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


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



<span data-ttu-id="96b1e-199">El segundo dispositivo Direct3D10.1 puede obtener la superficie compartida sincronizada para la representación mediante una llamada a AcquireSync y, a continuación, liberar la superficie para la representación del primer dispositivo mediante una llamada a ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="96b1e-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="96b1e-200">Tenga en cuenta que el dispositivo 2 puede adquirir la superficie compartida sincronizada con el mismo valor de clave que el especificado en la llamada ReleaseSync por el dispositivo 1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


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



<span data-ttu-id="96b1e-201">Los dispositivos adicionales que comparten la misma superficie pueden turnar la adquisición y liberación de la superficie mediante claves adicionales, como se muestra en las llamadas siguientes.</span><span class="sxs-lookup"><span data-stu-id="96b1e-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


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



<span data-ttu-id="96b1e-202">Tenga en cuenta que una aplicación real siempre podría representarse en una superficie intermedia que luego se copia en la superficie compartida para evitar que un dispositivo esté esperando en otro dispositivo que comparta la superficie.</span><span class="sxs-lookup"><span data-stu-id="96b1e-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="96b1e-203">Uso de superficies compartidas sincronizadas con Direct2D y Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="96b1e-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="96b1e-204">Del mismo modo, para compartir entre las API de Direct3D 11 y Direct3D 10.1, se puede crear una superficie compartida sincronizada desde cualquier dispositivo de API y compartirla con los otros dispositivos de API, dentro o fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="96b1e-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="96b1e-205">Las aplicaciones que usan Direct2D pueden compartir un dispositivo Direct3D 10.1 y usar una superficie compartida sincronizada para interoperar con Direct3D 11 u otros dispositivos Direct3D 10.1, tanto si pertenecen al mismo proceso como a procesos diferentes.</span><span class="sxs-lookup"><span data-stu-id="96b1e-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="96b1e-206">Sin embargo, para las aplicaciones de un solo proceso y subproceso, el uso compartido de dispositivos es el método de interoperabilidad más eficaz y de alto rendimiento entre Direct2D y Direct3D 10 o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="96b1e-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="96b1e-207">Rasterizador de software</span><span class="sxs-lookup"><span data-stu-id="96b1e-207">Software Rasterizer</span></span>

<span data-ttu-id="96b1e-208">Las superficies compartidas sincronizadas no se admiten cuando las aplicaciones usan los rasterizadores de software Direct3D o Direct2D, incluidos el rasterizador de referencia y WARP, en lugar de usar la aceleración de hardware gráfico.</span><span class="sxs-lookup"><span data-stu-id="96b1e-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="96b1e-209">Interoperabilidad entre las API basadas en Direct3D 9Ex y DXGI</span><span class="sxs-lookup"><span data-stu-id="96b1e-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="96b1e-210">Las API de Direct3D 9Ex incluían la noción de uso compartido de superficie para permitir que otras API leyesen desde la superficie compartida.</span><span class="sxs-lookup"><span data-stu-id="96b1e-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="96b1e-211">Para compartir la lectura y escritura en una superficie compartida de Direct3D 9Ex, debe agregar la sincronización manual a la propia aplicación.</span><span class="sxs-lookup"><span data-stu-id="96b1e-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="96b1e-212">Superficies compartidas de Direct3D 9Ex más asistente de sincronización manual</span><span class="sxs-lookup"><span data-stu-id="96b1e-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="96b1e-213">La tarea más fundamental de la interoperabilidad de Direct3D 9Ex y Direct3D 10 o 11 es pasar una sola superficie del primer dispositivo (dispositivo A) al segundo (dispositivo B), de modo que cuando el dispositivo B adquiere un identificador en la superficie, se garantiza que la representación del dispositivo A se ha completado.</span><span class="sxs-lookup"><span data-stu-id="96b1e-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="96b1e-214">Por lo tanto, el dispositivo B puede usar esta superficie sin preocuparse.</span><span class="sxs-lookup"><span data-stu-id="96b1e-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="96b1e-215">Esto es muy similar al problema clásico productor-consumidor y esta discusión modela el problema de esa manera.</span><span class="sxs-lookup"><span data-stu-id="96b1e-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="96b1e-216">El primer dispositivo que usa la superficie y, a continuación, lo vuelve a hacer, es el productor (dispositivo A) y el dispositivo que está esperando inicialmente es el consumidor (dispositivo B).</span><span class="sxs-lookup"><span data-stu-id="96b1e-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="96b1e-217">Cualquier aplicación real es más sofisticada que esta y encadenará varios bloques de creación productor-consumidor para crear la funcionalidad deseada.</span><span class="sxs-lookup"><span data-stu-id="96b1e-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="96b1e-218">Los bloques de creación productor-consumidor se implementan en el asistente mediante una cola de superficies.</span><span class="sxs-lookup"><span data-stu-id="96b1e-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="96b1e-219">El productor coloca las superficies en cola y las quita el consumidor.</span><span class="sxs-lookup"><span data-stu-id="96b1e-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="96b1e-220">El asistente presenta tres interfaces COM: ISurfaceQueue, ISurfaceProducer e ISurfaceConsumer.</span><span class="sxs-lookup"><span data-stu-id="96b1e-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="96b1e-221">High-Level información general del asistente</span><span class="sxs-lookup"><span data-stu-id="96b1e-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="96b1e-222">El objeto ISurfaceQueue es el bloque de creación para usar las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="96b1e-223">Se crea con un dispositivo Direct3D inicializado y una descripción para crear un número fijo de superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="96b1e-224">El objeto queue administra la creación de recursos y la apertura del código.</span><span class="sxs-lookup"><span data-stu-id="96b1e-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="96b1e-225">El número y el tipo de superficies son fijos; Una vez creadas las superficies, la aplicación no puede agregarlas ni quitarlas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="96b1e-226">Cada instancia del objeto ISurfaceQueue proporciona una clase de calle un solo sentido que se puede usar para enviar superficies desde el dispositivo de producción al dispositivo que lo consume.</span><span class="sxs-lookup"><span data-stu-id="96b1e-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="96b1e-227">Se pueden usar varias de estas calles un solo sentido para habilitar escenarios de uso compartido de superficie entre dispositivos de aplicaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="96b1e-228">**Creación/Duración de objetos**</span><span class="sxs-lookup"><span data-stu-id="96b1e-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="96b1e-229">Hay dos maneras de crear el objeto de cola: a través de CreateSurfaceQueue o mediante el método Clone de ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="96b1e-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="96b1e-230">Dado que las interfaces son objetos COM, se aplica la administración de la duración COM estándar.</span><span class="sxs-lookup"><span data-stu-id="96b1e-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="96b1e-231">**Modelo productor/consumidor**</span><span class="sxs-lookup"><span data-stu-id="96b1e-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="96b1e-232">Poner en cola (): el productor llama a esta función para indicar que se ha hecho con la superficie, que ahora puede estar disponible para otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="96b1e-233">Al volver de esta función, el dispositivo productor ya no tiene derechos sobre la superficie y no es seguro seguir usando esta función.</span><span class="sxs-lookup"><span data-stu-id="96b1e-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="96b1e-234">Quitar la cola (): el dispositivo de consumo llama a esta función para obtener una superficie compartida.</span><span class="sxs-lookup"><span data-stu-id="96b1e-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="96b1e-235">La API garantiza que las superficies quitadas de la cola están listas para usarse.</span><span class="sxs-lookup"><span data-stu-id="96b1e-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="96b1e-236">**Metadatos**</span><span class="sxs-lookup"><span data-stu-id="96b1e-236">**Metadata**</span></span>  
<span data-ttu-id="96b1e-237">La API admite la asociación de metadatos a las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="96b1e-238">Enqueue() tiene la opción de especificar metadatos adicionales que se pasarán al dispositivo que lo consume.</span><span class="sxs-lookup"><span data-stu-id="96b1e-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="96b1e-239">Los metadatos deben ser menores que un máximo conocido en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="96b1e-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="96b1e-240">Dequeue() puede pasar opcionalmente un búfer y un puntero al tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="96b1e-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="96b1e-241">La cola rellena el búfer con los metadatos de la llamada a Enqueue correspondiente.</span><span class="sxs-lookup"><span data-stu-id="96b1e-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="96b1e-242">**Clonación**</span><span class="sxs-lookup"><span data-stu-id="96b1e-242">**Cloning**</span></span>  
<span data-ttu-id="96b1e-243">Cada objeto ISurfaceQueue resuelve una sincronización un sentido.</span><span class="sxs-lookup"><span data-stu-id="96b1e-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="96b1e-244">Se supone que la gran mayoría de las aplicaciones que usan esta API usarán un sistema cerrado.</span><span class="sxs-lookup"><span data-stu-id="96b1e-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="96b1e-245">El sistema cerrado más sencillo con dos dispositivos que envían superficies de un lado a otro requiere dos colas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="96b1e-246">El objeto ISurfaceQueue tiene un método Clone() para que sea posible crear varias colas que forman parte de la misma canalización de mayor tamaño.</span><span class="sxs-lookup"><span data-stu-id="96b1e-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="96b1e-247">Clone crea un nuevo objeto ISurfaceQueue a partir de uno existente y comparte todos los recursos abiertos entre ellos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="96b1e-248">El objeto resultante tiene exactamente las mismas superficies que la cola de origen.</span><span class="sxs-lookup"><span data-stu-id="96b1e-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="96b1e-249">Las colas clonadas pueden tener tamaños de metadatos diferentes entre sí.</span><span class="sxs-lookup"><span data-stu-id="96b1e-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="96b1e-250">**Superficies**</span><span class="sxs-lookup"><span data-stu-id="96b1e-250">**Surfaces**</span></span>  
<span data-ttu-id="96b1e-251">ISurfaceQueue asume la responsabilidad de crear y administrar sus superficies.</span><span class="sxs-lookup"><span data-stu-id="96b1e-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="96b1e-252">No es válido poner en cola superficies arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="96b1e-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="96b1e-253">Además, una superficie solo debe tener un "propietario" activo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="96b1e-254">Debe estar en una cola específica o ser utilizada por un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="96b1e-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="96b1e-255">No es válido tenerla en varias colas o para que los dispositivos sigan usando la superficie después de ponerla en cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="96b1e-256">Detalles de la API</span><span class="sxs-lookup"><span data-stu-id="96b1e-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="96b1e-257">IsurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="96b1e-257">IsurfaceQueue</span></span>

<span data-ttu-id="96b1e-258">La cola es responsable de crear y mantener los recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="96b1e-259">También proporciona la funcionalidad para encadenar varias colas mediante Clonar.</span><span class="sxs-lookup"><span data-stu-id="96b1e-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="96b1e-260">La cola tiene métodos que abren el dispositivo de producción y un dispositivo de consumo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="96b1e-261">Solo se puede abrir una de ellas en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="96b1e-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="96b1e-262">La cola expone las siguientes API:</span><span class="sxs-lookup"><span data-stu-id="96b1e-262">The queue exposes the following APIs:</span></span>



| <span data-ttu-id="96b1e-263">API</span><span class="sxs-lookup"><span data-stu-id="96b1e-263">API</span></span>                            | <span data-ttu-id="96b1e-264">Descripción</span><span class="sxs-lookup"><span data-stu-id="96b1e-264">Description</span></span>                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="96b1e-265">CreateSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="96b1e-265">CreateSurfaceQueue</span></span>          | <span data-ttu-id="96b1e-266">Crea un objeto ISurfaceQueue (la cola "raíz").</span><span class="sxs-lookup"><span data-stu-id="96b1e-266">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="96b1e-267">ISurfaceQueue::OpenConsumer</span><span class="sxs-lookup"><span data-stu-id="96b1e-267">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="96b1e-268">Devuelve una interfaz para que el dispositivo de consumo se descola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-268">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="96b1e-269">ISurfaceQueue::OpenProducer</span><span class="sxs-lookup"><span data-stu-id="96b1e-269">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="96b1e-270">Devuelve una interfaz para que el dispositivo de producción se poner en cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-270">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="96b1e-271">ISurfaceQueue::Clone</span><span class="sxs-lookup"><span data-stu-id="96b1e-271">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="96b1e-272">Crea un objeto ISurfaceQueue que comparte superficies con el objeto de cola raíz.</span><span class="sxs-lookup"><span data-stu-id="96b1e-272">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="96b1e-273">**CreateSurfaceQueue**</span><span class="sxs-lookup"><span data-stu-id="96b1e-273">**CreateSurfaceQueue**</span></span>  


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



<span data-ttu-id="96b1e-274">**Miembros**</span><span class="sxs-lookup"><span data-stu-id="96b1e-274">**Members**</span></span>  

<span data-ttu-id="96b1e-275">**Width**, **Height**  Las dimensiones de las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-275">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="96b1e-276">Todas las superficies compartidas deben tener las mismas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="96b1e-276">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="96b1e-277">**Formato** Formato de las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-277">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="96b1e-278">Todas las superficies compartidas deben tener el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="96b1e-278">All shared surfaces must have the same format.</span></span> <span data-ttu-id="96b1e-279">Los formatos válidos dependen de los dispositivos que se usarán, ya que diferentes pares de dispositivos pueden compartir diferentes tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="96b1e-279">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="96b1e-280">**NumSurfaces**  Número de superficies que forman parte de la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-280">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="96b1e-281">Se trata de un número fijo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-281">This is a fixed number.</span></span>  
 <span data-ttu-id="96b1e-282">**MetaDataSize**  Tamaño máximo del búfer de metadatos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-282">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="96b1e-283">**Marcas**  Marcas para controlar el comportamiento de la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-283">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="96b1e-284">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="96b1e-284">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="96b1e-285">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="96b1e-285">**Parameters**</span></span>

 <span data-ttu-id="96b1e-286">*pDesc* \[ en \]  La descripción de la cola de superficie compartida que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="96b1e-286">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="96b1e-287">*pDevice* \[ en \]  El dispositivo que se debe usar para crear las superficies compartidas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-287">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="96b1e-288">Se trata de un parámetro explícito debido a una característica de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="96b1e-288">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="96b1e-289">Para las superficies compartidas entre Direct3D 9 y Direct3D 10, las superficies deben crearse con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="96b1e-289">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="96b1e-290">*ppQueue* \[ out \]  Al devolver, contiene un puntero al objeto ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="96b1e-290">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="96b1e-291">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="96b1e-291">**Return Values**</span></span>

<span data-ttu-id="96b1e-292">Si *pDevice* no es capaz de compartir recursos, esta función devuelve DXGI \_ ERROR INVALID \_ \_ CALL.</span><span class="sxs-lookup"><span data-stu-id="96b1e-292">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="96b1e-293">Esta función crea los recursos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-293">This function creates the resources.</span></span> <span data-ttu-id="96b1e-294">Si se produce un error, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="96b1e-294">If it fails, it returns an error.</span></span> <span data-ttu-id="96b1e-295">Si se realiza correctamente, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96b1e-295">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="96b1e-296">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="96b1e-296">**Remarks**</span></span>

<span data-ttu-id="96b1e-297">Al crear el objeto de cola también se crean todas las superficies.</span><span class="sxs-lookup"><span data-stu-id="96b1e-297">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="96b1e-298">Se supone que todas las superficies son destinos de representación 2D y se crearán con las marcas DE RECURSOS BIND RENDER TARGET y \_ \_ \_ D3D10 BIND SHADER de D3D10 \_ \_ \_ establecidas (o las marcas equivalentes para los distintos tiempos de ejecución).</span><span class="sxs-lookup"><span data-stu-id="96b1e-298">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="96b1e-299">El desarrollador puede especificar una marca que indica si varios subprocesos accederán a la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-299">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="96b1e-300">Si no se establece ninguna marca ( Flags == 0), varios **subprocesos** usarán la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-300">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="96b1e-301">El desarrollador puede especificar el acceso de subproceso único, lo que desactiva el código de sincronización y proporciona una mejora del rendimiento para esos casos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-301">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="96b1e-302">Cada cola clonada tiene su propia marca, por lo que es posible que las distintas colas del sistema tengan controles de sincronización diferentes.</span><span class="sxs-lookup"><span data-stu-id="96b1e-302">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="96b1e-303">**Abrir un productor**</span><span class="sxs-lookup"><span data-stu-id="96b1e-303">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="96b1e-304">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="96b1e-304">**Parameters**</span></span>  

<span data-ttu-id="96b1e-305">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="96b1e-305">*pDevice* \[in\]</span></span>  

<span data-ttu-id="96b1e-306">El dispositivo productor que pone en cola las superficies en la cola de superficie.</span><span class="sxs-lookup"><span data-stu-id="96b1e-306">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="96b1e-307">*ppProducer* \[ out \] Devuelve un objeto a la interfaz de productor.</span><span class="sxs-lookup"><span data-stu-id="96b1e-307">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="96b1e-308">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="96b1e-308">**Return Values**</span></span>

<span data-ttu-id="96b1e-309">Si el dispositivo no es capaz de compartir superficies, devuelve DXGI \_ ERROR \_ INVALID \_ CALL.</span><span class="sxs-lookup"><span data-stu-id="96b1e-309">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="96b1e-310">**Abrir un consumidor**</span><span class="sxs-lookup"><span data-stu-id="96b1e-310">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="96b1e-311">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="96b1e-311">**Parameters**</span></span>  
 <span data-ttu-id="96b1e-312">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="96b1e-312">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="96b1e-313">El dispositivo consumidor que quita las superficies de la cola de superficie.</span><span class="sxs-lookup"><span data-stu-id="96b1e-313">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="96b1e-314">*ppConsumer* \[ out \]  Devuelve un objeto a la interfaz de consumidor.</span><span class="sxs-lookup"><span data-stu-id="96b1e-314">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="96b1e-315">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="96b1e-315">**Return Values**</span></span>

<span data-ttu-id="96b1e-316">Si el dispositivo no es capaz de compartir superficies, devuelve DXGI \_ ERROR \_ INVALID \_ CALL.</span><span class="sxs-lookup"><span data-stu-id="96b1e-316">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="96b1e-317">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="96b1e-317">**Remarks**</span></span>

<span data-ttu-id="96b1e-318">Esta función abre todas las superficies de la cola para el dispositivo de entrada y las almacena en caché.</span><span class="sxs-lookup"><span data-stu-id="96b1e-318">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="96b1e-319">Las llamadas posteriores a Dequeue simplemente irán a la memoria caché y no tendrán que volver a abrir las superficies cada vez.</span><span class="sxs-lookup"><span data-stu-id="96b1e-319">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="96b1e-320">Clonación de IDXGIXSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="96b1e-320">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="96b1e-321">**Los** **miembros MetaDataSize** **y Flags** tienen el mismo comportamiento que para CreateSurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="96b1e-321">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="96b1e-322">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="96b1e-322">**Parameters**</span></span>

<span data-ttu-id="96b1e-323">*pDesc* \[ en \] un struct que proporciona una descripción del objeto Clone que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="96b1e-323">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="96b1e-324">Este parámetro se debe inicializar.</span><span class="sxs-lookup"><span data-stu-id="96b1e-324">This parameter should be initialized.</span></span>  
<span data-ttu-id="96b1e-325">*ppQueue* \[ out \] Devuelve el objeto inicializado.</span><span class="sxs-lookup"><span data-stu-id="96b1e-325">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="96b1e-326">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="96b1e-326">**Remarks**</span></span>

<span data-ttu-id="96b1e-327">Puede clonar desde cualquier objeto de cola existente, incluso si no es la raíz.</span><span class="sxs-lookup"><span data-stu-id="96b1e-327">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="96b1e-328">IDXGIXSurfaceConsumer</span><span class="sxs-lookup"><span data-stu-id="96b1e-328">IDXGIXSurfaceConsumer</span></span>

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



<span data-ttu-id="96b1e-329">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="96b1e-329">**Parameters**</span></span>  
<span data-ttu-id="96b1e-330">*id* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="96b1e-330">*id* \[in\]</span></span>  
<span data-ttu-id="96b1e-331">EL REFIID de una superficie 2D del dispositivo que lo consume.</span><span class="sxs-lookup"><span data-stu-id="96b1e-331">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="96b1e-332">Para un IDirect3DDevice9, el REFIID debe ser \_ \_ uuidof(IDirect3DTexture9).</span><span class="sxs-lookup"><span data-stu-id="96b1e-332">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="96b1e-333">Para un id3D10Device, el REFIID debe ser \_ \_ uuidof(ID3D10Texture2D).</span><span class="sxs-lookup"><span data-stu-id="96b1e-333">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="96b1e-334">Para un id3D11Device, el REFIID debe ser \_ \_ uuidof(ID3D11Texture2D).</span><span class="sxs-lookup"><span data-stu-id="96b1e-334">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="96b1e-335">*ppSurface* \[ out \] Devuelve un puntero a la superficie.</span><span class="sxs-lookup"><span data-stu-id="96b1e-335">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="96b1e-336">*pBuffer* \[ in, out Un parámetro opcional y, si no es NULL, en la devolución, contiene los metadatos que se pasaron en \] la llamada de puesta en cola correspondiente. </span><span class="sxs-lookup"><span data-stu-id="96b1e-336">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="96b1e-337">*pBufferSize* \[ in, out \] El tamaño de *pBuffer*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="96b1e-337">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="96b1e-338">Devuelve el número de bytes devueltos en *pBuffer.*</span><span class="sxs-lookup"><span data-stu-id="96b1e-338">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="96b1e-339">Si la llamada enqueue no proporciona metadatos, *pBuffer* se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="96b1e-339">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="96b1e-340">*dwTimeout* \[ en \] Especifica un valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="96b1e-340">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="96b1e-341">Consulte los comentarios para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="96b1e-341">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="96b1e-342">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="96b1e-342">**Return Values**</span></span>

<span data-ttu-id="96b1e-343">Esta función puede devolver WAIT TIMEOUT si se especifica un valor de tiempo de espera y la \_ función no devuelve antes del valor de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="96b1e-343">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="96b1e-344">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="96b1e-344">See Remarks.</span></span> <span data-ttu-id="96b1e-345">Si no hay ninguna superficie disponible, la función devuelve con *ppSurface* establecido en **NULL,** *pBufferSize* establecido en 0 y el valor devuelto es 0x80070120 (WIN32 \_ TO \_ HRESULT(WAIT \_ TIMEOUT)).</span><span class="sxs-lookup"><span data-stu-id="96b1e-345">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="96b1e-346">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="96b1e-346">**Remarks**</span></span>

<span data-ttu-id="96b1e-347">Esta API puede bloquearse si la cola está vacía.</span><span class="sxs-lookup"><span data-stu-id="96b1e-347">This API can block if the queue is empty.</span></span> <span data-ttu-id="96b1e-348">El *parámetro dwTimeout* funciona de forma idéntica a las API de sincronización de Windows, como WaitForSingleObject.</span><span class="sxs-lookup"><span data-stu-id="96b1e-348">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="96b1e-349">Para el comportamiento de no bloqueo, use un tiempo de espera de 0.</span><span class="sxs-lookup"><span data-stu-id="96b1e-349">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="96b1e-350">ISurfaceProducer</span><span class="sxs-lookup"><span data-stu-id="96b1e-350">ISurfaceProducer</span></span>

<span data-ttu-id="96b1e-351">Esta interfaz proporciona dos métodos que permiten a la aplicación poner en cola superficies.</span><span class="sxs-lookup"><span data-stu-id="96b1e-351">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="96b1e-352">Una vez puesta en cola una superficie, el puntero de superficie ya no es válido y no es seguro de usar.</span><span class="sxs-lookup"><span data-stu-id="96b1e-352">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="96b1e-353">La única acción que la aplicación debe realizar con el puntero es liberarla.</span><span class="sxs-lookup"><span data-stu-id="96b1e-353">The only action that the application should perform with the pointer is to release it.</span></span>



| <span data-ttu-id="96b1e-354">Método</span><span class="sxs-lookup"><span data-stu-id="96b1e-354">Method</span></span>                          | <span data-ttu-id="96b1e-355">Descripción</span><span class="sxs-lookup"><span data-stu-id="96b1e-355">Description</span></span>                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96b1e-356">ISurfaceProducer::Enqueue</span><span class="sxs-lookup"><span data-stu-id="96b1e-356">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="96b1e-357">Pone en cola una superficie al objeto de cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-357">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="96b1e-358">Una vez completada esta llamada, el productor se realiza con la superficie y la superficie está lista para otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-358">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="96b1e-359">ISurfaceProducer::Flush</span><span class="sxs-lookup"><span data-stu-id="96b1e-359">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="96b1e-360">Se usa si las aplicaciones deben tener un comportamiento sin bloqueo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-360">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="96b1e-361">Para obtener información detallada, vea la sección Comentarios de.</span><span class="sxs-lookup"><span data-stu-id="96b1e-361">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="96b1e-362">**Poner en cola**</span><span class="sxs-lookup"><span data-stu-id="96b1e-362">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="96b1e-363">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="96b1e-363">**Parameters**</span></span>  
<span data-ttu-id="96b1e-364">*pSurface* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="96b1e-364">*pSurface* \[in\]</span></span>  
<span data-ttu-id="96b1e-365">Superficie del dispositivo de producción que se debe poner en cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-365">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="96b1e-366">Esta superficie debe ser una superficie quitada de la cola de la misma red de cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-366">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="96b1e-367">*pBuffer* \[ en \] Un parámetro opcional, que se usa para pasar metadatos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-367">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="96b1e-368">Debe apuntar a los datos que se pasarán a la llamada de eliminación de cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-368">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="96b1e-369">*BufferSize* \[ en \] El tamaño de *pBuffer*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="96b1e-369">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="96b1e-370">*Marcas* \[ en \] Un parámetro opcional que controla el comportamiento de esta función.</span><span class="sxs-lookup"><span data-stu-id="96b1e-370">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="96b1e-371">La única marca es SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="96b1e-371">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="96b1e-372">Vea comentarios para Flush.</span><span class="sxs-lookup"><span data-stu-id="96b1e-372">See the Remarks for Flush.</span></span> <span data-ttu-id="96b1e-373">Si no se pasa ninguna marca (*Flags* == 0), se usa el comportamiento de bloqueo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="96b1e-373">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="96b1e-374">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="96b1e-374">**Return Values**</span></span>

<span data-ttu-id="96b1e-375">Esta función puede devolver DXGI ERROR WAS STILL DRAWING si se usa una marca \_ SURFACE QUEUE FLAG DO \_ NOT \_ \_ \_ \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="96b1e-375">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="96b1e-376">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="96b1e-376">**Remarks**</span></span>

-   <span data-ttu-id="96b1e-377">Esta función coloca la superficie en la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-377">This function puts the surface on the queue.</span></span> <span data-ttu-id="96b1e-378">Si la aplicación no especifica SURFACE QUEUE FLAG DO NOT WAIT, esta función está bloqueando y realizará una sincronización de \_ \_ \_ \_ GPU-CPU para asegurarse de que toda la representación en la superficie puesta en cola está \_ completa.</span><span class="sxs-lookup"><span data-stu-id="96b1e-378">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="96b1e-379">Si esta función se realiza correctamente, habrá una superficie disponible para la eliminación de la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-379">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="96b1e-380">Si desea un comportamiento sin bloqueo, use la marca \_ NO \_ ESPERAR.</span><span class="sxs-lookup"><span data-stu-id="96b1e-380">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="96b1e-381">Consulte Flush() para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="96b1e-381">See Flush() for details.</span></span>
-   <span data-ttu-id="96b1e-382">Según las reglas de recuento de referencias COM, la superficie devuelta por Dequeue será AddRef(), por lo que la aplicación no necesita hacerlo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-382">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="96b1e-383">Después de llamar a Enqueue, la aplicación debe liberar la superficie porque ya no la usa.</span><span class="sxs-lookup"><span data-stu-id="96b1e-383">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="96b1e-384">**Vaciar**</span><span class="sxs-lookup"><span data-stu-id="96b1e-384">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="96b1e-385">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="96b1e-385">**Parameters**</span></span>  
<span data-ttu-id="96b1e-386">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="96b1e-386">*Flags* \[in\]</span></span>  
<span data-ttu-id="96b1e-387">La única marca es SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="96b1e-387">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="96b1e-388">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="96b1e-388">See Remarks.</span></span> <span data-ttu-id="96b1e-389">*nSurfaces* \[ out \] Devuelve el número de superficies que todavía están pendientes y no vacías.</span><span class="sxs-lookup"><span data-stu-id="96b1e-389">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="96b1e-390">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="96b1e-390">**Return Values**</span></span>

<span data-ttu-id="96b1e-391">Esta función puede devolver DXGI ERROR WAS STILL DRAWING si se usa la marca \_ SURFACE QUEUE FLAG DO \_ NOT \_ \_ \_ \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="96b1e-391">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="96b1e-392">Esta función devuelve S \_ OK si alguna superficie se ha vaciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="96b1e-392">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="96b1e-393">Esta función devuelve DXGI \_ ERROR WAS STILL DRAWING solo si no se ha vaciado ninguna \_ \_ \_ superficie.</span><span class="sxs-lookup"><span data-stu-id="96b1e-393">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="96b1e-394">Juntos, el valor devuelto y *nSurfaces* indican a la aplicación qué trabajo se ha realizado y si queda algún trabajo por hacer.</span><span class="sxs-lookup"><span data-stu-id="96b1e-394">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="96b1e-395">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="96b1e-395">**Remarks**</span></span>

<span data-ttu-id="96b1e-396">El vaciado solo es significativo si la llamada anterior a enqueue usó la marca DO NOT WAIT; de \_ \_ lo contrario, será una operación no op.</span><span class="sxs-lookup"><span data-stu-id="96b1e-396">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="96b1e-397">Si la llamada a enqueue usa la marca DO NOT WAIT, la puesta en cola se devuelve inmediatamente y no se garantiza la sincronización \_ \_ de GPU-CPU.</span><span class="sxs-lookup"><span data-stu-id="96b1e-397">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="96b1e-398">La superficie todavía se considera en cola, el dispositivo que produce no puede seguir usándose, pero no está disponible para la eliminación de la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-398">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="96b1e-399">Para intentar confirmar la superficie para la eliminación de la cola, se debe llamar a Flush.</span><span class="sxs-lookup"><span data-stu-id="96b1e-399">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="96b1e-400">El vaciado intenta confirmar todas las superficies que están actualmente en cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-400">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="96b1e-401">Si no se pasa ninguna marca a Flush, se bloqueará y borrará toda la cola y se prepararán todas las superficies de ella para su eliminación de la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-401">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="96b1e-402">Si se usa la marca NO ESPERAR, la cola comprobará las superficies para ver si alguna de ellas está lista; este paso no \_ \_ es de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-402">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="96b1e-403">Las superficies que han finalizado la sincronización de GPU-CPU estarán listas para el dispositivo consumidor.</span><span class="sxs-lookup"><span data-stu-id="96b1e-403">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="96b1e-404">Las superficies que aún están pendientes no se verán afectadas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-404">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="96b1e-405">La función devuelve el número de superficies que todavía deben vaciarse.</span><span class="sxs-lookup"><span data-stu-id="96b1e-405">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="96b1e-406">El vaciado no interrumpirá la semántica de la cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-406">Flush will not break the queue semantics.</span></span> <span data-ttu-id="96b1e-407">La API garantiza que las superficies puestas en cola primero se confirman antes de que las superficies se pondrán en cola más adelante, independientemente de cuándo se produce la sincronización de GPU-CPU.</span><span class="sxs-lookup"><span data-stu-id="96b1e-407">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="96b1e-408">Asistente de interoperabilidad de Direct3D 9Ex y DXGI: Cómo usar</span><span class="sxs-lookup"><span data-stu-id="96b1e-408">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="96b1e-409">Esperamos que la mayoría de los casos de uso impliquen dos dispositivos que comparten una serie de superficies.</span><span class="sxs-lookup"><span data-stu-id="96b1e-409">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="96b1e-410">Dado que este también es el escenario más sencillo, en este documento se detalla cómo usar las API para lograr este objetivo, se describe una variación sin bloqueo y finaliza con una breve sección sobre la inicialización de tres dispositivos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-410">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="96b1e-411">Dos dispositivos</span><span class="sxs-lookup"><span data-stu-id="96b1e-411">Two Devices</span></span>

<span data-ttu-id="96b1e-412">La aplicación de ejemplo que usa este asistente puede usar Direct3D 9Ex y Direct3D 11 juntos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-412">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="96b1e-413">La aplicación puede procesar contenido con ambos dispositivos y presentar contenido mediante Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="96b1e-413">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="96b1e-414">El procesamiento podría significar la representación de contenido, la decodificación de vídeo, la ejecución de sombreadores de proceso, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="96b1e-414">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="96b1e-415">Para cada fotograma, la aplicación se procesará primero con Direct3D 11, luego con Direct3D 9 y, finalmente, se presentará con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="96b1e-415">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="96b1e-416">Además, el procesamiento con Direct3D 11 producirá algunos metadatos que direct3D 9 presente tendrá que consumir.</span><span class="sxs-lookup"><span data-stu-id="96b1e-416">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="96b1e-417">En esta sección se trata el uso del asistente en tres partes que corresponden a esta secuencia: Inicialización, Bucle principal y Limpieza.</span><span class="sxs-lookup"><span data-stu-id="96b1e-417">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="96b1e-418">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="96b1e-418">**Initialization**</span></span>  
<span data-ttu-id="96b1e-419">La inicialización implica los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="96b1e-419">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="96b1e-420">Inicialice ambos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-420">Initialize both devices.</span></span>
2.  <span data-ttu-id="96b1e-421">Cree la cola raíz: m \_ 11to9Queue.</span><span class="sxs-lookup"><span data-stu-id="96b1e-421">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="96b1e-422">Clone desde la cola raíz: m \_ 9to11Queue.</span><span class="sxs-lookup"><span data-stu-id="96b1e-422">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="96b1e-423">Llame a OpenProducer/OpenConsumer en ambas colas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-423">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="96b1e-424">Los nombres de cola usan los números 9 y 11 para indicar qué API es el productor y cuál es el consumidor: **m \_**_producer_*_to_*_consumer_*_Queue_*.</span><span class="sxs-lookup"><span data-stu-id="96b1e-424">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_**_producer_*_to_*_consumer_*_Queue_*.</span></span> <span data-ttu-id="96b1e-425">En consecuencia, m 11to9Queue indica una cola para la que el dispositivo Direct3D 11 genera superficies que el dispositivo \_ Direct3D 9 consume.</span><span class="sxs-lookup"><span data-stu-id="96b1e-425">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="96b1e-426">De forma similar, m 9to11Queue indica una cola para la que \_ Direct3D 9 genera superficies que consume Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="96b1e-426">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="96b1e-427">La cola raíz está inicialmente llena y todas las colas clonadas están inicialmente vacías.</span><span class="sxs-lookup"><span data-stu-id="96b1e-427">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="96b1e-428">Esto no debería ser un problema para la aplicación, excepto para el primer ciclo de puestas en cola y eliminaciones de colas y la disponibilidad de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-428">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="96b1e-429">Si una cola solicita metadatos pero no se estableció ninguno (ya sea porque no hay nada inicialmente o la cola no estableció nada), la eliminación de la cola ve que no se ha recibido ningún metadato.</span><span class="sxs-lookup"><span data-stu-id="96b1e-429">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="96b1e-430">**Inicialice ambos dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="96b1e-430">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="96b1e-431">**Cree la cola raíz.**</span><span class="sxs-lookup"><span data-stu-id="96b1e-431">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="96b1e-432">Este paso también crea las superficies.</span><span class="sxs-lookup"><span data-stu-id="96b1e-432">This step also creates the surfaces.</span></span> <span data-ttu-id="96b1e-433">Las restricciones de tamaño y formato son idénticas a la creación de cualquier recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="96b1e-433">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="96b1e-434">El tamaño del búfer de metadatos se fija en el momento de la creación y, en este caso, solo pasaremos un UINT.</span><span class="sxs-lookup"><span data-stu-id="96b1e-434">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="96b1e-435">La cola debe crearse con un número fijo de superficies.</span><span class="sxs-lookup"><span data-stu-id="96b1e-435">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="96b1e-436">El rendimiento variará en función del escenario.</span><span class="sxs-lookup"><span data-stu-id="96b1e-436">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="96b1e-437">Tener varias superficies aumenta las posibilidades de que los dispositivos estén ocupados.</span><span class="sxs-lookup"><span data-stu-id="96b1e-437">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="96b1e-438">Por ejemplo, si solo hay una superficie, no habrá ninguna paralelización entre los dos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-438">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="96b1e-439">Por otro lado, aumentar el número de superficies aumenta la superficie de memoria, lo que puede degradar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="96b1e-439">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="96b1e-440">En este ejemplo se usan dos superficies.</span><span class="sxs-lookup"><span data-stu-id="96b1e-440">This example uses two surfaces.</span></span>  
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

    

3.  <span data-ttu-id="96b1e-441">**Clone la cola raíz.**</span><span class="sxs-lookup"><span data-stu-id="96b1e-441">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="96b1e-442">Cada cola clonada debe usar las mismas superficies, pero puede tener diferentes tamaños de búfer de metadatos y marcas diferentes.</span><span class="sxs-lookup"><span data-stu-id="96b1e-442">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="96b1e-443">En este caso, no hay metadatos de Direct3D 9 a Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="96b1e-443">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="96b1e-444">**Abra los dispositivos productor y consumidor.**</span><span class="sxs-lookup"><span data-stu-id="96b1e-444">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="96b1e-445">La aplicación debe realizar este paso antes de llamar a Enqueue y Dequeue.</span><span class="sxs-lookup"><span data-stu-id="96b1e-445">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="96b1e-446">Al abrir un productor y un consumidor, se devuelven interfaces que contienen las API de puesta en cola o descola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-446">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="96b1e-447">**Bucle main**</span><span class="sxs-lookup"><span data-stu-id="96b1e-447">**Main Loop**</span></span>  
<span data-ttu-id="96b1e-448">El uso de la cola se modela después del problema clásico entre productor y consumidor.</span><span class="sxs-lookup"><span data-stu-id="96b1e-448">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="96b1e-449">Piense en esto desde la perspectiva de cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-449">Think of this from a per-device perspective.</span></span> <span data-ttu-id="96b1e-450">Cada dispositivo debe realizar estos pasos: quitar la cola para obtener una superficie de su cola de consumo, procesar en la superficie y, a continuación, poner en cola en su cola de producción.</span><span class="sxs-lookup"><span data-stu-id="96b1e-450">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="96b1e-451">Para el dispositivo Direct3D 11, el uso de Direct3D 9 es casi idéntico.</span><span class="sxs-lookup"><span data-stu-id="96b1e-451">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


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



<span data-ttu-id="96b1e-452">**Limpieza**</span><span class="sxs-lookup"><span data-stu-id="96b1e-452">**Cleaning Up**</span></span>  
<span data-ttu-id="96b1e-453">Este paso es muy sencillo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-453">This step is very straightforward.</span></span> <span data-ttu-id="96b1e-454">Además de los pasos normales para limpiar las API de Direct3D, la aplicación debe liberar las interfaces COM de retorno.</span><span class="sxs-lookup"><span data-stu-id="96b1e-454">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="96b1e-455">Uso sin bloqueo</span><span class="sxs-lookup"><span data-stu-id="96b1e-455">Non-Blocking Use</span></span>

<span data-ttu-id="96b1e-456">El ejemplo anterior tiene sentido para un caso de uso multiproceso en el que cada dispositivo tiene su propio subproceso.</span><span class="sxs-lookup"><span data-stu-id="96b1e-456">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="96b1e-457">En el ejemplo se usan las versiones de bloqueo de las API: INFINITE para el tiempo de espera y ninguna marca para poner en cola.</span><span class="sxs-lookup"><span data-stu-id="96b1e-457">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="96b1e-458">Si desea usar el asistente de forma sin bloqueo, solo tiene que realizar algunos cambios.</span><span class="sxs-lookup"><span data-stu-id="96b1e-458">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="96b1e-459">En esta sección se muestra el uso sin bloqueo con ambos dispositivos en un subproceso.</span><span class="sxs-lookup"><span data-stu-id="96b1e-459">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="96b1e-460">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="96b1e-460">**Initialization**</span></span>  
<span data-ttu-id="96b1e-461">La inicialización es idéntica, excepto para las marcas .</span><span class="sxs-lookup"><span data-stu-id="96b1e-461">Initialization is identical except for the flags.</span></span> <span data-ttu-id="96b1e-462">Dado que la aplicación es de un solo subproceso, use esa marca para la creación.</span><span class="sxs-lookup"><span data-stu-id="96b1e-462">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="96b1e-463">Esto desactiva parte del código de sincronización, lo que potencialmente mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="96b1e-463">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


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



<span data-ttu-id="96b1e-464">La apertura de los dispositivos de productor y consumidor es la misma que en el ejemplo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-464">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="96b1e-465">**Uso de la cola**</span><span class="sxs-lookup"><span data-stu-id="96b1e-465">**Using the Queue**</span></span>  
<span data-ttu-id="96b1e-466">Hay muchas maneras de usar la cola de forma sin bloqueo con varias características de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="96b1e-466">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="96b1e-467">El ejemplo siguiente es sencillo, pero tiene un rendimiento deficiente debido a un giro y sondeo excesivos.</span><span class="sxs-lookup"><span data-stu-id="96b1e-467">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="96b1e-468">A pesar de estos problemas, en el ejemplo se muestra cómo usar el asistente.</span><span class="sxs-lookup"><span data-stu-id="96b1e-468">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="96b1e-469">El enfoque es colocarse constantemente en un bucle y quitar la cola, procesar, poner en cola y vaciar.</span><span class="sxs-lookup"><span data-stu-id="96b1e-469">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="96b1e-470">Si alguno de los pasos genera un error porque el recurso no está disponible, la aplicación simplemente intenta de nuevo el bucle siguiente.</span><span class="sxs-lookup"><span data-stu-id="96b1e-470">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


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



<span data-ttu-id="96b1e-471">Una solución más compleja podría comprobar el valor devuelto de puesta en cola y de vaciado para determinar si es necesario vaciar.</span><span class="sxs-lookup"><span data-stu-id="96b1e-471">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="96b1e-472">Tres dispositivos</span><span class="sxs-lookup"><span data-stu-id="96b1e-472">Three Devices</span></span>

<span data-ttu-id="96b1e-473">Extender los ejemplos anteriores para abarcar varios dispositivos es sencillo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-473">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="96b1e-474">El código siguiente realiza la inicialización.</span><span class="sxs-lookup"><span data-stu-id="96b1e-474">The following code performs the initialization.</span></span> <span data-ttu-id="96b1e-475">Una vez creados los objetos Producer/Consumer, el código para usarlos es el mismo.</span><span class="sxs-lookup"><span data-stu-id="96b1e-475">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="96b1e-476">Este ejemplo tiene tres dispositivos y, por tanto, tres colas.</span><span class="sxs-lookup"><span data-stu-id="96b1e-476">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="96b1e-477">Las superficies fluyen de Direct3D 9 a Direct3D 10 a Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="96b1e-477">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


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



<span data-ttu-id="96b1e-478">Como se mencionó anteriormente, la clonación funciona de la misma manera, independientemente de la cola que se clone.</span><span class="sxs-lookup"><span data-stu-id="96b1e-478">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="96b1e-479">Por ejemplo, la segunda llamada a Clone podría haber estado fuera del objeto m \_ 9to10Queue.</span><span class="sxs-lookup"><span data-stu-id="96b1e-479">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


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



## <a name="conclusion"></a><span data-ttu-id="96b1e-480">Conclusión</span><span class="sxs-lookup"><span data-stu-id="96b1e-480">Conclusion</span></span>

<span data-ttu-id="96b1e-481">Puede crear soluciones que usen interoperabilidad para emplear la potencia de varias API de DirectX.</span><span class="sxs-lookup"><span data-stu-id="96b1e-481">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="96b1e-482">La interoperabilidad de la API de gráficos de Windows ahora ofrece un entorno de ejecución de administración de superficie común DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="96b1e-482">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="96b1e-483">Este runtime permite la compatibilidad con el uso compartido de superficies sincronizadas en las API recién desarrolladas, como Direct3D 11, Direct3D 10.1 y Direct2D.</span><span class="sxs-lookup"><span data-stu-id="96b1e-483">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="96b1e-484">Las mejoras de interoperabilidad entre las nuevas API y las API existentes ayudan a la migración de aplicaciones y a la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="96b1e-484">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="96b1e-485">Las API de consumidor de Direct3D 9Ex y DXGI 1.1 pueden interoperar, como se muestra con el mecanismo de sincronización proporcionado a través del código auxiliar de ejemplo en msdn code gallery.</span><span class="sxs-lookup"><span data-stu-id="96b1e-485">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 
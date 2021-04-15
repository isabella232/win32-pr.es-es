---
description: En este tema se describe cómo usar DirectShow para reproducir archivos multimedia que están protegidos con Rights Management digitales (DRM) de Windows Media.
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Leer DRM-Protected archivos ASF en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689686"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a><span data-ttu-id="42d3d-103">Leer DRM-Protected archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="42d3d-103">Reading DRM-Protected ASF Files in DirectShow</span></span>

<span data-ttu-id="42d3d-104">En este tema se describe cómo usar DirectShow para reproducir archivos multimedia que están protegidos con Rights Management digitales (DRM) de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="42d3d-104">This topic describes how to use DirectShow to play media files that are protected with Windows Media Digital Rights Management (DRM).</span></span>

## <a name="drm-concepts"></a><span data-ttu-id="42d3d-105">Conceptos de DRM</span><span class="sxs-lookup"><span data-stu-id="42d3d-105">DRM Concepts</span></span>

<span data-ttu-id="42d3d-106">La protección de un archivo multimedia con DRM de Windows Media implica dos pasos distintos:</span><span class="sxs-lookup"><span data-stu-id="42d3d-106">Protecting a media file with Windows Media DRM involves two distinct steps:</span></span>

-   <span data-ttu-id="42d3d-107">El proveedor de contenido empaqueta el archivo, es decir, cifra el archivo y adjunta la información de licencia al encabezado del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="42d3d-107">The content provider packages the file—that is, encrypts the file and attaches licensing information to the ASF file header.</span></span> <span data-ttu-id="42d3d-108">La información de licencia incluye una dirección URL en la que el cliente puede obtener la licencia.</span><span class="sxs-lookup"><span data-stu-id="42d3d-108">The licensing information includes a URL where the client can obtain the license.</span></span>
-   <span data-ttu-id="42d3d-109">La aplicación cliente adquiere una licencia para el contenido.</span><span class="sxs-lookup"><span data-stu-id="42d3d-109">The client application acquires a license for the content.</span></span>

<span data-ttu-id="42d3d-110">El empaquetado se produce antes de distribuir el archivo.</span><span class="sxs-lookup"><span data-stu-id="42d3d-110">Packaging happens before the file is distributed.</span></span> <span data-ttu-id="42d3d-111">La adquisición de licencias se produce cuando el usuario intenta reproducir o copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="42d3d-111">License acquisition occurs when the user tries to play or copy the file.</span></span> <span data-ttu-id="42d3d-112">La adquisición de licencias puede ser *silenciosa* o *no silenciosa*.</span><span class="sxs-lookup"><span data-stu-id="42d3d-112">License acquisition may be either *silent* or *non-silent*.</span></span> <span data-ttu-id="42d3d-113">La adquisición silenciosa no requiere ninguna interacción con el usuario.</span><span class="sxs-lookup"><span data-stu-id="42d3d-113">Silent acquisition does not require any interaction with the user.</span></span> <span data-ttu-id="42d3d-114">La adquisición no silenciosa requiere que la aplicación abra una ventana del explorador y muestre una página web al usuario.</span><span class="sxs-lookup"><span data-stu-id="42d3d-114">Non-silent acquisition requires the application to open a browser window and display a web page to the user.</span></span> <span data-ttu-id="42d3d-115">En ese momento, es posible que el usuario tenga que proporcionar algún tipo de información al proveedor de contenido.</span><span class="sxs-lookup"><span data-stu-id="42d3d-115">At that point, the user might need to provide some kind of information to the content provider.</span></span> <span data-ttu-id="42d3d-116">Sin embargo, ambos tipos de adquisición de licencias requieren que el cliente envíe una solicitud HTTP a un servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="42d3d-116">However, both types of license acquisition require the client to submit an HTTP request to a license server.</span></span>

### <a name="drm-versions"></a><span data-ttu-id="42d3d-117">Versiones de DRM</span><span class="sxs-lookup"><span data-stu-id="42d3d-117">DRM Versions</span></span>

<span data-ttu-id="42d3d-118">Existen varias versiones de DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="42d3d-118">Several versions of Windows Media DRM exist.</span></span> <span data-ttu-id="42d3d-119">Desde la perspectiva de una aplicación cliente, se pueden agrupar en dos categorías: DRM versión 1 y DRM versión 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="42d3d-119">From the perspective of a client application, they can be grouped into two categories: DRM version 1, and DRM version 7 or later.</span></span> <span data-ttu-id="42d3d-120">(La segunda categoría incluye las versiones de DRM 9 y 10, así como la versión 7). La razón para clasificar las versiones DRM de este modo es que las licencias de la versión 1 se controlan de forma ligeramente diferente que las licencias de la versión 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="42d3d-120">(The second category includes DRM versions 9 and 10, as well as version 7.) The reason for categorizing DRM versions this way is that version 1 licenses are handled somewhat differently than version 7 or later licenses.</span></span> <span data-ttu-id="42d3d-121">En esta documentación, la licencia del término *versión 7* significa la versión 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="42d3d-121">In this documentation, the term *version 7 license* means version 7 or later.</span></span>

<span data-ttu-id="42d3d-122">También es importante distinguir el empaquetado de DRM de la licencia de DRM.</span><span class="sxs-lookup"><span data-stu-id="42d3d-122">It is also important to distinguish the DRM packaging from the DRM license.</span></span> <span data-ttu-id="42d3d-123">Si el archivo está empaquetado con Windows Media Rights Manager versión 7 o posterior, el encabezado DRM puede contener una dirección URL de licencia de la versión 1, además de la dirección URL de la licencia de la versión 7.</span><span class="sxs-lookup"><span data-stu-id="42d3d-123">If the file is packaged using Windows Media Rights Manager version 7 or later, the DRM header can contain a version 1 license URL in addition to the version 7 license URL.</span></span> <span data-ttu-id="42d3d-124">La dirección URL de la licencia de la versión 1 permite a reproductores antiguos que no admiten la versión 7 para obtener una licencia para el contenido.</span><span class="sxs-lookup"><span data-stu-id="42d3d-124">The version 1 license URL enables older players that do not support version 7 to obtain a license for the content.</span></span> <span data-ttu-id="42d3d-125">Sin embargo, el contrario no es cierto, por lo que un archivo con empaquetado de la versión 1 no puede tener una dirección URL de la licencia de la versión 7.</span><span class="sxs-lookup"><span data-stu-id="42d3d-125">However, the converse is not true, so a file with version 1 packaging cannot have a version 7 license URL.</span></span>

### <a name="application-security-level"></a><span data-ttu-id="42d3d-126">Nivel de seguridad de la aplicación</span><span class="sxs-lookup"><span data-stu-id="42d3d-126">Application Security Level</span></span>

<span data-ttu-id="42d3d-127">Para reproducir archivos protegidos con DRM, la aplicación cliente debe estar vinculada a una biblioteca estática que Microsoft proporcione en formato binario.</span><span class="sxs-lookup"><span data-stu-id="42d3d-127">To play DRM-protected files, the client application must be linked to a static library that is provided in binary form by Microsoft.</span></span> <span data-ttu-id="42d3d-128">Esta biblioteca, que identifica de forma única la aplicación, a veces se denomina biblioteca de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="42d3d-128">This library, which uniquely identifies the application, is sometimes called the stub library.</span></span> <span data-ttu-id="42d3d-129">La biblioteca de código auxiliar tiene un nivel de seguridad asignado, cuyo valor viene determinado por el contrato de licencia que firmó al obtener la biblioteca de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="42d3d-129">The stub library has an assigned security level, the value of which is determined by the license agreement that you signed when you obtained the stub library.</span></span>

<span data-ttu-id="42d3d-130">El proveedor de contenido establece un nivel de seguridad mínimo necesario para adquirir la licencia.</span><span class="sxs-lookup"><span data-stu-id="42d3d-130">The content provider sets a minimum security level needed to acquire the license.</span></span> <span data-ttu-id="42d3d-131">Si el nivel de seguridad de la biblioteca de código auxiliar es menor que el nivel de seguridad mínimo que requiere el servidor de licencias, la aplicación no puede obtener la licencia.</span><span class="sxs-lookup"><span data-stu-id="42d3d-131">If the security level of your stub library is less than the minimum security level required by the license server, the application cannot obtain the license.</span></span>

### <a name="individualization"></a><span data-ttu-id="42d3d-132">Individualización</span><span class="sxs-lookup"><span data-stu-id="42d3d-132">Individualization</span></span>

<span data-ttu-id="42d3d-133">Para aumentar la seguridad, una aplicación puede actualizar los componentes de DRM en el equipo del cliente.</span><span class="sxs-lookup"><span data-stu-id="42d3d-133">To increase security, an application may update the DRM components on the client's computer.</span></span> <span data-ttu-id="42d3d-134">Esta actualización, denominada individualización, diferencia la copia del usuario de la aplicación de todas las demás copias de la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="42d3d-134">This update, called individualization, differentiates the user's copy of the application from all other copies of the same application.</span></span> <span data-ttu-id="42d3d-135">El encabezado DRM de un archivo protegido puede especificar un nivel de individualización mínimo.</span><span class="sxs-lookup"><span data-stu-id="42d3d-135">The DRM header of a protected file may specify may specify a minimum individualization level.</span></span> <span data-ttu-id="42d3d-136">(Para obtener más información, consulte la documentación de WMRMHeader. IndividualizedVersion en el SDK de Windows Media Rights Manager).</span><span class="sxs-lookup"><span data-stu-id="42d3d-136">(For more information, see the documentation for WMRMHeader.IndividualizedVersion in the Windows Media Rights Manager SDK.)</span></span>

<span data-ttu-id="42d3d-137">Dado que el servicio de individualización de Microsoft controla la información del usuario, debe mostrar la Directiva de privacidad de Microsoft o proporcionar un vínculo a esa página en el sitio web de Microsoft antes de que la aplicación individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240> .</span><span class="sxs-lookup"><span data-stu-id="42d3d-137">Because the Microsoft Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft website before your application individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240>.</span></span>

## <a name="provide-the-software-certificate"></a><span data-ttu-id="42d3d-138">Proporcionar el certificado de software</span><span class="sxs-lookup"><span data-stu-id="42d3d-138">Provide the Software Certificate</span></span>

<span data-ttu-id="42d3d-139">Para permitir que la aplicación use la licencia DRM, la aplicación debe proporcionar un certificado de software o una *clave* para el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="42d3d-139">To enable the application to use the DRM license, the application must provide a software certificate or *key* to the Filter Graph Manager.</span></span> <span data-ttu-id="42d3d-140">Esta clave está contenida en una biblioteca estática que es individualizada para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="42d3d-140">This key is contained in a static library that is individualized for the application.</span></span> <span data-ttu-id="42d3d-141">Para obtener información sobre cómo obtener la biblioteca individualizada, consulte [obtención de la biblioteca DRM necesaria](../wmformat/obtaining-the-required-drm-library.md) en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="42d3d-141">For information about obtaining the individualized library, see [Obtaining the Required DRM Library](../wmformat/obtaining-the-required-drm-library.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="42d3d-142">Para proporcionar la clave de software, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="42d3d-142">To provide the software key, perform the following steps:</span></span>

1.  <span data-ttu-id="42d3d-143">Vínculo a la biblioteca estática.</span><span class="sxs-lookup"><span data-stu-id="42d3d-143">Link to the static library.</span></span>
2.  <span data-ttu-id="42d3d-144">Implemente la interfaz **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="42d3d-144">Implement the **IServiceProvider** interface.</span></span>
3.  <span data-ttu-id="42d3d-145">Consulte el administrador de gráficos de filtro para la interfaz [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .</span><span class="sxs-lookup"><span data-stu-id="42d3d-145">Query the Filter Graph Manager for the [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) interface.</span></span>
4.  <span data-ttu-id="42d3d-146">Llame a [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) con un puntero a la implementación de **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="42d3d-146">Call [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) with a pointer to your implementation of **IServiceProvider**.</span></span>
5.  <span data-ttu-id="42d3d-147">Filter Graph Manager llamará a **IServiceProvider:: QueryService** y especificará el **IID \_ IWMReader** para el identificador de servicio.</span><span class="sxs-lookup"><span data-stu-id="42d3d-147">The Filter Graph Manager will call **IServiceProvider::QueryService**, specifying **IID\_IWMReader** for the service identifier.</span></span>
6.  <span data-ttu-id="42d3d-148">En la implementación de **QueryService**, llame a [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) para crear la clave de software.</span><span class="sxs-lookup"><span data-stu-id="42d3d-148">In your implementation of **QueryService**, call [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) to create the software key.</span></span>

<span data-ttu-id="42d3d-149">En el código siguiente se muestra cómo implementar el método **QueryService** :</span><span class="sxs-lookup"><span data-stu-id="42d3d-149">The following code shows how to implement the **QueryService** method:</span></span>


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



<span data-ttu-id="42d3d-150">En el código siguiente se muestra cómo llamar a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) en Filter Graph Manager:</span><span class="sxs-lookup"><span data-stu-id="42d3d-150">The following code shows how to call [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) on the Filter Graph Manager:</span></span>


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a><span data-ttu-id="42d3d-151">Compilar el gráfico de reproducción</span><span class="sxs-lookup"><span data-stu-id="42d3d-151">Building the Playback Graph</span></span>

<span data-ttu-id="42d3d-152">Para reproducir un archivo ASF protegido con DRM, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="42d3d-152">To play a DRM-protected ASF file, perform the following steps:</span></span>

1.  <span data-ttu-id="42d3d-153">Cree el [Administrador de gráficos de filtro](filter-graph-manager.md) y use la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para registrar eventos de grafos.</span><span class="sxs-lookup"><span data-stu-id="42d3d-153">Create the [Filter Graph Manager](filter-graph-manager.md) and use the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to register for graph events.</span></span>
2.  <span data-ttu-id="42d3d-154">Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una nueva instancia del filtro de [lector ASF de WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="42d3d-154">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>
3.  <span data-ttu-id="42d3d-155">Llame a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="42d3d-155">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph.</span></span>
4.  <span data-ttu-id="42d3d-156">Consulte el filtro para la interfaz [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="42d3d-156">Query the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface.</span></span>
5.  <span data-ttu-id="42d3d-157">Llame a [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) con la dirección URL del archivo.</span><span class="sxs-lookup"><span data-stu-id="42d3d-157">Call [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) with the URL of the file.</span></span>
6.  <span data-ttu-id="42d3d-158">Controlar eventos de [**\_ \_ evento WMT de EC**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="42d3d-158">Handle [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span>
7.  <span data-ttu-id="42d3d-159">En el primer evento de [**\_ \_ evento WMT EC**](ec-wmt-event.md) , consulte el filtro de [lector ASF de WM](wm-asf-reader-filter.md) para la interfaz **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="42d3d-159">On the first [**EC\_WMT\_EVENT**](ec-wmt-event.md) event, query the [WM ASF Reader](wm-asf-reader-filter.md) filter for the **IServiceProvider** interface.</span></span>
8.  <span data-ttu-id="42d3d-160">Llame a **IServiceProvider:: QueryService** para obtener un puntero a la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="42d3d-160">Call **IServiceProvider::QueryService** to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
9.  <span data-ttu-id="42d3d-161">Llame a [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para representar los pines de salida del filtro del [lector ASF de WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="42d3d-161">Call [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) to render the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="42d3d-162">Al abrir un archivo protegido con DRM, no llame a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para crear el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="42d3d-162">When opening a DRM-protected file, do not call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) to create the filter graph.</span></span> <span data-ttu-id="42d3d-163">El filtro lector ASF de WM no puede conectarse a ningún otro filtro hasta que se adquiera la licencia DRM.</span><span class="sxs-lookup"><span data-stu-id="42d3d-163">The WM ASF Reader filter cannot connect to any other filters until the DRM license is acquired.</span></span> <span data-ttu-id="42d3d-164">Este paso requiere que la aplicación use la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , que se debe obtener del filtro, tal y como se describe en los pasos 7 a 8.</span><span class="sxs-lookup"><span data-stu-id="42d3d-164">This step requires the application to use the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface, which must be obtained from the filter, as described in steps 7–8.</span></span> <span data-ttu-id="42d3d-165">Por lo tanto, debe crear el filtro y agregarlo al gráfico.</span><span class="sxs-lookup"><span data-stu-id="42d3d-165">Therefore, you must create the filter and add it to the graph</span></span>

 

> [!Note]  
> <span data-ttu-id="42d3d-166">Es importante registrarse para los eventos de gráfico (paso 1) antes de agregar el filtro de [lector ASF de WM](wm-asf-reader-filter.md) al gráfico (paso 3), ya que la aplicación debe controlar los eventos de [**\_ \_ evento WMT de EC**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="42d3d-166">It is important to register for graph events (step 1) before adding the [WM ASF Reader](wm-asf-reader-filter.md) filter to the graph (step 3), because the application must handle the [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span> <span data-ttu-id="42d3d-167">Los eventos se envían cuando se llama a [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) (paso 5).</span><span class="sxs-lookup"><span data-stu-id="42d3d-167">The events are sent when [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) is called (step 5).</span></span>

 

<span data-ttu-id="42d3d-168">En el código siguiente se muestra cómo compilar el gráfico:</span><span class="sxs-lookup"><span data-stu-id="42d3d-168">The following code shows how to build the graph:</span></span>


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="42d3d-169">C++</span><span class="sxs-lookup"><span data-stu-id="42d3d-169">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="42d3d-170">En el código anterior, la `RenderOutputPins` función enumera los terminales de salida en el filtro de [lector ASF de WM](wm-asf-reader-filter.md) y llama a [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para cada pin.</span><span class="sxs-lookup"><span data-stu-id="42d3d-170">In the previous code, the `RenderOutputPins` function enumerates the output pins on the [WM ASF Reader](wm-asf-reader-filter.md) filter and calls [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) for each pin.</span></span>


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



<span data-ttu-id="42d3d-171">En el código siguiente se muestra cómo obtener un puntero a la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) desde el [lector ASF de WM](wm-asf-reader-filter.md):</span><span class="sxs-lookup"><span data-stu-id="42d3d-171">The following code shows how to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md):</span></span>


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="42d3d-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42d3d-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42d3d-173">Leer archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="42d3d-173">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 

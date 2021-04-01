---
description: Protocolos admitidos
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocolos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811528"
---
# <a name="supported-protocols"></a><span data-ttu-id="87a19-103">Protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="87a19-103">Supported Protocols</span></span>

<span data-ttu-id="87a19-104">Media Foundation admite los siguientes protocolos:</span><span class="sxs-lookup"><span data-stu-id="87a19-104">Media Foundation supports the following protocols:</span></span>

-   <span data-ttu-id="87a19-105">Protocolo de streaming en tiempo real (RTSP)</span><span class="sxs-lookup"><span data-stu-id="87a19-105">Real Time Streaming Protocol (RTSP)</span></span>

    <span data-ttu-id="87a19-106">RTSP se usa principalmente para el streaming de contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="87a19-106">RTSP is mainly used for streaming media content.</span></span> <span data-ttu-id="87a19-107">Puede usar UDP o TCP como protocolos de transporte.</span><span class="sxs-lookup"><span data-stu-id="87a19-107">It can use UDP or TCP as transport protocols.</span></span> <span data-ttu-id="87a19-108">UDP es la más eficaz para la entrega de contenido porque la sobrecarga de ancho de banda es menor que con los protocolos basados en TCP.</span><span class="sxs-lookup"><span data-stu-id="87a19-108">UDP is the most efficient for content delivery because the bandwidth overhead is less than with TCP-based protocols.</span></span> <span data-ttu-id="87a19-109">A pesar de que el protocolo TCP garantiza la entrega de paquetes confiable, TCP no es adecuado para flujos multimedia digitales, donde el uso eficaz del ancho de banda es más importante que los paquetes perdidos ocasionales.</span><span class="sxs-lookup"><span data-stu-id="87a19-109">Even though the TCP protocol ensures reliable packet delivery, TCP is not well suited for digital media streams, where efficient use of bandwidth is more important than occasional lost packets.</span></span>

-   <span data-ttu-id="87a19-110">Protocolo de transferencia de hipertexto (HTTP)</span><span class="sxs-lookup"><span data-stu-id="87a19-110">Hypertext Transfer Protocol (HTTP)</span></span>

    <span data-ttu-id="87a19-111">HTTP usa TCP y lo usan los servidores Web.</span><span class="sxs-lookup"><span data-stu-id="87a19-111">HTTP uses TCP and is used by web servers.</span></span> <span data-ttu-id="87a19-112">El esquema "httpd://" indica que el origen se descarga desde un servidor Web.</span><span class="sxs-lookup"><span data-stu-id="87a19-112">The "httpd://" scheme indicates that the source is downloadable from a web server.</span></span> <span data-ttu-id="87a19-113">HTTP también se usa en el caso de los firewalls, que normalmente se configuran para aceptar solicitudes HTTP y suelen rechazar otros protocolos de streaming.</span><span class="sxs-lookup"><span data-stu-id="87a19-113">HTTP is also used in case of firewalls, which are usually configured to accept HTTP requests and typically reject other streaming protocols.</span></span>

<span data-ttu-id="87a19-114">La aplicación puede obtener los protocolos admitidos por Media Foundation mediante la interfaz [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) .</span><span class="sxs-lookup"><span data-stu-id="87a19-114">The application can get the protocols supported by Media Foundation by using the [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) interface.</span></span> <span data-ttu-id="87a19-115">Para ello, la aplicación debe recuperar primero el número de protocolos, llamando a [**IMFNetSchemeHandlerConfig:: GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) y, a continuación, obtener el tipo de protocolo basándose en el índice llamando a [**IMFNetSchemeHandlerConfig:: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span><span class="sxs-lookup"><span data-stu-id="87a19-115">To do this, the application must first retrieve the number of protocols, by calling [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) and then get the protocol type based on the index by calling [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span></span> <span data-ttu-id="87a19-116">Este método devuelve uno de los valores definidos en la enumeración del [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="87a19-116">This method returns one of the values defined in the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>

<span data-ttu-id="87a19-117">La aplicación también puede obtener los esquemas admitidos por la resolución de origen mediante una llamada a la función [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .</span><span class="sxs-lookup"><span data-stu-id="87a19-117">The application can also get the schemes supported by the source resolver by calling the [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) function.</span></span>

## <a name="protocol-rollover"></a><span data-ttu-id="87a19-118">Sustitución de protocolo</span><span class="sxs-lookup"><span data-stu-id="87a19-118">Protocol Rollover</span></span>

<span data-ttu-id="87a19-119">Cuando una aplicación especifica "mms://" como el esquema de la dirección URL, la resolución de origen realiza una operación de *sustitución del protocolo* .</span><span class="sxs-lookup"><span data-stu-id="87a19-119">When an application specifies "mms://" as the URL scheme, the source resolver performs a *protocol rollover* operation.</span></span> <span data-ttu-id="87a19-120">En este proceso, la resolución de origen determina el mejor protocolo para que el origen de red lo use para obtener el contenido.</span><span class="sxs-lookup"><span data-stu-id="87a19-120">In this process, the source resolver determines the best protocol for the network source to use for getting the content.</span></span> <span data-ttu-id="87a19-121">Normalmente, para el streaming multimedia, RTSP con UDP (RTSPU) es más eficaz que HTTP.</span><span class="sxs-lookup"><span data-stu-id="87a19-121">Typically, for media steaming, RTSP with UDP (RTSPU) is more efficient than HTTP.</span></span> <span data-ttu-id="87a19-122">Sin embargo, si el contenido está hospedado en un servidor Web, HTTP es una mejor opción.</span><span class="sxs-lookup"><span data-stu-id="87a19-122">However, if the content is hosted on a web server, HTTP is a better choice.</span></span>

<span data-ttu-id="87a19-123">La sustitución del protocolo también puede producirse cuando se produce un error al intentar usar el protocolo especificado en el esquema de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="87a19-123">Protocol rollover can also occur when an attempt to use the protocol specified in the URL scheme fails.</span></span> <span data-ttu-id="87a19-124">Por ejemplo, se puede producir un error en un protocolo cuando un Firewall bloquea paquetes UDP.</span><span class="sxs-lookup"><span data-stu-id="87a19-124">For example, a protocol can fail when a firewall blocks UDP packets.</span></span> <span data-ttu-id="87a19-125">En este caso, la resolución de origen cambia a HTTP.</span><span class="sxs-lookup"><span data-stu-id="87a19-125">In this case, the source resolver switches to HTTP.</span></span>

<span data-ttu-id="87a19-126">La sustitución de protocolos no se aplica si el esquema de direcciones URL contiene un protocolo específico, como "rtspu://".</span><span class="sxs-lookup"><span data-stu-id="87a19-126">Protocol rollover does not apply if the URL scheme contains a specific protocol, such as "rtspu://".</span></span> <span data-ttu-id="87a19-127">Además, la sustitución no se realiza si se produce un error de autenticación o el servidor ha alcanzado un límite de conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="87a19-127">Also, rollover is not performed if authentication fails or the server has reached a limit of client connections.</span></span> <span data-ttu-id="87a19-128">Se recomienda que las aplicaciones especifiquen el esquema "mms://" y que la resolución de origen Seleccione el mejor protocolo para el escenario.</span><span class="sxs-lookup"><span data-stu-id="87a19-128">It is recommended that applications specify the "mms://" scheme and allow the source resolver to select the best protocol for the scenario.</span></span>

<span data-ttu-id="87a19-129">En la tabla siguiente se muestra el orden de sustitución incremental.</span><span class="sxs-lookup"><span data-stu-id="87a19-129">The following table lists the rollover order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87a19-130">Esquemas permitidos</span><span class="sxs-lookup"><span data-stu-id="87a19-130">Schemes allowed</span></span></th>
<th><span data-ttu-id="87a19-131">Orden de sustitución de protocolos</span><span class="sxs-lookup"><span data-stu-id="87a19-131">Protocol rollover order</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87a19-132">mms://o rtsp://</span><span class="sxs-lookup"><span data-stu-id="87a19-132">mms:// or rtsp://</span></span></td>
<td><span data-ttu-id="87a19-133">Caché rápida habilitada:</span><span class="sxs-lookup"><span data-stu-id="87a19-133">Fast Cache enabled:</span></span><br/>
<ol>
<li><span data-ttu-id="87a19-134">RTSP con TCP (RTSPt)</span><span class="sxs-lookup"><span data-stu-id="87a19-134">RTSP with TCP (RTSPT)</span></span><br/></li>
<li><span data-ttu-id="87a19-135">RTSP con UDP (RTSPU)</span><span class="sxs-lookup"><span data-stu-id="87a19-135">RTSP with UDP (RTSPU)</span></span><br/></li>
<li><span data-ttu-id="87a19-136">Transmisión por secuencias HTTP</span><span class="sxs-lookup"><span data-stu-id="87a19-136">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="87a19-137">Descarga HTTP (HTTPD)</span><span class="sxs-lookup"><span data-stu-id="87a19-137">HTTP download (HTTPD)</span></span><br/></li>
</ol>
<span data-ttu-id="87a19-138">Caché rápida deshabilitada:</span><span class="sxs-lookup"><span data-stu-id="87a19-138">Fast Cache disabled:</span></span><br/>
<ol>
<li><span data-ttu-id="87a19-139">RTSPU</span><span class="sxs-lookup"><span data-stu-id="87a19-139">RTSPU</span></span><br/></li>
<li><span data-ttu-id="87a19-140">RTSPt</span><span class="sxs-lookup"><span data-stu-id="87a19-140">RTSPT</span></span><br/></li>
<li><span data-ttu-id="87a19-141">Transmisión por secuencias HTTP</span><span class="sxs-lookup"><span data-stu-id="87a19-141">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="87a19-142">Descarga HTTP</span><span class="sxs-lookup"><span data-stu-id="87a19-142">HTTP Download</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87a19-143">rtspu://</span><span class="sxs-lookup"><span data-stu-id="87a19-143">rtspu://</span></span></td>
<td><span data-ttu-id="87a19-144">RTSPU</span><span class="sxs-lookup"><span data-stu-id="87a19-144">RTSPU</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87a19-145">rtspt://</span><span class="sxs-lookup"><span data-stu-id="87a19-145">rtspt://</span></span></td>
<td><span data-ttu-id="87a19-146">RTSPt</span><span class="sxs-lookup"><span data-stu-id="87a19-146">RTSPT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87a19-147"> https://</span><span class="sxs-lookup"><span data-stu-id="87a19-147">https://</span></span></td>
<td><ol>
<li><span data-ttu-id="87a19-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="87a19-148">HTTP</span></span><br/></li>
<li><span data-ttu-id="87a19-149">HTTPD</span><span class="sxs-lookup"><span data-stu-id="87a19-149">HTTPD</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87a19-150">httpd://</span><span class="sxs-lookup"><span data-stu-id="87a19-150">httpd://</span></span></td>
<td><span data-ttu-id="87a19-151">HTTPD</span><span class="sxs-lookup"><span data-stu-id="87a19-151">HTTPD</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a><span data-ttu-id="87a19-152">Recuperación del protocolo actual</span><span class="sxs-lookup"><span data-stu-id="87a19-152">Retrieving the Current Protocol</span></span>

<span data-ttu-id="87a19-153">Después de una operación de sustitución de protocolo, el origen de red podría usar un protocolo distinto del especificado por la aplicación en el esquema de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="87a19-153">After a protocol rollover operation, the network source might use a protocol other than the one specified by the application in the URL scheme.</span></span> <span data-ttu-id="87a19-154">El resultado de la sustitución del protocolo está disponible para la aplicación después de que el origen de red establezca la conexión con el servidor multimedia.</span><span class="sxs-lookup"><span data-stu-id="87a19-154">The protocol rollover result is available to the application after the network source establishes the connection with the media server.</span></span>

<span data-ttu-id="87a19-155">Para obtener el protocolo y el transporte que se usan para obtener el contenido, la aplicación puede recuperar los valores de propiedad de la propiedad de [ \_ Protocolo MFNETSOURCE](mfnetsource-protocol-property.md) y la propiedad de [ \_ transporte MFNETSOURCE](mfnetsource-transport-property.md) de un objeto **IPropertyStore** desde el origen de red.</span><span class="sxs-lookup"><span data-stu-id="87a19-155">To get the protocol and transport that are used for getting the content, the application can retrieve the property values for the [MFNETSOURCE\_PROTOCOL](mfnetsource-protocol-property.md) property and the [MFNETSOURCE\_TRANSPORT](mfnetsource-transport-property.md) property of an **IPropertyStore** object from the network source.</span></span>

<span data-ttu-id="87a19-156">En el código siguiente se muestra cómo obtener estos valores.</span><span class="sxs-lookup"><span data-stu-id="87a19-156">The following code shows how to get these values.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



<span data-ttu-id="87a19-157">En el código de ejemplo anterior, **IPropertyStore:: GetValue** recupera el \_ valor del protocolo MFNETSOURCE, que es miembro de la enumeración del [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="87a19-157">In the preceding example code, **IPropertyStore::GetValue** retrieves the MFNETSOURCE\_PROTOCOL value, which is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span> <span data-ttu-id="87a19-158">En el caso del \_ transporte MFNETSOURCE, el valor es un miembro de la enumeración de [**\_ \_ tipo de transporte MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="87a19-158">For MFNETSOURCE\_TRANSPORT, the value is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>

<span data-ttu-id="87a19-159">Como alternativa, la aplicación puede obtener los mismos valores mediante el servicio MFNETSOURCE \_ Statistics \_ Service.</span><span class="sxs-lookup"><span data-stu-id="87a19-159">Alternately, the application can get the same values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span> <span data-ttu-id="87a19-160">Para usar este servicio, la aplicación puede llamar a la función [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener el almacén de propiedades del origen de red.</span><span class="sxs-lookup"><span data-stu-id="87a19-160">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store from the network source.</span></span> <span data-ttu-id="87a19-161">Este almacén de propiedades contiene estadísticas de red en la propiedad [MFNETSOURCE \_ Statistics](mfnetsource-statistics-property.md) .</span><span class="sxs-lookup"><span data-stu-id="87a19-161">This property store contains network statistics in the [MFNETSOURCE\_STATISTICS](mfnetsource-statistics-property.md) property.</span></span> <span data-ttu-id="87a19-162">Los valores de protocolo y transporte se pueden recuperar especificando \_ \_ el identificador de protocolo de MFNETSOURCE y \_ \_ el identificador de transporte de MFNETSOURCE, definidos en la enumeración de [**\_ \_ identificadores de MFNETSOURCE Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="87a19-162">Protocol and transport values can be retrieved by specifying MFNETSOURCE\_PROTOCOL\_ID and MFNETSOURCE\_TRANSPORT\_ID—defined in the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration.</span></span> <span data-ttu-id="87a19-163">En el código siguiente se muestra cómo obtener el protocolo y los valores de transporte mediante el \_ servicio MFNETSOURCE Statistics \_ Service.</span><span class="sxs-lookup"><span data-stu-id="87a19-163">The following code shows how to get the protocol and transport values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a><span data-ttu-id="87a19-164">Habilitar y deshabilitar protocolos</span><span class="sxs-lookup"><span data-stu-id="87a19-164">Enabling and Disabling Protocols</span></span>

<span data-ttu-id="87a19-165">La aplicación puede configurar el origen de red para que se omitan determinados protocolos durante el proceso de sustitución incremental.</span><span class="sxs-lookup"><span data-stu-id="87a19-165">The application can configure the network source so that certain protocols are skipped during the rollover process.</span></span> <span data-ttu-id="87a19-166">Para ello, se usan las propiedades de origen de red para deshabilitar determinados protocolos.</span><span class="sxs-lookup"><span data-stu-id="87a19-166">To do this, network source properties are used to disable specific protocols.</span></span> <span data-ttu-id="87a19-167">En la tabla siguiente se muestran las propiedades y los protocolos que controlan.</span><span class="sxs-lookup"><span data-stu-id="87a19-167">The following table shows the properties and the protocols they control.</span></span>



| <span data-ttu-id="87a19-168">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87a19-168">Property</span></span>                                                                    | <span data-ttu-id="87a19-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="87a19-169">Description</span></span>                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="87a19-170">MFNETSOURCE \_ habilitar \_ http</span><span class="sxs-lookup"><span data-stu-id="87a19-170">MFNETSOURCE\_ENABLE\_HTTP</span></span>](mfnetsource-enable-http-property.md)           | <span data-ttu-id="87a19-171">Habilita o deshabilita HTTP y HTTPD.</span><span class="sxs-lookup"><span data-stu-id="87a19-171">Enables or disables HTTP and HTTPD.</span></span>         |
| [<span data-ttu-id="87a19-172">MFNETSOURCE \_ habilitar \_ RTSP</span><span class="sxs-lookup"><span data-stu-id="87a19-172">MFNETSOURCE\_ENABLE\_RTSP</span></span>](mfnetsource-enable-rtsp-property.md)           | <span data-ttu-id="87a19-173">Habilita o deshabilita RTSPU y RTSPt.</span><span class="sxs-lookup"><span data-stu-id="87a19-173">Enables or disables RTSPU and RTSPT.</span></span>        |
| [<span data-ttu-id="87a19-174">MFNETSOURCE \_ habilitar \_ TCP</span><span class="sxs-lookup"><span data-stu-id="87a19-174">MFNETSOURCE\_ENABLE\_TCP</span></span>](mfnetsource-enable-tcp-property.md)             | <span data-ttu-id="87a19-175">Habilita o deshabilita RTSPt.</span><span class="sxs-lookup"><span data-stu-id="87a19-175">Enables or disables RTSPT.</span></span>                  |
| [<span data-ttu-id="87a19-176">MFNETSOURCE \_ habilitar \_ UDP</span><span class="sxs-lookup"><span data-stu-id="87a19-176">MFNETSOURCE\_ENABLE\_UDP</span></span>](mfnetsource-enable-udp-property.md)             | <span data-ttu-id="87a19-177">Habilita o deshabilita RTSPU.</span><span class="sxs-lookup"><span data-stu-id="87a19-177">Enables or disables RTSPU.</span></span>                  |
| [<span data-ttu-id="87a19-178">MFNETSOURCE \_ habilitar \_ descarga</span><span class="sxs-lookup"><span data-stu-id="87a19-178">MFNETSOURCE\_ENABLE\_DOWNLOAD</span></span>](mfnetsource-enable-download-property.md)   | <span data-ttu-id="87a19-179">Habilita o deshabilita HTTPD.</span><span class="sxs-lookup"><span data-stu-id="87a19-179">Enables or disables HTTPD.</span></span>                  |
| [<span data-ttu-id="87a19-180">MFNETSOURCE \_ habilitar \_ streaming</span><span class="sxs-lookup"><span data-stu-id="87a19-180">MFNETSOURCE\_ENABLE\_STREAMING</span></span>](mfnetsource-enable-streaming-property.md) | <span data-ttu-id="87a19-181">Habilita o deshabilita RTSPU, RTSPt y HTTP.</span><span class="sxs-lookup"><span data-stu-id="87a19-181">Enables or disables RTSPU, RTSPT, and HTTP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="87a19-182">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87a19-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87a19-183">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87a19-183">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 





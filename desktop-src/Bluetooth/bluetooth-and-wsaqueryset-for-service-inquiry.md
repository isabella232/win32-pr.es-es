---
title: Bluetooth y WSAQUERYSET para la consulta de servicio
description: Uso de la estructura WSAQUERYSET con las funciones WSALookupServiceBegin y WSALookupServiceNext para obtener información sobre el proceso de consulta de servicio.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth y WSAQUERYSET para la consulta de servicio Bluetooth
- WSAQUERYSET Bluetooth, para la consulta de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795303"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a><span data-ttu-id="f7f75-105">Bluetooth y WSAQUERYSET para la consulta de servicio</span><span class="sxs-lookup"><span data-stu-id="f7f75-105">Bluetooth and WSAQUERYSET for Service Inquiry</span></span>

<span data-ttu-id="f7f75-106">Bluetooth usa la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , con varias funciones, para facilitar la detección de dispositivos y servicios en el espacio de nombres Bluetooth, NS \_ BTH.</span><span class="sxs-lookup"><span data-stu-id="f7f75-106">Bluetooth uses the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure, with various functions, to facilitate the discovery of devices and services in the Bluetooth namespace, NS\_BTH.</span></span>

<span data-ttu-id="f7f75-107">Las funciones [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usan la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obtener datos sobre el proceso de consulta de servicio.</span><span class="sxs-lookup"><span data-stu-id="f7f75-107">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) and [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) functions use the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to obtain data about the service inquiry process.</span></span> <span data-ttu-id="f7f75-108">En la tabla siguiente se describe cómo establecer los valores de miembro de la estructura **WSAQUERYSET** para este propósito.</span><span class="sxs-lookup"><span data-stu-id="f7f75-108">The following table describes how to set the member values in the **WSAQUERYSET** structure for this purpose.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7f75-109">Miembro</span><span class="sxs-lookup"><span data-stu-id="f7f75-109">Member</span></span></th>
<th><span data-ttu-id="f7f75-110">Entrada en WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="f7f75-110">Input to WSALookupServiceBegin</span></span></th>
<th><span data-ttu-id="f7f75-111">Valor devuelto de WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="f7f75-111">Returned value from WSALookupServiceNext</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7f75-112"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-112"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="f7f75-113">Debe establecerse en <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="f7f75-113">Must be set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
<td><span data-ttu-id="f7f75-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) devuelto por System.</span><span class="sxs-lookup"><span data-stu-id="f7f75-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) returned by system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f75-115"><strong>dwOutputFlags</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-115"><strong>dwOutputFlags</strong></span></span></td>
<td><span data-ttu-id="f7f75-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-116">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-117">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7f75-118"><strong>lpszServiceInstanceName</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-118"><strong>lpszServiceInstanceName</strong></span></span></td>
<td><span data-ttu-id="f7f75-119">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-119">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-120">Nombre para mostrar del servicio, convertido en una cadena codificada en UTF-8 de la codificación de idioma predeterminada del atributo SDP de Bluetooth ServiceName.</span><span class="sxs-lookup"><span data-stu-id="f7f75-120">Display name of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceName SDP attribute.</span></span> <span data-ttu-id="f7f75-121">Se devuelve si se especifica LUP_RETURN_NAME.</span><span class="sxs-lookup"><span data-stu-id="f7f75-121">Returned if LUP_RETURN_NAME is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f75-122"><strong>lpServiceClassId</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-122"><strong>lpServiceClassId</strong></span></span></td>
<td><span data-ttu-id="f7f75-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7f75-123">Required.</span></span> <span data-ttu-id="f7f75-124">El UUID de Bluetooth único más específico para los servicios para los que se realiza la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f7f75-124">The most specific single Bluetooth UUID for the services for which the search is being conducted.</span></span> <span data-ttu-id="f7f75-125">Por ejemplo, si este valor se establece en el UUID del protocolo L2CAP, devuelve todos los servicios que usan el protocolo L2CAP en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="f7f75-125">For example, if this value is set to the UUID of the L2CAP protocol, it returns all services using the L2CAP protocol on the target device.</span></span> <span data-ttu-id="f7f75-126">Si se establece en el UUID de un servicio específico, solo devolverá las instancias de ese servicio.</span><span class="sxs-lookup"><span data-stu-id="f7f75-126">If set to the UUID of a specific service, it would return only the instances of that service.</span></span></td>
<td><span data-ttu-id="f7f75-127">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-127">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7f75-128"><strong>lpVersion</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-128"><strong>lpVersion</strong></span></span></td>
<td><span data-ttu-id="f7f75-129">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-129">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-130">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-130">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f75-131"><strong>lpszComment</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-131"><strong>lpszComment</strong></span></span></td>
<td><span data-ttu-id="f7f75-132">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-132">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-133">Descripción del servicio, convertido como una cadena codificada en UTF-8 de la codificación de idioma predeterminada del atributo de SDP de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="f7f75-133">Description of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceDescription SDP attribute.</span></span> <span data-ttu-id="f7f75-134">Se devuelve si se especifica <strong>LUP_RETURN_COMMENT</strong> .</span><span class="sxs-lookup"><span data-stu-id="f7f75-134">Returned if <strong>LUP_RETURN_COMMENT</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7f75-135"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-135"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="f7f75-136">Debe ser NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="f7f75-136">Must be NS_BTH.</span></span></td>
<td><span data-ttu-id="f7f75-137">Devuelve NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="f7f75-137">Returns NS_BTH.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f75-138"><strong>lpNSProviderId</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-138"><strong>lpNSProviderId</strong></span></span></td>
<td><span data-ttu-id="f7f75-139">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-139">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-140">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-140">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7f75-141"><strong>lpszContext</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-141"><strong>lpszContext</strong></span></span></td>
<td><span data-ttu-id="f7f75-142">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7f75-142">Required.</span></span> <span data-ttu-id="f7f75-143">La dirección del dispositivo Bluetooth con la que se establece una conexión SDP y se consultan los servicios.</span><span class="sxs-lookup"><span data-stu-id="f7f75-143">The Bluetooth Device Address with which to establish an SDP connection and query for services.</span></span> <span data-ttu-id="f7f75-144">Este valor debe ser una cadena convertida mediante la llamada a la función <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f7f75-144">This value must be a string that was converted by using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> function call.</span></span> <span data-ttu-id="f7f75-145">Si se proporciona la dirección del dispositivo Bluetooth local, se busca en la base de datos SDP local.</span><span class="sxs-lookup"><span data-stu-id="f7f75-145">If the local Bluetooth device address is provided, the local SDP database is searched.</span></span></td>
<td><span data-ttu-id="f7f75-146">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-146">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f75-147"><strong>dwNumberOfProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-147"><strong>dwNumberOfProtocols</strong></span></span></td>
<td><span data-ttu-id="f7f75-148">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-148">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-149">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-149">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7f75-150"><strong>lpafpProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-150"><strong>lpafpProtocols</strong></span></span></td>
<td><span data-ttu-id="f7f75-151">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-151">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-152">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-152">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f75-153"><strong>lpszQueryString</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-153"><strong>lpszQueryString</strong></span></span></td>
<td><span data-ttu-id="f7f75-154">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-154">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-155">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-155">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7f75-156"><strong>dwNumberOfCsAddrs</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-156"><strong>dwNumberOfCsAddrs</strong></span></span></td>
<td><span data-ttu-id="f7f75-157">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-157">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-158">Indica el número de elementos de la matriz de estructuras de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f7f75-158">Indicates the number of elements in the array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7f75-159"><strong>lpcsaBuffer</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-159"><strong>lpcsaBuffer</strong></span></span></td>
<td><span data-ttu-id="f7f75-160">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f7f75-160">Not used.</span></span></td>
<td><span data-ttu-id="f7f75-161">Puntero a una estructura de <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> cuyo miembro <strong>LocalAddr. lpSockaddr</strong> señala a un <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> que contiene la dirección completa conectable del servicio remoto, convertida a partir de la primera entrada del atributo SDP de Bluetooth ProtocolDescriptorList.</span><span class="sxs-lookup"><span data-stu-id="f7f75-161">Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structure whose <strong>LocalAddr.lpSockaddr</strong> member points to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> that contains the complete connectable address of the remote service, converted from the first entry of the Bluetooth ProtocolDescriptorList SDP attribute.</span></span> <span data-ttu-id="f7f75-162">Se devuelve si se especifica <strong>LUP_RETURN_ADDR</strong> .</span><span class="sxs-lookup"><span data-stu-id="f7f75-162">Returned if <strong>LUP_RETURN_ADDR</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7f75-163"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="f7f75-163"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="f7f75-164">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f7f75-164">Optional.</span></span> <span data-ttu-id="f7f75-165">Puntero a una estructura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> que contiene parámetros avanzados para limitar los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f7f75-165">Pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> structure that contains advanced parameters to limit the results of the search.</span></span> <span data-ttu-id="f7f75-166">Si se proporciona, se omite <strong>lpServiceClassId</strong> y las consultas en caché no se realizan correctamente.</span><span class="sxs-lookup"><span data-stu-id="f7f75-166">If provided, <strong>lpServiceClassId</strong> is ignored and cached queries do not succeed.</span></span></td>
<td><ul>
<li><span data-ttu-id="f7f75-167">Si se realiza una búsqueda de servicio: puntero a una estructura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> que devuelve los identificadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="f7f75-167">If a service search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the service handles.</span></span> <span data-ttu-id="f7f75-168">(<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ulong) calcula el número de identificadores.</span><span class="sxs-lookup"><span data-stu-id="f7f75-168">(<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calculates the number of handles.</span></span> <span data-ttu-id="f7f75-169"><strong>BLOB. pBlobData</strong> es una matriz de valores ulong que representan los identificadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="f7f75-169"><strong>BLOB.pBlobData</strong> is an array of ULONG values representing the service handles.</span></span></li>
<li><span data-ttu-id="f7f75-170">Si se realiza una búsqueda de atributos o serviceAttribute: puntero a una estructura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> que devuelve el registro SDP binario.</span><span class="sxs-lookup"><span data-stu-id="f7f75-170">If an attribute or serviceAttribute search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the binary SDP record.</span></span> <span data-ttu-id="f7f75-171"><strong>BLOB. cbSize</strong> es el tamaño del registro SDP binario.</span><span class="sxs-lookup"><span data-stu-id="f7f75-171"><strong>BLOB.cbSize</strong> is the size of the binary SDP record.</span></span> <span data-ttu-id="f7f75-172"><strong>BLOB. pBlobData</strong> apunta al propio registro.</span><span class="sxs-lookup"><span data-stu-id="f7f75-172"><strong>BLOB.pBlobData</strong> points to the record itself.</span></span> <span data-ttu-id="f7f75-173">El registro SDP binario es necesario en muchos casos porque solo se puede convertir un número limitado de atributos SDP en la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> y solo se convierten las cadenas UTF-8 codificadas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f7f75-173">The binary SDP record is necessary in many cases because only a limited number of SDP attributes are able to be converted to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure, and only default encoded UTF-8 strings are converted.</span></span> <span data-ttu-id="f7f75-174">Las funciones que ayudan a analizar el registro SDP binario se proporcionan en la sección de <a href="bluetooth-reference.md">referencia de Bluetooth</a> .</span><span class="sxs-lookup"><span data-stu-id="f7f75-174">Functions to assist in parsing the binary SDP record are provided in the <a href="bluetooth-reference.md">Bluetooth Reference</a> section.</span></span></li>
<li><span data-ttu-id="f7f75-175">Se devuelve si se especifica LUP_RETURN_BLOB.</span><span class="sxs-lookup"><span data-stu-id="f7f75-175">Returned if LUP_RETURN_BLOB is specified.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f7f75-176">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7f75-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7f75-177">Bluetooth y WSAQUERYSET para Set Service</span><span class="sxs-lookup"><span data-stu-id="f7f75-177">Bluetooth and WSAQUERYSET for Set Service</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[<span data-ttu-id="f7f75-178">Bluetooth y WSAQUERYSET para la consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f7f75-178">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="f7f75-179">Bluetooth y BLOB</span><span class="sxs-lookup"><span data-stu-id="f7f75-179">Bluetooth and BLOB</span></span>](bluetooth-and-blob.md)
</dt> <dt>

[<span data-ttu-id="f7f75-180">Bluetooth y WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="f7f75-180">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

<span data-ttu-id="f7f75-181">Bluetooth y WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="f7f75-181">Bluetooth and WSALookupServiceNext</span></span>
</dt> <dt>

[<span data-ttu-id="f7f75-182">Referencia de Bluetooth</span><span class="sxs-lookup"><span data-stu-id="f7f75-182">Bluetooth Reference</span></span>](bluetooth-reference.md)
</dt> <dt>

[<span data-ttu-id="f7f75-183">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="f7f75-183">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="f7f75-184">**\_servicio de consulta de BTH \_**</span><span class="sxs-lookup"><span data-stu-id="f7f75-184">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="f7f75-185">**información de CSADDR \_**</span><span class="sxs-lookup"><span data-stu-id="f7f75-185">**CSADDR\_INFO**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[<span data-ttu-id="f7f75-186">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="f7f75-186">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="f7f75-187">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="f7f75-187">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="f7f75-188">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="f7f75-188">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="f7f75-189">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="f7f75-189">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
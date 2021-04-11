---
title: Bluetooth y WSALookupServiceBegin para la consulta de dispositivo
description: En este tema se describe cómo usar la función WSALookupServiceBegin para realizar una consulta de dispositivos visibles y fantasma. Para obtener más información, vea detección de dispositivos y servicios Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth y WSALookupServiceBegin para la consulta de dispositivos Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104149690"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a><span data-ttu-id="54420-105">Bluetooth y WSALookupServiceBegin para la consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="54420-105">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>

<span data-ttu-id="54420-106">En este tema se describe cómo usar la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para realizar una consulta de dispositivos visibles y fantasma.</span><span class="sxs-lookup"><span data-stu-id="54420-106">This topic describes how to use the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function to perform an inquiry of both visible and ghosted devices.</span></span> <span data-ttu-id="54420-107">Para obtener más información, vea [detección de dispositivos y servicios Bluetooth](discovering-bluetooth-devices-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="54420-107">For more information, see [Discovering Bluetooth Devices and Services](discovering-bluetooth-devices-and-services.md).</span></span>

<span data-ttu-id="54420-108">La función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa una estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) en su primer parámetro, *lpqsRestrictions*, para definir los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="54420-108">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function uses a [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure in its first parameter, *lpqsRestrictions*, to define search criteria.</span></span> <span data-ttu-id="54420-109">Bluetooth proporciona instrucciones específicas para el uso de la función **WSALookupServiceBegin** y **WSAQUERYSET**.</span><span class="sxs-lookup"><span data-stu-id="54420-109">Bluetooth provides specific guidelines for use of the **WSALookupServiceBegin** function and **WSAQUERYSET**.</span></span>

<span data-ttu-id="54420-110">En la tabla siguiente se enumeran las restricciones que se aplican a la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) que se pasa al parámetro *lpqsRestrictions* al consultar los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="54420-110">The following table lists restrictions that apply to the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed to the *lpqsRestrictions* parameter when querying for devices.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54420-111">Miembro WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="54420-111">WSAQUERYSET member</span></span></th>
<th><span data-ttu-id="54420-112">Restricción</span><span class="sxs-lookup"><span data-stu-id="54420-112">Restriction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54420-113"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="54420-113"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="54420-114">Establezca en <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="54420-114">Set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54420-115"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="54420-115"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="54420-116">Este miembro contiene un puntero opcional a una estructura de <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>blobs</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="54420-116">This member contains an optional pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure.</span></span> <span data-ttu-id="54420-117">Si se especifica este miembro, los parámetros de consulta de dispositivo válidos para <strong>LUP_FLUSHCACHE</strong> son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="54420-117">If this member is specified, the valid device inquire parameters for <strong>LUP_FLUSHCACHE</strong> are as follows:</span></span>
<ul>
<li><span data-ttu-id="54420-118">El miembro <strong>cbSize</strong> de la estructura del <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> debe ser <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span><span class="sxs-lookup"><span data-stu-id="54420-118">The <strong>cbSize</strong> member of the <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure must be <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span></span></li>
<li><span data-ttu-id="54420-119">El miembro <strong>pBlobData</strong> es un puntero a una estructura de <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , para la que el miembro <strong>LAP</strong> es el código de acceso de la consulta Bluetooth y el miembro de <strong>longitud</strong> es la longitud, en segundos, de la consulta.</span><span class="sxs-lookup"><span data-stu-id="54420-119">The <strong>pBlobData</strong> member is a pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> structure, for which the <strong>LAP</strong> member is the Bluetooth inquiry access code, and the <strong>length</strong> member is the length, in seconds, of the inquiry.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54420-120"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="54420-120"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="54420-121">Establezca en <strong>NS_BTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="54420-121">Set to <strong>NS_BTH</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54420-122">Otros miembros</span><span class="sxs-lookup"><span data-stu-id="54420-122">Other members</span></span></td>
<td><span data-ttu-id="54420-123">Se omiten otros miembros de la estructura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="54420-123">Other members of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure are ignored.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="54420-124">Las marcas que se muestran en la tabla siguiente se usan en el parámetro *dwControlFlags* para controlar los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="54420-124">The flags listed in the following table are used in the *dwControlFlags* parameter to control the query results.</span></span> <span data-ttu-id="54420-125">Los **\_ contenedores LUP** y las marcas **\_ FLUSHCACHE LUP** se usan en la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ; el resto de las marcas se usan en las llamadas a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="54420-125">The **LUP\_CONTAINERS** and **LUP\_FLUSHCACHE** flags are used by the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function; the rest of the flags are used in calls to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span>

| <span data-ttu-id="54420-126">Marca</span><span class="sxs-lookup"><span data-stu-id="54420-126">Flag</span></span>               | <span data-ttu-id="54420-127">Resultado</span><span class="sxs-lookup"><span data-stu-id="54420-127">Result</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54420-128">contenedores de LUP \_</span><span class="sxs-lookup"><span data-stu-id="54420-128">LUP\_CONTAINERS</span></span>    | <span data-ttu-id="54420-129">Especifica que el propósito de la consulta es obtener una lista de dispositivos Bluetooth y no una lista de servicios.</span><span class="sxs-lookup"><span data-stu-id="54420-129">Specifies that the query purpose is to obtain a list of Bluetooth devices and not a list of services.</span></span> <span data-ttu-id="54420-130">Se debe establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="54420-130">This flag must be set.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="54420-131">LUP \_ FLUSHCACHE</span><span class="sxs-lookup"><span data-stu-id="54420-131">LUP\_FLUSHCACHE</span></span>    | <span data-ttu-id="54420-132">Desencadena una consulta de dispositivos locales o hace que se devuelvan los resultados almacenados en caché de las consultas anteriores.</span><span class="sxs-lookup"><span data-stu-id="54420-132">Triggers an inquiry of local devices or causes cached results from previous queries to be returned.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="54420-133">\_tipo de valor devuelto LUP \_</span><span class="sxs-lookup"><span data-stu-id="54420-133">LUP\_RETURN\_TYPE</span></span>  | <span data-ttu-id="54420-134">Devuelve el COD Bluetooth (clase de bits de dispositivo) directamente en el miembro **lpServiceClassId** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="54420-134">Return the Bluetooth COD (class of device bits) directly in the **lpServiceClassId** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="54420-135">El COD se asigna al miembro **data1** del GUID.</span><span class="sxs-lookup"><span data-stu-id="54420-135">The COD is mapped to the **Data1** member of the GUID.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="54420-136">\_servicio res de LUP \_</span><span class="sxs-lookup"><span data-stu-id="54420-136">LUP\_RES\_SERVICE</span></span>  | <span data-ttu-id="54420-137">Devuelve información de la dirección Bluetooth local.</span><span class="sxs-lookup"><span data-stu-id="54420-137">Return information for the local Bluetooth address.</span></span> <span data-ttu-id="54420-138">Esta marca solo tiene efecto si también se especifica **LUP \_ Return \_ addr** .</span><span class="sxs-lookup"><span data-stu-id="54420-138">This flag has an effect only if **LUP\_RETURN\_ADDR** is also specified.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="54420-139">\_nombre devuelto de LUP \_</span><span class="sxs-lookup"><span data-stu-id="54420-139">LUP\_RETURN\_NAME</span></span>  | <span data-ttu-id="54420-140">Devuelve el nombre para mostrar del dispositivo en el miembro **lpszServiceInstanceName** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada llamada a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="54420-140">Return the display name of the device in the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="54420-141">Esta marca también se debe especificar para recuperar el miembro **Name** de la estructura de [**\_ \_ información del dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) al especificar la marca **LUP \_ Return \_ BLOB** .</span><span class="sxs-lookup"><span data-stu-id="54420-141">This flag must also be specified to retrieve the **name** member of the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure when specifying the **LUP\_RETURN\_BLOB** flag.</span></span> |
| <span data-ttu-id="54420-142">LUP \_ devolver \_ dirección</span><span class="sxs-lookup"><span data-stu-id="54420-142">LUP\_RETURN\_ADDR</span></span>  | <span data-ttu-id="54420-143">Devuelve una [**estructura \_ SOCKADDR BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) que contiene la dirección de 48 bits del elemento del mismo nivel en el miembro **LpcsaBuffer** de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para cada llamada a la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="54420-143">Return a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure that contains the 48-bit address of the peer in the **lpcsaBuffer** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="54420-144">Otros miembros de la estructura **SOCKADDR \_ BTH** estarán vacíos.</span><span class="sxs-lookup"><span data-stu-id="54420-144">Other members in the **SOCKADDR\_BTH** structure will be empty.</span></span>                                                            |
| <span data-ttu-id="54420-145">LUP \_ devolver \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="54420-145">LUP\_RETURN\_BLOB</span></span>  | <span data-ttu-id="54420-146">Devuelve la estructura de [**\_ \_ información del dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) en cada llamada subsiguiente a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="54420-146">Return the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure on each subsequent call to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="54420-147">LUP \_ FLUSHPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="54420-147">LUP\_FLUSHPREVIOUS</span></span> | <span data-ttu-id="54420-148">Omitir el siguiente dispositivo disponible y devolver el dispositivo que le sigue.</span><span class="sxs-lookup"><span data-stu-id="54420-148">Skip the next available device, and return the device that follows it.</span></span>                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="54420-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54420-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54420-150">Bluetooth y WSALookupServiceBegin para la detección de servicios</span><span class="sxs-lookup"><span data-stu-id="54420-150">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="54420-151">Bluetooth y WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="54420-151">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="54420-152">Bluetooth y WSAQUERYSET para la consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="54420-152">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="54420-153">Detección de dispositivos y servicios Bluetooth</span><span class="sxs-lookup"><span data-stu-id="54420-153">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="54420-154">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="54420-154">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="54420-155">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="54420-155">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="54420-156">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="54420-156">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="54420-157">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="54420-157">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="54420-158">**\_dispositivo de consulta de BTH \_**</span><span class="sxs-lookup"><span data-stu-id="54420-158">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="54420-159">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="54420-159">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="54420-160">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="54420-160">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="54420-161">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="54420-161">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
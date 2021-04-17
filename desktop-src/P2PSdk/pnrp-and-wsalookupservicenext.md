---
description: PNRP usa la función WSALookupServiceNext para hacer coincidir las consultas especificadas en una llamada anterior a WSALookupServiceBegin.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP y WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667396"
---
# <a name="pnrp-and-wsalookupservicenext"></a><span data-ttu-id="5619c-103">PNRP y WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="5619c-103">PNRP and WSALookupServiceNext</span></span>

<span data-ttu-id="5619c-104">PNRP usa la función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para hacer coincidir las consultas especificadas en una llamada anterior a **WSALookupServiceBegin**.</span><span class="sxs-lookup"><span data-stu-id="5619c-104">PNRP uses the [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function to match queries specified in a previous call to **WSALookupServiceBegin**.</span></span> <span data-ttu-id="5619c-105">Los resultados de la función **WSALookupServiceNext** se determinan mediante la configuración de la estructura **WSAQUERYSET** pasada en la llamada de función **WSALookupServiceBegin** inicial.</span><span class="sxs-lookup"><span data-stu-id="5619c-105">The results of the **WSALookupServiceNext** function are determined by settings in the **WSAQUERYSET** structure passed in the initial **WSALookupServiceBegin** function call.</span></span> <span data-ttu-id="5619c-106">Esta función se usa para realizar las dos funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="5619c-106">This function is used to perform the following two functions:</span></span>

-   <span data-ttu-id="5619c-107">Resolver un nombre de mismo nivel en una lista de direcciones</span><span class="sxs-lookup"><span data-stu-id="5619c-107">Resolving a peer name to a list of addresses</span></span>
-   <span data-ttu-id="5619c-108">Enumerar nubes de red</span><span class="sxs-lookup"><span data-stu-id="5619c-108">Enumerating network clouds</span></span>

<span data-ttu-id="5619c-109">Mediante el uso de [**WSANSPIoctl**](winsock-nsp-reference-links.md), el servicio de búsqueda se puede usar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5619c-109">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="5619c-110">Para obtener información sobre el uso de las funciones del servicio de búsqueda de forma asincrónica, vea [PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="5619c-110">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="5619c-111">La función [**WSALookupServiceNext**](winsock-nsp-reference-links.md) se bloquea incluso si se llama a **WSANSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5619c-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="5619c-112">Antes de llamar a **WSALookupServiceNext**, una aplicación debe esperar hasta que reciba una notificación, si el bloqueo es un problema.</span><span class="sxs-lookup"><span data-stu-id="5619c-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a><span data-ttu-id="5619c-113">Resolver un nombre de mismo nivel en una lista de direcciones</span><span class="sxs-lookup"><span data-stu-id="5619c-113">Resolving a Peer Name to a List of Addresses</span></span>

<span data-ttu-id="5619c-114">Al resolver un nombre de mismo nivel en una lista de direcciones, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) devuelta en el parámetro *lpqsResults* contiene los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5619c-114">When resolving a peer name to a list of addresses, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5619c-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="5619c-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-116">Devuelve el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5619c-116">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="5619c-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-118">Devuelve un nombre del mismo nivel: si se especifica **LUP \_ \_**, **LUP \_ devolverá \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="5619c-118">Returns a peer name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="5619c-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-120">Devuelve **SVCID \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="5619c-120">Returns **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="5619c-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-122">Devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5619c-122">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="5619c-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-124">Devuelve un Comentario: si se especifica **LUP \_ Return \_ comment**, **LUP \_ Return \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="5619c-124">Returns a comment—if **LUP\_RETURN\_COMMENT**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="5619c-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-126">Devuelve **\_ PNRPNAME NS**.</span><span class="sxs-lookup"><span data-stu-id="5619c-126">Returns **NS\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="5619c-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-128">Devuelve **el \_ proveedor NS \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="5619c-128">Returns **NS\_PROVIDER\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="5619c-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-130">Devuelve el nombre de la nube si se especifica **LUP \_ Return \_ Name**, **LUP \_ Return \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="5619c-130">Returns the cloud name if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="5619c-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-132">Devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="5619c-132">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5619c-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="5619c-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-134">Devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5619c-134">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="5619c-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-136">Devuelve el número de entradas de la matriz de información de CSADDR \_ si **LUP \_ devuelve \_ addr**, **LUP \_ devuelve \_ All** o se especifica **null** .</span><span class="sxs-lookup"><span data-stu-id="5619c-136">Returns the number of entries in the CSADDR\_INFO array if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="5619c-137">Este valor y la información de **lpcsaBuffer** son los bits clave de la información que se devuelve en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="5619c-137">This value and the information in **lpcsaBuffer** are the key bits of information returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="5619c-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-139">Devuelve un puntero a una matriz de \_ estructuras de información CSADDR si **LUP \_ devuelve \_ addr**, **LUP \_ devuelve \_ All** o se especifica **null** .</span><span class="sxs-lookup"><span data-stu-id="5619c-139">Returns a pointer to an array of CSADDR\_INFO structures if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="5619c-140">Este búfer y el valor de **dwNumberOfCsAddrs** son los bits de información clave devueltos en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="5619c-140">This buffer and the value in **dwNumberOfCsAddrs** are the key information bits returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="5619c-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-142">Devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="5619c-142">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5619c-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="5619c-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-144">Devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5619c-144">Returns **NULL**.</span></span>

</dd> </dl>

## <a name="enumerating-network-clouds"></a><span data-ttu-id="5619c-145">Enumerar nubes de red</span><span class="sxs-lookup"><span data-stu-id="5619c-145">Enumerating Network Clouds</span></span>

<span data-ttu-id="5619c-146">Al enumerar las nubes, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) devuelta en el parámetro *lpqsResults* contiene los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5619c-146">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5619c-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="5619c-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-148">Devuelve el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5619c-148">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="5619c-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-150">Devuelve un nombre de nube: si se especifica **\_ \_ el nombre de retorno LUP**, **LUP \_ devuelve \_ All** o **null** .</span><span class="sxs-lookup"><span data-stu-id="5619c-150">Returns a cloud name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="5619c-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-152">Devuelve **SVCID \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="5619c-152">Returns **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="5619c-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-154">Devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5619c-154">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="5619c-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-156">Devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5619c-156">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="5619c-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-158">Devuelve **\_ PNRPCLOUD NS**.</span><span class="sxs-lookup"><span data-stu-id="5619c-158">Returns **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="5619c-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-160">Devuelve **el \_ proveedor NS \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="5619c-160">Returns **NS\_PROVIDER\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="5619c-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-162">Devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5619c-162">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="5619c-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-164">Devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="5619c-164">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5619c-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="5619c-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-166">Devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5619c-166">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="5619c-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-168">Devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="5619c-168">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5619c-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="5619c-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-170">Devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="5619c-170">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="5619c-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-172">Devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="5619c-172">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="5619c-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="5619c-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-174">Devuelve un puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) que apunta a una estructura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) : Si **LUP \_ devuelve \_ BLOB**, **LUP \_ devuelve \_ All** o se especifica **null** .</span><span class="sxs-lookup"><span data-stu-id="5619c-174">Returns a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure—if **LUP\_RETURN\_BLOB**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a><span data-ttu-id="5619c-175">Estructura PNRPCLOUDINFO</span><span class="sxs-lookup"><span data-stu-id="5619c-175">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="5619c-176">Al enumerar los nombres de nube, se devuelven los siguientes valores en la estructura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :</span><span class="sxs-lookup"><span data-stu-id="5619c-176">When enumerating cloud names, the following values are returned in the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure:</span></span>

<dl> <dt>

<span data-ttu-id="5619c-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="5619c-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-178">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="5619c-178">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Administración**</span><span class="sxs-lookup"><span data-stu-id="5619c-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-180">Valor real de la nube.</span><span class="sxs-lookup"><span data-stu-id="5619c-180">The actual cloud value.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span><span class="sxs-lookup"><span data-stu-id="5619c-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-182">Estado actual de una nube.</span><span class="sxs-lookup"><span data-stu-id="5619c-182">The current state of a cloud.</span></span> <span data-ttu-id="5619c-183">[**PNRP \_ \_Estado de nube**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) especifica los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="5619c-183">[**PNRP\_CLOUD\_STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifies the valid values.</span></span>

</dd> <dt>

<span data-ttu-id="5619c-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span><span class="sxs-lookup"><span data-stu-id="5619c-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5619c-185">Indica que un nombre de nube es válido en una red o solo es válido en un equipo actual.</span><span class="sxs-lookup"><span data-stu-id="5619c-185">Indicates that a cloud name is valid on a network, or only valid on a current computer.</span></span> <span data-ttu-id="5619c-186">[**PNRP \_ \_Marcas de nube**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) especifica los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="5619c-186">[**PNRP\_CLOUD\_FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifies the valid values.</span></span> <span data-ttu-id="5619c-187">Algunos nombres de nube son válidos en cualquier equipo de la misma red.</span><span class="sxs-lookup"><span data-stu-id="5619c-187">Some cloud names are valid on any computer on the same network.</span></span> <span data-ttu-id="5619c-188">Otros nombres de nube solo son válidos en un equipo actual y solo pueden ser válidos durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5619c-188">Other cloud names are valid only on a current computer, and may be valid only for a period of time.</span></span>

-   <span data-ttu-id="5619c-189">Si **enCloudFlags** se establece en **PNRP \_ Cloud \_ name \_ local,** el nombre solo es válido de forma local.</span><span class="sxs-lookup"><span data-stu-id="5619c-189">If **enCloudFlags** is set to **PNRP\_CLOUD\_NAME\_LOCAL,** the name is only valid locally.</span></span>
-   <span data-ttu-id="5619c-190">Si no se establece **enCloudFlags** , el nombre de la nube se puede transferir a otros equipos.</span><span class="sxs-lookup"><span data-stu-id="5619c-190">If **enCloudFlags** is not set, then the cloud name can be transferred to other computers.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="5619c-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5619c-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5619c-192">PNRP y BLOB</span><span class="sxs-lookup"><span data-stu-id="5619c-192">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="5619c-193">PNRP y WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="5619c-193">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="5619c-194">PNRP y WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="5619c-194">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="5619c-195">PNRP y WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="5619c-195">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="5619c-196">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="5619c-196">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="5619c-197">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="5619c-197">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="5619c-198">Códigos de error NSP de PNRP</span><span class="sxs-lookup"><span data-stu-id="5619c-198">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="5619c-199">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="5619c-199">**WSALookupServiceBegin**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 




---
description: PNRP usa la función WSALookupServiceBegin para iniciar el proceso que permite que una aplicación realice lo siguiente.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP y WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105670209"
---
# <a name="pnrp-and-wsalookupservicebegin"></a><span data-ttu-id="bb86e-103">PNRP y WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="bb86e-103">PNRP and WSALookupServiceBegin</span></span>

<span data-ttu-id="bb86e-104">PNRP usa la función [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para iniciar el proceso que permite a una aplicación realizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bb86e-104">PNRP uses the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function to start the process that allows an application to do the following:</span></span>

-   [<span data-ttu-id="bb86e-105">Resolver un nombre</span><span class="sxs-lookup"><span data-stu-id="bb86e-105">Resolving a name</span></span>](#resolving-a-name)
-   [<span data-ttu-id="bb86e-106">Enumerar nubes de red</span><span class="sxs-lookup"><span data-stu-id="bb86e-106">Enumerating network clouds</span></span>](#enumerating-network-clouds)

<span data-ttu-id="bb86e-107">Los clientes que intentan realizar una de las funciones usan las funciones [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** y **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="bb86e-107">Clients that attempt to perform one of the functions use the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span>

<span data-ttu-id="bb86e-108">Mediante el uso de [**WSANSPIoctl**](winsock-nsp-reference-links.md), el servicio de búsqueda se puede usar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bb86e-108">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="bb86e-109">Para obtener información sobre el uso de las funciones del servicio de búsqueda de forma asincrónica, vea [PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="bb86e-109">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="bb86e-110">El proceso para trabajar con nombres del mismo nivel es diferente de trabajar con nubes.</span><span class="sxs-lookup"><span data-stu-id="bb86e-110">The process for working with peer names is different from working with clouds.</span></span> <span data-ttu-id="bb86e-111">Cada proceso se describe por separado en este tema.</span><span class="sxs-lookup"><span data-stu-id="bb86e-111">Each process is described separately in this topic.</span></span>

## <a name="resolving-a-name"></a><span data-ttu-id="bb86e-112">Resolver un nombre</span><span class="sxs-lookup"><span data-stu-id="bb86e-112">Resolving a Name</span></span>

<span data-ttu-id="bb86e-113">Una aplicación utiliza [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para obtener la dirección IP, el puerto y el protocolo para un servicio del mismo nivel registrado en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="bb86e-113">An application uses [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) to obtain the IP address, port, and protocol for a peer service that is registered on another computer.</span></span> <span data-ttu-id="bb86e-114">La función **WSALookupServiceBegin** se usa para iniciar el proceso de resolución de nombres y configurar los parámetros y las restricciones.</span><span class="sxs-lookup"><span data-stu-id="bb86e-114">The **WSALookupServiceBegin** function is used to start the name resolution process, and set up the parameters and restrictions.</span></span> <span data-ttu-id="bb86e-115">Se devuelve un identificador y se debe usar al llamar a **WSALookupServiceNext** y **WSANSPIoctl**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-115">A handle is returned, and must be used when calling **WSALookupServiceNext** and **WSANSPIoctl**.</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="bb86e-116">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="bb86e-116">lpqsRestrictions</span></span>

<span data-ttu-id="bb86e-117">Al resolver un nombre del mismo nivel, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRestrictions* debe contener los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="bb86e-117">When resolving a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bb86e-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="bb86e-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-119">Especifica el tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="bb86e-119">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="bb86e-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-121">Especifica el nombre del mismo nivel que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="bb86e-121">Specifies a peer name to resolve.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="bb86e-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-123">Debe ser **SVCID \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-123">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="bb86e-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-125">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-125">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="bb86e-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-127">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-127">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="bb86e-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-129">Debe ser **NS \_ PNRPNAME** o **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-129">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="bb86e-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-131">Debe ser un **\_ proveedor NS \_ PNRPNAME** o **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-131">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="bb86e-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-133">Debe ser un nombre de nube, una cadena vacía o **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-133">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="bb86e-134">Si este valor es **null** o una cadena vacía, se usa la nube predeterminada, "global \_ ".</span><span class="sxs-lookup"><span data-stu-id="bb86e-134">If this value is **NULL** or an empty string, the default cloud, "Global\_" is used.</span></span> <span data-ttu-id="bb86e-135">De lo contrario, debe apuntar a un nombre de nube válido.</span><span class="sxs-lookup"><span data-stu-id="bb86e-135">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="bb86e-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-137">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-137">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="bb86e-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-139">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-139">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="bb86e-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-141">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-141">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="bb86e-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-143">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-143">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="bb86e-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-145">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-145">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="bb86e-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-147">Debe ser un puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-147">Must be either a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure or **NULL**.</span></span> <span data-ttu-id="bb86e-148">Si es **null**, se usan los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="bb86e-148">If it is **NULL**, default values are used.</span></span> <span data-ttu-id="bb86e-149">Si se establece, **lpBlob** apunta a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) y se deben establecer los parámetros específicos de la estructura **PNRPINFO** .</span><span class="sxs-lookup"><span data-stu-id="bb86e-149">If it is set, **lpBlob** points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure, and specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="bb86e-150">Para obtener más información, vea las siguientes descripciones de la estructura PNRPINFO.</span><span class="sxs-lookup"><span data-stu-id="bb86e-150">For more information, see the following descriptions for the PNRPINFO Structure.</span></span>

</dd> </dl>

<span data-ttu-id="bb86e-151">Estructura PNRPINFO</span><span class="sxs-lookup"><span data-stu-id="bb86e-151">PNRPINFO Structure</span></span>

<span data-ttu-id="bb86e-152">Si se establece el miembro **lpBlob** de la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) , se deben establecer los siguientes miembros de la estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :</span><span class="sxs-lookup"><span data-stu-id="bb86e-152">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="bb86e-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="bb86e-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-154">Especifica el tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="bb86e-154">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="bb86e-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-156">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-156">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="bb86e-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-158">Especifica el número solicitado de resoluciones.</span><span class="sxs-lookup"><span data-stu-id="bb86e-158">Specifies the requested number of resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="bb86e-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-160">Especifica el período de tiempo de espera solicitado para la espera de respuestas.</span><span class="sxs-lookup"><span data-stu-id="bb86e-160">Specifies the requested timeout period to wait for responses.</span></span> <span data-ttu-id="bb86e-161">El valor predeterminado es 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="bb86e-161">The default is 30 seconds.</span></span> <span data-ttu-id="bb86e-162">El máximo es de 600 segundos (10 minutos).</span><span class="sxs-lookup"><span data-stu-id="bb86e-162">The maximum is 600 seconds (10 minutes).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="bb86e-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-164">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-164">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="bb86e-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-166">Debe ser uno de los valores permitidos.</span><span class="sxs-lookup"><span data-stu-id="bb86e-166">Must be one of the allowed values.</span></span> <span data-ttu-id="bb86e-167">El valor predeterminado es **PNRP \_ resolver \_ criterios \_ no \_ actual \_ \_ \_ nombre del mismo nivel**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-167">The default is **PNRP\_RESOLVE\_CRITERIA\_NON\_CURRENT\_PROCESS\_PEER\_NAME**.</span></span> <span data-ttu-id="bb86e-168">Los valores válidos se especifican mediante los [**\_ \_ criterios de resolución de PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span><span class="sxs-lookup"><span data-stu-id="bb86e-168">Valid values are specified by [**PNRP\_RESOLVE\_CRITERIA**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="bb86e-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-170">Debe ser cero (0) o una **\_ sugerencia PNRPINFO**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-170">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="bb86e-171">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-171">The default is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span><span class="sxs-lookup"><span data-stu-id="bb86e-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-173">Especifica la dirección IP de la sugerencia.</span><span class="sxs-lookup"><span data-stu-id="bb86e-173">Specifies the IP address for the hint.</span></span> <span data-ttu-id="bb86e-174">La sugerencia se usa al intentar buscar el nombre del mismo nivel más cercano.</span><span class="sxs-lookup"><span data-stu-id="bb86e-174">The hint is used when attempting to find the nearest peer name.</span></span> <span data-ttu-id="bb86e-175">El formato de la sugerencia es una dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="bb86e-175">The format of the hint is an IPv6 address.</span></span> <span data-ttu-id="bb86e-176">Si no se especifica **saHint** al buscar el nombre del mismo nivel más cercano, se usa en su lugar una dirección IPv6 del equipo local.</span><span class="sxs-lookup"><span data-stu-id="bb86e-176">If **saHint** is not specified when finding the closest peer name, then an IPv6 address of the local computer is used instead.</span></span> <span data-ttu-id="bb86e-177">Este miembro se omite si **dwFlags** no está establecido.</span><span class="sxs-lookup"><span data-stu-id="bb86e-177">This member is ignored if **dwFlags** is not set.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span><span class="sxs-lookup"><span data-stu-id="bb86e-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-179">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-179">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="bb86e-180">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="bb86e-180">dwControlFlags</span></span>

<span data-ttu-id="bb86e-181">\_PNRP admite las siguientes marcas devueltas de LUP \_ \* :</span><span class="sxs-lookup"><span data-stu-id="bb86e-181">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="bb86e-182">Value</span><span class="sxs-lookup"><span data-stu-id="bb86e-182">Value</span></span>                | <span data-ttu-id="bb86e-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb86e-183">Description</span></span>                                |
|----------------------|--------------------------------------------|
| <span data-ttu-id="bb86e-184">\_nombre devuelto de LUP \_</span><span class="sxs-lookup"><span data-stu-id="bb86e-184">LUP\_RETURN\_NAME</span></span>    | <span data-ttu-id="bb86e-185">Devuelve un nombre y un contexto.</span><span class="sxs-lookup"><span data-stu-id="bb86e-185">Returns a name and context.</span></span>                |
| <span data-ttu-id="bb86e-186">LUP \_ Comentario devuelto \_</span><span class="sxs-lookup"><span data-stu-id="bb86e-186">LUP\_RETURN\_COMMENT</span></span> | <span data-ttu-id="bb86e-187">Devuelve un comentario asociado a un nombre.</span><span class="sxs-lookup"><span data-stu-id="bb86e-187">Returns a comment associated with a name.</span></span>  |
| <span data-ttu-id="bb86e-188">LUP \_ devolver \_ dirección</span><span class="sxs-lookup"><span data-stu-id="bb86e-188">LUP\_RETURN\_ADDR</span></span>    | <span data-ttu-id="bb86e-189">Devuelve una dirección asociada a un nombre.</span><span class="sxs-lookup"><span data-stu-id="bb86e-189">Returns an address associated with a name.</span></span> |



 

## <a name="enumerating-network-clouds"></a><span data-ttu-id="bb86e-190">Enumerar nubes de red</span><span class="sxs-lookup"><span data-stu-id="bb86e-190">Enumerating Network Clouds</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="bb86e-191">lpqsRestrictions</span><span class="sxs-lookup"><span data-stu-id="bb86e-191">lpqsRestrictions</span></span>

<span data-ttu-id="bb86e-192">Al enumerar las nubes, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRestrictions* debe contener los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="bb86e-192">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bb86e-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="bb86e-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-194">Especifica el tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="bb86e-194">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="bb86e-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-196">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-196">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="bb86e-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-198">Debe ser **SVCID \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-198">Must be **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="bb86e-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-200">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-200">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="bb86e-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-202">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-202">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="bb86e-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-204">Debe ser **NS \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-204">Must be **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="bb86e-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-206">Debe ser un **\_ proveedor NS \_ PNRPCLOUD** o **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-206">Must be either **NS\_PROVIDER\_PNRPCLOUD** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="bb86e-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-208">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-208">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="bb86e-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-210">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-210">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="bb86e-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-212">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-212">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="bb86e-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-214">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-214">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="bb86e-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-216">Reserved, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-216">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="bb86e-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-218">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-218">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="bb86e-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-220">Puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) que apunta a una estructura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) .</span><span class="sxs-lookup"><span data-stu-id="bb86e-220">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure.</span></span> <span data-ttu-id="bb86e-221">Si **lpBlob** es **null**, se enumeran todas las nubes.</span><span class="sxs-lookup"><span data-stu-id="bb86e-221">If **lpBlob** is **NULL**, all clouds are enumerated.</span></span>

</dd> </dl>

<span data-ttu-id="bb86e-222">Estructura PNRPCLOUDINFO</span><span class="sxs-lookup"><span data-stu-id="bb86e-222">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="bb86e-223">Al enumerar nubes, se deben establecer los siguientes miembros de la estructura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :</span><span class="sxs-lookup"><span data-stu-id="bb86e-223">When enumerating clouds, the following members of the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="bb86e-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="bb86e-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-225">Especifica el tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="bb86e-225">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Administración**</span><span class="sxs-lookup"><span data-stu-id="bb86e-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-227">Apunta a una estructura que especifica los criterios que se pueden usar para filtrar los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bb86e-227">Points to a structure that specifies criteria that you can use to filter search results.</span></span> <span data-ttu-id="bb86e-228">El **miembro Cloud. Scope** puede ser **el \_ ámbito \_ PNRP any**, el **\_ \_ ámbito global PNRP**, el **\_ \_ \_ ámbito local del sitio PNRP** o el **\_ \_ \_ ámbito local del vínculo PNRP**.</span><span class="sxs-lookup"><span data-stu-id="bb86e-228">The **Cloud.Scope** member can be **PNRP\_SCOPE\_ANY**, **PNRP\_GLOBAL\_SCOPE**, **PNRP\_SITE\_LOCAL\_SCOPE**, or **PNRP\_LINK\_LOCAL\_SCOPE**.</span></span> <span data-ttu-id="bb86e-229">Si se especifica el **\_ ámbito PNRP \_ any** , se devuelven todas las nubes.</span><span class="sxs-lookup"><span data-stu-id="bb86e-229">If **PNRP\_SCOPE\_ANY** is specified, all clouds are returned.</span></span> <span data-ttu-id="bb86e-230">De lo contrario, solo se devuelven las nubes que coinciden con la **nube. el ámbito** .</span><span class="sxs-lookup"><span data-stu-id="bb86e-230">Otherwise, only clouds that match the **Cloud.Scope** are returned.</span></span>

</dd> <dt>

<span data-ttu-id="bb86e-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span><span class="sxs-lookup"><span data-stu-id="bb86e-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="bb86e-232">Reserved, debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="bb86e-232">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="bb86e-233">dwControlFlags</span><span class="sxs-lookup"><span data-stu-id="bb86e-233">dwControlFlags</span></span>

<span data-ttu-id="bb86e-234">\_PNRP admite las siguientes marcas devueltas de LUP \_ \* :</span><span class="sxs-lookup"><span data-stu-id="bb86e-234">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="bb86e-235">Value</span><span class="sxs-lookup"><span data-stu-id="bb86e-235">Value</span></span>             | <span data-ttu-id="bb86e-236">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb86e-236">Description</span></span>                                                       |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bb86e-237">\_nombre devuelto de LUP \_</span><span class="sxs-lookup"><span data-stu-id="bb86e-237">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="bb86e-238">Devuelve un nombre y un contexto.</span><span class="sxs-lookup"><span data-stu-id="bb86e-238">Returns a name and context.</span></span>                                       |
| <span data-ttu-id="bb86e-239">LUP \_ devolver \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="bb86e-239">LUP\_RETURN\_BLOB</span></span> | <span data-ttu-id="bb86e-240">Devuelve el [BLOB](pnrp-and-blob.md) asociado a esta nube.</span><span class="sxs-lookup"><span data-stu-id="bb86e-240">Returns the [BLOB](pnrp-and-blob.md) associated with this cloud.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bb86e-241">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bb86e-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb86e-242">PNRP y BLOB</span><span class="sxs-lookup"><span data-stu-id="bb86e-242">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="bb86e-243">PNRP y WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="bb86e-243">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="bb86e-244">PNRP y WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="bb86e-244">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="bb86e-245">PNRP y WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="bb86e-245">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="bb86e-246">PNRP y WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="bb86e-246">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="bb86e-247">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="bb86e-247">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="bb86e-248">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="bb86e-248">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="bb86e-249">Códigos de error NSP de PNRP</span><span class="sxs-lookup"><span data-stu-id="bb86e-249">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 




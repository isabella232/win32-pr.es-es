---
description: PNRP usa la función WSASetService para registrar o quitar nombres de mismo nivel.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP y WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667389"
---
# <a name="pnrp-and-wsasetservice"></a><span data-ttu-id="c16bf-103">PNRP y WSASetService</span><span class="sxs-lookup"><span data-stu-id="c16bf-103">PNRP and WSASetService</span></span>

<span data-ttu-id="c16bf-104">PNRP usa la función [**WSASetService**](winsock-nsp-reference-links.md) para registrar o quitar [nombres de mismo nivel](peer-names.md).</span><span class="sxs-lookup"><span data-stu-id="c16bf-104">PNRP uses the [**WSASetService**](winsock-nsp-reference-links.md) function to register or remove [peer names](peer-names.md).</span></span>

## <a name="registering-a-name"></a><span data-ttu-id="c16bf-105">Registrar un nombre</span><span class="sxs-lookup"><span data-stu-id="c16bf-105">Registering a Name</span></span>

<span data-ttu-id="c16bf-106">El registro incluye un nombre del mismo nivel y un conjunto de puntos de conexión en los que se puede establecer contacto con un servicio.</span><span class="sxs-lookup"><span data-stu-id="c16bf-106">Registration includes a peer name and set of endpoints where a service can be contacted.</span></span> <span data-ttu-id="c16bf-107">Un registro es específico de una nube PNRP.</span><span class="sxs-lookup"><span data-stu-id="c16bf-107">A registration is specific to a PNRP cloud.</span></span> <span data-ttu-id="c16bf-108">Una vez registrado un elemento del mismo nivel, se produce un retraso entre el registro y la propagación de la información de registro a otros nodos.</span><span class="sxs-lookup"><span data-stu-id="c16bf-108">After a peer is registered, there is a delay between the registration and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="c16bf-109">Durante este tiempo, es posible que otros nodos no puedan resolver un elemento del mismo nivel registrado recientemente.</span><span class="sxs-lookup"><span data-stu-id="c16bf-109">During this time, other nodes may not be able to resolve a newly registered peer.</span></span>

<span data-ttu-id="c16bf-110">El registro del servicio no es persistente.</span><span class="sxs-lookup"><span data-stu-id="c16bf-110">Service registration is not persistent.</span></span>

-   <span data-ttu-id="c16bf-111">Si un proceso de cliente que registra un nombre del mismo nivel sale o llama a [**WSACleanup**](winsock-nsp-reference-links.md), se anula el registro del nombre del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="c16bf-111">If a client process that registers a peer name exits or calls [**WSACleanup**](winsock-nsp-reference-links.md), then the peer name is unregistered.</span></span>
-   <span data-ttu-id="c16bf-112">Si el proceso actual ya ha registrado un nombre de mismo nivel especificado en la misma nube, se reemplaza con nuevos valores de registro.</span><span class="sxs-lookup"><span data-stu-id="c16bf-112">If a specified peer name is already registered in the same cloud by the current process, it is replaced with new registration values.</span></span>

<span data-ttu-id="c16bf-113">Al registrar un nombre del mismo nivel, se deben indicar los siguientes valores de parámetro:</span><span class="sxs-lookup"><span data-stu-id="c16bf-113">When registering a peer name, the following parameter values must be indicated:</span></span>

-   <span data-ttu-id="c16bf-114">el parámetro *essOperation* debe tener un valor de **RNRSERVICE \_ Register**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-114">*essOperation* parameter must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="c16bf-115">el parámetro *dwControlFlags* debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-115">*dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="c16bf-116">Al registrar un nombre del mismo nivel, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRegInfo* debe contener los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c16bf-116">When registering a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure referenced by the *lpqsRegInfo* parameter must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c16bf-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="c16bf-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-118">Especifica el tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="c16bf-118">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="c16bf-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-120">Especifica un nombre del mismo nivel que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="c16bf-120">Specifies a peer name to register.</span></span> <span data-ttu-id="c16bf-121">Si el [nombre del mismo nivel](peer-names.md) no es seguro, la identidad es opcional.</span><span class="sxs-lookup"><span data-stu-id="c16bf-121">If the [peer name](peer-names.md) is unsecured, then the identity is optional.</span></span> <span data-ttu-id="c16bf-122">Si la identidad se especifica como **null**, PNRP usa la identidad local de la máquina, de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c16bf-122">If the identity is specified as **NULL**, PNRP uses the machine local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="c16bf-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-124">Debe ser SVCID \_ PNRPNAME.</span><span class="sxs-lookup"><span data-stu-id="c16bf-124">Must be SVCID\_PNRPNAME.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="c16bf-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-126">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-126">Ignored.</span></span> <span data-ttu-id="c16bf-127">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="c16bf-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-129">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-129">Ignored.</span></span> <span data-ttu-id="c16bf-130">Sin embargo, sigue siendo necesario que la cadena tenga menos de 40 caracteres, incluido el terminador **null** .</span><span class="sxs-lookup"><span data-stu-id="c16bf-130">However, the string is still required to be fewer than 40 characters, including the **NULL** terminator.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="c16bf-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-132">Debe ser **NS \_ PNRPNAME** o **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-132">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="c16bf-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-134">Debe ser un **\_ proveedor NS \_ PNRPNAME** o **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-134">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="c16bf-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-136">Debe ser un nombre de nube, una cadena vacía o **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-136">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="c16bf-137">Si este valor es **null** o una cadena vacía, se usa la nube predeterminada, "global".</span><span class="sxs-lookup"><span data-stu-id="c16bf-137">If this value is **NULL** or an empty string, the default cloud, "Global", is used.</span></span> <span data-ttu-id="c16bf-138">De lo contrario, debe apuntar a un nombre de nube válido.</span><span class="sxs-lookup"><span data-stu-id="c16bf-138">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="c16bf-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-140">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-140">Ignored.</span></span> <span data-ttu-id="c16bf-141">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-141">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="c16bf-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-143">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-143">Ignored.</span></span> <span data-ttu-id="c16bf-144">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-144">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="c16bf-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-146">Especifica el número de direcciones registradas por un servicio.</span><span class="sxs-lookup"><span data-stu-id="c16bf-146">Specifies the number of addresses registered by a service.</span></span> <span data-ttu-id="c16bf-147">El número máximo de direcciones que se pueden registrar para un único nombre es 10.</span><span class="sxs-lookup"><span data-stu-id="c16bf-147">The maximum number of addresses that can be registered for a single name is 10.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="c16bf-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-149">Puntero a una lista de direcciones que se van a registrar.</span><span class="sxs-lookup"><span data-stu-id="c16bf-149">Pointer to a list of addresses to register.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="c16bf-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-151">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-151">Ignored.</span></span> <span data-ttu-id="c16bf-152">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-152">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="c16bf-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-154">Puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) que apunta a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="c16bf-154">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="c16bf-155">Se deben establecer los parámetros específicos de la estructura **PNRPINFO** .</span><span class="sxs-lookup"><span data-stu-id="c16bf-155">Specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="c16bf-156">Para obtener más información, consulte la siguiente sección de la estructura **PNRPINFO** .</span><span class="sxs-lookup"><span data-stu-id="c16bf-156">For more information, see the following **PNRPINFO** structure section.</span></span>

</dd> </dl>

## <a name="pnrpinfo-structure"></a><span data-ttu-id="c16bf-157">Estructura PNRPINFO</span><span class="sxs-lookup"><span data-stu-id="c16bf-157">PNRPINFO Structure</span></span>

<span data-ttu-id="c16bf-158">Si se establece el miembro **lpBlob** de la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) , se deben establecer los siguientes miembros de la estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) :</span><span class="sxs-lookup"><span data-stu-id="c16bf-158">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="c16bf-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="c16bf-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-160">Especifica el tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="c16bf-160">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span><span class="sxs-lookup"><span data-stu-id="c16bf-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-162">Especifica la identidad del nombre del mismo nivel que se crea mediante [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="c16bf-162">Specifies the identity of the peer name that is created by using [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span> <span data-ttu-id="c16bf-163">Si un nombre del mismo nivel no es seguro, la identidad es opcional.</span><span class="sxs-lookup"><span data-stu-id="c16bf-163">If a peer name is unsecured, then the identity is optional.</span></span> <span data-ttu-id="c16bf-164">Si la identidad se especifica como **null**, PNRP usa la identidad local del equipo, de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c16bf-164">If the identity is specified as **NULL**, PNRP uses the computer local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span><span class="sxs-lookup"><span data-stu-id="c16bf-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-166">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-166">Ignored.</span></span> <span data-ttu-id="c16bf-167">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-167">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span><span class="sxs-lookup"><span data-stu-id="c16bf-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-169">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-169">Ignored.</span></span> <span data-ttu-id="c16bf-170">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-170">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span><span class="sxs-lookup"><span data-stu-id="c16bf-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-172">Especifica el número de segundos entre las operaciones de actualización.</span><span class="sxs-lookup"><span data-stu-id="c16bf-172">Specifies the number of seconds between refresh operations.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span><span class="sxs-lookup"><span data-stu-id="c16bf-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-174">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-174">Ignored.</span></span> <span data-ttu-id="c16bf-175">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-175">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="c16bf-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-177">Debe ser cero (0) o una **\_ sugerencia PNRPINFO**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-177">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="c16bf-178">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-178">The default is zero (0).</span></span> <span data-ttu-id="c16bf-179">Esto significa que la parte de la ubicación del servicio del identificador PNRP se genera mediante la dirección IP de **saHint**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-179">This means that the service location portion of the PNRP ID is built by using the IP address in **saHint**.</span></span> <span data-ttu-id="c16bf-180">De lo contrario, la ubicación del servicio se genera con la primera dirección IP en la primera entrada IPv6 del miembro **lpcsaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="c16bf-180">Otherwise, the service location is built by using the first IP address in the first IPv6 entry of the **lpcsaBuffer** member.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span><span class="sxs-lookup"><span data-stu-id="c16bf-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-182">Especifica la dirección IPv6 de la sugerencia.</span><span class="sxs-lookup"><span data-stu-id="c16bf-182">Specifies the IPv6 address for the hint.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span><span class="sxs-lookup"><span data-stu-id="c16bf-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-184">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-184">Ignored.</span></span> <span data-ttu-id="c16bf-185">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-185">Set to zero (0).</span></span>

</dd> </dl>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="c16bf-186">Anular el registro de un nombre de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="c16bf-186">Unregistering a Peer Name</span></span>

<span data-ttu-id="c16bf-187">La lista siguiente identifica la información importante sobre cómo anular el registro de un nombre de mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="c16bf-187">The following list identifies the important information about unregistering a peer name.</span></span>

-   <span data-ttu-id="c16bf-188">Solo una aplicación que registra un nombre del mismo nivel puede anular su registro.</span><span class="sxs-lookup"><span data-stu-id="c16bf-188">Only an application that registers a peer name can unregister it.</span></span>
-   <span data-ttu-id="c16bf-189">Un nombre del mismo nivel no se registra automáticamente si se llama a [**WSACleanup**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="c16bf-189">A peer name is unregistered automatically if [**WSACleanup**](winsock-nsp-reference-links.md) is called.</span></span>
-   <span data-ttu-id="c16bf-190">PNRP siempre quita el registro del nombre de servicio completo.</span><span class="sxs-lookup"><span data-stu-id="c16bf-190">PNRP always removes the entire service name registration.</span></span> <span data-ttu-id="c16bf-191">No permite la eliminación de direcciones individuales.</span><span class="sxs-lookup"><span data-stu-id="c16bf-191">It does not allow removal of individual addresses.</span></span>
-   <span data-ttu-id="c16bf-192">Al anular el registro de un nombre, el parámetro *essOperation* debe tener un valor de **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-192">When unregistering a name, the *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="c16bf-193">PNRP no admite el valor **RNRSERVICE \_ unregister**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-193">PNRP does not support the value **RNRSERVICE\_DEREGISTER**.</span></span>
-   <span data-ttu-id="c16bf-194">El parámetro *dwControlFlags* debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-194">The *dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="c16bf-195">Al anular el registro de un nombre, la estructura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) a la que hace referencia el parámetro *lpqsRegInfo* debe contener los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c16bf-195">When unregistering a name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRegInfo* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c16bf-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="c16bf-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-197">Especifica el tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="c16bf-197">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="c16bf-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-199">Especifica un nombre del mismo nivel del que se va a anular el registro.</span><span class="sxs-lookup"><span data-stu-id="c16bf-199">Specifies a peer name to unregister.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="c16bf-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-201">Debe ser **SVCID \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-201">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="c16bf-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-203">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-203">Ignored.</span></span> <span data-ttu-id="c16bf-204">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-204">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="c16bf-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-206">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-206">Ignored.</span></span> <span data-ttu-id="c16bf-207">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-207">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="c16bf-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-209">Debe ser **NS \_ PNRPNAME** o **NS \_ All**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-209">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="c16bf-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-211">Debe ser un **\_ proveedor NS \_ PNRPNAME** o **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-211">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="c16bf-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-213">Debe ser un nombre de nube, una cadena vacía o **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-213">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="c16bf-214">Si este valor es **null** o una cadena vacía, se usa la nube predeterminada, "global".</span><span class="sxs-lookup"><span data-stu-id="c16bf-214">If this value is **NULL** or an empty string, the default cloud, "Global" is used.</span></span> <span data-ttu-id="c16bf-215">De lo contrario, debe apuntar a un nombre de nube válido.</span><span class="sxs-lookup"><span data-stu-id="c16bf-215">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="c16bf-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-217">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-217">Ignored.</span></span> <span data-ttu-id="c16bf-218">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-218">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="c16bf-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-220">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-220">Ignored.</span></span> <span data-ttu-id="c16bf-221">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-221">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="c16bf-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-223">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-223">Ignored.</span></span> <span data-ttu-id="c16bf-224">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-224">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="c16bf-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-226">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-226">Ignored.</span></span> <span data-ttu-id="c16bf-227">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="c16bf-227">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="c16bf-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-229">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c16bf-229">Ignored.</span></span> <span data-ttu-id="c16bf-230">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="c16bf-230">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c16bf-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="c16bf-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="c16bf-232">Puntero a una estructura de [**BLOB**](winsock-nsp-reference-links.md) que apunta a una estructura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="c16bf-232">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="c16bf-233">El miembro **lpszIdentity** de la estructura **lpBlob** identifica el nombre de la identidad que se usa para registrar un nombre del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="c16bf-233">The **lpszIdentity** member of the **lpBlob** structure identifies the name of the identity that is used to register a peer name.</span></span> <span data-ttu-id="c16bf-234">Los miembros restantes se deben establecer en los mismos valores que se usan al registrar un nombre.</span><span class="sxs-lookup"><span data-stu-id="c16bf-234">The remaining members must be set to the same values that are used when registering a name.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c16bf-235">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c16bf-235">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c16bf-236">PNRP y BLOB</span><span class="sxs-lookup"><span data-stu-id="c16bf-236">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="c16bf-237">PNRP y WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="c16bf-237">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="c16bf-238">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="c16bf-238">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="c16bf-239">Códigos de error NSP de PNRP</span><span class="sxs-lookup"><span data-stu-id="c16bf-239">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="c16bf-240">**WSACleanup**</span><span class="sxs-lookup"><span data-stu-id="c16bf-240">**WSACleanup**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="c16bf-241">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="c16bf-241">**WSASetService**</span></span>
</dt> </dl>

 

 




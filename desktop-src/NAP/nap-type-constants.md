---
title: Constantes de tipo de NAP (NapTypes. h)
description: Se definen las siguientes constantes de NAP.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676884"
---
# <a name="nap-type-constants"></a><span data-ttu-id="18860-103">Constantes de tipo de NAP</span><span class="sxs-lookup"><span data-stu-id="18860-103">NAP Type Constants</span></span>

> [!Note]  
> <span data-ttu-id="18860-104">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="18860-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="18860-105">Se definen las siguientes constantes de NAP.</span><span class="sxs-lookup"><span data-stu-id="18860-105">The following NAP constants are defined.</span></span>

<span data-ttu-id="18860-106">Las siguientes constantes de NAP se definen en NapTypes. h:</span><span class="sxs-lookup"><span data-stu-id="18860-106">The following NAP constants are defined in NapTypes.h:</span></span>

<dl> <dt>

<span data-ttu-id="18860-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span><span class="sxs-lookup"><span data-stu-id="18860-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-108">0x64</span><span class="sxs-lookup"><span data-stu-id="18860-108">0x64</span></span>
</dt> <dt>



<span data-ttu-id="18860-109">Número máximo de objetos [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) tipo-longitud-valor (TLV) asociados a un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="18860-109">The maximum number of [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) objects associated with an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="18860-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-111">0xFA0</span><span class="sxs-lookup"><span data-stu-id="18860-111">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="18860-112">Tamaño máximo, en bytes, de un objeto [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) asociado a un paquete de informe de mantenimiento ([**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh)).</span><span class="sxs-lookup"><span data-stu-id="18860-112">The maximum size, in bytes, of a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) object associated with a statement of health ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="18860-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-114">0xC</span><span class="sxs-lookup"><span data-stu-id="18860-114">0xC</span></span>
</dt> <dt>



<span data-ttu-id="18860-115">El tamaño mínimo, en bytes, de un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="18860-115">The minimum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="18860-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-117">0xFA0</span><span class="sxs-lookup"><span data-stu-id="18860-117">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="18860-118">El tamaño máximo, en bytes, de un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="18860-118">The maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="18860-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-120">maxSoHAttributeSize/sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="18860-120">maxSoHAttributeSize / sizeof(DWORD)</span></span>
</dt> <dt>



<span data-ttu-id="18860-121">Número máximo de valores DWORD asociados a un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="18860-121">The maximum number of DWORD values associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="18860-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-123">maxSoHAttributeSize/0x4</span><span class="sxs-lookup"><span data-stu-id="18860-123">maxSoHAttributeSize / 0x4</span></span>
</dt> <dt>



<span data-ttu-id="18860-124">Número máximo de direcciones IPv4 asociadas a un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="18860-124">The maximum number of IPv4 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="18860-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-126">maxSoHAttributeSize/0x10</span><span class="sxs-lookup"><span data-stu-id="18860-126">maxSoHAttributeSize / 0x10</span></span>
</dt> <dt>



<span data-ttu-id="18860-127">Número máximo de direcciones IPv6 asociadas a un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span><span class="sxs-lookup"><span data-stu-id="18860-127">The maximum number of IPv6 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span><span class="sxs-lookup"><span data-stu-id="18860-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-129">0x400</span><span class="sxs-lookup"><span data-stu-id="18860-129">0x400</span></span>
</dt> <dt>



<span data-ttu-id="18860-130">La longitud máxima de una cadena especificada por la estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="18860-130">The maximum length of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span><span class="sxs-lookup"><span data-stu-id="18860-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-132">(maxStringLength + 1) \* sizeof (WCHAR)</span><span class="sxs-lookup"><span data-stu-id="18860-132">(maxStringLength + 1) \* sizeof(WCHAR)</span></span>
</dt> <dt>



<span data-ttu-id="18860-133">La longitud máxima, en bytes, de una cadena especificada por la estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="18860-133">The maximum length, in bytes, of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="18860-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-135">0x14</span><span class="sxs-lookup"><span data-stu-id="18860-135">0x14</span></span>
</dt> <dt>



<span data-ttu-id="18860-136">Número máximo de entidades de mantenimiento del sistema, como SHV y Sha.</span><span class="sxs-lookup"><span data-stu-id="18860-136">The maximum number of system health entities, such as SHVs and SHAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="18860-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-138">\[intervalo (0, maxSystemHealthEntityCount)\]</span><span class="sxs-lookup"><span data-stu-id="18860-138">\[range(0, maxSystemHealthEntityCount)\]</span></span> 
</dt> <dt>



<span data-ttu-id="18860-139">El intervalo de valores posibles para el número de entidades de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="18860-139">The range of possible values for the number of system health entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span><span class="sxs-lookup"><span data-stu-id="18860-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-141">0x14</span><span class="sxs-lookup"><span data-stu-id="18860-141">0x14</span></span>
</dt> <dt>



<span data-ttu-id="18860-142">Número máximo de entidades de cumplimiento, como QECs.</span><span class="sxs-lookup"><span data-stu-id="18860-142">The maximum number of enforcement entities, such as QECs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="18860-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-144">\[intervalo (0, maxEnforcerCount)\]</span><span class="sxs-lookup"><span data-stu-id="18860-144">\[range(0, maxEnforcerCount)\]</span></span>
</dt> <dt>



<span data-ttu-id="18860-145">El intervalo de valores posibles para el número de entidades de aplicación.</span><span class="sxs-lookup"><span data-stu-id="18860-145">The range of possible values for the number of enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span><span class="sxs-lookup"><span data-stu-id="18860-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-147">0xC8</span><span class="sxs-lookup"><span data-stu-id="18860-147">0xC8</span></span>
</dt> <dt>



<span data-ttu-id="18860-148">Tamaño máximo, en bytes, de una estructura [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .</span><span class="sxs-lookup"><span data-stu-id="18860-148">The maximum size, in bytes, of a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span><span class="sxs-lookup"><span data-stu-id="18860-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-150">0x14</span><span class="sxs-lookup"><span data-stu-id="18860-150">0x14</span></span>
</dt> <dt>



<span data-ttu-id="18860-151">Número máximo de objetos [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) asociados a una entidad de aplicación.</span><span class="sxs-lookup"><span data-stu-id="18860-151">The maximum number of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) objects associated with an enforcement entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span><span class="sxs-lookup"><span data-stu-id="18860-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span><span class="sxs-lookup"><span data-stu-id="18860-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span></span>
</dt> <dt>



<span data-ttu-id="18860-154">Número máximo de conexiones de SoH almacenadas en caché para todas las entidades de mantenimiento y cumplimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="18860-154">The maximum number of cached SoH connections for all system health and enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="18860-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-156">0x1</span><span class="sxs-lookup"><span data-stu-id="18860-156">0x1</span></span>
</dt> <dt>



<span data-ttu-id="18860-157">Especifica que un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)se debe a una nueva solicitud, no a una solicitud almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="18860-157">Specifies that an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)is due to a new request, not a cached request.</span></span> <span data-ttu-id="18860-158">Este marcador lo usa el agente NAP en un objeto [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="18860-158">This flag is used by the NAP agent on an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span><span class="sxs-lookup"><span data-stu-id="18860-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-160">0x1</span><span class="sxs-lookup"><span data-stu-id="18860-160">0x1</span></span>
</dt> <dt>



<span data-ttu-id="18860-161">Especifica que se requiere corrección.</span><span class="sxs-lookup"><span data-stu-id="18860-161">Specifies that fix-up is required.</span></span> <span data-ttu-id="18860-162">Este marcador lo usa un SHA.</span><span class="sxs-lookup"><span data-stu-id="18860-162">This flag is used by a SHA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span><span class="sxs-lookup"><span data-stu-id="18860-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-164">0X5</span><span class="sxs-lookup"><span data-stu-id="18860-164">0x5</span></span>
</dt> <dt>



<span data-ttu-id="18860-165">Número de categorías de error contenidas dentro de una estructura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="18860-165">The number of failure categories contained within a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span><span class="sxs-lookup"><span data-stu-id="18860-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-167">0x1</span><span class="sxs-lookup"><span data-stu-id="18860-167">0x1</span></span>
</dt> <dt>



<span data-ttu-id="18860-168">El componente es un cliente de cumplimiento de cuarentena (QEC) que envía un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) en banda durante la autenticación de la conexión.</span><span class="sxs-lookup"><span data-stu-id="18860-168">The component is a quarantine enforcement client (QEC) that sends an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet in-band during connection authentication.</span></span>

> [!Note]  
> <span data-ttu-id="18860-169">Los Sha y los SHV no utilizan este valor.</span><span class="sxs-lookup"><span data-stu-id="18860-169">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span><span class="sxs-lookup"><span data-stu-id="18860-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-171">0x2</span><span class="sxs-lookup"><span data-stu-id="18860-171">0x2</span></span>
</dt> <dt>



<span data-ttu-id="18860-172">El componente es un QEC que implementa [**INapCertRelyingParty**](inapcertrelyingparty.md) y debe interactuar con el servidor de certificados de mantenimiento (HCS) para obtener un certificado de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="18860-172">The component is a QEC that implements [**INapCertRelyingParty**](inapcertrelyingparty.md) and must interact with the Health Certificate Server (HCS) in order to obtain a health certificate.</span></span>

> [!Note]  
> <span data-ttu-id="18860-173">Los Sha y los SHV no utilizan este valor.</span><span class="sxs-lookup"><span data-stu-id="18860-173">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> </dl>

<span data-ttu-id="18860-174">Las siguientes constantes de NAP se definen en NapEnforcementClient. h.</span><span class="sxs-lookup"><span data-stu-id="18860-174">The following NAP constants are defined in NapEnforcementClient.h.</span></span>

<dl> <dt>

<span data-ttu-id="18860-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="18860-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-176">0x0FA0</span><span class="sxs-lookup"><span data-stu-id="18860-176">0x0FA0</span></span>
</dt> <dt>



<span data-ttu-id="18860-177">El tamaño máximo predeterminado, en bytes, de un paquete SoH.</span><span class="sxs-lookup"><span data-stu-id="18860-177">The default maximum size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="18860-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-179">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="18860-179">0xFFFF</span></span>
</dt> <dt>



<span data-ttu-id="18860-180">El tamaño máximo posible, en bytes, de un paquete SoH.</span><span class="sxs-lookup"><span data-stu-id="18860-180">The maximum possible size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="18860-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-182">0x012C</span><span class="sxs-lookup"><span data-stu-id="18860-182">0x012C</span></span>
</dt> <dt>



<span data-ttu-id="18860-183">Tamaño máximo posible mínimo, en bytes, de un paquete SoH.</span><span class="sxs-lookup"><span data-stu-id="18860-183">The smallest possible maximum size, in bytes, of an SoH packet.</span></span> <span data-ttu-id="18860-184">El tamaño real del paquete SoH puede ser menor que **minProtocolMaxSize**.</span><span class="sxs-lookup"><span data-stu-id="18860-184">The actual size of the SoH packet may be smaller than **minProtocolMaxSize**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18860-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="18860-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18860-186">Range (minProtocolMaxSize, maxProtocolMaxSize)</span><span class="sxs-lookup"><span data-stu-id="18860-186">range(minProtocolMaxSize, maxProtocolMaxSize)</span></span>
</dt> <dt>



<span data-ttu-id="18860-187">El intervalo de valores posibles para el tamaño máximo de un paquete SoH.</span><span class="sxs-lookup"><span data-stu-id="18860-187">The range of possible values for the maximum size of a SoH packet.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18860-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18860-188">Requirements</span></span>



| <span data-ttu-id="18860-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="18860-189">Requirement</span></span> | <span data-ttu-id="18860-190">Value</span><span class="sxs-lookup"><span data-stu-id="18860-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18860-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18860-191">Minimum supported client</span></span><br/> | <span data-ttu-id="18860-192">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="18860-192">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="18860-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18860-193">Minimum supported server</span></span><br/> | <span data-ttu-id="18860-194">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="18860-194">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="18860-195">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18860-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="18860-196"><dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="18860-196"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18860-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="18860-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18860-198">**Constantes de NAP**</span><span class="sxs-lookup"><span data-stu-id="18860-198">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 






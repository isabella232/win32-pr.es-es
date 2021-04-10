---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_WINSRType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de búsqueda inversa WINS (WINSr).
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c35863e00ace6c0772383604d0fbdfd7915cd02c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150636"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="b4f67-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WINSRType</span><span class="sxs-lookup"><span data-stu-id="b4f67-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="b4f67-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de búsqueda inversa WINS (WINSR).</span><span class="sxs-lookup"><span data-stu-id="b4f67-107">The **CreateInstanceFromPropertyData** method instantiates a WINS Reverse Lookup (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f67-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4f67-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b4f67-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4f67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f67-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="b4f67-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="b4f67-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="b4f67-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="b4f67-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="b4f67-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="b4f67-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="b4f67-117">Class of the RR.</span></span> <span data-ttu-id="b4f67-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="b4f67-118">Default value is 1.</span></span> <span data-ttu-id="b4f67-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="b4f67-119">The following values are valid.</span></span>



| <span data-ttu-id="b4f67-120">Value</span><span class="sxs-lookup"><span data-stu-id="b4f67-120">Value</span></span>                                                                                                | <span data-ttu-id="b4f67-121">Significado</span><span class="sxs-lookup"><span data-stu-id="b4f67-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="b4f67-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b4f67-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="b4f67-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="b4f67-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="b4f67-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b4f67-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="b4f67-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="b4f67-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="b4f67-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="b4f67-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="b4f67-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="b4f67-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="b4f67-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="b4f67-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="b4f67-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="b4f67-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="b4f67-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="b4f67-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b4f67-132">*MappingFlag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-133">Marca de asignación de WINSr que especifica si el registro debe incluirse en la replicación de zona.</span><span class="sxs-lookup"><span data-stu-id="b4f67-133">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="b4f67-134">Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y no replicación (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b4f67-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="b4f67-135">*Tiempodeesperadebúsqueda* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-135">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-136">Tiempo de espera, en segundos, para un servidor DNS que usa la búsqueda inversa de WINS.</span><span class="sxs-lookup"><span data-stu-id="b4f67-136">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="b4f67-137">*CacheTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-137">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-138">Tiempo, en segundos, que un servidor DNS que usa la búsqueda WINS puede almacenar en caché la respuesta del servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="b4f67-138">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="b4f67-139">*ResultDomain* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-139">*ResultDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-140">Nombre de dominio que se va a anexar a los nombres NetBIOS devueltos.</span><span class="sxs-lookup"><span data-stu-id="b4f67-140">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="b4f67-141">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="b4f67-141">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f67-142">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="b4f67-142">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f67-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4f67-143">Return value</span></span>

<span data-ttu-id="b4f67-144">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b4f67-144">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f67-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4f67-145">Requirements</span></span>



| <span data-ttu-id="b4f67-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4f67-146">Requirement</span></span> | <span data-ttu-id="b4f67-147">Value</span><span class="sxs-lookup"><span data-stu-id="b4f67-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f67-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4f67-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f67-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b4f67-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b4f67-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4f67-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f67-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4f67-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b4f67-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4f67-152">Namespace</span></span><br/>                | <span data-ttu-id="b4f67-153">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="b4f67-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b4f67-154">MOF</span><span class="sxs-lookup"><span data-stu-id="b4f67-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4f67-155"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4f67-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4f67-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4f67-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f67-157">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="b4f67-157">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="b4f67-158">**Método Modify de la \_ clase MicrosoftDNS WINSRType**</span><span class="sxs-lookup"><span data-stu-id="b4f67-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="b4f67-159">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="b4f67-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






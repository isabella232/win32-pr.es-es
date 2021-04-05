---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_WINSType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos del servicio de nombres Internet de Windows (WINS).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802834"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="0c7e1-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WINSType</span><span class="sxs-lookup"><span data-stu-id="0c7e1-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="0c7e1-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos del servicio de nombres Internet de Windows (WINS).</span><span class="sxs-lookup"><span data-stu-id="0c7e1-107">The **CreateInstanceFromPropertyData** method instantiates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c7e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c7e1-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="0c7e1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c7e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c7e1-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="0c7e1-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="0c7e1-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="0c7e1-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-117">Class of the RR.</span></span> <span data-ttu-id="0c7e1-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-118">Default value is 1.</span></span> <span data-ttu-id="0c7e1-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-119">The following values are valid.</span></span>



| <span data-ttu-id="0c7e1-120">Value</span><span class="sxs-lookup"><span data-stu-id="0c7e1-120">Value</span></span>                                                                                                | <span data-ttu-id="0c7e1-121">Significado</span><span class="sxs-lookup"><span data-stu-id="0c7e1-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="0c7e1-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e1-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0c7e1-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="0c7e1-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="0c7e1-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e1-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0c7e1-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="0c7e1-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="0c7e1-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e1-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="0c7e1-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="0c7e1-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="0c7e1-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e1-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="0c7e1-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="0c7e1-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="0c7e1-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="0c7e1-132">*MappingFlag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-133">Marca de asignación WINS que especifica si el registro debe incluirse en la replicación de zona.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-133">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="0c7e1-134">Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y no replicación (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="0c7e1-135">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-135">The following values are valid.</span></span>



| <span data-ttu-id="0c7e1-136">Value</span><span class="sxs-lookup"><span data-stu-id="0c7e1-136">Value</span></span>                                                                                                                                               | <span data-ttu-id="0c7e1-137">Significado</span><span class="sxs-lookup"><span data-stu-id="0c7e1-137">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="0c7e1-138"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e1-138"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="0c7e1-139">Marca de replicación</span><span class="sxs-lookup"><span data-stu-id="0c7e1-139">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="0c7e1-140"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e1-140"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="0c7e1-141">Marca de no replicación (registro local)</span><span class="sxs-lookup"><span data-stu-id="0c7e1-141">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0c7e1-142">*Tiempodeesperadebúsqueda* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-142">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-143">Tiempo, en segundos, que un servidor DNS intenta resolver mediante la búsqueda de WINS.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-143">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="0c7e1-144">*CacheTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-144">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-145">Tiempo, en segundos, que un servidor DNS que usa WINS buscan puede almacenar en caché la respuesta del servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-145">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="0c7e1-146">*WinsServers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-146">*WinsServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-147">Lista de direcciones IP separadas por comas de los servidores WINS utilizados en WINS looks.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-147">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="0c7e1-148">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="0c7e1-148">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0c7e1-149">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-149">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c7e1-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c7e1-150">Return value</span></span>

<span data-ttu-id="0c7e1-151">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0c7e1-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c7e1-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c7e1-152">Requirements</span></span>



| <span data-ttu-id="0c7e1-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c7e1-153">Requirement</span></span> | <span data-ttu-id="0c7e1-154">Value</span><span class="sxs-lookup"><span data-stu-id="0c7e1-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c7e1-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c7e1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="0c7e1-156">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0c7e1-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0c7e1-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c7e1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="0c7e1-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c7e1-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0c7e1-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0c7e1-159">Namespace</span></span><br/>                | <span data-ttu-id="0c7e1-160">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="0c7e1-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="0c7e1-161">MOF</span><span class="sxs-lookup"><span data-stu-id="0c7e1-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c7e1-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c7e1-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c7e1-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c7e1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c7e1-164">**MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="0c7e1-164">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="0c7e1-165">**Método Modify de la \_ clase MicrosoftDNS WINSType**</span><span class="sxs-lookup"><span data-stu-id="0c7e1-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="0c7e1-166">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="0c7e1-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






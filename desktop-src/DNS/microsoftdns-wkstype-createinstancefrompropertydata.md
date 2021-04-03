---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_WKSType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de Well-Known Services (WKS).
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e27b62bd2008c58d283d0e7564fa7821c452cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905389"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="669cd-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WKSType</span><span class="sxs-lookup"><span data-stu-id="669cd-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="669cd-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de Well-Known Services (WKS).</span><span class="sxs-lookup"><span data-stu-id="669cd-107">The **CreateInstanceFromPropertyData** method instantiates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="669cd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="669cd-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="669cd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="669cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="669cd-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="669cd-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="669cd-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="669cd-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="669cd-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="669cd-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="669cd-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="669cd-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="669cd-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="669cd-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="669cd-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="669cd-117">Class of the RR.</span></span> <span data-ttu-id="669cd-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="669cd-118">Default value is 1.</span></span> <span data-ttu-id="669cd-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="669cd-119">The following values are valid.</span></span>



| <span data-ttu-id="669cd-120">Value</span><span class="sxs-lookup"><span data-stu-id="669cd-120">Value</span></span>                                                                                                | <span data-ttu-id="669cd-121">Significado</span><span class="sxs-lookup"><span data-stu-id="669cd-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="669cd-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="669cd-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="669cd-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="669cd-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="669cd-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="669cd-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="669cd-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="669cd-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="669cd-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="669cd-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="669cd-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="669cd-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="669cd-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="669cd-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="669cd-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="669cd-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="669cd-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="669cd-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="669cd-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="669cd-132">*InternetAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="669cd-132">*InternetAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-133">Dirección IP de Internet del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="669cd-133">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="669cd-134">*IPProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="669cd-134">*IPProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-135">Cadena que representa el protocolo IP para este registro.</span><span class="sxs-lookup"><span data-stu-id="669cd-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="669cd-136">Los valores válidos son UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="669cd-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="669cd-137">*Servicios* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="669cd-137">*Services* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-138">Cadena que contiene todos los servicios utilizados por el registro de servicio conocido (WKS).</span><span class="sxs-lookup"><span data-stu-id="669cd-138">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="669cd-139">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="669cd-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="669cd-140">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="669cd-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="669cd-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="669cd-141">Return value</span></span>

<span data-ttu-id="669cd-142">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="669cd-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="669cd-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="669cd-143">Requirements</span></span>



| <span data-ttu-id="669cd-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="669cd-144">Requirement</span></span> | <span data-ttu-id="669cd-145">Value</span><span class="sxs-lookup"><span data-stu-id="669cd-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="669cd-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="669cd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="669cd-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="669cd-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="669cd-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="669cd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="669cd-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="669cd-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="669cd-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="669cd-150">Namespace</span></span><br/>                | <span data-ttu-id="669cd-151">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="669cd-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="669cd-152">MOF</span><span class="sxs-lookup"><span data-stu-id="669cd-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="669cd-153"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="669cd-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="669cd-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="669cd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="669cd-155">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="669cd-155">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="669cd-156">**Método Modify de la \_ clase MicrosoftDNS WKSType**</span><span class="sxs-lookup"><span data-stu-id="669cd-156">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="669cd-157">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="669cd-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






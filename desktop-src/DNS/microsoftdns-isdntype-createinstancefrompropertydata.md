---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_ISDNType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos ISDN.
ms.assetid: cd3b98e3-a804-473e-8831-5f045d43a54f
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f6adaaf374cac56d7d29d04d83c8765b0080ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534642"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="a5a99-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ISDNType</span><span class="sxs-lookup"><span data-stu-id="a5a99-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="a5a99-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos ISDN.</span><span class="sxs-lookup"><span data-stu-id="a5a99-107">The **CreateInstanceFromPropertyData** method instantiates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a99-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5a99-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                ISDNNumber,
  [in]           string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a5a99-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5a99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5a99-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5a99-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a99-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="a5a99-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a5a99-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5a99-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a99-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="a5a99-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a5a99-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5a99-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a99-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="a5a99-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a5a99-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a5a99-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a99-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="a5a99-117">Class of the RR.</span></span> <span data-ttu-id="a5a99-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="a5a99-118">Default value is 1.</span></span> <span data-ttu-id="a5a99-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="a5a99-119">The following values are valid.</span></span>



| <span data-ttu-id="a5a99-120">Value</span><span class="sxs-lookup"><span data-stu-id="a5a99-120">Value</span></span>                                                                                                | <span data-ttu-id="a5a99-121">Significado</span><span class="sxs-lookup"><span data-stu-id="a5a99-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a5a99-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a99-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a5a99-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="a5a99-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="a5a99-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a99-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a5a99-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="a5a99-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="a5a99-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a99-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a5a99-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="a5a99-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="a5a99-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a99-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="a5a99-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="a5a99-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a5a99-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a5a99-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a99-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="a5a99-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a5a99-132">*ISDNNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5a99-132">*ISDNNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a99-133">Número ISDN y DDI del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="a5a99-133">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="a5a99-134">*Subdirección* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5a99-134">*SubAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a99-135">Subdirección del propietario, si está definido.</span><span class="sxs-lookup"><span data-stu-id="a5a99-135">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="a5a99-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="a5a99-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a99-137">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="a5a99-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5a99-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5a99-138">Return value</span></span>

<span data-ttu-id="a5a99-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a5a99-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5a99-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5a99-140">Requirements</span></span>



| <span data-ttu-id="a5a99-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a99-141">Requirement</span></span> | <span data-ttu-id="a5a99-142">Value</span><span class="sxs-lookup"><span data-stu-id="a5a99-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a99-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5a99-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a99-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a5a99-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a5a99-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5a99-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a99-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5a99-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a5a99-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5a99-147">Namespace</span></span><br/>                | <span data-ttu-id="a5a99-148">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="a5a99-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a5a99-149">MOF</span><span class="sxs-lookup"><span data-stu-id="a5a99-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5a99-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5a99-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5a99-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5a99-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a99-152">**MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="a5a99-152">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="a5a99-153">**Método Modify de la \_ clase MicrosoftDNS ISDNType**</span><span class="sxs-lookup"><span data-stu-id="a5a99-153">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="a5a99-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a5a99-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






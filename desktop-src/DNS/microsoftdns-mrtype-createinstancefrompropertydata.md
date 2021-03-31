---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_MRType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de cambio de nombre de buzón (MR).
ms.assetid: 7dab86e0-bf05-4e98-b1f8-e1daecd4425c
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_MRType
- MicrosoftDNS_MRType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f41478d4ff59ff7999f6f3b052f203aeda78803
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905270"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="044d9-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MRType</span><span class="sxs-lookup"><span data-stu-id="044d9-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="044d9-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de cambio de nombre de buzón (MR).</span><span class="sxs-lookup"><span data-stu-id="044d9-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="044d9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="044d9-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="044d9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="044d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044d9-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="044d9-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="044d9-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="044d9-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="044d9-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="044d9-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="044d9-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="044d9-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="044d9-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="044d9-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="044d9-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="044d9-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="044d9-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="044d9-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="044d9-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="044d9-117">Class of the RR.</span></span> <span data-ttu-id="044d9-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="044d9-118">Default value is 1.</span></span> <span data-ttu-id="044d9-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="044d9-119">The following values are valid.</span></span>



| <span data-ttu-id="044d9-120">Value</span><span class="sxs-lookup"><span data-stu-id="044d9-120">Value</span></span>                                                                                                | <span data-ttu-id="044d9-121">Significado</span><span class="sxs-lookup"><span data-stu-id="044d9-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="044d9-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="044d9-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="044d9-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="044d9-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="044d9-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="044d9-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="044d9-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="044d9-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="044d9-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="044d9-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="044d9-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="044d9-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="044d9-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="044d9-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="044d9-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="044d9-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="044d9-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="044d9-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="044d9-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="044d9-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="044d9-132">*MRMailbox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="044d9-132">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="044d9-133">FQDN que especifica un buzón que es el cambio de nombre adecuado del buzón especificado en el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="044d9-133">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="044d9-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="044d9-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="044d9-135">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="044d9-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044d9-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="044d9-136">Return value</span></span>

<span data-ttu-id="044d9-137">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="044d9-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="044d9-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="044d9-138">Requirements</span></span>



| <span data-ttu-id="044d9-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="044d9-139">Requirement</span></span> | <span data-ttu-id="044d9-140">Value</span><span class="sxs-lookup"><span data-stu-id="044d9-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="044d9-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="044d9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="044d9-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="044d9-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="044d9-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="044d9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="044d9-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="044d9-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="044d9-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="044d9-145">Namespace</span></span><br/>                | <span data-ttu-id="044d9-146">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="044d9-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="044d9-147">MOF</span><span class="sxs-lookup"><span data-stu-id="044d9-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="044d9-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="044d9-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044d9-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="044d9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044d9-150">**MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="044d9-150">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="044d9-151">**Método Modify de la \_ clase MicrosoftDNS MRType**</span><span class="sxs-lookup"><span data-stu-id="044d9-151">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="044d9-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="044d9-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






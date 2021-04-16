---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_TXTType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de texto (TXT).
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23f9790189ca182cd65d9fe34890c31a90921d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658323"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="4c185-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS TXTType</span><span class="sxs-lookup"><span data-stu-id="4c185-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="4c185-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de texto (txt).</span><span class="sxs-lookup"><span data-stu-id="4c185-107">The **CreateInstanceFromPropertyData** method instantiates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c185-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c185-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4c185-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c185-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c185-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c185-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c185-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="4c185-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4c185-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c185-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c185-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="4c185-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4c185-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c185-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c185-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="4c185-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4c185-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4c185-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c185-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="4c185-117">Class of the RR.</span></span> <span data-ttu-id="4c185-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="4c185-118">Default value is 1.</span></span> <span data-ttu-id="4c185-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="4c185-119">The following values are valid.</span></span>



| <span data-ttu-id="4c185-120">Value</span><span class="sxs-lookup"><span data-stu-id="4c185-120">Value</span></span>                                                                                                | <span data-ttu-id="4c185-121">Significado</span><span class="sxs-lookup"><span data-stu-id="4c185-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4c185-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4c185-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4c185-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="4c185-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="4c185-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4c185-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4c185-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="4c185-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="4c185-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4c185-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4c185-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="4c185-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="4c185-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4c185-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4c185-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="4c185-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4c185-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4c185-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c185-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="4c185-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4c185-132">*DescriptiveText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c185-132">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c185-133">Texto descriptivo, la semántica de que depende del dominio del propietario.</span><span class="sxs-lookup"><span data-stu-id="4c185-133">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="4c185-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4c185-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4c185-135">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="4c185-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c185-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c185-136">Return value</span></span>

<span data-ttu-id="4c185-137">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4c185-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c185-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c185-138">Requirements</span></span>



| <span data-ttu-id="4c185-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c185-139">Requirement</span></span> | <span data-ttu-id="4c185-140">Value</span><span class="sxs-lookup"><span data-stu-id="4c185-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c185-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c185-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4c185-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4c185-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4c185-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c185-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4c185-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c185-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4c185-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4c185-145">Namespace</span></span><br/>                | <span data-ttu-id="4c185-146">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="4c185-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4c185-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4c185-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c185-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c185-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c185-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c185-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c185-150">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="4c185-150">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="4c185-151">**Método Modify de la \_ clase MicrosoftDNS TXTType**</span><span class="sxs-lookup"><span data-stu-id="4c185-151">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="4c185-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4c185-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_MBType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de buzón (MB).
ms.assetid: ac160a4d-2af7-428e-9cbd-bdd28f7c0910
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_MBType
- MicrosoftDNS_MBType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e340d78057c12e58159a293468598da7dbf53e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905344"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="4af7d-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MBType</span><span class="sxs-lookup"><span data-stu-id="4af7d-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="4af7d-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de buzón (MB).</span><span class="sxs-lookup"><span data-stu-id="4af7d-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4af7d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4af7d-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]       string              DnsServerName,
  [in]       string              ContainerName,
  [in]       string              OwnerName,
  [in]       uint32              RecordClass = 1,
  [in]       uint32              TTL,
  [in]       string              MBHost,
  [out, ref] MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4af7d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4af7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4af7d-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4af7d-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af7d-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="4af7d-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4af7d-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4af7d-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af7d-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="4af7d-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4af7d-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4af7d-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af7d-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="4af7d-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4af7d-116">*RecordClass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4af7d-116">*RecordClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af7d-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4af7d-117">Optional.</span></span> <span data-ttu-id="4af7d-118">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="4af7d-118">Class of the RR.</span></span> <span data-ttu-id="4af7d-119">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="4af7d-119">Default value is 1.</span></span> <span data-ttu-id="4af7d-120">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="4af7d-120">The following values are valid.</span></span>



| <span data-ttu-id="4af7d-121">Value</span><span class="sxs-lookup"><span data-stu-id="4af7d-121">Value</span></span>                                                                                                | <span data-ttu-id="4af7d-122">Significado</span><span class="sxs-lookup"><span data-stu-id="4af7d-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4af7d-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4af7d-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4af7d-124">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="4af7d-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="4af7d-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4af7d-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4af7d-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="4af7d-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="4af7d-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4af7d-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4af7d-128">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="4af7d-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="4af7d-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4af7d-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4af7d-130">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="4af7d-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4af7d-131">*TTL* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4af7d-131">*TTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af7d-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4af7d-132">Optional.</span></span> <span data-ttu-id="4af7d-133">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="4af7d-133">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4af7d-134">*MBHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4af7d-134">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af7d-135">Nombre del host de buzón del RR.</span><span class="sxs-lookup"><span data-stu-id="4af7d-135">Mailbox host name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4af7d-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4af7d-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4af7d-137">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="4af7d-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4af7d-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4af7d-138">Return value</span></span>

<span data-ttu-id="4af7d-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4af7d-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4af7d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4af7d-140">Requirements</span></span>



| <span data-ttu-id="4af7d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4af7d-141">Requirement</span></span> | <span data-ttu-id="4af7d-142">Value</span><span class="sxs-lookup"><span data-stu-id="4af7d-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4af7d-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4af7d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4af7d-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4af7d-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4af7d-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4af7d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4af7d-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4af7d-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4af7d-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4af7d-147">Namespace</span></span><br/>                | <span data-ttu-id="4af7d-148">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="4af7d-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4af7d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="4af7d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4af7d-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4af7d-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4af7d-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="4af7d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af7d-152">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="4af7d-152">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="4af7d-153">**Método Modify de la \_ clase MicrosoftDNS MBType**</span><span class="sxs-lookup"><span data-stu-id="4af7d-153">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="4af7d-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4af7d-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






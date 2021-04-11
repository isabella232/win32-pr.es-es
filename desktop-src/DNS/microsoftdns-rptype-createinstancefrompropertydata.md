---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_RPType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de persona responsable (RP).
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_RPType
- MicrosoftDNS_RPType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c150a8a91a7a94fbea8492faea08b61d437a4c9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274525"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="59b2d-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS RPType</span><span class="sxs-lookup"><span data-stu-id="59b2d-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="59b2d-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de persona responsable (RP).</span><span class="sxs-lookup"><span data-stu-id="59b2d-107">The **CreateInstanceFromPropertyData** method instantiates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b2d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59b2d-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="59b2d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59b2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b2d-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b2d-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b2d-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="59b2d-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="59b2d-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b2d-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b2d-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="59b2d-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="59b2d-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b2d-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b2d-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="59b2d-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="59b2d-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="59b2d-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59b2d-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="59b2d-117">Class of the RR.</span></span> <span data-ttu-id="59b2d-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="59b2d-118">Default value is 1.</span></span> <span data-ttu-id="59b2d-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="59b2d-119">The following values are valid.</span></span>



| <span data-ttu-id="59b2d-120">Value</span><span class="sxs-lookup"><span data-stu-id="59b2d-120">Value</span></span>                                                                                                | <span data-ttu-id="59b2d-121">Significado</span><span class="sxs-lookup"><span data-stu-id="59b2d-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="59b2d-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="59b2d-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="59b2d-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="59b2d-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="59b2d-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="59b2d-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="59b2d-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="59b2d-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="59b2d-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="59b2d-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="59b2d-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="59b2d-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="59b2d-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="59b2d-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="59b2d-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="59b2d-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="59b2d-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="59b2d-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59b2d-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="59b2d-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="59b2d-132">*RPMailbox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b2d-132">*RPMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b2d-133">FQDN que especifica el buzón de correo para la persona responsable.</span><span class="sxs-lookup"><span data-stu-id="59b2d-133">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="59b2d-134">*TXTDomainName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b2d-134">*TXTDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b2d-135">FQDN para el que existen registros de recursos TXT.</span><span class="sxs-lookup"><span data-stu-id="59b2d-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="59b2d-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="59b2d-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="59b2d-137">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="59b2d-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b2d-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59b2d-138">Return value</span></span>

<span data-ttu-id="59b2d-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="59b2d-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b2d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b2d-140">Requirements</span></span>



| <span data-ttu-id="59b2d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b2d-141">Requirement</span></span> | <span data-ttu-id="59b2d-142">Value</span><span class="sxs-lookup"><span data-stu-id="59b2d-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59b2d-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b2d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="59b2d-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="59b2d-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="59b2d-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b2d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="59b2d-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59b2d-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="59b2d-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="59b2d-147">Namespace</span></span><br/>                | <span data-ttu-id="59b2d-148">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="59b2d-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="59b2d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="59b2d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59b2d-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59b2d-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b2d-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="59b2d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b2d-152">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="59b2d-152">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="59b2d-153">**Método Modify de la \_ clase MicrosoftDNS RPType**</span><span class="sxs-lookup"><span data-stu-id="59b2d-153">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="59b2d-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="59b2d-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






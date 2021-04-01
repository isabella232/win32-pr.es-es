---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_MFType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos del agente de reenvío de correo para el dominio (MF).
ms.assetid: e669d065-bfba-4a86-8519-2317e03ed4ee
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_MFType
- MicrosoftDNS_MFType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26cafc766a6ea6419432b279f5389721f6572b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996368"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="89171-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MFType</span><span class="sxs-lookup"><span data-stu-id="89171-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="89171-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos del agente de reenvío de correo para el dominio (MF).</span><span class="sxs-lookup"><span data-stu-id="89171-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="89171-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89171-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="89171-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89171-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89171-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89171-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89171-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="89171-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="89171-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89171-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89171-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="89171-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="89171-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89171-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89171-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="89171-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="89171-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="89171-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89171-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="89171-117">Class of the RR.</span></span> <span data-ttu-id="89171-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="89171-118">Default value is 1.</span></span> <span data-ttu-id="89171-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="89171-119">The following values are valid.</span></span>



| <span data-ttu-id="89171-120">Value</span><span class="sxs-lookup"><span data-stu-id="89171-120">Value</span></span>                                                                                                | <span data-ttu-id="89171-121">Significado</span><span class="sxs-lookup"><span data-stu-id="89171-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="89171-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="89171-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="89171-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="89171-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="89171-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="89171-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="89171-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="89171-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="89171-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="89171-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="89171-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="89171-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="89171-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="89171-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="89171-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="89171-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="89171-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="89171-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89171-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="89171-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="89171-132">*MFHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89171-132">*MFHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89171-133">Nombre del host que proporciona el agente de reenvío de correo.</span><span class="sxs-lookup"><span data-stu-id="89171-133">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="89171-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="89171-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="89171-135">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="89171-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89171-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89171-136">Return value</span></span>

<span data-ttu-id="89171-137">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="89171-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="89171-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89171-138">Requirements</span></span>



| <span data-ttu-id="89171-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="89171-139">Requirement</span></span> | <span data-ttu-id="89171-140">Value</span><span class="sxs-lookup"><span data-stu-id="89171-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89171-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89171-141">Minimum supported client</span></span><br/> | <span data-ttu-id="89171-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="89171-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="89171-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89171-143">Minimum supported server</span></span><br/> | <span data-ttu-id="89171-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89171-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="89171-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="89171-145">Namespace</span></span><br/>                | <span data-ttu-id="89171-146">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="89171-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="89171-147">MOF</span><span class="sxs-lookup"><span data-stu-id="89171-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89171-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89171-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89171-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="89171-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89171-150">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="89171-150">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="89171-151">**Método Modify de la \_ clase MicrosoftDNS MFType**</span><span class="sxs-lookup"><span data-stu-id="89171-151">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="89171-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="89171-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






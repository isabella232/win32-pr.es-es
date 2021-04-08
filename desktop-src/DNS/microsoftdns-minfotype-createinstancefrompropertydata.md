---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_MINFOType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de información de correo (MINFO).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a565b1575dc51a59a09faea6fd271d719518f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078900"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="f389c-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MINFOType</span><span class="sxs-lookup"><span data-stu-id="f389c-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="f389c-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de información de correo (MINFO).</span><span class="sxs-lookup"><span data-stu-id="f389c-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f389c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f389c-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f389c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f389c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f389c-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f389c-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f389c-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="f389c-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f389c-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f389c-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f389c-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="f389c-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f389c-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f389c-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f389c-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="f389c-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f389c-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f389c-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f389c-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="f389c-117">Class of the RR.</span></span> <span data-ttu-id="f389c-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="f389c-118">Default value is 1.</span></span> <span data-ttu-id="f389c-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="f389c-119">The following values are valid.</span></span>



| <span data-ttu-id="f389c-120">Value</span><span class="sxs-lookup"><span data-stu-id="f389c-120">Value</span></span>                                                                                                | <span data-ttu-id="f389c-121">Significado</span><span class="sxs-lookup"><span data-stu-id="f389c-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f389c-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f389c-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f389c-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="f389c-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f389c-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f389c-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f389c-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="f389c-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f389c-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f389c-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f389c-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="f389c-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f389c-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f389c-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f389c-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="f389c-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f389c-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f389c-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f389c-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="f389c-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f389c-132">*ResponsibleMailbox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f389c-132">*ResponsibleMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f389c-133">FQDN que especifica un buzón responsable de la lista de distribución de correo o el buzón especificado en el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="f389c-133">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="f389c-134">*ErrorMailbox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f389c-134">*ErrorMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f389c-135">FQDN que especifica un buzón para recibir mensajes de error relacionados con la lista de distribución de correo o con el buzón especificado por el nombre del propietario del registro MINFO.</span><span class="sxs-lookup"><span data-stu-id="f389c-135">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="f389c-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f389c-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f389c-137">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="f389c-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f389c-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f389c-138">Return value</span></span>

<span data-ttu-id="f389c-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f389c-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f389c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f389c-140">Requirements</span></span>



| <span data-ttu-id="f389c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f389c-141">Requirement</span></span> | <span data-ttu-id="f389c-142">Value</span><span class="sxs-lookup"><span data-stu-id="f389c-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f389c-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f389c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f389c-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f389c-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f389c-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f389c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f389c-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f389c-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f389c-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f389c-147">Namespace</span></span><br/>                | <span data-ttu-id="f389c-148">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="f389c-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f389c-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f389c-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f389c-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f389c-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f389c-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="f389c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f389c-152">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="f389c-152">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="f389c-153">**Método Modify de la \_ clase MicrosoftDNS MINFOType**</span><span class="sxs-lookup"><span data-stu-id="f389c-153">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="f389c-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="f389c-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






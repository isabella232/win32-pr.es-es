---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_MGType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de grupo de correo (MG).
ms.assetid: 98e2ecb3-bf2f-42db-8a8b-de10a29f5a5a
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_MGType
- MicrosoftDNS_MGType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 313f6d14a10b1de9bc1d3b3b8042020ea5b0a522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150637"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="ac7c6-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MGType</span><span class="sxs-lookup"><span data-stu-id="ac7c6-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="ac7c6-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de grupo de correo (mg).</span><span class="sxs-lookup"><span data-stu-id="ac7c6-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac7c6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac7c6-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ac7c6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac7c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac7c6-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7c6-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7c6-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ac7c6-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7c6-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7c6-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ac7c6-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7c6-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7c6-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ac7c6-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ac7c6-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7c6-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-117">Class of the RR.</span></span> <span data-ttu-id="ac7c6-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-118">Default value is 1.</span></span> <span data-ttu-id="ac7c6-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-119">The following values are valid.</span></span>



| <span data-ttu-id="ac7c6-120">Value</span><span class="sxs-lookup"><span data-stu-id="ac7c6-120">Value</span></span>                                                                                                | <span data-ttu-id="ac7c6-121">Significado</span><span class="sxs-lookup"><span data-stu-id="ac7c6-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ac7c6-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c6-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ac7c6-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="ac7c6-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ac7c6-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c6-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ac7c6-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="ac7c6-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ac7c6-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c6-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ac7c6-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="ac7c6-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ac7c6-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c6-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ac7c6-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="ac7c6-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ac7c6-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ac7c6-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7c6-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ac7c6-132">*MGMailbox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac7c6-132">*MGMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7c6-133">FQDN que especifica un buzón que es miembro del grupo de correo especificado por el nombre del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-133">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="ac7c6-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ac7c6-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7c6-135">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac7c6-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac7c6-136">Return value</span></span>

<span data-ttu-id="ac7c6-137">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac7c6-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7c6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac7c6-138">Requirements</span></span>



| <span data-ttu-id="ac7c6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac7c6-139">Requirement</span></span> | <span data-ttu-id="ac7c6-140">Value</span><span class="sxs-lookup"><span data-stu-id="ac7c6-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7c6-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac7c6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ac7c6-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ac7c6-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ac7c6-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac7c6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ac7c6-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac7c6-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ac7c6-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ac7c6-145">Namespace</span></span><br/>                | <span data-ttu-id="ac7c6-146">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="ac7c6-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ac7c6-147">MOF</span><span class="sxs-lookup"><span data-stu-id="ac7c6-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac7c6-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c6-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac7c6-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac7c6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac7c6-150">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="ac7c6-150">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="ac7c6-151">**Método Modify de la \_ clase MicrosoftDNS MGType**</span><span class="sxs-lookup"><span data-stu-id="ac7c6-151">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="ac7c6-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ac7c6-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






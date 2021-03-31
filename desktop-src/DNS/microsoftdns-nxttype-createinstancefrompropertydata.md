---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_NXTType
description: El método CreateInstanceFromPropertyData crea una instancia de un siguiente registro de recursos (NXT).
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee00cd0afdb6ac629a981dbdb586a30252eac1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491416"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="4b3cb-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS NXTType</span><span class="sxs-lookup"><span data-stu-id="4b3cb-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="4b3cb-107">El método **CreateInstanceFromPropertyData** crea una instancia de un siguiente registro de recursos (NXT).</span><span class="sxs-lookup"><span data-stu-id="4b3cb-107">The **CreateInstanceFromPropertyData** method instantiates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b3cb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b3cb-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4b3cb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b3cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b3cb-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4b3cb-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4b3cb-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4b3cb-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-117">Class of the RR.</span></span> <span data-ttu-id="4b3cb-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-118">Default value is 1.</span></span> <span data-ttu-id="4b3cb-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-119">The following values are valid.</span></span>



| <span data-ttu-id="4b3cb-120">Value</span><span class="sxs-lookup"><span data-stu-id="4b3cb-120">Value</span></span>                                                                                                | <span data-ttu-id="4b3cb-121">Significado</span><span class="sxs-lookup"><span data-stu-id="4b3cb-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4b3cb-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4b3cb-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4b3cb-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="4b3cb-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="4b3cb-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4b3cb-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4b3cb-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="4b3cb-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="4b3cb-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4b3cb-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4b3cb-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="4b3cb-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="4b3cb-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4b3cb-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4b3cb-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="4b3cb-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4b3cb-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4b3cb-132">*NextDomainName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-132">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-133">Siguiente nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-133">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="4b3cb-134">*Tipos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-134">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-135">Lista separada por espacios de los códigos mnemónicos del tipo RR para el nombre del propietario del registro de recursos NXT.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-135">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="4b3cb-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-137">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b3cb-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b3cb-138">Return value</span></span>

<span data-ttu-id="4b3cb-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b3cb-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b3cb-140">Requirements</span></span>



| <span data-ttu-id="4b3cb-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b3cb-141">Requirement</span></span> | <span data-ttu-id="4b3cb-142">Value</span><span class="sxs-lookup"><span data-stu-id="4b3cb-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3cb-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b3cb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4b3cb-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4b3cb-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4b3cb-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b3cb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4b3cb-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b3cb-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4b3cb-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4b3cb-147">Namespace</span></span><br/>                | <span data-ttu-id="4b3cb-148">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="4b3cb-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4b3cb-149">MOF</span><span class="sxs-lookup"><span data-stu-id="4b3cb-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b3cb-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b3cb-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b3cb-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b3cb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3cb-152">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="4b3cb-152">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="4b3cb-153">**Método Modify de la \_ clase MicrosoftDNS NXTType**</span><span class="sxs-lookup"><span data-stu-id="4b3cb-153">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="4b3cb-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="4b3cb-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






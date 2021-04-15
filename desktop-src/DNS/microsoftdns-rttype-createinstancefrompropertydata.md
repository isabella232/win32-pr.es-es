---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_RTType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de ruta a través de (RT).
ms.assetid: 1ebb0543-d031-4430-acbe-708c4931b7a4
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_RTType
- MicrosoftDNS_RTType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c3b8d71c41fefa9b78aa9a469ee1426c553e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534329"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="73a4b-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS RTType</span><span class="sxs-lookup"><span data-stu-id="73a4b-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="73a4b-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de ruta a través de (RT).</span><span class="sxs-lookup"><span data-stu-id="73a4b-107">The **CreateInstanceFromPropertyData** method instantiates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a4b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73a4b-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="73a4b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73a4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73a4b-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73a4b-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a4b-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="73a4b-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="73a4b-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73a4b-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a4b-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="73a4b-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="73a4b-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73a4b-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a4b-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="73a4b-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="73a4b-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="73a4b-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73a4b-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="73a4b-117">Class of the RR.</span></span> <span data-ttu-id="73a4b-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="73a4b-118">Default value is 1.</span></span> <span data-ttu-id="73a4b-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="73a4b-119">The following values are valid.</span></span>



| <span data-ttu-id="73a4b-120">Value</span><span class="sxs-lookup"><span data-stu-id="73a4b-120">Value</span></span>                                                                                                | <span data-ttu-id="73a4b-121">Significado</span><span class="sxs-lookup"><span data-stu-id="73a4b-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="73a4b-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="73a4b-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="73a4b-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="73a4b-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="73a4b-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="73a4b-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="73a4b-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="73a4b-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="73a4b-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="73a4b-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="73a4b-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="73a4b-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="73a4b-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="73a4b-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="73a4b-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="73a4b-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="73a4b-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="73a4b-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73a4b-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="73a4b-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="73a4b-132">*Preferencia* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73a4b-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a4b-133">Preferencia asignada a este RR entre otros en el mismo propietario.</span><span class="sxs-lookup"><span data-stu-id="73a4b-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="73a4b-134">Se prefieren los valores inferiores.</span><span class="sxs-lookup"><span data-stu-id="73a4b-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="73a4b-135">*IntermediateHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73a4b-135">*IntermediateHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a4b-136">FQDN que especifica un host que actúa como intermediario para alcanzar el host especificado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="73a4b-136">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="73a4b-137">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="73a4b-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="73a4b-138">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="73a4b-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73a4b-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73a4b-139">Return value</span></span>

<span data-ttu-id="73a4b-140">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="73a4b-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="73a4b-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73a4b-141">Requirements</span></span>



| <span data-ttu-id="73a4b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="73a4b-142">Requirement</span></span> | <span data-ttu-id="73a4b-143">Value</span><span class="sxs-lookup"><span data-stu-id="73a4b-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73a4b-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73a4b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="73a4b-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="73a4b-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="73a4b-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73a4b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="73a4b-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="73a4b-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="73a4b-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="73a4b-148">Namespace</span></span><br/>                | <span data-ttu-id="73a4b-149">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="73a4b-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="73a4b-150">MOF</span><span class="sxs-lookup"><span data-stu-id="73a4b-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73a4b-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73a4b-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a4b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="73a4b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a4b-153">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="73a4b-153">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="73a4b-154">**Método Modify de la \_ clase MicrosoftDNS RTType**</span><span class="sxs-lookup"><span data-stu-id="73a4b-154">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="73a4b-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="73a4b-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






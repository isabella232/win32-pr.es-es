---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_AType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de dirección (A).
ms.assetid: 81d67eba-f2c6-49c0-af29-be3f3724a973
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_AType
- MicrosoftDNS_AType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d8d3e5c9d0ad4302da2243a3ef9611e295c86e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150297"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="33c5b-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AType</span><span class="sxs-lookup"><span data-stu-id="33c5b-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="33c5b-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de dirección (A).</span><span class="sxs-lookup"><span data-stu-id="33c5b-107">The **CreateInstanceFromPropertyData** method instantiates an Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c5b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33c5b-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string             DnsServerName,
  [in]           string             ContainerName,
  [in]           string             OwnerName,
  [in, optional] uint32             RecordClass = 1,
  [in, optional] uint32             TTL,
  [in]           string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="33c5b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33c5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c5b-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33c5b-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c5b-111">Nombre de dominio completo (FQDN) o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="33c5b-111">Fully Qualified Domain Name (FQDN) or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="33c5b-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33c5b-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c5b-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="33c5b-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="33c5b-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33c5b-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c5b-115">FQDN del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="33c5b-115">Owner FQDN for the RR.</span></span>

> [!Note]  
> <span data-ttu-id="33c5b-116">No use el nombre NetBIOS del propietario.</span><span class="sxs-lookup"><span data-stu-id="33c5b-116">Do not use the owner NetBIOS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="33c5b-117">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33c5b-117">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33c5b-118">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="33c5b-118">Class of the RR.</span></span> <span data-ttu-id="33c5b-119">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="33c5b-119">Default value is 1.</span></span> <span data-ttu-id="33c5b-120">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="33c5b-120">The following values are valid.</span></span>



| <span data-ttu-id="33c5b-121">Value</span><span class="sxs-lookup"><span data-stu-id="33c5b-121">Value</span></span>                                                                                                | <span data-ttu-id="33c5b-122">Significado</span><span class="sxs-lookup"><span data-stu-id="33c5b-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="33c5b-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="33c5b-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="33c5b-124">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="33c5b-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="33c5b-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="33c5b-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="33c5b-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="33c5b-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="33c5b-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="33c5b-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="33c5b-128">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="33c5b-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="33c5b-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="33c5b-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="33c5b-130">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="33c5b-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="33c5b-131">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33c5b-131">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33c5b-132">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="33c5b-132">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="33c5b-133">*Dirección IP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33c5b-133">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c5b-134">Cadena que representa la dirección IP del host.</span><span class="sxs-lookup"><span data-stu-id="33c5b-134">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="33c5b-135">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="33c5b-135">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="33c5b-136">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="33c5b-136">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c5b-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33c5b-137">Return value</span></span>

<span data-ttu-id="33c5b-138">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="33c5b-138">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c5b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33c5b-139">Requirements</span></span>



| <span data-ttu-id="33c5b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c5b-140">Requirement</span></span> | <span data-ttu-id="33c5b-141">Value</span><span class="sxs-lookup"><span data-stu-id="33c5b-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33c5b-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33c5b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="33c5b-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="33c5b-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="33c5b-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33c5b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="33c5b-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="33c5b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="33c5b-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="33c5b-146">Namespace</span></span><br/>                | <span data-ttu-id="33c5b-147">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="33c5b-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="33c5b-148">MOF</span><span class="sxs-lookup"><span data-stu-id="33c5b-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33c5b-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33c5b-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c5b-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="33c5b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c5b-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="33c5b-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="33c5b-152">**Método Modify de la \_ clase MicrosoftDNS AType**</span><span class="sxs-lookup"><span data-stu-id="33c5b-152">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 






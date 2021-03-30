---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_SRVType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de servicio (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 607ed606bf12e9e2a6f90a6e7f309aa708b7f230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803686"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="c6adb-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS SRVType</span><span class="sxs-lookup"><span data-stu-id="c6adb-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="c6adb-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de servicio (SRV).</span><span class="sxs-lookup"><span data-stu-id="c6adb-107">The **CreateInstanceFromPropertyData** method instantiates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6adb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6adb-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c6adb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6adb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6adb-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="c6adb-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c6adb-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="c6adb-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c6adb-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="c6adb-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c6adb-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="c6adb-117">Class of the RR.</span></span> <span data-ttu-id="c6adb-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="c6adb-118">Default value is 1.</span></span> <span data-ttu-id="c6adb-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="c6adb-119">The following values are valid.</span></span>



| <span data-ttu-id="c6adb-120">Value</span><span class="sxs-lookup"><span data-stu-id="c6adb-120">Value</span></span>                                                                                                | <span data-ttu-id="c6adb-121">Significado</span><span class="sxs-lookup"><span data-stu-id="c6adb-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c6adb-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c6adb-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c6adb-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="c6adb-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c6adb-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c6adb-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c6adb-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c6adb-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c6adb-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c6adb-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c6adb-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="c6adb-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c6adb-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c6adb-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c6adb-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="c6adb-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c6adb-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="c6adb-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c6adb-132">*Prioridad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-132">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-133">Prioridad del host de destino especificado en el nombre del propietario.</span><span class="sxs-lookup"><span data-stu-id="c6adb-133">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="c6adb-134">Los números más bajos implican prioridades más altas.</span><span class="sxs-lookup"><span data-stu-id="c6adb-134">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="c6adb-135">*Peso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-135">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-136">Peso del host de destino.</span><span class="sxs-lookup"><span data-stu-id="c6adb-136">Weight of the target host.</span></span> <span data-ttu-id="c6adb-137">Esto resulta útil al seleccionar entre los hosts que tienen la misma prioridad.</span><span class="sxs-lookup"><span data-stu-id="c6adb-137">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="c6adb-138">Las posibilidades de usar este host deben ser proporcionales a su peso.</span><span class="sxs-lookup"><span data-stu-id="c6adb-138">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="c6adb-139">*Puerto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-139">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-140">Puerto usado en el host de destino de un servicio de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c6adb-140">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="c6adb-141">*SRVDomainName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-141">*SRVDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-142">FQDN del host de destino.</span><span class="sxs-lookup"><span data-stu-id="c6adb-142">FQDN of the target host.</span></span> <span data-ttu-id="c6adb-143">Un destino de \\ . \\ significa que el servicio no está disponible en este dominio.</span><span class="sxs-lookup"><span data-stu-id="c6adb-143">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="c6adb-144">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c6adb-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c6adb-145">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="c6adb-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6adb-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6adb-146">Return value</span></span>

<span data-ttu-id="c6adb-147">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c6adb-147">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6adb-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6adb-148">Requirements</span></span>



| <span data-ttu-id="c6adb-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6adb-149">Requirement</span></span> | <span data-ttu-id="c6adb-150">Value</span><span class="sxs-lookup"><span data-stu-id="c6adb-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6adb-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6adb-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c6adb-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c6adb-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c6adb-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6adb-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c6adb-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6adb-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c6adb-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c6adb-155">Namespace</span></span><br/>                | <span data-ttu-id="c6adb-156">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="c6adb-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c6adb-157">MOF</span><span class="sxs-lookup"><span data-stu-id="c6adb-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6adb-158"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6adb-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6adb-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6adb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6adb-160">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="c6adb-160">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="c6adb-161">**Método Modify de la \_ clase MicrosoftDNS SRVType**</span><span class="sxs-lookup"><span data-stu-id="c6adb-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="c6adb-162">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c6adb-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






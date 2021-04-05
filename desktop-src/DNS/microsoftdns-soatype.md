---
title: MicrosoftDNS_SOAType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de inicio de autoridad (SOA).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- DNS de la clase MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078990"
---
# <a name="microsoftdns_soatype-class"></a><span data-ttu-id="cc82a-105">MicrosoftDNS ( \_ clase SOAType)</span><span class="sxs-lookup"><span data-stu-id="cc82a-105">MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="cc82a-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de inicio de autoridad (SOA).</span><span class="sxs-lookup"><span data-stu-id="cc82a-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Start Of Authority (SOA) record.</span></span>

<span data-ttu-id="cc82a-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="cc82a-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc82a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc82a-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a><span data-ttu-id="cc82a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc82a-109">Members</span></span>

<span data-ttu-id="cc82a-110">La clase **MicrosoftDNS \_ SOAType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cc82a-110">The **MicrosoftDNS\_SOAType** class has these types of members:</span></span>

-   [<span data-ttu-id="cc82a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc82a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cc82a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc82a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cc82a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc82a-113">Methods</span></span>

<span data-ttu-id="cc82a-114">La clase **MicrosoftDNS \_ SOAType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cc82a-114">The **MicrosoftDNS\_SOAType** class has these methods.</span></span>



| <span data-ttu-id="cc82a-115">Método</span><span class="sxs-lookup"><span data-stu-id="cc82a-115">Method</span></span>     | <span data-ttu-id="cc82a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc82a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc82a-117">**Modify**</span><span class="sxs-lookup"><span data-stu-id="cc82a-117">**Modify**</span></span> | <span data-ttu-id="cc82a-118">Actualiza el TTL, el número de serie de SOA, el servidor principal, la entidad responsable, el intervalo de actualización, el retraso de reintentos, el límite de expiración y el TTL mínimo (para la zona) a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="cc82a-118">Updates the TTL, SOA Serial Number, Primary Server, Responsible Party, Refresh Interval, Retry Delay, Expire Limit and Minimum TTL (for the zone) to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="cc82a-119">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="cc82a-119">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="cc82a-120">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="cc82a-120">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="cc82a-121">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="cc82a-121">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cc82a-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc82a-122">Properties</span></span>

<span data-ttu-id="cc82a-123">La clase **MicrosoftDNS \_ SOAType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cc82a-123">The **MicrosoftDNS\_SOAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc82a-124">**ExpireLimit**</span><span class="sxs-lookup"><span data-stu-id="cc82a-124">**ExpireLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc82a-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc82a-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc82a-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc82a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc82a-127">Tiempo, en segundos, antes de que una zona que no responde deje de ser autoritativa.</span><span class="sxs-lookup"><span data-stu-id="cc82a-127">Time, in seconds, before an unresponsive zone is no longer authoritative.</span></span>

</dd> <dt>

<span data-ttu-id="cc82a-128">**MinimumTTL**</span><span class="sxs-lookup"><span data-stu-id="cc82a-128">**MinimumTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc82a-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc82a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc82a-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc82a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc82a-131">Límite inferior en el tiempo, en segundos, que un servidor DNS o un solucionador de almacenamiento en caché pueden almacenar en caché cualquier registro de recursos de la zona a la que pertenece este registro.</span><span class="sxs-lookup"><span data-stu-id="cc82a-131">Lower limit on the time, in seconds, that a DNS Server or Caching resolver are allowed to cache any resource record from the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="cc82a-132">**PrimaryServer**</span><span class="sxs-lookup"><span data-stu-id="cc82a-132">**PrimaryServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc82a-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc82a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc82a-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc82a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc82a-135">Servidor DNS autoritativo para la zona a la que pertenece el registro.</span><span class="sxs-lookup"><span data-stu-id="cc82a-135">Authoritative DNS Server for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="cc82a-136">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="cc82a-136">**RefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc82a-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc82a-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc82a-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc82a-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc82a-139">Tiempo, en segundos, antes de que se actualice la zona que contiene este registro.</span><span class="sxs-lookup"><span data-stu-id="cc82a-139">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="cc82a-140">**ResponsibleParty**</span><span class="sxs-lookup"><span data-stu-id="cc82a-140">**ResponsibleParty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc82a-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc82a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc82a-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc82a-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc82a-143">Nombre de la entidad responsable de la zona a la que pertenece el registro.</span><span class="sxs-lookup"><span data-stu-id="cc82a-143">Name of the responsible party for the zone to which the record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="cc82a-144">**RetryDelay**</span><span class="sxs-lookup"><span data-stu-id="cc82a-144">**RetryDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc82a-145">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc82a-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc82a-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc82a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc82a-147">Tiempo, en segundos, antes de volver a intentar una actualización con errores de la zona a la que pertenece este registro.</span><span class="sxs-lookup"><span data-stu-id="cc82a-147">Time, in seconds, before retrying a failed refresh of the zone to which this record belongs.</span></span>

</dd> <dt>

<span data-ttu-id="cc82a-148">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="cc82a-148">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc82a-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc82a-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc82a-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc82a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc82a-151">Número de serie del registro SOA.</span><span class="sxs-lookup"><span data-stu-id="cc82a-151">Serial number of the SOA record.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc82a-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc82a-152">Requirements</span></span>



| <span data-ttu-id="cc82a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc82a-153">Requirement</span></span> | <span data-ttu-id="cc82a-154">Value</span><span class="sxs-lookup"><span data-stu-id="cc82a-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc82a-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc82a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="cc82a-156">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cc82a-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cc82a-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc82a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="cc82a-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc82a-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc82a-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc82a-159">Namespace</span></span><br/>                | <span data-ttu-id="cc82a-160">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="cc82a-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cc82a-161">MOF</span><span class="sxs-lookup"><span data-stu-id="cc82a-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc82a-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc82a-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc82a-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc82a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc82a-164">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="cc82a-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="cc82a-165">**Método Modify de la \_ clase MicrosoftDNS SOAType**</span><span class="sxs-lookup"><span data-stu-id="cc82a-165">**Modify Method of the MicrosoftDNS\_SOAType Class**</span></span>](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 






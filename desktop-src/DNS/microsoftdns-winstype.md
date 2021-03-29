---
title: MicrosoftDNS_WINSType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro del servicio de nombres Internet de Windows (WINS).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- DNS de la clase MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce23132073305142948518327ea5b6c7e46f1289
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905390"
---
# <a name="microsoftdns_winstype-class"></a><span data-ttu-id="c5229-105">MicrosoftDNS ( \_ clase WINSType)</span><span class="sxs-lookup"><span data-stu-id="c5229-105">MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="c5229-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro del servicio de nombres Internet de Windows (WINS).</span><span class="sxs-lookup"><span data-stu-id="c5229-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Windows Internet Name Service (WINS) record.</span></span>

<span data-ttu-id="c5229-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="c5229-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5229-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5229-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a><span data-ttu-id="c5229-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5229-109">Members</span></span>

<span data-ttu-id="c5229-110">La clase **MicrosoftDNS \_ WINSType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c5229-110">The **MicrosoftDNS\_WINSType** class has these types of members:</span></span>

-   [<span data-ttu-id="c5229-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5229-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c5229-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5229-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c5229-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5229-113">Methods</span></span>

<span data-ttu-id="c5229-114">La clase **MicrosoftDNS \_ WINSType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c5229-114">The **MicrosoftDNS\_WINSType** class has these methods.</span></span>



| <span data-ttu-id="c5229-115">Método</span><span class="sxs-lookup"><span data-stu-id="c5229-115">Method</span></span>                             | <span data-ttu-id="c5229-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5229-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5229-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c5229-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c5229-118">Crea una instancia de un tipo WINS de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la marca de asignación WINS, el tiempo de espera de búsqueda, el tiempo de espera de caché y la lista de direcciones</span><span class="sxs-lookup"><span data-stu-id="c5229-118">Instantiates a WINS Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, look-up time out, cache time out and list of IP addresses for look up.</span></span> <span data-ttu-id="c5229-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="c5229-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c5229-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="c5229-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="c5229-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="c5229-121">**Modify**</span></span>                         | <span data-ttu-id="c5229-122">Actualiza el TTL, la marca de asignación, el tiempo de espera de búsqueda, el tiempo de espera de la caché y los servidores WINS a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="c5229-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Wins Servers to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c5229-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="c5229-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="c5229-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="c5229-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c5229-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="c5229-125">Qualifiers: Implemented</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="c5229-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5229-126">Properties</span></span>

<span data-ttu-id="c5229-127">La clase **MicrosoftDNS \_ WINSType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c5229-127">The **MicrosoftDNS\_WINSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5229-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="c5229-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5229-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5229-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5229-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5229-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5229-131">Tiempo, en segundos, que un servidor DNS que usa WINS buscan puede almacenar en caché la respuesta del servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="c5229-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="c5229-132">**Tiempodeesperadebúsqueda**</span><span class="sxs-lookup"><span data-stu-id="c5229-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5229-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5229-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5229-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5229-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5229-135">Tiempo, en segundos, que un servidor DNS intenta resolver mediante la búsqueda de WINS.</span><span class="sxs-lookup"><span data-stu-id="c5229-135">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="c5229-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="c5229-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5229-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5229-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5229-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5229-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5229-139">Marca de asignación WINS que especifica si el registro debe incluirse en la replicación de zona.</span><span class="sxs-lookup"><span data-stu-id="c5229-139">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="c5229-140">Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y no replicación (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c5229-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="c5229-141">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="c5229-141">The following values are valid.</span></span>



| <span data-ttu-id="c5229-142">Value</span><span class="sxs-lookup"><span data-stu-id="c5229-142">Value</span></span>                                                                                                                                               | <span data-ttu-id="c5229-143">Significado</span><span class="sxs-lookup"><span data-stu-id="c5229-143">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="c5229-144"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="c5229-144"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="c5229-145">Marca de replicación</span><span class="sxs-lookup"><span data-stu-id="c5229-145">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="c5229-146"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="c5229-146"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="c5229-147">Marca de no replicación (registro local)</span><span class="sxs-lookup"><span data-stu-id="c5229-147">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c5229-148">**WinsServers**</span><span class="sxs-lookup"><span data-stu-id="c5229-148">**WinsServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5229-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c5229-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5229-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c5229-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5229-151">Lista de direcciones IP separadas por comas de los servidores WINS utilizados en WINS looks.</span><span class="sxs-lookup"><span data-stu-id="c5229-151">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5229-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5229-152">Requirements</span></span>



| <span data-ttu-id="c5229-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5229-153">Requirement</span></span> | <span data-ttu-id="c5229-154">Value</span><span class="sxs-lookup"><span data-stu-id="c5229-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5229-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5229-155">Minimum supported client</span></span><br/> | <span data-ttu-id="c5229-156">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c5229-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c5229-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5229-157">Minimum supported server</span></span><br/> | <span data-ttu-id="c5229-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5229-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c5229-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5229-159">Namespace</span></span><br/>                | <span data-ttu-id="c5229-160">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="c5229-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c5229-161">MOF</span><span class="sxs-lookup"><span data-stu-id="c5229-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5229-162"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5229-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5229-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5229-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5229-164">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WINSType**</span><span class="sxs-lookup"><span data-stu-id="c5229-164">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c5229-165">**Método Modify de la \_ clase MicrosoftDNS WINSType**</span><span class="sxs-lookup"><span data-stu-id="c5229-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="c5229-166">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c5229-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






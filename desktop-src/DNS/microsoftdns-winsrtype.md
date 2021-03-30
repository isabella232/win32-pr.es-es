---
title: MicrosoftDNS_WINSRType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de búsqueda inversa (WINS) de WINS.
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- DNS de la clase MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9500c6a36a1c3a7cc243f1cbcfbc0edca6cecf2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422585"
---
# <a name="microsoftdns_winsrtype-class"></a><span data-ttu-id="31f61-105">MicrosoftDNS ( \_ clase WINSRType)</span><span class="sxs-lookup"><span data-stu-id="31f61-105">MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="31f61-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de búsqueda inversa (WINS) de WINS.</span><span class="sxs-lookup"><span data-stu-id="31f61-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a WINS Reverse Look-up (WINSR) record.</span></span>

<span data-ttu-id="31f61-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="31f61-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f61-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31f61-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a><span data-ttu-id="31f61-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="31f61-109">Members</span></span>

<span data-ttu-id="31f61-110">La clase **MicrosoftDNS \_ WINSRType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="31f61-110">The **MicrosoftDNS\_WINSRType** class has these types of members:</span></span>

-   [<span data-ttu-id="31f61-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="31f61-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="31f61-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31f61-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="31f61-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="31f61-113">Methods</span></span>

<span data-ttu-id="31f61-114">La clase **MicrosoftDNS \_ WINSRType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="31f61-114">The **MicrosoftDNS\_WINSRType** class has these methods.</span></span>



| <span data-ttu-id="31f61-115">Método</span><span class="sxs-lookup"><span data-stu-id="31f61-115">Method</span></span>                             | <span data-ttu-id="31f61-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="31f61-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f61-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="31f61-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="31f61-118">Crea una instancia de un tipo de RR de WINS en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la marca de asignación de WINS, el tiempo de espera de búsqueda inverso, el tiempo de espera de la caché</span><span class="sxs-lookup"><span data-stu-id="31f61-118">Instantiates a WINSR Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="31f61-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="31f61-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="31f61-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="31f61-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="31f61-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="31f61-121">**Modify**</span></span>                         | <span data-ttu-id="31f61-122">Actualiza el TTL, la marca de asignación, el tiempo de espera de búsqueda, el tiempo de espera de caché y el dominio de resultado a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="31f61-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="31f61-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="31f61-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="31f61-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="31f61-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="31f61-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="31f61-125">Qualifiers: Implemented</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="31f61-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31f61-126">Properties</span></span>

<span data-ttu-id="31f61-127">La clase **MicrosoftDNS \_ WINSRType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="31f61-127">The **MicrosoftDNS\_WINSRType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31f61-128">**CacheTimeout**</span><span class="sxs-lookup"><span data-stu-id="31f61-128">**CacheTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f61-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f61-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f61-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31f61-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f61-131">Tiempo, en segundos, que un servidor DNS que usa WINS buscan puede almacenar en caché la respuesta del servidor WINS.</span><span class="sxs-lookup"><span data-stu-id="31f61-131">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="31f61-132">**Tiempodeesperadebúsqueda**</span><span class="sxs-lookup"><span data-stu-id="31f61-132">**LookupTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f61-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f61-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f61-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31f61-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f61-135">Tiempo de espera, en segundos, para un servidor DNS que usa la búsqueda inversa de WINS.</span><span class="sxs-lookup"><span data-stu-id="31f61-135">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="31f61-136">**MappingFlag**</span><span class="sxs-lookup"><span data-stu-id="31f61-136">**MappingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f61-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f61-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f61-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31f61-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f61-139">Marca de asignación de WINSr que especifica si el registro debe incluirse en la replicación de zona.</span><span class="sxs-lookup"><span data-stu-id="31f61-139">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="31f61-140">Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y no replicación (registro local), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="31f61-140">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="31f61-141">**ResultDomain**</span><span class="sxs-lookup"><span data-stu-id="31f61-141">**ResultDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f61-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="31f61-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31f61-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31f61-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f61-144">Nombre de dominio que se va a anexar a los nombres NetBIOS devueltos.</span><span class="sxs-lookup"><span data-stu-id="31f61-144">Domain name to append to returned NetBIOS names.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31f61-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f61-145">Requirements</span></span>



| <span data-ttu-id="31f61-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f61-146">Requirement</span></span> | <span data-ttu-id="31f61-147">Value</span><span class="sxs-lookup"><span data-stu-id="31f61-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31f61-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31f61-148">Minimum supported client</span></span><br/> | <span data-ttu-id="31f61-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="31f61-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="31f61-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31f61-150">Minimum supported server</span></span><br/> | <span data-ttu-id="31f61-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31f61-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="31f61-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="31f61-152">Namespace</span></span><br/>                | <span data-ttu-id="31f61-153">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="31f61-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="31f61-154">MOF</span><span class="sxs-lookup"><span data-stu-id="31f61-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31f61-155"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31f61-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f61-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="31f61-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f61-157">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WINSRType**</span><span class="sxs-lookup"><span data-stu-id="31f61-157">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="31f61-158">**Método Modify de la \_ clase MicrosoftDNS WINSRType**</span><span class="sxs-lookup"><span data-stu-id="31f61-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="31f61-159">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="31f61-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






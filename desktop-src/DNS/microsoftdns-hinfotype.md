---
title: MicrosoftDNS_HINFOType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de información de host (HINFO).
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- DNS de la clase MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3298e5a7f90dbaee24e5014b1a3aab76ad6997
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658249"
---
# <a name="microsoftdns_hinfotype-class"></a><span data-ttu-id="ce411-105">MicrosoftDNS ( \_ clase HINFOType)</span><span class="sxs-lookup"><span data-stu-id="ce411-105">MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="ce411-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de información de host (HINFO).</span><span class="sxs-lookup"><span data-stu-id="ce411-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Host Information (HINFO) record.</span></span>

<span data-ttu-id="ce411-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="ce411-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce411-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce411-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a><span data-ttu-id="ce411-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce411-109">Members</span></span>

<span data-ttu-id="ce411-110">La clase **MicrosoftDNS \_ HINFOType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ce411-110">The **MicrosoftDNS\_HINFOType** class has these types of members:</span></span>

-   [<span data-ttu-id="ce411-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce411-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ce411-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce411-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ce411-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce411-113">Methods</span></span>

<span data-ttu-id="ce411-114">La clase **MicrosoftDNS \_ HINFOType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ce411-114">The **MicrosoftDNS\_HINFOType** class has these methods.</span></span>



| <span data-ttu-id="ce411-115">Método</span><span class="sxs-lookup"><span data-stu-id="ce411-115">Method</span></span>                             | <span data-ttu-id="ce411-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce411-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce411-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="ce411-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="ce411-118">Crea una instancia de un HINFO de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y los tipos de sistema operativo y CPU del host.</span><span class="sxs-lookup"><span data-stu-id="ce411-118">Instantiates an HINFO of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the host's CPU and operating system types.</span></span> <span data-ttu-id="ce411-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="ce411-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="ce411-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="ce411-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="ce411-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="ce411-121">**Modify**</span></span>                         | <span data-ttu-id="ce411-122">Actualiza el TTL, la CPU y el sistema operativo a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="ce411-122">Updates the TTL, CPU, and operating system to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="ce411-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="ce411-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="ce411-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="ce411-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="ce411-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="ce411-125">Qualifiers: Implemented</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="ce411-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce411-126">Properties</span></span>

<span data-ttu-id="ce411-127">La clase **MicrosoftDNS \_ HINFOType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ce411-127">The **MicrosoftDNS\_HINFOType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce411-128">**CPU**</span><span class="sxs-lookup"><span data-stu-id="ce411-128">**CPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce411-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ce411-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce411-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ce411-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce411-131">Tipo de CPU del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="ce411-131">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="ce411-132">**SISTEMA OPERATIVO**</span><span class="sxs-lookup"><span data-stu-id="ce411-132">**OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce411-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ce411-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce411-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ce411-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce411-135">Sistema operativo del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="ce411-135">Operating system of the record owner.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce411-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce411-136">Requirements</span></span>



| <span data-ttu-id="ce411-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce411-137">Requirement</span></span> | <span data-ttu-id="ce411-138">Value</span><span class="sxs-lookup"><span data-stu-id="ce411-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce411-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce411-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ce411-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ce411-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ce411-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce411-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ce411-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce411-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ce411-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ce411-143">Namespace</span></span><br/>                | <span data-ttu-id="ce411-144">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="ce411-144">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ce411-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ce411-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce411-146"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce411-146"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce411-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce411-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce411-148">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS HINFOType**</span><span class="sxs-lookup"><span data-stu-id="ce411-148">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ce411-149">**Método Modify de la \_ clase MicrosoftDNS HINFOType**</span><span class="sxs-lookup"><span data-stu-id="ce411-149">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="ce411-150">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ce411-150">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






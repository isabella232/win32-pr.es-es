---
title: MicrosoftDNS_RTType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de ruta a través de (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- DNS de la clase MicrosoftDNS_RTType
- MicrosoftDNS_RTType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996543"
---
# <a name="microsoftdns_rttype-class"></a><span data-ttu-id="a468c-105">MicrosoftDNS ( \_ clase RTType)</span><span class="sxs-lookup"><span data-stu-id="a468c-105">MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="a468c-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de ruta a través de (RT).</span><span class="sxs-lookup"><span data-stu-id="a468c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Route Through (RT) record.</span></span>

<span data-ttu-id="a468c-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="a468c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a468c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a468c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a><span data-ttu-id="a468c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a468c-109">Members</span></span>

<span data-ttu-id="a468c-110">La clase **MicrosoftDNS \_ RTType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a468c-110">The **MicrosoftDNS\_RTType** class has these types of members:</span></span>

-   [<span data-ttu-id="a468c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a468c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a468c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a468c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a468c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a468c-113">Methods</span></span>

<span data-ttu-id="a468c-114">La clase **MicrosoftDNS \_ RTType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a468c-114">The **MicrosoftDNS\_RTType** class has these methods.</span></span>



| <span data-ttu-id="a468c-115">Método</span><span class="sxs-lookup"><span data-stu-id="a468c-115">Method</span></span>                             | <span data-ttu-id="a468c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a468c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a468c-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a468c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="a468c-118">Crea una instancia de un tipo RT de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el propietario o el nombre de host, la clase (valor predeterminado = IN), el valor de período de vida, la preferencia de registro y el nombre de host intermedio.</span><span class="sxs-lookup"><span data-stu-id="a468c-118">Instantiates an RT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/host Name, class (default = IN), time-to-live value, record preference and intermediate host name.</span></span> <span data-ttu-id="a468c-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="a468c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="a468c-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="a468c-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="a468c-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="a468c-121">**Modify**</span></span>                         | <span data-ttu-id="a468c-122">Actualiza el TTL, la preferencia y el host intermedio a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="a468c-122">Updates the TTL, Preference, and Intermediate Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="a468c-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="a468c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="a468c-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="a468c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="a468c-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="a468c-125">Qualifiers: Implemented</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="a468c-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a468c-126">Properties</span></span>

<span data-ttu-id="a468c-127">La clase **MicrosoftDNS \_ RTType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a468c-127">The **MicrosoftDNS\_RTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a468c-128">**IntermediateHost**</span><span class="sxs-lookup"><span data-stu-id="a468c-128">**IntermediateHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a468c-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a468c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a468c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a468c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a468c-131">FQDN que especifica un host que actúa como intermediario para alcanzar el host especificado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="a468c-131">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="a468c-132">**Justifica**</span><span class="sxs-lookup"><span data-stu-id="a468c-132">**Preference**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a468c-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a468c-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a468c-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a468c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a468c-135">Preferencia asignada a este RR entre otros en el mismo propietario.</span><span class="sxs-lookup"><span data-stu-id="a468c-135">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="a468c-136">Se prefieren los valores inferiores.</span><span class="sxs-lookup"><span data-stu-id="a468c-136">Lower values are preferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a468c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a468c-137">Requirements</span></span>



| <span data-ttu-id="a468c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a468c-138">Requirement</span></span> | <span data-ttu-id="a468c-139">Value</span><span class="sxs-lookup"><span data-stu-id="a468c-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a468c-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a468c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a468c-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a468c-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a468c-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a468c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a468c-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a468c-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a468c-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a468c-144">Namespace</span></span><br/>                | <span data-ttu-id="a468c-145">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="a468c-145">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a468c-146">MOF</span><span class="sxs-lookup"><span data-stu-id="a468c-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a468c-147"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a468c-147"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a468c-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="a468c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a468c-149">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS RTType**</span><span class="sxs-lookup"><span data-stu-id="a468c-149">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a468c-150">**Método Modify de la \_ clase MicrosoftDNS RTType**</span><span class="sxs-lookup"><span data-stu-id="a468c-150">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="a468c-151">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a468c-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






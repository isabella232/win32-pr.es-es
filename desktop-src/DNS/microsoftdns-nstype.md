---
title: MicrosoftDNS_NSType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de servidor de nombres (NS).
ms.assetid: 8d229acd-bc47-4a32-b6f1-b784a48dc91a
keywords:
- DNS de la clase MicrosoftDNS_NSType
- MicrosoftDNS_NSType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
- MicrosoftDNS_NSType.Modify
- MicrosoftDNS_NSType.NSHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07155c36089e60b12aeea214b19cb8aca146005a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997165"
---
# <a name="microsoftdns_nstype-class"></a><span data-ttu-id="2b83e-105">MicrosoftDNS ( \_ clase NSType)</span><span class="sxs-lookup"><span data-stu-id="2b83e-105">MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="2b83e-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de servidor de nombres (NS).</span><span class="sxs-lookup"><span data-stu-id="2b83e-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Name Server (NS) record.</span></span>

<span data-ttu-id="2b83e-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="2b83e-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b83e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b83e-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_NSType : MicrosoftDNS_ResourceRecord
{
  string NSHost;
};
```

## <a name="members"></a><span data-ttu-id="2b83e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b83e-109">Members</span></span>

<span data-ttu-id="2b83e-110">La clase **MicrosoftDNS \_ NSType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2b83e-110">The **MicrosoftDNS\_NSType** class has these types of members:</span></span>

-   [<span data-ttu-id="2b83e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b83e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2b83e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b83e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2b83e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b83e-113">Methods</span></span>

<span data-ttu-id="2b83e-114">La clase **MicrosoftDNS \_ NSType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2b83e-114">The **MicrosoftDNS\_NSType** class has these methods.</span></span>



| <span data-ttu-id="2b83e-115">Método</span><span class="sxs-lookup"><span data-stu-id="2b83e-115">Method</span></span>                             | <span data-ttu-id="2b83e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b83e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b83e-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2b83e-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="2b83e-118">Crea una instancia de un registro de recursos de DNS NS en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el host con autoridad para el dominio.</span><span class="sxs-lookup"><span data-stu-id="2b83e-118">Instantiates a DNS NS Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the host with authority for the domain.</span></span> <span data-ttu-id="2b83e-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="2b83e-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="2b83e-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="2b83e-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="2b83e-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="2b83e-121">**Modify**</span></span>                         | <span data-ttu-id="2b83e-122">Actualiza el TTL y el host NS a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="2b83e-122">Updates the TTL and NS Host to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="2b83e-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="2b83e-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="2b83e-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="2b83e-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="2b83e-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="2b83e-125">Qualifiers: Implemented</span></span><br/>                               |



 

### <a name="properties"></a><span data-ttu-id="2b83e-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b83e-126">Properties</span></span>

<span data-ttu-id="2b83e-127">La clase **MicrosoftDNS \_ NSType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2b83e-127">The **MicrosoftDNS\_NSType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b83e-128">**NSHost**</span><span class="sxs-lookup"><span data-stu-id="2b83e-128">**NSHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b83e-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2b83e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b83e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b83e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b83e-131">Host autoritativo para el dominio.</span><span class="sxs-lookup"><span data-stu-id="2b83e-131">Authoritative host for the domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b83e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b83e-132">Requirements</span></span>



| <span data-ttu-id="2b83e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b83e-133">Requirement</span></span> | <span data-ttu-id="2b83e-134">Value</span><span class="sxs-lookup"><span data-stu-id="2b83e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b83e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b83e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2b83e-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2b83e-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2b83e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b83e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2b83e-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b83e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2b83e-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b83e-139">Namespace</span></span><br/>                | <span data-ttu-id="2b83e-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="2b83e-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2b83e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2b83e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b83e-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b83e-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b83e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b83e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b83e-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS NSType**</span><span class="sxs-lookup"><span data-stu-id="2b83e-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="2b83e-145">**Método Modify de la \_ clase MicrosoftDNS NSType**</span><span class="sxs-lookup"><span data-stu-id="2b83e-145">**Modify Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-modify.md)
</dt> <dt>

[<span data-ttu-id="2b83e-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="2b83e-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






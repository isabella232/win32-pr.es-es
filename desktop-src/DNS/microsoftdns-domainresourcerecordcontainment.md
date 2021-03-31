---
title: MicrosoftDNS_DomainResourceRecordContainment (clase)
description: La \_ clase MicrosoftDNS DomainResourceRecordContainment se usa para la contención de RR; cada instancia del \_ dominio MicrosoftDNS puede contener varias instancias de la \_ clase MicrosoftDNS ResourceRecord.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- DNS de la clase MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490648"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a><span data-ttu-id="eb9d1-105">MicrosoftDNS ( \_ clase DomainResourceRecordContainment)</span><span class="sxs-lookup"><span data-stu-id="eb9d1-105">MicrosoftDNS\_DomainResourceRecordContainment class</span></span>

<span data-ttu-id="eb9d1-106">La clase **MicrosoftDNS \_ DomainResourceRecordContainment** se usa para la contención de RR; cada instancia [**del \_ dominio MicrosoftDNS**](microsoftdns-domain.md) puede contener varias instancias de la clase [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9d1-106">The **MicrosoftDNS\_DomainResourceRecordContainment** class is used for RR containment; every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) may contain multiple instances of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span> <span data-ttu-id="eb9d1-107">Cada instancia de la clase **MicrosoftDNS \_ ResourceRecord** pertenece a una única instancia de la clase de **\_ dominio microsoftdns** y se define como débil para esa instancia.</span><span class="sxs-lookup"><span data-stu-id="eb9d1-107">Every instance of the **MicrosoftDNS\_ResourceRecord** class belongs to a single instance of the **MicrosoftDNS\_Domain** class, and is defined to be weak to that instance.</span></span>

<span data-ttu-id="eb9d1-108">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="eb9d1-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9d1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb9d1-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="eb9d1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="eb9d1-110">Members</span></span>

<span data-ttu-id="eb9d1-111">La clase **MicrosoftDNS \_ DomainResourceRecordContainment** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eb9d1-111">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="eb9d1-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb9d1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb9d1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb9d1-113">Properties</span></span>

<span data-ttu-id="eb9d1-114">La clase **MicrosoftDNS \_ DomainResourceRecordContainment** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eb9d1-114">The **MicrosoftDNS\_DomainResourceRecordContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb9d1-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="eb9d1-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d1-116">Tipo de datos **: \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eb9d1-116">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d1-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9d1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9d1-118">Calificadores: clave, invalidación ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="eb9d1-118">Qualifiers: Key, Override("GroupComponent")</span></span>

<span data-ttu-id="eb9d1-119">Descripción: la zona, la memoria caché, el RootHints o el dominio que contiene directamente el registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb9d1-119">Description: The Zone, Cache, RootHints or Domain directly containing the Resource Record.</span></span>

<span data-ttu-id="eb9d1-120">Heredado del \_ componente CIM</span><span class="sxs-lookup"><span data-stu-id="eb9d1-120">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="eb9d1-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="eb9d1-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9d1-122">Tipo de datos: **MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="eb9d1-122">Data type: **MicrosoftDNS\_ResourceRecord**</span></span>
</dt> <dt>

<span data-ttu-id="eb9d1-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9d1-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9d1-124">Calificadores: clave, invalidación ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="eb9d1-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="eb9d1-125">Descripción: el registro de recursos contenido en un dominio, zona, caché o RootHints.</span><span class="sxs-lookup"><span data-stu-id="eb9d1-125">Description: The resource record contained in a Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="eb9d1-126">Heredado del \_ componente CIM.</span><span class="sxs-lookup"><span data-stu-id="eb9d1-126">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb9d1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb9d1-127">Requirements</span></span>



| <span data-ttu-id="eb9d1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb9d1-128">Requirement</span></span> | <span data-ttu-id="eb9d1-129">Value</span><span class="sxs-lookup"><span data-stu-id="eb9d1-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9d1-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb9d1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eb9d1-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="eb9d1-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eb9d1-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb9d1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eb9d1-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eb9d1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eb9d1-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb9d1-134">Namespace</span></span><br/>                | <span data-ttu-id="eb9d1-135">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="eb9d1-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="eb9d1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="eb9d1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb9d1-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb9d1-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb9d1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb9d1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9d1-139">**MicrosoftDNS \_ ServerDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="eb9d1-139">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="eb9d1-140">**MicrosoftDNS \_ DomainDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="eb9d1-140">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="eb9d1-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="eb9d1-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






---
title: MicrosoftDNS_DomainDomainContainment (clase)
description: La \_ clase MicrosoftDNS DomainDomainContainment se usa para la contención de dominio; Los dominios DNS pueden contener otros dominios DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- DNS de la clase MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079617"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a><span data-ttu-id="97c68-105">MicrosoftDNS ( \_ clase DomainDomainContainment)</span><span class="sxs-lookup"><span data-stu-id="97c68-105">MicrosoftDNS\_DomainDomainContainment class</span></span>

<span data-ttu-id="97c68-106">La clase **MicrosoftDNS \_ DomainDomainContainment** se usa para la contención de dominio; Los dominios DNS pueden contener otros dominios DNS.</span><span class="sxs-lookup"><span data-stu-id="97c68-106">The **MicrosoftDNS\_DomainDomainContainment** class is used for domain containment; DNS domains may contain other DNS domains.</span></span> <span data-ttu-id="97c68-107">Cada instancia de la clase de [**\_ dominio microsoftdns**](microsoftdns-domain.md) puede contener varias instancias del **\_ dominio microsoftdns**.</span><span class="sxs-lookup"><span data-stu-id="97c68-107">Every instance of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class may contain multiple other instances of **MicrosoftDNS\_Domain**.</span></span> <span data-ttu-id="97c68-108">Una instancia de un objeto de **\_ dominio microsoftdns** se encuentra directamente en no más de un **\_ dominio MicrosoftDNS** de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="97c68-108">An instance of a **MicrosoftDNS\_Domain** object is directly contained in no more than one higher level **MicrosoftDNS\_Domain**.</span></span>

<span data-ttu-id="97c68-109">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="97c68-109">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c68-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97c68-110">Syntax</span></span>

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="97c68-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="97c68-111">Members</span></span>

<span data-ttu-id="97c68-112">La clase **MicrosoftDNS \_ DomainDomainContainment** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="97c68-112">The **MicrosoftDNS\_DomainDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="97c68-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97c68-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97c68-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97c68-114">Properties</span></span>

<span data-ttu-id="97c68-115">La clase **MicrosoftDNS \_ DomainDomainContainment** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="97c68-115">The **MicrosoftDNS\_DomainDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97c68-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="97c68-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97c68-117">Tipo de datos **: \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="97c68-117">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="97c68-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97c68-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97c68-119">Calificadores: clave, máximo (1), invalidación ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="97c68-119">Qualifiers: Key, Max(1), Override("GroupComponent")</span></span>

<span data-ttu-id="97c68-120">Descripción: un dominio de nivel superior, zona, caché o RootHints.</span><span class="sxs-lookup"><span data-stu-id="97c68-120">Description: A higher level Domain, Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="97c68-121">Heredado del \_ componente CIM</span><span class="sxs-lookup"><span data-stu-id="97c68-121">Inherited from CIM\_Component</span></span>

</dd> <dt>

<span data-ttu-id="97c68-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="97c68-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97c68-123">Tipo de datos **: \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="97c68-123">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="97c68-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97c68-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97c68-125">Calificadores: clave, invalidación ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="97c68-125">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="97c68-126">Descripción: el dominio contenido en un dominio de nivel superior, zona, caché o RootHints.</span><span class="sxs-lookup"><span data-stu-id="97c68-126">Description: The Domain contained by a higher level Domain, Zone, Cache or RootHints.</span></span>

<span data-ttu-id="97c68-127">Heredado del \_ componente CIM.</span><span class="sxs-lookup"><span data-stu-id="97c68-127">Inherited from CIM\_Component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97c68-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c68-128">Requirements</span></span>



| <span data-ttu-id="97c68-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c68-129">Requirement</span></span> | <span data-ttu-id="97c68-130">Value</span><span class="sxs-lookup"><span data-stu-id="97c68-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c68-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97c68-131">Minimum supported client</span></span><br/> | <span data-ttu-id="97c68-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="97c68-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="97c68-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97c68-133">Minimum supported server</span></span><br/> | <span data-ttu-id="97c68-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="97c68-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="97c68-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="97c68-135">Namespace</span></span><br/>                | <span data-ttu-id="97c68-136">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="97c68-136">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="97c68-137">MOF</span><span class="sxs-lookup"><span data-stu-id="97c68-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97c68-138"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97c68-138"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c68-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="97c68-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c68-140">**MicrosoftDNS \_ DomainResourceRecordContainment**</span><span class="sxs-lookup"><span data-stu-id="97c68-140">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="97c68-141">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="97c68-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="97c68-142">**MicrosoftDNS \_ ServerDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="97c68-142">**MicrosoftDNS\_ServerDomainContainment**</span></span>](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 






---
title: MicrosoftDNS_ServerDomainContainment (clase)
description: Cada instancia de la \_ clase WMI de la Asociación de servidor microsoftdns puede contener varias instancias de la clase de dominio microsoftdns \_ .
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- DNS de la clase MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801351"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a><span data-ttu-id="01cda-105">MicrosoftDNS ( \_ clase ServerDomainContainment)</span><span class="sxs-lookup"><span data-stu-id="01cda-105">MicrosoftDNS\_ServerDomainContainment class</span></span>

<span data-ttu-id="01cda-106">Cada instancia de la clase WMI de la Asociación de [**\_ servidor microsoftdns**](microsoftdns-server.md) puede contener varias instancias de la clase de [**\_ dominio microsoftdns**](microsoftdns-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="01cda-106">Every instance of the [**MicrosoftDNS\_Server**](microsoftdns-server.md) association WMI class may contain multiple instances of the [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) class.</span></span> <span data-ttu-id="01cda-107">Cada instancia de la clase de **\_ dominio microsoftdns** pertenece a una única instancia de la clase de **\_ servidor microsoftdns** y se define como débil para ese servidor.</span><span class="sxs-lookup"><span data-stu-id="01cda-107">Every instance of the **MicrosoftDNS\_Domain** class belongs to a single instance of the **MicrosoftDNS\_Server** class, and is defined to be weak to that server.</span></span>

<span data-ttu-id="01cda-108">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="01cda-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01cda-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01cda-109">Syntax</span></span>

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="01cda-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="01cda-110">Members</span></span>

<span data-ttu-id="01cda-111">La clase **MicrosoftDNS \_ ServerDomainContainment** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01cda-111">The **MicrosoftDNS\_ServerDomainContainment** class has these types of members:</span></span>

-   [<span data-ttu-id="01cda-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01cda-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01cda-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01cda-113">Properties</span></span>

<span data-ttu-id="01cda-114">La clase **MicrosoftDNS \_ ServerDomainContainment** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01cda-114">The **MicrosoftDNS\_ServerDomainContainment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01cda-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="01cda-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01cda-116">Tipo de datos **: \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="01cda-116">Data type: **MicrosoftDNS\_Server**</span></span>
</dt> <dt>

<span data-ttu-id="01cda-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01cda-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01cda-118">Calificadores: clave, invalidación ("GroupComponent"), mín. (1), máx. (1)</span><span class="sxs-lookup"><span data-stu-id="01cda-118">Qualifiers: Key, Override ("GroupComponent"), Min (1), Max (1)</span></span>

<span data-ttu-id="01cda-119">Descripción: el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="01cda-119">Description: The DNS Server.</span></span>

<span data-ttu-id="01cda-120">Heredado **del \_ componente CIM**.</span><span class="sxs-lookup"><span data-stu-id="01cda-120">Inherited from **CIM\_Component**.</span></span>

</dd> <dt>

<span data-ttu-id="01cda-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="01cda-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01cda-122">Tipo de datos **: \_ dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="01cda-122">Data type: **MicrosoftDNS\_Domain**</span></span>
</dt> <dt>

<span data-ttu-id="01cda-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01cda-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01cda-124">Calificadores: clave, invalidación ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="01cda-124">Qualifiers: Key, Override("PartComponent")</span></span>

<span data-ttu-id="01cda-125">Descripción: dominio, zona, caché o RootHints administrado por el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="01cda-125">Description: A Domain, Zone, Cache, or RootHints managed by the DNS Server.</span></span>

<span data-ttu-id="01cda-126">Heredado **del \_ componente CIM**.</span><span class="sxs-lookup"><span data-stu-id="01cda-126">Inherited from **CIM\_Component**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01cda-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01cda-127">Remarks</span></span>

<span data-ttu-id="01cda-128">La clase **MicrosoftDNS \_ ServerDomainContainment** se deriva de la clase del **\_ componente CIM** .</span><span class="sxs-lookup"><span data-stu-id="01cda-128">The **MicrosoftDNS\_ServerDomainContainment** class is derived from the **CIM\_Component** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="01cda-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01cda-129">Requirements</span></span>



| <span data-ttu-id="01cda-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="01cda-130">Requirement</span></span> | <span data-ttu-id="01cda-131">Value</span><span class="sxs-lookup"><span data-stu-id="01cda-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01cda-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01cda-132">Minimum supported client</span></span><br/> | <span data-ttu-id="01cda-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="01cda-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="01cda-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01cda-134">Minimum supported server</span></span><br/> | <span data-ttu-id="01cda-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01cda-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="01cda-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01cda-136">Namespace</span></span><br/>                | <span data-ttu-id="01cda-137">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="01cda-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="01cda-138">MOF</span><span class="sxs-lookup"><span data-stu-id="01cda-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01cda-139"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01cda-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01cda-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="01cda-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01cda-141">**MicrosoftDNS \_ DomainDomainContainment**</span><span class="sxs-lookup"><span data-stu-id="01cda-141">**MicrosoftDNS\_DomainDomainContainment**</span></span>](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[<span data-ttu-id="01cda-142">**MicrosoftDNS \_ DomainResourceRecordContainment**</span><span class="sxs-lookup"><span data-stu-id="01cda-142">**MicrosoftDNS\_DomainResourceRecordContainment**</span></span>](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[<span data-ttu-id="01cda-143">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="01cda-143">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






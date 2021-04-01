---
title: MicrosoftDNS_Domain (clase)
description: La \_ clase de dominio MicrosoftDNS representa un dominio en una jerarquía de DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- DNS de la clase MicrosoftDNS_Domain
- MicrosoftDNS_Domain de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150295"
---
# <a name="microsoftdns_domain-class"></a><span data-ttu-id="dd651-105">\_Clase de dominio MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="dd651-105">MicrosoftDNS\_Domain class</span></span>

<span data-ttu-id="dd651-106">La clase de **\_ dominio MicrosoftDNS** representa un dominio en una jerarquía de DNS.</span><span class="sxs-lookup"><span data-stu-id="dd651-106">The **MicrosoftDNS\_Domain** class represents a Domain in a DNS hierarchy.</span></span>

<span data-ttu-id="dd651-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="dd651-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd651-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd651-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="dd651-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd651-109">Members</span></span>

<span data-ttu-id="dd651-110">La clase de **\_ dominio MicrosoftDNS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dd651-110">The **MicrosoftDNS\_Domain** class has these types of members:</span></span>

-   [<span data-ttu-id="dd651-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd651-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd651-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd651-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd651-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd651-113">Methods</span></span>

<span data-ttu-id="dd651-114">La clase de **\_ dominio MicrosoftDNS** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dd651-114">The **MicrosoftDNS\_Domain** class has these methods.</span></span>



| <span data-ttu-id="dd651-115">Método</span><span class="sxs-lookup"><span data-stu-id="dd651-115">Method</span></span>                   | <span data-ttu-id="dd651-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd651-116">Description</span></span>                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd651-117">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="dd651-117">**GetDistinguishedName**</span></span> | <span data-ttu-id="dd651-118">Obtiene el nombre distintivo de DS para la zona.</span><span class="sxs-lookup"><span data-stu-id="dd651-118">Obtains DS distinguished Name for the zone.</span></span> <br/> <span data-ttu-id="dd651-119">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="dd651-119">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd651-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd651-120">Properties</span></span>

<span data-ttu-id="dd651-121">La clase de **\_ dominio MicrosoftDNS** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd651-121">The **MicrosoftDNS\_Domain** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd651-122">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="dd651-122">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd651-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd651-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd651-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd651-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd651-125">Nombre del contenedor del dominio, que podría ser una zona, caché o RootHints.</span><span class="sxs-lookup"><span data-stu-id="dd651-125">Name of the container of the domain, which could be a Zone, Cache, or RootHints.</span></span>

<span data-ttu-id="dd651-126">En los casos en los que el contenedor es una zona (una instancia de la clase de [**\_ zona MicrosoftDNS**](microsoftdns-zone.md) ), esta propiedad contiene el FQDN de la zona.</span><span class="sxs-lookup"><span data-stu-id="dd651-126">In cases where the Container is a Zone (an instance of the [**MicrosoftDNS\_Zone**](microsoftdns-zone.md) class), this property contains the FQDN of the Zone.</span></span>

<span data-ttu-id="dd651-127">Cuando el contenedor es la zona raíz, \\ \\ se debe usar la cadena.</span><span class="sxs-lookup"><span data-stu-id="dd651-127">When the Container is the root zone, the string \\.\\ should be used.</span></span>

<span data-ttu-id="dd651-128">En los casos en los que el contenedor es la memoria caché de DNS de los registros de recursos (una instancia de la clase de [**\_ caché MicrosoftDNS**](microsoftdns-cache.md) ), esta propiedad se establece en la cadena \\ . Caché \\ .</span><span class="sxs-lookup"><span data-stu-id="dd651-128">In cases where the Container is the DNS cache of resource records (an instance of the [**MicrosoftDNS\_Cache**](microsoftdns-cache.md) class), this property is set to the string \\..Cache\\.</span></span>

<span data-ttu-id="dd651-129">Si el contenedor es RootHints (una instancia de la clase [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md) ), esta propiedad debe establecerse en \\ . RootHints \\ .</span><span class="sxs-lookup"><span data-stu-id="dd651-129">If the Container is RootHints (an instance of the [**MicrosoftDNS\_RootHints**](microsoftdns-roothints.md) class), this property should be set to \\..RootHints\\.</span></span>

</dd> <dt>

<span data-ttu-id="dd651-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="dd651-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd651-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd651-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd651-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd651-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd651-133">FQDN o dirección IP del servidor DNS que contiene el dominio.</span><span class="sxs-lookup"><span data-stu-id="dd651-133">FQDN or IP address of the DNS Server that contains the domain.</span></span>

</dd> <dt>

<span data-ttu-id="dd651-134">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="dd651-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd651-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd651-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd651-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd651-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd651-137">FQDN del dominio.</span><span class="sxs-lookup"><span data-stu-id="dd651-137">FQDN of the domain.</span></span>

<span data-ttu-id="dd651-138">En el caso de instancias de caché DNS o RootHints, las cadenas \\ . Almacenar en caché \\ y \\ .. \\ Se debe usar RootHints, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="dd651-138">For instances of DNS Cache or RootHints, the strings \\..Cache\\ and \\..RootHints\\ should be used, respectively.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd651-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd651-139">Requirements</span></span>



| <span data-ttu-id="dd651-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd651-140">Requirement</span></span> | <span data-ttu-id="dd651-141">Value</span><span class="sxs-lookup"><span data-stu-id="dd651-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd651-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd651-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dd651-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dd651-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dd651-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd651-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dd651-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd651-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dd651-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd651-146">Namespace</span></span><br/>                | <span data-ttu-id="dd651-147">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="dd651-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dd651-148">MOF</span><span class="sxs-lookup"><span data-stu-id="dd651-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd651-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd651-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd651-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd651-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd651-151">**Método GetDistinguishedName de la \_ clase de dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="dd651-151">**GetDistinguishedName Method of the MicrosoftDNS\_Domain Class**</span></span>](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 






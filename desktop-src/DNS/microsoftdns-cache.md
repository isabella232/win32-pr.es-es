---
title: MicrosoftDNS_Cache (clase)
description: La \_ clase de caché MicrosoftDNS describe una caché existente en un servidor DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- DNS de la clase MicrosoftDNS_Cache
- MicrosoftDNS_Cache de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079382"
---
# <a name="microsoftdns_cache-class"></a><span data-ttu-id="19e69-105">\_Clase de caché MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="19e69-105">MicrosoftDNS\_Cache class</span></span>

<span data-ttu-id="19e69-106">La clase de **\_ caché MicrosoftDNS** describe una caché existente en un servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="19e69-106">The **MicrosoftDNS\_Cache** class describes a cache existing on a DNS Server.</span></span> <span data-ttu-id="19e69-107">Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real.</span><span class="sxs-lookup"><span data-stu-id="19e69-107">This class simplifies visualizing the containment of DNS objects, rather than representing a real object.</span></span> <span data-ttu-id="19e69-108">La clase de **\_ caché MicrosoftDNS** es un contenedor para los registros de recursos almacenados en memoria caché por el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="19e69-108">The **MicrosoftDNS\_Cache** class is a container for the resource records cached by the DNS Server.</span></span> <span data-ttu-id="19e69-109">No lo confunda con un archivo caché que contiene sugerencias de raíz.</span><span class="sxs-lookup"><span data-stu-id="19e69-109">Do not confuse this with a Cache file that contains root hints.</span></span>

<span data-ttu-id="19e69-110">Cada instancia de la clase **de \_ caché MicrosoftDNS** debe asignarse exactamente a un servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="19e69-110">Every instance of the class **MicrosoftDNS\_Cache** must be assigned to exactly one DNS Server.</span></span> <span data-ttu-id="19e69-111">Puede estar asociado a varias instancias de las clases de [**\_ dominio Microsoftdns**](microsoftdns-domain.md) o [**microsoftdns \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="19e69-111">It may be associated with multiple instances of [**MicrosoftDNS\_Domain**](microsoftdns-domain.md) or [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) classes.</span></span>

<span data-ttu-id="19e69-112">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="19e69-112">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e69-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19e69-113">Syntax</span></span>

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a><span data-ttu-id="19e69-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="19e69-114">Members</span></span>

<span data-ttu-id="19e69-115">La clase de **\_ caché MicrosoftDNS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="19e69-115">The **MicrosoftDNS\_Cache** class has these types of members:</span></span>

-   [<span data-ttu-id="19e69-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="19e69-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="19e69-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="19e69-117">Methods</span></span>

<span data-ttu-id="19e69-118">La clase de **\_ caché MicrosoftDNS** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="19e69-118">The **MicrosoftDNS\_Cache** class has these methods.</span></span>



| <span data-ttu-id="19e69-119">Método</span><span class="sxs-lookup"><span data-stu-id="19e69-119">Method</span></span>                   | <span data-ttu-id="19e69-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="19e69-120">Description</span></span>                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e69-121">**ClearCache**</span><span class="sxs-lookup"><span data-stu-id="19e69-121">**ClearCache**</span></span>           | <span data-ttu-id="19e69-122">Borra la memoria caché del servidor DNS de los registros de recursos.</span><span class="sxs-lookup"><span data-stu-id="19e69-122">Clears the DNS Server cache of resource records.</span></span> <br/> <span data-ttu-id="19e69-123">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="19e69-123">Qualifiers: Implemented</span></span><br/> |
| <span data-ttu-id="19e69-124">**GetDistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="19e69-124">**GetDistinguishedName**</span></span> | <span data-ttu-id="19e69-125">Recupera el nombre distintivo de la zona.</span><span class="sxs-lookup"><span data-stu-id="19e69-125">Retrieves the distinguished name for the zone.</span></span> <br/> <span data-ttu-id="19e69-126">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="19e69-126">Qualifiers: Implemented</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="19e69-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19e69-127">Requirements</span></span>



| <span data-ttu-id="19e69-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="19e69-128">Requirement</span></span> | <span data-ttu-id="19e69-129">Value</span><span class="sxs-lookup"><span data-stu-id="19e69-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19e69-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19e69-130">Minimum supported client</span></span><br/> | <span data-ttu-id="19e69-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="19e69-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="19e69-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19e69-132">Minimum supported server</span></span><br/> | <span data-ttu-id="19e69-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="19e69-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="19e69-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19e69-134">Namespace</span></span><br/>                | <span data-ttu-id="19e69-135">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="19e69-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="19e69-136">MOF</span><span class="sxs-lookup"><span data-stu-id="19e69-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19e69-137"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19e69-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e69-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="19e69-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e69-139">**\_Dominio MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="19e69-139">**MicrosoftDNS\_Domain**</span></span>](microsoftdns-domain.md)
</dt> <dt>

[<span data-ttu-id="19e69-140">**Método ClearCache de la \_ clase cache MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="19e69-140">**ClearCache Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-clearcache.md)
</dt> <dt>

[<span data-ttu-id="19e69-141">**Método GetDistinguishedName de la \_ clase cache MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="19e69-141">**GetDistinguishedName Method of the MicrosoftDNS\_Cache Class**</span></span>](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 






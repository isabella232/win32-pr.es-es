---
title: atributo MS-DNS-NSEC3-usuario-Salt
description: Atributo que define una cadena de sal de NSEC3 especificada por el usuario que se va a usar al firmar la zona DNS. Si está vacío, se usará el valor Salt aleatorio.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DNS-NSEC3-usuario-sal
- msDN-NSEC3UserSalt atributo AD Schema
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d28acb28dec95ef13afc37f9d7f26d713d5cf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804717"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a><span data-ttu-id="334fd-106">atributo MS-DNS-NSEC3-usuario-Salt</span><span class="sxs-lookup"><span data-stu-id="334fd-106">ms-DNS-NSEC3-User-Salt attribute</span></span>

<span data-ttu-id="334fd-107">Atributo que define una cadena de sal de NSEC3 especificada por el usuario que se va a usar al firmar la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="334fd-107">An attribute that defines a user-specified NSEC3 salt string to use when signing the DNS zone.</span></span> <span data-ttu-id="334fd-108">Si está vacío, se usará el valor Salt aleatorio.</span><span class="sxs-lookup"><span data-stu-id="334fd-108">If empty, random salt will be used.</span></span>



| <span data-ttu-id="334fd-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="334fd-109">Entry</span></span> | <span data-ttu-id="334fd-110">Value</span><span class="sxs-lookup"><span data-stu-id="334fd-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="334fd-111">CN</span><span class="sxs-lookup"><span data-stu-id="334fd-111">CN</span></span>                | <span data-ttu-id="334fd-112">MS-DNS-NSEC3-usuario-sal</span><span class="sxs-lookup"><span data-stu-id="334fd-112">ms-DNS-NSEC3-User-Salt</span></span>                      |
| <span data-ttu-id="334fd-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="334fd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="334fd-114">msDN: NSEC3UserSalt</span><span class="sxs-lookup"><span data-stu-id="334fd-114">msDNS-NSEC3UserSalt</span></span>                         |
| <span data-ttu-id="334fd-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="334fd-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="334fd-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="334fd-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="334fd-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="334fd-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="334fd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="334fd-118">Attribute-Id</span></span>      | <span data-ttu-id="334fd-119">1.2.840.113556.1.4.2148</span><span class="sxs-lookup"><span data-stu-id="334fd-119">1.2.840.113556.1.4.2148</span></span>                     |
| <span data-ttu-id="334fd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="334fd-120">System-Id-Guid</span></span>    | <span data-ttu-id="334fd-121">aff16770-9622-4fbc-a128-3088777605b9</span><span class="sxs-lookup"><span data-stu-id="334fd-121">aff16770-9622-4fbc-a128-3088777605b9</span></span>        |
| <span data-ttu-id="334fd-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="334fd-122">Syntax</span></span>            | [<span data-ttu-id="334fd-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="334fd-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="334fd-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="334fd-124">Implementations</span></span>

-   [<span data-ttu-id="334fd-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="334fd-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="334fd-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="334fd-126">Windows Server 2012</span></span>



| <span data-ttu-id="334fd-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="334fd-127">Entry</span></span> | <span data-ttu-id="334fd-128">Value</span><span class="sxs-lookup"><span data-stu-id="334fd-128">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="334fd-129">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="334fd-129">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="334fd-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="334fd-130">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="334fd-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="334fd-131">System-Only</span></span>            | <span data-ttu-id="334fd-132">False</span><span class="sxs-lookup"><span data-stu-id="334fd-132">False</span></span>                                    |
| <span data-ttu-id="334fd-133">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="334fd-133">Is-Single-Valued</span></span>       | <span data-ttu-id="334fd-134">True</span><span class="sxs-lookup"><span data-stu-id="334fd-134">True</span></span>                                     |
| <span data-ttu-id="334fd-135">Está indexado</span><span class="sxs-lookup"><span data-stu-id="334fd-135">Is Indexed</span></span>             | <span data-ttu-id="334fd-136">False</span><span class="sxs-lookup"><span data-stu-id="334fd-136">False</span></span>                                    |
| <span data-ttu-id="334fd-137">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="334fd-137">In Global Catalog</span></span>      | <span data-ttu-id="334fd-138">False</span><span class="sxs-lookup"><span data-stu-id="334fd-138">False</span></span>                                    |
| <span data-ttu-id="334fd-139">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="334fd-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="334fd-140">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="334fd-140">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="334fd-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="334fd-141">Range-Lower</span></span>            | <span data-ttu-id="334fd-142">0</span><span class="sxs-lookup"><span data-stu-id="334fd-142">0</span></span>                                        |
| <span data-ttu-id="334fd-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="334fd-143">Range-Upper</span></span>            | <span data-ttu-id="334fd-144">510</span><span class="sxs-lookup"><span data-stu-id="334fd-144">510</span></span>                                      |
| <span data-ttu-id="334fd-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="334fd-145">Search-Flags</span></span>           | <span data-ttu-id="334fd-146">0x00000008</span><span class="sxs-lookup"><span data-stu-id="334fd-146">0x00000008</span></span>                               |
| <span data-ttu-id="334fd-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="334fd-147">System-Flags</span></span>           | <span data-ttu-id="334fd-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="334fd-148">0x00000010</span></span>                               |
| <span data-ttu-id="334fd-149">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="334fd-149">Classes used in</span></span>        | [<span data-ttu-id="334fd-150">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="334fd-150">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 






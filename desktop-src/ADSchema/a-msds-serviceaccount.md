---
title: atributo de la cuenta de servicio MS-DS
description: El FPO que representa la cuenta de servicio de ADAM.
ms.assetid: 9f93ed27-fb3f-4b37-b2a5-cf2e85b9d507
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de cuenta de servicio de MS-DS
- Esquema de AD de atributo msDS-ServiceAccount
topic_type:
- apiref
api_name:
- ms-DS-Service-Account
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315f5e5e9edd218b26da6ff73ccb5b4e6a4fc8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997554"
---
# <a name="ms-ds-service-account-attribute"></a><span data-ttu-id="88178-105">atributo de la cuenta de servicio MS-DS</span><span class="sxs-lookup"><span data-stu-id="88178-105">ms-DS-Service-Account attribute</span></span>

<span data-ttu-id="88178-106">El FPO que representa la cuenta de servicio de ADAM.</span><span class="sxs-lookup"><span data-stu-id="88178-106">The FPO that represents the ADAM service account.</span></span>



| <span data-ttu-id="88178-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="88178-107">Entry</span></span> | <span data-ttu-id="88178-108">Value</span><span class="sxs-lookup"><span data-stu-id="88178-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="88178-109">CN</span><span class="sxs-lookup"><span data-stu-id="88178-109">CN</span></span>                | <span data-ttu-id="88178-110">MS-DS-Service-Account</span><span class="sxs-lookup"><span data-stu-id="88178-110">ms-DS-Service-Account</span></span>                   |
| <span data-ttu-id="88178-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="88178-111">Ldap-Display-Name</span></span> | <span data-ttu-id="88178-112">msDS-ServiceAccount</span><span class="sxs-lookup"><span data-stu-id="88178-112">msDS-ServiceAccount</span></span>                     |
| <span data-ttu-id="88178-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="88178-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="88178-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="88178-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="88178-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="88178-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="88178-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88178-116">Attribute-Id</span></span>      | <span data-ttu-id="88178-117">1.2.840.113556.1.4.1866</span><span class="sxs-lookup"><span data-stu-id="88178-117">1.2.840.113556.1.4.1866</span></span>                 |
| <span data-ttu-id="88178-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88178-118">System-Id-Guid</span></span>    | <span data-ttu-id="88178-119">a7f73651-688b-401e-b0cf-9345857bab23</span><span class="sxs-lookup"><span data-stu-id="88178-119">a7f73651-688b-401e-b0cf-9345857bab23</span></span>    |
| <span data-ttu-id="88178-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88178-120">Syntax</span></span>            | [<span data-ttu-id="88178-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="88178-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="88178-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="88178-122">Implementations</span></span>

-   [<span data-ttu-id="88178-123">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="88178-123">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="88178-124">ADAM</span><span class="sxs-lookup"><span data-stu-id="88178-124">ADAM</span></span>



| <span data-ttu-id="88178-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="88178-125">Entry</span></span> | <span data-ttu-id="88178-126">Value</span><span class="sxs-lookup"><span data-stu-id="88178-126">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="88178-127">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88178-127">Link-Id</span></span>                | <span data-ttu-id="88178-128">2040</span><span class="sxs-lookup"><span data-stu-id="88178-128">2040</span></span>                                     |
| <span data-ttu-id="88178-129">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88178-129">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="88178-130">System-Only</span><span class="sxs-lookup"><span data-stu-id="88178-130">System-Only</span></span>            | <span data-ttu-id="88178-131">True</span><span class="sxs-lookup"><span data-stu-id="88178-131">True</span></span>                                     |
| <span data-ttu-id="88178-132">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88178-132">Is-Single-Valued</span></span>       | <span data-ttu-id="88178-133">False</span><span class="sxs-lookup"><span data-stu-id="88178-133">False</span></span>                                    |
| <span data-ttu-id="88178-134">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88178-134">Is Indexed</span></span>             | <span data-ttu-id="88178-135">False</span><span class="sxs-lookup"><span data-stu-id="88178-135">False</span></span>                                    |
| <span data-ttu-id="88178-136">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88178-136">In Global Catalog</span></span>      | <span data-ttu-id="88178-137">False</span><span class="sxs-lookup"><span data-stu-id="88178-137">False</span></span>                                    |
| <span data-ttu-id="88178-138">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88178-138">NT-Security-Descriptor</span></span> | <span data-ttu-id="88178-139">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88178-139">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="88178-140">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88178-140">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="88178-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88178-141">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="88178-142">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88178-142">Search-Flags</span></span>           | <span data-ttu-id="88178-143">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88178-143">0x00000000</span></span>                               |
| <span data-ttu-id="88178-144">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88178-144">System-Flags</span></span>           | <span data-ttu-id="88178-145">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88178-145">0x00000010</span></span>                               |
| <span data-ttu-id="88178-146">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88178-146">Classes used in</span></span>        | [<span data-ttu-id="88178-147">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="88178-147">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 






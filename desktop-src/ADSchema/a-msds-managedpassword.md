---
title: atributo MS-DS-ManagedPassword
description: Este atributo construido devuelve un BLOB que contiene la contraseña anterior y actual de texto no cifrado, TimeUntilEpochExpires y TimeUntilNextScheduledUpdate para un grupo MSA.
ms.assetid: bcabb20f-46f3-4c15-b71b-a8dfc43678bc
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-ManagedPassword
- Esquema de AD de atributo msDS-ManagedPassword
topic_type:
- apiref
api_name:
- ms-DS-ManagedPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a440f1849e01ae4930b72441f75b17ce51a0566b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151663"
---
# <a name="ms-ds-managedpassword-attribute"></a><span data-ttu-id="f15c3-105">atributo MS-DS-ManagedPassword</span><span class="sxs-lookup"><span data-stu-id="f15c3-105">ms-DS-ManagedPassword attribute</span></span>

<span data-ttu-id="f15c3-106">Este atributo construido devuelve un BLOB que contiene la contraseña anterior y actual de texto no cifrado, TimeUntilEpochExpires y TimeUntilNextScheduledUpdate para un grupo MSA.</span><span class="sxs-lookup"><span data-stu-id="f15c3-106">This constructed attribute returns a blob that contains the clear-text previous and current password, TimeUntilEpochExpires, and TimeUntilNextScheduledUpdate for a group MSA.</span></span>



| <span data-ttu-id="f15c3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f15c3-107">Entry</span></span> | <span data-ttu-id="f15c3-108">Value</span><span class="sxs-lookup"><span data-stu-id="f15c3-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f15c3-109">CN</span><span class="sxs-lookup"><span data-stu-id="f15c3-109">CN</span></span>                | <span data-ttu-id="f15c3-110">MS-DS-ManagedPassword</span><span class="sxs-lookup"><span data-stu-id="f15c3-110">ms-DS-ManagedPassword</span></span>                                 |
| <span data-ttu-id="f15c3-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f15c3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f15c3-112">msDS-ManagedPassword</span><span class="sxs-lookup"><span data-stu-id="f15c3-112">msDS-ManagedPassword</span></span>                                  |
| <span data-ttu-id="f15c3-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f15c3-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f15c3-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f15c3-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="f15c3-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f15c3-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f15c3-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f15c3-116">Attribute-Id</span></span>      | <span data-ttu-id="f15c3-117">1.2.840.113556.1.4.2196</span><span class="sxs-lookup"><span data-stu-id="f15c3-117">1.2.840.113556.1.4.2196</span></span>                               |
| <span data-ttu-id="f15c3-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f15c3-118">System-Id-Guid</span></span>    | <span data-ttu-id="f15c3-119">e362ed86-b728-0842-b27d-2dea7a9df218</span><span class="sxs-lookup"><span data-stu-id="f15c3-119">e362ed86-b728-0842-b27d-2dea7a9df218</span></span>                  |
| <span data-ttu-id="f15c3-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f15c3-120">Syntax</span></span>            | [<span data-ttu-id="f15c3-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f15c3-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f15c3-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f15c3-122">Implementations</span></span>

-   [<span data-ttu-id="f15c3-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f15c3-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="f15c3-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f15c3-124">Windows Server 2012</span></span>



| <span data-ttu-id="f15c3-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="f15c3-125">Entry</span></span> | <span data-ttu-id="f15c3-126">Value</span><span class="sxs-lookup"><span data-stu-id="f15c3-126">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f15c3-127">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f15c3-127">Link-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="f15c3-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f15c3-128">MAPI-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="f15c3-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="f15c3-129">System-Only</span></span>            | <span data-ttu-id="f15c3-130">False</span><span class="sxs-lookup"><span data-stu-id="f15c3-130">False</span></span>                                                                                       |
| <span data-ttu-id="f15c3-131">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f15c3-131">Is-Single-Valued</span></span>       | <span data-ttu-id="f15c3-132">True</span><span class="sxs-lookup"><span data-stu-id="f15c3-132">True</span></span>                                                                                        |
| <span data-ttu-id="f15c3-133">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f15c3-133">Is Indexed</span></span>             | <span data-ttu-id="f15c3-134">False</span><span class="sxs-lookup"><span data-stu-id="f15c3-134">False</span></span>                                                                                       |
| <span data-ttu-id="f15c3-135">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f15c3-135">In Global Catalog</span></span>      | <span data-ttu-id="f15c3-136">False</span><span class="sxs-lookup"><span data-stu-id="f15c3-136">False</span></span>                                                                                       |
| <span data-ttu-id="f15c3-137">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f15c3-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="f15c3-138">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f15c3-138">O:BAG:BAD:S:</span></span>                                                                                |
| <span data-ttu-id="f15c3-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f15c3-139">Range-Lower</span></span>            | \-                                                                                          |
| <span data-ttu-id="f15c3-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f15c3-140">Range-Upper</span></span>            | \-                                                                                          |
| <span data-ttu-id="f15c3-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f15c3-141">Search-Flags</span></span>           | <span data-ttu-id="f15c3-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f15c3-142">0x00000000</span></span>                                                                                  |
| <span data-ttu-id="f15c3-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f15c3-143">System-Flags</span></span>           | <span data-ttu-id="f15c3-144">0x00000014</span><span class="sxs-lookup"><span data-stu-id="f15c3-144">0x00000014</span></span>                                                                                  |
| <span data-ttu-id="f15c3-145">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f15c3-145">Classes used in</span></span>        | [<span data-ttu-id="f15c3-146">**MS-DS-Group-Managed-Service-Account**</span><span class="sxs-lookup"><span data-stu-id="f15c3-146">**ms-DS-Group-Managed-Service-Account**</span></span>](c-msds-groupmanagedserviceaccount.md)<br/> |



 

 






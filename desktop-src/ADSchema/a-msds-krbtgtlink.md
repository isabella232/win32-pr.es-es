---
title: atributo MS-DS-KrbTgt-Link
description: Se usa con los RODC para definir qué \_ cuenta de krbtgt xxxx corresponde a cada RODC.
ms.assetid: 08c3e50f-7f2a-4746-86b6-77780316679c
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-KrbTgt-Link
- Esquema de AD de atributo msDS-KrbTgtLink
topic_type:
- apiref
api_name:
- ms-DS-KrbTgt-Link
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcf8ddfee6f15532e4dad91fc1e34e1f136ea99b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906201"
---
# <a name="ms-ds-krbtgt-link-attribute"></a><span data-ttu-id="5ef52-105">atributo MS-DS-KrbTgt-Link</span><span class="sxs-lookup"><span data-stu-id="5ef52-105">ms-DS-KrbTgt-Link attribute</span></span>

<span data-ttu-id="5ef52-106">Se usa con los RODC para definir qué \_ cuenta de krbtgt xxxx corresponde a cada RODC.</span><span class="sxs-lookup"><span data-stu-id="5ef52-106">Used with RODCs to define which krbtgt\_XXXX account corresponds to each RODC.</span></span>



| <span data-ttu-id="5ef52-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef52-107">Entry</span></span> | <span data-ttu-id="5ef52-108">Value</span><span class="sxs-lookup"><span data-stu-id="5ef52-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="5ef52-109">CN</span><span class="sxs-lookup"><span data-stu-id="5ef52-109">CN</span></span>                | <span data-ttu-id="5ef52-110">MS-DS-KrbTgt-Link</span><span class="sxs-lookup"><span data-stu-id="5ef52-110">ms-DS-KrbTgt-Link</span></span>                       |
| <span data-ttu-id="5ef52-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5ef52-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5ef52-112">msDS-KrbTgtLink</span><span class="sxs-lookup"><span data-stu-id="5ef52-112">msDS-KrbTgtLink</span></span>                         |
| <span data-ttu-id="5ef52-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5ef52-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="5ef52-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5ef52-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="5ef52-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5ef52-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="5ef52-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5ef52-116">Attribute-Id</span></span>      | <span data-ttu-id="5ef52-117">1.2.840.113556.1.4.1923</span><span class="sxs-lookup"><span data-stu-id="5ef52-117">1.2.840.113556.1.4.1923</span></span>                 |
| <span data-ttu-id="5ef52-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5ef52-118">System-Id-Guid</span></span>    | <span data-ttu-id="5ef52-119">778ff5c9-6f4e-4b74-856a-d68383313910</span><span class="sxs-lookup"><span data-stu-id="5ef52-119">778ff5c9-6f4e-4b74-856a-d68383313910</span></span>    |
| <span data-ttu-id="5ef52-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ef52-120">Syntax</span></span>            | [<span data-ttu-id="5ef52-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="5ef52-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="5ef52-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5ef52-122">Implementations</span></span>

-   [<span data-ttu-id="5ef52-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5ef52-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5ef52-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5ef52-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5ef52-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5ef52-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="5ef52-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ef52-126">Windows Server 2008</span></span>



| <span data-ttu-id="5ef52-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef52-127">Entry</span></span> | <span data-ttu-id="5ef52-128">Value</span><span class="sxs-lookup"><span data-stu-id="5ef52-128">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5ef52-129">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5ef52-129">Link-Id</span></span>                | <span data-ttu-id="5ef52-130">2100</span><span class="sxs-lookup"><span data-stu-id="5ef52-130">2100</span></span>                                      |
| <span data-ttu-id="5ef52-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ef52-131">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5ef52-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ef52-132">System-Only</span></span>            | <span data-ttu-id="5ef52-133">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-133">False</span></span>                                     |
| <span data-ttu-id="5ef52-134">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5ef52-134">Is-Single-Valued</span></span>       | <span data-ttu-id="5ef52-135">True</span><span class="sxs-lookup"><span data-stu-id="5ef52-135">True</span></span>                                      |
| <span data-ttu-id="5ef52-136">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5ef52-136">Is Indexed</span></span>             | <span data-ttu-id="5ef52-137">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-137">False</span></span>                                     |
| <span data-ttu-id="5ef52-138">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ef52-138">In Global Catalog</span></span>      | <span data-ttu-id="5ef52-139">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-139">False</span></span>                                     |
| <span data-ttu-id="5ef52-140">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5ef52-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ef52-141">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5ef52-141">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5ef52-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ef52-142">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5ef52-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ef52-143">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5ef52-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef52-144">Search-Flags</span></span>           | <span data-ttu-id="5ef52-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ef52-145">0x00000000</span></span>                                |
| <span data-ttu-id="5ef52-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef52-146">System-Flags</span></span>           | <span data-ttu-id="5ef52-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ef52-147">0x00000010</span></span>                                |
| <span data-ttu-id="5ef52-148">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5ef52-148">Classes used in</span></span>        | [<span data-ttu-id="5ef52-149">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5ef52-149">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5ef52-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ef52-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5ef52-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef52-151">Entry</span></span> | <span data-ttu-id="5ef52-152">Value</span><span class="sxs-lookup"><span data-stu-id="5ef52-152">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5ef52-153">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5ef52-153">Link-Id</span></span>                | <span data-ttu-id="5ef52-154">2100</span><span class="sxs-lookup"><span data-stu-id="5ef52-154">2100</span></span>                                      |
| <span data-ttu-id="5ef52-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ef52-155">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5ef52-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ef52-156">System-Only</span></span>            | <span data-ttu-id="5ef52-157">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-157">False</span></span>                                     |
| <span data-ttu-id="5ef52-158">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5ef52-158">Is-Single-Valued</span></span>       | <span data-ttu-id="5ef52-159">True</span><span class="sxs-lookup"><span data-stu-id="5ef52-159">True</span></span>                                      |
| <span data-ttu-id="5ef52-160">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5ef52-160">Is Indexed</span></span>             | <span data-ttu-id="5ef52-161">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-161">False</span></span>                                     |
| <span data-ttu-id="5ef52-162">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ef52-162">In Global Catalog</span></span>      | <span data-ttu-id="5ef52-163">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-163">False</span></span>                                     |
| <span data-ttu-id="5ef52-164">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5ef52-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ef52-165">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5ef52-165">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5ef52-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ef52-166">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5ef52-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ef52-167">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5ef52-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef52-168">Search-Flags</span></span>           | <span data-ttu-id="5ef52-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ef52-169">0x00000000</span></span>                                |
| <span data-ttu-id="5ef52-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef52-170">System-Flags</span></span>           | <span data-ttu-id="5ef52-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ef52-171">0x00000010</span></span>                                |
| <span data-ttu-id="5ef52-172">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5ef52-172">Classes used in</span></span>        | [<span data-ttu-id="5ef52-173">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5ef52-173">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5ef52-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ef52-174">Windows Server 2012</span></span>



| <span data-ttu-id="5ef52-175">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ef52-175">Entry</span></span> | <span data-ttu-id="5ef52-176">Value</span><span class="sxs-lookup"><span data-stu-id="5ef52-176">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="5ef52-177">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5ef52-177">Link-Id</span></span>                | <span data-ttu-id="5ef52-178">2100</span><span class="sxs-lookup"><span data-stu-id="5ef52-178">2100</span></span>                                      |
| <span data-ttu-id="5ef52-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5ef52-179">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="5ef52-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="5ef52-180">System-Only</span></span>            | <span data-ttu-id="5ef52-181">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-181">False</span></span>                                     |
| <span data-ttu-id="5ef52-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5ef52-182">Is-Single-Valued</span></span>       | <span data-ttu-id="5ef52-183">True</span><span class="sxs-lookup"><span data-stu-id="5ef52-183">True</span></span>                                      |
| <span data-ttu-id="5ef52-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5ef52-184">Is Indexed</span></span>             | <span data-ttu-id="5ef52-185">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-185">False</span></span>                                     |
| <span data-ttu-id="5ef52-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5ef52-186">In Global Catalog</span></span>      | <span data-ttu-id="5ef52-187">False</span><span class="sxs-lookup"><span data-stu-id="5ef52-187">False</span></span>                                     |
| <span data-ttu-id="5ef52-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5ef52-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="5ef52-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5ef52-189">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="5ef52-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5ef52-190">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="5ef52-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5ef52-191">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="5ef52-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef52-192">Search-Flags</span></span>           | <span data-ttu-id="5ef52-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5ef52-193">0x00000000</span></span>                                |
| <span data-ttu-id="5ef52-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5ef52-194">System-Flags</span></span>           | <span data-ttu-id="5ef52-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5ef52-195">0x00000010</span></span>                                |
| <span data-ttu-id="5ef52-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5ef52-196">Classes used in</span></span>        | [<span data-ttu-id="5ef52-197">**Computer**</span><span class="sxs-lookup"><span data-stu-id="5ef52-197">**Computer**</span></span>](c-computer.md)<br/> |



 

 






---
title: Atributo FRS-Replica-Set-Type
description: Se trata de un código que indica si se trata de un conjunto de réplicas de SYSVOL, un conjunto de réplicas DFS u otro conjunto de réplicas.
ms.assetid: 687a854f-ffa1-41f4-a515-5224759696ab
ms.tgt_platform: multiple
keywords:
- FRS-Replica-Set-Type atributo AD Schema
- fRSReplicaSetType esquema de AD de atributos
topic_type:
- apiref
api_name:
- FRS-Replica-Set-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18046c9b4edb794687d275af52e35416419c7e2d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905788"
---
# <a name="frs-replica-set-type-attribute"></a><span data-ttu-id="d0a00-105">Atributo FRS-Replica-Set-Type</span><span class="sxs-lookup"><span data-stu-id="d0a00-105">FRS-Replica-Set-Type attribute</span></span>

<span data-ttu-id="d0a00-106">Se trata de un código que indica si se trata de un conjunto de réplicas de SYSVOL, un conjunto de réplicas DFS u otro conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="d0a00-106">This is a code that indicates whether this is a sysvol replica set, a DFS replica set, or other replica set.</span></span>



| <span data-ttu-id="d0a00-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0a00-107">Entry</span></span> | <span data-ttu-id="d0a00-108">Value</span><span class="sxs-lookup"><span data-stu-id="d0a00-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d0a00-109">CN</span><span class="sxs-lookup"><span data-stu-id="d0a00-109">CN</span></span>                | <span data-ttu-id="d0a00-110">FRS-Replica-Set-Type</span><span class="sxs-lookup"><span data-stu-id="d0a00-110">FRS-Replica-Set-Type</span></span>                 |
| <span data-ttu-id="d0a00-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d0a00-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d0a00-112">fRSReplicaSetType</span><span class="sxs-lookup"><span data-stu-id="d0a00-112">fRSReplicaSetType</span></span>                    |
| <span data-ttu-id="d0a00-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d0a00-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="d0a00-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d0a00-114">Update Privilege</span></span>  | <span data-ttu-id="d0a00-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="d0a00-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="d0a00-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d0a00-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d0a00-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d0a00-117">Attribute-Id</span></span>      | <span data-ttu-id="d0a00-118">1.2.840.113556.1.4.31</span><span class="sxs-lookup"><span data-stu-id="d0a00-118">1.2.840.113556.1.4.31</span></span>                |
| <span data-ttu-id="d0a00-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d0a00-119">System-Id-Guid</span></span>    | <span data-ttu-id="d0a00-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d0a00-120">26d9736b-6070-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="d0a00-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0a00-121">Syntax</span></span>            | [<span data-ttu-id="d0a00-122">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="d0a00-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d0a00-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d0a00-123">Implementations</span></span>

-   [<span data-ttu-id="d0a00-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d0a00-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d0a00-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d0a00-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d0a00-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d0a00-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d0a00-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d0a00-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d0a00-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d0a00-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d0a00-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d0a00-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d0a00-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0a00-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d0a00-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0a00-131">Entry</span></span> | <span data-ttu-id="d0a00-132">Value</span><span class="sxs-lookup"><span data-stu-id="d0a00-132">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0a00-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0a00-133">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0a00-134">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0a00-135">System-Only</span></span>            | <span data-ttu-id="d0a00-136">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-136">False</span></span>                                                     |
| <span data-ttu-id="d0a00-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0a00-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d0a00-138">True</span><span class="sxs-lookup"><span data-stu-id="d0a00-138">True</span></span>                                                      |
| <span data-ttu-id="d0a00-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0a00-139">Is Indexed</span></span>             | <span data-ttu-id="d0a00-140">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-140">False</span></span>                                                     |
| <span data-ttu-id="d0a00-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0a00-141">In Global Catalog</span></span>      | <span data-ttu-id="d0a00-142">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-142">False</span></span>                                                     |
| <span data-ttu-id="d0a00-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0a00-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0a00-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0a00-144">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0a00-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0a00-145">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0a00-146">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-147">Search-Flags</span></span>           | <span data-ttu-id="d0a00-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0a00-148">0x00000000</span></span>                                                |
| <span data-ttu-id="d0a00-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-149">System-Flags</span></span>           | <span data-ttu-id="d0a00-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0a00-150">0x00000010</span></span>                                                |
| <span data-ttu-id="d0a00-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0a00-151">Classes used in</span></span>        | [<span data-ttu-id="d0a00-152">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0a00-152">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d0a00-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0a00-153">Windows Server 2003</span></span>



| <span data-ttu-id="d0a00-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0a00-154">Entry</span></span> | <span data-ttu-id="d0a00-155">Value</span><span class="sxs-lookup"><span data-stu-id="d0a00-155">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0a00-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0a00-156">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0a00-157">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0a00-158">System-Only</span></span>            | <span data-ttu-id="d0a00-159">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-159">False</span></span>                                                     |
| <span data-ttu-id="d0a00-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0a00-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d0a00-161">True</span><span class="sxs-lookup"><span data-stu-id="d0a00-161">True</span></span>                                                      |
| <span data-ttu-id="d0a00-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0a00-162">Is Indexed</span></span>             | <span data-ttu-id="d0a00-163">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-163">False</span></span>                                                     |
| <span data-ttu-id="d0a00-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0a00-164">In Global Catalog</span></span>      | <span data-ttu-id="d0a00-165">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-165">False</span></span>                                                     |
| <span data-ttu-id="d0a00-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0a00-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0a00-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0a00-167">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0a00-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0a00-168">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0a00-169">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-170">Search-Flags</span></span>           | <span data-ttu-id="d0a00-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0a00-171">0x00000000</span></span>                                                |
| <span data-ttu-id="d0a00-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-172">System-Flags</span></span>           | <span data-ttu-id="d0a00-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0a00-173">0x00000010</span></span>                                                |
| <span data-ttu-id="d0a00-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0a00-174">Classes used in</span></span>        | [<span data-ttu-id="d0a00-175">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0a00-175">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d0a00-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d0a00-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d0a00-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0a00-177">Entry</span></span> | <span data-ttu-id="d0a00-178">Value</span><span class="sxs-lookup"><span data-stu-id="d0a00-178">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0a00-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0a00-179">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0a00-180">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0a00-181">System-Only</span></span>            | <span data-ttu-id="d0a00-182">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-182">False</span></span>                                                     |
| <span data-ttu-id="d0a00-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0a00-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d0a00-184">True</span><span class="sxs-lookup"><span data-stu-id="d0a00-184">True</span></span>                                                      |
| <span data-ttu-id="d0a00-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0a00-185">Is Indexed</span></span>             | <span data-ttu-id="d0a00-186">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-186">False</span></span>                                                     |
| <span data-ttu-id="d0a00-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0a00-187">In Global Catalog</span></span>      | <span data-ttu-id="d0a00-188">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-188">False</span></span>                                                     |
| <span data-ttu-id="d0a00-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0a00-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0a00-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0a00-190">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0a00-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0a00-191">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0a00-192">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-193">Search-Flags</span></span>           | <span data-ttu-id="d0a00-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0a00-194">0x00000000</span></span>                                                |
| <span data-ttu-id="d0a00-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-195">System-Flags</span></span>           | <span data-ttu-id="d0a00-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0a00-196">0x00000010</span></span>                                                |
| <span data-ttu-id="d0a00-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0a00-197">Classes used in</span></span>        | [<span data-ttu-id="d0a00-198">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0a00-198">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d0a00-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0a00-199">Windows Server 2008</span></span>



| <span data-ttu-id="d0a00-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0a00-200">Entry</span></span> | <span data-ttu-id="d0a00-201">Value</span><span class="sxs-lookup"><span data-stu-id="d0a00-201">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0a00-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0a00-202">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0a00-203">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0a00-204">System-Only</span></span>            | <span data-ttu-id="d0a00-205">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-205">False</span></span>                                                     |
| <span data-ttu-id="d0a00-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0a00-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d0a00-207">True</span><span class="sxs-lookup"><span data-stu-id="d0a00-207">True</span></span>                                                      |
| <span data-ttu-id="d0a00-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0a00-208">Is Indexed</span></span>             | <span data-ttu-id="d0a00-209">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-209">False</span></span>                                                     |
| <span data-ttu-id="d0a00-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0a00-210">In Global Catalog</span></span>      | <span data-ttu-id="d0a00-211">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-211">False</span></span>                                                     |
| <span data-ttu-id="d0a00-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0a00-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0a00-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0a00-213">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0a00-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0a00-214">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0a00-215">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-216">Search-Flags</span></span>           | <span data-ttu-id="d0a00-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0a00-217">0x00000000</span></span>                                                |
| <span data-ttu-id="d0a00-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-218">System-Flags</span></span>           | <span data-ttu-id="d0a00-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0a00-219">0x00000010</span></span>                                                |
| <span data-ttu-id="d0a00-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0a00-220">Classes used in</span></span>        | [<span data-ttu-id="d0a00-221">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0a00-221">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d0a00-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d0a00-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d0a00-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0a00-223">Entry</span></span> | <span data-ttu-id="d0a00-224">Value</span><span class="sxs-lookup"><span data-stu-id="d0a00-224">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0a00-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0a00-225">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0a00-226">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0a00-227">System-Only</span></span>            | <span data-ttu-id="d0a00-228">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-228">False</span></span>                                                     |
| <span data-ttu-id="d0a00-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0a00-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d0a00-230">True</span><span class="sxs-lookup"><span data-stu-id="d0a00-230">True</span></span>                                                      |
| <span data-ttu-id="d0a00-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0a00-231">Is Indexed</span></span>             | <span data-ttu-id="d0a00-232">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-232">False</span></span>                                                     |
| <span data-ttu-id="d0a00-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0a00-233">In Global Catalog</span></span>      | <span data-ttu-id="d0a00-234">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-234">False</span></span>                                                     |
| <span data-ttu-id="d0a00-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0a00-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0a00-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0a00-236">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0a00-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0a00-237">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0a00-238">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-239">Search-Flags</span></span>           | <span data-ttu-id="d0a00-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0a00-240">0x00000000</span></span>                                                |
| <span data-ttu-id="d0a00-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-241">System-Flags</span></span>           | <span data-ttu-id="d0a00-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0a00-242">0x00000010</span></span>                                                |
| <span data-ttu-id="d0a00-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0a00-243">Classes used in</span></span>        | [<span data-ttu-id="d0a00-244">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0a00-244">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d0a00-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0a00-245">Windows Server 2012</span></span>



| <span data-ttu-id="d0a00-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="d0a00-246">Entry</span></span> | <span data-ttu-id="d0a00-247">Value</span><span class="sxs-lookup"><span data-stu-id="d0a00-247">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d0a00-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d0a00-248">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0a00-249">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="d0a00-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0a00-250">System-Only</span></span>            | <span data-ttu-id="d0a00-251">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-251">False</span></span>                                                     |
| <span data-ttu-id="d0a00-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d0a00-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d0a00-253">True</span><span class="sxs-lookup"><span data-stu-id="d0a00-253">True</span></span>                                                      |
| <span data-ttu-id="d0a00-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d0a00-254">Is Indexed</span></span>             | <span data-ttu-id="d0a00-255">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-255">False</span></span>                                                     |
| <span data-ttu-id="d0a00-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d0a00-256">In Global Catalog</span></span>      | <span data-ttu-id="d0a00-257">False</span><span class="sxs-lookup"><span data-stu-id="d0a00-257">False</span></span>                                                     |
| <span data-ttu-id="d0a00-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d0a00-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0a00-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0a00-259">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="d0a00-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0a00-260">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0a00-261">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="d0a00-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-262">Search-Flags</span></span>           | <span data-ttu-id="d0a00-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0a00-263">0x00000000</span></span>                                                |
| <span data-ttu-id="d0a00-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0a00-264">System-Flags</span></span>           | <span data-ttu-id="d0a00-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0a00-265">0x00000010</span></span>                                                |
| <span data-ttu-id="d0a00-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d0a00-266">Classes used in</span></span>        | [<span data-ttu-id="d0a00-267">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="d0a00-267">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 






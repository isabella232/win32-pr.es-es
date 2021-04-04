---
title: atributo MS-DS-NC-REPL-Outbound-Neighbors
description: Asociados de replicación para esta partición. Este servidor envía datos de replicación a estos otros servidores, que actúan como destinos. Este servidor notificará a estos otros servidores cuando haya nuevos datos disponibles.
ms.assetid: 9dcc7485-1999-47ff-bb57-8193768a15a9
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-NC-REPL-Outbound-Neighbors
- Esquema de AD de atributo msDS-NCReplOutboundNeighbors
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Outbound-Neighbors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fd37ccab1b3faef6ca2c84a52c05249a52ff38a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906035"
---
# <a name="ms-ds-nc-repl-outbound-neighbors-attribute"></a><span data-ttu-id="152a7-107">atributo MS-DS-NC-REPL-Outbound-Neighbors</span><span class="sxs-lookup"><span data-stu-id="152a7-107">ms-DS-NC-Repl-Outbound-Neighbors attribute</span></span>

<span data-ttu-id="152a7-108">Asociados de replicación para esta partición.</span><span class="sxs-lookup"><span data-stu-id="152a7-108">Replication partners for this partition.</span></span> <span data-ttu-id="152a7-109">Este servidor envía datos de replicación a estos otros servidores, que actúan como destinos.</span><span class="sxs-lookup"><span data-stu-id="152a7-109">This server sends replication data to these other servers, which act as destinations.</span></span> <span data-ttu-id="152a7-110">Este servidor notificará a estos otros servidores cuando haya nuevos datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="152a7-110">This server will notify these other servers when new data is available.</span></span>



| <span data-ttu-id="152a7-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="152a7-111">Entry</span></span> | <span data-ttu-id="152a7-112">Value</span><span class="sxs-lookup"><span data-stu-id="152a7-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="152a7-113">CN</span><span class="sxs-lookup"><span data-stu-id="152a7-113">CN</span></span>                | <span data-ttu-id="152a7-114">MS-DS-NC-REPL-Outbound-Neighbors</span><span class="sxs-lookup"><span data-stu-id="152a7-114">ms-DS-NC-Repl-Outbound-Neighbors</span></span>            |
| <span data-ttu-id="152a7-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="152a7-115">Ldap-Display-Name</span></span> | <span data-ttu-id="152a7-116">msDS-NCReplOutboundNeighbors</span><span class="sxs-lookup"><span data-stu-id="152a7-116">msDS-NCReplOutboundNeighbors</span></span>                |
| <span data-ttu-id="152a7-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="152a7-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="152a7-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="152a7-118">Update Privilege</span></span>  | <span data-ttu-id="152a7-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="152a7-119">This value is set by the system.</span></span>            |
| <span data-ttu-id="152a7-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="152a7-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="152a7-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="152a7-121">Attribute-Id</span></span>      | <span data-ttu-id="152a7-122">1.2.840.113556.1.4.1706</span><span class="sxs-lookup"><span data-stu-id="152a7-122">1.2.840.113556.1.4.1706</span></span>                     |
| <span data-ttu-id="152a7-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="152a7-123">System-Id-Guid</span></span>    | <span data-ttu-id="152a7-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span><span class="sxs-lookup"><span data-stu-id="152a7-124">855f2ef5-a1c5-4cc4-ba6d-32522848b61f</span></span>        |
| <span data-ttu-id="152a7-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="152a7-125">Syntax</span></span>            | [<span data-ttu-id="152a7-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="152a7-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="152a7-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="152a7-127">Implementations</span></span>

-   [<span data-ttu-id="152a7-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="152a7-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="152a7-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="152a7-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="152a7-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="152a7-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="152a7-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="152a7-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="152a7-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="152a7-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="152a7-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="152a7-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="152a7-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="152a7-134">Windows Server 2003</span></span>



| <span data-ttu-id="152a7-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="152a7-135">Entry</span></span> | <span data-ttu-id="152a7-136">Value</span><span class="sxs-lookup"><span data-stu-id="152a7-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="152a7-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="152a7-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152a7-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="152a7-139">System-Only</span></span>            | <span data-ttu-id="152a7-140">False</span><span class="sxs-lookup"><span data-stu-id="152a7-140">False</span></span>                           |
| <span data-ttu-id="152a7-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="152a7-141">Is-Single-Valued</span></span>       | <span data-ttu-id="152a7-142">False</span><span class="sxs-lookup"><span data-stu-id="152a7-142">False</span></span>                           |
| <span data-ttu-id="152a7-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="152a7-143">Is Indexed</span></span>             | <span data-ttu-id="152a7-144">False</span><span class="sxs-lookup"><span data-stu-id="152a7-144">False</span></span>                           |
| <span data-ttu-id="152a7-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="152a7-145">In Global Catalog</span></span>      | <span data-ttu-id="152a7-146">False</span><span class="sxs-lookup"><span data-stu-id="152a7-146">False</span></span>                           |
| <span data-ttu-id="152a7-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="152a7-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="152a7-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="152a7-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="152a7-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152a7-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="152a7-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152a7-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="152a7-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-151">Search-Flags</span></span>           | <span data-ttu-id="152a7-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152a7-152">0x00000000</span></span>                      |
| <span data-ttu-id="152a7-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-153">System-Flags</span></span>           | <span data-ttu-id="152a7-154">0x00000014</span><span class="sxs-lookup"><span data-stu-id="152a7-154">0x00000014</span></span>                      |
| <span data-ttu-id="152a7-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="152a7-155">Classes used in</span></span>        | [<span data-ttu-id="152a7-156">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="152a7-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="152a7-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="152a7-157">ADAM</span></span>



| <span data-ttu-id="152a7-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="152a7-158">Entry</span></span> | <span data-ttu-id="152a7-159">Value</span><span class="sxs-lookup"><span data-stu-id="152a7-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="152a7-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="152a7-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152a7-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="152a7-162">System-Only</span></span>            | <span data-ttu-id="152a7-163">False</span><span class="sxs-lookup"><span data-stu-id="152a7-163">False</span></span>                           |
| <span data-ttu-id="152a7-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="152a7-164">Is-Single-Valued</span></span>       | <span data-ttu-id="152a7-165">False</span><span class="sxs-lookup"><span data-stu-id="152a7-165">False</span></span>                           |
| <span data-ttu-id="152a7-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="152a7-166">Is Indexed</span></span>             | <span data-ttu-id="152a7-167">False</span><span class="sxs-lookup"><span data-stu-id="152a7-167">False</span></span>                           |
| <span data-ttu-id="152a7-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="152a7-168">In Global Catalog</span></span>      | <span data-ttu-id="152a7-169">False</span><span class="sxs-lookup"><span data-stu-id="152a7-169">False</span></span>                           |
| <span data-ttu-id="152a7-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="152a7-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="152a7-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="152a7-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="152a7-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152a7-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="152a7-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152a7-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="152a7-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-174">Search-Flags</span></span>           | <span data-ttu-id="152a7-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152a7-175">0x00000000</span></span>                      |
| <span data-ttu-id="152a7-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-176">System-Flags</span></span>           | <span data-ttu-id="152a7-177">0x00000014</span><span class="sxs-lookup"><span data-stu-id="152a7-177">0x00000014</span></span>                      |
| <span data-ttu-id="152a7-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="152a7-178">Classes used in</span></span>        | [<span data-ttu-id="152a7-179">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="152a7-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="152a7-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="152a7-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="152a7-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="152a7-181">Entry</span></span> | <span data-ttu-id="152a7-182">Value</span><span class="sxs-lookup"><span data-stu-id="152a7-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="152a7-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="152a7-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152a7-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="152a7-185">System-Only</span></span>            | <span data-ttu-id="152a7-186">False</span><span class="sxs-lookup"><span data-stu-id="152a7-186">False</span></span>                           |
| <span data-ttu-id="152a7-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="152a7-187">Is-Single-Valued</span></span>       | <span data-ttu-id="152a7-188">False</span><span class="sxs-lookup"><span data-stu-id="152a7-188">False</span></span>                           |
| <span data-ttu-id="152a7-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="152a7-189">Is Indexed</span></span>             | <span data-ttu-id="152a7-190">False</span><span class="sxs-lookup"><span data-stu-id="152a7-190">False</span></span>                           |
| <span data-ttu-id="152a7-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="152a7-191">In Global Catalog</span></span>      | <span data-ttu-id="152a7-192">False</span><span class="sxs-lookup"><span data-stu-id="152a7-192">False</span></span>                           |
| <span data-ttu-id="152a7-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="152a7-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="152a7-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="152a7-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="152a7-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152a7-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="152a7-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152a7-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="152a7-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-197">Search-Flags</span></span>           | <span data-ttu-id="152a7-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152a7-198">0x00000000</span></span>                      |
| <span data-ttu-id="152a7-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-199">System-Flags</span></span>           | <span data-ttu-id="152a7-200">0x00000014</span><span class="sxs-lookup"><span data-stu-id="152a7-200">0x00000014</span></span>                      |
| <span data-ttu-id="152a7-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="152a7-201">Classes used in</span></span>        | [<span data-ttu-id="152a7-202">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="152a7-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="152a7-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="152a7-203">Windows Server 2008</span></span>



| <span data-ttu-id="152a7-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="152a7-204">Entry</span></span> | <span data-ttu-id="152a7-205">Value</span><span class="sxs-lookup"><span data-stu-id="152a7-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="152a7-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="152a7-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152a7-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="152a7-208">System-Only</span></span>            | <span data-ttu-id="152a7-209">False</span><span class="sxs-lookup"><span data-stu-id="152a7-209">False</span></span>                           |
| <span data-ttu-id="152a7-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="152a7-210">Is-Single-Valued</span></span>       | <span data-ttu-id="152a7-211">False</span><span class="sxs-lookup"><span data-stu-id="152a7-211">False</span></span>                           |
| <span data-ttu-id="152a7-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="152a7-212">Is Indexed</span></span>             | <span data-ttu-id="152a7-213">False</span><span class="sxs-lookup"><span data-stu-id="152a7-213">False</span></span>                           |
| <span data-ttu-id="152a7-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="152a7-214">In Global Catalog</span></span>      | <span data-ttu-id="152a7-215">False</span><span class="sxs-lookup"><span data-stu-id="152a7-215">False</span></span>                           |
| <span data-ttu-id="152a7-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="152a7-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="152a7-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="152a7-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="152a7-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152a7-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="152a7-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152a7-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="152a7-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-220">Search-Flags</span></span>           | <span data-ttu-id="152a7-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152a7-221">0x00000000</span></span>                      |
| <span data-ttu-id="152a7-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-222">System-Flags</span></span>           | <span data-ttu-id="152a7-223">0x00000014</span><span class="sxs-lookup"><span data-stu-id="152a7-223">0x00000014</span></span>                      |
| <span data-ttu-id="152a7-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="152a7-224">Classes used in</span></span>        | [<span data-ttu-id="152a7-225">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="152a7-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="152a7-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="152a7-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="152a7-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="152a7-227">Entry</span></span> | <span data-ttu-id="152a7-228">Value</span><span class="sxs-lookup"><span data-stu-id="152a7-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="152a7-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="152a7-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152a7-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="152a7-231">System-Only</span></span>            | <span data-ttu-id="152a7-232">False</span><span class="sxs-lookup"><span data-stu-id="152a7-232">False</span></span>                           |
| <span data-ttu-id="152a7-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="152a7-233">Is-Single-Valued</span></span>       | <span data-ttu-id="152a7-234">False</span><span class="sxs-lookup"><span data-stu-id="152a7-234">False</span></span>                           |
| <span data-ttu-id="152a7-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="152a7-235">Is Indexed</span></span>             | <span data-ttu-id="152a7-236">False</span><span class="sxs-lookup"><span data-stu-id="152a7-236">False</span></span>                           |
| <span data-ttu-id="152a7-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="152a7-237">In Global Catalog</span></span>      | <span data-ttu-id="152a7-238">False</span><span class="sxs-lookup"><span data-stu-id="152a7-238">False</span></span>                           |
| <span data-ttu-id="152a7-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="152a7-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="152a7-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="152a7-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="152a7-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152a7-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="152a7-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152a7-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="152a7-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-243">Search-Flags</span></span>           | <span data-ttu-id="152a7-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152a7-244">0x00000000</span></span>                      |
| <span data-ttu-id="152a7-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-245">System-Flags</span></span>           | <span data-ttu-id="152a7-246">0x00000014</span><span class="sxs-lookup"><span data-stu-id="152a7-246">0x00000014</span></span>                      |
| <span data-ttu-id="152a7-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="152a7-247">Classes used in</span></span>        | [<span data-ttu-id="152a7-248">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="152a7-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="152a7-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="152a7-249">Windows Server 2012</span></span>



| <span data-ttu-id="152a7-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="152a7-250">Entry</span></span> | <span data-ttu-id="152a7-251">Value</span><span class="sxs-lookup"><span data-stu-id="152a7-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="152a7-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="152a7-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="152a7-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="152a7-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="152a7-254">System-Only</span></span>            | <span data-ttu-id="152a7-255">False</span><span class="sxs-lookup"><span data-stu-id="152a7-255">False</span></span>                           |
| <span data-ttu-id="152a7-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="152a7-256">Is-Single-Valued</span></span>       | <span data-ttu-id="152a7-257">False</span><span class="sxs-lookup"><span data-stu-id="152a7-257">False</span></span>                           |
| <span data-ttu-id="152a7-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="152a7-258">Is Indexed</span></span>             | <span data-ttu-id="152a7-259">False</span><span class="sxs-lookup"><span data-stu-id="152a7-259">False</span></span>                           |
| <span data-ttu-id="152a7-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="152a7-260">In Global Catalog</span></span>      | <span data-ttu-id="152a7-261">False</span><span class="sxs-lookup"><span data-stu-id="152a7-261">False</span></span>                           |
| <span data-ttu-id="152a7-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="152a7-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="152a7-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="152a7-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="152a7-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="152a7-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="152a7-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="152a7-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="152a7-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-266">Search-Flags</span></span>           | <span data-ttu-id="152a7-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="152a7-267">0x00000000</span></span>                      |
| <span data-ttu-id="152a7-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="152a7-268">System-Flags</span></span>           | <span data-ttu-id="152a7-269">0x00000014</span><span class="sxs-lookup"><span data-stu-id="152a7-269">0x00000014</span></span>                      |
| <span data-ttu-id="152a7-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="152a7-270">Classes used in</span></span>        | [<span data-ttu-id="152a7-271">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="152a7-271">**Top**</span></span>](c-top.md)<br/> |



 

 






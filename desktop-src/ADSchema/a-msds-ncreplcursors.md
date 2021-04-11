---
title: atributo MS-DS-NC-REPL-cursor
description: Una lista de asociados de replicación pasados y presentes, y cómo se encuentran los actuales con cada uno de ellos.
ms.assetid: febe8614-b68a-4001-b6ae-dae3fe6eb25f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de MS-DS-NC-REPL-cursor
- Esquema de AD de atributo msDS-NCReplCursors
topic_type:
- apiref
api_name:
- ms-DS-NC-Repl-Cursors
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555a09520079df624fffb2cb3cb3aa34b81502c2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151659"
---
# <a name="ms-ds-nc-repl-cursors-attribute"></a><span data-ttu-id="a3714-105">atributo MS-DS-NC-REPL-cursor</span><span class="sxs-lookup"><span data-stu-id="a3714-105">ms-DS-NC-Repl-Cursors attribute</span></span>

<span data-ttu-id="a3714-106">Una lista de asociados de replicación pasados y presentes, y cómo se encuentran los actuales con cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="a3714-106">A list of past and present replication partners, and how current we are with each of them.</span></span>



| <span data-ttu-id="a3714-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3714-107">Entry</span></span> | <span data-ttu-id="a3714-108">Value</span><span class="sxs-lookup"><span data-stu-id="a3714-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a3714-109">CN</span><span class="sxs-lookup"><span data-stu-id="a3714-109">CN</span></span>                | <span data-ttu-id="a3714-110">MS-DS-NC-REPL-cursores</span><span class="sxs-lookup"><span data-stu-id="a3714-110">ms-DS-NC-Repl-Cursors</span></span>                       |
| <span data-ttu-id="a3714-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a3714-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a3714-112">msDS-NCReplCursors</span><span class="sxs-lookup"><span data-stu-id="a3714-112">msDS-NCReplCursors</span></span>                          |
| <span data-ttu-id="a3714-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a3714-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a3714-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a3714-114">Update Privilege</span></span>  | <span data-ttu-id="a3714-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a3714-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="a3714-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a3714-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a3714-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a3714-117">Attribute-Id</span></span>      | <span data-ttu-id="a3714-118">1.2.840.113556.1.4.1704</span><span class="sxs-lookup"><span data-stu-id="a3714-118">1.2.840.113556.1.4.1704</span></span>                     |
| <span data-ttu-id="a3714-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a3714-119">System-Id-Guid</span></span>    | <span data-ttu-id="a3714-120">8a167ce4-f9e8-47eb-8d78-f7fe80abb2cc</span><span class="sxs-lookup"><span data-stu-id="a3714-120">8a167ce4-f9e8-47eb-8d78-f7fe80abb2cc</span></span>        |
| <span data-ttu-id="a3714-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3714-121">Syntax</span></span>            | [<span data-ttu-id="a3714-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a3714-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a3714-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a3714-123">Implementations</span></span>

-   [<span data-ttu-id="a3714-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a3714-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a3714-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a3714-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a3714-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a3714-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a3714-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a3714-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a3714-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a3714-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a3714-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3714-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a3714-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3714-130">Windows Server 2003</span></span>



| <span data-ttu-id="a3714-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3714-131">Entry</span></span> | <span data-ttu-id="a3714-132">Value</span><span class="sxs-lookup"><span data-stu-id="a3714-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3714-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3714-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3714-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3714-135">System-Only</span></span>            | <span data-ttu-id="a3714-136">False</span><span class="sxs-lookup"><span data-stu-id="a3714-136">False</span></span>                           |
| <span data-ttu-id="a3714-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3714-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a3714-138">False</span><span class="sxs-lookup"><span data-stu-id="a3714-138">False</span></span>                           |
| <span data-ttu-id="a3714-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3714-139">Is Indexed</span></span>             | <span data-ttu-id="a3714-140">False</span><span class="sxs-lookup"><span data-stu-id="a3714-140">False</span></span>                           |
| <span data-ttu-id="a3714-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3714-141">In Global Catalog</span></span>      | <span data-ttu-id="a3714-142">False</span><span class="sxs-lookup"><span data-stu-id="a3714-142">False</span></span>                           |
| <span data-ttu-id="a3714-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3714-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3714-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3714-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3714-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3714-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3714-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3714-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3714-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-147">Search-Flags</span></span>           | <span data-ttu-id="a3714-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3714-148">0x00000000</span></span>                      |
| <span data-ttu-id="a3714-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-149">System-Flags</span></span>           | <span data-ttu-id="a3714-150">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a3714-150">0x00000014</span></span>                      |
| <span data-ttu-id="a3714-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3714-151">Classes used in</span></span>        | [<span data-ttu-id="a3714-152">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a3714-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a3714-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="a3714-153">ADAM</span></span>



| <span data-ttu-id="a3714-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3714-154">Entry</span></span> | <span data-ttu-id="a3714-155">Value</span><span class="sxs-lookup"><span data-stu-id="a3714-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3714-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3714-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3714-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3714-158">System-Only</span></span>            | <span data-ttu-id="a3714-159">False</span><span class="sxs-lookup"><span data-stu-id="a3714-159">False</span></span>                           |
| <span data-ttu-id="a3714-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3714-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a3714-161">False</span><span class="sxs-lookup"><span data-stu-id="a3714-161">False</span></span>                           |
| <span data-ttu-id="a3714-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3714-162">Is Indexed</span></span>             | <span data-ttu-id="a3714-163">False</span><span class="sxs-lookup"><span data-stu-id="a3714-163">False</span></span>                           |
| <span data-ttu-id="a3714-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3714-164">In Global Catalog</span></span>      | <span data-ttu-id="a3714-165">False</span><span class="sxs-lookup"><span data-stu-id="a3714-165">False</span></span>                           |
| <span data-ttu-id="a3714-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3714-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3714-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3714-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3714-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3714-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3714-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3714-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3714-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-170">Search-Flags</span></span>           | <span data-ttu-id="a3714-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3714-171">0x00000000</span></span>                      |
| <span data-ttu-id="a3714-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-172">System-Flags</span></span>           | <span data-ttu-id="a3714-173">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a3714-173">0x00000014</span></span>                      |
| <span data-ttu-id="a3714-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3714-174">Classes used in</span></span>        | [<span data-ttu-id="a3714-175">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a3714-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a3714-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a3714-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a3714-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3714-177">Entry</span></span> | <span data-ttu-id="a3714-178">Value</span><span class="sxs-lookup"><span data-stu-id="a3714-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3714-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3714-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3714-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3714-181">System-Only</span></span>            | <span data-ttu-id="a3714-182">False</span><span class="sxs-lookup"><span data-stu-id="a3714-182">False</span></span>                           |
| <span data-ttu-id="a3714-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3714-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a3714-184">False</span><span class="sxs-lookup"><span data-stu-id="a3714-184">False</span></span>                           |
| <span data-ttu-id="a3714-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3714-185">Is Indexed</span></span>             | <span data-ttu-id="a3714-186">False</span><span class="sxs-lookup"><span data-stu-id="a3714-186">False</span></span>                           |
| <span data-ttu-id="a3714-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3714-187">In Global Catalog</span></span>      | <span data-ttu-id="a3714-188">False</span><span class="sxs-lookup"><span data-stu-id="a3714-188">False</span></span>                           |
| <span data-ttu-id="a3714-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3714-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3714-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3714-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3714-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3714-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3714-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3714-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3714-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-193">Search-Flags</span></span>           | <span data-ttu-id="a3714-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3714-194">0x00000000</span></span>                      |
| <span data-ttu-id="a3714-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-195">System-Flags</span></span>           | <span data-ttu-id="a3714-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a3714-196">0x00000014</span></span>                      |
| <span data-ttu-id="a3714-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3714-197">Classes used in</span></span>        | [<span data-ttu-id="a3714-198">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a3714-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a3714-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3714-199">Windows Server 2008</span></span>



| <span data-ttu-id="a3714-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3714-200">Entry</span></span> | <span data-ttu-id="a3714-201">Value</span><span class="sxs-lookup"><span data-stu-id="a3714-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3714-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3714-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3714-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3714-204">System-Only</span></span>            | <span data-ttu-id="a3714-205">False</span><span class="sxs-lookup"><span data-stu-id="a3714-205">False</span></span>                           |
| <span data-ttu-id="a3714-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3714-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a3714-207">False</span><span class="sxs-lookup"><span data-stu-id="a3714-207">False</span></span>                           |
| <span data-ttu-id="a3714-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3714-208">Is Indexed</span></span>             | <span data-ttu-id="a3714-209">False</span><span class="sxs-lookup"><span data-stu-id="a3714-209">False</span></span>                           |
| <span data-ttu-id="a3714-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3714-210">In Global Catalog</span></span>      | <span data-ttu-id="a3714-211">False</span><span class="sxs-lookup"><span data-stu-id="a3714-211">False</span></span>                           |
| <span data-ttu-id="a3714-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3714-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3714-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3714-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3714-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3714-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3714-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3714-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3714-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-216">Search-Flags</span></span>           | <span data-ttu-id="a3714-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3714-217">0x00000000</span></span>                      |
| <span data-ttu-id="a3714-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-218">System-Flags</span></span>           | <span data-ttu-id="a3714-219">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a3714-219">0x00000014</span></span>                      |
| <span data-ttu-id="a3714-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3714-220">Classes used in</span></span>        | [<span data-ttu-id="a3714-221">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a3714-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a3714-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3714-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a3714-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3714-223">Entry</span></span> | <span data-ttu-id="a3714-224">Value</span><span class="sxs-lookup"><span data-stu-id="a3714-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3714-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3714-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3714-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3714-227">System-Only</span></span>            | <span data-ttu-id="a3714-228">False</span><span class="sxs-lookup"><span data-stu-id="a3714-228">False</span></span>                           |
| <span data-ttu-id="a3714-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3714-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a3714-230">False</span><span class="sxs-lookup"><span data-stu-id="a3714-230">False</span></span>                           |
| <span data-ttu-id="a3714-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3714-231">Is Indexed</span></span>             | <span data-ttu-id="a3714-232">False</span><span class="sxs-lookup"><span data-stu-id="a3714-232">False</span></span>                           |
| <span data-ttu-id="a3714-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3714-233">In Global Catalog</span></span>      | <span data-ttu-id="a3714-234">False</span><span class="sxs-lookup"><span data-stu-id="a3714-234">False</span></span>                           |
| <span data-ttu-id="a3714-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3714-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3714-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3714-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3714-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3714-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3714-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3714-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3714-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-239">Search-Flags</span></span>           | <span data-ttu-id="a3714-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3714-240">0x00000000</span></span>                      |
| <span data-ttu-id="a3714-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-241">System-Flags</span></span>           | <span data-ttu-id="a3714-242">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a3714-242">0x00000014</span></span>                      |
| <span data-ttu-id="a3714-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3714-243">Classes used in</span></span>        | [<span data-ttu-id="a3714-244">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a3714-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a3714-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3714-245">Windows Server 2012</span></span>



| <span data-ttu-id="a3714-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3714-246">Entry</span></span> | <span data-ttu-id="a3714-247">Value</span><span class="sxs-lookup"><span data-stu-id="a3714-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a3714-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a3714-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a3714-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="a3714-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a3714-250">System-Only</span></span>            | <span data-ttu-id="a3714-251">False</span><span class="sxs-lookup"><span data-stu-id="a3714-251">False</span></span>                           |
| <span data-ttu-id="a3714-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a3714-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a3714-253">False</span><span class="sxs-lookup"><span data-stu-id="a3714-253">False</span></span>                           |
| <span data-ttu-id="a3714-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a3714-254">Is Indexed</span></span>             | <span data-ttu-id="a3714-255">False</span><span class="sxs-lookup"><span data-stu-id="a3714-255">False</span></span>                           |
| <span data-ttu-id="a3714-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a3714-256">In Global Catalog</span></span>      | <span data-ttu-id="a3714-257">False</span><span class="sxs-lookup"><span data-stu-id="a3714-257">False</span></span>                           |
| <span data-ttu-id="a3714-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a3714-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a3714-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a3714-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a3714-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a3714-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a3714-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a3714-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a3714-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-262">Search-Flags</span></span>           | <span data-ttu-id="a3714-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a3714-263">0x00000000</span></span>                      |
| <span data-ttu-id="a3714-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a3714-264">System-Flags</span></span>           | <span data-ttu-id="a3714-265">0x00000014</span><span class="sxs-lookup"><span data-stu-id="a3714-265">0x00000014</span></span>                      |
| <span data-ttu-id="a3714-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a3714-266">Classes used in</span></span>        | [<span data-ttu-id="a3714-267">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a3714-267">**Top**</span></span>](c-top.md)<br/> |



 

 






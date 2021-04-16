---
title: atributo MS-DS-REPL-Attribute-meta-data
description: Una lista de metadatos para cada atributo replicado. Los metadatos indican quién cambió el atributo en último lugar.
ms.assetid: 07cfd323-eb90-4715-9307-583cf7e9f63e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-REPL-Attribute-meta-data
- Esquema de AD de atributo msDS-ReplAttributeMetaData
topic_type:
- apiref
api_name:
- ms-DS-Repl-Attribute-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edc991ead7104d8b9b4c023882d39adf1d53446
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658857"
---
# <a name="ms-ds-repl-attribute-meta-data-attribute"></a><span data-ttu-id="ad001-106">atributo MS-DS-REPL-Attribute-meta-data</span><span class="sxs-lookup"><span data-stu-id="ad001-106">ms-DS-Repl-Attribute-Meta-Data attribute</span></span>

<span data-ttu-id="ad001-107">Una lista de metadatos para cada atributo replicado.</span><span class="sxs-lookup"><span data-stu-id="ad001-107">A list of metadata for each replicated attribute.</span></span> <span data-ttu-id="ad001-108">Los metadatos indican quién cambió el atributo en último lugar.</span><span class="sxs-lookup"><span data-stu-id="ad001-108">The metadata indicates who changed the attribute last.</span></span>



| <span data-ttu-id="ad001-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad001-109">Entry</span></span> | <span data-ttu-id="ad001-110">Value</span><span class="sxs-lookup"><span data-stu-id="ad001-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ad001-111">CN</span><span class="sxs-lookup"><span data-stu-id="ad001-111">CN</span></span>                | <span data-ttu-id="ad001-112">MS-DS-REPL-Attribute-meta-data</span><span class="sxs-lookup"><span data-stu-id="ad001-112">ms-DS-Repl-Attribute-Meta-Data</span></span>              |
| <span data-ttu-id="ad001-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ad001-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ad001-114">msDS-ReplAttributeMetaData</span><span class="sxs-lookup"><span data-stu-id="ad001-114">msDS-ReplAttributeMetaData</span></span>                  |
| <span data-ttu-id="ad001-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ad001-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ad001-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ad001-116">Update Privilege</span></span>  | <span data-ttu-id="ad001-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="ad001-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="ad001-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ad001-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ad001-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad001-119">Attribute-Id</span></span>      | <span data-ttu-id="ad001-120">1.2.840.113556.1.4.1707</span><span class="sxs-lookup"><span data-stu-id="ad001-120">1.2.840.113556.1.4.1707</span></span>                     |
| <span data-ttu-id="ad001-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ad001-121">System-Id-Guid</span></span>    | <span data-ttu-id="ad001-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span><span class="sxs-lookup"><span data-stu-id="ad001-122">d7c53242-724e-4c39-9d4c-2df8c9d66c7a</span></span>        |
| <span data-ttu-id="ad001-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad001-123">Syntax</span></span>            | [<span data-ttu-id="ad001-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ad001-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ad001-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ad001-125">Implementations</span></span>

-   [<span data-ttu-id="ad001-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ad001-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ad001-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ad001-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ad001-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ad001-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ad001-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad001-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad001-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad001-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad001-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad001-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ad001-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad001-132">Windows Server 2003</span></span>



| <span data-ttu-id="ad001-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad001-133">Entry</span></span> | <span data-ttu-id="ad001-134">Value</span><span class="sxs-lookup"><span data-stu-id="ad001-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad001-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ad001-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad001-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad001-137">System-Only</span></span>            | <span data-ttu-id="ad001-138">False</span><span class="sxs-lookup"><span data-stu-id="ad001-138">False</span></span>                           |
| <span data-ttu-id="ad001-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ad001-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ad001-140">False</span><span class="sxs-lookup"><span data-stu-id="ad001-140">False</span></span>                           |
| <span data-ttu-id="ad001-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ad001-141">Is Indexed</span></span>             | <span data-ttu-id="ad001-142">False</span><span class="sxs-lookup"><span data-stu-id="ad001-142">False</span></span>                           |
| <span data-ttu-id="ad001-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad001-143">In Global Catalog</span></span>      | <span data-ttu-id="ad001-144">False</span><span class="sxs-lookup"><span data-stu-id="ad001-144">False</span></span>                           |
| <span data-ttu-id="ad001-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ad001-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad001-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad001-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad001-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad001-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad001-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad001-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad001-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-149">Search-Flags</span></span>           | <span data-ttu-id="ad001-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad001-150">0x00000000</span></span>                      |
| <span data-ttu-id="ad001-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-151">System-Flags</span></span>           | <span data-ttu-id="ad001-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ad001-152">0x00000014</span></span>                      |
| <span data-ttu-id="ad001-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ad001-153">Classes used in</span></span>        | [<span data-ttu-id="ad001-154">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="ad001-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ad001-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="ad001-155">ADAM</span></span>



| <span data-ttu-id="ad001-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad001-156">Entry</span></span> | <span data-ttu-id="ad001-157">Value</span><span class="sxs-lookup"><span data-stu-id="ad001-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad001-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ad001-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad001-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad001-160">System-Only</span></span>            | <span data-ttu-id="ad001-161">False</span><span class="sxs-lookup"><span data-stu-id="ad001-161">False</span></span>                           |
| <span data-ttu-id="ad001-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ad001-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ad001-163">False</span><span class="sxs-lookup"><span data-stu-id="ad001-163">False</span></span>                           |
| <span data-ttu-id="ad001-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ad001-164">Is Indexed</span></span>             | <span data-ttu-id="ad001-165">False</span><span class="sxs-lookup"><span data-stu-id="ad001-165">False</span></span>                           |
| <span data-ttu-id="ad001-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad001-166">In Global Catalog</span></span>      | <span data-ttu-id="ad001-167">False</span><span class="sxs-lookup"><span data-stu-id="ad001-167">False</span></span>                           |
| <span data-ttu-id="ad001-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ad001-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad001-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad001-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad001-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad001-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad001-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad001-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad001-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-172">Search-Flags</span></span>           | <span data-ttu-id="ad001-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad001-173">0x00000000</span></span>                      |
| <span data-ttu-id="ad001-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-174">System-Flags</span></span>           | <span data-ttu-id="ad001-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ad001-175">0x00000014</span></span>                      |
| <span data-ttu-id="ad001-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ad001-176">Classes used in</span></span>        | [<span data-ttu-id="ad001-177">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="ad001-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ad001-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ad001-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ad001-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad001-179">Entry</span></span> | <span data-ttu-id="ad001-180">Value</span><span class="sxs-lookup"><span data-stu-id="ad001-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad001-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ad001-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad001-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad001-183">System-Only</span></span>            | <span data-ttu-id="ad001-184">False</span><span class="sxs-lookup"><span data-stu-id="ad001-184">False</span></span>                           |
| <span data-ttu-id="ad001-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ad001-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ad001-186">False</span><span class="sxs-lookup"><span data-stu-id="ad001-186">False</span></span>                           |
| <span data-ttu-id="ad001-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ad001-187">Is Indexed</span></span>             | <span data-ttu-id="ad001-188">False</span><span class="sxs-lookup"><span data-stu-id="ad001-188">False</span></span>                           |
| <span data-ttu-id="ad001-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad001-189">In Global Catalog</span></span>      | <span data-ttu-id="ad001-190">False</span><span class="sxs-lookup"><span data-stu-id="ad001-190">False</span></span>                           |
| <span data-ttu-id="ad001-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ad001-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad001-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad001-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad001-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad001-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad001-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad001-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad001-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-195">Search-Flags</span></span>           | <span data-ttu-id="ad001-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad001-196">0x00000000</span></span>                      |
| <span data-ttu-id="ad001-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-197">System-Flags</span></span>           | <span data-ttu-id="ad001-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ad001-198">0x00000014</span></span>                      |
| <span data-ttu-id="ad001-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ad001-199">Classes used in</span></span>        | [<span data-ttu-id="ad001-200">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="ad001-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ad001-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad001-201">Windows Server 2008</span></span>



| <span data-ttu-id="ad001-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad001-202">Entry</span></span> | <span data-ttu-id="ad001-203">Value</span><span class="sxs-lookup"><span data-stu-id="ad001-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad001-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ad001-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad001-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad001-206">System-Only</span></span>            | <span data-ttu-id="ad001-207">False</span><span class="sxs-lookup"><span data-stu-id="ad001-207">False</span></span>                           |
| <span data-ttu-id="ad001-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ad001-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ad001-209">False</span><span class="sxs-lookup"><span data-stu-id="ad001-209">False</span></span>                           |
| <span data-ttu-id="ad001-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ad001-210">Is Indexed</span></span>             | <span data-ttu-id="ad001-211">False</span><span class="sxs-lookup"><span data-stu-id="ad001-211">False</span></span>                           |
| <span data-ttu-id="ad001-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad001-212">In Global Catalog</span></span>      | <span data-ttu-id="ad001-213">False</span><span class="sxs-lookup"><span data-stu-id="ad001-213">False</span></span>                           |
| <span data-ttu-id="ad001-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ad001-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad001-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad001-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad001-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad001-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad001-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad001-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad001-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-218">Search-Flags</span></span>           | <span data-ttu-id="ad001-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad001-219">0x00000000</span></span>                      |
| <span data-ttu-id="ad001-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-220">System-Flags</span></span>           | <span data-ttu-id="ad001-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ad001-221">0x00000014</span></span>                      |
| <span data-ttu-id="ad001-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ad001-222">Classes used in</span></span>        | [<span data-ttu-id="ad001-223">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="ad001-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad001-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad001-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad001-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad001-225">Entry</span></span> | <span data-ttu-id="ad001-226">Value</span><span class="sxs-lookup"><span data-stu-id="ad001-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad001-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ad001-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad001-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad001-229">System-Only</span></span>            | <span data-ttu-id="ad001-230">False</span><span class="sxs-lookup"><span data-stu-id="ad001-230">False</span></span>                           |
| <span data-ttu-id="ad001-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ad001-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ad001-232">False</span><span class="sxs-lookup"><span data-stu-id="ad001-232">False</span></span>                           |
| <span data-ttu-id="ad001-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ad001-233">Is Indexed</span></span>             | <span data-ttu-id="ad001-234">False</span><span class="sxs-lookup"><span data-stu-id="ad001-234">False</span></span>                           |
| <span data-ttu-id="ad001-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad001-235">In Global Catalog</span></span>      | <span data-ttu-id="ad001-236">False</span><span class="sxs-lookup"><span data-stu-id="ad001-236">False</span></span>                           |
| <span data-ttu-id="ad001-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ad001-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad001-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad001-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad001-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad001-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad001-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad001-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad001-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-241">Search-Flags</span></span>           | <span data-ttu-id="ad001-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad001-242">0x00000000</span></span>                      |
| <span data-ttu-id="ad001-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-243">System-Flags</span></span>           | <span data-ttu-id="ad001-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ad001-244">0x00000014</span></span>                      |
| <span data-ttu-id="ad001-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ad001-245">Classes used in</span></span>        | [<span data-ttu-id="ad001-246">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="ad001-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad001-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad001-247">Windows Server 2012</span></span>



| <span data-ttu-id="ad001-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad001-248">Entry</span></span> | <span data-ttu-id="ad001-249">Value</span><span class="sxs-lookup"><span data-stu-id="ad001-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="ad001-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ad001-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad001-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="ad001-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad001-252">System-Only</span></span>            | <span data-ttu-id="ad001-253">False</span><span class="sxs-lookup"><span data-stu-id="ad001-253">False</span></span>                           |
| <span data-ttu-id="ad001-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ad001-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ad001-255">False</span><span class="sxs-lookup"><span data-stu-id="ad001-255">False</span></span>                           |
| <span data-ttu-id="ad001-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ad001-256">Is Indexed</span></span>             | <span data-ttu-id="ad001-257">False</span><span class="sxs-lookup"><span data-stu-id="ad001-257">False</span></span>                           |
| <span data-ttu-id="ad001-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad001-258">In Global Catalog</span></span>      | <span data-ttu-id="ad001-259">False</span><span class="sxs-lookup"><span data-stu-id="ad001-259">False</span></span>                           |
| <span data-ttu-id="ad001-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ad001-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad001-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad001-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="ad001-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad001-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="ad001-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad001-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="ad001-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-264">Search-Flags</span></span>           | <span data-ttu-id="ad001-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad001-265">0x00000000</span></span>                      |
| <span data-ttu-id="ad001-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad001-266">System-Flags</span></span>           | <span data-ttu-id="ad001-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="ad001-267">0x00000014</span></span>                      |
| <span data-ttu-id="ad001-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ad001-268">Classes used in</span></span>        | [<span data-ttu-id="ad001-269">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="ad001-269">**Top**</span></span>](c-top.md)<br/> |



 

 






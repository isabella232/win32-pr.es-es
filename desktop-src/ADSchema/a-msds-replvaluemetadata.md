---
title: atributo MS-DS-REPL-Value-meta-data
description: Una lista de metadatos para cada valor de un atributo. Los metadatos indican quién cambió el valor en último lugar.
ms.assetid: 79c01bda-ea1b-41ca-b4de-c16c5167b270
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de metadatos de MS-DS-REPL-Value-meta
- Esquema de AD de atributo msDS-ReplValueMetaData
topic_type:
- apiref
api_name:
- ms-DS-Repl-Value-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e90cb5fd462fc75126b6ba80f10638826811d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659111"
---
# <a name="ms-ds-repl-value-meta-data-attribute"></a><span data-ttu-id="78c5f-106">atributo MS-DS-REPL-Value-meta-data</span><span class="sxs-lookup"><span data-stu-id="78c5f-106">ms-DS-Repl-Value-Meta-Data attribute</span></span>

<span data-ttu-id="78c5f-107">Una lista de metadatos para cada valor de un atributo.</span><span class="sxs-lookup"><span data-stu-id="78c5f-107">A list of metadata for each value of an attribute.</span></span> <span data-ttu-id="78c5f-108">Los metadatos indican quién cambió el valor en último lugar.</span><span class="sxs-lookup"><span data-stu-id="78c5f-108">The metadata indicates who changed the value last.</span></span>



| <span data-ttu-id="78c5f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="78c5f-109">Entry</span></span> | <span data-ttu-id="78c5f-110">Value</span><span class="sxs-lookup"><span data-stu-id="78c5f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="78c5f-111">CN</span><span class="sxs-lookup"><span data-stu-id="78c5f-111">CN</span></span>                | <span data-ttu-id="78c5f-112">MS-DS-REPL-Value-meta-data</span><span class="sxs-lookup"><span data-stu-id="78c5f-112">ms-DS-Repl-Value-Meta-Data</span></span>                  |
| <span data-ttu-id="78c5f-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="78c5f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="78c5f-114">msDS-ReplValueMetaData</span><span class="sxs-lookup"><span data-stu-id="78c5f-114">msDS-ReplValueMetaData</span></span>                      |
| <span data-ttu-id="78c5f-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="78c5f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="78c5f-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="78c5f-116">Update Privilege</span></span>  | <span data-ttu-id="78c5f-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="78c5f-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="78c5f-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="78c5f-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="78c5f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78c5f-119">Attribute-Id</span></span>      | <span data-ttu-id="78c5f-120">1.2.840.113556.1.4.1708</span><span class="sxs-lookup"><span data-stu-id="78c5f-120">1.2.840.113556.1.4.1708</span></span>                     |
| <span data-ttu-id="78c5f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="78c5f-121">System-Id-Guid</span></span>    | <span data-ttu-id="78c5f-122">2f5c8145-e1bd-410b-8957-8bfa81d5acfd</span><span class="sxs-lookup"><span data-stu-id="78c5f-122">2f5c8145-e1bd-410b-8957-8bfa81d5acfd</span></span>        |
| <span data-ttu-id="78c5f-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78c5f-123">Syntax</span></span>            | [<span data-ttu-id="78c5f-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="78c5f-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="78c5f-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="78c5f-125">Implementations</span></span>

-   [<span data-ttu-id="78c5f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78c5f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78c5f-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="78c5f-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="78c5f-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78c5f-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78c5f-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78c5f-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78c5f-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78c5f-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78c5f-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78c5f-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="78c5f-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78c5f-132">Windows Server 2003</span></span>



| <span data-ttu-id="78c5f-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="78c5f-133">Entry</span></span> | <span data-ttu-id="78c5f-134">Value</span><span class="sxs-lookup"><span data-stu-id="78c5f-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="78c5f-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="78c5f-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78c5f-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="78c5f-137">System-Only</span></span>            | <span data-ttu-id="78c5f-138">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-138">False</span></span>                           |
| <span data-ttu-id="78c5f-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="78c5f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="78c5f-140">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-140">False</span></span>                           |
| <span data-ttu-id="78c5f-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="78c5f-141">Is Indexed</span></span>             | <span data-ttu-id="78c5f-142">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-142">False</span></span>                           |
| <span data-ttu-id="78c5f-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="78c5f-143">In Global Catalog</span></span>      | <span data-ttu-id="78c5f-144">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-144">False</span></span>                           |
| <span data-ttu-id="78c5f-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="78c5f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="78c5f-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78c5f-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="78c5f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78c5f-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="78c5f-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78c5f-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="78c5f-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-149">Search-Flags</span></span>           | <span data-ttu-id="78c5f-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78c5f-150">0x00000000</span></span>                      |
| <span data-ttu-id="78c5f-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-151">System-Flags</span></span>           | <span data-ttu-id="78c5f-152">0x00000014</span><span class="sxs-lookup"><span data-stu-id="78c5f-152">0x00000014</span></span>                      |
| <span data-ttu-id="78c5f-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="78c5f-153">Classes used in</span></span>        | [<span data-ttu-id="78c5f-154">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="78c5f-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="78c5f-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="78c5f-155">ADAM</span></span>



| <span data-ttu-id="78c5f-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="78c5f-156">Entry</span></span> | <span data-ttu-id="78c5f-157">Value</span><span class="sxs-lookup"><span data-stu-id="78c5f-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="78c5f-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="78c5f-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78c5f-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="78c5f-160">System-Only</span></span>            | <span data-ttu-id="78c5f-161">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-161">False</span></span>                           |
| <span data-ttu-id="78c5f-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="78c5f-162">Is-Single-Valued</span></span>       | <span data-ttu-id="78c5f-163">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-163">False</span></span>                           |
| <span data-ttu-id="78c5f-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="78c5f-164">Is Indexed</span></span>             | <span data-ttu-id="78c5f-165">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-165">False</span></span>                           |
| <span data-ttu-id="78c5f-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="78c5f-166">In Global Catalog</span></span>      | <span data-ttu-id="78c5f-167">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-167">False</span></span>                           |
| <span data-ttu-id="78c5f-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="78c5f-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="78c5f-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78c5f-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="78c5f-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78c5f-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="78c5f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78c5f-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="78c5f-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-172">Search-Flags</span></span>           | <span data-ttu-id="78c5f-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78c5f-173">0x00000000</span></span>                      |
| <span data-ttu-id="78c5f-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-174">System-Flags</span></span>           | <span data-ttu-id="78c5f-175">0x00000014</span><span class="sxs-lookup"><span data-stu-id="78c5f-175">0x00000014</span></span>                      |
| <span data-ttu-id="78c5f-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="78c5f-176">Classes used in</span></span>        | [<span data-ttu-id="78c5f-177">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="78c5f-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78c5f-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78c5f-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78c5f-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="78c5f-179">Entry</span></span> | <span data-ttu-id="78c5f-180">Value</span><span class="sxs-lookup"><span data-stu-id="78c5f-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="78c5f-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="78c5f-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78c5f-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="78c5f-183">System-Only</span></span>            | <span data-ttu-id="78c5f-184">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-184">False</span></span>                           |
| <span data-ttu-id="78c5f-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="78c5f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="78c5f-186">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-186">False</span></span>                           |
| <span data-ttu-id="78c5f-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="78c5f-187">Is Indexed</span></span>             | <span data-ttu-id="78c5f-188">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-188">False</span></span>                           |
| <span data-ttu-id="78c5f-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="78c5f-189">In Global Catalog</span></span>      | <span data-ttu-id="78c5f-190">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-190">False</span></span>                           |
| <span data-ttu-id="78c5f-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="78c5f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="78c5f-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78c5f-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="78c5f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78c5f-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="78c5f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78c5f-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="78c5f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-195">Search-Flags</span></span>           | <span data-ttu-id="78c5f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78c5f-196">0x00000000</span></span>                      |
| <span data-ttu-id="78c5f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-197">System-Flags</span></span>           | <span data-ttu-id="78c5f-198">0x00000014</span><span class="sxs-lookup"><span data-stu-id="78c5f-198">0x00000014</span></span>                      |
| <span data-ttu-id="78c5f-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="78c5f-199">Classes used in</span></span>        | [<span data-ttu-id="78c5f-200">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="78c5f-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78c5f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78c5f-201">Windows Server 2008</span></span>



| <span data-ttu-id="78c5f-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="78c5f-202">Entry</span></span> | <span data-ttu-id="78c5f-203">Value</span><span class="sxs-lookup"><span data-stu-id="78c5f-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="78c5f-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="78c5f-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78c5f-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="78c5f-206">System-Only</span></span>            | <span data-ttu-id="78c5f-207">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-207">False</span></span>                           |
| <span data-ttu-id="78c5f-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="78c5f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="78c5f-209">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-209">False</span></span>                           |
| <span data-ttu-id="78c5f-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="78c5f-210">Is Indexed</span></span>             | <span data-ttu-id="78c5f-211">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-211">False</span></span>                           |
| <span data-ttu-id="78c5f-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="78c5f-212">In Global Catalog</span></span>      | <span data-ttu-id="78c5f-213">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-213">False</span></span>                           |
| <span data-ttu-id="78c5f-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="78c5f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="78c5f-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78c5f-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="78c5f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78c5f-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="78c5f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78c5f-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="78c5f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-218">Search-Flags</span></span>           | <span data-ttu-id="78c5f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78c5f-219">0x00000000</span></span>                      |
| <span data-ttu-id="78c5f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-220">System-Flags</span></span>           | <span data-ttu-id="78c5f-221">0x00000014</span><span class="sxs-lookup"><span data-stu-id="78c5f-221">0x00000014</span></span>                      |
| <span data-ttu-id="78c5f-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="78c5f-222">Classes used in</span></span>        | [<span data-ttu-id="78c5f-223">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="78c5f-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78c5f-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78c5f-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78c5f-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="78c5f-225">Entry</span></span> | <span data-ttu-id="78c5f-226">Value</span><span class="sxs-lookup"><span data-stu-id="78c5f-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="78c5f-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="78c5f-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78c5f-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="78c5f-229">System-Only</span></span>            | <span data-ttu-id="78c5f-230">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-230">False</span></span>                           |
| <span data-ttu-id="78c5f-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="78c5f-231">Is-Single-Valued</span></span>       | <span data-ttu-id="78c5f-232">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-232">False</span></span>                           |
| <span data-ttu-id="78c5f-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="78c5f-233">Is Indexed</span></span>             | <span data-ttu-id="78c5f-234">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-234">False</span></span>                           |
| <span data-ttu-id="78c5f-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="78c5f-235">In Global Catalog</span></span>      | <span data-ttu-id="78c5f-236">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-236">False</span></span>                           |
| <span data-ttu-id="78c5f-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="78c5f-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="78c5f-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78c5f-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="78c5f-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78c5f-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="78c5f-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78c5f-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="78c5f-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-241">Search-Flags</span></span>           | <span data-ttu-id="78c5f-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78c5f-242">0x00000000</span></span>                      |
| <span data-ttu-id="78c5f-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-243">System-Flags</span></span>           | <span data-ttu-id="78c5f-244">0x00000014</span><span class="sxs-lookup"><span data-stu-id="78c5f-244">0x00000014</span></span>                      |
| <span data-ttu-id="78c5f-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="78c5f-245">Classes used in</span></span>        | [<span data-ttu-id="78c5f-246">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="78c5f-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78c5f-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78c5f-247">Windows Server 2012</span></span>



| <span data-ttu-id="78c5f-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="78c5f-248">Entry</span></span> | <span data-ttu-id="78c5f-249">Value</span><span class="sxs-lookup"><span data-stu-id="78c5f-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="78c5f-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="78c5f-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78c5f-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="78c5f-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="78c5f-252">System-Only</span></span>            | <span data-ttu-id="78c5f-253">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-253">False</span></span>                           |
| <span data-ttu-id="78c5f-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="78c5f-254">Is-Single-Valued</span></span>       | <span data-ttu-id="78c5f-255">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-255">False</span></span>                           |
| <span data-ttu-id="78c5f-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="78c5f-256">Is Indexed</span></span>             | <span data-ttu-id="78c5f-257">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-257">False</span></span>                           |
| <span data-ttu-id="78c5f-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="78c5f-258">In Global Catalog</span></span>      | <span data-ttu-id="78c5f-259">False</span><span class="sxs-lookup"><span data-stu-id="78c5f-259">False</span></span>                           |
| <span data-ttu-id="78c5f-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="78c5f-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="78c5f-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="78c5f-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="78c5f-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78c5f-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="78c5f-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78c5f-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="78c5f-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-264">Search-Flags</span></span>           | <span data-ttu-id="78c5f-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78c5f-265">0x00000000</span></span>                      |
| <span data-ttu-id="78c5f-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78c5f-266">System-Flags</span></span>           | <span data-ttu-id="78c5f-267">0x00000014</span><span class="sxs-lookup"><span data-stu-id="78c5f-267">0x00000014</span></span>                      |
| <span data-ttu-id="78c5f-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="78c5f-268">Classes used in</span></span>        | [<span data-ttu-id="78c5f-269">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="78c5f-269">**Top**</span></span>](c-top.md)<br/> |



 

 






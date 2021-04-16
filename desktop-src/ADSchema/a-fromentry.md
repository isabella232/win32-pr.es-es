---
title: From-Entry atributo)
description: Se trata de un atributo construido que es TRUE si se puede escribir en el objeto y FALSE si es de solo lectura, por ejemplo, una instancia de réplica GC.
ms.assetid: b43e979d-15f9-4425-8a58-c9ed71bab1e4
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de From-Entry
- fromEntry esquema de AD de atributos
topic_type:
- apiref
api_name:
- From-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5f5e45e2897b917ad442f1b1b5d77246fa079c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658639"
---
# <a name="from-entry-attribute"></a><span data-ttu-id="12230-105">From-Entry atributo)</span><span class="sxs-lookup"><span data-stu-id="12230-105">From-Entry attribute</span></span>

<span data-ttu-id="12230-106">Se trata de un atributo construido que es **true** si se puede escribir en el objeto y **false** si es de solo lectura, por ejemplo, una instancia de réplica GC.</span><span class="sxs-lookup"><span data-stu-id="12230-106">This is a constructed attribute that is **TRUE** if the object is writable and **FALSE** if it is read-only, for example, a GC replica instance.</span></span>



| <span data-ttu-id="12230-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="12230-107">Entry</span></span> | <span data-ttu-id="12230-108">Value</span><span class="sxs-lookup"><span data-stu-id="12230-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="12230-109">CN</span><span class="sxs-lookup"><span data-stu-id="12230-109">CN</span></span>                | <span data-ttu-id="12230-110">From-Entry</span><span class="sxs-lookup"><span data-stu-id="12230-110">From-Entry</span></span>                           |
| <span data-ttu-id="12230-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="12230-111">Ldap-Display-Name</span></span> | <span data-ttu-id="12230-112">fromEntry</span><span class="sxs-lookup"><span data-stu-id="12230-112">fromEntry</span></span>                            |
| <span data-ttu-id="12230-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="12230-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="12230-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="12230-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="12230-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="12230-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="12230-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="12230-116">Attribute-Id</span></span>      | <span data-ttu-id="12230-117">1.2.840.113556.1.4.910</span><span class="sxs-lookup"><span data-stu-id="12230-117">1.2.840.113556.1.4.910</span></span>               |
| <span data-ttu-id="12230-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="12230-118">System-Id-Guid</span></span>    | <span data-ttu-id="12230-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="12230-119">9a7ad949-ca53-11d1-bbd0-0080c76670c0</span></span> |
| <span data-ttu-id="12230-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12230-120">Syntax</span></span>            | [<span data-ttu-id="12230-121">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="12230-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="12230-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="12230-122">Implementations</span></span>

-   [<span data-ttu-id="12230-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="12230-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="12230-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="12230-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="12230-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="12230-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="12230-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="12230-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="12230-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="12230-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="12230-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="12230-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="12230-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="12230-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="12230-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12230-130">Windows 2000 Server</span></span>



| <span data-ttu-id="12230-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="12230-131">Entry</span></span> | <span data-ttu-id="12230-132">Value</span><span class="sxs-lookup"><span data-stu-id="12230-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="12230-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12230-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12230-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="12230-135">System-Only</span></span>            | <span data-ttu-id="12230-136">True</span><span class="sxs-lookup"><span data-stu-id="12230-136">True</span></span>                            |
| <span data-ttu-id="12230-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12230-137">Is-Single-Valued</span></span>       | <span data-ttu-id="12230-138">False</span><span class="sxs-lookup"><span data-stu-id="12230-138">False</span></span>                           |
| <span data-ttu-id="12230-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12230-139">Is Indexed</span></span>             | <span data-ttu-id="12230-140">False</span><span class="sxs-lookup"><span data-stu-id="12230-140">False</span></span>                           |
| <span data-ttu-id="12230-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12230-141">In Global Catalog</span></span>      | <span data-ttu-id="12230-142">False</span><span class="sxs-lookup"><span data-stu-id="12230-142">False</span></span>                           |
| <span data-ttu-id="12230-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12230-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="12230-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12230-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="12230-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12230-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="12230-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12230-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="12230-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-147">Search-Flags</span></span>           | <span data-ttu-id="12230-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12230-148">0x00000000</span></span>                      |
| <span data-ttu-id="12230-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-149">System-Flags</span></span>           | <span data-ttu-id="12230-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12230-150">0x08000014</span></span>                      |
| <span data-ttu-id="12230-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12230-151">Classes used in</span></span>        | [<span data-ttu-id="12230-152">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="12230-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="12230-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12230-153">Windows Server 2003</span></span>



| <span data-ttu-id="12230-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="12230-154">Entry</span></span> | <span data-ttu-id="12230-155">Value</span><span class="sxs-lookup"><span data-stu-id="12230-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="12230-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12230-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12230-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="12230-158">System-Only</span></span>            | <span data-ttu-id="12230-159">True</span><span class="sxs-lookup"><span data-stu-id="12230-159">True</span></span>                            |
| <span data-ttu-id="12230-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12230-160">Is-Single-Valued</span></span>       | <span data-ttu-id="12230-161">False</span><span class="sxs-lookup"><span data-stu-id="12230-161">False</span></span>                           |
| <span data-ttu-id="12230-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12230-162">Is Indexed</span></span>             | <span data-ttu-id="12230-163">False</span><span class="sxs-lookup"><span data-stu-id="12230-163">False</span></span>                           |
| <span data-ttu-id="12230-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12230-164">In Global Catalog</span></span>      | <span data-ttu-id="12230-165">False</span><span class="sxs-lookup"><span data-stu-id="12230-165">False</span></span>                           |
| <span data-ttu-id="12230-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12230-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="12230-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12230-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="12230-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12230-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="12230-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12230-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="12230-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-170">Search-Flags</span></span>           | <span data-ttu-id="12230-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12230-171">0x00000000</span></span>                      |
| <span data-ttu-id="12230-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-172">System-Flags</span></span>           | <span data-ttu-id="12230-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12230-173">0x08000014</span></span>                      |
| <span data-ttu-id="12230-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12230-174">Classes used in</span></span>        | [<span data-ttu-id="12230-175">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="12230-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="12230-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="12230-176">ADAM</span></span>



| <span data-ttu-id="12230-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="12230-177">Entry</span></span> | <span data-ttu-id="12230-178">Value</span><span class="sxs-lookup"><span data-stu-id="12230-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="12230-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12230-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12230-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="12230-181">System-Only</span></span>            | <span data-ttu-id="12230-182">True</span><span class="sxs-lookup"><span data-stu-id="12230-182">True</span></span>                            |
| <span data-ttu-id="12230-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12230-183">Is-Single-Valued</span></span>       | <span data-ttu-id="12230-184">False</span><span class="sxs-lookup"><span data-stu-id="12230-184">False</span></span>                           |
| <span data-ttu-id="12230-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12230-185">Is Indexed</span></span>             | <span data-ttu-id="12230-186">False</span><span class="sxs-lookup"><span data-stu-id="12230-186">False</span></span>                           |
| <span data-ttu-id="12230-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12230-187">In Global Catalog</span></span>      | <span data-ttu-id="12230-188">False</span><span class="sxs-lookup"><span data-stu-id="12230-188">False</span></span>                           |
| <span data-ttu-id="12230-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12230-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="12230-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12230-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="12230-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12230-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="12230-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12230-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="12230-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-193">Search-Flags</span></span>           | <span data-ttu-id="12230-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12230-194">0x00000000</span></span>                      |
| <span data-ttu-id="12230-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-195">System-Flags</span></span>           | <span data-ttu-id="12230-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12230-196">0x08000014</span></span>                      |
| <span data-ttu-id="12230-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12230-197">Classes used in</span></span>        | [<span data-ttu-id="12230-198">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="12230-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="12230-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="12230-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="12230-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="12230-200">Entry</span></span> | <span data-ttu-id="12230-201">Value</span><span class="sxs-lookup"><span data-stu-id="12230-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="12230-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12230-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12230-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="12230-204">System-Only</span></span>            | <span data-ttu-id="12230-205">True</span><span class="sxs-lookup"><span data-stu-id="12230-205">True</span></span>                            |
| <span data-ttu-id="12230-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12230-206">Is-Single-Valued</span></span>       | <span data-ttu-id="12230-207">False</span><span class="sxs-lookup"><span data-stu-id="12230-207">False</span></span>                           |
| <span data-ttu-id="12230-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12230-208">Is Indexed</span></span>             | <span data-ttu-id="12230-209">False</span><span class="sxs-lookup"><span data-stu-id="12230-209">False</span></span>                           |
| <span data-ttu-id="12230-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12230-210">In Global Catalog</span></span>      | <span data-ttu-id="12230-211">False</span><span class="sxs-lookup"><span data-stu-id="12230-211">False</span></span>                           |
| <span data-ttu-id="12230-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12230-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="12230-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12230-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="12230-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12230-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="12230-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12230-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="12230-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-216">Search-Flags</span></span>           | <span data-ttu-id="12230-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12230-217">0x00000000</span></span>                      |
| <span data-ttu-id="12230-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-218">System-Flags</span></span>           | <span data-ttu-id="12230-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12230-219">0x08000014</span></span>                      |
| <span data-ttu-id="12230-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12230-220">Classes used in</span></span>        | [<span data-ttu-id="12230-221">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="12230-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="12230-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12230-222">Windows Server 2008</span></span>



| <span data-ttu-id="12230-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="12230-223">Entry</span></span> | <span data-ttu-id="12230-224">Value</span><span class="sxs-lookup"><span data-stu-id="12230-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="12230-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12230-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12230-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="12230-227">System-Only</span></span>            | <span data-ttu-id="12230-228">True</span><span class="sxs-lookup"><span data-stu-id="12230-228">True</span></span>                            |
| <span data-ttu-id="12230-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12230-229">Is-Single-Valued</span></span>       | <span data-ttu-id="12230-230">False</span><span class="sxs-lookup"><span data-stu-id="12230-230">False</span></span>                           |
| <span data-ttu-id="12230-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12230-231">Is Indexed</span></span>             | <span data-ttu-id="12230-232">False</span><span class="sxs-lookup"><span data-stu-id="12230-232">False</span></span>                           |
| <span data-ttu-id="12230-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12230-233">In Global Catalog</span></span>      | <span data-ttu-id="12230-234">False</span><span class="sxs-lookup"><span data-stu-id="12230-234">False</span></span>                           |
| <span data-ttu-id="12230-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12230-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="12230-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12230-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="12230-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12230-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="12230-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12230-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="12230-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-239">Search-Flags</span></span>           | <span data-ttu-id="12230-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12230-240">0x00000000</span></span>                      |
| <span data-ttu-id="12230-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-241">System-Flags</span></span>           | <span data-ttu-id="12230-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12230-242">0x08000014</span></span>                      |
| <span data-ttu-id="12230-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12230-243">Classes used in</span></span>        | [<span data-ttu-id="12230-244">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="12230-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="12230-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12230-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="12230-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="12230-246">Entry</span></span> | <span data-ttu-id="12230-247">Value</span><span class="sxs-lookup"><span data-stu-id="12230-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="12230-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12230-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12230-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="12230-250">System-Only</span></span>            | <span data-ttu-id="12230-251">True</span><span class="sxs-lookup"><span data-stu-id="12230-251">True</span></span>                            |
| <span data-ttu-id="12230-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12230-252">Is-Single-Valued</span></span>       | <span data-ttu-id="12230-253">False</span><span class="sxs-lookup"><span data-stu-id="12230-253">False</span></span>                           |
| <span data-ttu-id="12230-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12230-254">Is Indexed</span></span>             | <span data-ttu-id="12230-255">False</span><span class="sxs-lookup"><span data-stu-id="12230-255">False</span></span>                           |
| <span data-ttu-id="12230-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12230-256">In Global Catalog</span></span>      | <span data-ttu-id="12230-257">False</span><span class="sxs-lookup"><span data-stu-id="12230-257">False</span></span>                           |
| <span data-ttu-id="12230-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12230-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="12230-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12230-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="12230-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12230-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="12230-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12230-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="12230-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-262">Search-Flags</span></span>           | <span data-ttu-id="12230-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12230-263">0x00000000</span></span>                      |
| <span data-ttu-id="12230-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-264">System-Flags</span></span>           | <span data-ttu-id="12230-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12230-265">0x08000014</span></span>                      |
| <span data-ttu-id="12230-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12230-266">Classes used in</span></span>        | [<span data-ttu-id="12230-267">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="12230-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="12230-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12230-268">Windows Server 2012</span></span>



| <span data-ttu-id="12230-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="12230-269">Entry</span></span> | <span data-ttu-id="12230-270">Value</span><span class="sxs-lookup"><span data-stu-id="12230-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="12230-271">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12230-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12230-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="12230-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="12230-273">System-Only</span></span>            | <span data-ttu-id="12230-274">True</span><span class="sxs-lookup"><span data-stu-id="12230-274">True</span></span>                            |
| <span data-ttu-id="12230-275">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12230-275">Is-Single-Valued</span></span>       | <span data-ttu-id="12230-276">False</span><span class="sxs-lookup"><span data-stu-id="12230-276">False</span></span>                           |
| <span data-ttu-id="12230-277">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12230-277">Is Indexed</span></span>             | <span data-ttu-id="12230-278">False</span><span class="sxs-lookup"><span data-stu-id="12230-278">False</span></span>                           |
| <span data-ttu-id="12230-279">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12230-279">In Global Catalog</span></span>      | <span data-ttu-id="12230-280">False</span><span class="sxs-lookup"><span data-stu-id="12230-280">False</span></span>                           |
| <span data-ttu-id="12230-281">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12230-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="12230-282">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12230-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="12230-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12230-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="12230-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12230-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="12230-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-285">Search-Flags</span></span>           | <span data-ttu-id="12230-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12230-286">0x00000000</span></span>                      |
| <span data-ttu-id="12230-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12230-287">System-Flags</span></span>           | <span data-ttu-id="12230-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12230-288">0x08000014</span></span>                      |
| <span data-ttu-id="12230-289">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12230-289">Classes used in</span></span>        | [<span data-ttu-id="12230-290">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="12230-290">**Top**</span></span>](c-top.md)<br/> |



 

 






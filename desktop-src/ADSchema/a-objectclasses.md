---
title: Object-Classes atributo)
description: Una propiedad de varios valores que contiene cadenas que representan cada clase en el esquema. Cada valor contiene los valores governsID, lDAPDisplayName, mustContain, mayContain, etc.
ms.assetid: 7e3eda48-8e64-4a52-8d92-7a0d37e513ef
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Object-Classes
- objectClasses esquema de AD de atributos
topic_type:
- apiref
api_name:
- Object-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b799c725790115152ac70c0214d82a8c242ea600
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906147"
---
# <a name="object-classes-attribute"></a><span data-ttu-id="45089-106">Object-Classes atributo)</span><span class="sxs-lookup"><span data-stu-id="45089-106">Object-Classes attribute</span></span>

<span data-ttu-id="45089-107">Una propiedad de varios valores que contiene cadenas que representan cada clase en el esquema.</span><span class="sxs-lookup"><span data-stu-id="45089-107">A multiple-valued property that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="45089-108">Cada valor contiene los valores governsID, lDAPDisplayName, mustContain, mayContain, etc.</span><span class="sxs-lookup"><span data-stu-id="45089-108">Each value contains the governsID, lDAPDisplayName, mustContain, mayContain, and so on.</span></span>



| <span data-ttu-id="45089-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="45089-109">Entry</span></span> | <span data-ttu-id="45089-110">Value</span><span class="sxs-lookup"><span data-stu-id="45089-110">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="45089-111">CN</span><span class="sxs-lookup"><span data-stu-id="45089-111">CN</span></span>                | <span data-ttu-id="45089-112">Object-Classes</span><span class="sxs-lookup"><span data-stu-id="45089-112">Object-Classes</span></span>                                   |
| <span data-ttu-id="45089-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="45089-113">Ldap-Display-Name</span></span> | <span data-ttu-id="45089-114">objectClasses</span><span class="sxs-lookup"><span data-stu-id="45089-114">objectClasses</span></span>                                    |
| <span data-ttu-id="45089-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="45089-115">Size</span></span>              | <span data-ttu-id="45089-116">Unos 20 bytes como promedio por nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="45089-116">About 20 bytes on average per class name.</span></span>        |
| <span data-ttu-id="45089-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="45089-117">Update Privilege</span></span>  | <span data-ttu-id="45089-118">El diseñador del objeto establecería este valor.</span><span class="sxs-lookup"><span data-stu-id="45089-118">The designer of the object would set this value.</span></span> |
| <span data-ttu-id="45089-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="45089-119">Update Frequency</span></span>  | <span data-ttu-id="45089-120">Cada vez que el diseño de la clase cambia.</span><span class="sxs-lookup"><span data-stu-id="45089-120">Whenever the design of the class changes.</span></span>        |
| <span data-ttu-id="45089-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="45089-121">Attribute-Id</span></span>      | <span data-ttu-id="45089-122">2.5.21.6</span><span class="sxs-lookup"><span data-stu-id="45089-122">2.5.21.6</span></span>                                         |
| <span data-ttu-id="45089-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="45089-123">System-Id-Guid</span></span>    | <span data-ttu-id="45089-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="45089-124">9a7ad94b-ca53-11d1-bbd0-0080c76670c0</span></span>             |
| <span data-ttu-id="45089-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45089-125">Syntax</span></span>            | [<span data-ttu-id="45089-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="45089-126">**String(Unicode)**</span></span>](s-string-unicode.md)      |



## <a name="implementations"></a><span data-ttu-id="45089-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="45089-127">Implementations</span></span>

-   [<span data-ttu-id="45089-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="45089-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="45089-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="45089-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="45089-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="45089-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="45089-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="45089-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="45089-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="45089-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="45089-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="45089-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="45089-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="45089-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="45089-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45089-135">Windows 2000 Server</span></span>



| <span data-ttu-id="45089-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="45089-136">Entry</span></span> | <span data-ttu-id="45089-137">Value</span><span class="sxs-lookup"><span data-stu-id="45089-137">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="45089-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="45089-138">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45089-139">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="45089-140">System-Only</span></span>            | <span data-ttu-id="45089-141">True</span><span class="sxs-lookup"><span data-stu-id="45089-141">True</span></span>                                        |
| <span data-ttu-id="45089-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="45089-142">Is-Single-Valued</span></span>       | <span data-ttu-id="45089-143">False</span><span class="sxs-lookup"><span data-stu-id="45089-143">False</span></span>                                       |
| <span data-ttu-id="45089-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="45089-144">Is Indexed</span></span>             | <span data-ttu-id="45089-145">False</span><span class="sxs-lookup"><span data-stu-id="45089-145">False</span></span>                                       |
| <span data-ttu-id="45089-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="45089-146">In Global Catalog</span></span>      | <span data-ttu-id="45089-147">False</span><span class="sxs-lookup"><span data-stu-id="45089-147">False</span></span>                                       |
| <span data-ttu-id="45089-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="45089-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="45089-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45089-149">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="45089-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45089-150">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="45089-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45089-151">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="45089-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-152">Search-Flags</span></span>           | <span data-ttu-id="45089-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45089-153">0x00000000</span></span>                                  |
| <span data-ttu-id="45089-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-154">System-Flags</span></span>           | <span data-ttu-id="45089-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="45089-155">0x08000014</span></span>                                  |
| <span data-ttu-id="45089-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="45089-156">Classes used in</span></span>        | [<span data-ttu-id="45089-157">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="45089-157">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="45089-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="45089-158">Windows Server 2003</span></span>



| <span data-ttu-id="45089-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="45089-159">Entry</span></span> | <span data-ttu-id="45089-160">Value</span><span class="sxs-lookup"><span data-stu-id="45089-160">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="45089-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="45089-161">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45089-162">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="45089-163">System-Only</span></span>            | <span data-ttu-id="45089-164">True</span><span class="sxs-lookup"><span data-stu-id="45089-164">True</span></span>                                        |
| <span data-ttu-id="45089-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="45089-165">Is-Single-Valued</span></span>       | <span data-ttu-id="45089-166">False</span><span class="sxs-lookup"><span data-stu-id="45089-166">False</span></span>                                       |
| <span data-ttu-id="45089-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="45089-167">Is Indexed</span></span>             | <span data-ttu-id="45089-168">False</span><span class="sxs-lookup"><span data-stu-id="45089-168">False</span></span>                                       |
| <span data-ttu-id="45089-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="45089-169">In Global Catalog</span></span>      | <span data-ttu-id="45089-170">False</span><span class="sxs-lookup"><span data-stu-id="45089-170">False</span></span>                                       |
| <span data-ttu-id="45089-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="45089-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="45089-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45089-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="45089-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45089-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="45089-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45089-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="45089-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-175">Search-Flags</span></span>           | <span data-ttu-id="45089-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45089-176">0x00000000</span></span>                                  |
| <span data-ttu-id="45089-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-177">System-Flags</span></span>           | <span data-ttu-id="45089-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="45089-178">0x08000014</span></span>                                  |
| <span data-ttu-id="45089-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="45089-179">Classes used in</span></span>        | [<span data-ttu-id="45089-180">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="45089-180">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="45089-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="45089-181">ADAM</span></span>



| <span data-ttu-id="45089-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="45089-182">Entry</span></span> | <span data-ttu-id="45089-183">Value</span><span class="sxs-lookup"><span data-stu-id="45089-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="45089-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="45089-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45089-185">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="45089-186">System-Only</span></span>            | <span data-ttu-id="45089-187">True</span><span class="sxs-lookup"><span data-stu-id="45089-187">True</span></span>                                        |
| <span data-ttu-id="45089-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="45089-188">Is-Single-Valued</span></span>       | <span data-ttu-id="45089-189">False</span><span class="sxs-lookup"><span data-stu-id="45089-189">False</span></span>                                       |
| <span data-ttu-id="45089-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="45089-190">Is Indexed</span></span>             | <span data-ttu-id="45089-191">False</span><span class="sxs-lookup"><span data-stu-id="45089-191">False</span></span>                                       |
| <span data-ttu-id="45089-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="45089-192">In Global Catalog</span></span>      | <span data-ttu-id="45089-193">False</span><span class="sxs-lookup"><span data-stu-id="45089-193">False</span></span>                                       |
| <span data-ttu-id="45089-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="45089-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="45089-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45089-195">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="45089-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45089-196">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="45089-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45089-197">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="45089-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-198">Search-Flags</span></span>           | <span data-ttu-id="45089-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45089-199">0x00000000</span></span>                                  |
| <span data-ttu-id="45089-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-200">System-Flags</span></span>           | <span data-ttu-id="45089-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="45089-201">0x08000014</span></span>                                  |
| <span data-ttu-id="45089-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="45089-202">Classes used in</span></span>        | [<span data-ttu-id="45089-203">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="45089-203">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="45089-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="45089-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="45089-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="45089-205">Entry</span></span> | <span data-ttu-id="45089-206">Value</span><span class="sxs-lookup"><span data-stu-id="45089-206">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="45089-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="45089-207">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45089-208">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="45089-209">System-Only</span></span>            | <span data-ttu-id="45089-210">True</span><span class="sxs-lookup"><span data-stu-id="45089-210">True</span></span>                                        |
| <span data-ttu-id="45089-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="45089-211">Is-Single-Valued</span></span>       | <span data-ttu-id="45089-212">False</span><span class="sxs-lookup"><span data-stu-id="45089-212">False</span></span>                                       |
| <span data-ttu-id="45089-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="45089-213">Is Indexed</span></span>             | <span data-ttu-id="45089-214">False</span><span class="sxs-lookup"><span data-stu-id="45089-214">False</span></span>                                       |
| <span data-ttu-id="45089-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="45089-215">In Global Catalog</span></span>      | <span data-ttu-id="45089-216">False</span><span class="sxs-lookup"><span data-stu-id="45089-216">False</span></span>                                       |
| <span data-ttu-id="45089-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="45089-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="45089-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45089-218">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="45089-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45089-219">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="45089-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45089-220">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="45089-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-221">Search-Flags</span></span>           | <span data-ttu-id="45089-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45089-222">0x00000000</span></span>                                  |
| <span data-ttu-id="45089-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-223">System-Flags</span></span>           | <span data-ttu-id="45089-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="45089-224">0x08000014</span></span>                                  |
| <span data-ttu-id="45089-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="45089-225">Classes used in</span></span>        | [<span data-ttu-id="45089-226">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="45089-226">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="45089-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45089-227">Windows Server 2008</span></span>



| <span data-ttu-id="45089-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="45089-228">Entry</span></span> | <span data-ttu-id="45089-229">Value</span><span class="sxs-lookup"><span data-stu-id="45089-229">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="45089-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="45089-230">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45089-231">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="45089-232">System-Only</span></span>            | <span data-ttu-id="45089-233">True</span><span class="sxs-lookup"><span data-stu-id="45089-233">True</span></span>                                        |
| <span data-ttu-id="45089-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="45089-234">Is-Single-Valued</span></span>       | <span data-ttu-id="45089-235">False</span><span class="sxs-lookup"><span data-stu-id="45089-235">False</span></span>                                       |
| <span data-ttu-id="45089-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="45089-236">Is Indexed</span></span>             | <span data-ttu-id="45089-237">False</span><span class="sxs-lookup"><span data-stu-id="45089-237">False</span></span>                                       |
| <span data-ttu-id="45089-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="45089-238">In Global Catalog</span></span>      | <span data-ttu-id="45089-239">False</span><span class="sxs-lookup"><span data-stu-id="45089-239">False</span></span>                                       |
| <span data-ttu-id="45089-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="45089-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="45089-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45089-241">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="45089-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45089-242">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="45089-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45089-243">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="45089-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-244">Search-Flags</span></span>           | <span data-ttu-id="45089-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45089-245">0x00000000</span></span>                                  |
| <span data-ttu-id="45089-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-246">System-Flags</span></span>           | <span data-ttu-id="45089-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="45089-247">0x08000014</span></span>                                  |
| <span data-ttu-id="45089-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="45089-248">Classes used in</span></span>        | [<span data-ttu-id="45089-249">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="45089-249">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="45089-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45089-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="45089-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="45089-251">Entry</span></span> | <span data-ttu-id="45089-252">Value</span><span class="sxs-lookup"><span data-stu-id="45089-252">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="45089-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="45089-253">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45089-254">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="45089-255">System-Only</span></span>            | <span data-ttu-id="45089-256">True</span><span class="sxs-lookup"><span data-stu-id="45089-256">True</span></span>                                        |
| <span data-ttu-id="45089-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="45089-257">Is-Single-Valued</span></span>       | <span data-ttu-id="45089-258">False</span><span class="sxs-lookup"><span data-stu-id="45089-258">False</span></span>                                       |
| <span data-ttu-id="45089-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="45089-259">Is Indexed</span></span>             | <span data-ttu-id="45089-260">False</span><span class="sxs-lookup"><span data-stu-id="45089-260">False</span></span>                                       |
| <span data-ttu-id="45089-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="45089-261">In Global Catalog</span></span>      | <span data-ttu-id="45089-262">False</span><span class="sxs-lookup"><span data-stu-id="45089-262">False</span></span>                                       |
| <span data-ttu-id="45089-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="45089-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="45089-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45089-264">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="45089-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45089-265">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="45089-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45089-266">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="45089-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-267">Search-Flags</span></span>           | <span data-ttu-id="45089-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45089-268">0x00000000</span></span>                                  |
| <span data-ttu-id="45089-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-269">System-Flags</span></span>           | <span data-ttu-id="45089-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="45089-270">0x08000014</span></span>                                  |
| <span data-ttu-id="45089-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="45089-271">Classes used in</span></span>        | [<span data-ttu-id="45089-272">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="45089-272">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="45089-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45089-273">Windows Server 2012</span></span>



| <span data-ttu-id="45089-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="45089-274">Entry</span></span> | <span data-ttu-id="45089-275">Value</span><span class="sxs-lookup"><span data-stu-id="45089-275">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="45089-276">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="45089-276">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45089-277">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="45089-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="45089-278">System-Only</span></span>            | <span data-ttu-id="45089-279">True</span><span class="sxs-lookup"><span data-stu-id="45089-279">True</span></span>                                        |
| <span data-ttu-id="45089-280">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="45089-280">Is-Single-Valued</span></span>       | <span data-ttu-id="45089-281">False</span><span class="sxs-lookup"><span data-stu-id="45089-281">False</span></span>                                       |
| <span data-ttu-id="45089-282">Está indexado</span><span class="sxs-lookup"><span data-stu-id="45089-282">Is Indexed</span></span>             | <span data-ttu-id="45089-283">False</span><span class="sxs-lookup"><span data-stu-id="45089-283">False</span></span>                                       |
| <span data-ttu-id="45089-284">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="45089-284">In Global Catalog</span></span>      | <span data-ttu-id="45089-285">False</span><span class="sxs-lookup"><span data-stu-id="45089-285">False</span></span>                                       |
| <span data-ttu-id="45089-286">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="45089-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="45089-287">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="45089-287">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="45089-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45089-288">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="45089-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45089-289">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="45089-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-290">Search-Flags</span></span>           | <span data-ttu-id="45089-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45089-291">0x00000000</span></span>                                  |
| <span data-ttu-id="45089-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45089-292">System-Flags</span></span>           | <span data-ttu-id="45089-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="45089-293">0x08000014</span></span>                                  |
| <span data-ttu-id="45089-294">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="45089-294">Classes used in</span></span>        | [<span data-ttu-id="45089-295">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="45089-295">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 






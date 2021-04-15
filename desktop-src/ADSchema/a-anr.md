---
title: ANR (atributo)
description: Atributo de resolución de nombres ambiguo que se va a usar al elegir entre objetos.
ms.assetid: 9057dc7e-f669-4821-86b0-703ff7e5b120
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ANR
- Esquema de AD del atributo aNR
topic_type:
- apiref
api_name:
- ANR
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28efc6d6871eb737f9c1953fbdb5ad5798f7fd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494116"
---
# <a name="anr-attribute"></a><span data-ttu-id="12024-105">ANR (atributo)</span><span class="sxs-lookup"><span data-stu-id="12024-105">ANR attribute</span></span>

<span data-ttu-id="12024-106">Atributo de resolución de nombres ambiguo que se va a usar al elegir entre objetos.</span><span class="sxs-lookup"><span data-stu-id="12024-106">Ambiguous name resolution attribute to be used when choosing between objects.</span></span>



| <span data-ttu-id="12024-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="12024-107">Entry</span></span> | <span data-ttu-id="12024-108">Value</span><span class="sxs-lookup"><span data-stu-id="12024-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="12024-109">CN</span><span class="sxs-lookup"><span data-stu-id="12024-109">CN</span></span>                | <span data-ttu-id="12024-110">ANR</span><span class="sxs-lookup"><span data-stu-id="12024-110">ANR</span></span>                                                               |
| <span data-ttu-id="12024-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="12024-111">Ldap-Display-Name</span></span> | <span data-ttu-id="12024-112">aNR</span><span class="sxs-lookup"><span data-stu-id="12024-112">aNR</span></span>                                                               |
| <span data-ttu-id="12024-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="12024-113">Size</span></span>              | \-                                                                |
| <span data-ttu-id="12024-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="12024-114">Update Privilege</span></span>  | <span data-ttu-id="12024-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="12024-115">Schema administrator</span></span>                                              |
| <span data-ttu-id="12024-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="12024-116">Update Frequency</span></span>  | <span data-ttu-id="12024-117">Cuando es necesario agregar o quitar un atributo de la lista de ANR.</span><span class="sxs-lookup"><span data-stu-id="12024-117">When an attribute needs to be added or removed from the ANR list.</span></span> |
| <span data-ttu-id="12024-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="12024-118">Attribute-Id</span></span>      | <span data-ttu-id="12024-119">1.2.840.113556.1.4.1208</span><span class="sxs-lookup"><span data-stu-id="12024-119">1.2.840.113556.1.4.1208</span></span>                                           |
| <span data-ttu-id="12024-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="12024-120">System-Id-Guid</span></span>    | <span data-ttu-id="12024-121">45b01500-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="12024-121">45b01500-c419-11d1-bbc9-0080c76670c0</span></span>                              |
| <span data-ttu-id="12024-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12024-122">Syntax</span></span>            | [<span data-ttu-id="12024-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="12024-123">**String(Unicode)**</span></span>](s-string-unicode.md)                       |



## <a name="implementations"></a><span data-ttu-id="12024-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="12024-124">Implementations</span></span>

-   [<span data-ttu-id="12024-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="12024-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="12024-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="12024-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="12024-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="12024-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="12024-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="12024-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="12024-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="12024-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="12024-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="12024-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="12024-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="12024-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="12024-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12024-132">Windows 2000 Server</span></span>



| <span data-ttu-id="12024-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="12024-133">Entry</span></span> | <span data-ttu-id="12024-134">Value</span><span class="sxs-lookup"><span data-stu-id="12024-134">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="12024-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12024-135">Link-Id</span></span>                | \-           |
| <span data-ttu-id="12024-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12024-136">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="12024-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="12024-137">System-Only</span></span>            | <span data-ttu-id="12024-138">False</span><span class="sxs-lookup"><span data-stu-id="12024-138">False</span></span>        |
| <span data-ttu-id="12024-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12024-139">Is-Single-Valued</span></span>       | <span data-ttu-id="12024-140">True</span><span class="sxs-lookup"><span data-stu-id="12024-140">True</span></span>         |
| <span data-ttu-id="12024-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12024-141">Is Indexed</span></span>             | <span data-ttu-id="12024-142">False</span><span class="sxs-lookup"><span data-stu-id="12024-142">False</span></span>        |
| <span data-ttu-id="12024-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12024-143">In Global Catalog</span></span>      | <span data-ttu-id="12024-144">False</span><span class="sxs-lookup"><span data-stu-id="12024-144">False</span></span>        |
| <span data-ttu-id="12024-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12024-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="12024-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12024-146">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="12024-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12024-147">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="12024-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12024-148">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="12024-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-149">Search-Flags</span></span>           | <span data-ttu-id="12024-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12024-150">0x00000000</span></span>   |
| <span data-ttu-id="12024-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-151">System-Flags</span></span>           | <span data-ttu-id="12024-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12024-152">0x08000014</span></span>   |
| <span data-ttu-id="12024-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12024-153">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="12024-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12024-154">Windows Server 2003</span></span>



| <span data-ttu-id="12024-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="12024-155">Entry</span></span> | <span data-ttu-id="12024-156">Value</span><span class="sxs-lookup"><span data-stu-id="12024-156">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="12024-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12024-157">Link-Id</span></span>                | \-           |
| <span data-ttu-id="12024-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12024-158">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="12024-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="12024-159">System-Only</span></span>            | <span data-ttu-id="12024-160">False</span><span class="sxs-lookup"><span data-stu-id="12024-160">False</span></span>        |
| <span data-ttu-id="12024-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12024-161">Is-Single-Valued</span></span>       | <span data-ttu-id="12024-162">True</span><span class="sxs-lookup"><span data-stu-id="12024-162">True</span></span>         |
| <span data-ttu-id="12024-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12024-163">Is Indexed</span></span>             | <span data-ttu-id="12024-164">False</span><span class="sxs-lookup"><span data-stu-id="12024-164">False</span></span>        |
| <span data-ttu-id="12024-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12024-165">In Global Catalog</span></span>      | <span data-ttu-id="12024-166">False</span><span class="sxs-lookup"><span data-stu-id="12024-166">False</span></span>        |
| <span data-ttu-id="12024-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12024-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="12024-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12024-168">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="12024-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12024-169">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="12024-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12024-170">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="12024-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-171">Search-Flags</span></span>           | <span data-ttu-id="12024-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12024-172">0x00000000</span></span>   |
| <span data-ttu-id="12024-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-173">System-Flags</span></span>           | <span data-ttu-id="12024-174">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12024-174">0x08000014</span></span>   |
| <span data-ttu-id="12024-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12024-175">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="12024-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="12024-176">ADAM</span></span>



| <span data-ttu-id="12024-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="12024-177">Entry</span></span> | <span data-ttu-id="12024-178">Value</span><span class="sxs-lookup"><span data-stu-id="12024-178">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="12024-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12024-179">Link-Id</span></span>                | \-           |
| <span data-ttu-id="12024-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12024-180">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="12024-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="12024-181">System-Only</span></span>            | <span data-ttu-id="12024-182">False</span><span class="sxs-lookup"><span data-stu-id="12024-182">False</span></span>        |
| <span data-ttu-id="12024-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12024-183">Is-Single-Valued</span></span>       | <span data-ttu-id="12024-184">True</span><span class="sxs-lookup"><span data-stu-id="12024-184">True</span></span>         |
| <span data-ttu-id="12024-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12024-185">Is Indexed</span></span>             | <span data-ttu-id="12024-186">False</span><span class="sxs-lookup"><span data-stu-id="12024-186">False</span></span>        |
| <span data-ttu-id="12024-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12024-187">In Global Catalog</span></span>      | <span data-ttu-id="12024-188">False</span><span class="sxs-lookup"><span data-stu-id="12024-188">False</span></span>        |
| <span data-ttu-id="12024-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12024-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="12024-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12024-190">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="12024-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12024-191">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="12024-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12024-192">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="12024-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-193">Search-Flags</span></span>           | <span data-ttu-id="12024-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12024-194">0x00000000</span></span>   |
| <span data-ttu-id="12024-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-195">System-Flags</span></span>           | <span data-ttu-id="12024-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12024-196">0x08000014</span></span>   |
| <span data-ttu-id="12024-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12024-197">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="12024-198">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="12024-198">Windows Server 2003 R2</span></span>



| <span data-ttu-id="12024-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="12024-199">Entry</span></span> | <span data-ttu-id="12024-200">Value</span><span class="sxs-lookup"><span data-stu-id="12024-200">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="12024-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12024-201">Link-Id</span></span>                | \-           |
| <span data-ttu-id="12024-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12024-202">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="12024-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="12024-203">System-Only</span></span>            | <span data-ttu-id="12024-204">False</span><span class="sxs-lookup"><span data-stu-id="12024-204">False</span></span>        |
| <span data-ttu-id="12024-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12024-205">Is-Single-Valued</span></span>       | <span data-ttu-id="12024-206">True</span><span class="sxs-lookup"><span data-stu-id="12024-206">True</span></span>         |
| <span data-ttu-id="12024-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12024-207">Is Indexed</span></span>             | <span data-ttu-id="12024-208">False</span><span class="sxs-lookup"><span data-stu-id="12024-208">False</span></span>        |
| <span data-ttu-id="12024-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12024-209">In Global Catalog</span></span>      | <span data-ttu-id="12024-210">False</span><span class="sxs-lookup"><span data-stu-id="12024-210">False</span></span>        |
| <span data-ttu-id="12024-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12024-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="12024-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12024-212">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="12024-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12024-213">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="12024-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12024-214">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="12024-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-215">Search-Flags</span></span>           | <span data-ttu-id="12024-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12024-216">0x00000000</span></span>   |
| <span data-ttu-id="12024-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-217">System-Flags</span></span>           | <span data-ttu-id="12024-218">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12024-218">0x08000014</span></span>   |
| <span data-ttu-id="12024-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12024-219">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="12024-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12024-220">Windows Server 2008</span></span>



| <span data-ttu-id="12024-221">Entrada</span><span class="sxs-lookup"><span data-stu-id="12024-221">Entry</span></span> | <span data-ttu-id="12024-222">Value</span><span class="sxs-lookup"><span data-stu-id="12024-222">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="12024-223">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12024-223">Link-Id</span></span>                | \-           |
| <span data-ttu-id="12024-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12024-224">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="12024-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="12024-225">System-Only</span></span>            | <span data-ttu-id="12024-226">False</span><span class="sxs-lookup"><span data-stu-id="12024-226">False</span></span>        |
| <span data-ttu-id="12024-227">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12024-227">Is-Single-Valued</span></span>       | <span data-ttu-id="12024-228">True</span><span class="sxs-lookup"><span data-stu-id="12024-228">True</span></span>         |
| <span data-ttu-id="12024-229">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12024-229">Is Indexed</span></span>             | <span data-ttu-id="12024-230">False</span><span class="sxs-lookup"><span data-stu-id="12024-230">False</span></span>        |
| <span data-ttu-id="12024-231">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12024-231">In Global Catalog</span></span>      | <span data-ttu-id="12024-232">False</span><span class="sxs-lookup"><span data-stu-id="12024-232">False</span></span>        |
| <span data-ttu-id="12024-233">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12024-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="12024-234">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12024-234">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="12024-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12024-235">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="12024-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12024-236">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="12024-237">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-237">Search-Flags</span></span>           | <span data-ttu-id="12024-238">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12024-238">0x00000000</span></span>   |
| <span data-ttu-id="12024-239">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-239">System-Flags</span></span>           | <span data-ttu-id="12024-240">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12024-240">0x08000014</span></span>   |
| <span data-ttu-id="12024-241">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12024-241">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="12024-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12024-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="12024-243">Entrada</span><span class="sxs-lookup"><span data-stu-id="12024-243">Entry</span></span> | <span data-ttu-id="12024-244">Value</span><span class="sxs-lookup"><span data-stu-id="12024-244">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="12024-245">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12024-245">Link-Id</span></span>                | \-           |
| <span data-ttu-id="12024-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12024-246">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="12024-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="12024-247">System-Only</span></span>            | <span data-ttu-id="12024-248">False</span><span class="sxs-lookup"><span data-stu-id="12024-248">False</span></span>        |
| <span data-ttu-id="12024-249">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12024-249">Is-Single-Valued</span></span>       | <span data-ttu-id="12024-250">True</span><span class="sxs-lookup"><span data-stu-id="12024-250">True</span></span>         |
| <span data-ttu-id="12024-251">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12024-251">Is Indexed</span></span>             | <span data-ttu-id="12024-252">False</span><span class="sxs-lookup"><span data-stu-id="12024-252">False</span></span>        |
| <span data-ttu-id="12024-253">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12024-253">In Global Catalog</span></span>      | <span data-ttu-id="12024-254">False</span><span class="sxs-lookup"><span data-stu-id="12024-254">False</span></span>        |
| <span data-ttu-id="12024-255">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12024-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="12024-256">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12024-256">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="12024-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12024-257">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="12024-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12024-258">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="12024-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-259">Search-Flags</span></span>           | <span data-ttu-id="12024-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12024-260">0x00000000</span></span>   |
| <span data-ttu-id="12024-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-261">System-Flags</span></span>           | <span data-ttu-id="12024-262">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12024-262">0x08000014</span></span>   |
| <span data-ttu-id="12024-263">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12024-263">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="12024-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12024-264">Windows Server 2012</span></span>



| <span data-ttu-id="12024-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="12024-265">Entry</span></span> | <span data-ttu-id="12024-266">Value</span><span class="sxs-lookup"><span data-stu-id="12024-266">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="12024-267">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="12024-267">Link-Id</span></span>                | \-           |
| <span data-ttu-id="12024-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12024-268">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="12024-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="12024-269">System-Only</span></span>            | <span data-ttu-id="12024-270">False</span><span class="sxs-lookup"><span data-stu-id="12024-270">False</span></span>        |
| <span data-ttu-id="12024-271">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="12024-271">Is-Single-Valued</span></span>       | <span data-ttu-id="12024-272">True</span><span class="sxs-lookup"><span data-stu-id="12024-272">True</span></span>         |
| <span data-ttu-id="12024-273">Está indexado</span><span class="sxs-lookup"><span data-stu-id="12024-273">Is Indexed</span></span>             | <span data-ttu-id="12024-274">False</span><span class="sxs-lookup"><span data-stu-id="12024-274">False</span></span>        |
| <span data-ttu-id="12024-275">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="12024-275">In Global Catalog</span></span>      | <span data-ttu-id="12024-276">False</span><span class="sxs-lookup"><span data-stu-id="12024-276">False</span></span>        |
| <span data-ttu-id="12024-277">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="12024-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="12024-278">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="12024-278">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="12024-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12024-279">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="12024-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12024-280">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="12024-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-281">Search-Flags</span></span>           | <span data-ttu-id="12024-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12024-282">0x00000000</span></span>   |
| <span data-ttu-id="12024-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12024-283">System-Flags</span></span>           | <span data-ttu-id="12024-284">0x08000014</span><span class="sxs-lookup"><span data-stu-id="12024-284">0x08000014</span></span>   |
| <span data-ttu-id="12024-285">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="12024-285">Classes used in</span></span>        | \-           |



 

 





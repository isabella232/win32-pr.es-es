---
title: Atributo Sync-with-SID
description: Para el objeto grupo integrado SAM o la sincronización de la directiva local, es el grupo local al que corresponde un objeto.
ms.assetid: b983210d-1c54-4355-bc37-771e51016175
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Sync-with-SID
- syncWithSID esquema de AD de atributos
topic_type:
- apiref
api_name:
- Sync-With-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845a95b737a56a853fa7fb4e77d5612f1efc3c37
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151714"
---
# <a name="sync-with-sid-attribute"></a><span data-ttu-id="53482-105">Atributo Sync-with-SID</span><span class="sxs-lookup"><span data-stu-id="53482-105">Sync-With-SID attribute</span></span>

<span data-ttu-id="53482-106">Para el objeto grupo integrado SAM o la sincronización de la directiva local, es el grupo local al que corresponde un objeto.</span><span class="sxs-lookup"><span data-stu-id="53482-106">For the SAM builtin group object/ local policy synchronization, this is the local group to which an object corresponds.</span></span>



| <span data-ttu-id="53482-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="53482-107">Entry</span></span> | <span data-ttu-id="53482-108">Value</span><span class="sxs-lookup"><span data-stu-id="53482-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="53482-109">CN</span><span class="sxs-lookup"><span data-stu-id="53482-109">CN</span></span>                | <span data-ttu-id="53482-110">Sincronización con SID</span><span class="sxs-lookup"><span data-stu-id="53482-110">Sync-With-SID</span></span>                        |
| <span data-ttu-id="53482-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="53482-111">Ldap-Display-Name</span></span> | <span data-ttu-id="53482-112">syncWithSID</span><span class="sxs-lookup"><span data-stu-id="53482-112">syncWithSID</span></span>                          |
| <span data-ttu-id="53482-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="53482-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="53482-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="53482-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="53482-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="53482-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="53482-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53482-116">Attribute-Id</span></span>      | <span data-ttu-id="53482-117">1.2.840.113556.1.4.667</span><span class="sxs-lookup"><span data-stu-id="53482-117">1.2.840.113556.1.4.667</span></span>               |
| <span data-ttu-id="53482-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="53482-118">System-Id-Guid</span></span>    | <span data-ttu-id="53482-119">037651e5-441d-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="53482-119">037651e5-441d-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="53482-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53482-120">Syntax</span></span>            | [<span data-ttu-id="53482-121">**Cadena (SID)**</span><span class="sxs-lookup"><span data-stu-id="53482-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="53482-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="53482-122">Implementations</span></span>

-   [<span data-ttu-id="53482-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="53482-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="53482-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53482-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53482-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53482-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53482-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53482-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53482-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53482-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53482-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53482-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="53482-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53482-129">Windows 2000 Server</span></span>



| <span data-ttu-id="53482-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="53482-130">Entry</span></span> | <span data-ttu-id="53482-131">Value</span><span class="sxs-lookup"><span data-stu-id="53482-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="53482-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53482-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="53482-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53482-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="53482-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="53482-134">System-Only</span></span>            | <span data-ttu-id="53482-135">False</span><span class="sxs-lookup"><span data-stu-id="53482-135">False</span></span>        |
| <span data-ttu-id="53482-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53482-136">Is-Single-Valued</span></span>       | <span data-ttu-id="53482-137">True</span><span class="sxs-lookup"><span data-stu-id="53482-137">True</span></span>         |
| <span data-ttu-id="53482-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53482-138">Is Indexed</span></span>             | <span data-ttu-id="53482-139">False</span><span class="sxs-lookup"><span data-stu-id="53482-139">False</span></span>        |
| <span data-ttu-id="53482-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53482-140">In Global Catalog</span></span>      | <span data-ttu-id="53482-141">False</span><span class="sxs-lookup"><span data-stu-id="53482-141">False</span></span>        |
| <span data-ttu-id="53482-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53482-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="53482-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53482-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="53482-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53482-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="53482-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53482-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="53482-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-146">Search-Flags</span></span>           | <span data-ttu-id="53482-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53482-147">0x00000000</span></span>   |
| <span data-ttu-id="53482-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-148">System-Flags</span></span>           | <span data-ttu-id="53482-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53482-149">0x00000010</span></span>   |
| <span data-ttu-id="53482-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53482-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="53482-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53482-151">Windows Server 2003</span></span>



| <span data-ttu-id="53482-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="53482-152">Entry</span></span> | <span data-ttu-id="53482-153">Value</span><span class="sxs-lookup"><span data-stu-id="53482-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="53482-154">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53482-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="53482-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53482-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="53482-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="53482-156">System-Only</span></span>            | <span data-ttu-id="53482-157">False</span><span class="sxs-lookup"><span data-stu-id="53482-157">False</span></span>        |
| <span data-ttu-id="53482-158">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53482-158">Is-Single-Valued</span></span>       | <span data-ttu-id="53482-159">True</span><span class="sxs-lookup"><span data-stu-id="53482-159">True</span></span>         |
| <span data-ttu-id="53482-160">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53482-160">Is Indexed</span></span>             | <span data-ttu-id="53482-161">False</span><span class="sxs-lookup"><span data-stu-id="53482-161">False</span></span>        |
| <span data-ttu-id="53482-162">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53482-162">In Global Catalog</span></span>      | <span data-ttu-id="53482-163">False</span><span class="sxs-lookup"><span data-stu-id="53482-163">False</span></span>        |
| <span data-ttu-id="53482-164">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53482-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="53482-165">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53482-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="53482-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53482-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="53482-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53482-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="53482-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-168">Search-Flags</span></span>           | <span data-ttu-id="53482-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53482-169">0x00000000</span></span>   |
| <span data-ttu-id="53482-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-170">System-Flags</span></span>           | <span data-ttu-id="53482-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53482-171">0x00000010</span></span>   |
| <span data-ttu-id="53482-172">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53482-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53482-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53482-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53482-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="53482-174">Entry</span></span> | <span data-ttu-id="53482-175">Value</span><span class="sxs-lookup"><span data-stu-id="53482-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="53482-176">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53482-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="53482-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53482-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="53482-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="53482-178">System-Only</span></span>            | <span data-ttu-id="53482-179">False</span><span class="sxs-lookup"><span data-stu-id="53482-179">False</span></span>        |
| <span data-ttu-id="53482-180">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53482-180">Is-Single-Valued</span></span>       | <span data-ttu-id="53482-181">True</span><span class="sxs-lookup"><span data-stu-id="53482-181">True</span></span>         |
| <span data-ttu-id="53482-182">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53482-182">Is Indexed</span></span>             | <span data-ttu-id="53482-183">False</span><span class="sxs-lookup"><span data-stu-id="53482-183">False</span></span>        |
| <span data-ttu-id="53482-184">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53482-184">In Global Catalog</span></span>      | <span data-ttu-id="53482-185">False</span><span class="sxs-lookup"><span data-stu-id="53482-185">False</span></span>        |
| <span data-ttu-id="53482-186">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53482-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="53482-187">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53482-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="53482-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53482-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="53482-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53482-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="53482-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-190">Search-Flags</span></span>           | <span data-ttu-id="53482-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53482-191">0x00000000</span></span>   |
| <span data-ttu-id="53482-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-192">System-Flags</span></span>           | <span data-ttu-id="53482-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53482-193">0x00000010</span></span>   |
| <span data-ttu-id="53482-194">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53482-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="53482-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53482-195">Windows Server 2008</span></span>



| <span data-ttu-id="53482-196">Entrada</span><span class="sxs-lookup"><span data-stu-id="53482-196">Entry</span></span> | <span data-ttu-id="53482-197">Value</span><span class="sxs-lookup"><span data-stu-id="53482-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="53482-198">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53482-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="53482-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53482-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="53482-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="53482-200">System-Only</span></span>            | <span data-ttu-id="53482-201">False</span><span class="sxs-lookup"><span data-stu-id="53482-201">False</span></span>        |
| <span data-ttu-id="53482-202">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53482-202">Is-Single-Valued</span></span>       | <span data-ttu-id="53482-203">True</span><span class="sxs-lookup"><span data-stu-id="53482-203">True</span></span>         |
| <span data-ttu-id="53482-204">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53482-204">Is Indexed</span></span>             | <span data-ttu-id="53482-205">False</span><span class="sxs-lookup"><span data-stu-id="53482-205">False</span></span>        |
| <span data-ttu-id="53482-206">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53482-206">In Global Catalog</span></span>      | <span data-ttu-id="53482-207">False</span><span class="sxs-lookup"><span data-stu-id="53482-207">False</span></span>        |
| <span data-ttu-id="53482-208">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53482-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="53482-209">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53482-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="53482-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53482-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="53482-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53482-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="53482-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-212">Search-Flags</span></span>           | <span data-ttu-id="53482-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53482-213">0x00000000</span></span>   |
| <span data-ttu-id="53482-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-214">System-Flags</span></span>           | <span data-ttu-id="53482-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53482-215">0x00000010</span></span>   |
| <span data-ttu-id="53482-216">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53482-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53482-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53482-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53482-218">Entrada</span><span class="sxs-lookup"><span data-stu-id="53482-218">Entry</span></span> | <span data-ttu-id="53482-219">Value</span><span class="sxs-lookup"><span data-stu-id="53482-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="53482-220">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53482-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="53482-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53482-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="53482-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="53482-222">System-Only</span></span>            | <span data-ttu-id="53482-223">False</span><span class="sxs-lookup"><span data-stu-id="53482-223">False</span></span>        |
| <span data-ttu-id="53482-224">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53482-224">Is-Single-Valued</span></span>       | <span data-ttu-id="53482-225">True</span><span class="sxs-lookup"><span data-stu-id="53482-225">True</span></span>         |
| <span data-ttu-id="53482-226">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53482-226">Is Indexed</span></span>             | <span data-ttu-id="53482-227">False</span><span class="sxs-lookup"><span data-stu-id="53482-227">False</span></span>        |
| <span data-ttu-id="53482-228">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53482-228">In Global Catalog</span></span>      | <span data-ttu-id="53482-229">False</span><span class="sxs-lookup"><span data-stu-id="53482-229">False</span></span>        |
| <span data-ttu-id="53482-230">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53482-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="53482-231">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53482-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="53482-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53482-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="53482-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53482-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="53482-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-234">Search-Flags</span></span>           | <span data-ttu-id="53482-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53482-235">0x00000000</span></span>   |
| <span data-ttu-id="53482-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-236">System-Flags</span></span>           | <span data-ttu-id="53482-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53482-237">0x00000010</span></span>   |
| <span data-ttu-id="53482-238">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53482-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="53482-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53482-239">Windows Server 2012</span></span>



| <span data-ttu-id="53482-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="53482-240">Entry</span></span> | <span data-ttu-id="53482-241">Value</span><span class="sxs-lookup"><span data-stu-id="53482-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="53482-242">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="53482-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="53482-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53482-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="53482-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="53482-244">System-Only</span></span>            | <span data-ttu-id="53482-245">False</span><span class="sxs-lookup"><span data-stu-id="53482-245">False</span></span>        |
| <span data-ttu-id="53482-246">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="53482-246">Is-Single-Valued</span></span>       | <span data-ttu-id="53482-247">True</span><span class="sxs-lookup"><span data-stu-id="53482-247">True</span></span>         |
| <span data-ttu-id="53482-248">Está indexado</span><span class="sxs-lookup"><span data-stu-id="53482-248">Is Indexed</span></span>             | <span data-ttu-id="53482-249">False</span><span class="sxs-lookup"><span data-stu-id="53482-249">False</span></span>        |
| <span data-ttu-id="53482-250">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="53482-250">In Global Catalog</span></span>      | <span data-ttu-id="53482-251">False</span><span class="sxs-lookup"><span data-stu-id="53482-251">False</span></span>        |
| <span data-ttu-id="53482-252">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="53482-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="53482-253">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53482-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="53482-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53482-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="53482-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53482-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="53482-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-256">Search-Flags</span></span>           | <span data-ttu-id="53482-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="53482-257">0x00000000</span></span>   |
| <span data-ttu-id="53482-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53482-258">System-Flags</span></span>           | <span data-ttu-id="53482-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53482-259">0x00000010</span></span>   |
| <span data-ttu-id="53482-260">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="53482-260">Classes used in</span></span>        | \-           |



 

 





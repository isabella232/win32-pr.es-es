---
title: Atributo Link-ID
description: Un entero que indica que el atributo es un atributo vinculado. Un entero par es un vínculo hacia delante y un entero impar es un vínculo hacia atrás.
ms.assetid: 73851839-f70c-40c6-976c-0bf727083791
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de ID. de vínculo
- Esquema de AD de atributo linkID
topic_type:
- apiref
api_name:
- Link-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64ad1d26ce5510ac5643419ade46d0565df6487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536076"
---
# <a name="link-id-attribute"></a><span data-ttu-id="42b77-106">Atributo Link-ID</span><span class="sxs-lookup"><span data-stu-id="42b77-106">Link-ID attribute</span></span>

<span data-ttu-id="42b77-107">Un entero que indica que el atributo es un atributo vinculado.</span><span class="sxs-lookup"><span data-stu-id="42b77-107">An integer that indicates that the attribute is a linked attribute.</span></span> <span data-ttu-id="42b77-108">Un entero par es un vínculo hacia delante y un entero impar es un vínculo hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="42b77-108">An even integer is a forward link and an odd integer is a backward link.</span></span>



| <span data-ttu-id="42b77-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="42b77-109">Entry</span></span> | <span data-ttu-id="42b77-110">Value</span><span class="sxs-lookup"><span data-stu-id="42b77-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="42b77-111">CN</span><span class="sxs-lookup"><span data-stu-id="42b77-111">CN</span></span>                | <span data-ttu-id="42b77-112">IDENTIFICADOR de vínculo</span><span class="sxs-lookup"><span data-stu-id="42b77-112">Link-ID</span></span>                              |
| <span data-ttu-id="42b77-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="42b77-113">Ldap-Display-Name</span></span> | <span data-ttu-id="42b77-114">linkID</span><span class="sxs-lookup"><span data-stu-id="42b77-114">linkID</span></span>                               |
| <span data-ttu-id="42b77-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="42b77-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="42b77-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="42b77-116">Update Privilege</span></span>  | <span data-ttu-id="42b77-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="42b77-117">Schema administrator</span></span>                 |
| <span data-ttu-id="42b77-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="42b77-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="42b77-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42b77-119">Attribute-Id</span></span>      | <span data-ttu-id="42b77-120">1.2.840.113556.1.2.50</span><span class="sxs-lookup"><span data-stu-id="42b77-120">1.2.840.113556.1.2.50</span></span>                |
| <span data-ttu-id="42b77-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="42b77-121">System-Id-Guid</span></span>    | <span data-ttu-id="42b77-122">bf96799b-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="42b77-122">bf96799b-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="42b77-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42b77-123">Syntax</span></span>            | [<span data-ttu-id="42b77-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="42b77-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="42b77-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="42b77-125">Implementations</span></span>

-   [<span data-ttu-id="42b77-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="42b77-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="42b77-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42b77-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42b77-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="42b77-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="42b77-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42b77-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42b77-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42b77-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42b77-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42b77-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42b77-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42b77-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="42b77-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42b77-133">Windows 2000 Server</span></span>



| <span data-ttu-id="42b77-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="42b77-134">Entry</span></span> | <span data-ttu-id="42b77-135">Value</span><span class="sxs-lookup"><span data-stu-id="42b77-135">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="42b77-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="42b77-136">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="42b77-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42b77-137">MAPI-Id</span></span>                | <span data-ttu-id="42b77-138">0x80C5</span><span class="sxs-lookup"><span data-stu-id="42b77-138">0x80C5</span></span>                                                   |
| <span data-ttu-id="42b77-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="42b77-139">System-Only</span></span>            | <span data-ttu-id="42b77-140">True</span><span class="sxs-lookup"><span data-stu-id="42b77-140">True</span></span>                                                     |
| <span data-ttu-id="42b77-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="42b77-141">Is-Single-Valued</span></span>       | <span data-ttu-id="42b77-142">True</span><span class="sxs-lookup"><span data-stu-id="42b77-142">True</span></span>                                                     |
| <span data-ttu-id="42b77-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="42b77-143">Is Indexed</span></span>             | <span data-ttu-id="42b77-144">False</span><span class="sxs-lookup"><span data-stu-id="42b77-144">False</span></span>                                                    |
| <span data-ttu-id="42b77-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="42b77-145">In Global Catalog</span></span>      | <span data-ttu-id="42b77-146">False</span><span class="sxs-lookup"><span data-stu-id="42b77-146">False</span></span>                                                    |
| <span data-ttu-id="42b77-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="42b77-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="42b77-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42b77-148">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="42b77-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42b77-149">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42b77-150">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-151">Search-Flags</span></span>           | <span data-ttu-id="42b77-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42b77-152">0x00000000</span></span>                                               |
| <span data-ttu-id="42b77-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-153">System-Flags</span></span>           | <span data-ttu-id="42b77-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42b77-154">0x00000010</span></span>                                               |
| <span data-ttu-id="42b77-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="42b77-155">Classes used in</span></span>        | [<span data-ttu-id="42b77-156">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="42b77-156">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="42b77-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42b77-157">Windows Server 2003</span></span>



| <span data-ttu-id="42b77-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="42b77-158">Entry</span></span> | <span data-ttu-id="42b77-159">Value</span><span class="sxs-lookup"><span data-stu-id="42b77-159">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="42b77-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="42b77-160">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="42b77-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42b77-161">MAPI-Id</span></span>                | <span data-ttu-id="42b77-162">0x80C5</span><span class="sxs-lookup"><span data-stu-id="42b77-162">0x80C5</span></span>                                                   |
| <span data-ttu-id="42b77-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="42b77-163">System-Only</span></span>            | <span data-ttu-id="42b77-164">True</span><span class="sxs-lookup"><span data-stu-id="42b77-164">True</span></span>                                                     |
| <span data-ttu-id="42b77-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="42b77-165">Is-Single-Valued</span></span>       | <span data-ttu-id="42b77-166">True</span><span class="sxs-lookup"><span data-stu-id="42b77-166">True</span></span>                                                     |
| <span data-ttu-id="42b77-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="42b77-167">Is Indexed</span></span>             | <span data-ttu-id="42b77-168">False</span><span class="sxs-lookup"><span data-stu-id="42b77-168">False</span></span>                                                    |
| <span data-ttu-id="42b77-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="42b77-169">In Global Catalog</span></span>      | <span data-ttu-id="42b77-170">False</span><span class="sxs-lookup"><span data-stu-id="42b77-170">False</span></span>                                                    |
| <span data-ttu-id="42b77-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="42b77-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="42b77-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42b77-172">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="42b77-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42b77-173">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42b77-174">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-175">Search-Flags</span></span>           | <span data-ttu-id="42b77-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42b77-176">0x00000000</span></span>                                               |
| <span data-ttu-id="42b77-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-177">System-Flags</span></span>           | <span data-ttu-id="42b77-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42b77-178">0x00000010</span></span>                                               |
| <span data-ttu-id="42b77-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="42b77-179">Classes used in</span></span>        | [<span data-ttu-id="42b77-180">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="42b77-180">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="42b77-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="42b77-181">ADAM</span></span>



| <span data-ttu-id="42b77-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="42b77-182">Entry</span></span> | <span data-ttu-id="42b77-183">Value</span><span class="sxs-lookup"><span data-stu-id="42b77-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="42b77-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="42b77-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="42b77-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42b77-185">MAPI-Id</span></span>                | <span data-ttu-id="42b77-186">0x80C5</span><span class="sxs-lookup"><span data-stu-id="42b77-186">0x80C5</span></span>                                                   |
| <span data-ttu-id="42b77-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="42b77-187">System-Only</span></span>            | <span data-ttu-id="42b77-188">True</span><span class="sxs-lookup"><span data-stu-id="42b77-188">True</span></span>                                                     |
| <span data-ttu-id="42b77-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="42b77-189">Is-Single-Valued</span></span>       | <span data-ttu-id="42b77-190">True</span><span class="sxs-lookup"><span data-stu-id="42b77-190">True</span></span>                                                     |
| <span data-ttu-id="42b77-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="42b77-191">Is Indexed</span></span>             | <span data-ttu-id="42b77-192">False</span><span class="sxs-lookup"><span data-stu-id="42b77-192">False</span></span>                                                    |
| <span data-ttu-id="42b77-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="42b77-193">In Global Catalog</span></span>      | <span data-ttu-id="42b77-194">False</span><span class="sxs-lookup"><span data-stu-id="42b77-194">False</span></span>                                                    |
| <span data-ttu-id="42b77-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="42b77-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="42b77-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42b77-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="42b77-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42b77-197">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42b77-198">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-199">Search-Flags</span></span>           | <span data-ttu-id="42b77-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42b77-200">0x00000000</span></span>                                               |
| <span data-ttu-id="42b77-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-201">System-Flags</span></span>           | <span data-ttu-id="42b77-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42b77-202">0x00000010</span></span>                                               |
| <span data-ttu-id="42b77-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="42b77-203">Classes used in</span></span>        | [<span data-ttu-id="42b77-204">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="42b77-204">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42b77-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42b77-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42b77-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="42b77-206">Entry</span></span> | <span data-ttu-id="42b77-207">Value</span><span class="sxs-lookup"><span data-stu-id="42b77-207">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="42b77-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="42b77-208">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="42b77-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42b77-209">MAPI-Id</span></span>                | <span data-ttu-id="42b77-210">0x80C5</span><span class="sxs-lookup"><span data-stu-id="42b77-210">0x80C5</span></span>                                                   |
| <span data-ttu-id="42b77-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="42b77-211">System-Only</span></span>            | <span data-ttu-id="42b77-212">True</span><span class="sxs-lookup"><span data-stu-id="42b77-212">True</span></span>                                                     |
| <span data-ttu-id="42b77-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="42b77-213">Is-Single-Valued</span></span>       | <span data-ttu-id="42b77-214">True</span><span class="sxs-lookup"><span data-stu-id="42b77-214">True</span></span>                                                     |
| <span data-ttu-id="42b77-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="42b77-215">Is Indexed</span></span>             | <span data-ttu-id="42b77-216">False</span><span class="sxs-lookup"><span data-stu-id="42b77-216">False</span></span>                                                    |
| <span data-ttu-id="42b77-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="42b77-217">In Global Catalog</span></span>      | <span data-ttu-id="42b77-218">False</span><span class="sxs-lookup"><span data-stu-id="42b77-218">False</span></span>                                                    |
| <span data-ttu-id="42b77-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="42b77-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="42b77-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42b77-220">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="42b77-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42b77-221">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42b77-222">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-223">Search-Flags</span></span>           | <span data-ttu-id="42b77-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42b77-224">0x00000000</span></span>                                               |
| <span data-ttu-id="42b77-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-225">System-Flags</span></span>           | <span data-ttu-id="42b77-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42b77-226">0x00000010</span></span>                                               |
| <span data-ttu-id="42b77-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="42b77-227">Classes used in</span></span>        | [<span data-ttu-id="42b77-228">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="42b77-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42b77-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42b77-229">Windows Server 2008</span></span>



| <span data-ttu-id="42b77-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="42b77-230">Entry</span></span> | <span data-ttu-id="42b77-231">Value</span><span class="sxs-lookup"><span data-stu-id="42b77-231">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="42b77-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="42b77-232">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="42b77-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42b77-233">MAPI-Id</span></span>                | <span data-ttu-id="42b77-234">0x80C5</span><span class="sxs-lookup"><span data-stu-id="42b77-234">0x80C5</span></span>                                                   |
| <span data-ttu-id="42b77-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="42b77-235">System-Only</span></span>            | <span data-ttu-id="42b77-236">True</span><span class="sxs-lookup"><span data-stu-id="42b77-236">True</span></span>                                                     |
| <span data-ttu-id="42b77-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="42b77-237">Is-Single-Valued</span></span>       | <span data-ttu-id="42b77-238">True</span><span class="sxs-lookup"><span data-stu-id="42b77-238">True</span></span>                                                     |
| <span data-ttu-id="42b77-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="42b77-239">Is Indexed</span></span>             | <span data-ttu-id="42b77-240">False</span><span class="sxs-lookup"><span data-stu-id="42b77-240">False</span></span>                                                    |
| <span data-ttu-id="42b77-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="42b77-241">In Global Catalog</span></span>      | <span data-ttu-id="42b77-242">False</span><span class="sxs-lookup"><span data-stu-id="42b77-242">False</span></span>                                                    |
| <span data-ttu-id="42b77-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="42b77-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="42b77-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42b77-244">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="42b77-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42b77-245">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42b77-246">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-247">Search-Flags</span></span>           | <span data-ttu-id="42b77-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42b77-248">0x00000000</span></span>                                               |
| <span data-ttu-id="42b77-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-249">System-Flags</span></span>           | <span data-ttu-id="42b77-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42b77-250">0x00000010</span></span>                                               |
| <span data-ttu-id="42b77-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="42b77-251">Classes used in</span></span>        | [<span data-ttu-id="42b77-252">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="42b77-252">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42b77-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42b77-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42b77-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="42b77-254">Entry</span></span> | <span data-ttu-id="42b77-255">Value</span><span class="sxs-lookup"><span data-stu-id="42b77-255">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="42b77-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="42b77-256">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="42b77-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42b77-257">MAPI-Id</span></span>                | <span data-ttu-id="42b77-258">0x80C5</span><span class="sxs-lookup"><span data-stu-id="42b77-258">0x80C5</span></span>                                                   |
| <span data-ttu-id="42b77-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="42b77-259">System-Only</span></span>            | <span data-ttu-id="42b77-260">True</span><span class="sxs-lookup"><span data-stu-id="42b77-260">True</span></span>                                                     |
| <span data-ttu-id="42b77-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="42b77-261">Is-Single-Valued</span></span>       | <span data-ttu-id="42b77-262">True</span><span class="sxs-lookup"><span data-stu-id="42b77-262">True</span></span>                                                     |
| <span data-ttu-id="42b77-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="42b77-263">Is Indexed</span></span>             | <span data-ttu-id="42b77-264">False</span><span class="sxs-lookup"><span data-stu-id="42b77-264">False</span></span>                                                    |
| <span data-ttu-id="42b77-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="42b77-265">In Global Catalog</span></span>      | <span data-ttu-id="42b77-266">False</span><span class="sxs-lookup"><span data-stu-id="42b77-266">False</span></span>                                                    |
| <span data-ttu-id="42b77-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="42b77-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="42b77-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42b77-268">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="42b77-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42b77-269">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42b77-270">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-271">Search-Flags</span></span>           | <span data-ttu-id="42b77-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42b77-272">0x00000000</span></span>                                               |
| <span data-ttu-id="42b77-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-273">System-Flags</span></span>           | <span data-ttu-id="42b77-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42b77-274">0x00000010</span></span>                                               |
| <span data-ttu-id="42b77-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="42b77-275">Classes used in</span></span>        | [<span data-ttu-id="42b77-276">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="42b77-276">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42b77-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42b77-277">Windows Server 2012</span></span>



| <span data-ttu-id="42b77-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="42b77-278">Entry</span></span> | <span data-ttu-id="42b77-279">Value</span><span class="sxs-lookup"><span data-stu-id="42b77-279">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="42b77-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="42b77-280">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="42b77-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42b77-281">MAPI-Id</span></span>                | <span data-ttu-id="42b77-282">0x80C5</span><span class="sxs-lookup"><span data-stu-id="42b77-282">0x80C5</span></span>                                                   |
| <span data-ttu-id="42b77-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="42b77-283">System-Only</span></span>            | <span data-ttu-id="42b77-284">True</span><span class="sxs-lookup"><span data-stu-id="42b77-284">True</span></span>                                                     |
| <span data-ttu-id="42b77-285">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="42b77-285">Is-Single-Valued</span></span>       | <span data-ttu-id="42b77-286">True</span><span class="sxs-lookup"><span data-stu-id="42b77-286">True</span></span>                                                     |
| <span data-ttu-id="42b77-287">Está indexado</span><span class="sxs-lookup"><span data-stu-id="42b77-287">Is Indexed</span></span>             | <span data-ttu-id="42b77-288">False</span><span class="sxs-lookup"><span data-stu-id="42b77-288">False</span></span>                                                    |
| <span data-ttu-id="42b77-289">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="42b77-289">In Global Catalog</span></span>      | <span data-ttu-id="42b77-290">False</span><span class="sxs-lookup"><span data-stu-id="42b77-290">False</span></span>                                                    |
| <span data-ttu-id="42b77-291">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="42b77-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="42b77-292">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42b77-292">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="42b77-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42b77-293">Range-Lower</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42b77-294">Range-Upper</span></span>            | \-                                                       |
| <span data-ttu-id="42b77-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-295">Search-Flags</span></span>           | <span data-ttu-id="42b77-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42b77-296">0x00000000</span></span>                                               |
| <span data-ttu-id="42b77-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42b77-297">System-Flags</span></span>           | <span data-ttu-id="42b77-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42b77-298">0x00000010</span></span>                                               |
| <span data-ttu-id="42b77-299">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="42b77-299">Classes used in</span></span>        | [<span data-ttu-id="42b77-300">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="42b77-300">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> |



 

 






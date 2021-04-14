---
title: Object-Version atributo)
description: Se puede usar para almacenar un número de versión para el objeto.
ms.assetid: 1aa8520b-c640-4ea2-9230-f28154bf69b0
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Object-Version
- atributo objectVersion esquema de AD
topic_type:
- apiref
api_name:
- Object-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f038f6286db575f4141c2e306086bb9a8faac71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659012"
---
# <a name="object-version-attribute"></a><span data-ttu-id="9922d-105">Object-Version atributo)</span><span class="sxs-lookup"><span data-stu-id="9922d-105">Object-Version attribute</span></span>

<span data-ttu-id="9922d-106">Se puede usar para almacenar un número de versión para el objeto.</span><span class="sxs-lookup"><span data-stu-id="9922d-106">This can be used to store a version number for the object.</span></span>



| <span data-ttu-id="9922d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9922d-107">Entry</span></span> | <span data-ttu-id="9922d-108">Value</span><span class="sxs-lookup"><span data-stu-id="9922d-108">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="9922d-109">CN</span><span class="sxs-lookup"><span data-stu-id="9922d-109">CN</span></span>                | <span data-ttu-id="9922d-110">Object-Version</span><span class="sxs-lookup"><span data-stu-id="9922d-110">Object-Version</span></span>                                                 |
| <span data-ttu-id="9922d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="9922d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9922d-112">objectVersion</span><span class="sxs-lookup"><span data-stu-id="9922d-112">objectVersion</span></span>                                                  |
| <span data-ttu-id="9922d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9922d-113">Size</span></span>              | <span data-ttu-id="9922d-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="9922d-114">4 bytes</span></span>                                                        |
| <span data-ttu-id="9922d-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="9922d-115">Update Privilege</span></span>  | <span data-ttu-id="9922d-116">El diseñador del objeto establecería este valor.</span><span class="sxs-lookup"><span data-stu-id="9922d-116">The designer of the object would set this value.</span></span>               |
| <span data-ttu-id="9922d-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="9922d-117">Update Frequency</span></span>  | <span data-ttu-id="9922d-118">Este valor debe incrementarse cada vez que cambia el objeto.</span><span class="sxs-lookup"><span data-stu-id="9922d-118">This value should be incremented each time the object changes.</span></span> |
| <span data-ttu-id="9922d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9922d-119">Attribute-Id</span></span>      | <span data-ttu-id="9922d-120">1.2.840.113556.1.2.76</span><span class="sxs-lookup"><span data-stu-id="9922d-120">1.2.840.113556.1.2.76</span></span>                                          |
| <span data-ttu-id="9922d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9922d-121">System-Id-Guid</span></span>    | <span data-ttu-id="9922d-122">16775848-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9922d-122">16775848-47f3-11d1-a9c3-0000f80367c1</span></span>                           |
| <span data-ttu-id="9922d-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9922d-123">Syntax</span></span>            | [<span data-ttu-id="9922d-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="9922d-124">**Enumeration**</span></span>](s-enumeration.md)                           |



## <a name="implementations"></a><span data-ttu-id="9922d-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="9922d-125">Implementations</span></span>

-   [<span data-ttu-id="9922d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9922d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9922d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9922d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9922d-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9922d-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9922d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9922d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9922d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9922d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9922d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9922d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9922d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9922d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9922d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9922d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="9922d-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="9922d-134">Entry</span></span> | <span data-ttu-id="9922d-135">Value</span><span class="sxs-lookup"><span data-stu-id="9922d-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9922d-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9922d-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9922d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9922d-137">MAPI-Id</span></span>                | <span data-ttu-id="9922d-138">0x80F7</span><span class="sxs-lookup"><span data-stu-id="9922d-138">0x80F7</span></span>                          |
| <span data-ttu-id="9922d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="9922d-139">System-Only</span></span>            | <span data-ttu-id="9922d-140">False</span><span class="sxs-lookup"><span data-stu-id="9922d-140">False</span></span>                           |
| <span data-ttu-id="9922d-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9922d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="9922d-142">True</span><span class="sxs-lookup"><span data-stu-id="9922d-142">True</span></span>                            |
| <span data-ttu-id="9922d-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9922d-143">Is Indexed</span></span>             | <span data-ttu-id="9922d-144">False</span><span class="sxs-lookup"><span data-stu-id="9922d-144">False</span></span>                           |
| <span data-ttu-id="9922d-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9922d-145">In Global Catalog</span></span>      | <span data-ttu-id="9922d-146">False</span><span class="sxs-lookup"><span data-stu-id="9922d-146">False</span></span>                           |
| <span data-ttu-id="9922d-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9922d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="9922d-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9922d-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9922d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9922d-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9922d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9922d-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9922d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-151">Search-Flags</span></span>           | <span data-ttu-id="9922d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9922d-152">0x00000000</span></span>                      |
| <span data-ttu-id="9922d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-153">System-Flags</span></span>           | <span data-ttu-id="9922d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9922d-154">0x00000010</span></span>                      |
| <span data-ttu-id="9922d-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9922d-155">Classes used in</span></span>        | [<span data-ttu-id="9922d-156">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="9922d-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9922d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9922d-157">Windows Server 2003</span></span>



| <span data-ttu-id="9922d-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="9922d-158">Entry</span></span> | <span data-ttu-id="9922d-159">Value</span><span class="sxs-lookup"><span data-stu-id="9922d-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9922d-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9922d-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9922d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9922d-161">MAPI-Id</span></span>                | <span data-ttu-id="9922d-162">0x80F7</span><span class="sxs-lookup"><span data-stu-id="9922d-162">0x80F7</span></span>                          |
| <span data-ttu-id="9922d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="9922d-163">System-Only</span></span>            | <span data-ttu-id="9922d-164">False</span><span class="sxs-lookup"><span data-stu-id="9922d-164">False</span></span>                           |
| <span data-ttu-id="9922d-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9922d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="9922d-166">True</span><span class="sxs-lookup"><span data-stu-id="9922d-166">True</span></span>                            |
| <span data-ttu-id="9922d-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9922d-167">Is Indexed</span></span>             | <span data-ttu-id="9922d-168">False</span><span class="sxs-lookup"><span data-stu-id="9922d-168">False</span></span>                           |
| <span data-ttu-id="9922d-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9922d-169">In Global Catalog</span></span>      | <span data-ttu-id="9922d-170">False</span><span class="sxs-lookup"><span data-stu-id="9922d-170">False</span></span>                           |
| <span data-ttu-id="9922d-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9922d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="9922d-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9922d-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9922d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9922d-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9922d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9922d-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9922d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-175">Search-Flags</span></span>           | <span data-ttu-id="9922d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9922d-176">0x00000000</span></span>                      |
| <span data-ttu-id="9922d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-177">System-Flags</span></span>           | <span data-ttu-id="9922d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9922d-178">0x00000010</span></span>                      |
| <span data-ttu-id="9922d-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9922d-179">Classes used in</span></span>        | [<span data-ttu-id="9922d-180">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="9922d-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9922d-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="9922d-181">ADAM</span></span>



| <span data-ttu-id="9922d-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="9922d-182">Entry</span></span> | <span data-ttu-id="9922d-183">Value</span><span class="sxs-lookup"><span data-stu-id="9922d-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9922d-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9922d-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9922d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9922d-185">MAPI-Id</span></span>                | <span data-ttu-id="9922d-186">0x80F7</span><span class="sxs-lookup"><span data-stu-id="9922d-186">0x80F7</span></span>                          |
| <span data-ttu-id="9922d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="9922d-187">System-Only</span></span>            | <span data-ttu-id="9922d-188">False</span><span class="sxs-lookup"><span data-stu-id="9922d-188">False</span></span>                           |
| <span data-ttu-id="9922d-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9922d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="9922d-190">True</span><span class="sxs-lookup"><span data-stu-id="9922d-190">True</span></span>                            |
| <span data-ttu-id="9922d-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9922d-191">Is Indexed</span></span>             | <span data-ttu-id="9922d-192">False</span><span class="sxs-lookup"><span data-stu-id="9922d-192">False</span></span>                           |
| <span data-ttu-id="9922d-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9922d-193">In Global Catalog</span></span>      | <span data-ttu-id="9922d-194">False</span><span class="sxs-lookup"><span data-stu-id="9922d-194">False</span></span>                           |
| <span data-ttu-id="9922d-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9922d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="9922d-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9922d-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9922d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9922d-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9922d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9922d-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9922d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-199">Search-Flags</span></span>           | <span data-ttu-id="9922d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9922d-200">0x00000000</span></span>                      |
| <span data-ttu-id="9922d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-201">System-Flags</span></span>           | <span data-ttu-id="9922d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9922d-202">0x00000010</span></span>                      |
| <span data-ttu-id="9922d-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9922d-203">Classes used in</span></span>        | [<span data-ttu-id="9922d-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="9922d-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9922d-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9922d-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9922d-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="9922d-206">Entry</span></span> | <span data-ttu-id="9922d-207">Value</span><span class="sxs-lookup"><span data-stu-id="9922d-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9922d-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9922d-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9922d-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9922d-209">MAPI-Id</span></span>                | <span data-ttu-id="9922d-210">0x80F7</span><span class="sxs-lookup"><span data-stu-id="9922d-210">0x80F7</span></span>                          |
| <span data-ttu-id="9922d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="9922d-211">System-Only</span></span>            | <span data-ttu-id="9922d-212">False</span><span class="sxs-lookup"><span data-stu-id="9922d-212">False</span></span>                           |
| <span data-ttu-id="9922d-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9922d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="9922d-214">True</span><span class="sxs-lookup"><span data-stu-id="9922d-214">True</span></span>                            |
| <span data-ttu-id="9922d-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9922d-215">Is Indexed</span></span>             | <span data-ttu-id="9922d-216">False</span><span class="sxs-lookup"><span data-stu-id="9922d-216">False</span></span>                           |
| <span data-ttu-id="9922d-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9922d-217">In Global Catalog</span></span>      | <span data-ttu-id="9922d-218">False</span><span class="sxs-lookup"><span data-stu-id="9922d-218">False</span></span>                           |
| <span data-ttu-id="9922d-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9922d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="9922d-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9922d-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9922d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9922d-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9922d-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9922d-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9922d-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-223">Search-Flags</span></span>           | <span data-ttu-id="9922d-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9922d-224">0x00000000</span></span>                      |
| <span data-ttu-id="9922d-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-225">System-Flags</span></span>           | <span data-ttu-id="9922d-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9922d-226">0x00000010</span></span>                      |
| <span data-ttu-id="9922d-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9922d-227">Classes used in</span></span>        | [<span data-ttu-id="9922d-228">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="9922d-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9922d-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9922d-229">Windows Server 2008</span></span>



| <span data-ttu-id="9922d-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="9922d-230">Entry</span></span> | <span data-ttu-id="9922d-231">Value</span><span class="sxs-lookup"><span data-stu-id="9922d-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9922d-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9922d-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9922d-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9922d-233">MAPI-Id</span></span>                | <span data-ttu-id="9922d-234">0x80F7</span><span class="sxs-lookup"><span data-stu-id="9922d-234">0x80F7</span></span>                          |
| <span data-ttu-id="9922d-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="9922d-235">System-Only</span></span>            | <span data-ttu-id="9922d-236">False</span><span class="sxs-lookup"><span data-stu-id="9922d-236">False</span></span>                           |
| <span data-ttu-id="9922d-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9922d-237">Is-Single-Valued</span></span>       | <span data-ttu-id="9922d-238">True</span><span class="sxs-lookup"><span data-stu-id="9922d-238">True</span></span>                            |
| <span data-ttu-id="9922d-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9922d-239">Is Indexed</span></span>             | <span data-ttu-id="9922d-240">False</span><span class="sxs-lookup"><span data-stu-id="9922d-240">False</span></span>                           |
| <span data-ttu-id="9922d-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9922d-241">In Global Catalog</span></span>      | <span data-ttu-id="9922d-242">False</span><span class="sxs-lookup"><span data-stu-id="9922d-242">False</span></span>                           |
| <span data-ttu-id="9922d-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9922d-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="9922d-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9922d-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9922d-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9922d-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9922d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9922d-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9922d-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-247">Search-Flags</span></span>           | <span data-ttu-id="9922d-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9922d-248">0x00000000</span></span>                      |
| <span data-ttu-id="9922d-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-249">System-Flags</span></span>           | <span data-ttu-id="9922d-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9922d-250">0x00000010</span></span>                      |
| <span data-ttu-id="9922d-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9922d-251">Classes used in</span></span>        | [<span data-ttu-id="9922d-252">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="9922d-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9922d-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9922d-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9922d-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="9922d-254">Entry</span></span> | <span data-ttu-id="9922d-255">Value</span><span class="sxs-lookup"><span data-stu-id="9922d-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9922d-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9922d-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9922d-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9922d-257">MAPI-Id</span></span>                | <span data-ttu-id="9922d-258">0x80F7</span><span class="sxs-lookup"><span data-stu-id="9922d-258">0x80F7</span></span>                          |
| <span data-ttu-id="9922d-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="9922d-259">System-Only</span></span>            | <span data-ttu-id="9922d-260">False</span><span class="sxs-lookup"><span data-stu-id="9922d-260">False</span></span>                           |
| <span data-ttu-id="9922d-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9922d-261">Is-Single-Valued</span></span>       | <span data-ttu-id="9922d-262">True</span><span class="sxs-lookup"><span data-stu-id="9922d-262">True</span></span>                            |
| <span data-ttu-id="9922d-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9922d-263">Is Indexed</span></span>             | <span data-ttu-id="9922d-264">False</span><span class="sxs-lookup"><span data-stu-id="9922d-264">False</span></span>                           |
| <span data-ttu-id="9922d-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9922d-265">In Global Catalog</span></span>      | <span data-ttu-id="9922d-266">False</span><span class="sxs-lookup"><span data-stu-id="9922d-266">False</span></span>                           |
| <span data-ttu-id="9922d-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9922d-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="9922d-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9922d-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9922d-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9922d-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9922d-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9922d-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9922d-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-271">Search-Flags</span></span>           | <span data-ttu-id="9922d-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9922d-272">0x00000000</span></span>                      |
| <span data-ttu-id="9922d-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-273">System-Flags</span></span>           | <span data-ttu-id="9922d-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9922d-274">0x00000010</span></span>                      |
| <span data-ttu-id="9922d-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9922d-275">Classes used in</span></span>        | [<span data-ttu-id="9922d-276">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="9922d-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9922d-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9922d-277">Windows Server 2012</span></span>



| <span data-ttu-id="9922d-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="9922d-278">Entry</span></span> | <span data-ttu-id="9922d-279">Value</span><span class="sxs-lookup"><span data-stu-id="9922d-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9922d-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9922d-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9922d-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9922d-281">MAPI-Id</span></span>                | <span data-ttu-id="9922d-282">0x80F7</span><span class="sxs-lookup"><span data-stu-id="9922d-282">0x80F7</span></span>                          |
| <span data-ttu-id="9922d-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="9922d-283">System-Only</span></span>            | <span data-ttu-id="9922d-284">False</span><span class="sxs-lookup"><span data-stu-id="9922d-284">False</span></span>                           |
| <span data-ttu-id="9922d-285">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9922d-285">Is-Single-Valued</span></span>       | <span data-ttu-id="9922d-286">True</span><span class="sxs-lookup"><span data-stu-id="9922d-286">True</span></span>                            |
| <span data-ttu-id="9922d-287">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9922d-287">Is Indexed</span></span>             | <span data-ttu-id="9922d-288">False</span><span class="sxs-lookup"><span data-stu-id="9922d-288">False</span></span>                           |
| <span data-ttu-id="9922d-289">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9922d-289">In Global Catalog</span></span>      | <span data-ttu-id="9922d-290">False</span><span class="sxs-lookup"><span data-stu-id="9922d-290">False</span></span>                           |
| <span data-ttu-id="9922d-291">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9922d-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="9922d-292">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9922d-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9922d-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9922d-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9922d-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9922d-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9922d-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-295">Search-Flags</span></span>           | <span data-ttu-id="9922d-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9922d-296">0x00000000</span></span>                      |
| <span data-ttu-id="9922d-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9922d-297">System-Flags</span></span>           | <span data-ttu-id="9922d-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9922d-298">0x00000010</span></span>                      |
| <span data-ttu-id="9922d-299">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9922d-299">Classes used in</span></span>        | [<span data-ttu-id="9922d-300">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="9922d-300">**Top**</span></span>](c-top.md)<br/> |



 

 






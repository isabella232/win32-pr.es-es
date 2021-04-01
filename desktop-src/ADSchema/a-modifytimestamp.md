---
title: Atributo Modify-Time-Stamp
description: Atributo calculado que representa la fecha en que se cambió por última vez este objeto. Este valor no se replica.
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- 'Modificar: esquema de AD de atributos de marca de tiempo'
- modifyTimeStamp esquema de AD de atributos
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c032d19c3bd2bf5a6ee0cfe038e9fa9b184d36
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804405"
---
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="8a836-106">Atributo Modify-Time-Stamp</span><span class="sxs-lookup"><span data-stu-id="8a836-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="8a836-107">Atributo calculado que representa la fecha en que se cambió por última vez este objeto.</span><span class="sxs-lookup"><span data-stu-id="8a836-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="8a836-108">Este valor no se replica.</span><span class="sxs-lookup"><span data-stu-id="8a836-108">This value is not replicated.</span></span>



| <span data-ttu-id="8a836-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a836-109">Entry</span></span> | <span data-ttu-id="8a836-110">Value</span><span class="sxs-lookup"><span data-stu-id="8a836-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="8a836-111">CN</span><span class="sxs-lookup"><span data-stu-id="8a836-111">CN</span></span>                | <span data-ttu-id="8a836-112">Modificar: marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="8a836-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="8a836-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8a836-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8a836-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="8a836-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="8a836-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8a836-115">Size</span></span>              | <span data-ttu-id="8a836-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="8a836-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="8a836-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8a836-117">Update Privilege</span></span>  | <span data-ttu-id="8a836-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="8a836-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="8a836-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8a836-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="8a836-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8a836-120">Attribute-Id</span></span>      | <span data-ttu-id="8a836-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="8a836-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="8a836-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8a836-122">System-Id-Guid</span></span>    | <span data-ttu-id="8a836-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="8a836-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="8a836-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a836-124">Syntax</span></span>            | [<span data-ttu-id="8a836-125">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="8a836-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="8a836-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8a836-126">Implementations</span></span>

-   [<span data-ttu-id="8a836-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8a836-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8a836-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8a836-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8a836-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8a836-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8a836-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8a836-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8a836-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8a836-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8a836-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8a836-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8a836-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8a836-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8a836-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a836-134">Windows 2000 Server</span></span>



| <span data-ttu-id="8a836-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a836-135">Entry</span></span> | <span data-ttu-id="8a836-136">Value</span><span class="sxs-lookup"><span data-stu-id="8a836-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8a836-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8a836-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a836-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a836-139">System-Only</span></span>            | <span data-ttu-id="8a836-140">True</span><span class="sxs-lookup"><span data-stu-id="8a836-140">True</span></span>                                                                        |
| <span data-ttu-id="8a836-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8a836-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8a836-142">True</span><span class="sxs-lookup"><span data-stu-id="8a836-142">True</span></span>                                                                        |
| <span data-ttu-id="8a836-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8a836-143">Is Indexed</span></span>             | <span data-ttu-id="8a836-144">False</span><span class="sxs-lookup"><span data-stu-id="8a836-144">False</span></span>                                                                       |
| <span data-ttu-id="8a836-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a836-145">In Global Catalog</span></span>      | <span data-ttu-id="8a836-146">False</span><span class="sxs-lookup"><span data-stu-id="8a836-146">False</span></span>                                                                       |
| <span data-ttu-id="8a836-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8a836-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a836-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a836-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8a836-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a836-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a836-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-151">Search-Flags</span></span>           | <span data-ttu-id="8a836-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a836-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8a836-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-153">System-Flags</span></span>           | <span data-ttu-id="8a836-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a836-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8a836-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8a836-155">Classes used in</span></span>        | [<span data-ttu-id="8a836-156">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="8a836-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8a836-157">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8a836-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8a836-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a836-158">Windows Server 2003</span></span>



| <span data-ttu-id="8a836-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a836-159">Entry</span></span> | <span data-ttu-id="8a836-160">Value</span><span class="sxs-lookup"><span data-stu-id="8a836-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8a836-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8a836-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a836-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a836-163">System-Only</span></span>            | <span data-ttu-id="8a836-164">True</span><span class="sxs-lookup"><span data-stu-id="8a836-164">True</span></span>                                                                        |
| <span data-ttu-id="8a836-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8a836-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8a836-166">True</span><span class="sxs-lookup"><span data-stu-id="8a836-166">True</span></span>                                                                        |
| <span data-ttu-id="8a836-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8a836-167">Is Indexed</span></span>             | <span data-ttu-id="8a836-168">False</span><span class="sxs-lookup"><span data-stu-id="8a836-168">False</span></span>                                                                       |
| <span data-ttu-id="8a836-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a836-169">In Global Catalog</span></span>      | <span data-ttu-id="8a836-170">False</span><span class="sxs-lookup"><span data-stu-id="8a836-170">False</span></span>                                                                       |
| <span data-ttu-id="8a836-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8a836-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a836-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a836-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8a836-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a836-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a836-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-175">Search-Flags</span></span>           | <span data-ttu-id="8a836-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a836-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8a836-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-177">System-Flags</span></span>           | <span data-ttu-id="8a836-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a836-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8a836-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8a836-179">Classes used in</span></span>        | [<span data-ttu-id="8a836-180">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="8a836-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8a836-181">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8a836-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8a836-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="8a836-182">ADAM</span></span>



| <span data-ttu-id="8a836-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a836-183">Entry</span></span> | <span data-ttu-id="8a836-184">Value</span><span class="sxs-lookup"><span data-stu-id="8a836-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8a836-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8a836-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a836-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a836-187">System-Only</span></span>            | <span data-ttu-id="8a836-188">True</span><span class="sxs-lookup"><span data-stu-id="8a836-188">True</span></span>                                                                        |
| <span data-ttu-id="8a836-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8a836-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8a836-190">True</span><span class="sxs-lookup"><span data-stu-id="8a836-190">True</span></span>                                                                        |
| <span data-ttu-id="8a836-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8a836-191">Is Indexed</span></span>             | <span data-ttu-id="8a836-192">False</span><span class="sxs-lookup"><span data-stu-id="8a836-192">False</span></span>                                                                       |
| <span data-ttu-id="8a836-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a836-193">In Global Catalog</span></span>      | <span data-ttu-id="8a836-194">False</span><span class="sxs-lookup"><span data-stu-id="8a836-194">False</span></span>                                                                       |
| <span data-ttu-id="8a836-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8a836-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a836-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a836-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8a836-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a836-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a836-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-199">Search-Flags</span></span>           | <span data-ttu-id="8a836-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a836-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8a836-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-201">System-Flags</span></span>           | <span data-ttu-id="8a836-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a836-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8a836-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8a836-203">Classes used in</span></span>        | [<span data-ttu-id="8a836-204">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="8a836-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8a836-205">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8a836-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8a836-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8a836-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8a836-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a836-207">Entry</span></span> | <span data-ttu-id="8a836-208">Value</span><span class="sxs-lookup"><span data-stu-id="8a836-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8a836-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8a836-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a836-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a836-211">System-Only</span></span>            | <span data-ttu-id="8a836-212">True</span><span class="sxs-lookup"><span data-stu-id="8a836-212">True</span></span>                                                                        |
| <span data-ttu-id="8a836-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8a836-213">Is-Single-Valued</span></span>       | <span data-ttu-id="8a836-214">True</span><span class="sxs-lookup"><span data-stu-id="8a836-214">True</span></span>                                                                        |
| <span data-ttu-id="8a836-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8a836-215">Is Indexed</span></span>             | <span data-ttu-id="8a836-216">False</span><span class="sxs-lookup"><span data-stu-id="8a836-216">False</span></span>                                                                       |
| <span data-ttu-id="8a836-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a836-217">In Global Catalog</span></span>      | <span data-ttu-id="8a836-218">False</span><span class="sxs-lookup"><span data-stu-id="8a836-218">False</span></span>                                                                       |
| <span data-ttu-id="8a836-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8a836-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a836-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a836-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8a836-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a836-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a836-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-223">Search-Flags</span></span>           | <span data-ttu-id="8a836-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a836-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8a836-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-225">System-Flags</span></span>           | <span data-ttu-id="8a836-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a836-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8a836-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8a836-227">Classes used in</span></span>        | [<span data-ttu-id="8a836-228">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="8a836-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8a836-229">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8a836-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8a836-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a836-230">Windows Server 2008</span></span>



| <span data-ttu-id="8a836-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a836-231">Entry</span></span> | <span data-ttu-id="8a836-232">Value</span><span class="sxs-lookup"><span data-stu-id="8a836-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8a836-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8a836-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a836-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a836-235">System-Only</span></span>            | <span data-ttu-id="8a836-236">True</span><span class="sxs-lookup"><span data-stu-id="8a836-236">True</span></span>                                                                        |
| <span data-ttu-id="8a836-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8a836-237">Is-Single-Valued</span></span>       | <span data-ttu-id="8a836-238">True</span><span class="sxs-lookup"><span data-stu-id="8a836-238">True</span></span>                                                                        |
| <span data-ttu-id="8a836-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8a836-239">Is Indexed</span></span>             | <span data-ttu-id="8a836-240">False</span><span class="sxs-lookup"><span data-stu-id="8a836-240">False</span></span>                                                                       |
| <span data-ttu-id="8a836-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a836-241">In Global Catalog</span></span>      | <span data-ttu-id="8a836-242">False</span><span class="sxs-lookup"><span data-stu-id="8a836-242">False</span></span>                                                                       |
| <span data-ttu-id="8a836-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8a836-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a836-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a836-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8a836-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a836-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a836-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-247">Search-Flags</span></span>           | <span data-ttu-id="8a836-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a836-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8a836-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-249">System-Flags</span></span>           | <span data-ttu-id="8a836-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a836-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8a836-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8a836-251">Classes used in</span></span>        | [<span data-ttu-id="8a836-252">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="8a836-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8a836-253">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8a836-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8a836-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a836-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8a836-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a836-255">Entry</span></span> | <span data-ttu-id="8a836-256">Value</span><span class="sxs-lookup"><span data-stu-id="8a836-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8a836-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8a836-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a836-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a836-259">System-Only</span></span>            | <span data-ttu-id="8a836-260">True</span><span class="sxs-lookup"><span data-stu-id="8a836-260">True</span></span>                                                                        |
| <span data-ttu-id="8a836-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8a836-261">Is-Single-Valued</span></span>       | <span data-ttu-id="8a836-262">True</span><span class="sxs-lookup"><span data-stu-id="8a836-262">True</span></span>                                                                        |
| <span data-ttu-id="8a836-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8a836-263">Is Indexed</span></span>             | <span data-ttu-id="8a836-264">False</span><span class="sxs-lookup"><span data-stu-id="8a836-264">False</span></span>                                                                       |
| <span data-ttu-id="8a836-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a836-265">In Global Catalog</span></span>      | <span data-ttu-id="8a836-266">False</span><span class="sxs-lookup"><span data-stu-id="8a836-266">False</span></span>                                                                       |
| <span data-ttu-id="8a836-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8a836-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a836-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a836-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8a836-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a836-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a836-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-271">Search-Flags</span></span>           | <span data-ttu-id="8a836-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a836-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8a836-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-273">System-Flags</span></span>           | <span data-ttu-id="8a836-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a836-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8a836-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8a836-275">Classes used in</span></span>        | [<span data-ttu-id="8a836-276">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="8a836-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8a836-277">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8a836-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8a836-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a836-278">Windows Server 2012</span></span>



| <span data-ttu-id="8a836-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a836-279">Entry</span></span> | <span data-ttu-id="8a836-280">Value</span><span class="sxs-lookup"><span data-stu-id="8a836-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8a836-281">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8a836-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a836-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="8a836-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a836-283">System-Only</span></span>            | <span data-ttu-id="8a836-284">True</span><span class="sxs-lookup"><span data-stu-id="8a836-284">True</span></span>                                                                        |
| <span data-ttu-id="8a836-285">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8a836-285">Is-Single-Valued</span></span>       | <span data-ttu-id="8a836-286">True</span><span class="sxs-lookup"><span data-stu-id="8a836-286">True</span></span>                                                                        |
| <span data-ttu-id="8a836-287">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8a836-287">Is Indexed</span></span>             | <span data-ttu-id="8a836-288">False</span><span class="sxs-lookup"><span data-stu-id="8a836-288">False</span></span>                                                                       |
| <span data-ttu-id="8a836-289">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a836-289">In Global Catalog</span></span>      | <span data-ttu-id="8a836-290">False</span><span class="sxs-lookup"><span data-stu-id="8a836-290">False</span></span>                                                                       |
| <span data-ttu-id="8a836-291">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8a836-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a836-292">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a836-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="8a836-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a836-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a836-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="8a836-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-295">Search-Flags</span></span>           | <span data-ttu-id="8a836-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a836-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="8a836-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a836-297">System-Flags</span></span>           | <span data-ttu-id="8a836-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a836-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="8a836-299">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8a836-299">Classes used in</span></span>        | [<span data-ttu-id="8a836-300">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="8a836-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="8a836-301">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="8a836-301">**Top**</span></span>](c-top.md)<br/> |



 

 






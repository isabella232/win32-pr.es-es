---
title: Create-Time-Stamp (atributo)
description: Fecha en que se creó este objeto. Este valor se replica.
ms.assetid: 7b957a44-7185-49fa-a219-7c7f4b3e9fce
ms.tgt_platform: multiple
keywords:
- Create-Time-Stamp atributo AD Schema
- createTimeStamp esquema de AD de atributos
topic_type:
- apiref
api_name:
- Create-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66714aeb035667bc858b7a2e888f6334e7d09c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805101"
---
# <a name="create-time-stamp-attribute"></a><span data-ttu-id="6a209-106">Create-Time-Stamp (atributo)</span><span class="sxs-lookup"><span data-stu-id="6a209-106">Create-Time-Stamp attribute</span></span>

<span data-ttu-id="6a209-107">Fecha en que se creó este objeto.</span><span class="sxs-lookup"><span data-stu-id="6a209-107">The date when this object was created.</span></span> <span data-ttu-id="6a209-108">Este valor se replica.</span><span class="sxs-lookup"><span data-stu-id="6a209-108">This value is replicated.</span></span>



| <span data-ttu-id="6a209-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a209-109">Entry</span></span> | <span data-ttu-id="6a209-110">Value</span><span class="sxs-lookup"><span data-stu-id="6a209-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="6a209-111">CN</span><span class="sxs-lookup"><span data-stu-id="6a209-111">CN</span></span>                | <span data-ttu-id="6a209-112">Creación: marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="6a209-112">Create-Time-Stamp</span></span>                                             |
| <span data-ttu-id="6a209-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6a209-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6a209-114">createTimeStamp</span><span class="sxs-lookup"><span data-stu-id="6a209-114">createTimeStamp</span></span>                                               |
| <span data-ttu-id="6a209-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6a209-115">Size</span></span>              | <span data-ttu-id="6a209-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="6a209-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="6a209-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6a209-117">Update Privilege</span></span>  | <span data-ttu-id="6a209-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="6a209-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="6a209-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6a209-119">Update Frequency</span></span>  | <span data-ttu-id="6a209-120">Cuando se crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="6a209-120">When the object is created.</span></span>                                   |
| <span data-ttu-id="6a209-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a209-121">Attribute-Id</span></span>      | <span data-ttu-id="6a209-122">2.5.18.1</span><span class="sxs-lookup"><span data-stu-id="6a209-122">2.5.18.1</span></span>                                                      |
| <span data-ttu-id="6a209-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6a209-123">System-Id-Guid</span></span>    | <span data-ttu-id="6a209-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="6a209-124">2df90d73-009f-11d2-aa4c-00c04fd7d83a</span></span>                          |
| <span data-ttu-id="6a209-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a209-125">Syntax</span></span>            | [<span data-ttu-id="6a209-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="6a209-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="6a209-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6a209-127">Implementations</span></span>

-   [<span data-ttu-id="6a209-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6a209-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6a209-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a209-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a209-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6a209-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6a209-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a209-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a209-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a209-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a209-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a209-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a209-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a209-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6a209-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a209-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6a209-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a209-136">Entry</span></span> | <span data-ttu-id="6a209-137">Value</span><span class="sxs-lookup"><span data-stu-id="6a209-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6a209-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a209-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a209-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a209-140">System-Only</span></span>            | <span data-ttu-id="6a209-141">True</span><span class="sxs-lookup"><span data-stu-id="6a209-141">True</span></span>                            |
| <span data-ttu-id="6a209-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a209-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6a209-143">True</span><span class="sxs-lookup"><span data-stu-id="6a209-143">True</span></span>                            |
| <span data-ttu-id="6a209-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a209-144">Is Indexed</span></span>             | <span data-ttu-id="6a209-145">False</span><span class="sxs-lookup"><span data-stu-id="6a209-145">False</span></span>                           |
| <span data-ttu-id="6a209-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a209-146">In Global Catalog</span></span>      | <span data-ttu-id="6a209-147">False</span><span class="sxs-lookup"><span data-stu-id="6a209-147">False</span></span>                           |
| <span data-ttu-id="6a209-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a209-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a209-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a209-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6a209-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a209-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6a209-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a209-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6a209-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-152">Search-Flags</span></span>           | <span data-ttu-id="6a209-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a209-153">0x00000000</span></span>                      |
| <span data-ttu-id="6a209-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-154">System-Flags</span></span>           | <span data-ttu-id="6a209-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a209-155">0x08000014</span></span>                      |
| <span data-ttu-id="6a209-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a209-156">Classes used in</span></span>        | [<span data-ttu-id="6a209-157">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6a209-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6a209-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a209-158">Windows Server 2003</span></span>



| <span data-ttu-id="6a209-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a209-159">Entry</span></span> | <span data-ttu-id="6a209-160">Value</span><span class="sxs-lookup"><span data-stu-id="6a209-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6a209-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a209-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a209-162">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a209-163">System-Only</span></span>            | <span data-ttu-id="6a209-164">True</span><span class="sxs-lookup"><span data-stu-id="6a209-164">True</span></span>                            |
| <span data-ttu-id="6a209-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a209-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6a209-166">True</span><span class="sxs-lookup"><span data-stu-id="6a209-166">True</span></span>                            |
| <span data-ttu-id="6a209-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a209-167">Is Indexed</span></span>             | <span data-ttu-id="6a209-168">False</span><span class="sxs-lookup"><span data-stu-id="6a209-168">False</span></span>                           |
| <span data-ttu-id="6a209-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a209-169">In Global Catalog</span></span>      | <span data-ttu-id="6a209-170">False</span><span class="sxs-lookup"><span data-stu-id="6a209-170">False</span></span>                           |
| <span data-ttu-id="6a209-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a209-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a209-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a209-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6a209-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a209-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6a209-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a209-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6a209-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-175">Search-Flags</span></span>           | <span data-ttu-id="6a209-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a209-176">0x00000000</span></span>                      |
| <span data-ttu-id="6a209-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-177">System-Flags</span></span>           | <span data-ttu-id="6a209-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a209-178">0x08000014</span></span>                      |
| <span data-ttu-id="6a209-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a209-179">Classes used in</span></span>        | [<span data-ttu-id="6a209-180">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6a209-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6a209-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="6a209-181">ADAM</span></span>



| <span data-ttu-id="6a209-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a209-182">Entry</span></span> | <span data-ttu-id="6a209-183">Value</span><span class="sxs-lookup"><span data-stu-id="6a209-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6a209-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a209-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a209-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a209-186">System-Only</span></span>            | <span data-ttu-id="6a209-187">True</span><span class="sxs-lookup"><span data-stu-id="6a209-187">True</span></span>                            |
| <span data-ttu-id="6a209-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a209-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6a209-189">True</span><span class="sxs-lookup"><span data-stu-id="6a209-189">True</span></span>                            |
| <span data-ttu-id="6a209-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a209-190">Is Indexed</span></span>             | <span data-ttu-id="6a209-191">False</span><span class="sxs-lookup"><span data-stu-id="6a209-191">False</span></span>                           |
| <span data-ttu-id="6a209-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a209-192">In Global Catalog</span></span>      | <span data-ttu-id="6a209-193">False</span><span class="sxs-lookup"><span data-stu-id="6a209-193">False</span></span>                           |
| <span data-ttu-id="6a209-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a209-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a209-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a209-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6a209-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a209-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6a209-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a209-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6a209-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-198">Search-Flags</span></span>           | <span data-ttu-id="6a209-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a209-199">0x00000000</span></span>                      |
| <span data-ttu-id="6a209-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-200">System-Flags</span></span>           | <span data-ttu-id="6a209-201">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a209-201">0x08000014</span></span>                      |
| <span data-ttu-id="6a209-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a209-202">Classes used in</span></span>        | [<span data-ttu-id="6a209-203">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6a209-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a209-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a209-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a209-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a209-205">Entry</span></span> | <span data-ttu-id="6a209-206">Value</span><span class="sxs-lookup"><span data-stu-id="6a209-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6a209-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a209-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a209-208">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a209-209">System-Only</span></span>            | <span data-ttu-id="6a209-210">True</span><span class="sxs-lookup"><span data-stu-id="6a209-210">True</span></span>                            |
| <span data-ttu-id="6a209-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a209-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6a209-212">True</span><span class="sxs-lookup"><span data-stu-id="6a209-212">True</span></span>                            |
| <span data-ttu-id="6a209-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a209-213">Is Indexed</span></span>             | <span data-ttu-id="6a209-214">False</span><span class="sxs-lookup"><span data-stu-id="6a209-214">False</span></span>                           |
| <span data-ttu-id="6a209-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a209-215">In Global Catalog</span></span>      | <span data-ttu-id="6a209-216">False</span><span class="sxs-lookup"><span data-stu-id="6a209-216">False</span></span>                           |
| <span data-ttu-id="6a209-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a209-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a209-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a209-218">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6a209-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a209-219">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6a209-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a209-220">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6a209-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-221">Search-Flags</span></span>           | <span data-ttu-id="6a209-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a209-222">0x00000000</span></span>                      |
| <span data-ttu-id="6a209-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-223">System-Flags</span></span>           | <span data-ttu-id="6a209-224">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a209-224">0x08000014</span></span>                      |
| <span data-ttu-id="6a209-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a209-225">Classes used in</span></span>        | [<span data-ttu-id="6a209-226">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6a209-226">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6a209-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a209-227">Windows Server 2008</span></span>



| <span data-ttu-id="6a209-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a209-228">Entry</span></span> | <span data-ttu-id="6a209-229">Value</span><span class="sxs-lookup"><span data-stu-id="6a209-229">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6a209-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a209-230">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a209-231">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a209-232">System-Only</span></span>            | <span data-ttu-id="6a209-233">True</span><span class="sxs-lookup"><span data-stu-id="6a209-233">True</span></span>                            |
| <span data-ttu-id="6a209-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a209-234">Is-Single-Valued</span></span>       | <span data-ttu-id="6a209-235">True</span><span class="sxs-lookup"><span data-stu-id="6a209-235">True</span></span>                            |
| <span data-ttu-id="6a209-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a209-236">Is Indexed</span></span>             | <span data-ttu-id="6a209-237">False</span><span class="sxs-lookup"><span data-stu-id="6a209-237">False</span></span>                           |
| <span data-ttu-id="6a209-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a209-238">In Global Catalog</span></span>      | <span data-ttu-id="6a209-239">False</span><span class="sxs-lookup"><span data-stu-id="6a209-239">False</span></span>                           |
| <span data-ttu-id="6a209-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a209-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a209-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a209-241">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6a209-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a209-242">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6a209-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a209-243">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6a209-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-244">Search-Flags</span></span>           | <span data-ttu-id="6a209-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a209-245">0x00000000</span></span>                      |
| <span data-ttu-id="6a209-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-246">System-Flags</span></span>           | <span data-ttu-id="6a209-247">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a209-247">0x08000014</span></span>                      |
| <span data-ttu-id="6a209-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a209-248">Classes used in</span></span>        | [<span data-ttu-id="6a209-249">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6a209-249">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a209-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a209-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a209-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a209-251">Entry</span></span> | <span data-ttu-id="6a209-252">Value</span><span class="sxs-lookup"><span data-stu-id="6a209-252">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6a209-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a209-253">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a209-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a209-255">System-Only</span></span>            | <span data-ttu-id="6a209-256">True</span><span class="sxs-lookup"><span data-stu-id="6a209-256">True</span></span>                            |
| <span data-ttu-id="6a209-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a209-257">Is-Single-Valued</span></span>       | <span data-ttu-id="6a209-258">True</span><span class="sxs-lookup"><span data-stu-id="6a209-258">True</span></span>                            |
| <span data-ttu-id="6a209-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a209-259">Is Indexed</span></span>             | <span data-ttu-id="6a209-260">False</span><span class="sxs-lookup"><span data-stu-id="6a209-260">False</span></span>                           |
| <span data-ttu-id="6a209-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a209-261">In Global Catalog</span></span>      | <span data-ttu-id="6a209-262">False</span><span class="sxs-lookup"><span data-stu-id="6a209-262">False</span></span>                           |
| <span data-ttu-id="6a209-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a209-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a209-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a209-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6a209-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a209-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6a209-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a209-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6a209-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-267">Search-Flags</span></span>           | <span data-ttu-id="6a209-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a209-268">0x00000000</span></span>                      |
| <span data-ttu-id="6a209-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-269">System-Flags</span></span>           | <span data-ttu-id="6a209-270">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a209-270">0x08000014</span></span>                      |
| <span data-ttu-id="6a209-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a209-271">Classes used in</span></span>        | [<span data-ttu-id="6a209-272">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6a209-272">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6a209-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a209-273">Windows Server 2012</span></span>



| <span data-ttu-id="6a209-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a209-274">Entry</span></span> | <span data-ttu-id="6a209-275">Value</span><span class="sxs-lookup"><span data-stu-id="6a209-275">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6a209-276">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a209-276">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a209-277">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="6a209-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a209-278">System-Only</span></span>            | <span data-ttu-id="6a209-279">True</span><span class="sxs-lookup"><span data-stu-id="6a209-279">True</span></span>                            |
| <span data-ttu-id="6a209-280">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a209-280">Is-Single-Valued</span></span>       | <span data-ttu-id="6a209-281">True</span><span class="sxs-lookup"><span data-stu-id="6a209-281">True</span></span>                            |
| <span data-ttu-id="6a209-282">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a209-282">Is Indexed</span></span>             | <span data-ttu-id="6a209-283">False</span><span class="sxs-lookup"><span data-stu-id="6a209-283">False</span></span>                           |
| <span data-ttu-id="6a209-284">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a209-284">In Global Catalog</span></span>      | <span data-ttu-id="6a209-285">False</span><span class="sxs-lookup"><span data-stu-id="6a209-285">False</span></span>                           |
| <span data-ttu-id="6a209-286">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a209-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a209-287">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a209-287">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6a209-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a209-288">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6a209-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a209-289">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6a209-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-290">Search-Flags</span></span>           | <span data-ttu-id="6a209-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a209-291">0x00000000</span></span>                      |
| <span data-ttu-id="6a209-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a209-292">System-Flags</span></span>           | <span data-ttu-id="6a209-293">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a209-293">0x08000014</span></span>                      |
| <span data-ttu-id="6a209-294">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a209-294">Classes used in</span></span>        | [<span data-ttu-id="6a209-295">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6a209-295">**Top**</span></span>](c-top.md)<br/> |



 

 






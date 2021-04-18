---
title: RID-Allocation-Pool (atributo)
description: Un grupo que se capturó previamente para su uso por parte del administrador de RID cuando se ha usado el grupo RID-Previous-Allocation-Pool.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- RID-Allocation-Pool atributo AD Schema
- rIDAllocationPool esquema de AD de atributos
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a035cef460cc3081144d66391db78fb32c61108b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658753"
---
# <a name="rid-allocation-pool-attribute"></a><span data-ttu-id="1b13c-105">RID-Allocation-Pool (atributo)</span><span class="sxs-lookup"><span data-stu-id="1b13c-105">RID-Allocation-Pool attribute</span></span>

<span data-ttu-id="1b13c-106">Un grupo que se capturó previamente para su uso por parte del administrador de RID cuando se ha usado el grupo RID-Previous-Allocation-Pool.</span><span class="sxs-lookup"><span data-stu-id="1b13c-106">A pool that was prefetched for use by the RID manager when the RID-Previous-Allocation-Pool has been used up.</span></span>



| <span data-ttu-id="1b13c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b13c-107">Entry</span></span> | <span data-ttu-id="1b13c-108">Value</span><span class="sxs-lookup"><span data-stu-id="1b13c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1b13c-109">CN</span><span class="sxs-lookup"><span data-stu-id="1b13c-109">CN</span></span>                | <span data-ttu-id="1b13c-110">RID-asignación: Grupo</span><span class="sxs-lookup"><span data-stu-id="1b13c-110">RID-Allocation-Pool</span></span>                  |
| <span data-ttu-id="1b13c-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1b13c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1b13c-112">rIDAllocationPool</span><span class="sxs-lookup"><span data-stu-id="1b13c-112">rIDAllocationPool</span></span>                    |
| <span data-ttu-id="1b13c-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1b13c-113">Size</span></span>              | <span data-ttu-id="1b13c-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="1b13c-114">8 bytes</span></span>                              |
| <span data-ttu-id="1b13c-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1b13c-115">Update Privilege</span></span>  | <span data-ttu-id="1b13c-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="1b13c-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="1b13c-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1b13c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1b13c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1b13c-118">Attribute-Id</span></span>      | <span data-ttu-id="1b13c-119">1.2.840.113556.1.4.371</span><span class="sxs-lookup"><span data-stu-id="1b13c-119">1.2.840.113556.1.4.371</span></span>               |
| <span data-ttu-id="1b13c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1b13c-120">System-Id-Guid</span></span>    | <span data-ttu-id="1b13c-121">66171889-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="1b13c-121">66171889-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="1b13c-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b13c-122">Syntax</span></span>            | [<span data-ttu-id="1b13c-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="1b13c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="1b13c-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1b13c-124">Implementations</span></span>

-   [<span data-ttu-id="1b13c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1b13c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1b13c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1b13c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1b13c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1b13c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1b13c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1b13c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1b13c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b13c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1b13c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1b13c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1b13c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1b13c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1b13c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b13c-132">Entry</span></span> | <span data-ttu-id="1b13c-133">Value</span><span class="sxs-lookup"><span data-stu-id="1b13c-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1b13c-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1b13c-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b13c-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b13c-136">System-Only</span></span>            | <span data-ttu-id="1b13c-137">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-137">True</span></span>                                   |
| <span data-ttu-id="1b13c-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1b13c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1b13c-139">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-139">True</span></span>                                   |
| <span data-ttu-id="1b13c-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1b13c-140">Is Indexed</span></span>             | <span data-ttu-id="1b13c-141">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-141">False</span></span>                                  |
| <span data-ttu-id="1b13c-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b13c-142">In Global Catalog</span></span>      | <span data-ttu-id="1b13c-143">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-143">False</span></span>                                  |
| <span data-ttu-id="1b13c-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1b13c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b13c-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b13c-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1b13c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b13c-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b13c-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-148">Search-Flags</span></span>           | <span data-ttu-id="1b13c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b13c-149">0x00000000</span></span>                             |
| <span data-ttu-id="1b13c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-150">System-Flags</span></span>           | <span data-ttu-id="1b13c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b13c-151">0x00000010</span></span>                             |
| <span data-ttu-id="1b13c-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1b13c-152">Classes used in</span></span>        | [<span data-ttu-id="1b13c-153">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="1b13c-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1b13c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b13c-154">Windows Server 2003</span></span>



| <span data-ttu-id="1b13c-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b13c-155">Entry</span></span> | <span data-ttu-id="1b13c-156">Value</span><span class="sxs-lookup"><span data-stu-id="1b13c-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1b13c-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1b13c-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b13c-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b13c-159">System-Only</span></span>            | <span data-ttu-id="1b13c-160">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-160">True</span></span>                                   |
| <span data-ttu-id="1b13c-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1b13c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1b13c-162">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-162">True</span></span>                                   |
| <span data-ttu-id="1b13c-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1b13c-163">Is Indexed</span></span>             | <span data-ttu-id="1b13c-164">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-164">False</span></span>                                  |
| <span data-ttu-id="1b13c-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b13c-165">In Global Catalog</span></span>      | <span data-ttu-id="1b13c-166">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-166">False</span></span>                                  |
| <span data-ttu-id="1b13c-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1b13c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b13c-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b13c-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1b13c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b13c-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b13c-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-171">Search-Flags</span></span>           | <span data-ttu-id="1b13c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b13c-172">0x00000000</span></span>                             |
| <span data-ttu-id="1b13c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-173">System-Flags</span></span>           | <span data-ttu-id="1b13c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b13c-174">0x00000010</span></span>                             |
| <span data-ttu-id="1b13c-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1b13c-175">Classes used in</span></span>        | [<span data-ttu-id="1b13c-176">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="1b13c-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1b13c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1b13c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1b13c-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b13c-178">Entry</span></span> | <span data-ttu-id="1b13c-179">Value</span><span class="sxs-lookup"><span data-stu-id="1b13c-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1b13c-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1b13c-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b13c-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b13c-182">System-Only</span></span>            | <span data-ttu-id="1b13c-183">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-183">True</span></span>                                   |
| <span data-ttu-id="1b13c-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1b13c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1b13c-185">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-185">True</span></span>                                   |
| <span data-ttu-id="1b13c-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1b13c-186">Is Indexed</span></span>             | <span data-ttu-id="1b13c-187">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-187">False</span></span>                                  |
| <span data-ttu-id="1b13c-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b13c-188">In Global Catalog</span></span>      | <span data-ttu-id="1b13c-189">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-189">False</span></span>                                  |
| <span data-ttu-id="1b13c-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1b13c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b13c-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b13c-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1b13c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b13c-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b13c-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-194">Search-Flags</span></span>           | <span data-ttu-id="1b13c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b13c-195">0x00000000</span></span>                             |
| <span data-ttu-id="1b13c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-196">System-Flags</span></span>           | <span data-ttu-id="1b13c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b13c-197">0x00000010</span></span>                             |
| <span data-ttu-id="1b13c-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1b13c-198">Classes used in</span></span>        | [<span data-ttu-id="1b13c-199">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="1b13c-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1b13c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b13c-200">Windows Server 2008</span></span>



| <span data-ttu-id="1b13c-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b13c-201">Entry</span></span> | <span data-ttu-id="1b13c-202">Value</span><span class="sxs-lookup"><span data-stu-id="1b13c-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1b13c-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1b13c-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b13c-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b13c-205">System-Only</span></span>            | <span data-ttu-id="1b13c-206">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-206">True</span></span>                                   |
| <span data-ttu-id="1b13c-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1b13c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1b13c-208">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-208">True</span></span>                                   |
| <span data-ttu-id="1b13c-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1b13c-209">Is Indexed</span></span>             | <span data-ttu-id="1b13c-210">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-210">False</span></span>                                  |
| <span data-ttu-id="1b13c-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b13c-211">In Global Catalog</span></span>      | <span data-ttu-id="1b13c-212">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-212">False</span></span>                                  |
| <span data-ttu-id="1b13c-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1b13c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b13c-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b13c-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1b13c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b13c-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b13c-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-217">Search-Flags</span></span>           | <span data-ttu-id="1b13c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b13c-218">0x00000000</span></span>                             |
| <span data-ttu-id="1b13c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-219">System-Flags</span></span>           | <span data-ttu-id="1b13c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b13c-220">0x00000010</span></span>                             |
| <span data-ttu-id="1b13c-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1b13c-221">Classes used in</span></span>        | [<span data-ttu-id="1b13c-222">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="1b13c-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1b13c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b13c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1b13c-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b13c-224">Entry</span></span> | <span data-ttu-id="1b13c-225">Value</span><span class="sxs-lookup"><span data-stu-id="1b13c-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1b13c-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1b13c-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b13c-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b13c-228">System-Only</span></span>            | <span data-ttu-id="1b13c-229">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-229">True</span></span>                                   |
| <span data-ttu-id="1b13c-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1b13c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1b13c-231">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-231">True</span></span>                                   |
| <span data-ttu-id="1b13c-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1b13c-232">Is Indexed</span></span>             | <span data-ttu-id="1b13c-233">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-233">False</span></span>                                  |
| <span data-ttu-id="1b13c-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b13c-234">In Global Catalog</span></span>      | <span data-ttu-id="1b13c-235">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-235">False</span></span>                                  |
| <span data-ttu-id="1b13c-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1b13c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b13c-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b13c-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1b13c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b13c-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b13c-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-240">Search-Flags</span></span>           | <span data-ttu-id="1b13c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b13c-241">0x00000000</span></span>                             |
| <span data-ttu-id="1b13c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-242">System-Flags</span></span>           | <span data-ttu-id="1b13c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b13c-243">0x00000010</span></span>                             |
| <span data-ttu-id="1b13c-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1b13c-244">Classes used in</span></span>        | [<span data-ttu-id="1b13c-245">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="1b13c-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1b13c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b13c-246">Windows Server 2012</span></span>



| <span data-ttu-id="1b13c-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b13c-247">Entry</span></span> | <span data-ttu-id="1b13c-248">Value</span><span class="sxs-lookup"><span data-stu-id="1b13c-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="1b13c-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1b13c-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b13c-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="1b13c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b13c-251">System-Only</span></span>            | <span data-ttu-id="1b13c-252">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-252">True</span></span>                                   |
| <span data-ttu-id="1b13c-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1b13c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1b13c-254">True</span><span class="sxs-lookup"><span data-stu-id="1b13c-254">True</span></span>                                   |
| <span data-ttu-id="1b13c-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1b13c-255">Is Indexed</span></span>             | <span data-ttu-id="1b13c-256">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-256">False</span></span>                                  |
| <span data-ttu-id="1b13c-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b13c-257">In Global Catalog</span></span>      | <span data-ttu-id="1b13c-258">False</span><span class="sxs-lookup"><span data-stu-id="1b13c-258">False</span></span>                                  |
| <span data-ttu-id="1b13c-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1b13c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b13c-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1b13c-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="1b13c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b13c-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b13c-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="1b13c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-263">Search-Flags</span></span>           | <span data-ttu-id="1b13c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b13c-264">0x00000000</span></span>                             |
| <span data-ttu-id="1b13c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b13c-265">System-Flags</span></span>           | <span data-ttu-id="1b13c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b13c-266">0x00000010</span></span>                             |
| <span data-ttu-id="1b13c-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1b13c-267">Classes used in</span></span>        | [<span data-ttu-id="1b13c-268">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="1b13c-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 






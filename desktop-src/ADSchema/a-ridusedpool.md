---
title: Atributo RID-Used-Pool
description: Los grupos de RID utilizados por un controlador de dominio.
ms.assetid: ca779461-5b8f-4ab2-b9cf-5f829889f10d
ms.tgt_platform: multiple
keywords:
- RID-Used-Pool Attribute AD Schema
- rIDUsedPool esquema de AD de atributos
topic_type:
- apiref
api_name:
- RID-Used-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84547d99b162da9da6e634a7c35eb9700e84e2a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151583"
---
# <a name="rid-used-pool-attribute"></a><span data-ttu-id="91a23-105">Atributo RID-Used-Pool</span><span class="sxs-lookup"><span data-stu-id="91a23-105">RID-Used-Pool attribute</span></span>

<span data-ttu-id="91a23-106">Los grupos de RID utilizados por un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="91a23-106">The RID Pools that have been used by a DC.</span></span>



| <span data-ttu-id="91a23-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="91a23-107">Entry</span></span> | <span data-ttu-id="91a23-108">Value</span><span class="sxs-lookup"><span data-stu-id="91a23-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="91a23-109">CN</span><span class="sxs-lookup"><span data-stu-id="91a23-109">CN</span></span>                | <span data-ttu-id="91a23-110">RID: grupo usado</span><span class="sxs-lookup"><span data-stu-id="91a23-110">RID-Used-Pool</span></span>                        |
| <span data-ttu-id="91a23-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="91a23-111">Ldap-Display-Name</span></span> | <span data-ttu-id="91a23-112">rIDUsedPool</span><span class="sxs-lookup"><span data-stu-id="91a23-112">rIDUsedPool</span></span>                          |
| <span data-ttu-id="91a23-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="91a23-113">Size</span></span>              | <span data-ttu-id="91a23-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="91a23-114">8 bytes</span></span>                              |
| <span data-ttu-id="91a23-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="91a23-115">Update Privilege</span></span>  | <span data-ttu-id="91a23-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="91a23-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="91a23-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="91a23-117">Update Frequency</span></span>  | <span data-ttu-id="91a23-118">Cada vez que se vacía un grupo de RID.</span><span class="sxs-lookup"><span data-stu-id="91a23-118">Whenever a RID pool is emptied.</span></span>      |
| <span data-ttu-id="91a23-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="91a23-119">Attribute-Id</span></span>      | <span data-ttu-id="91a23-120">1.2.840.113556.1.4.373</span><span class="sxs-lookup"><span data-stu-id="91a23-120">1.2.840.113556.1.4.373</span></span>               |
| <span data-ttu-id="91a23-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="91a23-121">System-Id-Guid</span></span>    | <span data-ttu-id="91a23-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="91a23-122">6617188b-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="91a23-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91a23-123">Syntax</span></span>            | [<span data-ttu-id="91a23-124">**Interval**</span><span class="sxs-lookup"><span data-stu-id="91a23-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="91a23-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="91a23-125">Implementations</span></span>

-   [<span data-ttu-id="91a23-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="91a23-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="91a23-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="91a23-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="91a23-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="91a23-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="91a23-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="91a23-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="91a23-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="91a23-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="91a23-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="91a23-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="91a23-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="91a23-132">Windows 2000 Server</span></span>



| <span data-ttu-id="91a23-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="91a23-133">Entry</span></span> | <span data-ttu-id="91a23-134">Value</span><span class="sxs-lookup"><span data-stu-id="91a23-134">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="91a23-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="91a23-135">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91a23-136">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="91a23-137">System-Only</span></span>            | <span data-ttu-id="91a23-138">True</span><span class="sxs-lookup"><span data-stu-id="91a23-138">True</span></span>                                   |
| <span data-ttu-id="91a23-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="91a23-139">Is-Single-Valued</span></span>       | <span data-ttu-id="91a23-140">True</span><span class="sxs-lookup"><span data-stu-id="91a23-140">True</span></span>                                   |
| <span data-ttu-id="91a23-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="91a23-141">Is Indexed</span></span>             | <span data-ttu-id="91a23-142">False</span><span class="sxs-lookup"><span data-stu-id="91a23-142">False</span></span>                                  |
| <span data-ttu-id="91a23-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="91a23-143">In Global Catalog</span></span>      | <span data-ttu-id="91a23-144">False</span><span class="sxs-lookup"><span data-stu-id="91a23-144">False</span></span>                                  |
| <span data-ttu-id="91a23-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="91a23-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="91a23-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91a23-146">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="91a23-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91a23-147">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="91a23-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91a23-148">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="91a23-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-149">Search-Flags</span></span>           | <span data-ttu-id="91a23-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91a23-150">0x00000000</span></span>                             |
| <span data-ttu-id="91a23-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-151">System-Flags</span></span>           | <span data-ttu-id="91a23-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91a23-152">0x00000010</span></span>                             |
| <span data-ttu-id="91a23-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="91a23-153">Classes used in</span></span>        | [<span data-ttu-id="91a23-154">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="91a23-154">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="91a23-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91a23-155">Windows Server 2003</span></span>



| <span data-ttu-id="91a23-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="91a23-156">Entry</span></span> | <span data-ttu-id="91a23-157">Value</span><span class="sxs-lookup"><span data-stu-id="91a23-157">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="91a23-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="91a23-158">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91a23-159">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="91a23-160">System-Only</span></span>            | <span data-ttu-id="91a23-161">True</span><span class="sxs-lookup"><span data-stu-id="91a23-161">True</span></span>                                   |
| <span data-ttu-id="91a23-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="91a23-162">Is-Single-Valued</span></span>       | <span data-ttu-id="91a23-163">True</span><span class="sxs-lookup"><span data-stu-id="91a23-163">True</span></span>                                   |
| <span data-ttu-id="91a23-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="91a23-164">Is Indexed</span></span>             | <span data-ttu-id="91a23-165">False</span><span class="sxs-lookup"><span data-stu-id="91a23-165">False</span></span>                                  |
| <span data-ttu-id="91a23-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="91a23-166">In Global Catalog</span></span>      | <span data-ttu-id="91a23-167">False</span><span class="sxs-lookup"><span data-stu-id="91a23-167">False</span></span>                                  |
| <span data-ttu-id="91a23-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="91a23-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="91a23-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91a23-169">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="91a23-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91a23-170">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="91a23-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91a23-171">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="91a23-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-172">Search-Flags</span></span>           | <span data-ttu-id="91a23-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91a23-173">0x00000000</span></span>                             |
| <span data-ttu-id="91a23-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-174">System-Flags</span></span>           | <span data-ttu-id="91a23-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91a23-175">0x00000010</span></span>                             |
| <span data-ttu-id="91a23-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="91a23-176">Classes used in</span></span>        | [<span data-ttu-id="91a23-177">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="91a23-177">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="91a23-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="91a23-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="91a23-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="91a23-179">Entry</span></span> | <span data-ttu-id="91a23-180">Value</span><span class="sxs-lookup"><span data-stu-id="91a23-180">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="91a23-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="91a23-181">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91a23-182">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="91a23-183">System-Only</span></span>            | <span data-ttu-id="91a23-184">True</span><span class="sxs-lookup"><span data-stu-id="91a23-184">True</span></span>                                   |
| <span data-ttu-id="91a23-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="91a23-185">Is-Single-Valued</span></span>       | <span data-ttu-id="91a23-186">True</span><span class="sxs-lookup"><span data-stu-id="91a23-186">True</span></span>                                   |
| <span data-ttu-id="91a23-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="91a23-187">Is Indexed</span></span>             | <span data-ttu-id="91a23-188">False</span><span class="sxs-lookup"><span data-stu-id="91a23-188">False</span></span>                                  |
| <span data-ttu-id="91a23-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="91a23-189">In Global Catalog</span></span>      | <span data-ttu-id="91a23-190">False</span><span class="sxs-lookup"><span data-stu-id="91a23-190">False</span></span>                                  |
| <span data-ttu-id="91a23-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="91a23-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="91a23-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91a23-192">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="91a23-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91a23-193">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="91a23-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91a23-194">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="91a23-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-195">Search-Flags</span></span>           | <span data-ttu-id="91a23-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91a23-196">0x00000000</span></span>                             |
| <span data-ttu-id="91a23-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-197">System-Flags</span></span>           | <span data-ttu-id="91a23-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91a23-198">0x00000010</span></span>                             |
| <span data-ttu-id="91a23-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="91a23-199">Classes used in</span></span>        | [<span data-ttu-id="91a23-200">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="91a23-200">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="91a23-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91a23-201">Windows Server 2008</span></span>



| <span data-ttu-id="91a23-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="91a23-202">Entry</span></span> | <span data-ttu-id="91a23-203">Value</span><span class="sxs-lookup"><span data-stu-id="91a23-203">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="91a23-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="91a23-204">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91a23-205">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="91a23-206">System-Only</span></span>            | <span data-ttu-id="91a23-207">True</span><span class="sxs-lookup"><span data-stu-id="91a23-207">True</span></span>                                   |
| <span data-ttu-id="91a23-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="91a23-208">Is-Single-Valued</span></span>       | <span data-ttu-id="91a23-209">True</span><span class="sxs-lookup"><span data-stu-id="91a23-209">True</span></span>                                   |
| <span data-ttu-id="91a23-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="91a23-210">Is Indexed</span></span>             | <span data-ttu-id="91a23-211">False</span><span class="sxs-lookup"><span data-stu-id="91a23-211">False</span></span>                                  |
| <span data-ttu-id="91a23-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="91a23-212">In Global Catalog</span></span>      | <span data-ttu-id="91a23-213">False</span><span class="sxs-lookup"><span data-stu-id="91a23-213">False</span></span>                                  |
| <span data-ttu-id="91a23-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="91a23-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="91a23-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91a23-215">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="91a23-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91a23-216">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="91a23-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91a23-217">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="91a23-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-218">Search-Flags</span></span>           | <span data-ttu-id="91a23-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91a23-219">0x00000000</span></span>                             |
| <span data-ttu-id="91a23-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-220">System-Flags</span></span>           | <span data-ttu-id="91a23-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91a23-221">0x00000010</span></span>                             |
| <span data-ttu-id="91a23-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="91a23-222">Classes used in</span></span>        | [<span data-ttu-id="91a23-223">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="91a23-223">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="91a23-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="91a23-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="91a23-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="91a23-225">Entry</span></span> | <span data-ttu-id="91a23-226">Value</span><span class="sxs-lookup"><span data-stu-id="91a23-226">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="91a23-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="91a23-227">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91a23-228">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="91a23-229">System-Only</span></span>            | <span data-ttu-id="91a23-230">True</span><span class="sxs-lookup"><span data-stu-id="91a23-230">True</span></span>                                   |
| <span data-ttu-id="91a23-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="91a23-231">Is-Single-Valued</span></span>       | <span data-ttu-id="91a23-232">True</span><span class="sxs-lookup"><span data-stu-id="91a23-232">True</span></span>                                   |
| <span data-ttu-id="91a23-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="91a23-233">Is Indexed</span></span>             | <span data-ttu-id="91a23-234">False</span><span class="sxs-lookup"><span data-stu-id="91a23-234">False</span></span>                                  |
| <span data-ttu-id="91a23-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="91a23-235">In Global Catalog</span></span>      | <span data-ttu-id="91a23-236">False</span><span class="sxs-lookup"><span data-stu-id="91a23-236">False</span></span>                                  |
| <span data-ttu-id="91a23-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="91a23-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="91a23-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91a23-238">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="91a23-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91a23-239">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="91a23-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91a23-240">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="91a23-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-241">Search-Flags</span></span>           | <span data-ttu-id="91a23-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91a23-242">0x00000000</span></span>                             |
| <span data-ttu-id="91a23-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-243">System-Flags</span></span>           | <span data-ttu-id="91a23-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91a23-244">0x00000010</span></span>                             |
| <span data-ttu-id="91a23-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="91a23-245">Classes used in</span></span>        | [<span data-ttu-id="91a23-246">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="91a23-246">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="91a23-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91a23-247">Windows Server 2012</span></span>



| <span data-ttu-id="91a23-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="91a23-248">Entry</span></span> | <span data-ttu-id="91a23-249">Value</span><span class="sxs-lookup"><span data-stu-id="91a23-249">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="91a23-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="91a23-250">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="91a23-251">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="91a23-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="91a23-252">System-Only</span></span>            | <span data-ttu-id="91a23-253">True</span><span class="sxs-lookup"><span data-stu-id="91a23-253">True</span></span>                                   |
| <span data-ttu-id="91a23-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="91a23-254">Is-Single-Valued</span></span>       | <span data-ttu-id="91a23-255">True</span><span class="sxs-lookup"><span data-stu-id="91a23-255">True</span></span>                                   |
| <span data-ttu-id="91a23-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="91a23-256">Is Indexed</span></span>             | <span data-ttu-id="91a23-257">False</span><span class="sxs-lookup"><span data-stu-id="91a23-257">False</span></span>                                  |
| <span data-ttu-id="91a23-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="91a23-258">In Global Catalog</span></span>      | <span data-ttu-id="91a23-259">False</span><span class="sxs-lookup"><span data-stu-id="91a23-259">False</span></span>                                  |
| <span data-ttu-id="91a23-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="91a23-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="91a23-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="91a23-261">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="91a23-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="91a23-262">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="91a23-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="91a23-263">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="91a23-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-264">Search-Flags</span></span>           | <span data-ttu-id="91a23-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="91a23-265">0x00000000</span></span>                             |
| <span data-ttu-id="91a23-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="91a23-266">System-Flags</span></span>           | <span data-ttu-id="91a23-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="91a23-267">0x00000010</span></span>                             |
| <span data-ttu-id="91a23-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="91a23-268">Classes used in</span></span>        | [<span data-ttu-id="91a23-269">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="91a23-269">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 






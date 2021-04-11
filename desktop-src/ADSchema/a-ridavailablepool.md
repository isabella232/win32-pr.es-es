---
title: 'RID: atributo de Grupo disponible'
description: Espacio desde el que se asignan los grupos de RID.
ms.assetid: abb6218f-def2-4a38-964f-3f0ee6c6f917
ms.tgt_platform: multiple
keywords:
- RID-available-Pool atributo AD Schema
- rIDAvailablePool esquema de AD de atributos
topic_type:
- apiref
api_name:
- RID-Available-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59faf801b7f6f70e92c55a1d2a27857ed6ecb0c9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104274589"
---
# <a name="rid-available-pool-attribute"></a><span data-ttu-id="e5e2d-105">RID: atributo de Grupo disponible</span><span class="sxs-lookup"><span data-stu-id="e5e2d-105">RID-Available-Pool attribute</span></span>

<span data-ttu-id="e5e2d-106">Espacio desde el que se asignan los grupos de RID.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-106">The space from which RID Pools are allocated.</span></span>



| <span data-ttu-id="e5e2d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5e2d-107">Entry</span></span> | <span data-ttu-id="e5e2d-108">Value</span><span class="sxs-lookup"><span data-stu-id="e5e2d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e5e2d-109">CN</span><span class="sxs-lookup"><span data-stu-id="e5e2d-109">CN</span></span>                | <span data-ttu-id="e5e2d-110">RID: Grupo de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="e5e2d-110">RID-Available-Pool</span></span>                   |
| <span data-ttu-id="e5e2d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e5e2d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e5e2d-112">rIDAvailablePool</span><span class="sxs-lookup"><span data-stu-id="e5e2d-112">rIDAvailablePool</span></span>                     |
| <span data-ttu-id="e5e2d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e5e2d-113">Size</span></span>              | <span data-ttu-id="e5e2d-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="e5e2d-114">8 bytes</span></span>                              |
| <span data-ttu-id="e5e2d-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e5e2d-115">Update Privilege</span></span>  | <span data-ttu-id="e5e2d-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="e5e2d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="e5e2d-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e5e2d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e5e2d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e5e2d-118">Attribute-Id</span></span>      | <span data-ttu-id="e5e2d-119">1.2.840.113556.1.4.370</span><span class="sxs-lookup"><span data-stu-id="e5e2d-119">1.2.840.113556.1.4.370</span></span>               |
| <span data-ttu-id="e5e2d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e5e2d-120">System-Id-Guid</span></span>    | <span data-ttu-id="e5e2d-121">66171888-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="e5e2d-121">66171888-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="e5e2d-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5e2d-122">Syntax</span></span>            | [<span data-ttu-id="e5e2d-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e5e2d-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e5e2d-124">Implementations</span></span>

-   [<span data-ttu-id="e5e2d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e5e2d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e5e2d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e5e2d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e5e2d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e5e2d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e5e2d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5e2d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e5e2d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5e2d-132">Entry</span></span> | <span data-ttu-id="e5e2d-133">Value</span><span class="sxs-lookup"><span data-stu-id="e5e2d-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="e5e2d-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e5e2d-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e2d-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e2d-136">System-Only</span></span>            | <span data-ttu-id="e5e2d-137">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-137">False</span></span>                                          |
| <span data-ttu-id="e5e2d-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e5e2d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e2d-139">True</span><span class="sxs-lookup"><span data-stu-id="e5e2d-139">True</span></span>                                           |
| <span data-ttu-id="e5e2d-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e5e2d-140">Is Indexed</span></span>             | <span data-ttu-id="e5e2d-141">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-141">False</span></span>                                          |
| <span data-ttu-id="e5e2d-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5e2d-142">In Global Catalog</span></span>      | <span data-ttu-id="e5e2d-143">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-143">False</span></span>                                          |
| <span data-ttu-id="e5e2d-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e5e2d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e2d-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="e5e2d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e2d-146">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e2d-147">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-148">Search-Flags</span></span>           | <span data-ttu-id="e5e2d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e2d-149">0x00000000</span></span>                                     |
| <span data-ttu-id="e5e2d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-150">System-Flags</span></span>           | <span data-ttu-id="e5e2d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5e2d-151">0x00000010</span></span>                                     |
| <span data-ttu-id="e5e2d-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e5e2d-152">Classes used in</span></span>        | [<span data-ttu-id="e5e2d-153">**Administrador de RID**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-153">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e5e2d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5e2d-154">Windows Server 2003</span></span>



| <span data-ttu-id="e5e2d-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5e2d-155">Entry</span></span> | <span data-ttu-id="e5e2d-156">Value</span><span class="sxs-lookup"><span data-stu-id="e5e2d-156">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="e5e2d-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e5e2d-157">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e2d-158">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e2d-159">System-Only</span></span>            | <span data-ttu-id="e5e2d-160">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-160">False</span></span>                                          |
| <span data-ttu-id="e5e2d-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e5e2d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e2d-162">True</span><span class="sxs-lookup"><span data-stu-id="e5e2d-162">True</span></span>                                           |
| <span data-ttu-id="e5e2d-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e5e2d-163">Is Indexed</span></span>             | <span data-ttu-id="e5e2d-164">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-164">False</span></span>                                          |
| <span data-ttu-id="e5e2d-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5e2d-165">In Global Catalog</span></span>      | <span data-ttu-id="e5e2d-166">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-166">False</span></span>                                          |
| <span data-ttu-id="e5e2d-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e5e2d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e2d-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-168">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="e5e2d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e2d-169">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e2d-170">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-171">Search-Flags</span></span>           | <span data-ttu-id="e5e2d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e2d-172">0x00000000</span></span>                                     |
| <span data-ttu-id="e5e2d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-173">System-Flags</span></span>           | <span data-ttu-id="e5e2d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5e2d-174">0x00000010</span></span>                                     |
| <span data-ttu-id="e5e2d-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e5e2d-175">Classes used in</span></span>        | [<span data-ttu-id="e5e2d-176">**Administrador de RID**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-176">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e5e2d-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e5e2d-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e5e2d-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5e2d-178">Entry</span></span> | <span data-ttu-id="e5e2d-179">Value</span><span class="sxs-lookup"><span data-stu-id="e5e2d-179">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="e5e2d-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e5e2d-180">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e2d-181">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e2d-182">System-Only</span></span>            | <span data-ttu-id="e5e2d-183">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-183">False</span></span>                                          |
| <span data-ttu-id="e5e2d-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e5e2d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e2d-185">True</span><span class="sxs-lookup"><span data-stu-id="e5e2d-185">True</span></span>                                           |
| <span data-ttu-id="e5e2d-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e5e2d-186">Is Indexed</span></span>             | <span data-ttu-id="e5e2d-187">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-187">False</span></span>                                          |
| <span data-ttu-id="e5e2d-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5e2d-188">In Global Catalog</span></span>      | <span data-ttu-id="e5e2d-189">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-189">False</span></span>                                          |
| <span data-ttu-id="e5e2d-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e5e2d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e2d-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-191">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="e5e2d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e2d-192">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e2d-193">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-194">Search-Flags</span></span>           | <span data-ttu-id="e5e2d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e2d-195">0x00000000</span></span>                                     |
| <span data-ttu-id="e5e2d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-196">System-Flags</span></span>           | <span data-ttu-id="e5e2d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5e2d-197">0x00000010</span></span>                                     |
| <span data-ttu-id="e5e2d-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e5e2d-198">Classes used in</span></span>        | [<span data-ttu-id="e5e2d-199">**Administrador de RID**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-199">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e5e2d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5e2d-200">Windows Server 2008</span></span>



| <span data-ttu-id="e5e2d-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5e2d-201">Entry</span></span> | <span data-ttu-id="e5e2d-202">Value</span><span class="sxs-lookup"><span data-stu-id="e5e2d-202">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="e5e2d-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e5e2d-203">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e2d-204">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e2d-205">System-Only</span></span>            | <span data-ttu-id="e5e2d-206">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-206">False</span></span>                                          |
| <span data-ttu-id="e5e2d-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e5e2d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e2d-208">True</span><span class="sxs-lookup"><span data-stu-id="e5e2d-208">True</span></span>                                           |
| <span data-ttu-id="e5e2d-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e5e2d-209">Is Indexed</span></span>             | <span data-ttu-id="e5e2d-210">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-210">False</span></span>                                          |
| <span data-ttu-id="e5e2d-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5e2d-211">In Global Catalog</span></span>      | <span data-ttu-id="e5e2d-212">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-212">False</span></span>                                          |
| <span data-ttu-id="e5e2d-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e5e2d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e2d-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-214">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="e5e2d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e2d-215">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e2d-216">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-217">Search-Flags</span></span>           | <span data-ttu-id="e5e2d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e2d-218">0x00000000</span></span>                                     |
| <span data-ttu-id="e5e2d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-219">System-Flags</span></span>           | <span data-ttu-id="e5e2d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5e2d-220">0x00000010</span></span>                                     |
| <span data-ttu-id="e5e2d-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e5e2d-221">Classes used in</span></span>        | [<span data-ttu-id="e5e2d-222">**Administrador de RID**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-222">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e5e2d-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5e2d-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e5e2d-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5e2d-224">Entry</span></span> | <span data-ttu-id="e5e2d-225">Value</span><span class="sxs-lookup"><span data-stu-id="e5e2d-225">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="e5e2d-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e5e2d-226">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e2d-227">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e2d-228">System-Only</span></span>            | <span data-ttu-id="e5e2d-229">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-229">False</span></span>                                          |
| <span data-ttu-id="e5e2d-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e5e2d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e2d-231">True</span><span class="sxs-lookup"><span data-stu-id="e5e2d-231">True</span></span>                                           |
| <span data-ttu-id="e5e2d-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e5e2d-232">Is Indexed</span></span>             | <span data-ttu-id="e5e2d-233">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-233">False</span></span>                                          |
| <span data-ttu-id="e5e2d-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5e2d-234">In Global Catalog</span></span>      | <span data-ttu-id="e5e2d-235">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-235">False</span></span>                                          |
| <span data-ttu-id="e5e2d-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e5e2d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e2d-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-237">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="e5e2d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e2d-238">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e2d-239">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-240">Search-Flags</span></span>           | <span data-ttu-id="e5e2d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e2d-241">0x00000000</span></span>                                     |
| <span data-ttu-id="e5e2d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-242">System-Flags</span></span>           | <span data-ttu-id="e5e2d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5e2d-243">0x00000010</span></span>                                     |
| <span data-ttu-id="e5e2d-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e5e2d-244">Classes used in</span></span>        | [<span data-ttu-id="e5e2d-245">**Administrador de RID**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-245">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e5e2d-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5e2d-246">Windows Server 2012</span></span>



| <span data-ttu-id="e5e2d-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="e5e2d-247">Entry</span></span> | <span data-ttu-id="e5e2d-248">Value</span><span class="sxs-lookup"><span data-stu-id="e5e2d-248">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="e5e2d-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e5e2d-249">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5e2d-250">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="e5e2d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5e2d-251">System-Only</span></span>            | <span data-ttu-id="e5e2d-252">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-252">False</span></span>                                          |
| <span data-ttu-id="e5e2d-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e5e2d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e5e2d-254">True</span><span class="sxs-lookup"><span data-stu-id="e5e2d-254">True</span></span>                                           |
| <span data-ttu-id="e5e2d-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e5e2d-255">Is Indexed</span></span>             | <span data-ttu-id="e5e2d-256">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-256">False</span></span>                                          |
| <span data-ttu-id="e5e2d-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e5e2d-257">In Global Catalog</span></span>      | <span data-ttu-id="e5e2d-258">False</span><span class="sxs-lookup"><span data-stu-id="e5e2d-258">False</span></span>                                          |
| <span data-ttu-id="e5e2d-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e5e2d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5e2d-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5e2d-260">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="e5e2d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5e2d-261">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5e2d-262">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="e5e2d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-263">Search-Flags</span></span>           | <span data-ttu-id="e5e2d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e2d-264">0x00000000</span></span>                                     |
| <span data-ttu-id="e5e2d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5e2d-265">System-Flags</span></span>           | <span data-ttu-id="e5e2d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5e2d-266">0x00000010</span></span>                                     |
| <span data-ttu-id="e5e2d-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e5e2d-267">Classes used in</span></span>        | [<span data-ttu-id="e5e2d-268">**Administrador de RID**</span><span class="sxs-lookup"><span data-stu-id="e5e2d-268">**RID-Manager**</span></span>](c-ridmanager.md)<br/> |



 

 






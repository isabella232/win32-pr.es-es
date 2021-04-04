---
title: RID-Previous-Allocation-Pool (atributo)
description: Contiene el grupo de identificadores relativos (RID) del que un controlador de dominio asigna.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-Previous-Allocation-Pool atributo AD Schema
- rIDPreviousAllocationPool esquema de AD de atributos
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905927"
---
# <a name="rid-previous-allocation-pool-attribute"></a><span data-ttu-id="11452-105">RID-Previous-Allocation-Pool (atributo)</span><span class="sxs-lookup"><span data-stu-id="11452-105">RID-Previous-Allocation-Pool attribute</span></span>

<span data-ttu-id="11452-106">El atributo **RID-Previous-Allocation-Pool** contiene el grupo de identificadores relativos (RID) del que un controlador de dominio asigna.</span><span class="sxs-lookup"><span data-stu-id="11452-106">The **RID-Previous-Allocation-Pool** attribute contains the pool of relative identifiers (RIDs) that a domain controller allocates from.</span></span> <span data-ttu-id="11452-107">Este atributo es un valor de ocho bytes que contiene un par de enteros de cuatro bytes que representan los valores inicial y final del grupo RID.</span><span class="sxs-lookup"><span data-stu-id="11452-107">This attribute is an eight-byte value that contains a pair of four-byte integers that represent the start and end values of the RID pool.</span></span> <span data-ttu-id="11452-108">El valor de inicio está en los cuatro bytes inferiores y el valor final está en los cuatro bytes superiores.</span><span class="sxs-lookup"><span data-stu-id="11452-108">The start value is in the lower four bytes and the end value is in the upper four bytes.</span></span>



| <span data-ttu-id="11452-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="11452-109">Entry</span></span> | <span data-ttu-id="11452-110">Value</span><span class="sxs-lookup"><span data-stu-id="11452-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="11452-111">CN</span><span class="sxs-lookup"><span data-stu-id="11452-111">CN</span></span>                | <span data-ttu-id="11452-112">RID-anterior: Grupo de asignación</span><span class="sxs-lookup"><span data-stu-id="11452-112">RID-Previous-Allocation-Pool</span></span>         |
| <span data-ttu-id="11452-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="11452-113">Ldap-Display-Name</span></span> | <span data-ttu-id="11452-114">rIDPreviousAllocationPool</span><span class="sxs-lookup"><span data-stu-id="11452-114">rIDPreviousAllocationPool</span></span>            |
| <span data-ttu-id="11452-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="11452-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="11452-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="11452-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="11452-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="11452-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="11452-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="11452-118">Attribute-Id</span></span>      | <span data-ttu-id="11452-119">1.2.840.113556.1.4.372</span><span class="sxs-lookup"><span data-stu-id="11452-119">1.2.840.113556.1.4.372</span></span>               |
| <span data-ttu-id="11452-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="11452-120">System-Id-Guid</span></span>    | <span data-ttu-id="11452-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="11452-121">6617188a-8f3c-11d0-afda-00c04fd930c9</span></span> |
| <span data-ttu-id="11452-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11452-122">Syntax</span></span>            | [<span data-ttu-id="11452-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="11452-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="11452-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="11452-124">Implementations</span></span>

-   [<span data-ttu-id="11452-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="11452-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="11452-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="11452-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="11452-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="11452-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="11452-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="11452-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="11452-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="11452-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="11452-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="11452-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="11452-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11452-131">Windows 2000 Server</span></span>



| <span data-ttu-id="11452-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="11452-132">Entry</span></span> | <span data-ttu-id="11452-133">Value</span><span class="sxs-lookup"><span data-stu-id="11452-133">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="11452-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11452-134">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11452-135">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="11452-136">System-Only</span></span>            | <span data-ttu-id="11452-137">True</span><span class="sxs-lookup"><span data-stu-id="11452-137">True</span></span>                                   |
| <span data-ttu-id="11452-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11452-138">Is-Single-Valued</span></span>       | <span data-ttu-id="11452-139">True</span><span class="sxs-lookup"><span data-stu-id="11452-139">True</span></span>                                   |
| <span data-ttu-id="11452-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11452-140">Is Indexed</span></span>             | <span data-ttu-id="11452-141">False</span><span class="sxs-lookup"><span data-stu-id="11452-141">False</span></span>                                  |
| <span data-ttu-id="11452-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11452-142">In Global Catalog</span></span>      | <span data-ttu-id="11452-143">False</span><span class="sxs-lookup"><span data-stu-id="11452-143">False</span></span>                                  |
| <span data-ttu-id="11452-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11452-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="11452-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11452-145">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="11452-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11452-146">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="11452-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11452-147">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="11452-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-148">Search-Flags</span></span>           | <span data-ttu-id="11452-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11452-149">0x00000000</span></span>                             |
| <span data-ttu-id="11452-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-150">System-Flags</span></span>           | <span data-ttu-id="11452-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="11452-151">0x00000011</span></span>                             |
| <span data-ttu-id="11452-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11452-152">Classes used in</span></span>        | [<span data-ttu-id="11452-153">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="11452-153">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="11452-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11452-154">Windows Server 2003</span></span>



| <span data-ttu-id="11452-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="11452-155">Entry</span></span> | <span data-ttu-id="11452-156">Value</span><span class="sxs-lookup"><span data-stu-id="11452-156">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="11452-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11452-157">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11452-158">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="11452-159">System-Only</span></span>            | <span data-ttu-id="11452-160">True</span><span class="sxs-lookup"><span data-stu-id="11452-160">True</span></span>                                   |
| <span data-ttu-id="11452-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11452-161">Is-Single-Valued</span></span>       | <span data-ttu-id="11452-162">True</span><span class="sxs-lookup"><span data-stu-id="11452-162">True</span></span>                                   |
| <span data-ttu-id="11452-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11452-163">Is Indexed</span></span>             | <span data-ttu-id="11452-164">False</span><span class="sxs-lookup"><span data-stu-id="11452-164">False</span></span>                                  |
| <span data-ttu-id="11452-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11452-165">In Global Catalog</span></span>      | <span data-ttu-id="11452-166">False</span><span class="sxs-lookup"><span data-stu-id="11452-166">False</span></span>                                  |
| <span data-ttu-id="11452-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11452-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="11452-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11452-168">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="11452-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11452-169">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="11452-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11452-170">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="11452-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-171">Search-Flags</span></span>           | <span data-ttu-id="11452-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11452-172">0x00000000</span></span>                             |
| <span data-ttu-id="11452-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-173">System-Flags</span></span>           | <span data-ttu-id="11452-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="11452-174">0x00000011</span></span>                             |
| <span data-ttu-id="11452-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11452-175">Classes used in</span></span>        | [<span data-ttu-id="11452-176">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="11452-176">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="11452-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="11452-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="11452-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="11452-178">Entry</span></span> | <span data-ttu-id="11452-179">Value</span><span class="sxs-lookup"><span data-stu-id="11452-179">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="11452-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11452-180">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11452-181">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="11452-182">System-Only</span></span>            | <span data-ttu-id="11452-183">True</span><span class="sxs-lookup"><span data-stu-id="11452-183">True</span></span>                                   |
| <span data-ttu-id="11452-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11452-184">Is-Single-Valued</span></span>       | <span data-ttu-id="11452-185">True</span><span class="sxs-lookup"><span data-stu-id="11452-185">True</span></span>                                   |
| <span data-ttu-id="11452-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11452-186">Is Indexed</span></span>             | <span data-ttu-id="11452-187">False</span><span class="sxs-lookup"><span data-stu-id="11452-187">False</span></span>                                  |
| <span data-ttu-id="11452-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11452-188">In Global Catalog</span></span>      | <span data-ttu-id="11452-189">False</span><span class="sxs-lookup"><span data-stu-id="11452-189">False</span></span>                                  |
| <span data-ttu-id="11452-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11452-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="11452-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11452-191">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="11452-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11452-192">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="11452-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11452-193">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="11452-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-194">Search-Flags</span></span>           | <span data-ttu-id="11452-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11452-195">0x00000000</span></span>                             |
| <span data-ttu-id="11452-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-196">System-Flags</span></span>           | <span data-ttu-id="11452-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="11452-197">0x00000011</span></span>                             |
| <span data-ttu-id="11452-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11452-198">Classes used in</span></span>        | [<span data-ttu-id="11452-199">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="11452-199">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="11452-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11452-200">Windows Server 2008</span></span>



| <span data-ttu-id="11452-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="11452-201">Entry</span></span> | <span data-ttu-id="11452-202">Value</span><span class="sxs-lookup"><span data-stu-id="11452-202">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="11452-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11452-203">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11452-204">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="11452-205">System-Only</span></span>            | <span data-ttu-id="11452-206">True</span><span class="sxs-lookup"><span data-stu-id="11452-206">True</span></span>                                   |
| <span data-ttu-id="11452-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11452-207">Is-Single-Valued</span></span>       | <span data-ttu-id="11452-208">True</span><span class="sxs-lookup"><span data-stu-id="11452-208">True</span></span>                                   |
| <span data-ttu-id="11452-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11452-209">Is Indexed</span></span>             | <span data-ttu-id="11452-210">False</span><span class="sxs-lookup"><span data-stu-id="11452-210">False</span></span>                                  |
| <span data-ttu-id="11452-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11452-211">In Global Catalog</span></span>      | <span data-ttu-id="11452-212">False</span><span class="sxs-lookup"><span data-stu-id="11452-212">False</span></span>                                  |
| <span data-ttu-id="11452-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11452-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="11452-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11452-214">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="11452-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11452-215">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="11452-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11452-216">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="11452-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-217">Search-Flags</span></span>           | <span data-ttu-id="11452-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11452-218">0x00000000</span></span>                             |
| <span data-ttu-id="11452-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-219">System-Flags</span></span>           | <span data-ttu-id="11452-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="11452-220">0x00000011</span></span>                             |
| <span data-ttu-id="11452-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11452-221">Classes used in</span></span>        | [<span data-ttu-id="11452-222">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="11452-222">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="11452-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11452-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="11452-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="11452-224">Entry</span></span> | <span data-ttu-id="11452-225">Value</span><span class="sxs-lookup"><span data-stu-id="11452-225">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="11452-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11452-226">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11452-227">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="11452-228">System-Only</span></span>            | <span data-ttu-id="11452-229">True</span><span class="sxs-lookup"><span data-stu-id="11452-229">True</span></span>                                   |
| <span data-ttu-id="11452-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11452-230">Is-Single-Valued</span></span>       | <span data-ttu-id="11452-231">True</span><span class="sxs-lookup"><span data-stu-id="11452-231">True</span></span>                                   |
| <span data-ttu-id="11452-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11452-232">Is Indexed</span></span>             | <span data-ttu-id="11452-233">False</span><span class="sxs-lookup"><span data-stu-id="11452-233">False</span></span>                                  |
| <span data-ttu-id="11452-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11452-234">In Global Catalog</span></span>      | <span data-ttu-id="11452-235">False</span><span class="sxs-lookup"><span data-stu-id="11452-235">False</span></span>                                  |
| <span data-ttu-id="11452-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11452-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="11452-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11452-237">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="11452-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11452-238">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="11452-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11452-239">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="11452-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-240">Search-Flags</span></span>           | <span data-ttu-id="11452-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11452-241">0x00000000</span></span>                             |
| <span data-ttu-id="11452-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-242">System-Flags</span></span>           | <span data-ttu-id="11452-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="11452-243">0x00000011</span></span>                             |
| <span data-ttu-id="11452-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11452-244">Classes used in</span></span>        | [<span data-ttu-id="11452-245">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="11452-245">**RID-Set**</span></span>](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="11452-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11452-246">Windows Server 2012</span></span>



| <span data-ttu-id="11452-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="11452-247">Entry</span></span> | <span data-ttu-id="11452-248">Value</span><span class="sxs-lookup"><span data-stu-id="11452-248">Value</span></span> |
|------------------------|----------------------------------------|
| <span data-ttu-id="11452-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11452-249">Link-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11452-250">MAPI-Id</span></span>                | \-                                     |
| <span data-ttu-id="11452-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="11452-251">System-Only</span></span>            | <span data-ttu-id="11452-252">True</span><span class="sxs-lookup"><span data-stu-id="11452-252">True</span></span>                                   |
| <span data-ttu-id="11452-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11452-253">Is-Single-Valued</span></span>       | <span data-ttu-id="11452-254">True</span><span class="sxs-lookup"><span data-stu-id="11452-254">True</span></span>                                   |
| <span data-ttu-id="11452-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11452-255">Is Indexed</span></span>             | <span data-ttu-id="11452-256">False</span><span class="sxs-lookup"><span data-stu-id="11452-256">False</span></span>                                  |
| <span data-ttu-id="11452-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11452-257">In Global Catalog</span></span>      | <span data-ttu-id="11452-258">False</span><span class="sxs-lookup"><span data-stu-id="11452-258">False</span></span>                                  |
| <span data-ttu-id="11452-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11452-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="11452-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11452-260">O:BAG:BAD:S:</span></span>                           |
| <span data-ttu-id="11452-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11452-261">Range-Lower</span></span>            | \-                                     |
| <span data-ttu-id="11452-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11452-262">Range-Upper</span></span>            | \-                                     |
| <span data-ttu-id="11452-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-263">Search-Flags</span></span>           | <span data-ttu-id="11452-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11452-264">0x00000000</span></span>                             |
| <span data-ttu-id="11452-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11452-265">System-Flags</span></span>           | <span data-ttu-id="11452-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="11452-266">0x00000011</span></span>                             |
| <span data-ttu-id="11452-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11452-267">Classes used in</span></span>        | [<span data-ttu-id="11452-268">**RID: conjunto**</span><span class="sxs-lookup"><span data-stu-id="11452-268">**RID-Set**</span></span>](c-ridset.md)<br/> |



 

 






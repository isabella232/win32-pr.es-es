---
title: Atributo de conjunto de atributos parciales
description: Realiza un seguimiento del estado de replicación interna de réplicas parciales (es decir, en GC). Atributo del objeto NC de réplica parcial. Define el conjunto de atributos presentes en un NC de réplica parcial determinado.
ms.assetid: 2840d2b7-e186-4ef2-9107-f1e5c0c2f760
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de conjunto de atributos parciales
- partialAttributeSet esquema de AD de atributos
topic_type:
- apiref
api_name:
- Partial-Attribute-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932c07b0d4a8e3ea8f30f504194093d61912b7b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659003"
---
# <a name="partial-attribute-set-attribute"></a><span data-ttu-id="60184-107">Atributo de conjunto de atributos parciales</span><span class="sxs-lookup"><span data-stu-id="60184-107">Partial-Attribute-Set attribute</span></span>

<span data-ttu-id="60184-108">Realiza un seguimiento del estado de replicación interna de réplicas parciales (es decir, en GC).</span><span class="sxs-lookup"><span data-stu-id="60184-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="60184-109">Atributo del objeto NC de réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="60184-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="60184-110">Define el conjunto de atributos presentes en un NC de réplica parcial determinado.</span><span class="sxs-lookup"><span data-stu-id="60184-110">Defines the set of attributes present on a particular partial replica NC.</span></span>



| <span data-ttu-id="60184-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="60184-111">Entry</span></span> | <span data-ttu-id="60184-112">Value</span><span class="sxs-lookup"><span data-stu-id="60184-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="60184-113">CN</span><span class="sxs-lookup"><span data-stu-id="60184-113">CN</span></span>                | <span data-ttu-id="60184-114">Conjunto de atributos parciales</span><span class="sxs-lookup"><span data-stu-id="60184-114">Partial-Attribute-Set</span></span>                                 |
| <span data-ttu-id="60184-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="60184-115">Ldap-Display-Name</span></span> | <span data-ttu-id="60184-116">partialAttributeSet</span><span class="sxs-lookup"><span data-stu-id="60184-116">partialAttributeSet</span></span>                                   |
| <span data-ttu-id="60184-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="60184-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="60184-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="60184-118">Update Privilege</span></span>  | <span data-ttu-id="60184-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="60184-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="60184-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="60184-120">Update Frequency</span></span>  | <span data-ttu-id="60184-121">Durante la replicación</span><span class="sxs-lookup"><span data-stu-id="60184-121">During replication</span></span>                                    |
| <span data-ttu-id="60184-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="60184-122">Attribute-Id</span></span>      | <span data-ttu-id="60184-123">1.2.840.113556.1.4.640</span><span class="sxs-lookup"><span data-stu-id="60184-123">1.2.840.113556.1.4.640</span></span>                                |
| <span data-ttu-id="60184-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="60184-124">System-Id-Guid</span></span>    | <span data-ttu-id="60184-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="60184-125">19405b9e-3cfa-11d1-a9c0-0000f80367c1</span></span>                  |
| <span data-ttu-id="60184-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60184-126">Syntax</span></span>            | [<span data-ttu-id="60184-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="60184-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="60184-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="60184-128">Implementations</span></span>

-   [<span data-ttu-id="60184-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="60184-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="60184-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="60184-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="60184-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="60184-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="60184-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="60184-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="60184-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="60184-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="60184-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="60184-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="60184-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="60184-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="60184-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="60184-136">Windows 2000 Server</span></span>



| <span data-ttu-id="60184-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="60184-137">Entry</span></span> | <span data-ttu-id="60184-138">Value</span><span class="sxs-lookup"><span data-stu-id="60184-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60184-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60184-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60184-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="60184-141">System-Only</span></span>            | <span data-ttu-id="60184-142">True</span><span class="sxs-lookup"><span data-stu-id="60184-142">True</span></span>                            |
| <span data-ttu-id="60184-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60184-143">Is-Single-Valued</span></span>       | <span data-ttu-id="60184-144">True</span><span class="sxs-lookup"><span data-stu-id="60184-144">True</span></span>                            |
| <span data-ttu-id="60184-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60184-145">Is Indexed</span></span>             | <span data-ttu-id="60184-146">False</span><span class="sxs-lookup"><span data-stu-id="60184-146">False</span></span>                           |
| <span data-ttu-id="60184-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60184-147">In Global Catalog</span></span>      | <span data-ttu-id="60184-148">True</span><span class="sxs-lookup"><span data-stu-id="60184-148">True</span></span>                            |
| <span data-ttu-id="60184-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60184-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="60184-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60184-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60184-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60184-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60184-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60184-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60184-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-153">Search-Flags</span></span>           | <span data-ttu-id="60184-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60184-154">0x00000000</span></span>                      |
| <span data-ttu-id="60184-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-155">System-Flags</span></span>           | <span data-ttu-id="60184-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60184-156">0x00000013</span></span>                      |
| <span data-ttu-id="60184-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60184-157">Classes used in</span></span>        | [<span data-ttu-id="60184-158">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60184-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="60184-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60184-159">Windows Server 2003</span></span>



| <span data-ttu-id="60184-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="60184-160">Entry</span></span> | <span data-ttu-id="60184-161">Value</span><span class="sxs-lookup"><span data-stu-id="60184-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60184-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60184-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60184-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="60184-164">System-Only</span></span>            | <span data-ttu-id="60184-165">True</span><span class="sxs-lookup"><span data-stu-id="60184-165">True</span></span>                            |
| <span data-ttu-id="60184-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60184-166">Is-Single-Valued</span></span>       | <span data-ttu-id="60184-167">True</span><span class="sxs-lookup"><span data-stu-id="60184-167">True</span></span>                            |
| <span data-ttu-id="60184-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60184-168">Is Indexed</span></span>             | <span data-ttu-id="60184-169">False</span><span class="sxs-lookup"><span data-stu-id="60184-169">False</span></span>                           |
| <span data-ttu-id="60184-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60184-170">In Global Catalog</span></span>      | <span data-ttu-id="60184-171">True</span><span class="sxs-lookup"><span data-stu-id="60184-171">True</span></span>                            |
| <span data-ttu-id="60184-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60184-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="60184-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60184-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60184-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60184-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60184-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60184-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60184-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-176">Search-Flags</span></span>           | <span data-ttu-id="60184-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60184-177">0x00000000</span></span>                      |
| <span data-ttu-id="60184-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-178">System-Flags</span></span>           | <span data-ttu-id="60184-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60184-179">0x00000013</span></span>                      |
| <span data-ttu-id="60184-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60184-180">Classes used in</span></span>        | [<span data-ttu-id="60184-181">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60184-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="60184-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="60184-182">ADAM</span></span>



| <span data-ttu-id="60184-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="60184-183">Entry</span></span> | <span data-ttu-id="60184-184">Value</span><span class="sxs-lookup"><span data-stu-id="60184-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60184-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60184-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60184-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="60184-187">System-Only</span></span>            | <span data-ttu-id="60184-188">True</span><span class="sxs-lookup"><span data-stu-id="60184-188">True</span></span>                            |
| <span data-ttu-id="60184-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60184-189">Is-Single-Valued</span></span>       | <span data-ttu-id="60184-190">True</span><span class="sxs-lookup"><span data-stu-id="60184-190">True</span></span>                            |
| <span data-ttu-id="60184-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60184-191">Is Indexed</span></span>             | <span data-ttu-id="60184-192">False</span><span class="sxs-lookup"><span data-stu-id="60184-192">False</span></span>                           |
| <span data-ttu-id="60184-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60184-193">In Global Catalog</span></span>      | <span data-ttu-id="60184-194">True</span><span class="sxs-lookup"><span data-stu-id="60184-194">True</span></span>                            |
| <span data-ttu-id="60184-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60184-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="60184-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60184-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60184-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60184-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60184-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60184-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60184-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-199">Search-Flags</span></span>           | <span data-ttu-id="60184-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60184-200">0x00000000</span></span>                      |
| <span data-ttu-id="60184-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-201">System-Flags</span></span>           | <span data-ttu-id="60184-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60184-202">0x00000013</span></span>                      |
| <span data-ttu-id="60184-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60184-203">Classes used in</span></span>        | [<span data-ttu-id="60184-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60184-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="60184-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="60184-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="60184-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="60184-206">Entry</span></span> | <span data-ttu-id="60184-207">Value</span><span class="sxs-lookup"><span data-stu-id="60184-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60184-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60184-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60184-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="60184-210">System-Only</span></span>            | <span data-ttu-id="60184-211">True</span><span class="sxs-lookup"><span data-stu-id="60184-211">True</span></span>                            |
| <span data-ttu-id="60184-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60184-212">Is-Single-Valued</span></span>       | <span data-ttu-id="60184-213">True</span><span class="sxs-lookup"><span data-stu-id="60184-213">True</span></span>                            |
| <span data-ttu-id="60184-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60184-214">Is Indexed</span></span>             | <span data-ttu-id="60184-215">False</span><span class="sxs-lookup"><span data-stu-id="60184-215">False</span></span>                           |
| <span data-ttu-id="60184-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60184-216">In Global Catalog</span></span>      | <span data-ttu-id="60184-217">True</span><span class="sxs-lookup"><span data-stu-id="60184-217">True</span></span>                            |
| <span data-ttu-id="60184-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60184-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="60184-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60184-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60184-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60184-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60184-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60184-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60184-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-222">Search-Flags</span></span>           | <span data-ttu-id="60184-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60184-223">0x00000000</span></span>                      |
| <span data-ttu-id="60184-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-224">System-Flags</span></span>           | <span data-ttu-id="60184-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60184-225">0x00000013</span></span>                      |
| <span data-ttu-id="60184-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60184-226">Classes used in</span></span>        | [<span data-ttu-id="60184-227">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60184-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="60184-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60184-228">Windows Server 2008</span></span>



| <span data-ttu-id="60184-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="60184-229">Entry</span></span> | <span data-ttu-id="60184-230">Value</span><span class="sxs-lookup"><span data-stu-id="60184-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60184-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60184-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60184-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="60184-233">System-Only</span></span>            | <span data-ttu-id="60184-234">True</span><span class="sxs-lookup"><span data-stu-id="60184-234">True</span></span>                            |
| <span data-ttu-id="60184-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60184-235">Is-Single-Valued</span></span>       | <span data-ttu-id="60184-236">True</span><span class="sxs-lookup"><span data-stu-id="60184-236">True</span></span>                            |
| <span data-ttu-id="60184-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60184-237">Is Indexed</span></span>             | <span data-ttu-id="60184-238">False</span><span class="sxs-lookup"><span data-stu-id="60184-238">False</span></span>                           |
| <span data-ttu-id="60184-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60184-239">In Global Catalog</span></span>      | <span data-ttu-id="60184-240">True</span><span class="sxs-lookup"><span data-stu-id="60184-240">True</span></span>                            |
| <span data-ttu-id="60184-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60184-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="60184-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60184-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60184-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60184-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60184-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60184-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60184-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-245">Search-Flags</span></span>           | <span data-ttu-id="60184-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60184-246">0x00000000</span></span>                      |
| <span data-ttu-id="60184-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-247">System-Flags</span></span>           | <span data-ttu-id="60184-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60184-248">0x00000013</span></span>                      |
| <span data-ttu-id="60184-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60184-249">Classes used in</span></span>        | [<span data-ttu-id="60184-250">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60184-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="60184-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60184-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="60184-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="60184-252">Entry</span></span> | <span data-ttu-id="60184-253">Value</span><span class="sxs-lookup"><span data-stu-id="60184-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60184-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60184-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60184-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="60184-256">System-Only</span></span>            | <span data-ttu-id="60184-257">True</span><span class="sxs-lookup"><span data-stu-id="60184-257">True</span></span>                            |
| <span data-ttu-id="60184-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60184-258">Is-Single-Valued</span></span>       | <span data-ttu-id="60184-259">True</span><span class="sxs-lookup"><span data-stu-id="60184-259">True</span></span>                            |
| <span data-ttu-id="60184-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60184-260">Is Indexed</span></span>             | <span data-ttu-id="60184-261">False</span><span class="sxs-lookup"><span data-stu-id="60184-261">False</span></span>                           |
| <span data-ttu-id="60184-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60184-262">In Global Catalog</span></span>      | <span data-ttu-id="60184-263">True</span><span class="sxs-lookup"><span data-stu-id="60184-263">True</span></span>                            |
| <span data-ttu-id="60184-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60184-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="60184-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60184-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60184-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60184-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60184-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60184-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60184-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-268">Search-Flags</span></span>           | <span data-ttu-id="60184-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60184-269">0x00000000</span></span>                      |
| <span data-ttu-id="60184-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-270">System-Flags</span></span>           | <span data-ttu-id="60184-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60184-271">0x00000013</span></span>                      |
| <span data-ttu-id="60184-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60184-272">Classes used in</span></span>        | [<span data-ttu-id="60184-273">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60184-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="60184-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60184-274">Windows Server 2012</span></span>



| <span data-ttu-id="60184-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="60184-275">Entry</span></span> | <span data-ttu-id="60184-276">Value</span><span class="sxs-lookup"><span data-stu-id="60184-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60184-277">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60184-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60184-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="60184-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="60184-279">System-Only</span></span>            | <span data-ttu-id="60184-280">True</span><span class="sxs-lookup"><span data-stu-id="60184-280">True</span></span>                            |
| <span data-ttu-id="60184-281">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60184-281">Is-Single-Valued</span></span>       | <span data-ttu-id="60184-282">True</span><span class="sxs-lookup"><span data-stu-id="60184-282">True</span></span>                            |
| <span data-ttu-id="60184-283">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60184-283">Is Indexed</span></span>             | <span data-ttu-id="60184-284">False</span><span class="sxs-lookup"><span data-stu-id="60184-284">False</span></span>                           |
| <span data-ttu-id="60184-285">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60184-285">In Global Catalog</span></span>      | <span data-ttu-id="60184-286">True</span><span class="sxs-lookup"><span data-stu-id="60184-286">True</span></span>                            |
| <span data-ttu-id="60184-287">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60184-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="60184-288">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60184-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60184-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60184-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60184-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60184-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60184-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-291">Search-Flags</span></span>           | <span data-ttu-id="60184-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60184-292">0x00000000</span></span>                      |
| <span data-ttu-id="60184-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60184-293">System-Flags</span></span>           | <span data-ttu-id="60184-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60184-294">0x00000013</span></span>                      |
| <span data-ttu-id="60184-295">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60184-295">Classes used in</span></span>        | [<span data-ttu-id="60184-296">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60184-296">**Top**</span></span>](c-top.md)<br/> |



 

 






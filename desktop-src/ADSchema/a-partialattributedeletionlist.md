---
title: Atributo de lista de atributos parciales
description: Realiza un seguimiento del estado de replicación interna de réplicas parciales (es decir, en GC). Atributo del objeto NC de réplica parcial. Se usa cuando el GC está en el proceso de quitar atributos de los objetos en sus NC de réplica parcial.
ms.assetid: 0084774b-7231-4cfc-8f60-c014006da2b9
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de lista de atributos parciales
- partialAttributeDeletionList esquema de AD de atributos
topic_type:
- apiref
api_name:
- Partial-Attribute-Deletion-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2c6c0428d71dbba4199eeb441c838fb54a4463
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658778"
---
# <a name="partial-attribute-deletion-list-attribute"></a><span data-ttu-id="1e840-107">Atributo de lista de atributos parciales</span><span class="sxs-lookup"><span data-stu-id="1e840-107">Partial-Attribute-Deletion-List attribute</span></span>

<span data-ttu-id="1e840-108">Realiza un seguimiento del estado de replicación interna de réplicas parciales (es decir, en GC).</span><span class="sxs-lookup"><span data-stu-id="1e840-108">Tracks the internal replication state of partial replicas (that is, on GCs).</span></span> <span data-ttu-id="1e840-109">Atributo del objeto NC de réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="1e840-109">Attribute of the partial replica NC object.</span></span> <span data-ttu-id="1e840-110">Se usa cuando el GC está en el proceso de quitar atributos de los objetos en sus NC de réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="1e840-110">Used when the GC is in the process of removing attributes from the objects in its partial replica NCs.</span></span>



| <span data-ttu-id="1e840-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e840-111">Entry</span></span> | <span data-ttu-id="1e840-112">Value</span><span class="sxs-lookup"><span data-stu-id="1e840-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="1e840-113">CN</span><span class="sxs-lookup"><span data-stu-id="1e840-113">CN</span></span>                | <span data-ttu-id="1e840-114">Lista de atributos parciales eliminados</span><span class="sxs-lookup"><span data-stu-id="1e840-114">Partial-Attribute-Deletion-List</span></span>                       |
| <span data-ttu-id="1e840-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1e840-115">Ldap-Display-Name</span></span> | <span data-ttu-id="1e840-116">partialAttributeDeletionList</span><span class="sxs-lookup"><span data-stu-id="1e840-116">partialAttributeDeletionList</span></span>                          |
| <span data-ttu-id="1e840-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1e840-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="1e840-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1e840-118">Update Privilege</span></span>  | <span data-ttu-id="1e840-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="1e840-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="1e840-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1e840-120">Update Frequency</span></span>  | <span data-ttu-id="1e840-121">Durante la replicación</span><span class="sxs-lookup"><span data-stu-id="1e840-121">During replication</span></span>                                    |
| <span data-ttu-id="1e840-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1e840-122">Attribute-Id</span></span>      | <span data-ttu-id="1e840-123">1.2.840.113556.1.4.663</span><span class="sxs-lookup"><span data-stu-id="1e840-123">1.2.840.113556.1.4.663</span></span>                                |
| <span data-ttu-id="1e840-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1e840-124">System-Id-Guid</span></span>    | <span data-ttu-id="1e840-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1e840-125">28630ec0-41d5-11d1-a9c1-0000f80367c1</span></span>                  |
| <span data-ttu-id="1e840-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e840-126">Syntax</span></span>            | [<span data-ttu-id="1e840-127">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="1e840-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="1e840-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1e840-128">Implementations</span></span>

-   [<span data-ttu-id="1e840-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1e840-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1e840-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1e840-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1e840-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1e840-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1e840-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1e840-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1e840-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1e840-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1e840-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1e840-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1e840-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1e840-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1e840-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e840-136">Windows 2000 Server</span></span>



| <span data-ttu-id="1e840-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e840-137">Entry</span></span> | <span data-ttu-id="1e840-138">Value</span><span class="sxs-lookup"><span data-stu-id="1e840-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e840-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e840-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e840-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e840-141">System-Only</span></span>            | <span data-ttu-id="1e840-142">True</span><span class="sxs-lookup"><span data-stu-id="1e840-142">True</span></span>                            |
| <span data-ttu-id="1e840-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e840-143">Is-Single-Valued</span></span>       | <span data-ttu-id="1e840-144">True</span><span class="sxs-lookup"><span data-stu-id="1e840-144">True</span></span>                            |
| <span data-ttu-id="1e840-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e840-145">Is Indexed</span></span>             | <span data-ttu-id="1e840-146">False</span><span class="sxs-lookup"><span data-stu-id="1e840-146">False</span></span>                           |
| <span data-ttu-id="1e840-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e840-147">In Global Catalog</span></span>      | <span data-ttu-id="1e840-148">True</span><span class="sxs-lookup"><span data-stu-id="1e840-148">True</span></span>                            |
| <span data-ttu-id="1e840-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e840-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e840-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e840-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e840-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e840-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e840-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e840-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e840-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-153">Search-Flags</span></span>           | <span data-ttu-id="1e840-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e840-154">0x00000000</span></span>                      |
| <span data-ttu-id="1e840-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-155">System-Flags</span></span>           | <span data-ttu-id="1e840-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1e840-156">0x00000013</span></span>                      |
| <span data-ttu-id="1e840-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e840-157">Classes used in</span></span>        | [<span data-ttu-id="1e840-158">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e840-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1e840-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e840-159">Windows Server 2003</span></span>



| <span data-ttu-id="1e840-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e840-160">Entry</span></span> | <span data-ttu-id="1e840-161">Value</span><span class="sxs-lookup"><span data-stu-id="1e840-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e840-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e840-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e840-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e840-164">System-Only</span></span>            | <span data-ttu-id="1e840-165">True</span><span class="sxs-lookup"><span data-stu-id="1e840-165">True</span></span>                            |
| <span data-ttu-id="1e840-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e840-166">Is-Single-Valued</span></span>       | <span data-ttu-id="1e840-167">True</span><span class="sxs-lookup"><span data-stu-id="1e840-167">True</span></span>                            |
| <span data-ttu-id="1e840-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e840-168">Is Indexed</span></span>             | <span data-ttu-id="1e840-169">False</span><span class="sxs-lookup"><span data-stu-id="1e840-169">False</span></span>                           |
| <span data-ttu-id="1e840-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e840-170">In Global Catalog</span></span>      | <span data-ttu-id="1e840-171">True</span><span class="sxs-lookup"><span data-stu-id="1e840-171">True</span></span>                            |
| <span data-ttu-id="1e840-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e840-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e840-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e840-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e840-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e840-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e840-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e840-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e840-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-176">Search-Flags</span></span>           | <span data-ttu-id="1e840-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e840-177">0x00000000</span></span>                      |
| <span data-ttu-id="1e840-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-178">System-Flags</span></span>           | <span data-ttu-id="1e840-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1e840-179">0x00000013</span></span>                      |
| <span data-ttu-id="1e840-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e840-180">Classes used in</span></span>        | [<span data-ttu-id="1e840-181">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e840-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1e840-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="1e840-182">ADAM</span></span>



| <span data-ttu-id="1e840-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e840-183">Entry</span></span> | <span data-ttu-id="1e840-184">Value</span><span class="sxs-lookup"><span data-stu-id="1e840-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e840-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e840-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e840-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e840-187">System-Only</span></span>            | <span data-ttu-id="1e840-188">True</span><span class="sxs-lookup"><span data-stu-id="1e840-188">True</span></span>                            |
| <span data-ttu-id="1e840-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e840-189">Is-Single-Valued</span></span>       | <span data-ttu-id="1e840-190">True</span><span class="sxs-lookup"><span data-stu-id="1e840-190">True</span></span>                            |
| <span data-ttu-id="1e840-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e840-191">Is Indexed</span></span>             | <span data-ttu-id="1e840-192">False</span><span class="sxs-lookup"><span data-stu-id="1e840-192">False</span></span>                           |
| <span data-ttu-id="1e840-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e840-193">In Global Catalog</span></span>      | <span data-ttu-id="1e840-194">True</span><span class="sxs-lookup"><span data-stu-id="1e840-194">True</span></span>                            |
| <span data-ttu-id="1e840-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e840-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e840-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e840-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e840-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e840-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e840-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e840-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e840-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-199">Search-Flags</span></span>           | <span data-ttu-id="1e840-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e840-200">0x00000000</span></span>                      |
| <span data-ttu-id="1e840-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-201">System-Flags</span></span>           | <span data-ttu-id="1e840-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1e840-202">0x00000013</span></span>                      |
| <span data-ttu-id="1e840-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e840-203">Classes used in</span></span>        | [<span data-ttu-id="1e840-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e840-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1e840-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1e840-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1e840-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e840-206">Entry</span></span> | <span data-ttu-id="1e840-207">Value</span><span class="sxs-lookup"><span data-stu-id="1e840-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e840-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e840-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e840-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e840-210">System-Only</span></span>            | <span data-ttu-id="1e840-211">True</span><span class="sxs-lookup"><span data-stu-id="1e840-211">True</span></span>                            |
| <span data-ttu-id="1e840-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e840-212">Is-Single-Valued</span></span>       | <span data-ttu-id="1e840-213">True</span><span class="sxs-lookup"><span data-stu-id="1e840-213">True</span></span>                            |
| <span data-ttu-id="1e840-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e840-214">Is Indexed</span></span>             | <span data-ttu-id="1e840-215">False</span><span class="sxs-lookup"><span data-stu-id="1e840-215">False</span></span>                           |
| <span data-ttu-id="1e840-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e840-216">In Global Catalog</span></span>      | <span data-ttu-id="1e840-217">True</span><span class="sxs-lookup"><span data-stu-id="1e840-217">True</span></span>                            |
| <span data-ttu-id="1e840-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e840-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e840-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e840-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e840-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e840-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e840-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e840-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e840-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-222">Search-Flags</span></span>           | <span data-ttu-id="1e840-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e840-223">0x00000000</span></span>                      |
| <span data-ttu-id="1e840-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-224">System-Flags</span></span>           | <span data-ttu-id="1e840-225">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1e840-225">0x00000013</span></span>                      |
| <span data-ttu-id="1e840-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e840-226">Classes used in</span></span>        | [<span data-ttu-id="1e840-227">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e840-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1e840-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e840-228">Windows Server 2008</span></span>



| <span data-ttu-id="1e840-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e840-229">Entry</span></span> | <span data-ttu-id="1e840-230">Value</span><span class="sxs-lookup"><span data-stu-id="1e840-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e840-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e840-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e840-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e840-233">System-Only</span></span>            | <span data-ttu-id="1e840-234">True</span><span class="sxs-lookup"><span data-stu-id="1e840-234">True</span></span>                            |
| <span data-ttu-id="1e840-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e840-235">Is-Single-Valued</span></span>       | <span data-ttu-id="1e840-236">True</span><span class="sxs-lookup"><span data-stu-id="1e840-236">True</span></span>                            |
| <span data-ttu-id="1e840-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e840-237">Is Indexed</span></span>             | <span data-ttu-id="1e840-238">False</span><span class="sxs-lookup"><span data-stu-id="1e840-238">False</span></span>                           |
| <span data-ttu-id="1e840-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e840-239">In Global Catalog</span></span>      | <span data-ttu-id="1e840-240">True</span><span class="sxs-lookup"><span data-stu-id="1e840-240">True</span></span>                            |
| <span data-ttu-id="1e840-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e840-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e840-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e840-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e840-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e840-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e840-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e840-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e840-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-245">Search-Flags</span></span>           | <span data-ttu-id="1e840-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e840-246">0x00000000</span></span>                      |
| <span data-ttu-id="1e840-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-247">System-Flags</span></span>           | <span data-ttu-id="1e840-248">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1e840-248">0x00000013</span></span>                      |
| <span data-ttu-id="1e840-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e840-249">Classes used in</span></span>        | [<span data-ttu-id="1e840-250">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e840-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1e840-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e840-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1e840-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e840-252">Entry</span></span> | <span data-ttu-id="1e840-253">Value</span><span class="sxs-lookup"><span data-stu-id="1e840-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e840-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e840-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e840-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e840-256">System-Only</span></span>            | <span data-ttu-id="1e840-257">True</span><span class="sxs-lookup"><span data-stu-id="1e840-257">True</span></span>                            |
| <span data-ttu-id="1e840-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e840-258">Is-Single-Valued</span></span>       | <span data-ttu-id="1e840-259">True</span><span class="sxs-lookup"><span data-stu-id="1e840-259">True</span></span>                            |
| <span data-ttu-id="1e840-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e840-260">Is Indexed</span></span>             | <span data-ttu-id="1e840-261">False</span><span class="sxs-lookup"><span data-stu-id="1e840-261">False</span></span>                           |
| <span data-ttu-id="1e840-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e840-262">In Global Catalog</span></span>      | <span data-ttu-id="1e840-263">True</span><span class="sxs-lookup"><span data-stu-id="1e840-263">True</span></span>                            |
| <span data-ttu-id="1e840-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e840-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e840-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e840-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e840-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e840-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e840-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e840-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e840-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-268">Search-Flags</span></span>           | <span data-ttu-id="1e840-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e840-269">0x00000000</span></span>                      |
| <span data-ttu-id="1e840-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-270">System-Flags</span></span>           | <span data-ttu-id="1e840-271">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1e840-271">0x00000013</span></span>                      |
| <span data-ttu-id="1e840-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e840-272">Classes used in</span></span>        | [<span data-ttu-id="1e840-273">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e840-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1e840-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e840-274">Windows Server 2012</span></span>



| <span data-ttu-id="1e840-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e840-275">Entry</span></span> | <span data-ttu-id="1e840-276">Value</span><span class="sxs-lookup"><span data-stu-id="1e840-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e840-277">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e840-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e840-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="1e840-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e840-279">System-Only</span></span>            | <span data-ttu-id="1e840-280">True</span><span class="sxs-lookup"><span data-stu-id="1e840-280">True</span></span>                            |
| <span data-ttu-id="1e840-281">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e840-281">Is-Single-Valued</span></span>       | <span data-ttu-id="1e840-282">True</span><span class="sxs-lookup"><span data-stu-id="1e840-282">True</span></span>                            |
| <span data-ttu-id="1e840-283">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e840-283">Is Indexed</span></span>             | <span data-ttu-id="1e840-284">False</span><span class="sxs-lookup"><span data-stu-id="1e840-284">False</span></span>                           |
| <span data-ttu-id="1e840-285">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e840-285">In Global Catalog</span></span>      | <span data-ttu-id="1e840-286">True</span><span class="sxs-lookup"><span data-stu-id="1e840-286">True</span></span>                            |
| <span data-ttu-id="1e840-287">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e840-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e840-288">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e840-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e840-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e840-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e840-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e840-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e840-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-291">Search-Flags</span></span>           | <span data-ttu-id="1e840-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e840-292">0x00000000</span></span>                      |
| <span data-ttu-id="1e840-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e840-293">System-Flags</span></span>           | <span data-ttu-id="1e840-294">0x00000013</span><span class="sxs-lookup"><span data-stu-id="1e840-294">0x00000013</span></span>                      |
| <span data-ttu-id="1e840-295">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e840-295">Classes used in</span></span>        | [<span data-ttu-id="1e840-296">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e840-296">**Top**</span></span>](c-top.md)<br/> |



 

 






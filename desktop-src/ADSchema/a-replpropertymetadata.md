---
title: Atributo REPL-Property-meta-data
description: Realiza un seguimiento de la información de estado de replicación interna para objetos de DS. La información aquí se puede extraer de forma pública a través de la API pública DsReplicaGetInfo (). Presente en todos los objetos de DS.
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- Atributo REPL-Property-meta-data esquema de AD
- replPropertyMetaData esquema de AD de atributos
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7639d9bca600457d519862e1f57d9ee698d2a155
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804831"
---
# <a name="repl-property-meta-data-attribute"></a><span data-ttu-id="09489-107">Atributo REPL-Property-meta-data</span><span class="sxs-lookup"><span data-stu-id="09489-107">Repl-Property-Meta-Data attribute</span></span>

<span data-ttu-id="09489-108">Realiza un seguimiento de la información de estado de replicación interna para objetos de DS.</span><span class="sxs-lookup"><span data-stu-id="09489-108">Tracks internal replication state information for DS objects.</span></span> <span data-ttu-id="09489-109">La información aquí se puede extraer de forma pública a través de la API pública DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="09489-109">Information here can be extracted in public form through the public API DsReplicaGetInfo().</span></span> <span data-ttu-id="09489-110">Presente en todos los objetos de DS.</span><span class="sxs-lookup"><span data-stu-id="09489-110">Present on all DS objects.</span></span>



| <span data-ttu-id="09489-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="09489-111">Entry</span></span> | <span data-ttu-id="09489-112">Value</span><span class="sxs-lookup"><span data-stu-id="09489-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="09489-113">CN</span><span class="sxs-lookup"><span data-stu-id="09489-113">CN</span></span>                | <span data-ttu-id="09489-114">REPL-Property-meta-data</span><span class="sxs-lookup"><span data-stu-id="09489-114">Repl-Property-Meta-Data</span></span>                                                      |
| <span data-ttu-id="09489-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="09489-115">Ldap-Display-Name</span></span> | <span data-ttu-id="09489-116">replPropertyMetaData</span><span class="sxs-lookup"><span data-stu-id="09489-116">replPropertyMetaData</span></span>                                                         |
| <span data-ttu-id="09489-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="09489-117">Size</span></span>              | <span data-ttu-id="09489-118">La longitud es proporcional al número de atributos replicables en el objeto.</span><span class="sxs-lookup"><span data-stu-id="09489-118">Length is proportional to the number of replicable attributes on the object.</span></span> |
| <span data-ttu-id="09489-119">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="09489-119">Update Privilege</span></span>  | <span data-ttu-id="09489-120">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="09489-120">This value is set by the system.</span></span>                                             |
| <span data-ttu-id="09489-121">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="09489-121">Update Frequency</span></span>  | <span data-ttu-id="09489-122">Cambios en respuesta a los cambios de replicación en el objeto.</span><span class="sxs-lookup"><span data-stu-id="09489-122">Changes in response to any replicating changes in the object.</span></span>                |
| <span data-ttu-id="09489-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09489-123">Attribute-Id</span></span>      | <span data-ttu-id="09489-124">1.2.840.113556.1.4.3</span><span class="sxs-lookup"><span data-stu-id="09489-124">1.2.840.113556.1.4.3</span></span>                                                         |
| <span data-ttu-id="09489-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="09489-125">System-Id-Guid</span></span>    | <span data-ttu-id="09489-126">281416c0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="09489-126">281416c0-1968-11d0-a28f-00aa003049e2</span></span>                                         |
| <span data-ttu-id="09489-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09489-127">Syntax</span></span>            | [<span data-ttu-id="09489-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="09489-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="09489-129">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="09489-129">Implementations</span></span>

-   [<span data-ttu-id="09489-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="09489-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="09489-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09489-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09489-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="09489-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="09489-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09489-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09489-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09489-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09489-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09489-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09489-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09489-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="09489-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09489-137">Windows 2000 Server</span></span>



| <span data-ttu-id="09489-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="09489-138">Entry</span></span> | <span data-ttu-id="09489-139">Value</span><span class="sxs-lookup"><span data-stu-id="09489-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09489-140">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="09489-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09489-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="09489-142">System-Only</span></span>            | <span data-ttu-id="09489-143">True</span><span class="sxs-lookup"><span data-stu-id="09489-143">True</span></span>                            |
| <span data-ttu-id="09489-144">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="09489-144">Is-Single-Valued</span></span>       | <span data-ttu-id="09489-145">True</span><span class="sxs-lookup"><span data-stu-id="09489-145">True</span></span>                            |
| <span data-ttu-id="09489-146">Está indexado</span><span class="sxs-lookup"><span data-stu-id="09489-146">Is Indexed</span></span>             | <span data-ttu-id="09489-147">False</span><span class="sxs-lookup"><span data-stu-id="09489-147">False</span></span>                           |
| <span data-ttu-id="09489-148">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="09489-148">In Global Catalog</span></span>      | <span data-ttu-id="09489-149">True</span><span class="sxs-lookup"><span data-stu-id="09489-149">True</span></span>                            |
| <span data-ttu-id="09489-150">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="09489-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="09489-151">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09489-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09489-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09489-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09489-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09489-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09489-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-154">Search-Flags</span></span>           | <span data-ttu-id="09489-155">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09489-155">0x00000008</span></span>                      |
| <span data-ttu-id="09489-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-156">System-Flags</span></span>           | <span data-ttu-id="09489-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="09489-157">0x00000013</span></span>                      |
| <span data-ttu-id="09489-158">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="09489-158">Classes used in</span></span>        | [<span data-ttu-id="09489-159">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="09489-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="09489-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09489-160">Windows Server 2003</span></span>



| <span data-ttu-id="09489-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="09489-161">Entry</span></span> | <span data-ttu-id="09489-162">Value</span><span class="sxs-lookup"><span data-stu-id="09489-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09489-163">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="09489-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09489-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="09489-165">System-Only</span></span>            | <span data-ttu-id="09489-166">True</span><span class="sxs-lookup"><span data-stu-id="09489-166">True</span></span>                            |
| <span data-ttu-id="09489-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="09489-167">Is-Single-Valued</span></span>       | <span data-ttu-id="09489-168">True</span><span class="sxs-lookup"><span data-stu-id="09489-168">True</span></span>                            |
| <span data-ttu-id="09489-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="09489-169">Is Indexed</span></span>             | <span data-ttu-id="09489-170">False</span><span class="sxs-lookup"><span data-stu-id="09489-170">False</span></span>                           |
| <span data-ttu-id="09489-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="09489-171">In Global Catalog</span></span>      | <span data-ttu-id="09489-172">True</span><span class="sxs-lookup"><span data-stu-id="09489-172">True</span></span>                            |
| <span data-ttu-id="09489-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="09489-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="09489-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09489-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09489-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09489-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09489-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09489-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09489-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-177">Search-Flags</span></span>           | <span data-ttu-id="09489-178">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09489-178">0x00000008</span></span>                      |
| <span data-ttu-id="09489-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-179">System-Flags</span></span>           | <span data-ttu-id="09489-180">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="09489-180">0x0000001B</span></span>                      |
| <span data-ttu-id="09489-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="09489-181">Classes used in</span></span>        | [<span data-ttu-id="09489-182">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="09489-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="09489-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="09489-183">ADAM</span></span>



| <span data-ttu-id="09489-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="09489-184">Entry</span></span> | <span data-ttu-id="09489-185">Value</span><span class="sxs-lookup"><span data-stu-id="09489-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09489-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="09489-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09489-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="09489-188">System-Only</span></span>            | <span data-ttu-id="09489-189">True</span><span class="sxs-lookup"><span data-stu-id="09489-189">True</span></span>                            |
| <span data-ttu-id="09489-190">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="09489-190">Is-Single-Valued</span></span>       | <span data-ttu-id="09489-191">True</span><span class="sxs-lookup"><span data-stu-id="09489-191">True</span></span>                            |
| <span data-ttu-id="09489-192">Está indexado</span><span class="sxs-lookup"><span data-stu-id="09489-192">Is Indexed</span></span>             | <span data-ttu-id="09489-193">False</span><span class="sxs-lookup"><span data-stu-id="09489-193">False</span></span>                           |
| <span data-ttu-id="09489-194">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="09489-194">In Global Catalog</span></span>      | <span data-ttu-id="09489-195">True</span><span class="sxs-lookup"><span data-stu-id="09489-195">True</span></span>                            |
| <span data-ttu-id="09489-196">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="09489-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="09489-197">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09489-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09489-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09489-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09489-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09489-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09489-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-200">Search-Flags</span></span>           | <span data-ttu-id="09489-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09489-201">0x00000008</span></span>                      |
| <span data-ttu-id="09489-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-202">System-Flags</span></span>           | <span data-ttu-id="09489-203">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="09489-203">0x0000001B</span></span>                      |
| <span data-ttu-id="09489-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="09489-204">Classes used in</span></span>        | [<span data-ttu-id="09489-205">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="09489-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09489-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09489-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09489-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="09489-207">Entry</span></span> | <span data-ttu-id="09489-208">Value</span><span class="sxs-lookup"><span data-stu-id="09489-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09489-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="09489-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09489-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="09489-211">System-Only</span></span>            | <span data-ttu-id="09489-212">True</span><span class="sxs-lookup"><span data-stu-id="09489-212">True</span></span>                            |
| <span data-ttu-id="09489-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="09489-213">Is-Single-Valued</span></span>       | <span data-ttu-id="09489-214">True</span><span class="sxs-lookup"><span data-stu-id="09489-214">True</span></span>                            |
| <span data-ttu-id="09489-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="09489-215">Is Indexed</span></span>             | <span data-ttu-id="09489-216">False</span><span class="sxs-lookup"><span data-stu-id="09489-216">False</span></span>                           |
| <span data-ttu-id="09489-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="09489-217">In Global Catalog</span></span>      | <span data-ttu-id="09489-218">True</span><span class="sxs-lookup"><span data-stu-id="09489-218">True</span></span>                            |
| <span data-ttu-id="09489-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="09489-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="09489-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09489-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09489-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09489-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09489-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09489-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09489-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-223">Search-Flags</span></span>           | <span data-ttu-id="09489-224">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09489-224">0x00000008</span></span>                      |
| <span data-ttu-id="09489-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-225">System-Flags</span></span>           | <span data-ttu-id="09489-226">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="09489-226">0x0000001B</span></span>                      |
| <span data-ttu-id="09489-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="09489-227">Classes used in</span></span>        | [<span data-ttu-id="09489-228">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="09489-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09489-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09489-229">Windows Server 2008</span></span>



| <span data-ttu-id="09489-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="09489-230">Entry</span></span> | <span data-ttu-id="09489-231">Value</span><span class="sxs-lookup"><span data-stu-id="09489-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09489-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="09489-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09489-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="09489-234">System-Only</span></span>            | <span data-ttu-id="09489-235">True</span><span class="sxs-lookup"><span data-stu-id="09489-235">True</span></span>                            |
| <span data-ttu-id="09489-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="09489-236">Is-Single-Valued</span></span>       | <span data-ttu-id="09489-237">True</span><span class="sxs-lookup"><span data-stu-id="09489-237">True</span></span>                            |
| <span data-ttu-id="09489-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="09489-238">Is Indexed</span></span>             | <span data-ttu-id="09489-239">False</span><span class="sxs-lookup"><span data-stu-id="09489-239">False</span></span>                           |
| <span data-ttu-id="09489-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="09489-240">In Global Catalog</span></span>      | <span data-ttu-id="09489-241">True</span><span class="sxs-lookup"><span data-stu-id="09489-241">True</span></span>                            |
| <span data-ttu-id="09489-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="09489-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="09489-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09489-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09489-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09489-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09489-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09489-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09489-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-246">Search-Flags</span></span>           | <span data-ttu-id="09489-247">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09489-247">0x00000008</span></span>                      |
| <span data-ttu-id="09489-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-248">System-Flags</span></span>           | <span data-ttu-id="09489-249">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="09489-249">0x0000001B</span></span>                      |
| <span data-ttu-id="09489-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="09489-250">Classes used in</span></span>        | [<span data-ttu-id="09489-251">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="09489-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09489-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09489-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09489-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="09489-253">Entry</span></span> | <span data-ttu-id="09489-254">Value</span><span class="sxs-lookup"><span data-stu-id="09489-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09489-255">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="09489-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09489-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="09489-257">System-Only</span></span>            | <span data-ttu-id="09489-258">True</span><span class="sxs-lookup"><span data-stu-id="09489-258">True</span></span>                            |
| <span data-ttu-id="09489-259">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="09489-259">Is-Single-Valued</span></span>       | <span data-ttu-id="09489-260">True</span><span class="sxs-lookup"><span data-stu-id="09489-260">True</span></span>                            |
| <span data-ttu-id="09489-261">Está indexado</span><span class="sxs-lookup"><span data-stu-id="09489-261">Is Indexed</span></span>             | <span data-ttu-id="09489-262">False</span><span class="sxs-lookup"><span data-stu-id="09489-262">False</span></span>                           |
| <span data-ttu-id="09489-263">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="09489-263">In Global Catalog</span></span>      | <span data-ttu-id="09489-264">True</span><span class="sxs-lookup"><span data-stu-id="09489-264">True</span></span>                            |
| <span data-ttu-id="09489-265">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="09489-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="09489-266">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09489-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09489-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09489-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09489-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09489-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09489-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-269">Search-Flags</span></span>           | <span data-ttu-id="09489-270">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09489-270">0x00000008</span></span>                      |
| <span data-ttu-id="09489-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-271">System-Flags</span></span>           | <span data-ttu-id="09489-272">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="09489-272">0x0000001B</span></span>                      |
| <span data-ttu-id="09489-273">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="09489-273">Classes used in</span></span>        | [<span data-ttu-id="09489-274">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="09489-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09489-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09489-275">Windows Server 2012</span></span>



| <span data-ttu-id="09489-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="09489-276">Entry</span></span> | <span data-ttu-id="09489-277">Value</span><span class="sxs-lookup"><span data-stu-id="09489-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="09489-278">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="09489-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09489-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="09489-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="09489-280">System-Only</span></span>            | <span data-ttu-id="09489-281">True</span><span class="sxs-lookup"><span data-stu-id="09489-281">True</span></span>                            |
| <span data-ttu-id="09489-282">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="09489-282">Is-Single-Valued</span></span>       | <span data-ttu-id="09489-283">True</span><span class="sxs-lookup"><span data-stu-id="09489-283">True</span></span>                            |
| <span data-ttu-id="09489-284">Está indexado</span><span class="sxs-lookup"><span data-stu-id="09489-284">Is Indexed</span></span>             | <span data-ttu-id="09489-285">False</span><span class="sxs-lookup"><span data-stu-id="09489-285">False</span></span>                           |
| <span data-ttu-id="09489-286">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="09489-286">In Global Catalog</span></span>      | <span data-ttu-id="09489-287">True</span><span class="sxs-lookup"><span data-stu-id="09489-287">True</span></span>                            |
| <span data-ttu-id="09489-288">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="09489-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="09489-289">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09489-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="09489-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09489-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="09489-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09489-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="09489-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-292">Search-Flags</span></span>           | <span data-ttu-id="09489-293">0x00000008</span><span class="sxs-lookup"><span data-stu-id="09489-293">0x00000008</span></span>                      |
| <span data-ttu-id="09489-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09489-294">System-Flags</span></span>           | <span data-ttu-id="09489-295">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="09489-295">0x0000001B</span></span>                      |
| <span data-ttu-id="09489-296">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="09489-296">Classes used in</span></span>        | [<span data-ttu-id="09489-297">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="09489-297">**Top**</span></span>](c-top.md)<br/> |



 

 






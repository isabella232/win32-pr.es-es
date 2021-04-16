---
title: REPL-UpToDate-vector (atributo)
description: Realiza el seguimiento de la información de estado de replicación interna para un NC completo. La información aquí se puede extraer de forma pública a través de la API DsReplicaGetInfo (). Presente en todos los objetos raíz de NC.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- REPL-UpToDate-esquema de AD de atributo de vector
- Del repluptodatevector esquema de AD de atributos
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9263111459d01d99cf5990d1c818b5ff2a7a19be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658987"
---
# <a name="repl-uptodate-vector-attribute"></a><span data-ttu-id="976ab-107">REPL-UpToDate-vector (atributo)</span><span class="sxs-lookup"><span data-stu-id="976ab-107">Repl-UpToDate-Vector attribute</span></span>

<span data-ttu-id="976ab-108">Realiza el seguimiento de la información de estado de replicación interna para un NC completo.</span><span class="sxs-lookup"><span data-stu-id="976ab-108">Tracks internal replication state information for an entire NC.</span></span> <span data-ttu-id="976ab-109">La información aquí se puede extraer de forma pública a través de la API DsReplicaGetInfo ().</span><span class="sxs-lookup"><span data-stu-id="976ab-109">Information here can be extracted in public form through the API DsReplicaGetInfo().</span></span> <span data-ttu-id="976ab-110">Presente en todos los objetos raíz de NC.</span><span class="sxs-lookup"><span data-stu-id="976ab-110">Present on all NC root objects.</span></span>



| <span data-ttu-id="976ab-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="976ab-111">Entry</span></span> | <span data-ttu-id="976ab-112">Value</span><span class="sxs-lookup"><span data-stu-id="976ab-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="976ab-113">CN</span><span class="sxs-lookup"><span data-stu-id="976ab-113">CN</span></span>                | <span data-ttu-id="976ab-114">REPL-UpToDate-Vector</span><span class="sxs-lookup"><span data-stu-id="976ab-114">Repl-UpToDate-Vector</span></span>                                                           |
| <span data-ttu-id="976ab-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="976ab-115">Ldap-Display-Name</span></span> | <span data-ttu-id="976ab-116">Del repluptodatevector</span><span class="sxs-lookup"><span data-stu-id="976ab-116">replUpToDateVector</span></span>                                                             |
| <span data-ttu-id="976ab-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="976ab-117">Size</span></span>              | <span data-ttu-id="976ab-118">La longitud es proporcional al número de réplicas (pasadas y presentes) del NC.</span><span class="sxs-lookup"><span data-stu-id="976ab-118">Length is proportional to the number of replicas (past and present) of the NC.</span></span> |
| <span data-ttu-id="976ab-119">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="976ab-119">Update Privilege</span></span>  | <span data-ttu-id="976ab-120">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="976ab-120">This value is set by the system.</span></span>                                               |
| <span data-ttu-id="976ab-121">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="976ab-121">Update Frequency</span></span>  | <span data-ttu-id="976ab-122">Cambios en respuesta a los ciclos de replicación de entrada completados.</span><span class="sxs-lookup"><span data-stu-id="976ab-122">Changes in response to completed inbound replication cycles.</span></span>                   |
| <span data-ttu-id="976ab-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="976ab-123">Attribute-Id</span></span>      | <span data-ttu-id="976ab-124">1.2.840.113556.1.4.4</span><span class="sxs-lookup"><span data-stu-id="976ab-124">1.2.840.113556.1.4.4</span></span>                                                           |
| <span data-ttu-id="976ab-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="976ab-125">System-Id-Guid</span></span>    | <span data-ttu-id="976ab-126">bf967a16-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="976ab-126">bf967a16-0de6-11d0-a285-00aa003049e2</span></span>                                           |
| <span data-ttu-id="976ab-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="976ab-127">Syntax</span></span>            | [<span data-ttu-id="976ab-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="976ab-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                          |



## <a name="implementations"></a><span data-ttu-id="976ab-129">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="976ab-129">Implementations</span></span>

-   [<span data-ttu-id="976ab-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="976ab-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="976ab-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="976ab-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="976ab-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="976ab-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="976ab-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="976ab-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="976ab-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="976ab-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="976ab-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="976ab-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="976ab-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="976ab-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="976ab-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="976ab-137">Windows 2000 Server</span></span>



| <span data-ttu-id="976ab-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="976ab-138">Entry</span></span> | <span data-ttu-id="976ab-139">Value</span><span class="sxs-lookup"><span data-stu-id="976ab-139">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="976ab-140">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="976ab-140">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="976ab-141">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="976ab-142">System-Only</span></span>            | <span data-ttu-id="976ab-143">True</span><span class="sxs-lookup"><span data-stu-id="976ab-143">True</span></span>                            |
| <span data-ttu-id="976ab-144">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="976ab-144">Is-Single-Valued</span></span>       | <span data-ttu-id="976ab-145">True</span><span class="sxs-lookup"><span data-stu-id="976ab-145">True</span></span>                            |
| <span data-ttu-id="976ab-146">Está indexado</span><span class="sxs-lookup"><span data-stu-id="976ab-146">Is Indexed</span></span>             | <span data-ttu-id="976ab-147">False</span><span class="sxs-lookup"><span data-stu-id="976ab-147">False</span></span>                           |
| <span data-ttu-id="976ab-148">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="976ab-148">In Global Catalog</span></span>      | <span data-ttu-id="976ab-149">True</span><span class="sxs-lookup"><span data-stu-id="976ab-149">True</span></span>                            |
| <span data-ttu-id="976ab-150">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="976ab-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="976ab-151">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="976ab-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="976ab-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="976ab-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="976ab-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="976ab-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="976ab-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-154">Search-Flags</span></span>           | <span data-ttu-id="976ab-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="976ab-155">0x00000000</span></span>                      |
| <span data-ttu-id="976ab-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-156">System-Flags</span></span>           | <span data-ttu-id="976ab-157">0x00000013</span><span class="sxs-lookup"><span data-stu-id="976ab-157">0x00000013</span></span>                      |
| <span data-ttu-id="976ab-158">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="976ab-158">Classes used in</span></span>        | [<span data-ttu-id="976ab-159">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="976ab-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="976ab-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="976ab-160">Windows Server 2003</span></span>



| <span data-ttu-id="976ab-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="976ab-161">Entry</span></span> | <span data-ttu-id="976ab-162">Value</span><span class="sxs-lookup"><span data-stu-id="976ab-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="976ab-163">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="976ab-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="976ab-164">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="976ab-165">System-Only</span></span>            | <span data-ttu-id="976ab-166">True</span><span class="sxs-lookup"><span data-stu-id="976ab-166">True</span></span>                            |
| <span data-ttu-id="976ab-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="976ab-167">Is-Single-Valued</span></span>       | <span data-ttu-id="976ab-168">True</span><span class="sxs-lookup"><span data-stu-id="976ab-168">True</span></span>                            |
| <span data-ttu-id="976ab-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="976ab-169">Is Indexed</span></span>             | <span data-ttu-id="976ab-170">False</span><span class="sxs-lookup"><span data-stu-id="976ab-170">False</span></span>                           |
| <span data-ttu-id="976ab-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="976ab-171">In Global Catalog</span></span>      | <span data-ttu-id="976ab-172">True</span><span class="sxs-lookup"><span data-stu-id="976ab-172">True</span></span>                            |
| <span data-ttu-id="976ab-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="976ab-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="976ab-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="976ab-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="976ab-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="976ab-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="976ab-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="976ab-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="976ab-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-177">Search-Flags</span></span>           | <span data-ttu-id="976ab-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="976ab-178">0x00000000</span></span>                      |
| <span data-ttu-id="976ab-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-179">System-Flags</span></span>           | <span data-ttu-id="976ab-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="976ab-180">0x00000013</span></span>                      |
| <span data-ttu-id="976ab-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="976ab-181">Classes used in</span></span>        | [<span data-ttu-id="976ab-182">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="976ab-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="976ab-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="976ab-183">ADAM</span></span>



| <span data-ttu-id="976ab-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="976ab-184">Entry</span></span> | <span data-ttu-id="976ab-185">Value</span><span class="sxs-lookup"><span data-stu-id="976ab-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="976ab-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="976ab-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="976ab-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="976ab-188">System-Only</span></span>            | <span data-ttu-id="976ab-189">True</span><span class="sxs-lookup"><span data-stu-id="976ab-189">True</span></span>                            |
| <span data-ttu-id="976ab-190">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="976ab-190">Is-Single-Valued</span></span>       | <span data-ttu-id="976ab-191">True</span><span class="sxs-lookup"><span data-stu-id="976ab-191">True</span></span>                            |
| <span data-ttu-id="976ab-192">Está indexado</span><span class="sxs-lookup"><span data-stu-id="976ab-192">Is Indexed</span></span>             | <span data-ttu-id="976ab-193">False</span><span class="sxs-lookup"><span data-stu-id="976ab-193">False</span></span>                           |
| <span data-ttu-id="976ab-194">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="976ab-194">In Global Catalog</span></span>      | <span data-ttu-id="976ab-195">True</span><span class="sxs-lookup"><span data-stu-id="976ab-195">True</span></span>                            |
| <span data-ttu-id="976ab-196">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="976ab-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="976ab-197">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="976ab-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="976ab-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="976ab-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="976ab-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="976ab-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="976ab-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-200">Search-Flags</span></span>           | <span data-ttu-id="976ab-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="976ab-201">0x00000000</span></span>                      |
| <span data-ttu-id="976ab-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-202">System-Flags</span></span>           | <span data-ttu-id="976ab-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="976ab-203">0x00000013</span></span>                      |
| <span data-ttu-id="976ab-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="976ab-204">Classes used in</span></span>        | [<span data-ttu-id="976ab-205">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="976ab-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="976ab-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="976ab-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="976ab-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="976ab-207">Entry</span></span> | <span data-ttu-id="976ab-208">Value</span><span class="sxs-lookup"><span data-stu-id="976ab-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="976ab-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="976ab-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="976ab-210">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="976ab-211">System-Only</span></span>            | <span data-ttu-id="976ab-212">True</span><span class="sxs-lookup"><span data-stu-id="976ab-212">True</span></span>                            |
| <span data-ttu-id="976ab-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="976ab-213">Is-Single-Valued</span></span>       | <span data-ttu-id="976ab-214">True</span><span class="sxs-lookup"><span data-stu-id="976ab-214">True</span></span>                            |
| <span data-ttu-id="976ab-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="976ab-215">Is Indexed</span></span>             | <span data-ttu-id="976ab-216">False</span><span class="sxs-lookup"><span data-stu-id="976ab-216">False</span></span>                           |
| <span data-ttu-id="976ab-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="976ab-217">In Global Catalog</span></span>      | <span data-ttu-id="976ab-218">True</span><span class="sxs-lookup"><span data-stu-id="976ab-218">True</span></span>                            |
| <span data-ttu-id="976ab-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="976ab-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="976ab-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="976ab-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="976ab-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="976ab-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="976ab-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="976ab-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="976ab-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-223">Search-Flags</span></span>           | <span data-ttu-id="976ab-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="976ab-224">0x00000000</span></span>                      |
| <span data-ttu-id="976ab-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-225">System-Flags</span></span>           | <span data-ttu-id="976ab-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="976ab-226">0x00000013</span></span>                      |
| <span data-ttu-id="976ab-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="976ab-227">Classes used in</span></span>        | [<span data-ttu-id="976ab-228">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="976ab-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="976ab-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="976ab-229">Windows Server 2008</span></span>



| <span data-ttu-id="976ab-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="976ab-230">Entry</span></span> | <span data-ttu-id="976ab-231">Value</span><span class="sxs-lookup"><span data-stu-id="976ab-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="976ab-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="976ab-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="976ab-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="976ab-234">System-Only</span></span>            | <span data-ttu-id="976ab-235">True</span><span class="sxs-lookup"><span data-stu-id="976ab-235">True</span></span>                            |
| <span data-ttu-id="976ab-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="976ab-236">Is-Single-Valued</span></span>       | <span data-ttu-id="976ab-237">True</span><span class="sxs-lookup"><span data-stu-id="976ab-237">True</span></span>                            |
| <span data-ttu-id="976ab-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="976ab-238">Is Indexed</span></span>             | <span data-ttu-id="976ab-239">False</span><span class="sxs-lookup"><span data-stu-id="976ab-239">False</span></span>                           |
| <span data-ttu-id="976ab-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="976ab-240">In Global Catalog</span></span>      | <span data-ttu-id="976ab-241">True</span><span class="sxs-lookup"><span data-stu-id="976ab-241">True</span></span>                            |
| <span data-ttu-id="976ab-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="976ab-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="976ab-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="976ab-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="976ab-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="976ab-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="976ab-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="976ab-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="976ab-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-246">Search-Flags</span></span>           | <span data-ttu-id="976ab-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="976ab-247">0x00000000</span></span>                      |
| <span data-ttu-id="976ab-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-248">System-Flags</span></span>           | <span data-ttu-id="976ab-249">0x00000013</span><span class="sxs-lookup"><span data-stu-id="976ab-249">0x00000013</span></span>                      |
| <span data-ttu-id="976ab-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="976ab-250">Classes used in</span></span>        | [<span data-ttu-id="976ab-251">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="976ab-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="976ab-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="976ab-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="976ab-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="976ab-253">Entry</span></span> | <span data-ttu-id="976ab-254">Value</span><span class="sxs-lookup"><span data-stu-id="976ab-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="976ab-255">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="976ab-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="976ab-256">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="976ab-257">System-Only</span></span>            | <span data-ttu-id="976ab-258">True</span><span class="sxs-lookup"><span data-stu-id="976ab-258">True</span></span>                            |
| <span data-ttu-id="976ab-259">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="976ab-259">Is-Single-Valued</span></span>       | <span data-ttu-id="976ab-260">True</span><span class="sxs-lookup"><span data-stu-id="976ab-260">True</span></span>                            |
| <span data-ttu-id="976ab-261">Está indexado</span><span class="sxs-lookup"><span data-stu-id="976ab-261">Is Indexed</span></span>             | <span data-ttu-id="976ab-262">False</span><span class="sxs-lookup"><span data-stu-id="976ab-262">False</span></span>                           |
| <span data-ttu-id="976ab-263">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="976ab-263">In Global Catalog</span></span>      | <span data-ttu-id="976ab-264">True</span><span class="sxs-lookup"><span data-stu-id="976ab-264">True</span></span>                            |
| <span data-ttu-id="976ab-265">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="976ab-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="976ab-266">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="976ab-266">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="976ab-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="976ab-267">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="976ab-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="976ab-268">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="976ab-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-269">Search-Flags</span></span>           | <span data-ttu-id="976ab-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="976ab-270">0x00000000</span></span>                      |
| <span data-ttu-id="976ab-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-271">System-Flags</span></span>           | <span data-ttu-id="976ab-272">0x00000013</span><span class="sxs-lookup"><span data-stu-id="976ab-272">0x00000013</span></span>                      |
| <span data-ttu-id="976ab-273">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="976ab-273">Classes used in</span></span>        | [<span data-ttu-id="976ab-274">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="976ab-274">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="976ab-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="976ab-275">Windows Server 2012</span></span>



| <span data-ttu-id="976ab-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="976ab-276">Entry</span></span> | <span data-ttu-id="976ab-277">Value</span><span class="sxs-lookup"><span data-stu-id="976ab-277">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="976ab-278">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="976ab-278">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="976ab-279">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="976ab-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="976ab-280">System-Only</span></span>            | <span data-ttu-id="976ab-281">True</span><span class="sxs-lookup"><span data-stu-id="976ab-281">True</span></span>                            |
| <span data-ttu-id="976ab-282">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="976ab-282">Is-Single-Valued</span></span>       | <span data-ttu-id="976ab-283">True</span><span class="sxs-lookup"><span data-stu-id="976ab-283">True</span></span>                            |
| <span data-ttu-id="976ab-284">Está indexado</span><span class="sxs-lookup"><span data-stu-id="976ab-284">Is Indexed</span></span>             | <span data-ttu-id="976ab-285">False</span><span class="sxs-lookup"><span data-stu-id="976ab-285">False</span></span>                           |
| <span data-ttu-id="976ab-286">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="976ab-286">In Global Catalog</span></span>      | <span data-ttu-id="976ab-287">True</span><span class="sxs-lookup"><span data-stu-id="976ab-287">True</span></span>                            |
| <span data-ttu-id="976ab-288">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="976ab-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="976ab-289">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="976ab-289">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="976ab-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="976ab-290">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="976ab-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="976ab-291">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="976ab-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-292">Search-Flags</span></span>           | <span data-ttu-id="976ab-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="976ab-293">0x00000000</span></span>                      |
| <span data-ttu-id="976ab-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="976ab-294">System-Flags</span></span>           | <span data-ttu-id="976ab-295">0x00000013</span><span class="sxs-lookup"><span data-stu-id="976ab-295">0x00000013</span></span>                      |
| <span data-ttu-id="976ab-296">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="976ab-296">Classes used in</span></span>        | [<span data-ttu-id="976ab-297">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="976ab-297">**Top**</span></span>](c-top.md)<br/> |



 

 






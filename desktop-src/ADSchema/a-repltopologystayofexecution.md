---
title: REPL-topología-mantener el atributo de ejecución
description: Retraso entre la eliminación de un objeto de servidor y su eliminación permanente de la topología de replicación.
ms.assetid: 770231b0-4886-41c2-a3b5-ac488ac09669
ms.tgt_platform: multiple
keywords:
- 'REPL-topología: esquema de AD de atributo de permanencia de ejecución'
- replTopologyStayOfExecution esquema de AD de atributos
topic_type:
- apiref
api_name:
- Repl-Topology-Stay-Of-Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51c74c477cce926dd18ea17b8df2b1adcf99df1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804567"
---
# <a name="repl-topology-stay-of-execution-attribute"></a><span data-ttu-id="5b66a-105">REPL-topología-mantener el atributo de ejecución</span><span class="sxs-lookup"><span data-stu-id="5b66a-105">Repl-Topology-Stay-Of-Execution attribute</span></span>

<span data-ttu-id="5b66a-106">Retraso entre la eliminación de un objeto de servidor y su eliminación permanente de la topología de replicación.</span><span class="sxs-lookup"><span data-stu-id="5b66a-106">The delay between deleting a server object and it being permanently removed from the replication topology.</span></span>



| <span data-ttu-id="5b66a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b66a-107">Entry</span></span> | <span data-ttu-id="5b66a-108">Value</span><span class="sxs-lookup"><span data-stu-id="5b66a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5b66a-109">CN</span><span class="sxs-lookup"><span data-stu-id="5b66a-109">CN</span></span>                | <span data-ttu-id="5b66a-110">REPL-topología-permanencia de ejecución</span><span class="sxs-lookup"><span data-stu-id="5b66a-110">Repl-Topology-Stay-Of-Execution</span></span>      |
| <span data-ttu-id="5b66a-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5b66a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5b66a-112">replTopologyStayOfExecution</span><span class="sxs-lookup"><span data-stu-id="5b66a-112">replTopologyStayOfExecution</span></span>          |
| <span data-ttu-id="5b66a-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5b66a-113">Size</span></span>              | <span data-ttu-id="5b66a-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="5b66a-114">4 bytes</span></span>                              |
| <span data-ttu-id="5b66a-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5b66a-115">Update Privilege</span></span>  | <span data-ttu-id="5b66a-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="5b66a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="5b66a-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5b66a-117">Update Frequency</span></span>  | <span data-ttu-id="5b66a-118">Cada vez que se elimina un objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="5b66a-118">Whenever a server object is deleted.</span></span> |
| <span data-ttu-id="5b66a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5b66a-119">Attribute-Id</span></span>      | <span data-ttu-id="5b66a-120">1.2.840.113556.1.4.677</span><span class="sxs-lookup"><span data-stu-id="5b66a-120">1.2.840.113556.1.4.677</span></span>               |
| <span data-ttu-id="5b66a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5b66a-121">System-Id-Guid</span></span>    | <span data-ttu-id="5b66a-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5b66a-122">7bfdcb83-4807-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="5b66a-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b66a-123">Syntax</span></span>            | [<span data-ttu-id="5b66a-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="5b66a-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="5b66a-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5b66a-125">Implementations</span></span>

-   [<span data-ttu-id="5b66a-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5b66a-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5b66a-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5b66a-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5b66a-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5b66a-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5b66a-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5b66a-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5b66a-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5b66a-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5b66a-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5b66a-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5b66a-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5b66a-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5b66a-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b66a-133">Windows 2000 Server</span></span>



| <span data-ttu-id="5b66a-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b66a-134">Entry</span></span> | <span data-ttu-id="5b66a-135">Value</span><span class="sxs-lookup"><span data-stu-id="5b66a-135">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5b66a-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5b66a-136">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b66a-137">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b66a-138">System-Only</span></span>            | <span data-ttu-id="5b66a-139">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-139">False</span></span>                                            |
| <span data-ttu-id="5b66a-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5b66a-140">Is-Single-Valued</span></span>       | <span data-ttu-id="5b66a-141">True</span><span class="sxs-lookup"><span data-stu-id="5b66a-141">True</span></span>                                             |
| <span data-ttu-id="5b66a-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5b66a-142">Is Indexed</span></span>             | <span data-ttu-id="5b66a-143">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-143">False</span></span>                                            |
| <span data-ttu-id="5b66a-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5b66a-144">In Global Catalog</span></span>      | <span data-ttu-id="5b66a-145">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-145">False</span></span>                                            |
| <span data-ttu-id="5b66a-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5b66a-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b66a-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b66a-147">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5b66a-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b66a-148">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b66a-149">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-150">Search-Flags</span></span>           | <span data-ttu-id="5b66a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b66a-151">0x00000000</span></span>                                       |
| <span data-ttu-id="5b66a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-152">System-Flags</span></span>           | <span data-ttu-id="5b66a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b66a-153">0x00000010</span></span>                                       |
| <span data-ttu-id="5b66a-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5b66a-154">Classes used in</span></span>        | [<span data-ttu-id="5b66a-155">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="5b66a-155">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5b66a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5b66a-156">Windows Server 2003</span></span>



| <span data-ttu-id="5b66a-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b66a-157">Entry</span></span> | <span data-ttu-id="5b66a-158">Value</span><span class="sxs-lookup"><span data-stu-id="5b66a-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5b66a-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5b66a-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b66a-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b66a-161">System-Only</span></span>            | <span data-ttu-id="5b66a-162">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-162">False</span></span>                                            |
| <span data-ttu-id="5b66a-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5b66a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="5b66a-164">True</span><span class="sxs-lookup"><span data-stu-id="5b66a-164">True</span></span>                                             |
| <span data-ttu-id="5b66a-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5b66a-165">Is Indexed</span></span>             | <span data-ttu-id="5b66a-166">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-166">False</span></span>                                            |
| <span data-ttu-id="5b66a-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5b66a-167">In Global Catalog</span></span>      | <span data-ttu-id="5b66a-168">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-168">False</span></span>                                            |
| <span data-ttu-id="5b66a-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5b66a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b66a-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b66a-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5b66a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b66a-171">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b66a-172">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-173">Search-Flags</span></span>           | <span data-ttu-id="5b66a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b66a-174">0x00000000</span></span>                                       |
| <span data-ttu-id="5b66a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-175">System-Flags</span></span>           | <span data-ttu-id="5b66a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b66a-176">0x00000010</span></span>                                       |
| <span data-ttu-id="5b66a-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5b66a-177">Classes used in</span></span>        | [<span data-ttu-id="5b66a-178">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="5b66a-178">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5b66a-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="5b66a-179">ADAM</span></span>



| <span data-ttu-id="5b66a-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b66a-180">Entry</span></span> | <span data-ttu-id="5b66a-181">Value</span><span class="sxs-lookup"><span data-stu-id="5b66a-181">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5b66a-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5b66a-182">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b66a-183">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b66a-184">System-Only</span></span>            | <span data-ttu-id="5b66a-185">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-185">False</span></span>                                            |
| <span data-ttu-id="5b66a-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5b66a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5b66a-187">True</span><span class="sxs-lookup"><span data-stu-id="5b66a-187">True</span></span>                                             |
| <span data-ttu-id="5b66a-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5b66a-188">Is Indexed</span></span>             | <span data-ttu-id="5b66a-189">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-189">False</span></span>                                            |
| <span data-ttu-id="5b66a-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5b66a-190">In Global Catalog</span></span>      | <span data-ttu-id="5b66a-191">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-191">False</span></span>                                            |
| <span data-ttu-id="5b66a-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5b66a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b66a-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b66a-193">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5b66a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b66a-194">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b66a-195">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-196">Search-Flags</span></span>           | <span data-ttu-id="5b66a-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b66a-197">0x00000000</span></span>                                       |
| <span data-ttu-id="5b66a-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-198">System-Flags</span></span>           | <span data-ttu-id="5b66a-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b66a-199">0x00000010</span></span>                                       |
| <span data-ttu-id="5b66a-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5b66a-200">Classes used in</span></span>        | [<span data-ttu-id="5b66a-201">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="5b66a-201">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5b66a-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5b66a-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5b66a-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b66a-203">Entry</span></span> | <span data-ttu-id="5b66a-204">Value</span><span class="sxs-lookup"><span data-stu-id="5b66a-204">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5b66a-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5b66a-205">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b66a-206">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b66a-207">System-Only</span></span>            | <span data-ttu-id="5b66a-208">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-208">False</span></span>                                            |
| <span data-ttu-id="5b66a-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5b66a-209">Is-Single-Valued</span></span>       | <span data-ttu-id="5b66a-210">True</span><span class="sxs-lookup"><span data-stu-id="5b66a-210">True</span></span>                                             |
| <span data-ttu-id="5b66a-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5b66a-211">Is Indexed</span></span>             | <span data-ttu-id="5b66a-212">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-212">False</span></span>                                            |
| <span data-ttu-id="5b66a-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5b66a-213">In Global Catalog</span></span>      | <span data-ttu-id="5b66a-214">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-214">False</span></span>                                            |
| <span data-ttu-id="5b66a-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5b66a-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b66a-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b66a-216">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5b66a-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b66a-217">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b66a-218">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-219">Search-Flags</span></span>           | <span data-ttu-id="5b66a-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b66a-220">0x00000000</span></span>                                       |
| <span data-ttu-id="5b66a-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-221">System-Flags</span></span>           | <span data-ttu-id="5b66a-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b66a-222">0x00000010</span></span>                                       |
| <span data-ttu-id="5b66a-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5b66a-223">Classes used in</span></span>        | [<span data-ttu-id="5b66a-224">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="5b66a-224">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5b66a-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b66a-225">Windows Server 2008</span></span>



| <span data-ttu-id="5b66a-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b66a-226">Entry</span></span> | <span data-ttu-id="5b66a-227">Value</span><span class="sxs-lookup"><span data-stu-id="5b66a-227">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5b66a-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5b66a-228">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b66a-229">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b66a-230">System-Only</span></span>            | <span data-ttu-id="5b66a-231">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-231">False</span></span>                                            |
| <span data-ttu-id="5b66a-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5b66a-232">Is-Single-Valued</span></span>       | <span data-ttu-id="5b66a-233">True</span><span class="sxs-lookup"><span data-stu-id="5b66a-233">True</span></span>                                             |
| <span data-ttu-id="5b66a-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5b66a-234">Is Indexed</span></span>             | <span data-ttu-id="5b66a-235">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-235">False</span></span>                                            |
| <span data-ttu-id="5b66a-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5b66a-236">In Global Catalog</span></span>      | <span data-ttu-id="5b66a-237">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-237">False</span></span>                                            |
| <span data-ttu-id="5b66a-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5b66a-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b66a-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b66a-239">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5b66a-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b66a-240">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b66a-241">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-242">Search-Flags</span></span>           | <span data-ttu-id="5b66a-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b66a-243">0x00000000</span></span>                                       |
| <span data-ttu-id="5b66a-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-244">System-Flags</span></span>           | <span data-ttu-id="5b66a-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b66a-245">0x00000010</span></span>                                       |
| <span data-ttu-id="5b66a-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5b66a-246">Classes used in</span></span>        | [<span data-ttu-id="5b66a-247">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="5b66a-247">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5b66a-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5b66a-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5b66a-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b66a-249">Entry</span></span> | <span data-ttu-id="5b66a-250">Value</span><span class="sxs-lookup"><span data-stu-id="5b66a-250">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5b66a-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5b66a-251">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b66a-252">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b66a-253">System-Only</span></span>            | <span data-ttu-id="5b66a-254">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-254">False</span></span>                                            |
| <span data-ttu-id="5b66a-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5b66a-255">Is-Single-Valued</span></span>       | <span data-ttu-id="5b66a-256">True</span><span class="sxs-lookup"><span data-stu-id="5b66a-256">True</span></span>                                             |
| <span data-ttu-id="5b66a-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5b66a-257">Is Indexed</span></span>             | <span data-ttu-id="5b66a-258">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-258">False</span></span>                                            |
| <span data-ttu-id="5b66a-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5b66a-259">In Global Catalog</span></span>      | <span data-ttu-id="5b66a-260">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-260">False</span></span>                                            |
| <span data-ttu-id="5b66a-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5b66a-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b66a-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b66a-262">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5b66a-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b66a-263">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b66a-264">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-265">Search-Flags</span></span>           | <span data-ttu-id="5b66a-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b66a-266">0x00000000</span></span>                                       |
| <span data-ttu-id="5b66a-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-267">System-Flags</span></span>           | <span data-ttu-id="5b66a-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b66a-268">0x00000010</span></span>                                       |
| <span data-ttu-id="5b66a-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5b66a-269">Classes used in</span></span>        | [<span data-ttu-id="5b66a-270">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="5b66a-270">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5b66a-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b66a-271">Windows Server 2012</span></span>



| <span data-ttu-id="5b66a-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b66a-272">Entry</span></span> | <span data-ttu-id="5b66a-273">Value</span><span class="sxs-lookup"><span data-stu-id="5b66a-273">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5b66a-274">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5b66a-274">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b66a-275">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5b66a-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b66a-276">System-Only</span></span>            | <span data-ttu-id="5b66a-277">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-277">False</span></span>                                            |
| <span data-ttu-id="5b66a-278">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5b66a-278">Is-Single-Valued</span></span>       | <span data-ttu-id="5b66a-279">True</span><span class="sxs-lookup"><span data-stu-id="5b66a-279">True</span></span>                                             |
| <span data-ttu-id="5b66a-280">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5b66a-280">Is Indexed</span></span>             | <span data-ttu-id="5b66a-281">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-281">False</span></span>                                            |
| <span data-ttu-id="5b66a-282">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5b66a-282">In Global Catalog</span></span>      | <span data-ttu-id="5b66a-283">False</span><span class="sxs-lookup"><span data-stu-id="5b66a-283">False</span></span>                                            |
| <span data-ttu-id="5b66a-284">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5b66a-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b66a-285">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b66a-285">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5b66a-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b66a-286">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b66a-287">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5b66a-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-288">Search-Flags</span></span>           | <span data-ttu-id="5b66a-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b66a-289">0x00000000</span></span>                                       |
| <span data-ttu-id="5b66a-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b66a-290">System-Flags</span></span>           | <span data-ttu-id="5b66a-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b66a-291">0x00000010</span></span>                                       |
| <span data-ttu-id="5b66a-292">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5b66a-292">Classes used in</span></span>        | [<span data-ttu-id="5b66a-293">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="5b66a-293">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 






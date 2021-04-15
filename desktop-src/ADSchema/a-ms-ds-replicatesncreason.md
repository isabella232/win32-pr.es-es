---
title: Atributo MS-DS-Replications-NC-Reason
description: Atributo del objeto ntdsConnection que indica por qué (o si) el KCC muestra que la conexión es útil en la topología de replicación. Tiene varios valores y tiene DistName + sintaxis binaria, donde la parte binaria es un campo de bits de tamaño int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-Replications-NC-Reason
- Esquema de AD del atributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422653"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a><span data-ttu-id="a7509-106">Atributo MS-DS-Replications-NC-Reason</span><span class="sxs-lookup"><span data-stu-id="a7509-106">MS-DS-Replicates-NC-Reason attribute</span></span>

<span data-ttu-id="a7509-107">Atributo del objeto ntdsConnection que indica por qué (o si) el KCC muestra que la conexión es útil en la topología de replicación.</span><span class="sxs-lookup"><span data-stu-id="a7509-107">Attribute of ntdsConnection object that indicates why (or whether) the KCC shows the connection is useful in the replication topology.</span></span> <span data-ttu-id="a7509-108">Tiene varios valores y tiene DistName + sintaxis binaria, donde la parte binaria es un campo de bits de tamaño int.</span><span class="sxs-lookup"><span data-stu-id="a7509-108">Is multiple-valued and has DistName+Binary syntax, where the binary part is an int-size bitfield.</span></span>



| <span data-ttu-id="a7509-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7509-109">Entry</span></span> | <span data-ttu-id="a7509-110">Value</span><span class="sxs-lookup"><span data-stu-id="a7509-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7509-111">CN</span><span class="sxs-lookup"><span data-stu-id="a7509-111">CN</span></span>                | <span data-ttu-id="a7509-112">MS-DS-Replications-NC-motivo</span><span class="sxs-lookup"><span data-stu-id="a7509-112">MS-DS-Replicates-NC-Reason</span></span>                                                                                                                 |
| <span data-ttu-id="a7509-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a7509-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a7509-114">mS-DS-ReplicatesNCReason</span><span class="sxs-lookup"><span data-stu-id="a7509-114">mS-DS-ReplicatesNCReason</span></span>                                                                                                                   |
| <span data-ttu-id="a7509-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a7509-115">Size</span></span>              | <span data-ttu-id="a7509-116">Valor de la parte binaria: 0 = sin \_ motivo, 1 = topología de GC \_ , 2 = topología en anillo \_ , 4 = minimizar la \_ \_ topología de saltos, 8 = topología de servidores obsoletos \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a7509-116">Value for binary portion: 0 = NO\_REASON,1 = GC\_TOPOLOGY, 2 = RING\_TOPOLOGY, 4 = MINIMIZE\_HOPS\_TOPOLOGY, 8 = STALE\_SERVERS\_TOPOLOGY.</span></span> |
| <span data-ttu-id="a7509-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a7509-117">Update Privilege</span></span>  | <span data-ttu-id="a7509-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a7509-118">This value is set by the system.</span></span>                                                                                                           |
| <span data-ttu-id="a7509-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a7509-119">Update Frequency</span></span>  | <span data-ttu-id="a7509-120">Puede cambiar en respuesta a los cambios en la topología de red.</span><span class="sxs-lookup"><span data-stu-id="a7509-120">Can change in response to changes in the network topology.</span></span>                                                                                 |
| <span data-ttu-id="a7509-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a7509-121">Attribute-Id</span></span>      | <span data-ttu-id="a7509-122">1.2.840.113556.1.4.1408</span><span class="sxs-lookup"><span data-stu-id="a7509-122">1.2.840.113556.1.4.1408</span></span>                                                                                                                    |
| <span data-ttu-id="a7509-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a7509-123">System-Id-Guid</span></span>    | <span data-ttu-id="a7509-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="a7509-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span></span>                                                                                                       |
| <span data-ttu-id="a7509-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7509-125">Syntax</span></span>            | [<span data-ttu-id="a7509-126">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="a7509-126">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a><span data-ttu-id="a7509-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a7509-127">Implementations</span></span>

-   [<span data-ttu-id="a7509-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a7509-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a7509-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a7509-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a7509-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a7509-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a7509-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a7509-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a7509-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a7509-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a7509-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a7509-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a7509-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a7509-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a7509-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7509-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a7509-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7509-136">Entry</span></span> | <span data-ttu-id="a7509-137">Value</span><span class="sxs-lookup"><span data-stu-id="a7509-137">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="a7509-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a7509-138">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7509-139">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7509-140">System-Only</span></span>            | <span data-ttu-id="a7509-141">False</span><span class="sxs-lookup"><span data-stu-id="a7509-141">False</span></span>                                                  |
| <span data-ttu-id="a7509-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a7509-142">Is-Single-Valued</span></span>       | <span data-ttu-id="a7509-143">False</span><span class="sxs-lookup"><span data-stu-id="a7509-143">False</span></span>                                                  |
| <span data-ttu-id="a7509-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a7509-144">Is Indexed</span></span>             | <span data-ttu-id="a7509-145">False</span><span class="sxs-lookup"><span data-stu-id="a7509-145">False</span></span>                                                  |
| <span data-ttu-id="a7509-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7509-146">In Global Catalog</span></span>      | <span data-ttu-id="a7509-147">False</span><span class="sxs-lookup"><span data-stu-id="a7509-147">False</span></span>                                                  |
| <span data-ttu-id="a7509-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a7509-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7509-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7509-149">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="a7509-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7509-150">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7509-151">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-152">Search-Flags</span></span>           | <span data-ttu-id="a7509-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7509-153">0x00000000</span></span>                                             |
| <span data-ttu-id="a7509-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-154">System-Flags</span></span>           | <span data-ttu-id="a7509-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7509-155">0x00000010</span></span>                                             |
| <span data-ttu-id="a7509-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a7509-156">Classes used in</span></span>        | [<span data-ttu-id="a7509-157">**NTDS-conexión**</span><span class="sxs-lookup"><span data-stu-id="a7509-157">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a7509-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7509-158">Windows Server 2003</span></span>



| <span data-ttu-id="a7509-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7509-159">Entry</span></span> | <span data-ttu-id="a7509-160">Value</span><span class="sxs-lookup"><span data-stu-id="a7509-160">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="a7509-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a7509-161">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7509-162">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7509-163">System-Only</span></span>            | <span data-ttu-id="a7509-164">False</span><span class="sxs-lookup"><span data-stu-id="a7509-164">False</span></span>                                                  |
| <span data-ttu-id="a7509-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a7509-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a7509-166">False</span><span class="sxs-lookup"><span data-stu-id="a7509-166">False</span></span>                                                  |
| <span data-ttu-id="a7509-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a7509-167">Is Indexed</span></span>             | <span data-ttu-id="a7509-168">False</span><span class="sxs-lookup"><span data-stu-id="a7509-168">False</span></span>                                                  |
| <span data-ttu-id="a7509-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7509-169">In Global Catalog</span></span>      | <span data-ttu-id="a7509-170">False</span><span class="sxs-lookup"><span data-stu-id="a7509-170">False</span></span>                                                  |
| <span data-ttu-id="a7509-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a7509-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7509-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7509-172">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="a7509-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7509-173">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7509-174">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-175">Search-Flags</span></span>           | <span data-ttu-id="a7509-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7509-176">0x00000000</span></span>                                             |
| <span data-ttu-id="a7509-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-177">System-Flags</span></span>           | <span data-ttu-id="a7509-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7509-178">0x00000010</span></span>                                             |
| <span data-ttu-id="a7509-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a7509-179">Classes used in</span></span>        | [<span data-ttu-id="a7509-180">**NTDS-conexión**</span><span class="sxs-lookup"><span data-stu-id="a7509-180">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a7509-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="a7509-181">ADAM</span></span>



| <span data-ttu-id="a7509-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7509-182">Entry</span></span> | <span data-ttu-id="a7509-183">Value</span><span class="sxs-lookup"><span data-stu-id="a7509-183">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="a7509-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a7509-184">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7509-185">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7509-186">System-Only</span></span>            | <span data-ttu-id="a7509-187">False</span><span class="sxs-lookup"><span data-stu-id="a7509-187">False</span></span>                                                  |
| <span data-ttu-id="a7509-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a7509-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a7509-189">False</span><span class="sxs-lookup"><span data-stu-id="a7509-189">False</span></span>                                                  |
| <span data-ttu-id="a7509-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a7509-190">Is Indexed</span></span>             | <span data-ttu-id="a7509-191">False</span><span class="sxs-lookup"><span data-stu-id="a7509-191">False</span></span>                                                  |
| <span data-ttu-id="a7509-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7509-192">In Global Catalog</span></span>      | <span data-ttu-id="a7509-193">False</span><span class="sxs-lookup"><span data-stu-id="a7509-193">False</span></span>                                                  |
| <span data-ttu-id="a7509-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a7509-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7509-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7509-195">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="a7509-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7509-196">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7509-197">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-198">Search-Flags</span></span>           | <span data-ttu-id="a7509-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7509-199">0x00000000</span></span>                                             |
| <span data-ttu-id="a7509-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-200">System-Flags</span></span>           | <span data-ttu-id="a7509-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7509-201">0x00000010</span></span>                                             |
| <span data-ttu-id="a7509-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a7509-202">Classes used in</span></span>        | [<span data-ttu-id="a7509-203">**NTDS-conexión**</span><span class="sxs-lookup"><span data-stu-id="a7509-203">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a7509-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a7509-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a7509-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7509-205">Entry</span></span> | <span data-ttu-id="a7509-206">Value</span><span class="sxs-lookup"><span data-stu-id="a7509-206">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="a7509-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a7509-207">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7509-208">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7509-209">System-Only</span></span>            | <span data-ttu-id="a7509-210">False</span><span class="sxs-lookup"><span data-stu-id="a7509-210">False</span></span>                                                  |
| <span data-ttu-id="a7509-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a7509-211">Is-Single-Valued</span></span>       | <span data-ttu-id="a7509-212">False</span><span class="sxs-lookup"><span data-stu-id="a7509-212">False</span></span>                                                  |
| <span data-ttu-id="a7509-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a7509-213">Is Indexed</span></span>             | <span data-ttu-id="a7509-214">False</span><span class="sxs-lookup"><span data-stu-id="a7509-214">False</span></span>                                                  |
| <span data-ttu-id="a7509-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7509-215">In Global Catalog</span></span>      | <span data-ttu-id="a7509-216">False</span><span class="sxs-lookup"><span data-stu-id="a7509-216">False</span></span>                                                  |
| <span data-ttu-id="a7509-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a7509-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7509-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7509-218">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="a7509-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7509-219">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7509-220">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-221">Search-Flags</span></span>           | <span data-ttu-id="a7509-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7509-222">0x00000000</span></span>                                             |
| <span data-ttu-id="a7509-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-223">System-Flags</span></span>           | <span data-ttu-id="a7509-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7509-224">0x00000010</span></span>                                             |
| <span data-ttu-id="a7509-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a7509-225">Classes used in</span></span>        | [<span data-ttu-id="a7509-226">**NTDS-conexión**</span><span class="sxs-lookup"><span data-stu-id="a7509-226">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a7509-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7509-227">Windows Server 2008</span></span>



| <span data-ttu-id="a7509-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7509-228">Entry</span></span> | <span data-ttu-id="a7509-229">Value</span><span class="sxs-lookup"><span data-stu-id="a7509-229">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="a7509-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a7509-230">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7509-231">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7509-232">System-Only</span></span>            | <span data-ttu-id="a7509-233">False</span><span class="sxs-lookup"><span data-stu-id="a7509-233">False</span></span>                                                  |
| <span data-ttu-id="a7509-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a7509-234">Is-Single-Valued</span></span>       | <span data-ttu-id="a7509-235">False</span><span class="sxs-lookup"><span data-stu-id="a7509-235">False</span></span>                                                  |
| <span data-ttu-id="a7509-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a7509-236">Is Indexed</span></span>             | <span data-ttu-id="a7509-237">False</span><span class="sxs-lookup"><span data-stu-id="a7509-237">False</span></span>                                                  |
| <span data-ttu-id="a7509-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7509-238">In Global Catalog</span></span>      | <span data-ttu-id="a7509-239">False</span><span class="sxs-lookup"><span data-stu-id="a7509-239">False</span></span>                                                  |
| <span data-ttu-id="a7509-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a7509-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7509-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7509-241">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="a7509-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7509-242">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7509-243">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-244">Search-Flags</span></span>           | <span data-ttu-id="a7509-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7509-245">0x00000000</span></span>                                             |
| <span data-ttu-id="a7509-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-246">System-Flags</span></span>           | <span data-ttu-id="a7509-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7509-247">0x00000010</span></span>                                             |
| <span data-ttu-id="a7509-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a7509-248">Classes used in</span></span>        | [<span data-ttu-id="a7509-249">**NTDS-conexión**</span><span class="sxs-lookup"><span data-stu-id="a7509-249">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a7509-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7509-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a7509-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7509-251">Entry</span></span> | <span data-ttu-id="a7509-252">Value</span><span class="sxs-lookup"><span data-stu-id="a7509-252">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="a7509-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a7509-253">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7509-254">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7509-255">System-Only</span></span>            | <span data-ttu-id="a7509-256">False</span><span class="sxs-lookup"><span data-stu-id="a7509-256">False</span></span>                                                  |
| <span data-ttu-id="a7509-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a7509-257">Is-Single-Valued</span></span>       | <span data-ttu-id="a7509-258">False</span><span class="sxs-lookup"><span data-stu-id="a7509-258">False</span></span>                                                  |
| <span data-ttu-id="a7509-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a7509-259">Is Indexed</span></span>             | <span data-ttu-id="a7509-260">False</span><span class="sxs-lookup"><span data-stu-id="a7509-260">False</span></span>                                                  |
| <span data-ttu-id="a7509-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7509-261">In Global Catalog</span></span>      | <span data-ttu-id="a7509-262">False</span><span class="sxs-lookup"><span data-stu-id="a7509-262">False</span></span>                                                  |
| <span data-ttu-id="a7509-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a7509-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7509-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7509-264">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="a7509-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7509-265">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7509-266">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-267">Search-Flags</span></span>           | <span data-ttu-id="a7509-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7509-268">0x00000000</span></span>                                             |
| <span data-ttu-id="a7509-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-269">System-Flags</span></span>           | <span data-ttu-id="a7509-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7509-270">0x00000010</span></span>                                             |
| <span data-ttu-id="a7509-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a7509-271">Classes used in</span></span>        | [<span data-ttu-id="a7509-272">**NTDS-conexión**</span><span class="sxs-lookup"><span data-stu-id="a7509-272">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a7509-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7509-273">Windows Server 2012</span></span>



| <span data-ttu-id="a7509-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7509-274">Entry</span></span> | <span data-ttu-id="a7509-275">Value</span><span class="sxs-lookup"><span data-stu-id="a7509-275">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="a7509-276">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a7509-276">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7509-277">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="a7509-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7509-278">System-Only</span></span>            | <span data-ttu-id="a7509-279">False</span><span class="sxs-lookup"><span data-stu-id="a7509-279">False</span></span>                                                  |
| <span data-ttu-id="a7509-280">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a7509-280">Is-Single-Valued</span></span>       | <span data-ttu-id="a7509-281">False</span><span class="sxs-lookup"><span data-stu-id="a7509-281">False</span></span>                                                  |
| <span data-ttu-id="a7509-282">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a7509-282">Is Indexed</span></span>             | <span data-ttu-id="a7509-283">False</span><span class="sxs-lookup"><span data-stu-id="a7509-283">False</span></span>                                                  |
| <span data-ttu-id="a7509-284">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a7509-284">In Global Catalog</span></span>      | <span data-ttu-id="a7509-285">False</span><span class="sxs-lookup"><span data-stu-id="a7509-285">False</span></span>                                                  |
| <span data-ttu-id="a7509-286">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a7509-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7509-287">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7509-287">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="a7509-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7509-288">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7509-289">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="a7509-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-290">Search-Flags</span></span>           | <span data-ttu-id="a7509-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7509-291">0x00000000</span></span>                                             |
| <span data-ttu-id="a7509-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7509-292">System-Flags</span></span>           | <span data-ttu-id="a7509-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7509-293">0x00000010</span></span>                                             |
| <span data-ttu-id="a7509-294">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a7509-294">Classes used in</span></span>        | [<span data-ttu-id="a7509-295">**NTDS-conexión**</span><span class="sxs-lookup"><span data-stu-id="a7509-295">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 






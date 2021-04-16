---
title: atributo MS-FRS-Hub-Member
description: El atributo MS-FRS-Hub-Member se usa para registrar la configuración de topología de NTFRS preferida.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-FRS-Hub-Member
- 'msFRS-Hub: esquema de AD de atributos de miembro'
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658846"
---
# <a name="ms-frs-hub-member-attribute"></a><span data-ttu-id="334f2-105">atributo MS-FRS-Hub-Member</span><span class="sxs-lookup"><span data-stu-id="334f2-105">ms-FRS-Hub-Member attribute</span></span>

<span data-ttu-id="334f2-106">El atributo **MS-FRS-Hub-Member** se usa para registrar la configuración de topología de NTFRS preferida.</span><span class="sxs-lookup"><span data-stu-id="334f2-106">The **ms-FRS-Hub-Member** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="334f2-107">Cuando se agrega o se elimina un miembro de FRS en un conjunto de réplicas, se hace referencia a estos atributos y se realizan los ajustes adecuados en las conexiones entre el resto de los miembros FRS del conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="334f2-107">When an FRS member gets added or deleted to a replica set, these attributes are referred and appropriate adjustments are made to the connections between the rest of the FRS members in the replica set.</span></span>



| <span data-ttu-id="334f2-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="334f2-108">Entry</span></span> | <span data-ttu-id="334f2-109">Value</span><span class="sxs-lookup"><span data-stu-id="334f2-109">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="334f2-110">CN</span><span class="sxs-lookup"><span data-stu-id="334f2-110">CN</span></span>                | <span data-ttu-id="334f2-111">Miembro de centro de MS-FRS</span><span class="sxs-lookup"><span data-stu-id="334f2-111">ms-FRS-Hub-Member</span></span>                                                  |
| <span data-ttu-id="334f2-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="334f2-112">Ldap-Display-Name</span></span> | <span data-ttu-id="334f2-113">msFRS: miembro central</span><span class="sxs-lookup"><span data-stu-id="334f2-113">msFRS-Hub-Member</span></span>                                                   |
| <span data-ttu-id="334f2-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="334f2-114">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="334f2-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="334f2-115">Update Privilege</span></span>  | <span data-ttu-id="334f2-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="334f2-116">Domain administrator</span></span>                                               |
| <span data-ttu-id="334f2-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="334f2-117">Update Frequency</span></span>  | <span data-ttu-id="334f2-118">Cuando se crea el conjunto de réplicas o se cambia la topología preferida.</span><span class="sxs-lookup"><span data-stu-id="334f2-118">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="334f2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="334f2-119">Attribute-Id</span></span>      | <span data-ttu-id="334f2-120">1.2.840.113556.1.4.1693</span><span class="sxs-lookup"><span data-stu-id="334f2-120">1.2.840.113556.1.4.1693</span></span>                                            |
| <span data-ttu-id="334f2-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="334f2-121">System-Id-Guid</span></span>    | <span data-ttu-id="334f2-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span><span class="sxs-lookup"><span data-stu-id="334f2-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span></span>                               |
| <span data-ttu-id="334f2-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="334f2-123">Syntax</span></span>            | [<span data-ttu-id="334f2-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="334f2-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                            |



## <a name="implementations"></a><span data-ttu-id="334f2-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="334f2-125">Implementations</span></span>

-   [<span data-ttu-id="334f2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="334f2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="334f2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="334f2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="334f2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="334f2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="334f2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="334f2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="334f2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="334f2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="334f2-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="334f2-131">Windows Server 2003</span></span>



| <span data-ttu-id="334f2-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="334f2-132">Entry</span></span> | <span data-ttu-id="334f2-133">Value</span><span class="sxs-lookup"><span data-stu-id="334f2-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="334f2-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="334f2-134">Link-Id</span></span>                | <span data-ttu-id="334f2-135">1046</span><span class="sxs-lookup"><span data-stu-id="334f2-135">1046</span></span>                                                      |
| <span data-ttu-id="334f2-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="334f2-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="334f2-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="334f2-137">System-Only</span></span>            | <span data-ttu-id="334f2-138">False</span><span class="sxs-lookup"><span data-stu-id="334f2-138">False</span></span>                                                     |
| <span data-ttu-id="334f2-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="334f2-139">Is-Single-Valued</span></span>       | <span data-ttu-id="334f2-140">True</span><span class="sxs-lookup"><span data-stu-id="334f2-140">True</span></span>                                                      |
| <span data-ttu-id="334f2-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="334f2-141">Is Indexed</span></span>             | <span data-ttu-id="334f2-142">False</span><span class="sxs-lookup"><span data-stu-id="334f2-142">False</span></span>                                                     |
| <span data-ttu-id="334f2-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="334f2-143">In Global Catalog</span></span>      | <span data-ttu-id="334f2-144">False</span><span class="sxs-lookup"><span data-stu-id="334f2-144">False</span></span>                                                     |
| <span data-ttu-id="334f2-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="334f2-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="334f2-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="334f2-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="334f2-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="334f2-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="334f2-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-149">Search-Flags</span></span>           | <span data-ttu-id="334f2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-150">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-151">System-Flags</span></span>           | <span data-ttu-id="334f2-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-152">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="334f2-153">Classes used in</span></span>        | [<span data-ttu-id="334f2-154">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="334f2-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="334f2-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="334f2-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="334f2-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="334f2-156">Entry</span></span> | <span data-ttu-id="334f2-157">Value</span><span class="sxs-lookup"><span data-stu-id="334f2-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="334f2-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="334f2-158">Link-Id</span></span>                | <span data-ttu-id="334f2-159">1046</span><span class="sxs-lookup"><span data-stu-id="334f2-159">1046</span></span>                                                      |
| <span data-ttu-id="334f2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="334f2-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="334f2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="334f2-161">System-Only</span></span>            | <span data-ttu-id="334f2-162">False</span><span class="sxs-lookup"><span data-stu-id="334f2-162">False</span></span>                                                     |
| <span data-ttu-id="334f2-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="334f2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="334f2-164">True</span><span class="sxs-lookup"><span data-stu-id="334f2-164">True</span></span>                                                      |
| <span data-ttu-id="334f2-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="334f2-165">Is Indexed</span></span>             | <span data-ttu-id="334f2-166">False</span><span class="sxs-lookup"><span data-stu-id="334f2-166">False</span></span>                                                     |
| <span data-ttu-id="334f2-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="334f2-167">In Global Catalog</span></span>      | <span data-ttu-id="334f2-168">False</span><span class="sxs-lookup"><span data-stu-id="334f2-168">False</span></span>                                                     |
| <span data-ttu-id="334f2-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="334f2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="334f2-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="334f2-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="334f2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="334f2-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="334f2-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-173">Search-Flags</span></span>           | <span data-ttu-id="334f2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-174">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-175">System-Flags</span></span>           | <span data-ttu-id="334f2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-176">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="334f2-177">Classes used in</span></span>        | [<span data-ttu-id="334f2-178">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="334f2-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="334f2-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="334f2-179">Windows Server 2008</span></span>



| <span data-ttu-id="334f2-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="334f2-180">Entry</span></span> | <span data-ttu-id="334f2-181">Value</span><span class="sxs-lookup"><span data-stu-id="334f2-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="334f2-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="334f2-182">Link-Id</span></span>                | <span data-ttu-id="334f2-183">1046</span><span class="sxs-lookup"><span data-stu-id="334f2-183">1046</span></span>                                                      |
| <span data-ttu-id="334f2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="334f2-184">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="334f2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="334f2-185">System-Only</span></span>            | <span data-ttu-id="334f2-186">False</span><span class="sxs-lookup"><span data-stu-id="334f2-186">False</span></span>                                                     |
| <span data-ttu-id="334f2-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="334f2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="334f2-188">True</span><span class="sxs-lookup"><span data-stu-id="334f2-188">True</span></span>                                                      |
| <span data-ttu-id="334f2-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="334f2-189">Is Indexed</span></span>             | <span data-ttu-id="334f2-190">False</span><span class="sxs-lookup"><span data-stu-id="334f2-190">False</span></span>                                                     |
| <span data-ttu-id="334f2-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="334f2-191">In Global Catalog</span></span>      | <span data-ttu-id="334f2-192">False</span><span class="sxs-lookup"><span data-stu-id="334f2-192">False</span></span>                                                     |
| <span data-ttu-id="334f2-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="334f2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="334f2-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="334f2-194">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="334f2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="334f2-195">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="334f2-196">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-197">Search-Flags</span></span>           | <span data-ttu-id="334f2-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-198">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-199">System-Flags</span></span>           | <span data-ttu-id="334f2-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-200">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="334f2-201">Classes used in</span></span>        | [<span data-ttu-id="334f2-202">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="334f2-202">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="334f2-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="334f2-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="334f2-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="334f2-204">Entry</span></span> | <span data-ttu-id="334f2-205">Value</span><span class="sxs-lookup"><span data-stu-id="334f2-205">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="334f2-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="334f2-206">Link-Id</span></span>                | <span data-ttu-id="334f2-207">1046</span><span class="sxs-lookup"><span data-stu-id="334f2-207">1046</span></span>                                                      |
| <span data-ttu-id="334f2-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="334f2-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="334f2-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="334f2-209">System-Only</span></span>            | <span data-ttu-id="334f2-210">False</span><span class="sxs-lookup"><span data-stu-id="334f2-210">False</span></span>                                                     |
| <span data-ttu-id="334f2-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="334f2-211">Is-Single-Valued</span></span>       | <span data-ttu-id="334f2-212">True</span><span class="sxs-lookup"><span data-stu-id="334f2-212">True</span></span>                                                      |
| <span data-ttu-id="334f2-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="334f2-213">Is Indexed</span></span>             | <span data-ttu-id="334f2-214">False</span><span class="sxs-lookup"><span data-stu-id="334f2-214">False</span></span>                                                     |
| <span data-ttu-id="334f2-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="334f2-215">In Global Catalog</span></span>      | <span data-ttu-id="334f2-216">False</span><span class="sxs-lookup"><span data-stu-id="334f2-216">False</span></span>                                                     |
| <span data-ttu-id="334f2-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="334f2-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="334f2-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="334f2-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="334f2-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="334f2-219">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="334f2-220">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-221">Search-Flags</span></span>           | <span data-ttu-id="334f2-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-222">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-223">System-Flags</span></span>           | <span data-ttu-id="334f2-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-224">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="334f2-225">Classes used in</span></span>        | [<span data-ttu-id="334f2-226">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="334f2-226">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="334f2-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="334f2-227">Windows Server 2012</span></span>



| <span data-ttu-id="334f2-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="334f2-228">Entry</span></span> | <span data-ttu-id="334f2-229">Value</span><span class="sxs-lookup"><span data-stu-id="334f2-229">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="334f2-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="334f2-230">Link-Id</span></span>                | <span data-ttu-id="334f2-231">1046</span><span class="sxs-lookup"><span data-stu-id="334f2-231">1046</span></span>                                                      |
| <span data-ttu-id="334f2-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="334f2-232">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="334f2-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="334f2-233">System-Only</span></span>            | <span data-ttu-id="334f2-234">False</span><span class="sxs-lookup"><span data-stu-id="334f2-234">False</span></span>                                                     |
| <span data-ttu-id="334f2-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="334f2-235">Is-Single-Valued</span></span>       | <span data-ttu-id="334f2-236">True</span><span class="sxs-lookup"><span data-stu-id="334f2-236">True</span></span>                                                      |
| <span data-ttu-id="334f2-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="334f2-237">Is Indexed</span></span>             | <span data-ttu-id="334f2-238">False</span><span class="sxs-lookup"><span data-stu-id="334f2-238">False</span></span>                                                     |
| <span data-ttu-id="334f2-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="334f2-239">In Global Catalog</span></span>      | <span data-ttu-id="334f2-240">False</span><span class="sxs-lookup"><span data-stu-id="334f2-240">False</span></span>                                                     |
| <span data-ttu-id="334f2-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="334f2-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="334f2-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="334f2-242">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="334f2-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="334f2-243">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="334f2-244">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="334f2-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-245">Search-Flags</span></span>           | <span data-ttu-id="334f2-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-246">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="334f2-247">System-Flags</span></span>           | <span data-ttu-id="334f2-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="334f2-248">0x00000000</span></span>                                                |
| <span data-ttu-id="334f2-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="334f2-249">Classes used in</span></span>        | [<span data-ttu-id="334f2-250">**NTFRS-Replica-set**</span><span class="sxs-lookup"><span data-stu-id="334f2-250">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="334f2-251">Observaciones</span><span class="sxs-lookup"><span data-stu-id="334f2-251">Remarks</span></span>

<span data-ttu-id="334f2-252">Es el nombre distintivo completo de un objeto de [**NTFRS-Member**](c-ntfrsmember.md) .</span><span class="sxs-lookup"><span data-stu-id="334f2-252">This is the fully qualified distinguished name of an [**NTFRS-Member**](c-ntfrsmember.md) object.</span></span> <span data-ttu-id="334f2-253">El nombre distintivo está en el formato de "CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = volúmenes DFS, CN = servicio de replicación de archivos, CN = System, DC =..."</span><span class="sxs-lookup"><span data-stu-id="334f2-253">The distinguished name is in the format of "CN=*<computerGuid>*, CN=*<Dfs Link Name>*, CN=*<Dfs Root name>*, CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."</span></span>

 

 






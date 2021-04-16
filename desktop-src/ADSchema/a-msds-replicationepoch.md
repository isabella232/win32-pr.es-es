---
title: atributo MS-DS-ReplicationEpoch
description: Se usa para mantener la época en la que se replican todos los controladores de dominios. Una época es el período de tiempo en el que un dominio tiene un nombre específico. Un nuevo tiempo se inicia cuando se produce un cambio de nombre de dominio.
ms.assetid: d8a3c4fd-f416-483f-820f-7b3182d0bfc3
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-ReplicationEpoch
- Esquema de AD de atributo msDS-ReplicationEpoch
topic_type:
- apiref
api_name:
- ms-DS-ReplicationEpoch
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9aaefefe5cd1ae269508390ae13f67037fdb8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536004"
---
# <a name="ms-ds-replicationepoch-attribute"></a><span data-ttu-id="e538d-107">atributo MS-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="e538d-107">ms-DS-ReplicationEpoch attribute</span></span>

<span data-ttu-id="e538d-108">Se usa para mantener la época en la que se replican todos los controladores de dominios.</span><span class="sxs-lookup"><span data-stu-id="e538d-108">This is used to hold the epoch under which all the DCs are replicating.</span></span> <span data-ttu-id="e538d-109">Una época es el período de tiempo en el que un dominio tiene un nombre específico.</span><span class="sxs-lookup"><span data-stu-id="e538d-109">An epoch is the period of time in which a domain has a specific name.</span></span> <span data-ttu-id="e538d-110">Un nuevo tiempo se inicia cuando se produce un cambio de nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="e538d-110">A new epoch starts when a domain name change occurs.</span></span>



| <span data-ttu-id="e538d-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="e538d-111">Entry</span></span> | <span data-ttu-id="e538d-112">Value</span><span class="sxs-lookup"><span data-stu-id="e538d-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e538d-113">CN</span><span class="sxs-lookup"><span data-stu-id="e538d-113">CN</span></span>                | <span data-ttu-id="e538d-114">MS-DS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="e538d-114">ms-DS-ReplicationEpoch</span></span>               |
| <span data-ttu-id="e538d-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e538d-115">Ldap-Display-Name</span></span> | <span data-ttu-id="e538d-116">msDS-ReplicationEpoch</span><span class="sxs-lookup"><span data-stu-id="e538d-116">msDS-ReplicationEpoch</span></span>                |
| <span data-ttu-id="e538d-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e538d-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="e538d-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e538d-118">Update Privilege</span></span>  | <span data-ttu-id="e538d-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="e538d-119">This value is set by the system.</span></span>     |
| <span data-ttu-id="e538d-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e538d-120">Update Frequency</span></span>  | <span data-ttu-id="e538d-121">Solo durante la reestructuración de dominios.</span><span class="sxs-lookup"><span data-stu-id="e538d-121">Only during domain restructure.</span></span>      |
| <span data-ttu-id="e538d-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e538d-122">Attribute-Id</span></span>      | <span data-ttu-id="e538d-123">1.2.840.113556.1.4.1720</span><span class="sxs-lookup"><span data-stu-id="e538d-123">1.2.840.113556.1.4.1720</span></span>              |
| <span data-ttu-id="e538d-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e538d-124">System-Id-Guid</span></span>    | <span data-ttu-id="e538d-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span><span class="sxs-lookup"><span data-stu-id="e538d-125">08e3aa79-eb1c-45b5-af7b-8f94246c8e41</span></span> |
| <span data-ttu-id="e538d-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e538d-126">Syntax</span></span>            | [<span data-ttu-id="e538d-127">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="e538d-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e538d-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e538d-128">Implementations</span></span>

-   [<span data-ttu-id="e538d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e538d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e538d-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e538d-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e538d-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e538d-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e538d-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e538d-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e538d-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e538d-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e538d-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e538d-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e538d-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e538d-135">Windows Server 2003</span></span>



| <span data-ttu-id="e538d-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="e538d-136">Entry</span></span> | <span data-ttu-id="e538d-137">Value</span><span class="sxs-lookup"><span data-stu-id="e538d-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e538d-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e538d-138">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e538d-139">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="e538d-140">System-Only</span></span>            | <span data-ttu-id="e538d-141">False</span><span class="sxs-lookup"><span data-stu-id="e538d-141">False</span></span>                                    |
| <span data-ttu-id="e538d-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e538d-142">Is-Single-Valued</span></span>       | <span data-ttu-id="e538d-143">True</span><span class="sxs-lookup"><span data-stu-id="e538d-143">True</span></span>                                     |
| <span data-ttu-id="e538d-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e538d-144">Is Indexed</span></span>             | <span data-ttu-id="e538d-145">False</span><span class="sxs-lookup"><span data-stu-id="e538d-145">False</span></span>                                    |
| <span data-ttu-id="e538d-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e538d-146">In Global Catalog</span></span>      | <span data-ttu-id="e538d-147">False</span><span class="sxs-lookup"><span data-stu-id="e538d-147">False</span></span>                                    |
| <span data-ttu-id="e538d-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e538d-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="e538d-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e538d-149">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e538d-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e538d-150">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e538d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e538d-151">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e538d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-152">Search-Flags</span></span>           | <span data-ttu-id="e538d-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e538d-153">0x00000000</span></span>                               |
| <span data-ttu-id="e538d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-154">System-Flags</span></span>           | <span data-ttu-id="e538d-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e538d-155">0x00000011</span></span>                               |
| <span data-ttu-id="e538d-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e538d-156">Classes used in</span></span>        | [<span data-ttu-id="e538d-157">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e538d-157">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e538d-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="e538d-158">ADAM</span></span>



| <span data-ttu-id="e538d-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="e538d-159">Entry</span></span> | <span data-ttu-id="e538d-160">Value</span><span class="sxs-lookup"><span data-stu-id="e538d-160">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e538d-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e538d-161">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e538d-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="e538d-163">System-Only</span></span>            | <span data-ttu-id="e538d-164">False</span><span class="sxs-lookup"><span data-stu-id="e538d-164">False</span></span>                                    |
| <span data-ttu-id="e538d-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e538d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="e538d-166">True</span><span class="sxs-lookup"><span data-stu-id="e538d-166">True</span></span>                                     |
| <span data-ttu-id="e538d-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e538d-167">Is Indexed</span></span>             | <span data-ttu-id="e538d-168">False</span><span class="sxs-lookup"><span data-stu-id="e538d-168">False</span></span>                                    |
| <span data-ttu-id="e538d-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e538d-169">In Global Catalog</span></span>      | <span data-ttu-id="e538d-170">False</span><span class="sxs-lookup"><span data-stu-id="e538d-170">False</span></span>                                    |
| <span data-ttu-id="e538d-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e538d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="e538d-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e538d-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e538d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e538d-173">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e538d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e538d-174">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e538d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-175">Search-Flags</span></span>           | <span data-ttu-id="e538d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e538d-176">0x00000000</span></span>                               |
| <span data-ttu-id="e538d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-177">System-Flags</span></span>           | <span data-ttu-id="e538d-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e538d-178">0x00000011</span></span>                               |
| <span data-ttu-id="e538d-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e538d-179">Classes used in</span></span>        | [<span data-ttu-id="e538d-180">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e538d-180">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e538d-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e538d-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e538d-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="e538d-182">Entry</span></span> | <span data-ttu-id="e538d-183">Value</span><span class="sxs-lookup"><span data-stu-id="e538d-183">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e538d-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e538d-184">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e538d-185">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="e538d-186">System-Only</span></span>            | <span data-ttu-id="e538d-187">False</span><span class="sxs-lookup"><span data-stu-id="e538d-187">False</span></span>                                    |
| <span data-ttu-id="e538d-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e538d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="e538d-189">True</span><span class="sxs-lookup"><span data-stu-id="e538d-189">True</span></span>                                     |
| <span data-ttu-id="e538d-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e538d-190">Is Indexed</span></span>             | <span data-ttu-id="e538d-191">False</span><span class="sxs-lookup"><span data-stu-id="e538d-191">False</span></span>                                    |
| <span data-ttu-id="e538d-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e538d-192">In Global Catalog</span></span>      | <span data-ttu-id="e538d-193">False</span><span class="sxs-lookup"><span data-stu-id="e538d-193">False</span></span>                                    |
| <span data-ttu-id="e538d-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e538d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="e538d-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e538d-195">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e538d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e538d-196">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e538d-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e538d-197">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e538d-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-198">Search-Flags</span></span>           | <span data-ttu-id="e538d-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e538d-199">0x00000000</span></span>                               |
| <span data-ttu-id="e538d-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-200">System-Flags</span></span>           | <span data-ttu-id="e538d-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e538d-201">0x00000011</span></span>                               |
| <span data-ttu-id="e538d-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e538d-202">Classes used in</span></span>        | [<span data-ttu-id="e538d-203">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e538d-203">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e538d-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e538d-204">Windows Server 2008</span></span>



| <span data-ttu-id="e538d-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="e538d-205">Entry</span></span> | <span data-ttu-id="e538d-206">Value</span><span class="sxs-lookup"><span data-stu-id="e538d-206">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e538d-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e538d-207">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e538d-208">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e538d-209">System-Only</span></span>            | <span data-ttu-id="e538d-210">False</span><span class="sxs-lookup"><span data-stu-id="e538d-210">False</span></span>                                    |
| <span data-ttu-id="e538d-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e538d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e538d-212">True</span><span class="sxs-lookup"><span data-stu-id="e538d-212">True</span></span>                                     |
| <span data-ttu-id="e538d-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e538d-213">Is Indexed</span></span>             | <span data-ttu-id="e538d-214">False</span><span class="sxs-lookup"><span data-stu-id="e538d-214">False</span></span>                                    |
| <span data-ttu-id="e538d-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e538d-215">In Global Catalog</span></span>      | <span data-ttu-id="e538d-216">False</span><span class="sxs-lookup"><span data-stu-id="e538d-216">False</span></span>                                    |
| <span data-ttu-id="e538d-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e538d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e538d-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e538d-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e538d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e538d-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e538d-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e538d-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e538d-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-221">Search-Flags</span></span>           | <span data-ttu-id="e538d-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e538d-222">0x00000000</span></span>                               |
| <span data-ttu-id="e538d-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-223">System-Flags</span></span>           | <span data-ttu-id="e538d-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e538d-224">0x00000011</span></span>                               |
| <span data-ttu-id="e538d-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e538d-225">Classes used in</span></span>        | [<span data-ttu-id="e538d-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e538d-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e538d-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e538d-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e538d-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="e538d-228">Entry</span></span> | <span data-ttu-id="e538d-229">Value</span><span class="sxs-lookup"><span data-stu-id="e538d-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e538d-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e538d-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e538d-231">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="e538d-232">System-Only</span></span>            | <span data-ttu-id="e538d-233">False</span><span class="sxs-lookup"><span data-stu-id="e538d-233">False</span></span>                                    |
| <span data-ttu-id="e538d-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e538d-234">Is-Single-Valued</span></span>       | <span data-ttu-id="e538d-235">True</span><span class="sxs-lookup"><span data-stu-id="e538d-235">True</span></span>                                     |
| <span data-ttu-id="e538d-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e538d-236">Is Indexed</span></span>             | <span data-ttu-id="e538d-237">False</span><span class="sxs-lookup"><span data-stu-id="e538d-237">False</span></span>                                    |
| <span data-ttu-id="e538d-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e538d-238">In Global Catalog</span></span>      | <span data-ttu-id="e538d-239">False</span><span class="sxs-lookup"><span data-stu-id="e538d-239">False</span></span>                                    |
| <span data-ttu-id="e538d-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e538d-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="e538d-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e538d-241">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e538d-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e538d-242">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e538d-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e538d-243">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e538d-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-244">Search-Flags</span></span>           | <span data-ttu-id="e538d-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e538d-245">0x00000000</span></span>                               |
| <span data-ttu-id="e538d-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-246">System-Flags</span></span>           | <span data-ttu-id="e538d-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e538d-247">0x00000011</span></span>                               |
| <span data-ttu-id="e538d-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e538d-248">Classes used in</span></span>        | [<span data-ttu-id="e538d-249">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e538d-249">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e538d-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e538d-250">Windows Server 2012</span></span>



| <span data-ttu-id="e538d-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="e538d-251">Entry</span></span> | <span data-ttu-id="e538d-252">Value</span><span class="sxs-lookup"><span data-stu-id="e538d-252">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="e538d-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e538d-253">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e538d-254">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="e538d-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="e538d-255">System-Only</span></span>            | <span data-ttu-id="e538d-256">False</span><span class="sxs-lookup"><span data-stu-id="e538d-256">False</span></span>                                    |
| <span data-ttu-id="e538d-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e538d-257">Is-Single-Valued</span></span>       | <span data-ttu-id="e538d-258">True</span><span class="sxs-lookup"><span data-stu-id="e538d-258">True</span></span>                                     |
| <span data-ttu-id="e538d-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e538d-259">Is Indexed</span></span>             | <span data-ttu-id="e538d-260">False</span><span class="sxs-lookup"><span data-stu-id="e538d-260">False</span></span>                                    |
| <span data-ttu-id="e538d-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e538d-261">In Global Catalog</span></span>      | <span data-ttu-id="e538d-262">False</span><span class="sxs-lookup"><span data-stu-id="e538d-262">False</span></span>                                    |
| <span data-ttu-id="e538d-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e538d-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="e538d-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e538d-264">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="e538d-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e538d-265">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="e538d-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e538d-266">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="e538d-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-267">Search-Flags</span></span>           | <span data-ttu-id="e538d-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e538d-268">0x00000000</span></span>                               |
| <span data-ttu-id="e538d-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e538d-269">System-Flags</span></span>           | <span data-ttu-id="e538d-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e538d-270">0x00000011</span></span>                               |
| <span data-ttu-id="e538d-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e538d-271">Classes used in</span></span>        | [<span data-ttu-id="e538d-272">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="e538d-272">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 






---
title: atributo MS-DS-Replication-Notify-First-DSA-Delay
description: Este atributo controla el retraso en el tiempo entre los cambios en el DS y la notificación del primer asociado de réplica para un NC.
ms.assetid: 58474bf9-9069-402a-a94b-4d1b6df0810e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-Replication-Notify-First-DSA-Delay
- msDS-Replication-Notify-First-DSA-Delay Attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-First-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a981ff257562e701b12e3855b279b7995721e39
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906024"
---
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="e934c-105">atributo MS-DS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="e934c-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="e934c-106">Este atributo controla el retraso en el tiempo entre los cambios en el DS y la notificación del primer asociado de réplica para un NC.</span><span class="sxs-lookup"><span data-stu-id="e934c-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="e934c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e934c-107">Entry</span></span> | <span data-ttu-id="e934c-108">Value</span><span class="sxs-lookup"><span data-stu-id="e934c-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="e934c-109">CN</span><span class="sxs-lookup"><span data-stu-id="e934c-109">CN</span></span>                | <span data-ttu-id="e934c-110">MS-DS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="e934c-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="e934c-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e934c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e934c-112">msDS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="e934c-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="e934c-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e934c-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="e934c-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e934c-114">Update Privilege</span></span>  | <span data-ttu-id="e934c-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="e934c-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="e934c-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e934c-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="e934c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e934c-117">Attribute-Id</span></span>      | <span data-ttu-id="e934c-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="e934c-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="e934c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e934c-119">System-Id-Guid</span></span>    | <span data-ttu-id="e934c-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="e934c-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="e934c-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e934c-121">Syntax</span></span>            | [<span data-ttu-id="e934c-122">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="e934c-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="e934c-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e934c-123">Implementations</span></span>

-   [<span data-ttu-id="e934c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e934c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e934c-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e934c-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e934c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e934c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e934c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e934c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e934c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e934c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e934c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e934c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e934c-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e934c-130">Windows Server 2003</span></span>



| <span data-ttu-id="e934c-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="e934c-131">Entry</span></span> | <span data-ttu-id="e934c-132">Value</span><span class="sxs-lookup"><span data-stu-id="e934c-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e934c-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e934c-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e934c-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e934c-135">System-Only</span></span>            | <span data-ttu-id="e934c-136">False</span><span class="sxs-lookup"><span data-stu-id="e934c-136">False</span></span>                                      |
| <span data-ttu-id="e934c-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e934c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e934c-138">True</span><span class="sxs-lookup"><span data-stu-id="e934c-138">True</span></span>                                       |
| <span data-ttu-id="e934c-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e934c-139">Is Indexed</span></span>             | <span data-ttu-id="e934c-140">False</span><span class="sxs-lookup"><span data-stu-id="e934c-140">False</span></span>                                      |
| <span data-ttu-id="e934c-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e934c-141">In Global Catalog</span></span>      | <span data-ttu-id="e934c-142">False</span><span class="sxs-lookup"><span data-stu-id="e934c-142">False</span></span>                                      |
| <span data-ttu-id="e934c-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e934c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e934c-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e934c-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e934c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e934c-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e934c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e934c-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e934c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-147">Search-Flags</span></span>           | <span data-ttu-id="e934c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e934c-148">0x00000000</span></span>                                 |
| <span data-ttu-id="e934c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-149">System-Flags</span></span>           | <span data-ttu-id="e934c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e934c-150">0x00000010</span></span>                                 |
| <span data-ttu-id="e934c-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e934c-151">Classes used in</span></span>        | [<span data-ttu-id="e934c-152">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="e934c-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e934c-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="e934c-153">ADAM</span></span>



| <span data-ttu-id="e934c-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="e934c-154">Entry</span></span> | <span data-ttu-id="e934c-155">Value</span><span class="sxs-lookup"><span data-stu-id="e934c-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e934c-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e934c-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e934c-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e934c-158">System-Only</span></span>            | <span data-ttu-id="e934c-159">False</span><span class="sxs-lookup"><span data-stu-id="e934c-159">False</span></span>                                      |
| <span data-ttu-id="e934c-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e934c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e934c-161">True</span><span class="sxs-lookup"><span data-stu-id="e934c-161">True</span></span>                                       |
| <span data-ttu-id="e934c-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e934c-162">Is Indexed</span></span>             | <span data-ttu-id="e934c-163">False</span><span class="sxs-lookup"><span data-stu-id="e934c-163">False</span></span>                                      |
| <span data-ttu-id="e934c-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e934c-164">In Global Catalog</span></span>      | <span data-ttu-id="e934c-165">False</span><span class="sxs-lookup"><span data-stu-id="e934c-165">False</span></span>                                      |
| <span data-ttu-id="e934c-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e934c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e934c-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e934c-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e934c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e934c-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e934c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e934c-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e934c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-170">Search-Flags</span></span>           | <span data-ttu-id="e934c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e934c-171">0x00000000</span></span>                                 |
| <span data-ttu-id="e934c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-172">System-Flags</span></span>           | <span data-ttu-id="e934c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e934c-173">0x00000010</span></span>                                 |
| <span data-ttu-id="e934c-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e934c-174">Classes used in</span></span>        | [<span data-ttu-id="e934c-175">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="e934c-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e934c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e934c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e934c-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="e934c-177">Entry</span></span> | <span data-ttu-id="e934c-178">Value</span><span class="sxs-lookup"><span data-stu-id="e934c-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e934c-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e934c-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e934c-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e934c-181">System-Only</span></span>            | <span data-ttu-id="e934c-182">False</span><span class="sxs-lookup"><span data-stu-id="e934c-182">False</span></span>                                      |
| <span data-ttu-id="e934c-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e934c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e934c-184">True</span><span class="sxs-lookup"><span data-stu-id="e934c-184">True</span></span>                                       |
| <span data-ttu-id="e934c-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e934c-185">Is Indexed</span></span>             | <span data-ttu-id="e934c-186">False</span><span class="sxs-lookup"><span data-stu-id="e934c-186">False</span></span>                                      |
| <span data-ttu-id="e934c-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e934c-187">In Global Catalog</span></span>      | <span data-ttu-id="e934c-188">False</span><span class="sxs-lookup"><span data-stu-id="e934c-188">False</span></span>                                      |
| <span data-ttu-id="e934c-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e934c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e934c-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e934c-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e934c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e934c-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e934c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e934c-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e934c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-193">Search-Flags</span></span>           | <span data-ttu-id="e934c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e934c-194">0x00000000</span></span>                                 |
| <span data-ttu-id="e934c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-195">System-Flags</span></span>           | <span data-ttu-id="e934c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e934c-196">0x00000010</span></span>                                 |
| <span data-ttu-id="e934c-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e934c-197">Classes used in</span></span>        | [<span data-ttu-id="e934c-198">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="e934c-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e934c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e934c-199">Windows Server 2008</span></span>



| <span data-ttu-id="e934c-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="e934c-200">Entry</span></span> | <span data-ttu-id="e934c-201">Value</span><span class="sxs-lookup"><span data-stu-id="e934c-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e934c-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e934c-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e934c-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e934c-204">System-Only</span></span>            | <span data-ttu-id="e934c-205">False</span><span class="sxs-lookup"><span data-stu-id="e934c-205">False</span></span>                                      |
| <span data-ttu-id="e934c-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e934c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e934c-207">True</span><span class="sxs-lookup"><span data-stu-id="e934c-207">True</span></span>                                       |
| <span data-ttu-id="e934c-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e934c-208">Is Indexed</span></span>             | <span data-ttu-id="e934c-209">False</span><span class="sxs-lookup"><span data-stu-id="e934c-209">False</span></span>                                      |
| <span data-ttu-id="e934c-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e934c-210">In Global Catalog</span></span>      | <span data-ttu-id="e934c-211">False</span><span class="sxs-lookup"><span data-stu-id="e934c-211">False</span></span>                                      |
| <span data-ttu-id="e934c-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e934c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e934c-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e934c-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e934c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e934c-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e934c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e934c-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e934c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-216">Search-Flags</span></span>           | <span data-ttu-id="e934c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e934c-217">0x00000000</span></span>                                 |
| <span data-ttu-id="e934c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-218">System-Flags</span></span>           | <span data-ttu-id="e934c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e934c-219">0x00000010</span></span>                                 |
| <span data-ttu-id="e934c-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e934c-220">Classes used in</span></span>        | [<span data-ttu-id="e934c-221">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="e934c-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e934c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e934c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e934c-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="e934c-223">Entry</span></span> | <span data-ttu-id="e934c-224">Value</span><span class="sxs-lookup"><span data-stu-id="e934c-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e934c-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e934c-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e934c-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e934c-227">System-Only</span></span>            | <span data-ttu-id="e934c-228">False</span><span class="sxs-lookup"><span data-stu-id="e934c-228">False</span></span>                                      |
| <span data-ttu-id="e934c-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e934c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e934c-230">True</span><span class="sxs-lookup"><span data-stu-id="e934c-230">True</span></span>                                       |
| <span data-ttu-id="e934c-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e934c-231">Is Indexed</span></span>             | <span data-ttu-id="e934c-232">False</span><span class="sxs-lookup"><span data-stu-id="e934c-232">False</span></span>                                      |
| <span data-ttu-id="e934c-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e934c-233">In Global Catalog</span></span>      | <span data-ttu-id="e934c-234">False</span><span class="sxs-lookup"><span data-stu-id="e934c-234">False</span></span>                                      |
| <span data-ttu-id="e934c-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e934c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e934c-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e934c-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e934c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e934c-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e934c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e934c-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e934c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-239">Search-Flags</span></span>           | <span data-ttu-id="e934c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e934c-240">0x00000000</span></span>                                 |
| <span data-ttu-id="e934c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-241">System-Flags</span></span>           | <span data-ttu-id="e934c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e934c-242">0x00000010</span></span>                                 |
| <span data-ttu-id="e934c-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e934c-243">Classes used in</span></span>        | [<span data-ttu-id="e934c-244">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="e934c-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e934c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e934c-245">Windows Server 2012</span></span>



| <span data-ttu-id="e934c-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="e934c-246">Entry</span></span> | <span data-ttu-id="e934c-247">Value</span><span class="sxs-lookup"><span data-stu-id="e934c-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="e934c-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e934c-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e934c-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="e934c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e934c-250">System-Only</span></span>            | <span data-ttu-id="e934c-251">False</span><span class="sxs-lookup"><span data-stu-id="e934c-251">False</span></span>                                      |
| <span data-ttu-id="e934c-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e934c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e934c-253">True</span><span class="sxs-lookup"><span data-stu-id="e934c-253">True</span></span>                                       |
| <span data-ttu-id="e934c-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e934c-254">Is Indexed</span></span>             | <span data-ttu-id="e934c-255">False</span><span class="sxs-lookup"><span data-stu-id="e934c-255">False</span></span>                                      |
| <span data-ttu-id="e934c-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e934c-256">In Global Catalog</span></span>      | <span data-ttu-id="e934c-257">False</span><span class="sxs-lookup"><span data-stu-id="e934c-257">False</span></span>                                      |
| <span data-ttu-id="e934c-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e934c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e934c-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e934c-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="e934c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e934c-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="e934c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e934c-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="e934c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-262">Search-Flags</span></span>           | <span data-ttu-id="e934c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e934c-263">0x00000000</span></span>                                 |
| <span data-ttu-id="e934c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e934c-264">System-Flags</span></span>           | <span data-ttu-id="e934c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e934c-265">0x00000010</span></span>                                 |
| <span data-ttu-id="e934c-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e934c-266">Classes used in</span></span>        | [<span data-ttu-id="e934c-267">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="e934c-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






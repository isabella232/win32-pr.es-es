---
title: atributo MS-DS-NC-Replica-locations
description: Una lista de servidores que son el conjunto de réplicas para el contexto de nomenclatura que no es de dominio correspondiente.
ms.assetid: b0379bb6-feee-432a-b484-1a6c8100d027
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-NC-Replica-locations
- atributo msDS-NC-réplica-locations esquema de AD
topic_type:
- apiref
api_name:
- ms-DS-NC-Replica-Locations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4adc3d3ca3553c8e57cdc114eb045206c1501060
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997558"
---
# <a name="ms-ds-nc-replica-locations-attribute"></a><span data-ttu-id="a4ce2-105">atributo MS-DS-NC-Replica-locations</span><span class="sxs-lookup"><span data-stu-id="a4ce2-105">ms-DS-NC-Replica-Locations attribute</span></span>

<span data-ttu-id="a4ce2-106">Una lista de servidores que son el conjunto de réplicas para el contexto de nomenclatura que no es de dominio correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a4ce2-106">A list of servers that are the replica set for the corresponding Non-Domain Naming Context.</span></span>



| <span data-ttu-id="a4ce2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4ce2-107">Entry</span></span> | <span data-ttu-id="a4ce2-108">Value</span><span class="sxs-lookup"><span data-stu-id="a4ce2-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a4ce2-109">CN</span><span class="sxs-lookup"><span data-stu-id="a4ce2-109">CN</span></span>                | <span data-ttu-id="a4ce2-110">MS-DS-NC-réplica-ubicaciones</span><span class="sxs-lookup"><span data-stu-id="a4ce2-110">ms-DS-NC-Replica-Locations</span></span>              |
| <span data-ttu-id="a4ce2-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a4ce2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a4ce2-112">msDS-NC-réplica-ubicaciones</span><span class="sxs-lookup"><span data-stu-id="a4ce2-112">msDS-NC-Replica-Locations</span></span>               |
| <span data-ttu-id="a4ce2-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a4ce2-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="a4ce2-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a4ce2-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="a4ce2-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a4ce2-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="a4ce2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a4ce2-116">Attribute-Id</span></span>      | <span data-ttu-id="a4ce2-117">1.2.840.113556.1.4.1661</span><span class="sxs-lookup"><span data-stu-id="a4ce2-117">1.2.840.113556.1.4.1661</span></span>                 |
| <span data-ttu-id="a4ce2-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a4ce2-118">System-Id-Guid</span></span>    | <span data-ttu-id="a4ce2-119">97de9615-b537-46bc-ac0f-10720f3909f3</span><span class="sxs-lookup"><span data-stu-id="a4ce2-119">97de9615-b537-46bc-ac0f-10720f3909f3</span></span>    |
| <span data-ttu-id="a4ce2-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4ce2-120">Syntax</span></span>            | [<span data-ttu-id="a4ce2-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a4ce2-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a4ce2-122">Implementations</span></span>

-   [<span data-ttu-id="a4ce2-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a4ce2-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a4ce2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a4ce2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a4ce2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a4ce2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a4ce2-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4ce2-129">Windows Server 2003</span></span>



| <span data-ttu-id="a4ce2-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4ce2-130">Entry</span></span> | <span data-ttu-id="a4ce2-131">Value</span><span class="sxs-lookup"><span data-stu-id="a4ce2-131">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a4ce2-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a4ce2-132">Link-Id</span></span>                | <span data-ttu-id="a4ce2-133">1044</span><span class="sxs-lookup"><span data-stu-id="a4ce2-133">1044</span></span>                                       |
| <span data-ttu-id="a4ce2-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4ce2-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a4ce2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4ce2-135">System-Only</span></span>            | <span data-ttu-id="a4ce2-136">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-136">False</span></span>                                      |
| <span data-ttu-id="a4ce2-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a4ce2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a4ce2-138">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-138">False</span></span>                                      |
| <span data-ttu-id="a4ce2-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a4ce2-139">Is Indexed</span></span>             | <span data-ttu-id="a4ce2-140">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-140">False</span></span>                                      |
| <span data-ttu-id="a4ce2-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4ce2-141">In Global Catalog</span></span>      | <span data-ttu-id="a4ce2-142">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-142">False</span></span>                                      |
| <span data-ttu-id="a4ce2-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a4ce2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4ce2-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a4ce2-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a4ce2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4ce2-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4ce2-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-147">Search-Flags</span></span>           | <span data-ttu-id="a4ce2-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4ce2-148">0x00000000</span></span>                                 |
| <span data-ttu-id="a4ce2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-149">System-Flags</span></span>           | <span data-ttu-id="a4ce2-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4ce2-150">0x00000010</span></span>                                 |
| <span data-ttu-id="a4ce2-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a4ce2-151">Classes used in</span></span>        | [<span data-ttu-id="a4ce2-152">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a4ce2-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="a4ce2-153">ADAM</span></span>



| <span data-ttu-id="a4ce2-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4ce2-154">Entry</span></span> | <span data-ttu-id="a4ce2-155">Value</span><span class="sxs-lookup"><span data-stu-id="a4ce2-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a4ce2-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a4ce2-156">Link-Id</span></span>                | <span data-ttu-id="a4ce2-157">1044</span><span class="sxs-lookup"><span data-stu-id="a4ce2-157">1044</span></span>                                       |
| <span data-ttu-id="a4ce2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4ce2-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a4ce2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4ce2-159">System-Only</span></span>            | <span data-ttu-id="a4ce2-160">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-160">False</span></span>                                      |
| <span data-ttu-id="a4ce2-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a4ce2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a4ce2-162">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-162">False</span></span>                                      |
| <span data-ttu-id="a4ce2-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a4ce2-163">Is Indexed</span></span>             | <span data-ttu-id="a4ce2-164">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-164">False</span></span>                                      |
| <span data-ttu-id="a4ce2-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4ce2-165">In Global Catalog</span></span>      | <span data-ttu-id="a4ce2-166">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-166">False</span></span>                                      |
| <span data-ttu-id="a4ce2-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a4ce2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4ce2-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a4ce2-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a4ce2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4ce2-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4ce2-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-171">Search-Flags</span></span>           | <span data-ttu-id="a4ce2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4ce2-172">0x00000000</span></span>                                 |
| <span data-ttu-id="a4ce2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-173">System-Flags</span></span>           | <span data-ttu-id="a4ce2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4ce2-174">0x00000010</span></span>                                 |
| <span data-ttu-id="a4ce2-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a4ce2-175">Classes used in</span></span>        | [<span data-ttu-id="a4ce2-176">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a4ce2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a4ce2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a4ce2-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4ce2-178">Entry</span></span> | <span data-ttu-id="a4ce2-179">Value</span><span class="sxs-lookup"><span data-stu-id="a4ce2-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a4ce2-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a4ce2-180">Link-Id</span></span>                | <span data-ttu-id="a4ce2-181">1044</span><span class="sxs-lookup"><span data-stu-id="a4ce2-181">1044</span></span>                                       |
| <span data-ttu-id="a4ce2-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4ce2-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a4ce2-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4ce2-183">System-Only</span></span>            | <span data-ttu-id="a4ce2-184">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-184">False</span></span>                                      |
| <span data-ttu-id="a4ce2-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a4ce2-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a4ce2-186">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-186">False</span></span>                                      |
| <span data-ttu-id="a4ce2-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a4ce2-187">Is Indexed</span></span>             | <span data-ttu-id="a4ce2-188">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-188">False</span></span>                                      |
| <span data-ttu-id="a4ce2-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4ce2-189">In Global Catalog</span></span>      | <span data-ttu-id="a4ce2-190">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-190">False</span></span>                                      |
| <span data-ttu-id="a4ce2-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a4ce2-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4ce2-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a4ce2-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a4ce2-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4ce2-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4ce2-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-195">Search-Flags</span></span>           | <span data-ttu-id="a4ce2-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4ce2-196">0x00000000</span></span>                                 |
| <span data-ttu-id="a4ce2-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-197">System-Flags</span></span>           | <span data-ttu-id="a4ce2-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4ce2-198">0x00000010</span></span>                                 |
| <span data-ttu-id="a4ce2-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a4ce2-199">Classes used in</span></span>        | [<span data-ttu-id="a4ce2-200">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a4ce2-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4ce2-201">Windows Server 2008</span></span>



| <span data-ttu-id="a4ce2-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4ce2-202">Entry</span></span> | <span data-ttu-id="a4ce2-203">Value</span><span class="sxs-lookup"><span data-stu-id="a4ce2-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a4ce2-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a4ce2-204">Link-Id</span></span>                | <span data-ttu-id="a4ce2-205">1044</span><span class="sxs-lookup"><span data-stu-id="a4ce2-205">1044</span></span>                                       |
| <span data-ttu-id="a4ce2-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4ce2-206">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a4ce2-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4ce2-207">System-Only</span></span>            | <span data-ttu-id="a4ce2-208">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-208">False</span></span>                                      |
| <span data-ttu-id="a4ce2-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a4ce2-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a4ce2-210">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-210">False</span></span>                                      |
| <span data-ttu-id="a4ce2-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a4ce2-211">Is Indexed</span></span>             | <span data-ttu-id="a4ce2-212">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-212">False</span></span>                                      |
| <span data-ttu-id="a4ce2-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4ce2-213">In Global Catalog</span></span>      | <span data-ttu-id="a4ce2-214">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-214">False</span></span>                                      |
| <span data-ttu-id="a4ce2-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a4ce2-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4ce2-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a4ce2-216">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a4ce2-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4ce2-217">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4ce2-218">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-219">Search-Flags</span></span>           | <span data-ttu-id="a4ce2-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4ce2-220">0x00000000</span></span>                                 |
| <span data-ttu-id="a4ce2-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-221">System-Flags</span></span>           | <span data-ttu-id="a4ce2-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4ce2-222">0x00000010</span></span>                                 |
| <span data-ttu-id="a4ce2-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a4ce2-223">Classes used in</span></span>        | [<span data-ttu-id="a4ce2-224">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-224">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a4ce2-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4ce2-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a4ce2-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4ce2-226">Entry</span></span> | <span data-ttu-id="a4ce2-227">Value</span><span class="sxs-lookup"><span data-stu-id="a4ce2-227">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a4ce2-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a4ce2-228">Link-Id</span></span>                | <span data-ttu-id="a4ce2-229">1044</span><span class="sxs-lookup"><span data-stu-id="a4ce2-229">1044</span></span>                                       |
| <span data-ttu-id="a4ce2-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4ce2-230">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a4ce2-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4ce2-231">System-Only</span></span>            | <span data-ttu-id="a4ce2-232">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-232">False</span></span>                                      |
| <span data-ttu-id="a4ce2-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a4ce2-233">Is-Single-Valued</span></span>       | <span data-ttu-id="a4ce2-234">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-234">False</span></span>                                      |
| <span data-ttu-id="a4ce2-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a4ce2-235">Is Indexed</span></span>             | <span data-ttu-id="a4ce2-236">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-236">False</span></span>                                      |
| <span data-ttu-id="a4ce2-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4ce2-237">In Global Catalog</span></span>      | <span data-ttu-id="a4ce2-238">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-238">False</span></span>                                      |
| <span data-ttu-id="a4ce2-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a4ce2-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4ce2-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a4ce2-240">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a4ce2-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4ce2-241">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4ce2-242">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-243">Search-Flags</span></span>           | <span data-ttu-id="a4ce2-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4ce2-244">0x00000000</span></span>                                 |
| <span data-ttu-id="a4ce2-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-245">System-Flags</span></span>           | <span data-ttu-id="a4ce2-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4ce2-246">0x00000010</span></span>                                 |
| <span data-ttu-id="a4ce2-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a4ce2-247">Classes used in</span></span>        | [<span data-ttu-id="a4ce2-248">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-248">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a4ce2-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4ce2-249">Windows Server 2012</span></span>



| <span data-ttu-id="a4ce2-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4ce2-250">Entry</span></span> | <span data-ttu-id="a4ce2-251">Value</span><span class="sxs-lookup"><span data-stu-id="a4ce2-251">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a4ce2-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a4ce2-252">Link-Id</span></span>                | <span data-ttu-id="a4ce2-253">1044</span><span class="sxs-lookup"><span data-stu-id="a4ce2-253">1044</span></span>                                       |
| <span data-ttu-id="a4ce2-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a4ce2-254">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a4ce2-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="a4ce2-255">System-Only</span></span>            | <span data-ttu-id="a4ce2-256">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-256">False</span></span>                                      |
| <span data-ttu-id="a4ce2-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a4ce2-257">Is-Single-Valued</span></span>       | <span data-ttu-id="a4ce2-258">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-258">False</span></span>                                      |
| <span data-ttu-id="a4ce2-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a4ce2-259">Is Indexed</span></span>             | <span data-ttu-id="a4ce2-260">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-260">False</span></span>                                      |
| <span data-ttu-id="a4ce2-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a4ce2-261">In Global Catalog</span></span>      | <span data-ttu-id="a4ce2-262">False</span><span class="sxs-lookup"><span data-stu-id="a4ce2-262">False</span></span>                                      |
| <span data-ttu-id="a4ce2-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a4ce2-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="a4ce2-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a4ce2-264">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a4ce2-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a4ce2-265">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a4ce2-266">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="a4ce2-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-267">Search-Flags</span></span>           | <span data-ttu-id="a4ce2-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a4ce2-268">0x00000000</span></span>                                 |
| <span data-ttu-id="a4ce2-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a4ce2-269">System-Flags</span></span>           | <span data-ttu-id="a4ce2-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a4ce2-270">0x00000010</span></span>                                 |
| <span data-ttu-id="a4ce2-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a4ce2-271">Classes used in</span></span>        | [<span data-ttu-id="a4ce2-272">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a4ce2-272">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






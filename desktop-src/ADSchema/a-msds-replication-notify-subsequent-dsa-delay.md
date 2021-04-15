---
title: atributo MS-DS-Replication-Notify-subsiguiente-DSA-Delay
description: Este atributo controla el retraso en el tiempo entre la notificación de cada asociado de réplica subsiguiente para un NC.
ms.assetid: 6bd9fed7-2003-4156-b1a0-da8622dc2ca8
ms.tgt_platform: multiple
keywords:
- MS-DS-Replication-Notify-subestado-DSA-Delay atributo AD Schema
- msDS-Replication-Notify-subsiguientes-DSA-Delay Attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-Subsequent-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd8b267309fa8d017ace926f7497ca210fb2b00
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536256"
---
# <a name="ms-ds-replication-notify-subsequent-dsa-delay-attribute"></a><span data-ttu-id="7742a-105">atributo MS-DS-Replication-Notify-subsiguiente-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="7742a-105">ms-DS-Replication-Notify-Subsequent-DSA-Delay attribute</span></span>

<span data-ttu-id="7742a-106">Este atributo controla el retraso en el tiempo entre la notificación de cada asociado de réplica subsiguiente para un NC.</span><span class="sxs-lookup"><span data-stu-id="7742a-106">This attribute controls the delay in time between notification of each subsequent replica partner for an NC.</span></span>



| <span data-ttu-id="7742a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7742a-107">Entry</span></span> | <span data-ttu-id="7742a-108">Value</span><span class="sxs-lookup"><span data-stu-id="7742a-108">Value</span></span> |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="7742a-109">CN</span><span class="sxs-lookup"><span data-stu-id="7742a-109">CN</span></span>                | <span data-ttu-id="7742a-110">MS-DS-Replication-Notify-subsiguiente-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="7742a-110">ms-DS-Replication-Notify-Subsequent-DSA-Delay</span></span> |
| <span data-ttu-id="7742a-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7742a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7742a-112">msDS-Replication-Notify-subsiguientes-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="7742a-112">msDS-Replication-Notify-Subsequent-DSA-Delay</span></span>  |
| <span data-ttu-id="7742a-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7742a-113">Size</span></span>              | \-                                            |
| <span data-ttu-id="7742a-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7742a-114">Update Privilege</span></span>  | <span data-ttu-id="7742a-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="7742a-115">This value is set by the system.</span></span>              |
| <span data-ttu-id="7742a-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7742a-116">Update Frequency</span></span>  | \-                                            |
| <span data-ttu-id="7742a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7742a-117">Attribute-Id</span></span>      | <span data-ttu-id="7742a-118">1.2.840.113556.1.4.1664</span><span class="sxs-lookup"><span data-stu-id="7742a-118">1.2.840.113556.1.4.1664</span></span>                       |
| <span data-ttu-id="7742a-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7742a-119">System-Id-Guid</span></span>    | <span data-ttu-id="7742a-120">d63db385-dd92-4b52-b1d8-0d3ecc0e86b6</span><span class="sxs-lookup"><span data-stu-id="7742a-120">d63db385-dd92-4b52-b1d8-0d3ecc0e86b6</span></span>          |
| <span data-ttu-id="7742a-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7742a-121">Syntax</span></span>            | [<span data-ttu-id="7742a-122">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="7742a-122">**Enumeration**</span></span>](s-enumeration.md)          |



## <a name="implementations"></a><span data-ttu-id="7742a-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7742a-123">Implementations</span></span>

-   [<span data-ttu-id="7742a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7742a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7742a-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7742a-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7742a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7742a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7742a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7742a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7742a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7742a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7742a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7742a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7742a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7742a-130">Windows Server 2003</span></span>



| <span data-ttu-id="7742a-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="7742a-131">Entry</span></span> | <span data-ttu-id="7742a-132">Value</span><span class="sxs-lookup"><span data-stu-id="7742a-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7742a-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7742a-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7742a-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7742a-135">System-Only</span></span>            | <span data-ttu-id="7742a-136">False</span><span class="sxs-lookup"><span data-stu-id="7742a-136">False</span></span>                                      |
| <span data-ttu-id="7742a-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7742a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7742a-138">True</span><span class="sxs-lookup"><span data-stu-id="7742a-138">True</span></span>                                       |
| <span data-ttu-id="7742a-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7742a-139">Is Indexed</span></span>             | <span data-ttu-id="7742a-140">False</span><span class="sxs-lookup"><span data-stu-id="7742a-140">False</span></span>                                      |
| <span data-ttu-id="7742a-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7742a-141">In Global Catalog</span></span>      | <span data-ttu-id="7742a-142">False</span><span class="sxs-lookup"><span data-stu-id="7742a-142">False</span></span>                                      |
| <span data-ttu-id="7742a-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7742a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7742a-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7742a-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7742a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7742a-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7742a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7742a-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7742a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-147">Search-Flags</span></span>           | <span data-ttu-id="7742a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7742a-148">0x00000000</span></span>                                 |
| <span data-ttu-id="7742a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-149">System-Flags</span></span>           | <span data-ttu-id="7742a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7742a-150">0x00000010</span></span>                                 |
| <span data-ttu-id="7742a-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7742a-151">Classes used in</span></span>        | [<span data-ttu-id="7742a-152">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="7742a-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7742a-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="7742a-153">ADAM</span></span>



| <span data-ttu-id="7742a-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="7742a-154">Entry</span></span> | <span data-ttu-id="7742a-155">Value</span><span class="sxs-lookup"><span data-stu-id="7742a-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7742a-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7742a-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7742a-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7742a-158">System-Only</span></span>            | <span data-ttu-id="7742a-159">False</span><span class="sxs-lookup"><span data-stu-id="7742a-159">False</span></span>                                      |
| <span data-ttu-id="7742a-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7742a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7742a-161">True</span><span class="sxs-lookup"><span data-stu-id="7742a-161">True</span></span>                                       |
| <span data-ttu-id="7742a-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7742a-162">Is Indexed</span></span>             | <span data-ttu-id="7742a-163">False</span><span class="sxs-lookup"><span data-stu-id="7742a-163">False</span></span>                                      |
| <span data-ttu-id="7742a-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7742a-164">In Global Catalog</span></span>      | <span data-ttu-id="7742a-165">False</span><span class="sxs-lookup"><span data-stu-id="7742a-165">False</span></span>                                      |
| <span data-ttu-id="7742a-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7742a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7742a-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7742a-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7742a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7742a-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7742a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7742a-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7742a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-170">Search-Flags</span></span>           | <span data-ttu-id="7742a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7742a-171">0x00000000</span></span>                                 |
| <span data-ttu-id="7742a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-172">System-Flags</span></span>           | <span data-ttu-id="7742a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7742a-173">0x00000010</span></span>                                 |
| <span data-ttu-id="7742a-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7742a-174">Classes used in</span></span>        | [<span data-ttu-id="7742a-175">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="7742a-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7742a-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7742a-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7742a-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="7742a-177">Entry</span></span> | <span data-ttu-id="7742a-178">Value</span><span class="sxs-lookup"><span data-stu-id="7742a-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7742a-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7742a-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7742a-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7742a-181">System-Only</span></span>            | <span data-ttu-id="7742a-182">False</span><span class="sxs-lookup"><span data-stu-id="7742a-182">False</span></span>                                      |
| <span data-ttu-id="7742a-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7742a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7742a-184">True</span><span class="sxs-lookup"><span data-stu-id="7742a-184">True</span></span>                                       |
| <span data-ttu-id="7742a-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7742a-185">Is Indexed</span></span>             | <span data-ttu-id="7742a-186">False</span><span class="sxs-lookup"><span data-stu-id="7742a-186">False</span></span>                                      |
| <span data-ttu-id="7742a-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7742a-187">In Global Catalog</span></span>      | <span data-ttu-id="7742a-188">False</span><span class="sxs-lookup"><span data-stu-id="7742a-188">False</span></span>                                      |
| <span data-ttu-id="7742a-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7742a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7742a-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7742a-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7742a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7742a-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7742a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7742a-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7742a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-193">Search-Flags</span></span>           | <span data-ttu-id="7742a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7742a-194">0x00000000</span></span>                                 |
| <span data-ttu-id="7742a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-195">System-Flags</span></span>           | <span data-ttu-id="7742a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7742a-196">0x00000010</span></span>                                 |
| <span data-ttu-id="7742a-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7742a-197">Classes used in</span></span>        | [<span data-ttu-id="7742a-198">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="7742a-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7742a-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7742a-199">Windows Server 2008</span></span>



| <span data-ttu-id="7742a-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="7742a-200">Entry</span></span> | <span data-ttu-id="7742a-201">Value</span><span class="sxs-lookup"><span data-stu-id="7742a-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7742a-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7742a-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7742a-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7742a-204">System-Only</span></span>            | <span data-ttu-id="7742a-205">False</span><span class="sxs-lookup"><span data-stu-id="7742a-205">False</span></span>                                      |
| <span data-ttu-id="7742a-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7742a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7742a-207">True</span><span class="sxs-lookup"><span data-stu-id="7742a-207">True</span></span>                                       |
| <span data-ttu-id="7742a-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7742a-208">Is Indexed</span></span>             | <span data-ttu-id="7742a-209">False</span><span class="sxs-lookup"><span data-stu-id="7742a-209">False</span></span>                                      |
| <span data-ttu-id="7742a-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7742a-210">In Global Catalog</span></span>      | <span data-ttu-id="7742a-211">False</span><span class="sxs-lookup"><span data-stu-id="7742a-211">False</span></span>                                      |
| <span data-ttu-id="7742a-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7742a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7742a-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7742a-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7742a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7742a-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7742a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7742a-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7742a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-216">Search-Flags</span></span>           | <span data-ttu-id="7742a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7742a-217">0x00000000</span></span>                                 |
| <span data-ttu-id="7742a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-218">System-Flags</span></span>           | <span data-ttu-id="7742a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7742a-219">0x00000010</span></span>                                 |
| <span data-ttu-id="7742a-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7742a-220">Classes used in</span></span>        | [<span data-ttu-id="7742a-221">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="7742a-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7742a-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7742a-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7742a-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="7742a-223">Entry</span></span> | <span data-ttu-id="7742a-224">Value</span><span class="sxs-lookup"><span data-stu-id="7742a-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7742a-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7742a-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7742a-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7742a-227">System-Only</span></span>            | <span data-ttu-id="7742a-228">False</span><span class="sxs-lookup"><span data-stu-id="7742a-228">False</span></span>                                      |
| <span data-ttu-id="7742a-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7742a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7742a-230">True</span><span class="sxs-lookup"><span data-stu-id="7742a-230">True</span></span>                                       |
| <span data-ttu-id="7742a-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7742a-231">Is Indexed</span></span>             | <span data-ttu-id="7742a-232">False</span><span class="sxs-lookup"><span data-stu-id="7742a-232">False</span></span>                                      |
| <span data-ttu-id="7742a-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7742a-233">In Global Catalog</span></span>      | <span data-ttu-id="7742a-234">False</span><span class="sxs-lookup"><span data-stu-id="7742a-234">False</span></span>                                      |
| <span data-ttu-id="7742a-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7742a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7742a-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7742a-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7742a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7742a-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7742a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7742a-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7742a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-239">Search-Flags</span></span>           | <span data-ttu-id="7742a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7742a-240">0x00000000</span></span>                                 |
| <span data-ttu-id="7742a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-241">System-Flags</span></span>           | <span data-ttu-id="7742a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7742a-242">0x00000010</span></span>                                 |
| <span data-ttu-id="7742a-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7742a-243">Classes used in</span></span>        | [<span data-ttu-id="7742a-244">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="7742a-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7742a-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7742a-245">Windows Server 2012</span></span>



| <span data-ttu-id="7742a-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="7742a-246">Entry</span></span> | <span data-ttu-id="7742a-247">Value</span><span class="sxs-lookup"><span data-stu-id="7742a-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="7742a-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7742a-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7742a-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="7742a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7742a-250">System-Only</span></span>            | <span data-ttu-id="7742a-251">False</span><span class="sxs-lookup"><span data-stu-id="7742a-251">False</span></span>                                      |
| <span data-ttu-id="7742a-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7742a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7742a-253">True</span><span class="sxs-lookup"><span data-stu-id="7742a-253">True</span></span>                                       |
| <span data-ttu-id="7742a-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7742a-254">Is Indexed</span></span>             | <span data-ttu-id="7742a-255">False</span><span class="sxs-lookup"><span data-stu-id="7742a-255">False</span></span>                                      |
| <span data-ttu-id="7742a-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7742a-256">In Global Catalog</span></span>      | <span data-ttu-id="7742a-257">False</span><span class="sxs-lookup"><span data-stu-id="7742a-257">False</span></span>                                      |
| <span data-ttu-id="7742a-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7742a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7742a-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7742a-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="7742a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7742a-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="7742a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7742a-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="7742a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-262">Search-Flags</span></span>           | <span data-ttu-id="7742a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7742a-263">0x00000000</span></span>                                 |
| <span data-ttu-id="7742a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7742a-264">System-Flags</span></span>           | <span data-ttu-id="7742a-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7742a-265">0x00000010</span></span>                                 |
| <span data-ttu-id="7742a-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7742a-266">Classes used in</span></span>        | [<span data-ttu-id="7742a-267">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="7742a-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






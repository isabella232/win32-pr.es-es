---
title: Atributo MS-DS-Consistency-GUID
description: Este atributo se usa para comprobar la coherencia entre el directorio y otro objeto, base de datos o aplicación mediante la comparación de los GUID.
ms.assetid: 1372f46a-5569-4b06-9803-7d3862cdb745
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Consistency-GUID
- Esquema de AD del atributo mS-DS-ConsistencyGuid
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbea1e9fba4ac28f968fdd61a054f55fe47deb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906063"
---
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="15dc6-105">Atributo MS-DS-Consistency-GUID</span><span class="sxs-lookup"><span data-stu-id="15dc6-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="15dc6-106">Este atributo se usa para comprobar la coherencia entre el directorio y otro objeto, base de datos o aplicación mediante la comparación de los GUID.</span><span class="sxs-lookup"><span data-stu-id="15dc6-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="15dc6-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="15dc6-107">Entry</span></span> | <span data-ttu-id="15dc6-108">Value</span><span class="sxs-lookup"><span data-stu-id="15dc6-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="15dc6-109">CN</span><span class="sxs-lookup"><span data-stu-id="15dc6-109">CN</span></span>                | <span data-ttu-id="15dc6-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="15dc6-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="15dc6-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="15dc6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="15dc6-112">mS-DS-ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="15dc6-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="15dc6-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="15dc6-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="15dc6-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="15dc6-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="15dc6-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="15dc6-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="15dc6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="15dc6-116">Attribute-Id</span></span>      | <span data-ttu-id="15dc6-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="15dc6-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="15dc6-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="15dc6-118">System-Id-Guid</span></span>    | <span data-ttu-id="15dc6-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="15dc6-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="15dc6-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15dc6-120">Syntax</span></span>            | [<span data-ttu-id="15dc6-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="15dc6-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="15dc6-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="15dc6-122">Implementations</span></span>

-   [<span data-ttu-id="15dc6-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="15dc6-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="15dc6-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="15dc6-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="15dc6-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="15dc6-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="15dc6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="15dc6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="15dc6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="15dc6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="15dc6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="15dc6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="15dc6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="15dc6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="15dc6-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="15dc6-130">Windows 2000 Server</span></span>



| <span data-ttu-id="15dc6-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="15dc6-131">Entry</span></span> | <span data-ttu-id="15dc6-132">Value</span><span class="sxs-lookup"><span data-stu-id="15dc6-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15dc6-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15dc6-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15dc6-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="15dc6-135">System-Only</span></span>            | <span data-ttu-id="15dc6-136">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-136">False</span></span>                           |
| <span data-ttu-id="15dc6-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15dc6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="15dc6-138">True</span><span class="sxs-lookup"><span data-stu-id="15dc6-138">True</span></span>                            |
| <span data-ttu-id="15dc6-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15dc6-139">Is Indexed</span></span>             | <span data-ttu-id="15dc6-140">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-140">False</span></span>                           |
| <span data-ttu-id="15dc6-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15dc6-141">In Global Catalog</span></span>      | <span data-ttu-id="15dc6-142">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-142">False</span></span>                           |
| <span data-ttu-id="15dc6-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15dc6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="15dc6-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15dc6-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15dc6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15dc6-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15dc6-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15dc6-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15dc6-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-147">Search-Flags</span></span>           | <span data-ttu-id="15dc6-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15dc6-148">0x00000000</span></span>                      |
| <span data-ttu-id="15dc6-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-149">System-Flags</span></span>           | <span data-ttu-id="15dc6-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15dc6-150">0x00000010</span></span>                      |
| <span data-ttu-id="15dc6-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15dc6-151">Classes used in</span></span>        | [<span data-ttu-id="15dc6-152">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="15dc6-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="15dc6-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15dc6-153">Windows Server 2003</span></span>



| <span data-ttu-id="15dc6-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="15dc6-154">Entry</span></span> | <span data-ttu-id="15dc6-155">Value</span><span class="sxs-lookup"><span data-stu-id="15dc6-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15dc6-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15dc6-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15dc6-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="15dc6-158">System-Only</span></span>            | <span data-ttu-id="15dc6-159">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-159">False</span></span>                           |
| <span data-ttu-id="15dc6-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15dc6-160">Is-Single-Valued</span></span>       | <span data-ttu-id="15dc6-161">True</span><span class="sxs-lookup"><span data-stu-id="15dc6-161">True</span></span>                            |
| <span data-ttu-id="15dc6-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15dc6-162">Is Indexed</span></span>             | <span data-ttu-id="15dc6-163">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-163">False</span></span>                           |
| <span data-ttu-id="15dc6-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15dc6-164">In Global Catalog</span></span>      | <span data-ttu-id="15dc6-165">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-165">False</span></span>                           |
| <span data-ttu-id="15dc6-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15dc6-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="15dc6-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15dc6-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15dc6-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15dc6-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15dc6-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15dc6-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15dc6-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-170">Search-Flags</span></span>           | <span data-ttu-id="15dc6-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15dc6-171">0x00000000</span></span>                      |
| <span data-ttu-id="15dc6-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-172">System-Flags</span></span>           | <span data-ttu-id="15dc6-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15dc6-173">0x00000010</span></span>                      |
| <span data-ttu-id="15dc6-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15dc6-174">Classes used in</span></span>        | [<span data-ttu-id="15dc6-175">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="15dc6-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="15dc6-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="15dc6-176">ADAM</span></span>



| <span data-ttu-id="15dc6-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="15dc6-177">Entry</span></span> | <span data-ttu-id="15dc6-178">Value</span><span class="sxs-lookup"><span data-stu-id="15dc6-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15dc6-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15dc6-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15dc6-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="15dc6-181">System-Only</span></span>            | <span data-ttu-id="15dc6-182">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-182">False</span></span>                           |
| <span data-ttu-id="15dc6-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15dc6-183">Is-Single-Valued</span></span>       | <span data-ttu-id="15dc6-184">True</span><span class="sxs-lookup"><span data-stu-id="15dc6-184">True</span></span>                            |
| <span data-ttu-id="15dc6-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15dc6-185">Is Indexed</span></span>             | <span data-ttu-id="15dc6-186">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-186">False</span></span>                           |
| <span data-ttu-id="15dc6-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15dc6-187">In Global Catalog</span></span>      | <span data-ttu-id="15dc6-188">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-188">False</span></span>                           |
| <span data-ttu-id="15dc6-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15dc6-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="15dc6-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15dc6-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15dc6-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15dc6-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15dc6-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15dc6-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15dc6-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-193">Search-Flags</span></span>           | <span data-ttu-id="15dc6-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15dc6-194">0x00000000</span></span>                      |
| <span data-ttu-id="15dc6-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-195">System-Flags</span></span>           | <span data-ttu-id="15dc6-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15dc6-196">0x00000010</span></span>                      |
| <span data-ttu-id="15dc6-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15dc6-197">Classes used in</span></span>        | [<span data-ttu-id="15dc6-198">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="15dc6-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="15dc6-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="15dc6-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="15dc6-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="15dc6-200">Entry</span></span> | <span data-ttu-id="15dc6-201">Value</span><span class="sxs-lookup"><span data-stu-id="15dc6-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15dc6-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15dc6-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15dc6-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="15dc6-204">System-Only</span></span>            | <span data-ttu-id="15dc6-205">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-205">False</span></span>                           |
| <span data-ttu-id="15dc6-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15dc6-206">Is-Single-Valued</span></span>       | <span data-ttu-id="15dc6-207">True</span><span class="sxs-lookup"><span data-stu-id="15dc6-207">True</span></span>                            |
| <span data-ttu-id="15dc6-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15dc6-208">Is Indexed</span></span>             | <span data-ttu-id="15dc6-209">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-209">False</span></span>                           |
| <span data-ttu-id="15dc6-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15dc6-210">In Global Catalog</span></span>      | <span data-ttu-id="15dc6-211">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-211">False</span></span>                           |
| <span data-ttu-id="15dc6-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15dc6-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="15dc6-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15dc6-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15dc6-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15dc6-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15dc6-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15dc6-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15dc6-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-216">Search-Flags</span></span>           | <span data-ttu-id="15dc6-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15dc6-217">0x00000000</span></span>                      |
| <span data-ttu-id="15dc6-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-218">System-Flags</span></span>           | <span data-ttu-id="15dc6-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15dc6-219">0x00000010</span></span>                      |
| <span data-ttu-id="15dc6-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15dc6-220">Classes used in</span></span>        | [<span data-ttu-id="15dc6-221">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="15dc6-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="15dc6-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15dc6-222">Windows Server 2008</span></span>



| <span data-ttu-id="15dc6-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="15dc6-223">Entry</span></span> | <span data-ttu-id="15dc6-224">Value</span><span class="sxs-lookup"><span data-stu-id="15dc6-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15dc6-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15dc6-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15dc6-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="15dc6-227">System-Only</span></span>            | <span data-ttu-id="15dc6-228">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-228">False</span></span>                           |
| <span data-ttu-id="15dc6-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15dc6-229">Is-Single-Valued</span></span>       | <span data-ttu-id="15dc6-230">True</span><span class="sxs-lookup"><span data-stu-id="15dc6-230">True</span></span>                            |
| <span data-ttu-id="15dc6-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15dc6-231">Is Indexed</span></span>             | <span data-ttu-id="15dc6-232">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-232">False</span></span>                           |
| <span data-ttu-id="15dc6-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15dc6-233">In Global Catalog</span></span>      | <span data-ttu-id="15dc6-234">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-234">False</span></span>                           |
| <span data-ttu-id="15dc6-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15dc6-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="15dc6-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15dc6-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15dc6-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15dc6-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15dc6-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15dc6-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15dc6-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-239">Search-Flags</span></span>           | <span data-ttu-id="15dc6-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15dc6-240">0x00000000</span></span>                      |
| <span data-ttu-id="15dc6-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-241">System-Flags</span></span>           | <span data-ttu-id="15dc6-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15dc6-242">0x00000010</span></span>                      |
| <span data-ttu-id="15dc6-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15dc6-243">Classes used in</span></span>        | [<span data-ttu-id="15dc6-244">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="15dc6-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="15dc6-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15dc6-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="15dc6-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="15dc6-246">Entry</span></span> | <span data-ttu-id="15dc6-247">Value</span><span class="sxs-lookup"><span data-stu-id="15dc6-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15dc6-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15dc6-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15dc6-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="15dc6-250">System-Only</span></span>            | <span data-ttu-id="15dc6-251">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-251">False</span></span>                           |
| <span data-ttu-id="15dc6-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15dc6-252">Is-Single-Valued</span></span>       | <span data-ttu-id="15dc6-253">True</span><span class="sxs-lookup"><span data-stu-id="15dc6-253">True</span></span>                            |
| <span data-ttu-id="15dc6-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15dc6-254">Is Indexed</span></span>             | <span data-ttu-id="15dc6-255">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-255">False</span></span>                           |
| <span data-ttu-id="15dc6-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15dc6-256">In Global Catalog</span></span>      | <span data-ttu-id="15dc6-257">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-257">False</span></span>                           |
| <span data-ttu-id="15dc6-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15dc6-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="15dc6-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15dc6-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15dc6-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15dc6-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15dc6-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15dc6-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15dc6-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-262">Search-Flags</span></span>           | <span data-ttu-id="15dc6-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15dc6-263">0x00000000</span></span>                      |
| <span data-ttu-id="15dc6-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-264">System-Flags</span></span>           | <span data-ttu-id="15dc6-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15dc6-265">0x00000010</span></span>                      |
| <span data-ttu-id="15dc6-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15dc6-266">Classes used in</span></span>        | [<span data-ttu-id="15dc6-267">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="15dc6-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="15dc6-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15dc6-268">Windows Server 2012</span></span>



| <span data-ttu-id="15dc6-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="15dc6-269">Entry</span></span> | <span data-ttu-id="15dc6-270">Value</span><span class="sxs-lookup"><span data-stu-id="15dc6-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="15dc6-271">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="15dc6-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15dc6-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="15dc6-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="15dc6-273">System-Only</span></span>            | <span data-ttu-id="15dc6-274">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-274">False</span></span>                           |
| <span data-ttu-id="15dc6-275">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="15dc6-275">Is-Single-Valued</span></span>       | <span data-ttu-id="15dc6-276">True</span><span class="sxs-lookup"><span data-stu-id="15dc6-276">True</span></span>                            |
| <span data-ttu-id="15dc6-277">Está indexado</span><span class="sxs-lookup"><span data-stu-id="15dc6-277">Is Indexed</span></span>             | <span data-ttu-id="15dc6-278">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-278">False</span></span>                           |
| <span data-ttu-id="15dc6-279">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="15dc6-279">In Global Catalog</span></span>      | <span data-ttu-id="15dc6-280">False</span><span class="sxs-lookup"><span data-stu-id="15dc6-280">False</span></span>                           |
| <span data-ttu-id="15dc6-281">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="15dc6-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="15dc6-282">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="15dc6-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="15dc6-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15dc6-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="15dc6-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15dc6-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="15dc6-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-285">Search-Flags</span></span>           | <span data-ttu-id="15dc6-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="15dc6-286">0x00000000</span></span>                      |
| <span data-ttu-id="15dc6-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15dc6-287">System-Flags</span></span>           | <span data-ttu-id="15dc6-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15dc6-288">0x00000010</span></span>                      |
| <span data-ttu-id="15dc6-289">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="15dc6-289">Classes used in</span></span>        | [<span data-ttu-id="15dc6-290">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="15dc6-290">**Top**</span></span>](c-top.md)<br/> |



 

 






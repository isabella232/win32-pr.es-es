---
title: Atributo MS-DS-Consistency-Child-Count
description: Este atributo se usa para comprobar la coherencia entre el directorio y otro objeto, base de datos o aplicación mediante la comparación de un recuento de objetos secundarios.
ms.assetid: f7d6e8f0-963b-45a9-86af-8e51d6de32bb
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Consistency-Child-Count
- Esquema de AD del atributo mS-DS-ConsistencyChildCount
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Child-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b9c46d1c4519550a91d92d0a82f726a20572490
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151456"
---
# <a name="ms-ds-consistency-child-count-attribute"></a><span data-ttu-id="84f03-105">Atributo MS-DS-Consistency-Child-Count</span><span class="sxs-lookup"><span data-stu-id="84f03-105">MS-DS-Consistency-Child-Count attribute</span></span>

<span data-ttu-id="84f03-106">Este atributo se usa para comprobar la coherencia entre el directorio y otro objeto, base de datos o aplicación mediante la comparación de un recuento de objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="84f03-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing a count of child objects.</span></span>



| <span data-ttu-id="84f03-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="84f03-107">Entry</span></span> | <span data-ttu-id="84f03-108">Value</span><span class="sxs-lookup"><span data-stu-id="84f03-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="84f03-109">CN</span><span class="sxs-lookup"><span data-stu-id="84f03-109">CN</span></span>                | <span data-ttu-id="84f03-110">MS-DS-Consistency-Child-Count</span><span class="sxs-lookup"><span data-stu-id="84f03-110">MS-DS-Consistency-Child-Count</span></span>        |
| <span data-ttu-id="84f03-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="84f03-111">Ldap-Display-Name</span></span> | <span data-ttu-id="84f03-112">mS-DS-ConsistencyChildCount</span><span class="sxs-lookup"><span data-stu-id="84f03-112">mS-DS-ConsistencyChildCount</span></span>          |
| <span data-ttu-id="84f03-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="84f03-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="84f03-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="84f03-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="84f03-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="84f03-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="84f03-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="84f03-116">Attribute-Id</span></span>      | <span data-ttu-id="84f03-117">1.2.840.113556.1.4.1361</span><span class="sxs-lookup"><span data-stu-id="84f03-117">1.2.840.113556.1.4.1361</span></span>              |
| <span data-ttu-id="84f03-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="84f03-118">System-Id-Guid</span></span>    | <span data-ttu-id="84f03-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="84f03-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span></span> |
| <span data-ttu-id="84f03-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84f03-120">Syntax</span></span>            | [<span data-ttu-id="84f03-121">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="84f03-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="84f03-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="84f03-122">Implementations</span></span>

-   [<span data-ttu-id="84f03-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="84f03-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="84f03-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="84f03-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="84f03-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="84f03-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="84f03-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="84f03-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="84f03-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="84f03-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="84f03-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="84f03-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="84f03-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="84f03-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="84f03-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="84f03-130">Windows 2000 Server</span></span>



| <span data-ttu-id="84f03-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="84f03-131">Entry</span></span> | <span data-ttu-id="84f03-132">Value</span><span class="sxs-lookup"><span data-stu-id="84f03-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="84f03-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="84f03-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f03-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f03-135">System-Only</span></span>            | <span data-ttu-id="84f03-136">False</span><span class="sxs-lookup"><span data-stu-id="84f03-136">False</span></span>                           |
| <span data-ttu-id="84f03-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="84f03-137">Is-Single-Valued</span></span>       | <span data-ttu-id="84f03-138">True</span><span class="sxs-lookup"><span data-stu-id="84f03-138">True</span></span>                            |
| <span data-ttu-id="84f03-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="84f03-139">Is Indexed</span></span>             | <span data-ttu-id="84f03-140">False</span><span class="sxs-lookup"><span data-stu-id="84f03-140">False</span></span>                           |
| <span data-ttu-id="84f03-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="84f03-141">In Global Catalog</span></span>      | <span data-ttu-id="84f03-142">False</span><span class="sxs-lookup"><span data-stu-id="84f03-142">False</span></span>                           |
| <span data-ttu-id="84f03-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="84f03-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f03-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f03-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="84f03-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f03-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="84f03-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f03-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="84f03-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-147">Search-Flags</span></span>           | <span data-ttu-id="84f03-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f03-148">0x00000000</span></span>                      |
| <span data-ttu-id="84f03-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-149">System-Flags</span></span>           | <span data-ttu-id="84f03-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f03-150">0x00000010</span></span>                      |
| <span data-ttu-id="84f03-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="84f03-151">Classes used in</span></span>        | [<span data-ttu-id="84f03-152">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="84f03-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="84f03-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84f03-153">Windows Server 2003</span></span>



| <span data-ttu-id="84f03-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="84f03-154">Entry</span></span> | <span data-ttu-id="84f03-155">Value</span><span class="sxs-lookup"><span data-stu-id="84f03-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="84f03-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="84f03-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f03-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f03-158">System-Only</span></span>            | <span data-ttu-id="84f03-159">False</span><span class="sxs-lookup"><span data-stu-id="84f03-159">False</span></span>                           |
| <span data-ttu-id="84f03-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="84f03-160">Is-Single-Valued</span></span>       | <span data-ttu-id="84f03-161">True</span><span class="sxs-lookup"><span data-stu-id="84f03-161">True</span></span>                            |
| <span data-ttu-id="84f03-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="84f03-162">Is Indexed</span></span>             | <span data-ttu-id="84f03-163">False</span><span class="sxs-lookup"><span data-stu-id="84f03-163">False</span></span>                           |
| <span data-ttu-id="84f03-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="84f03-164">In Global Catalog</span></span>      | <span data-ttu-id="84f03-165">False</span><span class="sxs-lookup"><span data-stu-id="84f03-165">False</span></span>                           |
| <span data-ttu-id="84f03-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="84f03-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f03-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f03-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="84f03-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f03-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="84f03-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f03-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="84f03-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-170">Search-Flags</span></span>           | <span data-ttu-id="84f03-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f03-171">0x00000000</span></span>                      |
| <span data-ttu-id="84f03-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-172">System-Flags</span></span>           | <span data-ttu-id="84f03-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f03-173">0x00000010</span></span>                      |
| <span data-ttu-id="84f03-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="84f03-174">Classes used in</span></span>        | [<span data-ttu-id="84f03-175">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="84f03-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="84f03-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="84f03-176">ADAM</span></span>



| <span data-ttu-id="84f03-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="84f03-177">Entry</span></span> | <span data-ttu-id="84f03-178">Value</span><span class="sxs-lookup"><span data-stu-id="84f03-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="84f03-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="84f03-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f03-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f03-181">System-Only</span></span>            | <span data-ttu-id="84f03-182">False</span><span class="sxs-lookup"><span data-stu-id="84f03-182">False</span></span>                           |
| <span data-ttu-id="84f03-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="84f03-183">Is-Single-Valued</span></span>       | <span data-ttu-id="84f03-184">True</span><span class="sxs-lookup"><span data-stu-id="84f03-184">True</span></span>                            |
| <span data-ttu-id="84f03-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="84f03-185">Is Indexed</span></span>             | <span data-ttu-id="84f03-186">False</span><span class="sxs-lookup"><span data-stu-id="84f03-186">False</span></span>                           |
| <span data-ttu-id="84f03-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="84f03-187">In Global Catalog</span></span>      | <span data-ttu-id="84f03-188">False</span><span class="sxs-lookup"><span data-stu-id="84f03-188">False</span></span>                           |
| <span data-ttu-id="84f03-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="84f03-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f03-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f03-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="84f03-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f03-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="84f03-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f03-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="84f03-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-193">Search-Flags</span></span>           | <span data-ttu-id="84f03-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f03-194">0x00000000</span></span>                      |
| <span data-ttu-id="84f03-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-195">System-Flags</span></span>           | <span data-ttu-id="84f03-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f03-196">0x00000010</span></span>                      |
| <span data-ttu-id="84f03-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="84f03-197">Classes used in</span></span>        | [<span data-ttu-id="84f03-198">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="84f03-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="84f03-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="84f03-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="84f03-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="84f03-200">Entry</span></span> | <span data-ttu-id="84f03-201">Value</span><span class="sxs-lookup"><span data-stu-id="84f03-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="84f03-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="84f03-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f03-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f03-204">System-Only</span></span>            | <span data-ttu-id="84f03-205">False</span><span class="sxs-lookup"><span data-stu-id="84f03-205">False</span></span>                           |
| <span data-ttu-id="84f03-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="84f03-206">Is-Single-Valued</span></span>       | <span data-ttu-id="84f03-207">True</span><span class="sxs-lookup"><span data-stu-id="84f03-207">True</span></span>                            |
| <span data-ttu-id="84f03-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="84f03-208">Is Indexed</span></span>             | <span data-ttu-id="84f03-209">False</span><span class="sxs-lookup"><span data-stu-id="84f03-209">False</span></span>                           |
| <span data-ttu-id="84f03-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="84f03-210">In Global Catalog</span></span>      | <span data-ttu-id="84f03-211">False</span><span class="sxs-lookup"><span data-stu-id="84f03-211">False</span></span>                           |
| <span data-ttu-id="84f03-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="84f03-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f03-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f03-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="84f03-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f03-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="84f03-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f03-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="84f03-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-216">Search-Flags</span></span>           | <span data-ttu-id="84f03-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f03-217">0x00000000</span></span>                      |
| <span data-ttu-id="84f03-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-218">System-Flags</span></span>           | <span data-ttu-id="84f03-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f03-219">0x00000010</span></span>                      |
| <span data-ttu-id="84f03-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="84f03-220">Classes used in</span></span>        | [<span data-ttu-id="84f03-221">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="84f03-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="84f03-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84f03-222">Windows Server 2008</span></span>



| <span data-ttu-id="84f03-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="84f03-223">Entry</span></span> | <span data-ttu-id="84f03-224">Value</span><span class="sxs-lookup"><span data-stu-id="84f03-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="84f03-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="84f03-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f03-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f03-227">System-Only</span></span>            | <span data-ttu-id="84f03-228">False</span><span class="sxs-lookup"><span data-stu-id="84f03-228">False</span></span>                           |
| <span data-ttu-id="84f03-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="84f03-229">Is-Single-Valued</span></span>       | <span data-ttu-id="84f03-230">True</span><span class="sxs-lookup"><span data-stu-id="84f03-230">True</span></span>                            |
| <span data-ttu-id="84f03-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="84f03-231">Is Indexed</span></span>             | <span data-ttu-id="84f03-232">False</span><span class="sxs-lookup"><span data-stu-id="84f03-232">False</span></span>                           |
| <span data-ttu-id="84f03-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="84f03-233">In Global Catalog</span></span>      | <span data-ttu-id="84f03-234">False</span><span class="sxs-lookup"><span data-stu-id="84f03-234">False</span></span>                           |
| <span data-ttu-id="84f03-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="84f03-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f03-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f03-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="84f03-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f03-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="84f03-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f03-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="84f03-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-239">Search-Flags</span></span>           | <span data-ttu-id="84f03-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f03-240">0x00000000</span></span>                      |
| <span data-ttu-id="84f03-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-241">System-Flags</span></span>           | <span data-ttu-id="84f03-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f03-242">0x00000010</span></span>                      |
| <span data-ttu-id="84f03-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="84f03-243">Classes used in</span></span>        | [<span data-ttu-id="84f03-244">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="84f03-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="84f03-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84f03-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="84f03-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="84f03-246">Entry</span></span> | <span data-ttu-id="84f03-247">Value</span><span class="sxs-lookup"><span data-stu-id="84f03-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="84f03-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="84f03-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f03-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f03-250">System-Only</span></span>            | <span data-ttu-id="84f03-251">False</span><span class="sxs-lookup"><span data-stu-id="84f03-251">False</span></span>                           |
| <span data-ttu-id="84f03-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="84f03-252">Is-Single-Valued</span></span>       | <span data-ttu-id="84f03-253">True</span><span class="sxs-lookup"><span data-stu-id="84f03-253">True</span></span>                            |
| <span data-ttu-id="84f03-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="84f03-254">Is Indexed</span></span>             | <span data-ttu-id="84f03-255">False</span><span class="sxs-lookup"><span data-stu-id="84f03-255">False</span></span>                           |
| <span data-ttu-id="84f03-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="84f03-256">In Global Catalog</span></span>      | <span data-ttu-id="84f03-257">False</span><span class="sxs-lookup"><span data-stu-id="84f03-257">False</span></span>                           |
| <span data-ttu-id="84f03-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="84f03-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f03-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f03-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="84f03-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f03-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="84f03-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f03-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="84f03-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-262">Search-Flags</span></span>           | <span data-ttu-id="84f03-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f03-263">0x00000000</span></span>                      |
| <span data-ttu-id="84f03-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-264">System-Flags</span></span>           | <span data-ttu-id="84f03-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f03-265">0x00000010</span></span>                      |
| <span data-ttu-id="84f03-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="84f03-266">Classes used in</span></span>        | [<span data-ttu-id="84f03-267">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="84f03-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="84f03-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84f03-268">Windows Server 2012</span></span>



| <span data-ttu-id="84f03-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="84f03-269">Entry</span></span> | <span data-ttu-id="84f03-270">Value</span><span class="sxs-lookup"><span data-stu-id="84f03-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="84f03-271">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="84f03-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84f03-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="84f03-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="84f03-273">System-Only</span></span>            | <span data-ttu-id="84f03-274">False</span><span class="sxs-lookup"><span data-stu-id="84f03-274">False</span></span>                           |
| <span data-ttu-id="84f03-275">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="84f03-275">Is-Single-Valued</span></span>       | <span data-ttu-id="84f03-276">True</span><span class="sxs-lookup"><span data-stu-id="84f03-276">True</span></span>                            |
| <span data-ttu-id="84f03-277">Está indexado</span><span class="sxs-lookup"><span data-stu-id="84f03-277">Is Indexed</span></span>             | <span data-ttu-id="84f03-278">False</span><span class="sxs-lookup"><span data-stu-id="84f03-278">False</span></span>                           |
| <span data-ttu-id="84f03-279">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="84f03-279">In Global Catalog</span></span>      | <span data-ttu-id="84f03-280">False</span><span class="sxs-lookup"><span data-stu-id="84f03-280">False</span></span>                           |
| <span data-ttu-id="84f03-281">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="84f03-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="84f03-282">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="84f03-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="84f03-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84f03-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="84f03-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84f03-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="84f03-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-285">Search-Flags</span></span>           | <span data-ttu-id="84f03-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84f03-286">0x00000000</span></span>                      |
| <span data-ttu-id="84f03-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84f03-287">System-Flags</span></span>           | <span data-ttu-id="84f03-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84f03-288">0x00000010</span></span>                      |
| <span data-ttu-id="84f03-289">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="84f03-289">Classes used in</span></span>        | [<span data-ttu-id="84f03-290">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="84f03-290">**Top**</span></span>](c-top.md)<br/> |



 

 






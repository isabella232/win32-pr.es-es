---
title: DSA-Signature atributo)
description: El DSA-Signature de un objeto es el identificador de invocación del último directorio en el que se va a modificar el objeto.
ms.assetid: 7ae65f15-b0c9-4d73-8a65-92c23d0a239b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de DSA-Signature
- dSASignature esquema de AD de atributos
topic_type:
- apiref
api_name:
- DSA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfed9e2cb871f3418c8bdbf4401d03c1e78492b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658549"
---
# <a name="dsa-signature-attribute"></a><span data-ttu-id="73960-105">DSA-Signature atributo)</span><span class="sxs-lookup"><span data-stu-id="73960-105">DSA-Signature attribute</span></span>

<span data-ttu-id="73960-106">El DSA-Signature de un objeto es el identificador de invocación del último directorio en el que se va a modificar el objeto.</span><span class="sxs-lookup"><span data-stu-id="73960-106">The DSA-Signature of an object is the Invocation-ID of the last directory to modify the object.</span></span>



| <span data-ttu-id="73960-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="73960-107">Entry</span></span> | <span data-ttu-id="73960-108">Value</span><span class="sxs-lookup"><span data-stu-id="73960-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="73960-109">CN</span><span class="sxs-lookup"><span data-stu-id="73960-109">CN</span></span>                | <span data-ttu-id="73960-110">DSA-Signature</span><span class="sxs-lookup"><span data-stu-id="73960-110">DSA-Signature</span></span>                                         |
| <span data-ttu-id="73960-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="73960-111">Ldap-Display-Name</span></span> | <span data-ttu-id="73960-112">dSASignature</span><span class="sxs-lookup"><span data-stu-id="73960-112">dSASignature</span></span>                                          |
| <span data-ttu-id="73960-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="73960-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="73960-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="73960-114">Update Privilege</span></span>  | <span data-ttu-id="73960-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="73960-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="73960-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="73960-116">Update Frequency</span></span>  | <span data-ttu-id="73960-117">Cada vez que se modifica un objeto.</span><span class="sxs-lookup"><span data-stu-id="73960-117">Whenever an object is modified.</span></span>                       |
| <span data-ttu-id="73960-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="73960-118">Attribute-Id</span></span>      | <span data-ttu-id="73960-119">1.2.840.113556.1.2.74</span><span class="sxs-lookup"><span data-stu-id="73960-119">1.2.840.113556.1.2.74</span></span>                                 |
| <span data-ttu-id="73960-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="73960-120">System-Id-Guid</span></span>    | <span data-ttu-id="73960-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="73960-121">167757bc-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="73960-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73960-122">Syntax</span></span>            | [<span data-ttu-id="73960-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="73960-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="73960-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="73960-124">Implementations</span></span>

-   [<span data-ttu-id="73960-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="73960-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="73960-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="73960-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="73960-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="73960-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="73960-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="73960-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="73960-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="73960-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="73960-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="73960-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="73960-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="73960-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="73960-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="73960-132">Windows 2000 Server</span></span>



| <span data-ttu-id="73960-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="73960-133">Entry</span></span> | <span data-ttu-id="73960-134">Value</span><span class="sxs-lookup"><span data-stu-id="73960-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="73960-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="73960-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="73960-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73960-136">MAPI-Id</span></span>                | <span data-ttu-id="73960-137">0x8077</span><span class="sxs-lookup"><span data-stu-id="73960-137">0x8077</span></span>                          |
| <span data-ttu-id="73960-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="73960-138">System-Only</span></span>            | <span data-ttu-id="73960-139">False</span><span class="sxs-lookup"><span data-stu-id="73960-139">False</span></span>                           |
| <span data-ttu-id="73960-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="73960-140">Is-Single-Valued</span></span>       | <span data-ttu-id="73960-141">True</span><span class="sxs-lookup"><span data-stu-id="73960-141">True</span></span>                            |
| <span data-ttu-id="73960-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="73960-142">Is Indexed</span></span>             | <span data-ttu-id="73960-143">False</span><span class="sxs-lookup"><span data-stu-id="73960-143">False</span></span>                           |
| <span data-ttu-id="73960-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="73960-144">In Global Catalog</span></span>      | <span data-ttu-id="73960-145">False</span><span class="sxs-lookup"><span data-stu-id="73960-145">False</span></span>                           |
| <span data-ttu-id="73960-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="73960-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="73960-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73960-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="73960-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73960-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="73960-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73960-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="73960-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-150">Search-Flags</span></span>           | <span data-ttu-id="73960-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73960-151">0x00000000</span></span>                      |
| <span data-ttu-id="73960-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-152">System-Flags</span></span>           | <span data-ttu-id="73960-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73960-153">0x00000010</span></span>                      |
| <span data-ttu-id="73960-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="73960-154">Classes used in</span></span>        | [<span data-ttu-id="73960-155">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="73960-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="73960-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="73960-156">Windows Server 2003</span></span>



| <span data-ttu-id="73960-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="73960-157">Entry</span></span> | <span data-ttu-id="73960-158">Value</span><span class="sxs-lookup"><span data-stu-id="73960-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="73960-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="73960-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="73960-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73960-160">MAPI-Id</span></span>                | <span data-ttu-id="73960-161">0x8077</span><span class="sxs-lookup"><span data-stu-id="73960-161">0x8077</span></span>                          |
| <span data-ttu-id="73960-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="73960-162">System-Only</span></span>            | <span data-ttu-id="73960-163">False</span><span class="sxs-lookup"><span data-stu-id="73960-163">False</span></span>                           |
| <span data-ttu-id="73960-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="73960-164">Is-Single-Valued</span></span>       | <span data-ttu-id="73960-165">True</span><span class="sxs-lookup"><span data-stu-id="73960-165">True</span></span>                            |
| <span data-ttu-id="73960-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="73960-166">Is Indexed</span></span>             | <span data-ttu-id="73960-167">False</span><span class="sxs-lookup"><span data-stu-id="73960-167">False</span></span>                           |
| <span data-ttu-id="73960-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="73960-168">In Global Catalog</span></span>      | <span data-ttu-id="73960-169">False</span><span class="sxs-lookup"><span data-stu-id="73960-169">False</span></span>                           |
| <span data-ttu-id="73960-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="73960-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="73960-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73960-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="73960-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73960-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="73960-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73960-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="73960-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-174">Search-Flags</span></span>           | <span data-ttu-id="73960-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73960-175">0x00000000</span></span>                      |
| <span data-ttu-id="73960-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-176">System-Flags</span></span>           | <span data-ttu-id="73960-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73960-177">0x00000010</span></span>                      |
| <span data-ttu-id="73960-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="73960-178">Classes used in</span></span>        | [<span data-ttu-id="73960-179">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="73960-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="73960-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="73960-180">ADAM</span></span>



| <span data-ttu-id="73960-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="73960-181">Entry</span></span> | <span data-ttu-id="73960-182">Value</span><span class="sxs-lookup"><span data-stu-id="73960-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="73960-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="73960-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="73960-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73960-184">MAPI-Id</span></span>                | <span data-ttu-id="73960-185">0x8077</span><span class="sxs-lookup"><span data-stu-id="73960-185">0x8077</span></span>                          |
| <span data-ttu-id="73960-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="73960-186">System-Only</span></span>            | <span data-ttu-id="73960-187">False</span><span class="sxs-lookup"><span data-stu-id="73960-187">False</span></span>                           |
| <span data-ttu-id="73960-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="73960-188">Is-Single-Valued</span></span>       | <span data-ttu-id="73960-189">True</span><span class="sxs-lookup"><span data-stu-id="73960-189">True</span></span>                            |
| <span data-ttu-id="73960-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="73960-190">Is Indexed</span></span>             | <span data-ttu-id="73960-191">False</span><span class="sxs-lookup"><span data-stu-id="73960-191">False</span></span>                           |
| <span data-ttu-id="73960-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="73960-192">In Global Catalog</span></span>      | <span data-ttu-id="73960-193">False</span><span class="sxs-lookup"><span data-stu-id="73960-193">False</span></span>                           |
| <span data-ttu-id="73960-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="73960-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="73960-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73960-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="73960-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73960-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="73960-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73960-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="73960-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-198">Search-Flags</span></span>           | <span data-ttu-id="73960-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73960-199">0x00000000</span></span>                      |
| <span data-ttu-id="73960-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-200">System-Flags</span></span>           | <span data-ttu-id="73960-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73960-201">0x00000010</span></span>                      |
| <span data-ttu-id="73960-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="73960-202">Classes used in</span></span>        | [<span data-ttu-id="73960-203">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="73960-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="73960-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="73960-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="73960-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="73960-205">Entry</span></span> | <span data-ttu-id="73960-206">Value</span><span class="sxs-lookup"><span data-stu-id="73960-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="73960-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="73960-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="73960-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73960-208">MAPI-Id</span></span>                | <span data-ttu-id="73960-209">0x8077</span><span class="sxs-lookup"><span data-stu-id="73960-209">0x8077</span></span>                          |
| <span data-ttu-id="73960-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="73960-210">System-Only</span></span>            | <span data-ttu-id="73960-211">False</span><span class="sxs-lookup"><span data-stu-id="73960-211">False</span></span>                           |
| <span data-ttu-id="73960-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="73960-212">Is-Single-Valued</span></span>       | <span data-ttu-id="73960-213">True</span><span class="sxs-lookup"><span data-stu-id="73960-213">True</span></span>                            |
| <span data-ttu-id="73960-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="73960-214">Is Indexed</span></span>             | <span data-ttu-id="73960-215">False</span><span class="sxs-lookup"><span data-stu-id="73960-215">False</span></span>                           |
| <span data-ttu-id="73960-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="73960-216">In Global Catalog</span></span>      | <span data-ttu-id="73960-217">False</span><span class="sxs-lookup"><span data-stu-id="73960-217">False</span></span>                           |
| <span data-ttu-id="73960-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="73960-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="73960-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73960-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="73960-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73960-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="73960-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73960-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="73960-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-222">Search-Flags</span></span>           | <span data-ttu-id="73960-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73960-223">0x00000000</span></span>                      |
| <span data-ttu-id="73960-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-224">System-Flags</span></span>           | <span data-ttu-id="73960-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73960-225">0x00000010</span></span>                      |
| <span data-ttu-id="73960-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="73960-226">Classes used in</span></span>        | [<span data-ttu-id="73960-227">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="73960-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="73960-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73960-228">Windows Server 2008</span></span>



| <span data-ttu-id="73960-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="73960-229">Entry</span></span> | <span data-ttu-id="73960-230">Value</span><span class="sxs-lookup"><span data-stu-id="73960-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="73960-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="73960-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="73960-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73960-232">MAPI-Id</span></span>                | <span data-ttu-id="73960-233">0x8077</span><span class="sxs-lookup"><span data-stu-id="73960-233">0x8077</span></span>                          |
| <span data-ttu-id="73960-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="73960-234">System-Only</span></span>            | <span data-ttu-id="73960-235">False</span><span class="sxs-lookup"><span data-stu-id="73960-235">False</span></span>                           |
| <span data-ttu-id="73960-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="73960-236">Is-Single-Valued</span></span>       | <span data-ttu-id="73960-237">True</span><span class="sxs-lookup"><span data-stu-id="73960-237">True</span></span>                            |
| <span data-ttu-id="73960-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="73960-238">Is Indexed</span></span>             | <span data-ttu-id="73960-239">False</span><span class="sxs-lookup"><span data-stu-id="73960-239">False</span></span>                           |
| <span data-ttu-id="73960-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="73960-240">In Global Catalog</span></span>      | <span data-ttu-id="73960-241">False</span><span class="sxs-lookup"><span data-stu-id="73960-241">False</span></span>                           |
| <span data-ttu-id="73960-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="73960-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="73960-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73960-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="73960-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73960-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="73960-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73960-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="73960-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-246">Search-Flags</span></span>           | <span data-ttu-id="73960-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73960-247">0x00000000</span></span>                      |
| <span data-ttu-id="73960-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-248">System-Flags</span></span>           | <span data-ttu-id="73960-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73960-249">0x00000010</span></span>                      |
| <span data-ttu-id="73960-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="73960-250">Classes used in</span></span>        | [<span data-ttu-id="73960-251">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="73960-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="73960-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="73960-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="73960-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="73960-253">Entry</span></span> | <span data-ttu-id="73960-254">Value</span><span class="sxs-lookup"><span data-stu-id="73960-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="73960-255">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="73960-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="73960-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73960-256">MAPI-Id</span></span>                | <span data-ttu-id="73960-257">0x8077</span><span class="sxs-lookup"><span data-stu-id="73960-257">0x8077</span></span>                          |
| <span data-ttu-id="73960-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="73960-258">System-Only</span></span>            | <span data-ttu-id="73960-259">False</span><span class="sxs-lookup"><span data-stu-id="73960-259">False</span></span>                           |
| <span data-ttu-id="73960-260">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="73960-260">Is-Single-Valued</span></span>       | <span data-ttu-id="73960-261">True</span><span class="sxs-lookup"><span data-stu-id="73960-261">True</span></span>                            |
| <span data-ttu-id="73960-262">Está indexado</span><span class="sxs-lookup"><span data-stu-id="73960-262">Is Indexed</span></span>             | <span data-ttu-id="73960-263">False</span><span class="sxs-lookup"><span data-stu-id="73960-263">False</span></span>                           |
| <span data-ttu-id="73960-264">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="73960-264">In Global Catalog</span></span>      | <span data-ttu-id="73960-265">False</span><span class="sxs-lookup"><span data-stu-id="73960-265">False</span></span>                           |
| <span data-ttu-id="73960-266">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="73960-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="73960-267">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73960-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="73960-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73960-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="73960-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73960-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="73960-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-270">Search-Flags</span></span>           | <span data-ttu-id="73960-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73960-271">0x00000000</span></span>                      |
| <span data-ttu-id="73960-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-272">System-Flags</span></span>           | <span data-ttu-id="73960-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73960-273">0x00000010</span></span>                      |
| <span data-ttu-id="73960-274">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="73960-274">Classes used in</span></span>        | [<span data-ttu-id="73960-275">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="73960-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="73960-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73960-276">Windows Server 2012</span></span>



| <span data-ttu-id="73960-277">Entrada</span><span class="sxs-lookup"><span data-stu-id="73960-277">Entry</span></span> | <span data-ttu-id="73960-278">Value</span><span class="sxs-lookup"><span data-stu-id="73960-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="73960-279">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="73960-279">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="73960-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="73960-280">MAPI-Id</span></span>                | <span data-ttu-id="73960-281">0x8077</span><span class="sxs-lookup"><span data-stu-id="73960-281">0x8077</span></span>                          |
| <span data-ttu-id="73960-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="73960-282">System-Only</span></span>            | <span data-ttu-id="73960-283">False</span><span class="sxs-lookup"><span data-stu-id="73960-283">False</span></span>                           |
| <span data-ttu-id="73960-284">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="73960-284">Is-Single-Valued</span></span>       | <span data-ttu-id="73960-285">True</span><span class="sxs-lookup"><span data-stu-id="73960-285">True</span></span>                            |
| <span data-ttu-id="73960-286">Está indexado</span><span class="sxs-lookup"><span data-stu-id="73960-286">Is Indexed</span></span>             | <span data-ttu-id="73960-287">False</span><span class="sxs-lookup"><span data-stu-id="73960-287">False</span></span>                           |
| <span data-ttu-id="73960-288">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="73960-288">In Global Catalog</span></span>      | <span data-ttu-id="73960-289">False</span><span class="sxs-lookup"><span data-stu-id="73960-289">False</span></span>                           |
| <span data-ttu-id="73960-290">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="73960-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="73960-291">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="73960-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="73960-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="73960-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="73960-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="73960-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="73960-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-294">Search-Flags</span></span>           | <span data-ttu-id="73960-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="73960-295">0x00000000</span></span>                      |
| <span data-ttu-id="73960-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="73960-296">System-Flags</span></span>           | <span data-ttu-id="73960-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="73960-297">0x00000010</span></span>                      |
| <span data-ttu-id="73960-298">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="73960-298">Classes used in</span></span>        | [<span data-ttu-id="73960-299">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="73960-299">**Top**</span></span>](c-top.md)<br/> |



 

 






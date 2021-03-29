---
title: Atributo de clase de objeto estructural
description: Este atributo construido almacena una lista de clases contenidas en una jerarquía de clases, incluidas las clases abstractas. Esta lista contiene clases auxiliares vinculadas dinámicamente.
ms.assetid: f7311cb9-4816-4caa-9cae-cbcd61b93d27
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de clase de objeto estructural
- structuralObjectClass esquema de AD de atributos
topic_type:
- apiref
api_name:
- Structural-Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdcc236c0c65aa365400894dd6ccfb845af04b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658972"
---
# <a name="structural-object-class-attribute"></a><span data-ttu-id="747ee-106">Atributo de clase de objeto estructural</span><span class="sxs-lookup"><span data-stu-id="747ee-106">Structural-Object-Class attribute</span></span>

<span data-ttu-id="747ee-107">Este atributo construido almacena una lista de clases contenidas en una jerarquía de clases, incluidas las clases abstractas.</span><span class="sxs-lookup"><span data-stu-id="747ee-107">This constructed attribute stores a list of classes contained in a class hierarchy, including abstract classes.</span></span> <span data-ttu-id="747ee-108">Esta lista contiene clases auxiliares vinculadas dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="747ee-108">This list does contain dynamically linked auxiliary classes.</span></span>



| <span data-ttu-id="747ee-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="747ee-109">Entry</span></span> | <span data-ttu-id="747ee-110">Value</span><span class="sxs-lookup"><span data-stu-id="747ee-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="747ee-111">CN</span><span class="sxs-lookup"><span data-stu-id="747ee-111">CN</span></span>                | <span data-ttu-id="747ee-112">Clase de objeto estructural</span><span class="sxs-lookup"><span data-stu-id="747ee-112">Structural-Object-Class</span></span>                                         |
| <span data-ttu-id="747ee-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="747ee-113">Ldap-Display-Name</span></span> | <span data-ttu-id="747ee-114">structuralObjectClass</span><span class="sxs-lookup"><span data-stu-id="747ee-114">structuralObjectClass</span></span>                                           |
| <span data-ttu-id="747ee-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="747ee-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="747ee-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="747ee-116">Update Privilege</span></span>  | <span data-ttu-id="747ee-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="747ee-117">This value is set by the system.</span></span>                                |
| <span data-ttu-id="747ee-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="747ee-118">Update Frequency</span></span>  | <span data-ttu-id="747ee-119">Al crear la clase.</span><span class="sxs-lookup"><span data-stu-id="747ee-119">At class creation.</span></span>                                              |
| <span data-ttu-id="747ee-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="747ee-120">Attribute-Id</span></span>      | <span data-ttu-id="747ee-121">2.5.21.9</span><span class="sxs-lookup"><span data-stu-id="747ee-121">2.5.21.9</span></span>                                                        |
| <span data-ttu-id="747ee-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="747ee-122">System-Id-Guid</span></span>    | <span data-ttu-id="747ee-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span><span class="sxs-lookup"><span data-stu-id="747ee-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span></span>                            |
| <span data-ttu-id="747ee-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="747ee-124">Syntax</span></span>            | [<span data-ttu-id="747ee-125">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="747ee-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="747ee-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="747ee-126">Implementations</span></span>

-   [<span data-ttu-id="747ee-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="747ee-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="747ee-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="747ee-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="747ee-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="747ee-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="747ee-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="747ee-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="747ee-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="747ee-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="747ee-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="747ee-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="747ee-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="747ee-133">Windows Server 2003</span></span>



| <span data-ttu-id="747ee-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="747ee-134">Entry</span></span> | <span data-ttu-id="747ee-135">Value</span><span class="sxs-lookup"><span data-stu-id="747ee-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="747ee-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="747ee-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="747ee-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="747ee-138">System-Only</span></span>            | <span data-ttu-id="747ee-139">False</span><span class="sxs-lookup"><span data-stu-id="747ee-139">False</span></span>                           |
| <span data-ttu-id="747ee-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="747ee-140">Is-Single-Valued</span></span>       | <span data-ttu-id="747ee-141">False</span><span class="sxs-lookup"><span data-stu-id="747ee-141">False</span></span>                           |
| <span data-ttu-id="747ee-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="747ee-142">Is Indexed</span></span>             | <span data-ttu-id="747ee-143">False</span><span class="sxs-lookup"><span data-stu-id="747ee-143">False</span></span>                           |
| <span data-ttu-id="747ee-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="747ee-144">In Global Catalog</span></span>      | <span data-ttu-id="747ee-145">False</span><span class="sxs-lookup"><span data-stu-id="747ee-145">False</span></span>                           |
| <span data-ttu-id="747ee-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="747ee-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="747ee-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="747ee-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="747ee-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="747ee-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="747ee-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="747ee-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="747ee-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-150">Search-Flags</span></span>           | <span data-ttu-id="747ee-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="747ee-151">0x00000000</span></span>                      |
| <span data-ttu-id="747ee-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-152">System-Flags</span></span>           | <span data-ttu-id="747ee-153">0x00000014</span><span class="sxs-lookup"><span data-stu-id="747ee-153">0x00000014</span></span>                      |
| <span data-ttu-id="747ee-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="747ee-154">Classes used in</span></span>        | [<span data-ttu-id="747ee-155">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="747ee-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="747ee-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="747ee-156">ADAM</span></span>



| <span data-ttu-id="747ee-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="747ee-157">Entry</span></span> | <span data-ttu-id="747ee-158">Value</span><span class="sxs-lookup"><span data-stu-id="747ee-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="747ee-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="747ee-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="747ee-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="747ee-161">System-Only</span></span>            | <span data-ttu-id="747ee-162">False</span><span class="sxs-lookup"><span data-stu-id="747ee-162">False</span></span>                           |
| <span data-ttu-id="747ee-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="747ee-163">Is-Single-Valued</span></span>       | <span data-ttu-id="747ee-164">False</span><span class="sxs-lookup"><span data-stu-id="747ee-164">False</span></span>                           |
| <span data-ttu-id="747ee-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="747ee-165">Is Indexed</span></span>             | <span data-ttu-id="747ee-166">False</span><span class="sxs-lookup"><span data-stu-id="747ee-166">False</span></span>                           |
| <span data-ttu-id="747ee-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="747ee-167">In Global Catalog</span></span>      | <span data-ttu-id="747ee-168">False</span><span class="sxs-lookup"><span data-stu-id="747ee-168">False</span></span>                           |
| <span data-ttu-id="747ee-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="747ee-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="747ee-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="747ee-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="747ee-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="747ee-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="747ee-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="747ee-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="747ee-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-173">Search-Flags</span></span>           | <span data-ttu-id="747ee-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="747ee-174">0x00000000</span></span>                      |
| <span data-ttu-id="747ee-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-175">System-Flags</span></span>           | <span data-ttu-id="747ee-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="747ee-176">0x00000014</span></span>                      |
| <span data-ttu-id="747ee-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="747ee-177">Classes used in</span></span>        | [<span data-ttu-id="747ee-178">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="747ee-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="747ee-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="747ee-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="747ee-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="747ee-180">Entry</span></span> | <span data-ttu-id="747ee-181">Value</span><span class="sxs-lookup"><span data-stu-id="747ee-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="747ee-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="747ee-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="747ee-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="747ee-184">System-Only</span></span>            | <span data-ttu-id="747ee-185">False</span><span class="sxs-lookup"><span data-stu-id="747ee-185">False</span></span>                           |
| <span data-ttu-id="747ee-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="747ee-186">Is-Single-Valued</span></span>       | <span data-ttu-id="747ee-187">False</span><span class="sxs-lookup"><span data-stu-id="747ee-187">False</span></span>                           |
| <span data-ttu-id="747ee-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="747ee-188">Is Indexed</span></span>             | <span data-ttu-id="747ee-189">False</span><span class="sxs-lookup"><span data-stu-id="747ee-189">False</span></span>                           |
| <span data-ttu-id="747ee-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="747ee-190">In Global Catalog</span></span>      | <span data-ttu-id="747ee-191">False</span><span class="sxs-lookup"><span data-stu-id="747ee-191">False</span></span>                           |
| <span data-ttu-id="747ee-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="747ee-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="747ee-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="747ee-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="747ee-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="747ee-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="747ee-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="747ee-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="747ee-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-196">Search-Flags</span></span>           | <span data-ttu-id="747ee-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="747ee-197">0x00000000</span></span>                      |
| <span data-ttu-id="747ee-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-198">System-Flags</span></span>           | <span data-ttu-id="747ee-199">0x00000014</span><span class="sxs-lookup"><span data-stu-id="747ee-199">0x00000014</span></span>                      |
| <span data-ttu-id="747ee-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="747ee-200">Classes used in</span></span>        | [<span data-ttu-id="747ee-201">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="747ee-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="747ee-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="747ee-202">Windows Server 2008</span></span>



| <span data-ttu-id="747ee-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="747ee-203">Entry</span></span> | <span data-ttu-id="747ee-204">Value</span><span class="sxs-lookup"><span data-stu-id="747ee-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="747ee-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="747ee-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="747ee-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="747ee-207">System-Only</span></span>            | <span data-ttu-id="747ee-208">False</span><span class="sxs-lookup"><span data-stu-id="747ee-208">False</span></span>                           |
| <span data-ttu-id="747ee-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="747ee-209">Is-Single-Valued</span></span>       | <span data-ttu-id="747ee-210">False</span><span class="sxs-lookup"><span data-stu-id="747ee-210">False</span></span>                           |
| <span data-ttu-id="747ee-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="747ee-211">Is Indexed</span></span>             | <span data-ttu-id="747ee-212">False</span><span class="sxs-lookup"><span data-stu-id="747ee-212">False</span></span>                           |
| <span data-ttu-id="747ee-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="747ee-213">In Global Catalog</span></span>      | <span data-ttu-id="747ee-214">False</span><span class="sxs-lookup"><span data-stu-id="747ee-214">False</span></span>                           |
| <span data-ttu-id="747ee-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="747ee-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="747ee-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="747ee-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="747ee-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="747ee-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="747ee-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="747ee-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="747ee-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-219">Search-Flags</span></span>           | <span data-ttu-id="747ee-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="747ee-220">0x00000000</span></span>                      |
| <span data-ttu-id="747ee-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-221">System-Flags</span></span>           | <span data-ttu-id="747ee-222">0x00000014</span><span class="sxs-lookup"><span data-stu-id="747ee-222">0x00000014</span></span>                      |
| <span data-ttu-id="747ee-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="747ee-223">Classes used in</span></span>        | [<span data-ttu-id="747ee-224">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="747ee-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="747ee-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="747ee-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="747ee-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="747ee-226">Entry</span></span> | <span data-ttu-id="747ee-227">Value</span><span class="sxs-lookup"><span data-stu-id="747ee-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="747ee-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="747ee-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="747ee-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="747ee-230">System-Only</span></span>            | <span data-ttu-id="747ee-231">False</span><span class="sxs-lookup"><span data-stu-id="747ee-231">False</span></span>                           |
| <span data-ttu-id="747ee-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="747ee-232">Is-Single-Valued</span></span>       | <span data-ttu-id="747ee-233">False</span><span class="sxs-lookup"><span data-stu-id="747ee-233">False</span></span>                           |
| <span data-ttu-id="747ee-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="747ee-234">Is Indexed</span></span>             | <span data-ttu-id="747ee-235">False</span><span class="sxs-lookup"><span data-stu-id="747ee-235">False</span></span>                           |
| <span data-ttu-id="747ee-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="747ee-236">In Global Catalog</span></span>      | <span data-ttu-id="747ee-237">False</span><span class="sxs-lookup"><span data-stu-id="747ee-237">False</span></span>                           |
| <span data-ttu-id="747ee-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="747ee-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="747ee-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="747ee-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="747ee-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="747ee-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="747ee-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="747ee-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="747ee-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-242">Search-Flags</span></span>           | <span data-ttu-id="747ee-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="747ee-243">0x00000000</span></span>                      |
| <span data-ttu-id="747ee-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-244">System-Flags</span></span>           | <span data-ttu-id="747ee-245">0x00000014</span><span class="sxs-lookup"><span data-stu-id="747ee-245">0x00000014</span></span>                      |
| <span data-ttu-id="747ee-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="747ee-246">Classes used in</span></span>        | [<span data-ttu-id="747ee-247">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="747ee-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="747ee-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="747ee-248">Windows Server 2012</span></span>



| <span data-ttu-id="747ee-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="747ee-249">Entry</span></span> | <span data-ttu-id="747ee-250">Value</span><span class="sxs-lookup"><span data-stu-id="747ee-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="747ee-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="747ee-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="747ee-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="747ee-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="747ee-253">System-Only</span></span>            | <span data-ttu-id="747ee-254">False</span><span class="sxs-lookup"><span data-stu-id="747ee-254">False</span></span>                           |
| <span data-ttu-id="747ee-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="747ee-255">Is-Single-Valued</span></span>       | <span data-ttu-id="747ee-256">False</span><span class="sxs-lookup"><span data-stu-id="747ee-256">False</span></span>                           |
| <span data-ttu-id="747ee-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="747ee-257">Is Indexed</span></span>             | <span data-ttu-id="747ee-258">False</span><span class="sxs-lookup"><span data-stu-id="747ee-258">False</span></span>                           |
| <span data-ttu-id="747ee-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="747ee-259">In Global Catalog</span></span>      | <span data-ttu-id="747ee-260">False</span><span class="sxs-lookup"><span data-stu-id="747ee-260">False</span></span>                           |
| <span data-ttu-id="747ee-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="747ee-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="747ee-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="747ee-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="747ee-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="747ee-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="747ee-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="747ee-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="747ee-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-265">Search-Flags</span></span>           | <span data-ttu-id="747ee-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="747ee-266">0x00000000</span></span>                      |
| <span data-ttu-id="747ee-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="747ee-267">System-Flags</span></span>           | <span data-ttu-id="747ee-268">0x00000014</span><span class="sxs-lookup"><span data-stu-id="747ee-268">0x00000014</span></span>                      |
| <span data-ttu-id="747ee-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="747ee-269">Classes used in</span></span>        | [<span data-ttu-id="747ee-270">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="747ee-270">**Top**</span></span>](c-top.md)<br/> |



 

 






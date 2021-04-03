---
title: Atributo Object-Class-Category
description: Este atributo contiene el tipo de clase, como abstract, auxiliar o estructurado.
ms.assetid: 0698392d-991e-4a3c-b734-54d025a38d50
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de clase de objeto y categoría
- objectClassCategory esquema de AD de atributos
topic_type:
- apiref
api_name:
- Object-Class-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397bb50e0af0c9dcddcc535d0bcddb1c8d525cfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997380"
---
# <a name="object-class-category-attribute"></a><span data-ttu-id="cb9ef-105">Atributo Object-Class-Category</span><span class="sxs-lookup"><span data-stu-id="cb9ef-105">Object-Class-Category attribute</span></span>

<span data-ttu-id="cb9ef-106">Este atributo contiene el tipo de clase, como abstract, auxiliar o estructurado.</span><span class="sxs-lookup"><span data-stu-id="cb9ef-106">This attribute contains the class type, such as abstract, auxiliary, or structured.</span></span>



| <span data-ttu-id="cb9ef-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb9ef-107">Entry</span></span> | <span data-ttu-id="cb9ef-108">Value</span><span class="sxs-lookup"><span data-stu-id="cb9ef-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="cb9ef-109">CN</span><span class="sxs-lookup"><span data-stu-id="cb9ef-109">CN</span></span>                | <span data-ttu-id="cb9ef-110">Objeto-clase-categoría</span><span class="sxs-lookup"><span data-stu-id="cb9ef-110">Object-Class-Category</span></span>                                                           |
| <span data-ttu-id="cb9ef-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="cb9ef-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cb9ef-112">objectClassCategory</span><span class="sxs-lookup"><span data-stu-id="cb9ef-112">objectClassCategory</span></span>                                                             |
| <span data-ttu-id="cb9ef-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cb9ef-113">Size</span></span>              | <span data-ttu-id="cb9ef-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="cb9ef-114">4 bytes.</span></span> <span data-ttu-id="cb9ef-115">Estructural 1, abstract 2, auxiliar 3.</span><span class="sxs-lookup"><span data-stu-id="cb9ef-115">Structural 1, abstract 2, auxiliary 3.</span></span> <span data-ttu-id="cb9ef-116">No se debe usar la clase 88, 0.</span><span class="sxs-lookup"><span data-stu-id="cb9ef-116">Class 88, 0 should not be used.</span></span> |
| <span data-ttu-id="cb9ef-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="cb9ef-117">Update Privilege</span></span>  | <span data-ttu-id="cb9ef-118">El diseñador del objeto establecería este valor.</span><span class="sxs-lookup"><span data-stu-id="cb9ef-118">The designer of the object would set this value.</span></span>                                |
| <span data-ttu-id="cb9ef-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="cb9ef-119">Update Frequency</span></span>  | <span data-ttu-id="cb9ef-120">Este valor no debe cambiar nunca.</span><span class="sxs-lookup"><span data-stu-id="cb9ef-120">This value should never change.</span></span>                                                 |
| <span data-ttu-id="cb9ef-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cb9ef-121">Attribute-Id</span></span>      | <span data-ttu-id="cb9ef-122">1.2.840.113556.1.2.370</span><span class="sxs-lookup"><span data-stu-id="cb9ef-122">1.2.840.113556.1.2.370</span></span>                                                          |
| <span data-ttu-id="cb9ef-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cb9ef-123">System-Id-Guid</span></span>    | <span data-ttu-id="cb9ef-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cb9ef-124">bf9679e6-0de6-11d0-a285-00aa003049e2</span></span>                                            |
| <span data-ttu-id="cb9ef-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb9ef-125">Syntax</span></span>            | [<span data-ttu-id="cb9ef-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-126">**Enumeration**</span></span>](s-enumeration.md)                                            |



## <a name="implementations"></a><span data-ttu-id="cb9ef-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="cb9ef-127">Implementations</span></span>

-   [<span data-ttu-id="cb9ef-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cb9ef-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cb9ef-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cb9ef-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cb9ef-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cb9ef-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cb9ef-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cb9ef-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cb9ef-135">Windows 2000 Server</span></span>



| <span data-ttu-id="cb9ef-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb9ef-136">Entry</span></span> | <span data-ttu-id="cb9ef-137">Value</span><span class="sxs-lookup"><span data-stu-id="cb9ef-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb9ef-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb9ef-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb9ef-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb9ef-139">MAPI-Id</span></span>                | <span data-ttu-id="cb9ef-140">0x80F6</span><span class="sxs-lookup"><span data-stu-id="cb9ef-140">0x80F6</span></span>                                           |
| <span data-ttu-id="cb9ef-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb9ef-141">System-Only</span></span>            | <span data-ttu-id="cb9ef-142">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-142">True</span></span>                                             |
| <span data-ttu-id="cb9ef-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb9ef-143">Is-Single-Valued</span></span>       | <span data-ttu-id="cb9ef-144">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-144">True</span></span>                                             |
| <span data-ttu-id="cb9ef-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb9ef-145">Is Indexed</span></span>             | <span data-ttu-id="cb9ef-146">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-146">False</span></span>                                            |
| <span data-ttu-id="cb9ef-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb9ef-147">In Global Catalog</span></span>      | <span data-ttu-id="cb9ef-148">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-148">False</span></span>                                            |
| <span data-ttu-id="cb9ef-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb9ef-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb9ef-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb9ef-150">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb9ef-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb9ef-151">Range-Lower</span></span>            | <span data-ttu-id="cb9ef-152">0</span><span class="sxs-lookup"><span data-stu-id="cb9ef-152">0</span></span>                                                |
| <span data-ttu-id="cb9ef-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb9ef-153">Range-Upper</span></span>            | <span data-ttu-id="cb9ef-154">3</span><span class="sxs-lookup"><span data-stu-id="cb9ef-154">3</span></span>                                                |
| <span data-ttu-id="cb9ef-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-155">Search-Flags</span></span>           | <span data-ttu-id="cb9ef-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb9ef-156">0x00000000</span></span>                                       |
| <span data-ttu-id="cb9ef-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-157">System-Flags</span></span>           | <span data-ttu-id="cb9ef-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb9ef-158">0x00000010</span></span>                                       |
| <span data-ttu-id="cb9ef-159">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb9ef-159">Classes used in</span></span>        | [<span data-ttu-id="cb9ef-160">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-160">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cb9ef-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb9ef-161">Windows Server 2003</span></span>



| <span data-ttu-id="cb9ef-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb9ef-162">Entry</span></span> | <span data-ttu-id="cb9ef-163">Value</span><span class="sxs-lookup"><span data-stu-id="cb9ef-163">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb9ef-164">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb9ef-164">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb9ef-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb9ef-165">MAPI-Id</span></span>                | <span data-ttu-id="cb9ef-166">0x80F6</span><span class="sxs-lookup"><span data-stu-id="cb9ef-166">0x80F6</span></span>                                           |
| <span data-ttu-id="cb9ef-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb9ef-167">System-Only</span></span>            | <span data-ttu-id="cb9ef-168">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-168">True</span></span>                                             |
| <span data-ttu-id="cb9ef-169">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb9ef-169">Is-Single-Valued</span></span>       | <span data-ttu-id="cb9ef-170">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-170">True</span></span>                                             |
| <span data-ttu-id="cb9ef-171">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb9ef-171">Is Indexed</span></span>             | <span data-ttu-id="cb9ef-172">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-172">False</span></span>                                            |
| <span data-ttu-id="cb9ef-173">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb9ef-173">In Global Catalog</span></span>      | <span data-ttu-id="cb9ef-174">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-174">False</span></span>                                            |
| <span data-ttu-id="cb9ef-175">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb9ef-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb9ef-176">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb9ef-176">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb9ef-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb9ef-177">Range-Lower</span></span>            | <span data-ttu-id="cb9ef-178">0</span><span class="sxs-lookup"><span data-stu-id="cb9ef-178">0</span></span>                                                |
| <span data-ttu-id="cb9ef-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb9ef-179">Range-Upper</span></span>            | <span data-ttu-id="cb9ef-180">3</span><span class="sxs-lookup"><span data-stu-id="cb9ef-180">3</span></span>                                                |
| <span data-ttu-id="cb9ef-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-181">Search-Flags</span></span>           | <span data-ttu-id="cb9ef-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb9ef-182">0x00000000</span></span>                                       |
| <span data-ttu-id="cb9ef-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-183">System-Flags</span></span>           | <span data-ttu-id="cb9ef-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb9ef-184">0x00000010</span></span>                                       |
| <span data-ttu-id="cb9ef-185">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb9ef-185">Classes used in</span></span>        | [<span data-ttu-id="cb9ef-186">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-186">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cb9ef-187">ADAM</span><span class="sxs-lookup"><span data-stu-id="cb9ef-187">ADAM</span></span>



| <span data-ttu-id="cb9ef-188">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb9ef-188">Entry</span></span> | <span data-ttu-id="cb9ef-189">Value</span><span class="sxs-lookup"><span data-stu-id="cb9ef-189">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb9ef-190">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb9ef-190">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb9ef-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb9ef-191">MAPI-Id</span></span>                | <span data-ttu-id="cb9ef-192">0x80F6</span><span class="sxs-lookup"><span data-stu-id="cb9ef-192">0x80F6</span></span>                                           |
| <span data-ttu-id="cb9ef-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb9ef-193">System-Only</span></span>            | <span data-ttu-id="cb9ef-194">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-194">True</span></span>                                             |
| <span data-ttu-id="cb9ef-195">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb9ef-195">Is-Single-Valued</span></span>       | <span data-ttu-id="cb9ef-196">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-196">True</span></span>                                             |
| <span data-ttu-id="cb9ef-197">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb9ef-197">Is Indexed</span></span>             | <span data-ttu-id="cb9ef-198">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-198">False</span></span>                                            |
| <span data-ttu-id="cb9ef-199">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb9ef-199">In Global Catalog</span></span>      | <span data-ttu-id="cb9ef-200">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-200">False</span></span>                                            |
| <span data-ttu-id="cb9ef-201">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb9ef-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb9ef-202">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb9ef-202">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb9ef-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb9ef-203">Range-Lower</span></span>            | <span data-ttu-id="cb9ef-204">0</span><span class="sxs-lookup"><span data-stu-id="cb9ef-204">0</span></span>                                                |
| <span data-ttu-id="cb9ef-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb9ef-205">Range-Upper</span></span>            | <span data-ttu-id="cb9ef-206">3</span><span class="sxs-lookup"><span data-stu-id="cb9ef-206">3</span></span>                                                |
| <span data-ttu-id="cb9ef-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-207">Search-Flags</span></span>           | <span data-ttu-id="cb9ef-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb9ef-208">0x00000000</span></span>                                       |
| <span data-ttu-id="cb9ef-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-209">System-Flags</span></span>           | <span data-ttu-id="cb9ef-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb9ef-210">0x00000010</span></span>                                       |
| <span data-ttu-id="cb9ef-211">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb9ef-211">Classes used in</span></span>        | [<span data-ttu-id="cb9ef-212">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-212">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cb9ef-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cb9ef-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cb9ef-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb9ef-214">Entry</span></span> | <span data-ttu-id="cb9ef-215">Value</span><span class="sxs-lookup"><span data-stu-id="cb9ef-215">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb9ef-216">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb9ef-216">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb9ef-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb9ef-217">MAPI-Id</span></span>                | <span data-ttu-id="cb9ef-218">0x80F6</span><span class="sxs-lookup"><span data-stu-id="cb9ef-218">0x80F6</span></span>                                           |
| <span data-ttu-id="cb9ef-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb9ef-219">System-Only</span></span>            | <span data-ttu-id="cb9ef-220">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-220">True</span></span>                                             |
| <span data-ttu-id="cb9ef-221">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb9ef-221">Is-Single-Valued</span></span>       | <span data-ttu-id="cb9ef-222">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-222">True</span></span>                                             |
| <span data-ttu-id="cb9ef-223">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb9ef-223">Is Indexed</span></span>             | <span data-ttu-id="cb9ef-224">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-224">False</span></span>                                            |
| <span data-ttu-id="cb9ef-225">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb9ef-225">In Global Catalog</span></span>      | <span data-ttu-id="cb9ef-226">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-226">False</span></span>                                            |
| <span data-ttu-id="cb9ef-227">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb9ef-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb9ef-228">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb9ef-228">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb9ef-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb9ef-229">Range-Lower</span></span>            | <span data-ttu-id="cb9ef-230">0</span><span class="sxs-lookup"><span data-stu-id="cb9ef-230">0</span></span>                                                |
| <span data-ttu-id="cb9ef-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb9ef-231">Range-Upper</span></span>            | <span data-ttu-id="cb9ef-232">3</span><span class="sxs-lookup"><span data-stu-id="cb9ef-232">3</span></span>                                                |
| <span data-ttu-id="cb9ef-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-233">Search-Flags</span></span>           | <span data-ttu-id="cb9ef-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb9ef-234">0x00000000</span></span>                                       |
| <span data-ttu-id="cb9ef-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-235">System-Flags</span></span>           | <span data-ttu-id="cb9ef-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb9ef-236">0x00000010</span></span>                                       |
| <span data-ttu-id="cb9ef-237">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb9ef-237">Classes used in</span></span>        | [<span data-ttu-id="cb9ef-238">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-238">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cb9ef-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb9ef-239">Windows Server 2008</span></span>



| <span data-ttu-id="cb9ef-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb9ef-240">Entry</span></span> | <span data-ttu-id="cb9ef-241">Value</span><span class="sxs-lookup"><span data-stu-id="cb9ef-241">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb9ef-242">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb9ef-242">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb9ef-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb9ef-243">MAPI-Id</span></span>                | <span data-ttu-id="cb9ef-244">0x80F6</span><span class="sxs-lookup"><span data-stu-id="cb9ef-244">0x80F6</span></span>                                           |
| <span data-ttu-id="cb9ef-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb9ef-245">System-Only</span></span>            | <span data-ttu-id="cb9ef-246">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-246">True</span></span>                                             |
| <span data-ttu-id="cb9ef-247">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb9ef-247">Is-Single-Valued</span></span>       | <span data-ttu-id="cb9ef-248">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-248">True</span></span>                                             |
| <span data-ttu-id="cb9ef-249">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb9ef-249">Is Indexed</span></span>             | <span data-ttu-id="cb9ef-250">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-250">False</span></span>                                            |
| <span data-ttu-id="cb9ef-251">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb9ef-251">In Global Catalog</span></span>      | <span data-ttu-id="cb9ef-252">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-252">False</span></span>                                            |
| <span data-ttu-id="cb9ef-253">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb9ef-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb9ef-254">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb9ef-254">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb9ef-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb9ef-255">Range-Lower</span></span>            | <span data-ttu-id="cb9ef-256">0</span><span class="sxs-lookup"><span data-stu-id="cb9ef-256">0</span></span>                                                |
| <span data-ttu-id="cb9ef-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb9ef-257">Range-Upper</span></span>            | <span data-ttu-id="cb9ef-258">3</span><span class="sxs-lookup"><span data-stu-id="cb9ef-258">3</span></span>                                                |
| <span data-ttu-id="cb9ef-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-259">Search-Flags</span></span>           | <span data-ttu-id="cb9ef-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb9ef-260">0x00000000</span></span>                                       |
| <span data-ttu-id="cb9ef-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-261">System-Flags</span></span>           | <span data-ttu-id="cb9ef-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb9ef-262">0x00000010</span></span>                                       |
| <span data-ttu-id="cb9ef-263">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb9ef-263">Classes used in</span></span>        | [<span data-ttu-id="cb9ef-264">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-264">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cb9ef-265">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cb9ef-265">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cb9ef-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb9ef-266">Entry</span></span> | <span data-ttu-id="cb9ef-267">Value</span><span class="sxs-lookup"><span data-stu-id="cb9ef-267">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb9ef-268">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb9ef-268">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb9ef-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb9ef-269">MAPI-Id</span></span>                | <span data-ttu-id="cb9ef-270">0x80F6</span><span class="sxs-lookup"><span data-stu-id="cb9ef-270">0x80F6</span></span>                                           |
| <span data-ttu-id="cb9ef-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb9ef-271">System-Only</span></span>            | <span data-ttu-id="cb9ef-272">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-272">True</span></span>                                             |
| <span data-ttu-id="cb9ef-273">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb9ef-273">Is-Single-Valued</span></span>       | <span data-ttu-id="cb9ef-274">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-274">True</span></span>                                             |
| <span data-ttu-id="cb9ef-275">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb9ef-275">Is Indexed</span></span>             | <span data-ttu-id="cb9ef-276">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-276">False</span></span>                                            |
| <span data-ttu-id="cb9ef-277">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb9ef-277">In Global Catalog</span></span>      | <span data-ttu-id="cb9ef-278">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-278">False</span></span>                                            |
| <span data-ttu-id="cb9ef-279">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb9ef-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb9ef-280">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb9ef-280">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb9ef-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb9ef-281">Range-Lower</span></span>            | <span data-ttu-id="cb9ef-282">0</span><span class="sxs-lookup"><span data-stu-id="cb9ef-282">0</span></span>                                                |
| <span data-ttu-id="cb9ef-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb9ef-283">Range-Upper</span></span>            | <span data-ttu-id="cb9ef-284">3</span><span class="sxs-lookup"><span data-stu-id="cb9ef-284">3</span></span>                                                |
| <span data-ttu-id="cb9ef-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-285">Search-Flags</span></span>           | <span data-ttu-id="cb9ef-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb9ef-286">0x00000000</span></span>                                       |
| <span data-ttu-id="cb9ef-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-287">System-Flags</span></span>           | <span data-ttu-id="cb9ef-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb9ef-288">0x00000010</span></span>                                       |
| <span data-ttu-id="cb9ef-289">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb9ef-289">Classes used in</span></span>        | [<span data-ttu-id="cb9ef-290">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-290">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cb9ef-291">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb9ef-291">Windows Server 2012</span></span>



| <span data-ttu-id="cb9ef-292">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb9ef-292">Entry</span></span> | <span data-ttu-id="cb9ef-293">Value</span><span class="sxs-lookup"><span data-stu-id="cb9ef-293">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="cb9ef-294">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="cb9ef-294">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="cb9ef-295">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb9ef-295">MAPI-Id</span></span>                | <span data-ttu-id="cb9ef-296">0x80F6</span><span class="sxs-lookup"><span data-stu-id="cb9ef-296">0x80F6</span></span>                                           |
| <span data-ttu-id="cb9ef-297">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb9ef-297">System-Only</span></span>            | <span data-ttu-id="cb9ef-298">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-298">True</span></span>                                             |
| <span data-ttu-id="cb9ef-299">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="cb9ef-299">Is-Single-Valued</span></span>       | <span data-ttu-id="cb9ef-300">True</span><span class="sxs-lookup"><span data-stu-id="cb9ef-300">True</span></span>                                             |
| <span data-ttu-id="cb9ef-301">Está indexado</span><span class="sxs-lookup"><span data-stu-id="cb9ef-301">Is Indexed</span></span>             | <span data-ttu-id="cb9ef-302">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-302">False</span></span>                                            |
| <span data-ttu-id="cb9ef-303">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb9ef-303">In Global Catalog</span></span>      | <span data-ttu-id="cb9ef-304">False</span><span class="sxs-lookup"><span data-stu-id="cb9ef-304">False</span></span>                                            |
| <span data-ttu-id="cb9ef-305">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="cb9ef-305">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb9ef-306">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cb9ef-306">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="cb9ef-307">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb9ef-307">Range-Lower</span></span>            | <span data-ttu-id="cb9ef-308">0</span><span class="sxs-lookup"><span data-stu-id="cb9ef-308">0</span></span>                                                |
| <span data-ttu-id="cb9ef-309">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb9ef-309">Range-Upper</span></span>            | <span data-ttu-id="cb9ef-310">3</span><span class="sxs-lookup"><span data-stu-id="cb9ef-310">3</span></span>                                                |
| <span data-ttu-id="cb9ef-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-311">Search-Flags</span></span>           | <span data-ttu-id="cb9ef-312">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb9ef-312">0x00000000</span></span>                                       |
| <span data-ttu-id="cb9ef-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb9ef-313">System-Flags</span></span>           | <span data-ttu-id="cb9ef-314">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb9ef-314">0x00000010</span></span>                                       |
| <span data-ttu-id="cb9ef-315">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="cb9ef-315">Classes used in</span></span>        | [<span data-ttu-id="cb9ef-316">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="cb9ef-316">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






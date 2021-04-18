---
title: Atributo extendido-Class-info
description: Una propiedad con varios valores que contiene cadenas que representan información adicional para cada clase. Cada valor contiene los governsID, lDAPDisplayName y schemaIDGUID de la clase.
ms.assetid: f0f07950-28f8-4fe7-b030-1ab7632569e1
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Extended-Class-info
- extendedClassInfo esquema de AD de atributos
topic_type:
- apiref
api_name:
- Extended-Class-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1b3320f547a3dbb41a151a33765cf9729e82c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422659"
---
# <a name="extended-class-info-attribute"></a><span data-ttu-id="fdd0e-106">Atributo extendido-Class-info</span><span class="sxs-lookup"><span data-stu-id="fdd0e-106">Extended-Class-Info attribute</span></span>

<span data-ttu-id="fdd0e-107">Una propiedad con varios valores que contiene cadenas que representan información adicional para cada clase.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-107">A multi-valued property that contains strings that represent additional information for each class.</span></span> <span data-ttu-id="fdd0e-108">Cada valor contiene los governsID, lDAPDisplayName y schemaIDGUID de la clase.</span><span class="sxs-lookup"><span data-stu-id="fdd0e-108">Each value contains the governsID, lDAPDisplayName, and schemaIDGUID of the class.</span></span>



| <span data-ttu-id="fdd0e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdd0e-109">Entry</span></span> | <span data-ttu-id="fdd0e-110">Value</span><span class="sxs-lookup"><span data-stu-id="fdd0e-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="fdd0e-111">CN</span><span class="sxs-lookup"><span data-stu-id="fdd0e-111">CN</span></span>                | <span data-ttu-id="fdd0e-112">Extended-Class-info</span><span class="sxs-lookup"><span data-stu-id="fdd0e-112">Extended-Class-Info</span></span>                         |
| <span data-ttu-id="fdd0e-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="fdd0e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fdd0e-114">extendedClassInfo</span><span class="sxs-lookup"><span data-stu-id="fdd0e-114">extendedClassInfo</span></span>                           |
| <span data-ttu-id="fdd0e-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="fdd0e-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="fdd0e-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="fdd0e-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="fdd0e-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="fdd0e-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="fdd0e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fdd0e-118">Attribute-Id</span></span>      | <span data-ttu-id="fdd0e-119">1.2.840.113556.1.4.908</span><span class="sxs-lookup"><span data-stu-id="fdd0e-119">1.2.840.113556.1.4.908</span></span>                      |
| <span data-ttu-id="fdd0e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fdd0e-120">System-Id-Guid</span></span>    | <span data-ttu-id="fdd0e-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="fdd0e-121">9a7ad948-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="fdd0e-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdd0e-122">Syntax</span></span>            | [<span data-ttu-id="fdd0e-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="fdd0e-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="fdd0e-124">Implementations</span></span>

-   [<span data-ttu-id="fdd0e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fdd0e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fdd0e-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="fdd0e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fdd0e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fdd0e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fdd0e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fdd0e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fdd0e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="fdd0e-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdd0e-133">Entry</span></span> | <span data-ttu-id="fdd0e-134">Value</span><span class="sxs-lookup"><span data-stu-id="fdd0e-134">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="fdd0e-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fdd0e-135">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd0e-136">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd0e-137">System-Only</span></span>            | <span data-ttu-id="fdd0e-138">True</span><span class="sxs-lookup"><span data-stu-id="fdd0e-138">True</span></span>                                        |
| <span data-ttu-id="fdd0e-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fdd0e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd0e-140">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-140">False</span></span>                                       |
| <span data-ttu-id="fdd0e-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fdd0e-141">Is Indexed</span></span>             | <span data-ttu-id="fdd0e-142">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-142">False</span></span>                                       |
| <span data-ttu-id="fdd0e-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fdd0e-143">In Global Catalog</span></span>      | <span data-ttu-id="fdd0e-144">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-144">False</span></span>                                       |
| <span data-ttu-id="fdd0e-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fdd0e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd0e-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd0e-146">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="fdd0e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd0e-147">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd0e-148">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-149">Search-Flags</span></span>           | <span data-ttu-id="fdd0e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd0e-150">0x00000000</span></span>                                  |
| <span data-ttu-id="fdd0e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-151">System-Flags</span></span>           | <span data-ttu-id="fdd0e-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdd0e-152">0x08000014</span></span>                                  |
| <span data-ttu-id="fdd0e-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fdd0e-153">Classes used in</span></span>        | [<span data-ttu-id="fdd0e-154">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-154">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fdd0e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fdd0e-155">Windows Server 2003</span></span>



| <span data-ttu-id="fdd0e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdd0e-156">Entry</span></span> | <span data-ttu-id="fdd0e-157">Value</span><span class="sxs-lookup"><span data-stu-id="fdd0e-157">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="fdd0e-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fdd0e-158">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd0e-159">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd0e-160">System-Only</span></span>            | <span data-ttu-id="fdd0e-161">True</span><span class="sxs-lookup"><span data-stu-id="fdd0e-161">True</span></span>                                        |
| <span data-ttu-id="fdd0e-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fdd0e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd0e-163">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-163">False</span></span>                                       |
| <span data-ttu-id="fdd0e-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fdd0e-164">Is Indexed</span></span>             | <span data-ttu-id="fdd0e-165">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-165">False</span></span>                                       |
| <span data-ttu-id="fdd0e-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fdd0e-166">In Global Catalog</span></span>      | <span data-ttu-id="fdd0e-167">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-167">False</span></span>                                       |
| <span data-ttu-id="fdd0e-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fdd0e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd0e-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd0e-169">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="fdd0e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd0e-170">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd0e-171">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-172">Search-Flags</span></span>           | <span data-ttu-id="fdd0e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd0e-173">0x00000000</span></span>                                  |
| <span data-ttu-id="fdd0e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-174">System-Flags</span></span>           | <span data-ttu-id="fdd0e-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdd0e-175">0x08000014</span></span>                                  |
| <span data-ttu-id="fdd0e-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fdd0e-176">Classes used in</span></span>        | [<span data-ttu-id="fdd0e-177">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-177">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="fdd0e-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="fdd0e-178">ADAM</span></span>



| <span data-ttu-id="fdd0e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdd0e-179">Entry</span></span> | <span data-ttu-id="fdd0e-180">Value</span><span class="sxs-lookup"><span data-stu-id="fdd0e-180">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="fdd0e-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fdd0e-181">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd0e-182">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd0e-183">System-Only</span></span>            | <span data-ttu-id="fdd0e-184">True</span><span class="sxs-lookup"><span data-stu-id="fdd0e-184">True</span></span>                                        |
| <span data-ttu-id="fdd0e-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fdd0e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd0e-186">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-186">False</span></span>                                       |
| <span data-ttu-id="fdd0e-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fdd0e-187">Is Indexed</span></span>             | <span data-ttu-id="fdd0e-188">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-188">False</span></span>                                       |
| <span data-ttu-id="fdd0e-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fdd0e-189">In Global Catalog</span></span>      | <span data-ttu-id="fdd0e-190">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-190">False</span></span>                                       |
| <span data-ttu-id="fdd0e-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fdd0e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd0e-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd0e-192">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="fdd0e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd0e-193">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd0e-194">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-195">Search-Flags</span></span>           | <span data-ttu-id="fdd0e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd0e-196">0x00000000</span></span>                                  |
| <span data-ttu-id="fdd0e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-197">System-Flags</span></span>           | <span data-ttu-id="fdd0e-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdd0e-198">0x08000014</span></span>                                  |
| <span data-ttu-id="fdd0e-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fdd0e-199">Classes used in</span></span>        | [<span data-ttu-id="fdd0e-200">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-200">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fdd0e-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fdd0e-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fdd0e-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdd0e-202">Entry</span></span> | <span data-ttu-id="fdd0e-203">Value</span><span class="sxs-lookup"><span data-stu-id="fdd0e-203">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="fdd0e-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fdd0e-204">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd0e-205">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd0e-206">System-Only</span></span>            | <span data-ttu-id="fdd0e-207">True</span><span class="sxs-lookup"><span data-stu-id="fdd0e-207">True</span></span>                                        |
| <span data-ttu-id="fdd0e-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fdd0e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd0e-209">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-209">False</span></span>                                       |
| <span data-ttu-id="fdd0e-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fdd0e-210">Is Indexed</span></span>             | <span data-ttu-id="fdd0e-211">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-211">False</span></span>                                       |
| <span data-ttu-id="fdd0e-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fdd0e-212">In Global Catalog</span></span>      | <span data-ttu-id="fdd0e-213">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-213">False</span></span>                                       |
| <span data-ttu-id="fdd0e-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fdd0e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd0e-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd0e-215">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="fdd0e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd0e-216">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd0e-217">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-218">Search-Flags</span></span>           | <span data-ttu-id="fdd0e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd0e-219">0x00000000</span></span>                                  |
| <span data-ttu-id="fdd0e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-220">System-Flags</span></span>           | <span data-ttu-id="fdd0e-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdd0e-221">0x08000014</span></span>                                  |
| <span data-ttu-id="fdd0e-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fdd0e-222">Classes used in</span></span>        | [<span data-ttu-id="fdd0e-223">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-223">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fdd0e-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdd0e-224">Windows Server 2008</span></span>



| <span data-ttu-id="fdd0e-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdd0e-225">Entry</span></span> | <span data-ttu-id="fdd0e-226">Value</span><span class="sxs-lookup"><span data-stu-id="fdd0e-226">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="fdd0e-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fdd0e-227">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd0e-228">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd0e-229">System-Only</span></span>            | <span data-ttu-id="fdd0e-230">True</span><span class="sxs-lookup"><span data-stu-id="fdd0e-230">True</span></span>                                        |
| <span data-ttu-id="fdd0e-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fdd0e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd0e-232">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-232">False</span></span>                                       |
| <span data-ttu-id="fdd0e-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fdd0e-233">Is Indexed</span></span>             | <span data-ttu-id="fdd0e-234">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-234">False</span></span>                                       |
| <span data-ttu-id="fdd0e-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fdd0e-235">In Global Catalog</span></span>      | <span data-ttu-id="fdd0e-236">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-236">False</span></span>                                       |
| <span data-ttu-id="fdd0e-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fdd0e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd0e-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd0e-238">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="fdd0e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd0e-239">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd0e-240">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-241">Search-Flags</span></span>           | <span data-ttu-id="fdd0e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd0e-242">0x00000000</span></span>                                  |
| <span data-ttu-id="fdd0e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-243">System-Flags</span></span>           | <span data-ttu-id="fdd0e-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdd0e-244">0x08000014</span></span>                                  |
| <span data-ttu-id="fdd0e-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fdd0e-245">Classes used in</span></span>        | [<span data-ttu-id="fdd0e-246">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-246">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fdd0e-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fdd0e-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fdd0e-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdd0e-248">Entry</span></span> | <span data-ttu-id="fdd0e-249">Value</span><span class="sxs-lookup"><span data-stu-id="fdd0e-249">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="fdd0e-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fdd0e-250">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd0e-251">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd0e-252">System-Only</span></span>            | <span data-ttu-id="fdd0e-253">True</span><span class="sxs-lookup"><span data-stu-id="fdd0e-253">True</span></span>                                        |
| <span data-ttu-id="fdd0e-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fdd0e-254">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd0e-255">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-255">False</span></span>                                       |
| <span data-ttu-id="fdd0e-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fdd0e-256">Is Indexed</span></span>             | <span data-ttu-id="fdd0e-257">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-257">False</span></span>                                       |
| <span data-ttu-id="fdd0e-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fdd0e-258">In Global Catalog</span></span>      | <span data-ttu-id="fdd0e-259">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-259">False</span></span>                                       |
| <span data-ttu-id="fdd0e-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fdd0e-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd0e-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd0e-261">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="fdd0e-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd0e-262">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd0e-263">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-264">Search-Flags</span></span>           | <span data-ttu-id="fdd0e-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd0e-265">0x00000000</span></span>                                  |
| <span data-ttu-id="fdd0e-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-266">System-Flags</span></span>           | <span data-ttu-id="fdd0e-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdd0e-267">0x08000014</span></span>                                  |
| <span data-ttu-id="fdd0e-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fdd0e-268">Classes used in</span></span>        | [<span data-ttu-id="fdd0e-269">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-269">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fdd0e-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fdd0e-270">Windows Server 2012</span></span>



| <span data-ttu-id="fdd0e-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="fdd0e-271">Entry</span></span> | <span data-ttu-id="fdd0e-272">Value</span><span class="sxs-lookup"><span data-stu-id="fdd0e-272">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="fdd0e-273">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fdd0e-273">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd0e-274">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="fdd0e-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd0e-275">System-Only</span></span>            | <span data-ttu-id="fdd0e-276">True</span><span class="sxs-lookup"><span data-stu-id="fdd0e-276">True</span></span>                                        |
| <span data-ttu-id="fdd0e-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fdd0e-277">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd0e-278">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-278">False</span></span>                                       |
| <span data-ttu-id="fdd0e-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fdd0e-279">Is Indexed</span></span>             | <span data-ttu-id="fdd0e-280">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-280">False</span></span>                                       |
| <span data-ttu-id="fdd0e-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fdd0e-281">In Global Catalog</span></span>      | <span data-ttu-id="fdd0e-282">False</span><span class="sxs-lookup"><span data-stu-id="fdd0e-282">False</span></span>                                       |
| <span data-ttu-id="fdd0e-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fdd0e-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd0e-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd0e-284">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="fdd0e-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd0e-285">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd0e-286">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="fdd0e-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-287">Search-Flags</span></span>           | <span data-ttu-id="fdd0e-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd0e-288">0x00000000</span></span>                                  |
| <span data-ttu-id="fdd0e-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd0e-289">System-Flags</span></span>           | <span data-ttu-id="fdd0e-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="fdd0e-290">0x08000014</span></span>                                  |
| <span data-ttu-id="fdd0e-291">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fdd0e-291">Classes used in</span></span>        | [<span data-ttu-id="fdd0e-292">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="fdd0e-292">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 






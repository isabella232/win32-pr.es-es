---
title: Atributo SubSchemaSubEntry
description: Nombre distintivo de la ubicación del objeto de subesquema donde se define una clase o un atributo.
ms.assetid: 16beeb31-436c-4ae1-b1f7-fa00abb3bcbb
ms.tgt_platform: multiple
keywords:
- SubSchemaSubEntry esquema de AD de atributos
- subSchemaSubEntry esquema de AD de atributos
topic_type:
- apiref
api_name:
- SubSchemaSubEntry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0278d63d3a6ed9d0f84ad67df87e248af31f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535884"
---
# <a name="subschemasubentry-attribute"></a><span data-ttu-id="909f4-105">Atributo SubSchemaSubEntry</span><span class="sxs-lookup"><span data-stu-id="909f4-105">SubSchemaSubEntry attribute</span></span>

<span data-ttu-id="909f4-106">Nombre distintivo de la ubicación del objeto de subesquema donde se define una clase o un atributo.</span><span class="sxs-lookup"><span data-stu-id="909f4-106">The distinguished name for the location of the subschema object where a class or attribute is defined.</span></span>



| <span data-ttu-id="909f4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="909f4-107">Entry</span></span> | <span data-ttu-id="909f4-108">Value</span><span class="sxs-lookup"><span data-stu-id="909f4-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="909f4-109">CN</span><span class="sxs-lookup"><span data-stu-id="909f4-109">CN</span></span>                | <span data-ttu-id="909f4-110">SubSchemaSubEntry</span><span class="sxs-lookup"><span data-stu-id="909f4-110">SubSchemaSubEntry</span></span>                                                                |
| <span data-ttu-id="909f4-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="909f4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="909f4-112">subSchemaSubEntry</span><span class="sxs-lookup"><span data-stu-id="909f4-112">subSchemaSubEntry</span></span>                                                                |
| <span data-ttu-id="909f4-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="909f4-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="909f4-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="909f4-114">Update Privilege</span></span>  | <span data-ttu-id="909f4-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="909f4-115">Schema administrator</span></span>                                                             |
| <span data-ttu-id="909f4-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="909f4-116">Update Frequency</span></span>  | <span data-ttu-id="909f4-117">Cuando se carga el Active Directory o cuando se define una nueva clase o atributo.</span><span class="sxs-lookup"><span data-stu-id="909f4-117">When the Active Directory is loaded or when a new class or attribute is defined.</span></span> |
| <span data-ttu-id="909f4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-118">Attribute-Id</span></span>      | <span data-ttu-id="909f4-119">2.5.18.10</span><span class="sxs-lookup"><span data-stu-id="909f4-119">2.5.18.10</span></span>                                                                        |
| <span data-ttu-id="909f4-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="909f4-120">System-Id-Guid</span></span>    | <span data-ttu-id="909f4-121">9a7ad94d-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="909f4-121">9a7ad94d-ca53-11d1-bbd0-0080c76670c0</span></span>                                             |
| <span data-ttu-id="909f4-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="909f4-122">Syntax</span></span>            | [<span data-ttu-id="909f4-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="909f4-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                          |



## <a name="implementations"></a><span data-ttu-id="909f4-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="909f4-124">Implementations</span></span>

-   [<span data-ttu-id="909f4-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="909f4-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="909f4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="909f4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="909f4-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="909f4-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="909f4-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="909f4-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="909f4-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="909f4-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="909f4-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="909f4-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="909f4-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="909f4-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="909f4-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="909f4-132">Windows 2000 Server</span></span>



| <span data-ttu-id="909f4-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="909f4-133">Entry</span></span> | <span data-ttu-id="909f4-134">Value</span><span class="sxs-lookup"><span data-stu-id="909f4-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="909f4-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="909f4-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-137">System-Only</span></span>            | <span data-ttu-id="909f4-138">True</span><span class="sxs-lookup"><span data-stu-id="909f4-138">True</span></span>                            |
| <span data-ttu-id="909f4-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="909f4-139">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-140">False</span><span class="sxs-lookup"><span data-stu-id="909f4-140">False</span></span>                           |
| <span data-ttu-id="909f4-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="909f4-141">Is Indexed</span></span>             | <span data-ttu-id="909f4-142">False</span><span class="sxs-lookup"><span data-stu-id="909f4-142">False</span></span>                           |
| <span data-ttu-id="909f4-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="909f4-143">In Global Catalog</span></span>      | <span data-ttu-id="909f4-144">False</span><span class="sxs-lookup"><span data-stu-id="909f4-144">False</span></span>                           |
| <span data-ttu-id="909f4-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="909f4-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="909f4-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="909f4-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="909f4-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="909f4-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-149">Search-Flags</span></span>           | <span data-ttu-id="909f4-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="909f4-150">0x00000000</span></span>                      |
| <span data-ttu-id="909f4-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-151">System-Flags</span></span>           | <span data-ttu-id="909f4-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="909f4-152">0x08000014</span></span>                      |
| <span data-ttu-id="909f4-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="909f4-153">Classes used in</span></span>        | [<span data-ttu-id="909f4-154">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="909f4-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="909f4-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="909f4-155">Windows Server 2003</span></span>



| <span data-ttu-id="909f4-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="909f4-156">Entry</span></span> | <span data-ttu-id="909f4-157">Value</span><span class="sxs-lookup"><span data-stu-id="909f4-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="909f4-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="909f4-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-160">System-Only</span></span>            | <span data-ttu-id="909f4-161">True</span><span class="sxs-lookup"><span data-stu-id="909f4-161">True</span></span>                            |
| <span data-ttu-id="909f4-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="909f4-162">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-163">False</span><span class="sxs-lookup"><span data-stu-id="909f4-163">False</span></span>                           |
| <span data-ttu-id="909f4-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="909f4-164">Is Indexed</span></span>             | <span data-ttu-id="909f4-165">False</span><span class="sxs-lookup"><span data-stu-id="909f4-165">False</span></span>                           |
| <span data-ttu-id="909f4-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="909f4-166">In Global Catalog</span></span>      | <span data-ttu-id="909f4-167">False</span><span class="sxs-lookup"><span data-stu-id="909f4-167">False</span></span>                           |
| <span data-ttu-id="909f4-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="909f4-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="909f4-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="909f4-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="909f4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="909f4-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-172">Search-Flags</span></span>           | <span data-ttu-id="909f4-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="909f4-173">0x00000000</span></span>                      |
| <span data-ttu-id="909f4-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-174">System-Flags</span></span>           | <span data-ttu-id="909f4-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="909f4-175">0x08000014</span></span>                      |
| <span data-ttu-id="909f4-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="909f4-176">Classes used in</span></span>        | [<span data-ttu-id="909f4-177">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="909f4-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="909f4-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="909f4-178">ADAM</span></span>



| <span data-ttu-id="909f4-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="909f4-179">Entry</span></span> | <span data-ttu-id="909f4-180">Value</span><span class="sxs-lookup"><span data-stu-id="909f4-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="909f4-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="909f4-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-183">System-Only</span></span>            | <span data-ttu-id="909f4-184">True</span><span class="sxs-lookup"><span data-stu-id="909f4-184">True</span></span>                            |
| <span data-ttu-id="909f4-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="909f4-185">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-186">False</span><span class="sxs-lookup"><span data-stu-id="909f4-186">False</span></span>                           |
| <span data-ttu-id="909f4-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="909f4-187">Is Indexed</span></span>             | <span data-ttu-id="909f4-188">False</span><span class="sxs-lookup"><span data-stu-id="909f4-188">False</span></span>                           |
| <span data-ttu-id="909f4-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="909f4-189">In Global Catalog</span></span>      | <span data-ttu-id="909f4-190">False</span><span class="sxs-lookup"><span data-stu-id="909f4-190">False</span></span>                           |
| <span data-ttu-id="909f4-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="909f4-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="909f4-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="909f4-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="909f4-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="909f4-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-195">Search-Flags</span></span>           | <span data-ttu-id="909f4-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="909f4-196">0x00000000</span></span>                      |
| <span data-ttu-id="909f4-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-197">System-Flags</span></span>           | <span data-ttu-id="909f4-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="909f4-198">0x08000014</span></span>                      |
| <span data-ttu-id="909f4-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="909f4-199">Classes used in</span></span>        | [<span data-ttu-id="909f4-200">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="909f4-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="909f4-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="909f4-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="909f4-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="909f4-202">Entry</span></span> | <span data-ttu-id="909f4-203">Value</span><span class="sxs-lookup"><span data-stu-id="909f4-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="909f4-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="909f4-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-206">System-Only</span></span>            | <span data-ttu-id="909f4-207">True</span><span class="sxs-lookup"><span data-stu-id="909f4-207">True</span></span>                            |
| <span data-ttu-id="909f4-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="909f4-208">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-209">False</span><span class="sxs-lookup"><span data-stu-id="909f4-209">False</span></span>                           |
| <span data-ttu-id="909f4-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="909f4-210">Is Indexed</span></span>             | <span data-ttu-id="909f4-211">False</span><span class="sxs-lookup"><span data-stu-id="909f4-211">False</span></span>                           |
| <span data-ttu-id="909f4-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="909f4-212">In Global Catalog</span></span>      | <span data-ttu-id="909f4-213">False</span><span class="sxs-lookup"><span data-stu-id="909f4-213">False</span></span>                           |
| <span data-ttu-id="909f4-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="909f4-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="909f4-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="909f4-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="909f4-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="909f4-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-218">Search-Flags</span></span>           | <span data-ttu-id="909f4-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="909f4-219">0x00000000</span></span>                      |
| <span data-ttu-id="909f4-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-220">System-Flags</span></span>           | <span data-ttu-id="909f4-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="909f4-221">0x08000014</span></span>                      |
| <span data-ttu-id="909f4-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="909f4-222">Classes used in</span></span>        | [<span data-ttu-id="909f4-223">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="909f4-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="909f4-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="909f4-224">Windows Server 2008</span></span>



| <span data-ttu-id="909f4-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="909f4-225">Entry</span></span> | <span data-ttu-id="909f4-226">Value</span><span class="sxs-lookup"><span data-stu-id="909f4-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="909f4-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="909f4-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-229">System-Only</span></span>            | <span data-ttu-id="909f4-230">True</span><span class="sxs-lookup"><span data-stu-id="909f4-230">True</span></span>                            |
| <span data-ttu-id="909f4-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="909f4-231">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-232">False</span><span class="sxs-lookup"><span data-stu-id="909f4-232">False</span></span>                           |
| <span data-ttu-id="909f4-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="909f4-233">Is Indexed</span></span>             | <span data-ttu-id="909f4-234">False</span><span class="sxs-lookup"><span data-stu-id="909f4-234">False</span></span>                           |
| <span data-ttu-id="909f4-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="909f4-235">In Global Catalog</span></span>      | <span data-ttu-id="909f4-236">False</span><span class="sxs-lookup"><span data-stu-id="909f4-236">False</span></span>                           |
| <span data-ttu-id="909f4-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="909f4-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="909f4-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="909f4-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="909f4-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="909f4-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-241">Search-Flags</span></span>           | <span data-ttu-id="909f4-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="909f4-242">0x00000000</span></span>                      |
| <span data-ttu-id="909f4-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-243">System-Flags</span></span>           | <span data-ttu-id="909f4-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="909f4-244">0x08000014</span></span>                      |
| <span data-ttu-id="909f4-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="909f4-245">Classes used in</span></span>        | [<span data-ttu-id="909f4-246">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="909f4-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="909f4-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="909f4-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="909f4-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="909f4-248">Entry</span></span> | <span data-ttu-id="909f4-249">Value</span><span class="sxs-lookup"><span data-stu-id="909f4-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="909f4-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="909f4-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-252">System-Only</span></span>            | <span data-ttu-id="909f4-253">True</span><span class="sxs-lookup"><span data-stu-id="909f4-253">True</span></span>                            |
| <span data-ttu-id="909f4-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="909f4-254">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-255">False</span><span class="sxs-lookup"><span data-stu-id="909f4-255">False</span></span>                           |
| <span data-ttu-id="909f4-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="909f4-256">Is Indexed</span></span>             | <span data-ttu-id="909f4-257">False</span><span class="sxs-lookup"><span data-stu-id="909f4-257">False</span></span>                           |
| <span data-ttu-id="909f4-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="909f4-258">In Global Catalog</span></span>      | <span data-ttu-id="909f4-259">False</span><span class="sxs-lookup"><span data-stu-id="909f4-259">False</span></span>                           |
| <span data-ttu-id="909f4-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="909f4-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="909f4-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="909f4-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="909f4-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="909f4-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-264">Search-Flags</span></span>           | <span data-ttu-id="909f4-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="909f4-265">0x00000000</span></span>                      |
| <span data-ttu-id="909f4-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-266">System-Flags</span></span>           | <span data-ttu-id="909f4-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="909f4-267">0x08000014</span></span>                      |
| <span data-ttu-id="909f4-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="909f4-268">Classes used in</span></span>        | [<span data-ttu-id="909f4-269">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="909f4-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="909f4-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="909f4-270">Windows Server 2012</span></span>



| <span data-ttu-id="909f4-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="909f4-271">Entry</span></span> | <span data-ttu-id="909f4-272">Value</span><span class="sxs-lookup"><span data-stu-id="909f4-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="909f4-273">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="909f4-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="909f4-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="909f4-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="909f4-275">System-Only</span></span>            | <span data-ttu-id="909f4-276">True</span><span class="sxs-lookup"><span data-stu-id="909f4-276">True</span></span>                            |
| <span data-ttu-id="909f4-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="909f4-277">Is-Single-Valued</span></span>       | <span data-ttu-id="909f4-278">False</span><span class="sxs-lookup"><span data-stu-id="909f4-278">False</span></span>                           |
| <span data-ttu-id="909f4-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="909f4-279">Is Indexed</span></span>             | <span data-ttu-id="909f4-280">False</span><span class="sxs-lookup"><span data-stu-id="909f4-280">False</span></span>                           |
| <span data-ttu-id="909f4-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="909f4-281">In Global Catalog</span></span>      | <span data-ttu-id="909f4-282">False</span><span class="sxs-lookup"><span data-stu-id="909f4-282">False</span></span>                           |
| <span data-ttu-id="909f4-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="909f4-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="909f4-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="909f4-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="909f4-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="909f4-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="909f4-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="909f4-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="909f4-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-287">Search-Flags</span></span>           | <span data-ttu-id="909f4-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="909f4-288">0x00000000</span></span>                      |
| <span data-ttu-id="909f4-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="909f4-289">System-Flags</span></span>           | <span data-ttu-id="909f4-290">0x08000014</span><span class="sxs-lookup"><span data-stu-id="909f4-290">0x08000014</span></span>                      |
| <span data-ttu-id="909f4-291">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="909f4-291">Classes used in</span></span>        | [<span data-ttu-id="909f4-292">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="909f4-292">**Top**</span></span>](c-top.md)<br/> |



 

 






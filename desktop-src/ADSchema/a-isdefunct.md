---
title: Is-Defunct atributo)
description: Si es TRUE, la clase o el atributo ya no se pueden usar. Puede que existan versiones anteriores de este objeto, pero no se pueden crear otras nuevas.
ms.assetid: ca1b7701-e501-424d-9c07-20835b23dcd3
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Is-Defunct
- isDefunct esquema de AD de atributos
topic_type:
- apiref
api_name:
- Is-Defunct
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895a4af5d02c76a709607753065b6e965966bb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658937"
---
# <a name="is-defunct-attribute"></a><span data-ttu-id="5a46d-106">Is-Defunct atributo)</span><span class="sxs-lookup"><span data-stu-id="5a46d-106">Is-Defunct attribute</span></span>

<span data-ttu-id="5a46d-107">Si es **true**, la clase o el atributo ya no se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="5a46d-107">If **TRUE**, the class or attribute is no longer usable.</span></span> <span data-ttu-id="5a46d-108">Puede que existan versiones anteriores de este objeto, pero no se pueden crear otras nuevas.</span><span class="sxs-lookup"><span data-stu-id="5a46d-108">Old versions of this object may exist, but new ones cannot be created.</span></span>



| <span data-ttu-id="5a46d-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a46d-109">Entry</span></span> | <span data-ttu-id="5a46d-110">Value</span><span class="sxs-lookup"><span data-stu-id="5a46d-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5a46d-111">CN</span><span class="sxs-lookup"><span data-stu-id="5a46d-111">CN</span></span>                | <span data-ttu-id="5a46d-112">Is-Defunct</span><span class="sxs-lookup"><span data-stu-id="5a46d-112">Is-Defunct</span></span>                           |
| <span data-ttu-id="5a46d-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5a46d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5a46d-114">isDefunct</span><span class="sxs-lookup"><span data-stu-id="5a46d-114">isDefunct</span></span>                            |
| <span data-ttu-id="5a46d-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5a46d-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="5a46d-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5a46d-116">Update Privilege</span></span>  | <span data-ttu-id="5a46d-117">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="5a46d-117">Schema administrator</span></span>                 |
| <span data-ttu-id="5a46d-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5a46d-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5a46d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5a46d-119">Attribute-Id</span></span>      | <span data-ttu-id="5a46d-120">1.2.840.113556.1.4.661</span><span class="sxs-lookup"><span data-stu-id="5a46d-120">1.2.840.113556.1.4.661</span></span>               |
| <span data-ttu-id="5a46d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5a46d-121">System-Id-Guid</span></span>    | <span data-ttu-id="5a46d-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5a46d-122">28630ebe-41d5-11d1-a9c1-0000f80367c1</span></span> |
| <span data-ttu-id="5a46d-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a46d-123">Syntax</span></span>            | [<span data-ttu-id="5a46d-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="5a46d-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="5a46d-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5a46d-125">Implementations</span></span>

-   [<span data-ttu-id="5a46d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5a46d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5a46d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5a46d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5a46d-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5a46d-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5a46d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5a46d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5a46d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5a46d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5a46d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5a46d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5a46d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5a46d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5a46d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a46d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="5a46d-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a46d-134">Entry</span></span> | <span data-ttu-id="5a46d-135">Value</span><span class="sxs-lookup"><span data-stu-id="5a46d-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a46d-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5a46d-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a46d-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a46d-138">System-Only</span></span>            | <span data-ttu-id="5a46d-139">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-139">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5a46d-140">Is-Single-Valued</span></span>       | <span data-ttu-id="5a46d-141">True</span><span class="sxs-lookup"><span data-stu-id="5a46d-141">True</span></span>                                                                                                      |
| <span data-ttu-id="5a46d-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5a46d-142">Is Indexed</span></span>             | <span data-ttu-id="5a46d-143">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-143">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5a46d-144">In Global Catalog</span></span>      | <span data-ttu-id="5a46d-145">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-145">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5a46d-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a46d-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a46d-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="5a46d-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a46d-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a46d-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-150">Search-Flags</span></span>           | <span data-ttu-id="5a46d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a46d-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="5a46d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-152">System-Flags</span></span>           | <span data-ttu-id="5a46d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a46d-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="5a46d-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5a46d-154">Classes used in</span></span>        | [<span data-ttu-id="5a46d-155">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="5a46d-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="5a46d-156">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="5a46d-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5a46d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a46d-157">Windows Server 2003</span></span>



| <span data-ttu-id="5a46d-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a46d-158">Entry</span></span> | <span data-ttu-id="5a46d-159">Value</span><span class="sxs-lookup"><span data-stu-id="5a46d-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a46d-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5a46d-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a46d-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a46d-162">System-Only</span></span>            | <span data-ttu-id="5a46d-163">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-163">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5a46d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="5a46d-165">True</span><span class="sxs-lookup"><span data-stu-id="5a46d-165">True</span></span>                                                                                                      |
| <span data-ttu-id="5a46d-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5a46d-166">Is Indexed</span></span>             | <span data-ttu-id="5a46d-167">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-167">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5a46d-168">In Global Catalog</span></span>      | <span data-ttu-id="5a46d-169">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-169">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5a46d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a46d-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a46d-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="5a46d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a46d-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a46d-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-174">Search-Flags</span></span>           | <span data-ttu-id="5a46d-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a46d-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="5a46d-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-176">System-Flags</span></span>           | <span data-ttu-id="5a46d-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a46d-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="5a46d-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5a46d-178">Classes used in</span></span>        | [<span data-ttu-id="5a46d-179">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="5a46d-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="5a46d-180">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="5a46d-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5a46d-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="5a46d-181">ADAM</span></span>



| <span data-ttu-id="5a46d-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a46d-182">Entry</span></span> | <span data-ttu-id="5a46d-183">Value</span><span class="sxs-lookup"><span data-stu-id="5a46d-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a46d-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5a46d-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a46d-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a46d-186">System-Only</span></span>            | <span data-ttu-id="5a46d-187">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-187">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5a46d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="5a46d-189">True</span><span class="sxs-lookup"><span data-stu-id="5a46d-189">True</span></span>                                                                                                      |
| <span data-ttu-id="5a46d-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5a46d-190">Is Indexed</span></span>             | <span data-ttu-id="5a46d-191">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-191">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5a46d-192">In Global Catalog</span></span>      | <span data-ttu-id="5a46d-193">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-193">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5a46d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a46d-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a46d-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="5a46d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a46d-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a46d-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-198">Search-Flags</span></span>           | <span data-ttu-id="5a46d-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a46d-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="5a46d-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-200">System-Flags</span></span>           | <span data-ttu-id="5a46d-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a46d-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="5a46d-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5a46d-202">Classes used in</span></span>        | [<span data-ttu-id="5a46d-203">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="5a46d-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="5a46d-204">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="5a46d-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5a46d-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5a46d-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5a46d-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a46d-206">Entry</span></span> | <span data-ttu-id="5a46d-207">Value</span><span class="sxs-lookup"><span data-stu-id="5a46d-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a46d-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5a46d-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a46d-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a46d-210">System-Only</span></span>            | <span data-ttu-id="5a46d-211">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-211">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5a46d-212">Is-Single-Valued</span></span>       | <span data-ttu-id="5a46d-213">True</span><span class="sxs-lookup"><span data-stu-id="5a46d-213">True</span></span>                                                                                                      |
| <span data-ttu-id="5a46d-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5a46d-214">Is Indexed</span></span>             | <span data-ttu-id="5a46d-215">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-215">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5a46d-216">In Global Catalog</span></span>      | <span data-ttu-id="5a46d-217">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-217">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5a46d-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a46d-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a46d-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="5a46d-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a46d-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a46d-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-222">Search-Flags</span></span>           | <span data-ttu-id="5a46d-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a46d-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="5a46d-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-224">System-Flags</span></span>           | <span data-ttu-id="5a46d-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a46d-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="5a46d-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5a46d-226">Classes used in</span></span>        | [<span data-ttu-id="5a46d-227">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="5a46d-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="5a46d-228">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="5a46d-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5a46d-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a46d-229">Windows Server 2008</span></span>



| <span data-ttu-id="5a46d-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a46d-230">Entry</span></span> | <span data-ttu-id="5a46d-231">Value</span><span class="sxs-lookup"><span data-stu-id="5a46d-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a46d-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5a46d-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a46d-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a46d-234">System-Only</span></span>            | <span data-ttu-id="5a46d-235">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-235">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5a46d-236">Is-Single-Valued</span></span>       | <span data-ttu-id="5a46d-237">True</span><span class="sxs-lookup"><span data-stu-id="5a46d-237">True</span></span>                                                                                                      |
| <span data-ttu-id="5a46d-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5a46d-238">Is Indexed</span></span>             | <span data-ttu-id="5a46d-239">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-239">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5a46d-240">In Global Catalog</span></span>      | <span data-ttu-id="5a46d-241">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-241">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5a46d-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a46d-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a46d-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="5a46d-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a46d-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a46d-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-246">Search-Flags</span></span>           | <span data-ttu-id="5a46d-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a46d-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="5a46d-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-248">System-Flags</span></span>           | <span data-ttu-id="5a46d-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a46d-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="5a46d-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5a46d-250">Classes used in</span></span>        | [<span data-ttu-id="5a46d-251">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="5a46d-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="5a46d-252">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="5a46d-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5a46d-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5a46d-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5a46d-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a46d-254">Entry</span></span> | <span data-ttu-id="5a46d-255">Value</span><span class="sxs-lookup"><span data-stu-id="5a46d-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a46d-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5a46d-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a46d-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a46d-258">System-Only</span></span>            | <span data-ttu-id="5a46d-259">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-259">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-260">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5a46d-260">Is-Single-Valued</span></span>       | <span data-ttu-id="5a46d-261">True</span><span class="sxs-lookup"><span data-stu-id="5a46d-261">True</span></span>                                                                                                      |
| <span data-ttu-id="5a46d-262">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5a46d-262">Is Indexed</span></span>             | <span data-ttu-id="5a46d-263">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-263">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-264">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5a46d-264">In Global Catalog</span></span>      | <span data-ttu-id="5a46d-265">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-265">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-266">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5a46d-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a46d-267">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a46d-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="5a46d-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a46d-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a46d-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-270">Search-Flags</span></span>           | <span data-ttu-id="5a46d-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a46d-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="5a46d-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-272">System-Flags</span></span>           | <span data-ttu-id="5a46d-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a46d-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="5a46d-274">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5a46d-274">Classes used in</span></span>        | [<span data-ttu-id="5a46d-275">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="5a46d-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="5a46d-276">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="5a46d-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5a46d-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a46d-277">Windows Server 2012</span></span>



| <span data-ttu-id="5a46d-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="5a46d-278">Entry</span></span> | <span data-ttu-id="5a46d-279">Value</span><span class="sxs-lookup"><span data-stu-id="5a46d-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a46d-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5a46d-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a46d-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="5a46d-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a46d-282">System-Only</span></span>            | <span data-ttu-id="5a46d-283">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-283">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-284">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5a46d-284">Is-Single-Valued</span></span>       | <span data-ttu-id="5a46d-285">True</span><span class="sxs-lookup"><span data-stu-id="5a46d-285">True</span></span>                                                                                                      |
| <span data-ttu-id="5a46d-286">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5a46d-286">Is Indexed</span></span>             | <span data-ttu-id="5a46d-287">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-287">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-288">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5a46d-288">In Global Catalog</span></span>      | <span data-ttu-id="5a46d-289">False</span><span class="sxs-lookup"><span data-stu-id="5a46d-289">False</span></span>                                                                                                     |
| <span data-ttu-id="5a46d-290">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5a46d-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a46d-291">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a46d-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="5a46d-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a46d-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a46d-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="5a46d-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-294">Search-Flags</span></span>           | <span data-ttu-id="5a46d-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a46d-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="5a46d-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a46d-296">System-Flags</span></span>           | <span data-ttu-id="5a46d-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a46d-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="5a46d-298">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5a46d-298">Classes used in</span></span>        | [<span data-ttu-id="5a46d-299">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="5a46d-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="5a46d-300">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="5a46d-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






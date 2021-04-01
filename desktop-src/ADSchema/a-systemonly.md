---
title: System-Only atributo)
description: Valor booleano que especifica si solo Active Directory puede modificar la clase. El agente del sistema de directorio solo puede crear o eliminar clases de sistema único.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de System-Only
- systemOnly esquema de AD de atributos
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1310eb5f13da3c17c20ac9c01f337ff2a018a545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905915"
---
# <a name="system-only-attribute"></a><span data-ttu-id="eb84e-106">System-Only atributo)</span><span class="sxs-lookup"><span data-stu-id="eb84e-106">System-Only attribute</span></span>

<span data-ttu-id="eb84e-107">Valor booleano que especifica si solo Active Directory puede modificar la clase.</span><span class="sxs-lookup"><span data-stu-id="eb84e-107">A Boolean value that specifies whether only Active Directory can modify the class.</span></span> <span data-ttu-id="eb84e-108">El agente del sistema de directorio solo puede crear o eliminar clases de sistema único.</span><span class="sxs-lookup"><span data-stu-id="eb84e-108">System-only classes can only be created or deleted by the Directory System Agent.</span></span>



| <span data-ttu-id="eb84e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb84e-109">Entry</span></span> | <span data-ttu-id="eb84e-110">Value</span><span class="sxs-lookup"><span data-stu-id="eb84e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="eb84e-111">CN</span><span class="sxs-lookup"><span data-stu-id="eb84e-111">CN</span></span>                | <span data-ttu-id="eb84e-112">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb84e-112">System-Only</span></span>                          |
| <span data-ttu-id="eb84e-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="eb84e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="eb84e-114">systemOnly</span><span class="sxs-lookup"><span data-stu-id="eb84e-114">systemOnly</span></span>                           |
| <span data-ttu-id="eb84e-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="eb84e-115">Size</span></span>              | <span data-ttu-id="eb84e-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="eb84e-116">4 bytes</span></span>                              |
| <span data-ttu-id="eb84e-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="eb84e-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="eb84e-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="eb84e-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="eb84e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eb84e-119">Attribute-Id</span></span>      | <span data-ttu-id="eb84e-120">1.2.840.113556.1.4.170</span><span class="sxs-lookup"><span data-stu-id="eb84e-120">1.2.840.113556.1.4.170</span></span>               |
| <span data-ttu-id="eb84e-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="eb84e-121">System-Id-Guid</span></span>    | <span data-ttu-id="eb84e-122">bf967a46-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="eb84e-122">bf967a46-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="eb84e-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb84e-123">Syntax</span></span>            | [<span data-ttu-id="eb84e-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="eb84e-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="eb84e-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="eb84e-125">Implementations</span></span>

-   [<span data-ttu-id="eb84e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="eb84e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="eb84e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eb84e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eb84e-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="eb84e-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="eb84e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eb84e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eb84e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eb84e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eb84e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eb84e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eb84e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eb84e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="eb84e-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eb84e-133">Windows 2000 Server</span></span>



| <span data-ttu-id="eb84e-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb84e-134">Entry</span></span> | <span data-ttu-id="eb84e-135">Value</span><span class="sxs-lookup"><span data-stu-id="eb84e-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb84e-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb84e-136">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb84e-137">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb84e-138">System-Only</span></span>            | <span data-ttu-id="eb84e-139">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-139">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb84e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="eb84e-141">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-141">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb84e-142">Is Indexed</span></span>             | <span data-ttu-id="eb84e-143">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-143">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb84e-144">In Global Catalog</span></span>      | <span data-ttu-id="eb84e-145">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-145">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb84e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb84e-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb84e-147">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="eb84e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb84e-148">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb84e-149">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-150">Search-Flags</span></span>           | <span data-ttu-id="eb84e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb84e-151">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="eb84e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-152">System-Flags</span></span>           | <span data-ttu-id="eb84e-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eb84e-153">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="eb84e-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb84e-154">Classes used in</span></span>        | [<span data-ttu-id="eb84e-155">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="eb84e-155">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="eb84e-156">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="eb84e-156">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="eb84e-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eb84e-157">Windows Server 2003</span></span>



| <span data-ttu-id="eb84e-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb84e-158">Entry</span></span> | <span data-ttu-id="eb84e-159">Value</span><span class="sxs-lookup"><span data-stu-id="eb84e-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb84e-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb84e-160">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb84e-161">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb84e-162">System-Only</span></span>            | <span data-ttu-id="eb84e-163">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-163">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb84e-164">Is-Single-Valued</span></span>       | <span data-ttu-id="eb84e-165">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-165">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb84e-166">Is Indexed</span></span>             | <span data-ttu-id="eb84e-167">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-167">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb84e-168">In Global Catalog</span></span>      | <span data-ttu-id="eb84e-169">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-169">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb84e-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb84e-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb84e-171">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="eb84e-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb84e-172">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb84e-173">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-174">Search-Flags</span></span>           | <span data-ttu-id="eb84e-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb84e-175">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="eb84e-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-176">System-Flags</span></span>           | <span data-ttu-id="eb84e-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eb84e-177">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="eb84e-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb84e-178">Classes used in</span></span>        | [<span data-ttu-id="eb84e-179">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="eb84e-179">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="eb84e-180">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="eb84e-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="eb84e-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="eb84e-181">ADAM</span></span>



| <span data-ttu-id="eb84e-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb84e-182">Entry</span></span> | <span data-ttu-id="eb84e-183">Value</span><span class="sxs-lookup"><span data-stu-id="eb84e-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb84e-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb84e-184">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb84e-185">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb84e-186">System-Only</span></span>            | <span data-ttu-id="eb84e-187">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-187">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb84e-188">Is-Single-Valued</span></span>       | <span data-ttu-id="eb84e-189">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-189">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb84e-190">Is Indexed</span></span>             | <span data-ttu-id="eb84e-191">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-191">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb84e-192">In Global Catalog</span></span>      | <span data-ttu-id="eb84e-193">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-193">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb84e-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb84e-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb84e-195">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="eb84e-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb84e-196">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb84e-197">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-198">Search-Flags</span></span>           | <span data-ttu-id="eb84e-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb84e-199">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="eb84e-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-200">System-Flags</span></span>           | <span data-ttu-id="eb84e-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eb84e-201">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="eb84e-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb84e-202">Classes used in</span></span>        | [<span data-ttu-id="eb84e-203">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="eb84e-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="eb84e-204">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="eb84e-204">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eb84e-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eb84e-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eb84e-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb84e-206">Entry</span></span> | <span data-ttu-id="eb84e-207">Value</span><span class="sxs-lookup"><span data-stu-id="eb84e-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb84e-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb84e-208">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb84e-209">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb84e-210">System-Only</span></span>            | <span data-ttu-id="eb84e-211">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-211">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb84e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="eb84e-213">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-213">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb84e-214">Is Indexed</span></span>             | <span data-ttu-id="eb84e-215">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-215">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb84e-216">In Global Catalog</span></span>      | <span data-ttu-id="eb84e-217">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-217">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb84e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb84e-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb84e-219">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="eb84e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb84e-220">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb84e-221">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-222">Search-Flags</span></span>           | <span data-ttu-id="eb84e-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb84e-223">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="eb84e-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-224">System-Flags</span></span>           | <span data-ttu-id="eb84e-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eb84e-225">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="eb84e-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb84e-226">Classes used in</span></span>        | [<span data-ttu-id="eb84e-227">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="eb84e-227">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="eb84e-228">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="eb84e-228">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eb84e-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb84e-229">Windows Server 2008</span></span>



| <span data-ttu-id="eb84e-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb84e-230">Entry</span></span> | <span data-ttu-id="eb84e-231">Value</span><span class="sxs-lookup"><span data-stu-id="eb84e-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb84e-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb84e-232">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb84e-233">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb84e-234">System-Only</span></span>            | <span data-ttu-id="eb84e-235">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-235">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-236">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb84e-236">Is-Single-Valued</span></span>       | <span data-ttu-id="eb84e-237">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-237">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-238">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb84e-238">Is Indexed</span></span>             | <span data-ttu-id="eb84e-239">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-239">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-240">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb84e-240">In Global Catalog</span></span>      | <span data-ttu-id="eb84e-241">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-241">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-242">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb84e-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb84e-243">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb84e-243">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="eb84e-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb84e-244">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb84e-245">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-246">Search-Flags</span></span>           | <span data-ttu-id="eb84e-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb84e-247">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="eb84e-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-248">System-Flags</span></span>           | <span data-ttu-id="eb84e-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eb84e-249">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="eb84e-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb84e-250">Classes used in</span></span>        | [<span data-ttu-id="eb84e-251">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="eb84e-251">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="eb84e-252">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="eb84e-252">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eb84e-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb84e-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eb84e-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb84e-254">Entry</span></span> | <span data-ttu-id="eb84e-255">Value</span><span class="sxs-lookup"><span data-stu-id="eb84e-255">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb84e-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb84e-256">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb84e-257">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb84e-258">System-Only</span></span>            | <span data-ttu-id="eb84e-259">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-259">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-260">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb84e-260">Is-Single-Valued</span></span>       | <span data-ttu-id="eb84e-261">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-261">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-262">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb84e-262">Is Indexed</span></span>             | <span data-ttu-id="eb84e-263">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-263">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-264">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb84e-264">In Global Catalog</span></span>      | <span data-ttu-id="eb84e-265">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-265">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-266">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb84e-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb84e-267">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb84e-267">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="eb84e-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb84e-268">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb84e-269">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-270">Search-Flags</span></span>           | <span data-ttu-id="eb84e-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb84e-271">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="eb84e-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-272">System-Flags</span></span>           | <span data-ttu-id="eb84e-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eb84e-273">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="eb84e-274">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb84e-274">Classes used in</span></span>        | [<span data-ttu-id="eb84e-275">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="eb84e-275">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="eb84e-276">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="eb84e-276">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eb84e-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb84e-277">Windows Server 2012</span></span>



| <span data-ttu-id="eb84e-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb84e-278">Entry</span></span> | <span data-ttu-id="eb84e-279">Value</span><span class="sxs-lookup"><span data-stu-id="eb84e-279">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb84e-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="eb84e-280">Link-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb84e-281">MAPI-Id</span></span>                | \-                                                                                                        |
| <span data-ttu-id="eb84e-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb84e-282">System-Only</span></span>            | <span data-ttu-id="eb84e-283">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-283">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-284">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="eb84e-284">Is-Single-Valued</span></span>       | <span data-ttu-id="eb84e-285">True</span><span class="sxs-lookup"><span data-stu-id="eb84e-285">True</span></span>                                                                                                      |
| <span data-ttu-id="eb84e-286">Está indexado</span><span class="sxs-lookup"><span data-stu-id="eb84e-286">Is Indexed</span></span>             | <span data-ttu-id="eb84e-287">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-287">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-288">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="eb84e-288">In Global Catalog</span></span>      | <span data-ttu-id="eb84e-289">False</span><span class="sxs-lookup"><span data-stu-id="eb84e-289">False</span></span>                                                                                                     |
| <span data-ttu-id="eb84e-290">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="eb84e-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb84e-291">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb84e-291">O:BAG:BAD:S:</span></span>                                                                                              |
| <span data-ttu-id="eb84e-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb84e-292">Range-Lower</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb84e-293">Range-Upper</span></span>            | \-                                                                                                        |
| <span data-ttu-id="eb84e-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-294">Search-Flags</span></span>           | <span data-ttu-id="eb84e-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb84e-295">0x00000000</span></span>                                                                                                |
| <span data-ttu-id="eb84e-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb84e-296">System-Flags</span></span>           | <span data-ttu-id="eb84e-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eb84e-297">0x00000010</span></span>                                                                                                |
| <span data-ttu-id="eb84e-298">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="eb84e-298">Classes used in</span></span>        | [<span data-ttu-id="eb84e-299">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="eb84e-299">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="eb84e-300">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="eb84e-300">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






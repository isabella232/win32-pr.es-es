---
title: Atributo default-Security-Descriptor
description: El descriptor de seguridad que se va a asignar al objeto cuando se crea por primera vez.
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- Default-Security-Descriptor atributo AD Schema
- defaultSecurityDescriptor esquema de AD de atributos
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0b4a8dbe0c633a15b6a5167cb1171a14d1769
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493552"
---
# <a name="default-security-descriptor-attribute"></a><span data-ttu-id="a2ad9-105">Atributo default-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-105">Default-Security-Descriptor attribute</span></span>

<span data-ttu-id="a2ad9-106">El descriptor de seguridad que se va a asignar al objeto cuando se crea por primera vez.</span><span class="sxs-lookup"><span data-stu-id="a2ad9-106">The security descriptor to be assigned to the object when it is first created.</span></span>



| <span data-ttu-id="a2ad9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2ad9-107">Entry</span></span> | <span data-ttu-id="a2ad9-108">Value</span><span class="sxs-lookup"><span data-stu-id="a2ad9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a2ad9-109">CN</span><span class="sxs-lookup"><span data-stu-id="a2ad9-109">CN</span></span>                | <span data-ttu-id="a2ad9-110">Default-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-110">Default-Security-Descriptor</span></span>                 |
| <span data-ttu-id="a2ad9-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a2ad9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a2ad9-112">defaultSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-112">defaultSecurityDescriptor</span></span>                   |
| <span data-ttu-id="a2ad9-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a2ad9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a2ad9-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a2ad9-114">Update Privilege</span></span>  | <span data-ttu-id="a2ad9-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="a2ad9-115">Schema administrator</span></span>                        |
| <span data-ttu-id="a2ad9-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a2ad9-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a2ad9-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a2ad9-117">Attribute-Id</span></span>      | <span data-ttu-id="a2ad9-118">1.2.840.113556.1.4.224</span><span class="sxs-lookup"><span data-stu-id="a2ad9-118">1.2.840.113556.1.4.224</span></span>                      |
| <span data-ttu-id="a2ad9-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a2ad9-119">System-Id-Guid</span></span>    | <span data-ttu-id="a2ad9-120">807a6d30-1669-11d0-a064-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="a2ad9-120">807a6d30-1669-11d0-a064-00aa006c33ed</span></span>        |
| <span data-ttu-id="a2ad9-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2ad9-121">Syntax</span></span>            | [<span data-ttu-id="a2ad9-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a2ad9-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a2ad9-123">Implementations</span></span>

-   [<span data-ttu-id="a2ad9-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a2ad9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a2ad9-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a2ad9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a2ad9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a2ad9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a2ad9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a2ad9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2ad9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a2ad9-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2ad9-132">Entry</span></span> | <span data-ttu-id="a2ad9-133">Value</span><span class="sxs-lookup"><span data-stu-id="a2ad9-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a2ad9-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a2ad9-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ad9-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ad9-136">System-Only</span></span>            | <span data-ttu-id="a2ad9-137">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-137">False</span></span>                                            |
| <span data-ttu-id="a2ad9-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ad9-139">True</span><span class="sxs-lookup"><span data-stu-id="a2ad9-139">True</span></span>                                             |
| <span data-ttu-id="a2ad9-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a2ad9-140">Is Indexed</span></span>             | <span data-ttu-id="a2ad9-141">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-141">False</span></span>                                            |
| <span data-ttu-id="a2ad9-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2ad9-142">In Global Catalog</span></span>      | <span data-ttu-id="a2ad9-143">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-143">False</span></span>                                            |
| <span data-ttu-id="a2ad9-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a2ad9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ad9-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2ad9-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a2ad9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ad9-146">Range-Lower</span></span>            | <span data-ttu-id="a2ad9-147">0</span><span class="sxs-lookup"><span data-stu-id="a2ad9-147">0</span></span>                                                |
| <span data-ttu-id="a2ad9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ad9-148">Range-Upper</span></span>            | <span data-ttu-id="a2ad9-149">32767</span><span class="sxs-lookup"><span data-stu-id="a2ad9-149">32767</span></span>                                            |
| <span data-ttu-id="a2ad9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-150">Search-Flags</span></span>           | <span data-ttu-id="a2ad9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ad9-151">0x00000000</span></span>                                       |
| <span data-ttu-id="a2ad9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-152">System-Flags</span></span>           | <span data-ttu-id="a2ad9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ad9-153">0x00000010</span></span>                                       |
| <span data-ttu-id="a2ad9-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a2ad9-154">Classes used in</span></span>        | [<span data-ttu-id="a2ad9-155">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-155">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a2ad9-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2ad9-156">Windows Server 2003</span></span>



| <span data-ttu-id="a2ad9-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2ad9-157">Entry</span></span> | <span data-ttu-id="a2ad9-158">Value</span><span class="sxs-lookup"><span data-stu-id="a2ad9-158">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a2ad9-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a2ad9-159">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ad9-160">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ad9-161">System-Only</span></span>            | <span data-ttu-id="a2ad9-162">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-162">False</span></span>                                            |
| <span data-ttu-id="a2ad9-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ad9-164">True</span><span class="sxs-lookup"><span data-stu-id="a2ad9-164">True</span></span>                                             |
| <span data-ttu-id="a2ad9-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a2ad9-165">Is Indexed</span></span>             | <span data-ttu-id="a2ad9-166">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-166">False</span></span>                                            |
| <span data-ttu-id="a2ad9-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2ad9-167">In Global Catalog</span></span>      | <span data-ttu-id="a2ad9-168">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-168">False</span></span>                                            |
| <span data-ttu-id="a2ad9-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a2ad9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ad9-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2ad9-170">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a2ad9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ad9-171">Range-Lower</span></span>            | <span data-ttu-id="a2ad9-172">0</span><span class="sxs-lookup"><span data-stu-id="a2ad9-172">0</span></span>                                                |
| <span data-ttu-id="a2ad9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ad9-173">Range-Upper</span></span>            | <span data-ttu-id="a2ad9-174">32767</span><span class="sxs-lookup"><span data-stu-id="a2ad9-174">32767</span></span>                                            |
| <span data-ttu-id="a2ad9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-175">Search-Flags</span></span>           | <span data-ttu-id="a2ad9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ad9-176">0x00000000</span></span>                                       |
| <span data-ttu-id="a2ad9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-177">System-Flags</span></span>           | <span data-ttu-id="a2ad9-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ad9-178">0x00000010</span></span>                                       |
| <span data-ttu-id="a2ad9-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a2ad9-179">Classes used in</span></span>        | [<span data-ttu-id="a2ad9-180">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-180">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a2ad9-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="a2ad9-181">ADAM</span></span>



| <span data-ttu-id="a2ad9-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2ad9-182">Entry</span></span> | <span data-ttu-id="a2ad9-183">Value</span><span class="sxs-lookup"><span data-stu-id="a2ad9-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a2ad9-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a2ad9-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ad9-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ad9-186">System-Only</span></span>            | <span data-ttu-id="a2ad9-187">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-187">False</span></span>                                            |
| <span data-ttu-id="a2ad9-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ad9-189">True</span><span class="sxs-lookup"><span data-stu-id="a2ad9-189">True</span></span>                                             |
| <span data-ttu-id="a2ad9-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a2ad9-190">Is Indexed</span></span>             | <span data-ttu-id="a2ad9-191">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-191">False</span></span>                                            |
| <span data-ttu-id="a2ad9-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2ad9-192">In Global Catalog</span></span>      | <span data-ttu-id="a2ad9-193">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-193">False</span></span>                                            |
| <span data-ttu-id="a2ad9-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a2ad9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ad9-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2ad9-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a2ad9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ad9-196">Range-Lower</span></span>            | <span data-ttu-id="a2ad9-197">0</span><span class="sxs-lookup"><span data-stu-id="a2ad9-197">0</span></span>                                                |
| <span data-ttu-id="a2ad9-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ad9-198">Range-Upper</span></span>            | <span data-ttu-id="a2ad9-199">32767</span><span class="sxs-lookup"><span data-stu-id="a2ad9-199">32767</span></span>                                            |
| <span data-ttu-id="a2ad9-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-200">Search-Flags</span></span>           | <span data-ttu-id="a2ad9-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ad9-201">0x00000000</span></span>                                       |
| <span data-ttu-id="a2ad9-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-202">System-Flags</span></span>           | <span data-ttu-id="a2ad9-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ad9-203">0x00000010</span></span>                                       |
| <span data-ttu-id="a2ad9-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a2ad9-204">Classes used in</span></span>        | [<span data-ttu-id="a2ad9-205">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-205">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a2ad9-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a2ad9-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a2ad9-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2ad9-207">Entry</span></span> | <span data-ttu-id="a2ad9-208">Value</span><span class="sxs-lookup"><span data-stu-id="a2ad9-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a2ad9-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a2ad9-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ad9-210">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ad9-211">System-Only</span></span>            | <span data-ttu-id="a2ad9-212">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-212">False</span></span>                                            |
| <span data-ttu-id="a2ad9-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ad9-214">True</span><span class="sxs-lookup"><span data-stu-id="a2ad9-214">True</span></span>                                             |
| <span data-ttu-id="a2ad9-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a2ad9-215">Is Indexed</span></span>             | <span data-ttu-id="a2ad9-216">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-216">False</span></span>                                            |
| <span data-ttu-id="a2ad9-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2ad9-217">In Global Catalog</span></span>      | <span data-ttu-id="a2ad9-218">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-218">False</span></span>                                            |
| <span data-ttu-id="a2ad9-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a2ad9-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ad9-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2ad9-220">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a2ad9-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ad9-221">Range-Lower</span></span>            | <span data-ttu-id="a2ad9-222">0</span><span class="sxs-lookup"><span data-stu-id="a2ad9-222">0</span></span>                                                |
| <span data-ttu-id="a2ad9-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ad9-223">Range-Upper</span></span>            | <span data-ttu-id="a2ad9-224">32767</span><span class="sxs-lookup"><span data-stu-id="a2ad9-224">32767</span></span>                                            |
| <span data-ttu-id="a2ad9-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-225">Search-Flags</span></span>           | <span data-ttu-id="a2ad9-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ad9-226">0x00000000</span></span>                                       |
| <span data-ttu-id="a2ad9-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-227">System-Flags</span></span>           | <span data-ttu-id="a2ad9-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ad9-228">0x00000010</span></span>                                       |
| <span data-ttu-id="a2ad9-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a2ad9-229">Classes used in</span></span>        | [<span data-ttu-id="a2ad9-230">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-230">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a2ad9-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2ad9-231">Windows Server 2008</span></span>



| <span data-ttu-id="a2ad9-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2ad9-232">Entry</span></span> | <span data-ttu-id="a2ad9-233">Value</span><span class="sxs-lookup"><span data-stu-id="a2ad9-233">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a2ad9-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a2ad9-234">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ad9-235">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ad9-236">System-Only</span></span>            | <span data-ttu-id="a2ad9-237">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-237">False</span></span>                                            |
| <span data-ttu-id="a2ad9-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-238">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ad9-239">True</span><span class="sxs-lookup"><span data-stu-id="a2ad9-239">True</span></span>                                             |
| <span data-ttu-id="a2ad9-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a2ad9-240">Is Indexed</span></span>             | <span data-ttu-id="a2ad9-241">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-241">False</span></span>                                            |
| <span data-ttu-id="a2ad9-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2ad9-242">In Global Catalog</span></span>      | <span data-ttu-id="a2ad9-243">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-243">False</span></span>                                            |
| <span data-ttu-id="a2ad9-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a2ad9-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ad9-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2ad9-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a2ad9-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ad9-246">Range-Lower</span></span>            | <span data-ttu-id="a2ad9-247">0</span><span class="sxs-lookup"><span data-stu-id="a2ad9-247">0</span></span>                                                |
| <span data-ttu-id="a2ad9-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ad9-248">Range-Upper</span></span>            | <span data-ttu-id="a2ad9-249">32767</span><span class="sxs-lookup"><span data-stu-id="a2ad9-249">32767</span></span>                                            |
| <span data-ttu-id="a2ad9-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-250">Search-Flags</span></span>           | <span data-ttu-id="a2ad9-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ad9-251">0x00000000</span></span>                                       |
| <span data-ttu-id="a2ad9-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-252">System-Flags</span></span>           | <span data-ttu-id="a2ad9-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ad9-253">0x00000010</span></span>                                       |
| <span data-ttu-id="a2ad9-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a2ad9-254">Classes used in</span></span>        | [<span data-ttu-id="a2ad9-255">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-255">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a2ad9-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2ad9-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a2ad9-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2ad9-257">Entry</span></span> | <span data-ttu-id="a2ad9-258">Value</span><span class="sxs-lookup"><span data-stu-id="a2ad9-258">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a2ad9-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a2ad9-259">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ad9-260">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ad9-261">System-Only</span></span>            | <span data-ttu-id="a2ad9-262">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-262">False</span></span>                                            |
| <span data-ttu-id="a2ad9-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-263">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ad9-264">True</span><span class="sxs-lookup"><span data-stu-id="a2ad9-264">True</span></span>                                             |
| <span data-ttu-id="a2ad9-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a2ad9-265">Is Indexed</span></span>             | <span data-ttu-id="a2ad9-266">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-266">False</span></span>                                            |
| <span data-ttu-id="a2ad9-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2ad9-267">In Global Catalog</span></span>      | <span data-ttu-id="a2ad9-268">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-268">False</span></span>                                            |
| <span data-ttu-id="a2ad9-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a2ad9-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ad9-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2ad9-270">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a2ad9-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ad9-271">Range-Lower</span></span>            | <span data-ttu-id="a2ad9-272">0</span><span class="sxs-lookup"><span data-stu-id="a2ad9-272">0</span></span>                                                |
| <span data-ttu-id="a2ad9-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ad9-273">Range-Upper</span></span>            | <span data-ttu-id="a2ad9-274">32767</span><span class="sxs-lookup"><span data-stu-id="a2ad9-274">32767</span></span>                                            |
| <span data-ttu-id="a2ad9-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-275">Search-Flags</span></span>           | <span data-ttu-id="a2ad9-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ad9-276">0x00000000</span></span>                                       |
| <span data-ttu-id="a2ad9-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-277">System-Flags</span></span>           | <span data-ttu-id="a2ad9-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ad9-278">0x00000010</span></span>                                       |
| <span data-ttu-id="a2ad9-279">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a2ad9-279">Classes used in</span></span>        | [<span data-ttu-id="a2ad9-280">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-280">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a2ad9-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2ad9-281">Windows Server 2012</span></span>



| <span data-ttu-id="a2ad9-282">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2ad9-282">Entry</span></span> | <span data-ttu-id="a2ad9-283">Value</span><span class="sxs-lookup"><span data-stu-id="a2ad9-283">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="a2ad9-284">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a2ad9-284">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-285">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a2ad9-285">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="a2ad9-286">System-Only</span><span class="sxs-lookup"><span data-stu-id="a2ad9-286">System-Only</span></span>            | <span data-ttu-id="a2ad9-287">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-287">False</span></span>                                            |
| <span data-ttu-id="a2ad9-288">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a2ad9-288">Is-Single-Valued</span></span>       | <span data-ttu-id="a2ad9-289">True</span><span class="sxs-lookup"><span data-stu-id="a2ad9-289">True</span></span>                                             |
| <span data-ttu-id="a2ad9-290">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a2ad9-290">Is Indexed</span></span>             | <span data-ttu-id="a2ad9-291">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-291">False</span></span>                                            |
| <span data-ttu-id="a2ad9-292">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a2ad9-292">In Global Catalog</span></span>      | <span data-ttu-id="a2ad9-293">False</span><span class="sxs-lookup"><span data-stu-id="a2ad9-293">False</span></span>                                            |
| <span data-ttu-id="a2ad9-294">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a2ad9-294">NT-Security-Descriptor</span></span> | <span data-ttu-id="a2ad9-295">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a2ad9-295">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="a2ad9-296">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a2ad9-296">Range-Lower</span></span>            | <span data-ttu-id="a2ad9-297">0</span><span class="sxs-lookup"><span data-stu-id="a2ad9-297">0</span></span>                                                |
| <span data-ttu-id="a2ad9-298">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a2ad9-298">Range-Upper</span></span>            | <span data-ttu-id="a2ad9-299">32767</span><span class="sxs-lookup"><span data-stu-id="a2ad9-299">32767</span></span>                                            |
| <span data-ttu-id="a2ad9-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-300">Search-Flags</span></span>           | <span data-ttu-id="a2ad9-301">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a2ad9-301">0x00000000</span></span>                                       |
| <span data-ttu-id="a2ad9-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a2ad9-302">System-Flags</span></span>           | <span data-ttu-id="a2ad9-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a2ad9-303">0x00000010</span></span>                                       |
| <span data-ttu-id="a2ad9-304">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a2ad9-304">Classes used in</span></span>        | [<span data-ttu-id="a2ad9-305">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="a2ad9-305">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






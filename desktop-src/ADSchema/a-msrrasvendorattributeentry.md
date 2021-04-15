---
title: atributo MS-RRAS-Vendor-Attribute-entry
description: Cadena que permite a los proveedores agregar atributos de enrutador al DS para su uso en consultas, con el formato AttributeName vendorID AttributeType.
ms.assetid: 07bc4d9b-eba9-456b-be21-cd7bb8a5b0b6
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-RRAS-Vendor-Attribute-entry
- msRRASVendorAttributeEntry esquema de AD de atributos
topic_type:
- apiref
api_name:
- ms-RRAS-Vendor-Attribute-Entry
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28ee353122107db5b1247860e9799db861b4d6bf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493769"
---
# <a name="ms-rras-vendor-attribute-entry-attribute"></a><span data-ttu-id="6df67-105">atributo MS-RRAS-Vendor-Attribute-entry</span><span class="sxs-lookup"><span data-stu-id="6df67-105">ms-RRAS-Vendor-Attribute-Entry attribute</span></span>

<span data-ttu-id="6df67-106">Cadena que permite a los proveedores agregar atributos de enrutador al DS para su uso en las consultas, con el formato AttributeName: vendorID: AttributeType.</span><span class="sxs-lookup"><span data-stu-id="6df67-106">A string that enables vendors to add router attributes to the DS for use in queries, in the form AttributeName:vendorID:AttributeType.</span></span>



| <span data-ttu-id="6df67-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="6df67-107">Entry</span></span> | <span data-ttu-id="6df67-108">Value</span><span class="sxs-lookup"><span data-stu-id="6df67-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6df67-109">CN</span><span class="sxs-lookup"><span data-stu-id="6df67-109">CN</span></span>                | <span data-ttu-id="6df67-110">MS-RRAS-Vendor-Attribute-entry</span><span class="sxs-lookup"><span data-stu-id="6df67-110">ms-RRAS-Vendor-Attribute-Entry</span></span>              |
| <span data-ttu-id="6df67-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6df67-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6df67-112">msRRASVendorAttributeEntry</span><span class="sxs-lookup"><span data-stu-id="6df67-112">msRRASVendorAttributeEntry</span></span>                  |
| <span data-ttu-id="6df67-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6df67-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6df67-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6df67-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6df67-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6df67-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6df67-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6df67-116">Attribute-Id</span></span>      | <span data-ttu-id="6df67-117">1.2.840.113556.1.4.883</span><span class="sxs-lookup"><span data-stu-id="6df67-117">1.2.840.113556.1.4.883</span></span>                      |
| <span data-ttu-id="6df67-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6df67-118">System-Id-Guid</span></span>    | <span data-ttu-id="6df67-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6df67-119">f39b98ac-938d-11d1-aebd-0000f80367c1</span></span>        |
| <span data-ttu-id="6df67-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6df67-120">Syntax</span></span>            | [<span data-ttu-id="6df67-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6df67-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6df67-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6df67-122">Implementations</span></span>

-   [<span data-ttu-id="6df67-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6df67-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6df67-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6df67-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6df67-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6df67-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6df67-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6df67-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6df67-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6df67-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6df67-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6df67-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6df67-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6df67-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6df67-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="6df67-130">Entry</span></span> | <span data-ttu-id="6df67-131">Value</span><span class="sxs-lookup"><span data-stu-id="6df67-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6df67-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6df67-132">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6df67-133">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6df67-134">System-Only</span></span>            | <span data-ttu-id="6df67-135">False</span><span class="sxs-lookup"><span data-stu-id="6df67-135">False</span></span>                                                                               |
| <span data-ttu-id="6df67-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6df67-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6df67-137">False</span><span class="sxs-lookup"><span data-stu-id="6df67-137">False</span></span>                                                                               |
| <span data-ttu-id="6df67-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6df67-138">Is Indexed</span></span>             | <span data-ttu-id="6df67-139">False</span><span class="sxs-lookup"><span data-stu-id="6df67-139">False</span></span>                                                                               |
| <span data-ttu-id="6df67-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6df67-140">In Global Catalog</span></span>      | <span data-ttu-id="6df67-141">False</span><span class="sxs-lookup"><span data-stu-id="6df67-141">False</span></span>                                                                               |
| <span data-ttu-id="6df67-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6df67-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6df67-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6df67-143">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="6df67-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6df67-144">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6df67-145">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-146">Search-Flags</span></span>           | <span data-ttu-id="6df67-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6df67-147">0x00000000</span></span>                                                                          |
| <span data-ttu-id="6df67-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-148">System-Flags</span></span>           | <span data-ttu-id="6df67-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6df67-149">0x00000010</span></span>                                                                          |
| <span data-ttu-id="6df67-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6df67-150">Classes used in</span></span>        | [<span data-ttu-id="6df67-151">**RRAS-Administration-Diccionario**</span><span class="sxs-lookup"><span data-stu-id="6df67-151">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6df67-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6df67-152">Windows Server 2003</span></span>



| <span data-ttu-id="6df67-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="6df67-153">Entry</span></span> | <span data-ttu-id="6df67-154">Value</span><span class="sxs-lookup"><span data-stu-id="6df67-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6df67-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6df67-155">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6df67-156">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="6df67-157">System-Only</span></span>            | <span data-ttu-id="6df67-158">False</span><span class="sxs-lookup"><span data-stu-id="6df67-158">False</span></span>                                                                               |
| <span data-ttu-id="6df67-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6df67-159">Is-Single-Valued</span></span>       | <span data-ttu-id="6df67-160">False</span><span class="sxs-lookup"><span data-stu-id="6df67-160">False</span></span>                                                                               |
| <span data-ttu-id="6df67-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6df67-161">Is Indexed</span></span>             | <span data-ttu-id="6df67-162">False</span><span class="sxs-lookup"><span data-stu-id="6df67-162">False</span></span>                                                                               |
| <span data-ttu-id="6df67-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6df67-163">In Global Catalog</span></span>      | <span data-ttu-id="6df67-164">False</span><span class="sxs-lookup"><span data-stu-id="6df67-164">False</span></span>                                                                               |
| <span data-ttu-id="6df67-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6df67-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="6df67-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6df67-166">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="6df67-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6df67-167">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6df67-168">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-169">Search-Flags</span></span>           | <span data-ttu-id="6df67-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6df67-170">0x00000000</span></span>                                                                          |
| <span data-ttu-id="6df67-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-171">System-Flags</span></span>           | <span data-ttu-id="6df67-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6df67-172">0x00000010</span></span>                                                                          |
| <span data-ttu-id="6df67-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6df67-173">Classes used in</span></span>        | [<span data-ttu-id="6df67-174">**RRAS-Administration-Diccionario**</span><span class="sxs-lookup"><span data-stu-id="6df67-174">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6df67-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6df67-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6df67-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="6df67-176">Entry</span></span> | <span data-ttu-id="6df67-177">Value</span><span class="sxs-lookup"><span data-stu-id="6df67-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6df67-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6df67-178">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6df67-179">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="6df67-180">System-Only</span></span>            | <span data-ttu-id="6df67-181">False</span><span class="sxs-lookup"><span data-stu-id="6df67-181">False</span></span>                                                                               |
| <span data-ttu-id="6df67-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6df67-182">Is-Single-Valued</span></span>       | <span data-ttu-id="6df67-183">False</span><span class="sxs-lookup"><span data-stu-id="6df67-183">False</span></span>                                                                               |
| <span data-ttu-id="6df67-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6df67-184">Is Indexed</span></span>             | <span data-ttu-id="6df67-185">False</span><span class="sxs-lookup"><span data-stu-id="6df67-185">False</span></span>                                                                               |
| <span data-ttu-id="6df67-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6df67-186">In Global Catalog</span></span>      | <span data-ttu-id="6df67-187">False</span><span class="sxs-lookup"><span data-stu-id="6df67-187">False</span></span>                                                                               |
| <span data-ttu-id="6df67-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6df67-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="6df67-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6df67-189">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="6df67-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6df67-190">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6df67-191">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-192">Search-Flags</span></span>           | <span data-ttu-id="6df67-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6df67-193">0x00000000</span></span>                                                                          |
| <span data-ttu-id="6df67-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-194">System-Flags</span></span>           | <span data-ttu-id="6df67-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6df67-195">0x00000010</span></span>                                                                          |
| <span data-ttu-id="6df67-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6df67-196">Classes used in</span></span>        | [<span data-ttu-id="6df67-197">**RRAS-Administration-Diccionario**</span><span class="sxs-lookup"><span data-stu-id="6df67-197">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6df67-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6df67-198">Windows Server 2008</span></span>



| <span data-ttu-id="6df67-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="6df67-199">Entry</span></span> | <span data-ttu-id="6df67-200">Value</span><span class="sxs-lookup"><span data-stu-id="6df67-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6df67-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6df67-201">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6df67-202">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="6df67-203">System-Only</span></span>            | <span data-ttu-id="6df67-204">False</span><span class="sxs-lookup"><span data-stu-id="6df67-204">False</span></span>                                                                               |
| <span data-ttu-id="6df67-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6df67-205">Is-Single-Valued</span></span>       | <span data-ttu-id="6df67-206">False</span><span class="sxs-lookup"><span data-stu-id="6df67-206">False</span></span>                                                                               |
| <span data-ttu-id="6df67-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6df67-207">Is Indexed</span></span>             | <span data-ttu-id="6df67-208">False</span><span class="sxs-lookup"><span data-stu-id="6df67-208">False</span></span>                                                                               |
| <span data-ttu-id="6df67-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6df67-209">In Global Catalog</span></span>      | <span data-ttu-id="6df67-210">False</span><span class="sxs-lookup"><span data-stu-id="6df67-210">False</span></span>                                                                               |
| <span data-ttu-id="6df67-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6df67-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="6df67-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6df67-212">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="6df67-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6df67-213">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6df67-214">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-215">Search-Flags</span></span>           | <span data-ttu-id="6df67-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6df67-216">0x00000000</span></span>                                                                          |
| <span data-ttu-id="6df67-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-217">System-Flags</span></span>           | <span data-ttu-id="6df67-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6df67-218">0x00000010</span></span>                                                                          |
| <span data-ttu-id="6df67-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6df67-219">Classes used in</span></span>        | [<span data-ttu-id="6df67-220">**RRAS-Administration-Diccionario**</span><span class="sxs-lookup"><span data-stu-id="6df67-220">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6df67-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6df67-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6df67-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="6df67-222">Entry</span></span> | <span data-ttu-id="6df67-223">Value</span><span class="sxs-lookup"><span data-stu-id="6df67-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6df67-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6df67-224">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6df67-225">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="6df67-226">System-Only</span></span>            | <span data-ttu-id="6df67-227">False</span><span class="sxs-lookup"><span data-stu-id="6df67-227">False</span></span>                                                                               |
| <span data-ttu-id="6df67-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6df67-228">Is-Single-Valued</span></span>       | <span data-ttu-id="6df67-229">False</span><span class="sxs-lookup"><span data-stu-id="6df67-229">False</span></span>                                                                               |
| <span data-ttu-id="6df67-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6df67-230">Is Indexed</span></span>             | <span data-ttu-id="6df67-231">False</span><span class="sxs-lookup"><span data-stu-id="6df67-231">False</span></span>                                                                               |
| <span data-ttu-id="6df67-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6df67-232">In Global Catalog</span></span>      | <span data-ttu-id="6df67-233">False</span><span class="sxs-lookup"><span data-stu-id="6df67-233">False</span></span>                                                                               |
| <span data-ttu-id="6df67-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6df67-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="6df67-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6df67-235">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="6df67-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6df67-236">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6df67-237">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-238">Search-Flags</span></span>           | <span data-ttu-id="6df67-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6df67-239">0x00000000</span></span>                                                                          |
| <span data-ttu-id="6df67-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-240">System-Flags</span></span>           | <span data-ttu-id="6df67-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6df67-241">0x00000010</span></span>                                                                          |
| <span data-ttu-id="6df67-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6df67-242">Classes used in</span></span>        | [<span data-ttu-id="6df67-243">**RRAS-Administration-Diccionario**</span><span class="sxs-lookup"><span data-stu-id="6df67-243">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6df67-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6df67-244">Windows Server 2012</span></span>



| <span data-ttu-id="6df67-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="6df67-245">Entry</span></span> | <span data-ttu-id="6df67-246">Value</span><span class="sxs-lookup"><span data-stu-id="6df67-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6df67-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6df67-247">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6df67-248">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="6df67-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="6df67-249">System-Only</span></span>            | <span data-ttu-id="6df67-250">False</span><span class="sxs-lookup"><span data-stu-id="6df67-250">False</span></span>                                                                               |
| <span data-ttu-id="6df67-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6df67-251">Is-Single-Valued</span></span>       | <span data-ttu-id="6df67-252">False</span><span class="sxs-lookup"><span data-stu-id="6df67-252">False</span></span>                                                                               |
| <span data-ttu-id="6df67-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6df67-253">Is Indexed</span></span>             | <span data-ttu-id="6df67-254">False</span><span class="sxs-lookup"><span data-stu-id="6df67-254">False</span></span>                                                                               |
| <span data-ttu-id="6df67-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6df67-255">In Global Catalog</span></span>      | <span data-ttu-id="6df67-256">False</span><span class="sxs-lookup"><span data-stu-id="6df67-256">False</span></span>                                                                               |
| <span data-ttu-id="6df67-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6df67-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="6df67-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6df67-258">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="6df67-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6df67-259">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6df67-260">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="6df67-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-261">Search-Flags</span></span>           | <span data-ttu-id="6df67-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6df67-262">0x00000000</span></span>                                                                          |
| <span data-ttu-id="6df67-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6df67-263">System-Flags</span></span>           | <span data-ttu-id="6df67-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6df67-264">0x00000010</span></span>                                                                          |
| <span data-ttu-id="6df67-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6df67-265">Classes used in</span></span>        | [<span data-ttu-id="6df67-266">**RRAS-Administration-Diccionario**</span><span class="sxs-lookup"><span data-stu-id="6df67-266">**RRAS-Administration-Dictionary**</span></span>](c-rrasadministrationdictionary.md)<br/> |



 

 






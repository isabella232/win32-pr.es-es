---
title: atributo MS-DS-DnsRootAlias
description: Se utiliza para almacenar el alias del dominio.
ms.assetid: 36b64363-947f-4af9-947f-eefead55bb02
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-DnsRootAlias
- Esquema de AD de atributo msDS-DnsRootAlias
topic_type:
- apiref
api_name:
- ms-DS-DnsRootAlias
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0b20b9316aaa9e68ab1ed907135c5640c1480f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805029"
---
# <a name="ms-ds-dnsrootalias-attribute"></a><span data-ttu-id="a63fa-105">atributo MS-DS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="a63fa-105">ms-DS-DnsRootAlias attribute</span></span>

<span data-ttu-id="a63fa-106">Se utiliza para almacenar el alias del dominio.</span><span class="sxs-lookup"><span data-stu-id="a63fa-106">Used to store the domain alias.</span></span>



| <span data-ttu-id="a63fa-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a63fa-107">Entry</span></span> | <span data-ttu-id="a63fa-108">Value</span><span class="sxs-lookup"><span data-stu-id="a63fa-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a63fa-109">CN</span><span class="sxs-lookup"><span data-stu-id="a63fa-109">CN</span></span>                | <span data-ttu-id="a63fa-110">MS-DS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="a63fa-110">ms-DS-DnsRootAlias</span></span>                          |
| <span data-ttu-id="a63fa-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a63fa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a63fa-112">msDS-DnsRootAlias</span><span class="sxs-lookup"><span data-stu-id="a63fa-112">msDS-DnsRootAlias</span></span>                           |
| <span data-ttu-id="a63fa-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a63fa-113">Size</span></span>              | <span data-ttu-id="a63fa-114">Tamaño máximo 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="a63fa-114">Maximum size 255 bytes.</span></span>                     |
| <span data-ttu-id="a63fa-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a63fa-115">Update Privilege</span></span>  | <span data-ttu-id="a63fa-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a63fa-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="a63fa-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a63fa-117">Update Frequency</span></span>  | <span data-ttu-id="a63fa-118">Solo durante la reestructuración de dominios.</span><span class="sxs-lookup"><span data-stu-id="a63fa-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="a63fa-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a63fa-119">Attribute-Id</span></span>      | <span data-ttu-id="a63fa-120">1.2.840.113556.1.4.1719</span><span class="sxs-lookup"><span data-stu-id="a63fa-120">1.2.840.113556.1.4.1719</span></span>                     |
| <span data-ttu-id="a63fa-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a63fa-121">System-Id-Guid</span></span>    | <span data-ttu-id="a63fa-122">2143acca-eead-4d29-b591-85fa49ce9173</span><span class="sxs-lookup"><span data-stu-id="a63fa-122">2143acca-eead-4d29-b591-85fa49ce9173</span></span>        |
| <span data-ttu-id="a63fa-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a63fa-123">Syntax</span></span>            | [<span data-ttu-id="a63fa-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a63fa-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a63fa-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a63fa-125">Implementations</span></span>

-   [<span data-ttu-id="a63fa-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a63fa-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a63fa-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a63fa-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a63fa-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a63fa-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a63fa-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a63fa-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a63fa-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a63fa-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a63fa-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a63fa-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a63fa-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a63fa-132">Windows Server 2003</span></span>



| <span data-ttu-id="a63fa-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="a63fa-133">Entry</span></span> | <span data-ttu-id="a63fa-134">Value</span><span class="sxs-lookup"><span data-stu-id="a63fa-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a63fa-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a63fa-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a63fa-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a63fa-137">System-Only</span></span>            | <span data-ttu-id="a63fa-138">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-138">False</span></span>                                      |
| <span data-ttu-id="a63fa-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a63fa-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a63fa-140">True</span><span class="sxs-lookup"><span data-stu-id="a63fa-140">True</span></span>                                       |
| <span data-ttu-id="a63fa-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a63fa-141">Is Indexed</span></span>             | <span data-ttu-id="a63fa-142">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-142">False</span></span>                                      |
| <span data-ttu-id="a63fa-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a63fa-143">In Global Catalog</span></span>      | <span data-ttu-id="a63fa-144">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-144">False</span></span>                                      |
| <span data-ttu-id="a63fa-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a63fa-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a63fa-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a63fa-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a63fa-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a63fa-147">Range-Lower</span></span>            | <span data-ttu-id="a63fa-148">0</span><span class="sxs-lookup"><span data-stu-id="a63fa-148">0</span></span>                                          |
| <span data-ttu-id="a63fa-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a63fa-149">Range-Upper</span></span>            | <span data-ttu-id="a63fa-150">255</span><span class="sxs-lookup"><span data-stu-id="a63fa-150">255</span></span>                                        |
| <span data-ttu-id="a63fa-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-151">Search-Flags</span></span>           | <span data-ttu-id="a63fa-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a63fa-152">0x00000000</span></span>                                 |
| <span data-ttu-id="a63fa-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-153">System-Flags</span></span>           | <span data-ttu-id="a63fa-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a63fa-154">0x00000010</span></span>                                 |
| <span data-ttu-id="a63fa-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a63fa-155">Classes used in</span></span>        | [<span data-ttu-id="a63fa-156">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a63fa-156">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a63fa-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="a63fa-157">ADAM</span></span>



| <span data-ttu-id="a63fa-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="a63fa-158">Entry</span></span> | <span data-ttu-id="a63fa-159">Value</span><span class="sxs-lookup"><span data-stu-id="a63fa-159">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a63fa-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a63fa-160">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a63fa-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a63fa-162">System-Only</span></span>            | <span data-ttu-id="a63fa-163">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-163">False</span></span>                                      |
| <span data-ttu-id="a63fa-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a63fa-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a63fa-165">True</span><span class="sxs-lookup"><span data-stu-id="a63fa-165">True</span></span>                                       |
| <span data-ttu-id="a63fa-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a63fa-166">Is Indexed</span></span>             | <span data-ttu-id="a63fa-167">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-167">False</span></span>                                      |
| <span data-ttu-id="a63fa-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a63fa-168">In Global Catalog</span></span>      | <span data-ttu-id="a63fa-169">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-169">False</span></span>                                      |
| <span data-ttu-id="a63fa-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a63fa-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a63fa-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a63fa-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a63fa-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a63fa-172">Range-Lower</span></span>            | <span data-ttu-id="a63fa-173">0</span><span class="sxs-lookup"><span data-stu-id="a63fa-173">0</span></span>                                          |
| <span data-ttu-id="a63fa-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a63fa-174">Range-Upper</span></span>            | <span data-ttu-id="a63fa-175">255</span><span class="sxs-lookup"><span data-stu-id="a63fa-175">255</span></span>                                        |
| <span data-ttu-id="a63fa-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-176">Search-Flags</span></span>           | <span data-ttu-id="a63fa-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a63fa-177">0x00000000</span></span>                                 |
| <span data-ttu-id="a63fa-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-178">System-Flags</span></span>           | <span data-ttu-id="a63fa-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a63fa-179">0x00000010</span></span>                                 |
| <span data-ttu-id="a63fa-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a63fa-180">Classes used in</span></span>        | [<span data-ttu-id="a63fa-181">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a63fa-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a63fa-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a63fa-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a63fa-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="a63fa-183">Entry</span></span> | <span data-ttu-id="a63fa-184">Value</span><span class="sxs-lookup"><span data-stu-id="a63fa-184">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a63fa-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a63fa-185">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a63fa-186">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="a63fa-187">System-Only</span></span>            | <span data-ttu-id="a63fa-188">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-188">False</span></span>                                      |
| <span data-ttu-id="a63fa-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a63fa-189">Is-Single-Valued</span></span>       | <span data-ttu-id="a63fa-190">True</span><span class="sxs-lookup"><span data-stu-id="a63fa-190">True</span></span>                                       |
| <span data-ttu-id="a63fa-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a63fa-191">Is Indexed</span></span>             | <span data-ttu-id="a63fa-192">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-192">False</span></span>                                      |
| <span data-ttu-id="a63fa-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a63fa-193">In Global Catalog</span></span>      | <span data-ttu-id="a63fa-194">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-194">False</span></span>                                      |
| <span data-ttu-id="a63fa-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a63fa-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="a63fa-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a63fa-196">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a63fa-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a63fa-197">Range-Lower</span></span>            | <span data-ttu-id="a63fa-198">0</span><span class="sxs-lookup"><span data-stu-id="a63fa-198">0</span></span>                                          |
| <span data-ttu-id="a63fa-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a63fa-199">Range-Upper</span></span>            | <span data-ttu-id="a63fa-200">255</span><span class="sxs-lookup"><span data-stu-id="a63fa-200">255</span></span>                                        |
| <span data-ttu-id="a63fa-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-201">Search-Flags</span></span>           | <span data-ttu-id="a63fa-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a63fa-202">0x00000000</span></span>                                 |
| <span data-ttu-id="a63fa-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-203">System-Flags</span></span>           | <span data-ttu-id="a63fa-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a63fa-204">0x00000010</span></span>                                 |
| <span data-ttu-id="a63fa-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a63fa-205">Classes used in</span></span>        | [<span data-ttu-id="a63fa-206">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a63fa-206">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a63fa-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a63fa-207">Windows Server 2008</span></span>



| <span data-ttu-id="a63fa-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="a63fa-208">Entry</span></span> | <span data-ttu-id="a63fa-209">Value</span><span class="sxs-lookup"><span data-stu-id="a63fa-209">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a63fa-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a63fa-210">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a63fa-211">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="a63fa-212">System-Only</span></span>            | <span data-ttu-id="a63fa-213">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-213">False</span></span>                                      |
| <span data-ttu-id="a63fa-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a63fa-214">Is-Single-Valued</span></span>       | <span data-ttu-id="a63fa-215">True</span><span class="sxs-lookup"><span data-stu-id="a63fa-215">True</span></span>                                       |
| <span data-ttu-id="a63fa-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a63fa-216">Is Indexed</span></span>             | <span data-ttu-id="a63fa-217">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-217">False</span></span>                                      |
| <span data-ttu-id="a63fa-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a63fa-218">In Global Catalog</span></span>      | <span data-ttu-id="a63fa-219">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-219">False</span></span>                                      |
| <span data-ttu-id="a63fa-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a63fa-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="a63fa-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a63fa-221">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a63fa-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a63fa-222">Range-Lower</span></span>            | <span data-ttu-id="a63fa-223">0</span><span class="sxs-lookup"><span data-stu-id="a63fa-223">0</span></span>                                          |
| <span data-ttu-id="a63fa-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a63fa-224">Range-Upper</span></span>            | <span data-ttu-id="a63fa-225">255</span><span class="sxs-lookup"><span data-stu-id="a63fa-225">255</span></span>                                        |
| <span data-ttu-id="a63fa-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-226">Search-Flags</span></span>           | <span data-ttu-id="a63fa-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a63fa-227">0x00000000</span></span>                                 |
| <span data-ttu-id="a63fa-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-228">System-Flags</span></span>           | <span data-ttu-id="a63fa-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a63fa-229">0x00000010</span></span>                                 |
| <span data-ttu-id="a63fa-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a63fa-230">Classes used in</span></span>        | [<span data-ttu-id="a63fa-231">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a63fa-231">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a63fa-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a63fa-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a63fa-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="a63fa-233">Entry</span></span> | <span data-ttu-id="a63fa-234">Value</span><span class="sxs-lookup"><span data-stu-id="a63fa-234">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a63fa-235">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a63fa-235">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a63fa-236">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="a63fa-237">System-Only</span></span>            | <span data-ttu-id="a63fa-238">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-238">False</span></span>                                      |
| <span data-ttu-id="a63fa-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a63fa-239">Is-Single-Valued</span></span>       | <span data-ttu-id="a63fa-240">True</span><span class="sxs-lookup"><span data-stu-id="a63fa-240">True</span></span>                                       |
| <span data-ttu-id="a63fa-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a63fa-241">Is Indexed</span></span>             | <span data-ttu-id="a63fa-242">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-242">False</span></span>                                      |
| <span data-ttu-id="a63fa-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a63fa-243">In Global Catalog</span></span>      | <span data-ttu-id="a63fa-244">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-244">False</span></span>                                      |
| <span data-ttu-id="a63fa-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a63fa-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="a63fa-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a63fa-246">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a63fa-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a63fa-247">Range-Lower</span></span>            | <span data-ttu-id="a63fa-248">0</span><span class="sxs-lookup"><span data-stu-id="a63fa-248">0</span></span>                                          |
| <span data-ttu-id="a63fa-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a63fa-249">Range-Upper</span></span>            | <span data-ttu-id="a63fa-250">255</span><span class="sxs-lookup"><span data-stu-id="a63fa-250">255</span></span>                                        |
| <span data-ttu-id="a63fa-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-251">Search-Flags</span></span>           | <span data-ttu-id="a63fa-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a63fa-252">0x00000000</span></span>                                 |
| <span data-ttu-id="a63fa-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-253">System-Flags</span></span>           | <span data-ttu-id="a63fa-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a63fa-254">0x00000010</span></span>                                 |
| <span data-ttu-id="a63fa-255">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a63fa-255">Classes used in</span></span>        | [<span data-ttu-id="a63fa-256">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a63fa-256">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a63fa-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a63fa-257">Windows Server 2012</span></span>



| <span data-ttu-id="a63fa-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="a63fa-258">Entry</span></span> | <span data-ttu-id="a63fa-259">Value</span><span class="sxs-lookup"><span data-stu-id="a63fa-259">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="a63fa-260">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a63fa-260">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a63fa-261">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="a63fa-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="a63fa-262">System-Only</span></span>            | <span data-ttu-id="a63fa-263">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-263">False</span></span>                                      |
| <span data-ttu-id="a63fa-264">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a63fa-264">Is-Single-Valued</span></span>       | <span data-ttu-id="a63fa-265">True</span><span class="sxs-lookup"><span data-stu-id="a63fa-265">True</span></span>                                       |
| <span data-ttu-id="a63fa-266">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a63fa-266">Is Indexed</span></span>             | <span data-ttu-id="a63fa-267">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-267">False</span></span>                                      |
| <span data-ttu-id="a63fa-268">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a63fa-268">In Global Catalog</span></span>      | <span data-ttu-id="a63fa-269">False</span><span class="sxs-lookup"><span data-stu-id="a63fa-269">False</span></span>                                      |
| <span data-ttu-id="a63fa-270">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a63fa-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="a63fa-271">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a63fa-271">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="a63fa-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a63fa-272">Range-Lower</span></span>            | <span data-ttu-id="a63fa-273">0</span><span class="sxs-lookup"><span data-stu-id="a63fa-273">0</span></span>                                          |
| <span data-ttu-id="a63fa-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a63fa-274">Range-Upper</span></span>            | <span data-ttu-id="a63fa-275">255</span><span class="sxs-lookup"><span data-stu-id="a63fa-275">255</span></span>                                        |
| <span data-ttu-id="a63fa-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-276">Search-Flags</span></span>           | <span data-ttu-id="a63fa-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a63fa-277">0x00000000</span></span>                                 |
| <span data-ttu-id="a63fa-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a63fa-278">System-Flags</span></span>           | <span data-ttu-id="a63fa-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a63fa-279">0x00000010</span></span>                                 |
| <span data-ttu-id="a63fa-280">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a63fa-280">Classes used in</span></span>        | [<span data-ttu-id="a63fa-281">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="a63fa-281">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 






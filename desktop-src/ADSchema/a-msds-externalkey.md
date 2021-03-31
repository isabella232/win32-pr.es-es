---
title: atributo MS-DS-external-Key
description: Una cadena que identifica un objeto en un almacén externo, como un registro en una base de datos.
ms.assetid: aa5b02eb-f872-4184-9508-fe3d4180c680
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de clave externa de MS-DS-external
- Esquema de AD de atributo msDS-ExternalKey
topic_type:
- apiref
api_name:
- ms-DS-External-Key
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aeaaf506495dd2feffe7bdb6d76ea702b84ff00
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805023"
---
# <a name="ms-ds-external-key-attribute"></a><span data-ttu-id="96855-105">atributo MS-DS-external-Key</span><span class="sxs-lookup"><span data-stu-id="96855-105">ms-DS-External-Key attribute</span></span>

<span data-ttu-id="96855-106">Una cadena que identifica un objeto en un almacén externo, como un registro en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="96855-106">A string that identifies an object in an external store, such as a record in a database.</span></span>



| <span data-ttu-id="96855-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="96855-107">Entry</span></span> | <span data-ttu-id="96855-108">Value</span><span class="sxs-lookup"><span data-stu-id="96855-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="96855-109">CN</span><span class="sxs-lookup"><span data-stu-id="96855-109">CN</span></span>                | <span data-ttu-id="96855-110">MS-DS-external-Key</span><span class="sxs-lookup"><span data-stu-id="96855-110">ms-DS-External-Key</span></span>                          |
| <span data-ttu-id="96855-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="96855-111">Ldap-Display-Name</span></span> | <span data-ttu-id="96855-112">msDS-ExternalKey</span><span class="sxs-lookup"><span data-stu-id="96855-112">msDS-ExternalKey</span></span>                            |
| <span data-ttu-id="96855-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="96855-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="96855-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="96855-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="96855-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="96855-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="96855-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="96855-116">Attribute-Id</span></span>      | <span data-ttu-id="96855-117">1.2.840.113556.1.4.1833</span><span class="sxs-lookup"><span data-stu-id="96855-117">1.2.840.113556.1.4.1833</span></span>                     |
| <span data-ttu-id="96855-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="96855-118">System-Id-Guid</span></span>    | <span data-ttu-id="96855-119">b92fd528-38ac-40d4-818d-0433380837c1</span><span class="sxs-lookup"><span data-stu-id="96855-119">b92fd528-38ac-40d4-818d-0433380837c1</span></span>        |
| <span data-ttu-id="96855-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96855-120">Syntax</span></span>            | [<span data-ttu-id="96855-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="96855-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="96855-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="96855-122">Implementations</span></span>

-   [<span data-ttu-id="96855-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="96855-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="96855-124">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="96855-124">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="96855-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="96855-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="96855-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="96855-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="96855-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="96855-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="96855-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="96855-128">Windows Server 2003</span></span>



| <span data-ttu-id="96855-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="96855-129">Entry</span></span> | <span data-ttu-id="96855-130">Value</span><span class="sxs-lookup"><span data-stu-id="96855-130">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="96855-131">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="96855-131">Link-Id</span></span>                | \-           |
| <span data-ttu-id="96855-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96855-132">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="96855-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="96855-133">System-Only</span></span>            | <span data-ttu-id="96855-134">False</span><span class="sxs-lookup"><span data-stu-id="96855-134">False</span></span>        |
| <span data-ttu-id="96855-135">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="96855-135">Is-Single-Valued</span></span>       | <span data-ttu-id="96855-136">False</span><span class="sxs-lookup"><span data-stu-id="96855-136">False</span></span>        |
| <span data-ttu-id="96855-137">Está indexado</span><span class="sxs-lookup"><span data-stu-id="96855-137">Is Indexed</span></span>             | <span data-ttu-id="96855-138">False</span><span class="sxs-lookup"><span data-stu-id="96855-138">False</span></span>        |
| <span data-ttu-id="96855-139">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="96855-139">In Global Catalog</span></span>      | <span data-ttu-id="96855-140">False</span><span class="sxs-lookup"><span data-stu-id="96855-140">False</span></span>        |
| <span data-ttu-id="96855-141">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="96855-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="96855-142">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96855-142">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="96855-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96855-143">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="96855-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96855-144">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="96855-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-145">Search-Flags</span></span>           | <span data-ttu-id="96855-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-146">0x00000000</span></span>   |
| <span data-ttu-id="96855-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-147">System-Flags</span></span>           | <span data-ttu-id="96855-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-148">0x00000000</span></span>   |
| <span data-ttu-id="96855-149">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="96855-149">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="96855-150">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="96855-150">Windows Server 2003 R2</span></span>



| <span data-ttu-id="96855-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="96855-151">Entry</span></span> | <span data-ttu-id="96855-152">Value</span><span class="sxs-lookup"><span data-stu-id="96855-152">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="96855-153">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="96855-153">Link-Id</span></span>                | \-           |
| <span data-ttu-id="96855-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96855-154">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="96855-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="96855-155">System-Only</span></span>            | <span data-ttu-id="96855-156">False</span><span class="sxs-lookup"><span data-stu-id="96855-156">False</span></span>        |
| <span data-ttu-id="96855-157">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="96855-157">Is-Single-Valued</span></span>       | <span data-ttu-id="96855-158">False</span><span class="sxs-lookup"><span data-stu-id="96855-158">False</span></span>        |
| <span data-ttu-id="96855-159">Está indexado</span><span class="sxs-lookup"><span data-stu-id="96855-159">Is Indexed</span></span>             | <span data-ttu-id="96855-160">False</span><span class="sxs-lookup"><span data-stu-id="96855-160">False</span></span>        |
| <span data-ttu-id="96855-161">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="96855-161">In Global Catalog</span></span>      | <span data-ttu-id="96855-162">False</span><span class="sxs-lookup"><span data-stu-id="96855-162">False</span></span>        |
| <span data-ttu-id="96855-163">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="96855-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="96855-164">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96855-164">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="96855-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96855-165">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="96855-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96855-166">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="96855-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-167">Search-Flags</span></span>           | <span data-ttu-id="96855-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-168">0x00000000</span></span>   |
| <span data-ttu-id="96855-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-169">System-Flags</span></span>           | <span data-ttu-id="96855-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-170">0x00000000</span></span>   |
| <span data-ttu-id="96855-171">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="96855-171">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="96855-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96855-172">Windows Server 2008</span></span>



| <span data-ttu-id="96855-173">Entrada</span><span class="sxs-lookup"><span data-stu-id="96855-173">Entry</span></span> | <span data-ttu-id="96855-174">Value</span><span class="sxs-lookup"><span data-stu-id="96855-174">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="96855-175">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="96855-175">Link-Id</span></span>                | \-           |
| <span data-ttu-id="96855-176">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96855-176">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="96855-177">System-Only</span><span class="sxs-lookup"><span data-stu-id="96855-177">System-Only</span></span>            | <span data-ttu-id="96855-178">False</span><span class="sxs-lookup"><span data-stu-id="96855-178">False</span></span>        |
| <span data-ttu-id="96855-179">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="96855-179">Is-Single-Valued</span></span>       | <span data-ttu-id="96855-180">False</span><span class="sxs-lookup"><span data-stu-id="96855-180">False</span></span>        |
| <span data-ttu-id="96855-181">Está indexado</span><span class="sxs-lookup"><span data-stu-id="96855-181">Is Indexed</span></span>             | <span data-ttu-id="96855-182">False</span><span class="sxs-lookup"><span data-stu-id="96855-182">False</span></span>        |
| <span data-ttu-id="96855-183">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="96855-183">In Global Catalog</span></span>      | <span data-ttu-id="96855-184">False</span><span class="sxs-lookup"><span data-stu-id="96855-184">False</span></span>        |
| <span data-ttu-id="96855-185">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="96855-185">NT-Security-Descriptor</span></span> | <span data-ttu-id="96855-186">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96855-186">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="96855-187">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96855-187">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="96855-188">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96855-188">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="96855-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-189">Search-Flags</span></span>           | <span data-ttu-id="96855-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-190">0x00000000</span></span>   |
| <span data-ttu-id="96855-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-191">System-Flags</span></span>           | <span data-ttu-id="96855-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-192">0x00000000</span></span>   |
| <span data-ttu-id="96855-193">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="96855-193">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="96855-194">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96855-194">Windows Server 2008 R2</span></span>



| <span data-ttu-id="96855-195">Entrada</span><span class="sxs-lookup"><span data-stu-id="96855-195">Entry</span></span> | <span data-ttu-id="96855-196">Value</span><span class="sxs-lookup"><span data-stu-id="96855-196">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="96855-197">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="96855-197">Link-Id</span></span>                | \-           |
| <span data-ttu-id="96855-198">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96855-198">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="96855-199">System-Only</span><span class="sxs-lookup"><span data-stu-id="96855-199">System-Only</span></span>            | <span data-ttu-id="96855-200">False</span><span class="sxs-lookup"><span data-stu-id="96855-200">False</span></span>        |
| <span data-ttu-id="96855-201">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="96855-201">Is-Single-Valued</span></span>       | <span data-ttu-id="96855-202">False</span><span class="sxs-lookup"><span data-stu-id="96855-202">False</span></span>        |
| <span data-ttu-id="96855-203">Está indexado</span><span class="sxs-lookup"><span data-stu-id="96855-203">Is Indexed</span></span>             | <span data-ttu-id="96855-204">False</span><span class="sxs-lookup"><span data-stu-id="96855-204">False</span></span>        |
| <span data-ttu-id="96855-205">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="96855-205">In Global Catalog</span></span>      | <span data-ttu-id="96855-206">False</span><span class="sxs-lookup"><span data-stu-id="96855-206">False</span></span>        |
| <span data-ttu-id="96855-207">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="96855-207">NT-Security-Descriptor</span></span> | <span data-ttu-id="96855-208">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96855-208">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="96855-209">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96855-209">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="96855-210">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96855-210">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="96855-211">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-211">Search-Flags</span></span>           | <span data-ttu-id="96855-212">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-212">0x00000000</span></span>   |
| <span data-ttu-id="96855-213">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-213">System-Flags</span></span>           | <span data-ttu-id="96855-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-214">0x00000000</span></span>   |
| <span data-ttu-id="96855-215">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="96855-215">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="96855-216">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96855-216">Windows Server 2012</span></span>



| <span data-ttu-id="96855-217">Entrada</span><span class="sxs-lookup"><span data-stu-id="96855-217">Entry</span></span> | <span data-ttu-id="96855-218">Value</span><span class="sxs-lookup"><span data-stu-id="96855-218">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="96855-219">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="96855-219">Link-Id</span></span>                | \-           |
| <span data-ttu-id="96855-220">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="96855-220">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="96855-221">System-Only</span><span class="sxs-lookup"><span data-stu-id="96855-221">System-Only</span></span>            | <span data-ttu-id="96855-222">False</span><span class="sxs-lookup"><span data-stu-id="96855-222">False</span></span>        |
| <span data-ttu-id="96855-223">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="96855-223">Is-Single-Valued</span></span>       | <span data-ttu-id="96855-224">False</span><span class="sxs-lookup"><span data-stu-id="96855-224">False</span></span>        |
| <span data-ttu-id="96855-225">Está indexado</span><span class="sxs-lookup"><span data-stu-id="96855-225">Is Indexed</span></span>             | <span data-ttu-id="96855-226">False</span><span class="sxs-lookup"><span data-stu-id="96855-226">False</span></span>        |
| <span data-ttu-id="96855-227">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="96855-227">In Global Catalog</span></span>      | <span data-ttu-id="96855-228">False</span><span class="sxs-lookup"><span data-stu-id="96855-228">False</span></span>        |
| <span data-ttu-id="96855-229">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="96855-229">NT-Security-Descriptor</span></span> | <span data-ttu-id="96855-230">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="96855-230">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="96855-231">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="96855-231">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="96855-232">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="96855-232">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="96855-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-233">Search-Flags</span></span>           | <span data-ttu-id="96855-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-234">0x00000000</span></span>   |
| <span data-ttu-id="96855-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="96855-235">System-Flags</span></span>           | <span data-ttu-id="96855-236">0x00000000</span><span class="sxs-lookup"><span data-stu-id="96855-236">0x00000000</span></span>   |
| <span data-ttu-id="96855-237">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="96855-237">Classes used in</span></span>        | \-           |



 

 





---
title: Flat-Name atributo)
description: En el caso de los dominios de Windows NT, el nombre plano es el nombre de NetBIOS. Para vínculos con un valor de no \ 8211; Dominios de Windows NT, el nombre plano es el nombre de identificación del dominio o es NULL.
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Flat-Name
- flatName esquema de AD de atributos
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373ee0736c051932fdb6dd20701f0c5ec353ad3b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493594"
---
# <a name="flat-name-attribute"></a><span data-ttu-id="924f6-106">Flat-Name atributo)</span><span class="sxs-lookup"><span data-stu-id="924f6-106">Flat-Name attribute</span></span>

<span data-ttu-id="924f6-107">En el caso de los dominios de Windows NT, el nombre plano es el nombre de NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="924f6-107">For Windows NT domains, the flat name is the NetBIOS name.</span></span> <span data-ttu-id="924f6-108">En el caso de los vínculos con dominios que no son de Windows NT, el nombre plano es el nombre de identificación del dominio o es **null**.</span><span class="sxs-lookup"><span data-stu-id="924f6-108">For links with non Windows NT domains, the flat name is the identifying name of that domain, or it is **NULL**.</span></span>



| <span data-ttu-id="924f6-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="924f6-109">Entry</span></span> | <span data-ttu-id="924f6-110">Value</span><span class="sxs-lookup"><span data-stu-id="924f6-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="924f6-111">CN</span><span class="sxs-lookup"><span data-stu-id="924f6-111">CN</span></span>                | <span data-ttu-id="924f6-112">Flat-Name</span><span class="sxs-lookup"><span data-stu-id="924f6-112">Flat-Name</span></span>                                   |
| <span data-ttu-id="924f6-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="924f6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="924f6-114">flatName</span><span class="sxs-lookup"><span data-stu-id="924f6-114">flatName</span></span>                                    |
| <span data-ttu-id="924f6-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="924f6-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="924f6-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="924f6-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="924f6-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="924f6-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="924f6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="924f6-118">Attribute-Id</span></span>      | <span data-ttu-id="924f6-119">1.2.840.113556.1.4.511</span><span class="sxs-lookup"><span data-stu-id="924f6-119">1.2.840.113556.1.4.511</span></span>                      |
| <span data-ttu-id="924f6-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="924f6-120">System-Id-Guid</span></span>    | <span data-ttu-id="924f6-121">b7b13117-b82e-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="924f6-121">b7b13117-b82e-11d0-afee-0000f80367c1</span></span>        |
| <span data-ttu-id="924f6-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="924f6-122">Syntax</span></span>            | [<span data-ttu-id="924f6-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="924f6-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="924f6-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="924f6-124">Implementations</span></span>

-   [<span data-ttu-id="924f6-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="924f6-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="924f6-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="924f6-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="924f6-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="924f6-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="924f6-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="924f6-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="924f6-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="924f6-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="924f6-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="924f6-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="924f6-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="924f6-131">Windows 2000 Server</span></span>



| <span data-ttu-id="924f6-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="924f6-132">Entry</span></span> | <span data-ttu-id="924f6-133">Value</span><span class="sxs-lookup"><span data-stu-id="924f6-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="924f6-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="924f6-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="924f6-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="924f6-136">System-Only</span></span>            | <span data-ttu-id="924f6-137">False</span><span class="sxs-lookup"><span data-stu-id="924f6-137">False</span></span>                                                |
| <span data-ttu-id="924f6-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="924f6-138">Is-Single-Valued</span></span>       | <span data-ttu-id="924f6-139">True</span><span class="sxs-lookup"><span data-stu-id="924f6-139">True</span></span>                                                 |
| <span data-ttu-id="924f6-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="924f6-140">Is Indexed</span></span>             | <span data-ttu-id="924f6-141">True</span><span class="sxs-lookup"><span data-stu-id="924f6-141">True</span></span>                                                 |
| <span data-ttu-id="924f6-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="924f6-142">In Global Catalog</span></span>      | <span data-ttu-id="924f6-143">False</span><span class="sxs-lookup"><span data-stu-id="924f6-143">False</span></span>                                                |
| <span data-ttu-id="924f6-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="924f6-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="924f6-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="924f6-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="924f6-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="924f6-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="924f6-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-148">Search-Flags</span></span>           | <span data-ttu-id="924f6-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="924f6-149">0x00000001</span></span>                                           |
| <span data-ttu-id="924f6-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-150">System-Flags</span></span>           | <span data-ttu-id="924f6-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="924f6-151">0x00000010</span></span>                                           |
| <span data-ttu-id="924f6-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="924f6-152">Classes used in</span></span>        | [<span data-ttu-id="924f6-153">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="924f6-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="924f6-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="924f6-154">Windows Server 2003</span></span>



| <span data-ttu-id="924f6-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="924f6-155">Entry</span></span> | <span data-ttu-id="924f6-156">Value</span><span class="sxs-lookup"><span data-stu-id="924f6-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="924f6-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="924f6-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="924f6-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="924f6-159">System-Only</span></span>            | <span data-ttu-id="924f6-160">False</span><span class="sxs-lookup"><span data-stu-id="924f6-160">False</span></span>                                                |
| <span data-ttu-id="924f6-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="924f6-161">Is-Single-Valued</span></span>       | <span data-ttu-id="924f6-162">True</span><span class="sxs-lookup"><span data-stu-id="924f6-162">True</span></span>                                                 |
| <span data-ttu-id="924f6-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="924f6-163">Is Indexed</span></span>             | <span data-ttu-id="924f6-164">True</span><span class="sxs-lookup"><span data-stu-id="924f6-164">True</span></span>                                                 |
| <span data-ttu-id="924f6-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="924f6-165">In Global Catalog</span></span>      | <span data-ttu-id="924f6-166">False</span><span class="sxs-lookup"><span data-stu-id="924f6-166">False</span></span>                                                |
| <span data-ttu-id="924f6-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="924f6-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="924f6-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="924f6-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="924f6-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="924f6-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="924f6-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-171">Search-Flags</span></span>           | <span data-ttu-id="924f6-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="924f6-172">0x00000001</span></span>                                           |
| <span data-ttu-id="924f6-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-173">System-Flags</span></span>           | <span data-ttu-id="924f6-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="924f6-174">0x00000010</span></span>                                           |
| <span data-ttu-id="924f6-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="924f6-175">Classes used in</span></span>        | [<span data-ttu-id="924f6-176">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="924f6-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="924f6-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="924f6-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="924f6-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="924f6-178">Entry</span></span> | <span data-ttu-id="924f6-179">Value</span><span class="sxs-lookup"><span data-stu-id="924f6-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="924f6-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="924f6-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="924f6-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="924f6-182">System-Only</span></span>            | <span data-ttu-id="924f6-183">False</span><span class="sxs-lookup"><span data-stu-id="924f6-183">False</span></span>                                                |
| <span data-ttu-id="924f6-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="924f6-184">Is-Single-Valued</span></span>       | <span data-ttu-id="924f6-185">True</span><span class="sxs-lookup"><span data-stu-id="924f6-185">True</span></span>                                                 |
| <span data-ttu-id="924f6-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="924f6-186">Is Indexed</span></span>             | <span data-ttu-id="924f6-187">True</span><span class="sxs-lookup"><span data-stu-id="924f6-187">True</span></span>                                                 |
| <span data-ttu-id="924f6-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="924f6-188">In Global Catalog</span></span>      | <span data-ttu-id="924f6-189">False</span><span class="sxs-lookup"><span data-stu-id="924f6-189">False</span></span>                                                |
| <span data-ttu-id="924f6-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="924f6-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="924f6-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="924f6-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="924f6-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="924f6-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="924f6-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-194">Search-Flags</span></span>           | <span data-ttu-id="924f6-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="924f6-195">0x00000001</span></span>                                           |
| <span data-ttu-id="924f6-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-196">System-Flags</span></span>           | <span data-ttu-id="924f6-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="924f6-197">0x00000010</span></span>                                           |
| <span data-ttu-id="924f6-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="924f6-198">Classes used in</span></span>        | [<span data-ttu-id="924f6-199">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="924f6-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="924f6-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="924f6-200">Windows Server 2008</span></span>



| <span data-ttu-id="924f6-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="924f6-201">Entry</span></span> | <span data-ttu-id="924f6-202">Value</span><span class="sxs-lookup"><span data-stu-id="924f6-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="924f6-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="924f6-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="924f6-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="924f6-205">System-Only</span></span>            | <span data-ttu-id="924f6-206">False</span><span class="sxs-lookup"><span data-stu-id="924f6-206">False</span></span>                                                |
| <span data-ttu-id="924f6-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="924f6-207">Is-Single-Valued</span></span>       | <span data-ttu-id="924f6-208">True</span><span class="sxs-lookup"><span data-stu-id="924f6-208">True</span></span>                                                 |
| <span data-ttu-id="924f6-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="924f6-209">Is Indexed</span></span>             | <span data-ttu-id="924f6-210">True</span><span class="sxs-lookup"><span data-stu-id="924f6-210">True</span></span>                                                 |
| <span data-ttu-id="924f6-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="924f6-211">In Global Catalog</span></span>      | <span data-ttu-id="924f6-212">False</span><span class="sxs-lookup"><span data-stu-id="924f6-212">False</span></span>                                                |
| <span data-ttu-id="924f6-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="924f6-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="924f6-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="924f6-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="924f6-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="924f6-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="924f6-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-217">Search-Flags</span></span>           | <span data-ttu-id="924f6-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="924f6-218">0x00000001</span></span>                                           |
| <span data-ttu-id="924f6-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-219">System-Flags</span></span>           | <span data-ttu-id="924f6-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="924f6-220">0x00000010</span></span>                                           |
| <span data-ttu-id="924f6-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="924f6-221">Classes used in</span></span>        | [<span data-ttu-id="924f6-222">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="924f6-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="924f6-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="924f6-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="924f6-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="924f6-224">Entry</span></span> | <span data-ttu-id="924f6-225">Value</span><span class="sxs-lookup"><span data-stu-id="924f6-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="924f6-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="924f6-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="924f6-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="924f6-228">System-Only</span></span>            | <span data-ttu-id="924f6-229">False</span><span class="sxs-lookup"><span data-stu-id="924f6-229">False</span></span>                                                |
| <span data-ttu-id="924f6-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="924f6-230">Is-Single-Valued</span></span>       | <span data-ttu-id="924f6-231">True</span><span class="sxs-lookup"><span data-stu-id="924f6-231">True</span></span>                                                 |
| <span data-ttu-id="924f6-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="924f6-232">Is Indexed</span></span>             | <span data-ttu-id="924f6-233">True</span><span class="sxs-lookup"><span data-stu-id="924f6-233">True</span></span>                                                 |
| <span data-ttu-id="924f6-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="924f6-234">In Global Catalog</span></span>      | <span data-ttu-id="924f6-235">False</span><span class="sxs-lookup"><span data-stu-id="924f6-235">False</span></span>                                                |
| <span data-ttu-id="924f6-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="924f6-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="924f6-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="924f6-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="924f6-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="924f6-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="924f6-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-240">Search-Flags</span></span>           | <span data-ttu-id="924f6-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="924f6-241">0x00000001</span></span>                                           |
| <span data-ttu-id="924f6-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-242">System-Flags</span></span>           | <span data-ttu-id="924f6-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="924f6-243">0x00000010</span></span>                                           |
| <span data-ttu-id="924f6-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="924f6-244">Classes used in</span></span>        | [<span data-ttu-id="924f6-245">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="924f6-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="924f6-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="924f6-246">Windows Server 2012</span></span>



| <span data-ttu-id="924f6-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="924f6-247">Entry</span></span> | <span data-ttu-id="924f6-248">Value</span><span class="sxs-lookup"><span data-stu-id="924f6-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="924f6-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="924f6-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="924f6-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="924f6-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="924f6-251">System-Only</span></span>            | <span data-ttu-id="924f6-252">False</span><span class="sxs-lookup"><span data-stu-id="924f6-252">False</span></span>                                                |
| <span data-ttu-id="924f6-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="924f6-253">Is-Single-Valued</span></span>       | <span data-ttu-id="924f6-254">True</span><span class="sxs-lookup"><span data-stu-id="924f6-254">True</span></span>                                                 |
| <span data-ttu-id="924f6-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="924f6-255">Is Indexed</span></span>             | <span data-ttu-id="924f6-256">True</span><span class="sxs-lookup"><span data-stu-id="924f6-256">True</span></span>                                                 |
| <span data-ttu-id="924f6-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="924f6-257">In Global Catalog</span></span>      | <span data-ttu-id="924f6-258">False</span><span class="sxs-lookup"><span data-stu-id="924f6-258">False</span></span>                                                |
| <span data-ttu-id="924f6-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="924f6-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="924f6-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="924f6-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="924f6-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="924f6-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="924f6-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="924f6-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-263">Search-Flags</span></span>           | <span data-ttu-id="924f6-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="924f6-264">0x00000001</span></span>                                           |
| <span data-ttu-id="924f6-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="924f6-265">System-Flags</span></span>           | <span data-ttu-id="924f6-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="924f6-266">0x00000010</span></span>                                           |
| <span data-ttu-id="924f6-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="924f6-267">Classes used in</span></span>        | [<span data-ttu-id="924f6-268">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="924f6-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






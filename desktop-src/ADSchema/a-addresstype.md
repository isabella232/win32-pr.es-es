---
title: Address-Type atributo)
description: Cadena de caracteres que describe el formato de la dirección del usuario. Los tipos de direcciones se asignan a los formatos de dirección. Es decir, al examinar el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección que sea adecuada para el destinatario.
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Address-Type
- Esquema de AD del atributo addressType
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece3b396d619272c616ff1a959d01efb64ccd46
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659232"
---
# <a name="address-type-attribute"></a><span data-ttu-id="29a66-107">Address-Type atributo)</span><span class="sxs-lookup"><span data-stu-id="29a66-107">Address-Type attribute</span></span>

<span data-ttu-id="29a66-108">Cadena de caracteres que describe el formato de la dirección del usuario.</span><span class="sxs-lookup"><span data-stu-id="29a66-108">A character string that describes the format of the user's address.</span></span> <span data-ttu-id="29a66-109">Los tipos de direcciones se asignan a los formatos de dirección.</span><span class="sxs-lookup"><span data-stu-id="29a66-109">Address types map to address formats.</span></span> <span data-ttu-id="29a66-110">Es decir, al examinar el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección que sea adecuada para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="29a66-110">That is, by looking at a recipient's address type, client applications can determine how to format an address that is appropriate for the recipient.</span></span>



| <span data-ttu-id="29a66-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a66-111">Entry</span></span> | <span data-ttu-id="29a66-112">Value</span><span class="sxs-lookup"><span data-stu-id="29a66-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29a66-113">CN</span><span class="sxs-lookup"><span data-stu-id="29a66-113">CN</span></span>                | <span data-ttu-id="29a66-114">Address-Type</span><span class="sxs-lookup"><span data-stu-id="29a66-114">Address-Type</span></span>                                                                                                              |
| <span data-ttu-id="29a66-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="29a66-115">Ldap-Display-Name</span></span> | <span data-ttu-id="29a66-116">addressType</span><span class="sxs-lookup"><span data-stu-id="29a66-116">addressType</span></span>                                                                                                               |
| <span data-ttu-id="29a66-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="29a66-117">Size</span></span>              | <span data-ttu-id="29a66-118">Tipos de direcciones: 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN, PROFs, SMTP, SNADS, télex, X400, X500</span><span class="sxs-lookup"><span data-stu-id="29a66-118">Address types: 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN,PROFS,SMTP, SNADS, TELEX, X400, X500</span></span> |
| <span data-ttu-id="29a66-119">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="29a66-119">Update Privilege</span></span>  | <span data-ttu-id="29a66-120">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="29a66-120">This value is set by the system.</span></span>                                                                                          |
| <span data-ttu-id="29a66-121">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="29a66-121">Update Frequency</span></span>  | <span data-ttu-id="29a66-122">Se establece cuando se crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="29a66-122">Set when the object is created.</span></span>                                                                                           |
| <span data-ttu-id="29a66-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29a66-123">Attribute-Id</span></span>      | <span data-ttu-id="29a66-124">1.2.840.113556.1.2.350</span><span class="sxs-lookup"><span data-stu-id="29a66-124">1.2.840.113556.1.2.350</span></span>                                                                                                    |
| <span data-ttu-id="29a66-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="29a66-125">System-Id-Guid</span></span>    | <span data-ttu-id="29a66-126">5fd42464-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="29a66-126">5fd42464-1262-11d0-a060-00aa006c33ed</span></span>                                                                                      |
| <span data-ttu-id="29a66-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29a66-127">Syntax</span></span>            | [<span data-ttu-id="29a66-128">**String(Teletex)**</span><span class="sxs-lookup"><span data-stu-id="29a66-128">**String(Teletex)**</span></span>](s-string-teletex.md)                                                                               |



## <a name="implementations"></a><span data-ttu-id="29a66-129">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="29a66-129">Implementations</span></span>

-   [<span data-ttu-id="29a66-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="29a66-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="29a66-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29a66-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29a66-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29a66-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29a66-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29a66-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29a66-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29a66-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29a66-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29a66-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="29a66-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29a66-136">Windows 2000 Server</span></span>



| <span data-ttu-id="29a66-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a66-137">Entry</span></span> | <span data-ttu-id="29a66-138">Value</span><span class="sxs-lookup"><span data-stu-id="29a66-138">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="29a66-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29a66-139">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="29a66-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a66-140">MAPI-Id</span></span>                | <span data-ttu-id="29a66-141">0x8048</span><span class="sxs-lookup"><span data-stu-id="29a66-141">0x8048</span></span>                                                   |
| <span data-ttu-id="29a66-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a66-142">System-Only</span></span>            | <span data-ttu-id="29a66-143">False</span><span class="sxs-lookup"><span data-stu-id="29a66-143">False</span></span>                                                    |
| <span data-ttu-id="29a66-144">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29a66-144">Is-Single-Valued</span></span>       | <span data-ttu-id="29a66-145">True</span><span class="sxs-lookup"><span data-stu-id="29a66-145">True</span></span>                                                     |
| <span data-ttu-id="29a66-146">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29a66-146">Is Indexed</span></span>             | <span data-ttu-id="29a66-147">False</span><span class="sxs-lookup"><span data-stu-id="29a66-147">False</span></span>                                                    |
| <span data-ttu-id="29a66-148">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a66-148">In Global Catalog</span></span>      | <span data-ttu-id="29a66-149">False</span><span class="sxs-lookup"><span data-stu-id="29a66-149">False</span></span>                                                    |
| <span data-ttu-id="29a66-150">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29a66-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a66-151">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29a66-151">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="29a66-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a66-152">Range-Lower</span></span>            | <span data-ttu-id="29a66-153">1</span><span class="sxs-lookup"><span data-stu-id="29a66-153">1</span></span>                                                        |
| <span data-ttu-id="29a66-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a66-154">Range-Upper</span></span>            | <span data-ttu-id="29a66-155">32</span><span class="sxs-lookup"><span data-stu-id="29a66-155">32</span></span>                                                       |
| <span data-ttu-id="29a66-156">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-156">Search-Flags</span></span>           | <span data-ttu-id="29a66-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a66-157">0x00000000</span></span>                                               |
| <span data-ttu-id="29a66-158">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-158">System-Flags</span></span>           | <span data-ttu-id="29a66-159">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a66-159">0x00000010</span></span>                                               |
| <span data-ttu-id="29a66-160">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29a66-160">Classes used in</span></span>        | [<span data-ttu-id="29a66-161">**Dirección: plantilla**</span><span class="sxs-lookup"><span data-stu-id="29a66-161">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="29a66-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29a66-162">Windows Server 2003</span></span>



| <span data-ttu-id="29a66-163">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a66-163">Entry</span></span> | <span data-ttu-id="29a66-164">Value</span><span class="sxs-lookup"><span data-stu-id="29a66-164">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="29a66-165">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29a66-165">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="29a66-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a66-166">MAPI-Id</span></span>                | <span data-ttu-id="29a66-167">0x8048</span><span class="sxs-lookup"><span data-stu-id="29a66-167">0x8048</span></span>                                                   |
| <span data-ttu-id="29a66-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a66-168">System-Only</span></span>            | <span data-ttu-id="29a66-169">False</span><span class="sxs-lookup"><span data-stu-id="29a66-169">False</span></span>                                                    |
| <span data-ttu-id="29a66-170">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29a66-170">Is-Single-Valued</span></span>       | <span data-ttu-id="29a66-171">True</span><span class="sxs-lookup"><span data-stu-id="29a66-171">True</span></span>                                                     |
| <span data-ttu-id="29a66-172">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29a66-172">Is Indexed</span></span>             | <span data-ttu-id="29a66-173">False</span><span class="sxs-lookup"><span data-stu-id="29a66-173">False</span></span>                                                    |
| <span data-ttu-id="29a66-174">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a66-174">In Global Catalog</span></span>      | <span data-ttu-id="29a66-175">False</span><span class="sxs-lookup"><span data-stu-id="29a66-175">False</span></span>                                                    |
| <span data-ttu-id="29a66-176">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29a66-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a66-177">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29a66-177">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="29a66-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a66-178">Range-Lower</span></span>            | <span data-ttu-id="29a66-179">1</span><span class="sxs-lookup"><span data-stu-id="29a66-179">1</span></span>                                                        |
| <span data-ttu-id="29a66-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a66-180">Range-Upper</span></span>            | <span data-ttu-id="29a66-181">32</span><span class="sxs-lookup"><span data-stu-id="29a66-181">32</span></span>                                                       |
| <span data-ttu-id="29a66-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-182">Search-Flags</span></span>           | <span data-ttu-id="29a66-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a66-183">0x00000000</span></span>                                               |
| <span data-ttu-id="29a66-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-184">System-Flags</span></span>           | <span data-ttu-id="29a66-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a66-185">0x00000010</span></span>                                               |
| <span data-ttu-id="29a66-186">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29a66-186">Classes used in</span></span>        | [<span data-ttu-id="29a66-187">**Dirección: plantilla**</span><span class="sxs-lookup"><span data-stu-id="29a66-187">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29a66-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29a66-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29a66-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a66-189">Entry</span></span> | <span data-ttu-id="29a66-190">Value</span><span class="sxs-lookup"><span data-stu-id="29a66-190">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="29a66-191">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29a66-191">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="29a66-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a66-192">MAPI-Id</span></span>                | <span data-ttu-id="29a66-193">0x8048</span><span class="sxs-lookup"><span data-stu-id="29a66-193">0x8048</span></span>                                                   |
| <span data-ttu-id="29a66-194">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a66-194">System-Only</span></span>            | <span data-ttu-id="29a66-195">False</span><span class="sxs-lookup"><span data-stu-id="29a66-195">False</span></span>                                                    |
| <span data-ttu-id="29a66-196">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29a66-196">Is-Single-Valued</span></span>       | <span data-ttu-id="29a66-197">True</span><span class="sxs-lookup"><span data-stu-id="29a66-197">True</span></span>                                                     |
| <span data-ttu-id="29a66-198">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29a66-198">Is Indexed</span></span>             | <span data-ttu-id="29a66-199">False</span><span class="sxs-lookup"><span data-stu-id="29a66-199">False</span></span>                                                    |
| <span data-ttu-id="29a66-200">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a66-200">In Global Catalog</span></span>      | <span data-ttu-id="29a66-201">False</span><span class="sxs-lookup"><span data-stu-id="29a66-201">False</span></span>                                                    |
| <span data-ttu-id="29a66-202">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29a66-202">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a66-203">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29a66-203">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="29a66-204">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a66-204">Range-Lower</span></span>            | <span data-ttu-id="29a66-205">1</span><span class="sxs-lookup"><span data-stu-id="29a66-205">1</span></span>                                                        |
| <span data-ttu-id="29a66-206">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a66-206">Range-Upper</span></span>            | <span data-ttu-id="29a66-207">32</span><span class="sxs-lookup"><span data-stu-id="29a66-207">32</span></span>                                                       |
| <span data-ttu-id="29a66-208">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-208">Search-Flags</span></span>           | <span data-ttu-id="29a66-209">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a66-209">0x00000000</span></span>                                               |
| <span data-ttu-id="29a66-210">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-210">System-Flags</span></span>           | <span data-ttu-id="29a66-211">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a66-211">0x00000010</span></span>                                               |
| <span data-ttu-id="29a66-212">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29a66-212">Classes used in</span></span>        | [<span data-ttu-id="29a66-213">**Dirección: plantilla**</span><span class="sxs-lookup"><span data-stu-id="29a66-213">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29a66-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29a66-214">Windows Server 2008</span></span>



| <span data-ttu-id="29a66-215">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a66-215">Entry</span></span> | <span data-ttu-id="29a66-216">Value</span><span class="sxs-lookup"><span data-stu-id="29a66-216">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="29a66-217">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29a66-217">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="29a66-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a66-218">MAPI-Id</span></span>                | <span data-ttu-id="29a66-219">0x8048</span><span class="sxs-lookup"><span data-stu-id="29a66-219">0x8048</span></span>                                                   |
| <span data-ttu-id="29a66-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a66-220">System-Only</span></span>            | <span data-ttu-id="29a66-221">False</span><span class="sxs-lookup"><span data-stu-id="29a66-221">False</span></span>                                                    |
| <span data-ttu-id="29a66-222">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29a66-222">Is-Single-Valued</span></span>       | <span data-ttu-id="29a66-223">True</span><span class="sxs-lookup"><span data-stu-id="29a66-223">True</span></span>                                                     |
| <span data-ttu-id="29a66-224">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29a66-224">Is Indexed</span></span>             | <span data-ttu-id="29a66-225">False</span><span class="sxs-lookup"><span data-stu-id="29a66-225">False</span></span>                                                    |
| <span data-ttu-id="29a66-226">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a66-226">In Global Catalog</span></span>      | <span data-ttu-id="29a66-227">False</span><span class="sxs-lookup"><span data-stu-id="29a66-227">False</span></span>                                                    |
| <span data-ttu-id="29a66-228">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29a66-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a66-229">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29a66-229">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="29a66-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a66-230">Range-Lower</span></span>            | <span data-ttu-id="29a66-231">1</span><span class="sxs-lookup"><span data-stu-id="29a66-231">1</span></span>                                                        |
| <span data-ttu-id="29a66-232">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a66-232">Range-Upper</span></span>            | <span data-ttu-id="29a66-233">32</span><span class="sxs-lookup"><span data-stu-id="29a66-233">32</span></span>                                                       |
| <span data-ttu-id="29a66-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-234">Search-Flags</span></span>           | <span data-ttu-id="29a66-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a66-235">0x00000000</span></span>                                               |
| <span data-ttu-id="29a66-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-236">System-Flags</span></span>           | <span data-ttu-id="29a66-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a66-237">0x00000010</span></span>                                               |
| <span data-ttu-id="29a66-238">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29a66-238">Classes used in</span></span>        | [<span data-ttu-id="29a66-239">**Dirección: plantilla**</span><span class="sxs-lookup"><span data-stu-id="29a66-239">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29a66-240">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29a66-240">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29a66-241">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a66-241">Entry</span></span> | <span data-ttu-id="29a66-242">Value</span><span class="sxs-lookup"><span data-stu-id="29a66-242">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="29a66-243">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29a66-243">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="29a66-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a66-244">MAPI-Id</span></span>                | <span data-ttu-id="29a66-245">0x8048</span><span class="sxs-lookup"><span data-stu-id="29a66-245">0x8048</span></span>                                                   |
| <span data-ttu-id="29a66-246">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a66-246">System-Only</span></span>            | <span data-ttu-id="29a66-247">False</span><span class="sxs-lookup"><span data-stu-id="29a66-247">False</span></span>                                                    |
| <span data-ttu-id="29a66-248">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29a66-248">Is-Single-Valued</span></span>       | <span data-ttu-id="29a66-249">True</span><span class="sxs-lookup"><span data-stu-id="29a66-249">True</span></span>                                                     |
| <span data-ttu-id="29a66-250">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29a66-250">Is Indexed</span></span>             | <span data-ttu-id="29a66-251">False</span><span class="sxs-lookup"><span data-stu-id="29a66-251">False</span></span>                                                    |
| <span data-ttu-id="29a66-252">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a66-252">In Global Catalog</span></span>      | <span data-ttu-id="29a66-253">False</span><span class="sxs-lookup"><span data-stu-id="29a66-253">False</span></span>                                                    |
| <span data-ttu-id="29a66-254">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29a66-254">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a66-255">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29a66-255">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="29a66-256">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a66-256">Range-Lower</span></span>            | <span data-ttu-id="29a66-257">1</span><span class="sxs-lookup"><span data-stu-id="29a66-257">1</span></span>                                                        |
| <span data-ttu-id="29a66-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a66-258">Range-Upper</span></span>            | <span data-ttu-id="29a66-259">32</span><span class="sxs-lookup"><span data-stu-id="29a66-259">32</span></span>                                                       |
| <span data-ttu-id="29a66-260">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-260">Search-Flags</span></span>           | <span data-ttu-id="29a66-261">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a66-261">0x00000000</span></span>                                               |
| <span data-ttu-id="29a66-262">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-262">System-Flags</span></span>           | <span data-ttu-id="29a66-263">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a66-263">0x00000010</span></span>                                               |
| <span data-ttu-id="29a66-264">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29a66-264">Classes used in</span></span>        | [<span data-ttu-id="29a66-265">**Dirección: plantilla**</span><span class="sxs-lookup"><span data-stu-id="29a66-265">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29a66-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29a66-266">Windows Server 2012</span></span>



| <span data-ttu-id="29a66-267">Entrada</span><span class="sxs-lookup"><span data-stu-id="29a66-267">Entry</span></span> | <span data-ttu-id="29a66-268">Value</span><span class="sxs-lookup"><span data-stu-id="29a66-268">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="29a66-269">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29a66-269">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="29a66-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29a66-270">MAPI-Id</span></span>                | <span data-ttu-id="29a66-271">0x8048</span><span class="sxs-lookup"><span data-stu-id="29a66-271">0x8048</span></span>                                                   |
| <span data-ttu-id="29a66-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="29a66-272">System-Only</span></span>            | <span data-ttu-id="29a66-273">False</span><span class="sxs-lookup"><span data-stu-id="29a66-273">False</span></span>                                                    |
| <span data-ttu-id="29a66-274">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29a66-274">Is-Single-Valued</span></span>       | <span data-ttu-id="29a66-275">True</span><span class="sxs-lookup"><span data-stu-id="29a66-275">True</span></span>                                                     |
| <span data-ttu-id="29a66-276">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29a66-276">Is Indexed</span></span>             | <span data-ttu-id="29a66-277">False</span><span class="sxs-lookup"><span data-stu-id="29a66-277">False</span></span>                                                    |
| <span data-ttu-id="29a66-278">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29a66-278">In Global Catalog</span></span>      | <span data-ttu-id="29a66-279">False</span><span class="sxs-lookup"><span data-stu-id="29a66-279">False</span></span>                                                    |
| <span data-ttu-id="29a66-280">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29a66-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="29a66-281">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29a66-281">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="29a66-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29a66-282">Range-Lower</span></span>            | <span data-ttu-id="29a66-283">1</span><span class="sxs-lookup"><span data-stu-id="29a66-283">1</span></span>                                                        |
| <span data-ttu-id="29a66-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29a66-284">Range-Upper</span></span>            | <span data-ttu-id="29a66-285">32</span><span class="sxs-lookup"><span data-stu-id="29a66-285">32</span></span>                                                       |
| <span data-ttu-id="29a66-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-286">Search-Flags</span></span>           | <span data-ttu-id="29a66-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29a66-287">0x00000000</span></span>                                               |
| <span data-ttu-id="29a66-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29a66-288">System-Flags</span></span>           | <span data-ttu-id="29a66-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29a66-289">0x00000010</span></span>                                               |
| <span data-ttu-id="29a66-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29a66-290">Classes used in</span></span>        | [<span data-ttu-id="29a66-291">**Dirección: plantilla**</span><span class="sxs-lookup"><span data-stu-id="29a66-291">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



 

 






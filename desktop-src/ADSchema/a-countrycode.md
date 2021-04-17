---
title: Country-Code atributo)
description: Especifica el código de país o región para el idioma de elección del usuario. Windows 2000 no usa este valor.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Country-Code
- countryCode atributo AD Schema
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659214"
---
# <a name="country-code-attribute"></a><span data-ttu-id="8733d-106">Country-Code atributo)</span><span class="sxs-lookup"><span data-stu-id="8733d-106">Country-Code attribute</span></span>

<span data-ttu-id="8733d-107">Especifica el código de país o región para el idioma de elección del usuario.</span><span class="sxs-lookup"><span data-stu-id="8733d-107">Specifies the country/region code for the user's language of choice.</span></span> <span data-ttu-id="8733d-108">Windows 2000 no usa este valor.</span><span class="sxs-lookup"><span data-stu-id="8733d-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="8733d-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8733d-109">Entry</span></span> | <span data-ttu-id="8733d-110">Value</span><span class="sxs-lookup"><span data-stu-id="8733d-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="8733d-111">CN</span><span class="sxs-lookup"><span data-stu-id="8733d-111">CN</span></span>                | <span data-ttu-id="8733d-112">Country-Code</span><span class="sxs-lookup"><span data-stu-id="8733d-112">Country-Code</span></span>                            |
| <span data-ttu-id="8733d-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8733d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8733d-114">countryCode</span><span class="sxs-lookup"><span data-stu-id="8733d-114">countryCode</span></span>                             |
| <span data-ttu-id="8733d-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8733d-115">Size</span></span>              | <span data-ttu-id="8733d-116">2 bytes</span><span class="sxs-lookup"><span data-stu-id="8733d-116">2 bytes</span></span>                                 |
| <span data-ttu-id="8733d-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8733d-117">Update Privilege</span></span>  | <span data-ttu-id="8733d-118">Propietario de la cuenta o administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="8733d-118">Account owner or domain administrator</span></span>   |
| <span data-ttu-id="8733d-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8733d-119">Update Frequency</span></span>  | <span data-ttu-id="8733d-120">Cuando cambia el país o la región del usuario.</span><span class="sxs-lookup"><span data-stu-id="8733d-120">When the user's country/region changes.</span></span> |
| <span data-ttu-id="8733d-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8733d-121">Attribute-Id</span></span>      | <span data-ttu-id="8733d-122">1.2.840.113556.1.4.25</span><span class="sxs-lookup"><span data-stu-id="8733d-122">1.2.840.113556.1.4.25</span></span>                   |
| <span data-ttu-id="8733d-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8733d-123">System-Id-Guid</span></span>    | <span data-ttu-id="8733d-124">5fd42471-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="8733d-124">5fd42471-1262-11d0-a060-00aa006c33ed</span></span>    |
| <span data-ttu-id="8733d-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8733d-125">Syntax</span></span>            | [<span data-ttu-id="8733d-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="8733d-126">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="8733d-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8733d-127">Implementations</span></span>

-   [<span data-ttu-id="8733d-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8733d-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8733d-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8733d-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8733d-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8733d-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8733d-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8733d-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8733d-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8733d-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8733d-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8733d-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8733d-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8733d-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8733d-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8733d-135">Windows 2000 Server</span></span>



| <span data-ttu-id="8733d-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="8733d-136">Entry</span></span> | <span data-ttu-id="8733d-137">Value</span><span class="sxs-lookup"><span data-stu-id="8733d-137">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8733d-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8733d-138">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8733d-139">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="8733d-140">System-Only</span></span>            | <span data-ttu-id="8733d-141">False</span><span class="sxs-lookup"><span data-stu-id="8733d-141">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8733d-142">Is-Single-Valued</span></span>       | <span data-ttu-id="8733d-143">True</span><span class="sxs-lookup"><span data-stu-id="8733d-143">True</span></span>                                                                                                                              |
| <span data-ttu-id="8733d-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8733d-144">Is Indexed</span></span>             | <span data-ttu-id="8733d-145">False</span><span class="sxs-lookup"><span data-stu-id="8733d-145">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8733d-146">In Global Catalog</span></span>      | <span data-ttu-id="8733d-147">False</span><span class="sxs-lookup"><span data-stu-id="8733d-147">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8733d-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="8733d-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8733d-149">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="8733d-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8733d-150">Range-Lower</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="8733d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8733d-151">Range-Upper</span></span>            | \-                                                                                                                                |
| <span data-ttu-id="8733d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-152">Search-Flags</span></span>           | <span data-ttu-id="8733d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-153">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-154">System-Flags</span></span>           | <span data-ttu-id="8733d-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-155">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8733d-156">Classes used in</span></span>        | [<span data-ttu-id="8733d-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8733d-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="8733d-158">**Unidad organizativa**</span><span class="sxs-lookup"><span data-stu-id="8733d-158">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8733d-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8733d-159">Windows Server 2003</span></span>



| <span data-ttu-id="8733d-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="8733d-160">Entry</span></span> | <span data-ttu-id="8733d-161">Value</span><span class="sxs-lookup"><span data-stu-id="8733d-161">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8733d-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8733d-162">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8733d-163">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="8733d-164">System-Only</span></span>            | <span data-ttu-id="8733d-165">False</span><span class="sxs-lookup"><span data-stu-id="8733d-165">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8733d-166">Is-Single-Valued</span></span>       | <span data-ttu-id="8733d-167">True</span><span class="sxs-lookup"><span data-stu-id="8733d-167">True</span></span>                                                                                                                              |
| <span data-ttu-id="8733d-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8733d-168">Is Indexed</span></span>             | <span data-ttu-id="8733d-169">False</span><span class="sxs-lookup"><span data-stu-id="8733d-169">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8733d-170">In Global Catalog</span></span>      | <span data-ttu-id="8733d-171">False</span><span class="sxs-lookup"><span data-stu-id="8733d-171">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8733d-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="8733d-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8733d-173">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="8733d-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8733d-174">Range-Lower</span></span>            | <span data-ttu-id="8733d-175">0</span><span class="sxs-lookup"><span data-stu-id="8733d-175">0</span></span>                                                                                                                                 |
| <span data-ttu-id="8733d-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8733d-176">Range-Upper</span></span>            | <span data-ttu-id="8733d-177">65535</span><span class="sxs-lookup"><span data-stu-id="8733d-177">65535</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-178">Search-Flags</span></span>           | <span data-ttu-id="8733d-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-179">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-180">System-Flags</span></span>           | <span data-ttu-id="8733d-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-181">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8733d-182">Classes used in</span></span>        | [<span data-ttu-id="8733d-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8733d-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="8733d-184">**Unidad organizativa**</span><span class="sxs-lookup"><span data-stu-id="8733d-184">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8733d-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="8733d-185">ADAM</span></span>



| <span data-ttu-id="8733d-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="8733d-186">Entry</span></span> | <span data-ttu-id="8733d-187">Value</span><span class="sxs-lookup"><span data-stu-id="8733d-187">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8733d-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8733d-188">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8733d-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8733d-189">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="8733d-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="8733d-190">System-Only</span></span>            | <span data-ttu-id="8733d-191">False</span><span class="sxs-lookup"><span data-stu-id="8733d-191">False</span></span>                                                          |
| <span data-ttu-id="8733d-192">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8733d-192">Is-Single-Valued</span></span>       | <span data-ttu-id="8733d-193">True</span><span class="sxs-lookup"><span data-stu-id="8733d-193">True</span></span>                                                           |
| <span data-ttu-id="8733d-194">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8733d-194">Is Indexed</span></span>             | <span data-ttu-id="8733d-195">False</span><span class="sxs-lookup"><span data-stu-id="8733d-195">False</span></span>                                                          |
| <span data-ttu-id="8733d-196">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8733d-196">In Global Catalog</span></span>      | <span data-ttu-id="8733d-197">False</span><span class="sxs-lookup"><span data-stu-id="8733d-197">False</span></span>                                                          |
| <span data-ttu-id="8733d-198">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8733d-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="8733d-199">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8733d-199">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="8733d-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8733d-200">Range-Lower</span></span>            | <span data-ttu-id="8733d-201">0</span><span class="sxs-lookup"><span data-stu-id="8733d-201">0</span></span>                                                              |
| <span data-ttu-id="8733d-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8733d-202">Range-Upper</span></span>            | <span data-ttu-id="8733d-203">65535</span><span class="sxs-lookup"><span data-stu-id="8733d-203">65535</span></span>                                                          |
| <span data-ttu-id="8733d-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-204">Search-Flags</span></span>           | <span data-ttu-id="8733d-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-205">0x00000010</span></span>                                                     |
| <span data-ttu-id="8733d-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-206">System-Flags</span></span>           | <span data-ttu-id="8733d-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-207">0x00000010</span></span>                                                     |
| <span data-ttu-id="8733d-208">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8733d-208">Classes used in</span></span>        | [<span data-ttu-id="8733d-209">**Unidad organizativa**</span><span class="sxs-lookup"><span data-stu-id="8733d-209">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8733d-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8733d-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8733d-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="8733d-211">Entry</span></span> | <span data-ttu-id="8733d-212">Value</span><span class="sxs-lookup"><span data-stu-id="8733d-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8733d-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8733d-213">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8733d-214">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="8733d-215">System-Only</span></span>            | <span data-ttu-id="8733d-216">False</span><span class="sxs-lookup"><span data-stu-id="8733d-216">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-217">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8733d-217">Is-Single-Valued</span></span>       | <span data-ttu-id="8733d-218">True</span><span class="sxs-lookup"><span data-stu-id="8733d-218">True</span></span>                                                                                                                              |
| <span data-ttu-id="8733d-219">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8733d-219">Is Indexed</span></span>             | <span data-ttu-id="8733d-220">False</span><span class="sxs-lookup"><span data-stu-id="8733d-220">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-221">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8733d-221">In Global Catalog</span></span>      | <span data-ttu-id="8733d-222">False</span><span class="sxs-lookup"><span data-stu-id="8733d-222">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-223">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8733d-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="8733d-224">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8733d-224">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="8733d-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8733d-225">Range-Lower</span></span>            | <span data-ttu-id="8733d-226">0</span><span class="sxs-lookup"><span data-stu-id="8733d-226">0</span></span>                                                                                                                                 |
| <span data-ttu-id="8733d-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8733d-227">Range-Upper</span></span>            | <span data-ttu-id="8733d-228">65535</span><span class="sxs-lookup"><span data-stu-id="8733d-228">65535</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-229">Search-Flags</span></span>           | <span data-ttu-id="8733d-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-230">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-231">System-Flags</span></span>           | <span data-ttu-id="8733d-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-232">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8733d-233">Classes used in</span></span>        | [<span data-ttu-id="8733d-234">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8733d-234">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="8733d-235">**Unidad organizativa**</span><span class="sxs-lookup"><span data-stu-id="8733d-235">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8733d-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8733d-236">Windows Server 2008</span></span>



| <span data-ttu-id="8733d-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="8733d-237">Entry</span></span> | <span data-ttu-id="8733d-238">Value</span><span class="sxs-lookup"><span data-stu-id="8733d-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8733d-239">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8733d-239">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8733d-240">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="8733d-241">System-Only</span></span>            | <span data-ttu-id="8733d-242">False</span><span class="sxs-lookup"><span data-stu-id="8733d-242">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-243">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8733d-243">Is-Single-Valued</span></span>       | <span data-ttu-id="8733d-244">True</span><span class="sxs-lookup"><span data-stu-id="8733d-244">True</span></span>                                                                                                                              |
| <span data-ttu-id="8733d-245">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8733d-245">Is Indexed</span></span>             | <span data-ttu-id="8733d-246">False</span><span class="sxs-lookup"><span data-stu-id="8733d-246">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-247">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8733d-247">In Global Catalog</span></span>      | <span data-ttu-id="8733d-248">False</span><span class="sxs-lookup"><span data-stu-id="8733d-248">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-249">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8733d-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="8733d-250">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8733d-250">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="8733d-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8733d-251">Range-Lower</span></span>            | <span data-ttu-id="8733d-252">0</span><span class="sxs-lookup"><span data-stu-id="8733d-252">0</span></span>                                                                                                                                 |
| <span data-ttu-id="8733d-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8733d-253">Range-Upper</span></span>            | <span data-ttu-id="8733d-254">65535</span><span class="sxs-lookup"><span data-stu-id="8733d-254">65535</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-255">Search-Flags</span></span>           | <span data-ttu-id="8733d-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-256">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-257">System-Flags</span></span>           | <span data-ttu-id="8733d-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-258">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8733d-259">Classes used in</span></span>        | [<span data-ttu-id="8733d-260">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8733d-260">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="8733d-261">**Unidad organizativa**</span><span class="sxs-lookup"><span data-stu-id="8733d-261">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8733d-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8733d-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8733d-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="8733d-263">Entry</span></span> | <span data-ttu-id="8733d-264">Value</span><span class="sxs-lookup"><span data-stu-id="8733d-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8733d-265">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8733d-265">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8733d-266">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="8733d-267">System-Only</span></span>            | <span data-ttu-id="8733d-268">False</span><span class="sxs-lookup"><span data-stu-id="8733d-268">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-269">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8733d-269">Is-Single-Valued</span></span>       | <span data-ttu-id="8733d-270">True</span><span class="sxs-lookup"><span data-stu-id="8733d-270">True</span></span>                                                                                                                              |
| <span data-ttu-id="8733d-271">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8733d-271">Is Indexed</span></span>             | <span data-ttu-id="8733d-272">False</span><span class="sxs-lookup"><span data-stu-id="8733d-272">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-273">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8733d-273">In Global Catalog</span></span>      | <span data-ttu-id="8733d-274">False</span><span class="sxs-lookup"><span data-stu-id="8733d-274">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-275">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8733d-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="8733d-276">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8733d-276">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="8733d-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8733d-277">Range-Lower</span></span>            | <span data-ttu-id="8733d-278">0</span><span class="sxs-lookup"><span data-stu-id="8733d-278">0</span></span>                                                                                                                                 |
| <span data-ttu-id="8733d-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8733d-279">Range-Upper</span></span>            | <span data-ttu-id="8733d-280">65535</span><span class="sxs-lookup"><span data-stu-id="8733d-280">65535</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-281">Search-Flags</span></span>           | <span data-ttu-id="8733d-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-282">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-283">System-Flags</span></span>           | <span data-ttu-id="8733d-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-284">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-285">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8733d-285">Classes used in</span></span>        | [<span data-ttu-id="8733d-286">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8733d-286">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="8733d-287">**Unidad organizativa**</span><span class="sxs-lookup"><span data-stu-id="8733d-287">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8733d-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8733d-288">Windows Server 2012</span></span>



| <span data-ttu-id="8733d-289">Entrada</span><span class="sxs-lookup"><span data-stu-id="8733d-289">Entry</span></span> | <span data-ttu-id="8733d-290">Value</span><span class="sxs-lookup"><span data-stu-id="8733d-290">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8733d-291">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8733d-291">Link-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8733d-292">MAPI-Id</span></span>                | \-                                                                                                                                |
| <span data-ttu-id="8733d-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="8733d-293">System-Only</span></span>            | <span data-ttu-id="8733d-294">False</span><span class="sxs-lookup"><span data-stu-id="8733d-294">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-295">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8733d-295">Is-Single-Valued</span></span>       | <span data-ttu-id="8733d-296">True</span><span class="sxs-lookup"><span data-stu-id="8733d-296">True</span></span>                                                                                                                              |
| <span data-ttu-id="8733d-297">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8733d-297">Is Indexed</span></span>             | <span data-ttu-id="8733d-298">False</span><span class="sxs-lookup"><span data-stu-id="8733d-298">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-299">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8733d-299">In Global Catalog</span></span>      | <span data-ttu-id="8733d-300">False</span><span class="sxs-lookup"><span data-stu-id="8733d-300">False</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-301">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8733d-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="8733d-302">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8733d-302">O:BAG:BAD:S:</span></span>                                                                                                                      |
| <span data-ttu-id="8733d-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8733d-303">Range-Lower</span></span>            | <span data-ttu-id="8733d-304">0</span><span class="sxs-lookup"><span data-stu-id="8733d-304">0</span></span>                                                                                                                                 |
| <span data-ttu-id="8733d-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8733d-305">Range-Upper</span></span>            | <span data-ttu-id="8733d-306">65535</span><span class="sxs-lookup"><span data-stu-id="8733d-306">65535</span></span>                                                                                                                             |
| <span data-ttu-id="8733d-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-307">Search-Flags</span></span>           | <span data-ttu-id="8733d-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-308">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8733d-309">System-Flags</span></span>           | <span data-ttu-id="8733d-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8733d-310">0x00000010</span></span>                                                                                                                        |
| <span data-ttu-id="8733d-311">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8733d-311">Classes used in</span></span>        | [<span data-ttu-id="8733d-312">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8733d-312">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="8733d-313">**Unidad organizativa**</span><span class="sxs-lookup"><span data-stu-id="8733d-313">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 






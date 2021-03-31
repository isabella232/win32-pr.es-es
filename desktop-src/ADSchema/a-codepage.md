---
title: Code-Page atributo)
description: Especifica la página de códigos para el idioma de elección del usuario. Windows 2000 no usa este valor.
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Code-Page
- atributo de página de códigos esquema de AD
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c3e9858ba387b98d5556c6010490c024be836b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804453"
---
# <a name="code-page-attribute"></a><span data-ttu-id="e2e55-106">Code-Page atributo)</span><span class="sxs-lookup"><span data-stu-id="e2e55-106">Code-Page attribute</span></span>

<span data-ttu-id="e2e55-107">Especifica la página de códigos para el idioma de elección del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2e55-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="e2e55-108">Windows 2000 no usa este valor.</span><span class="sxs-lookup"><span data-stu-id="e2e55-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="e2e55-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="e2e55-109">Entry</span></span> | <span data-ttu-id="e2e55-110">Value</span><span class="sxs-lookup"><span data-stu-id="e2e55-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e2e55-111">CN</span><span class="sxs-lookup"><span data-stu-id="e2e55-111">CN</span></span>                | <span data-ttu-id="e2e55-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="e2e55-112">Code-Page</span></span>                                             |
| <span data-ttu-id="e2e55-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e2e55-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e2e55-114">737</span><span class="sxs-lookup"><span data-stu-id="e2e55-114">codePage</span></span>                                              |
| <span data-ttu-id="e2e55-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e2e55-115">Size</span></span>              | <span data-ttu-id="e2e55-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="e2e55-116">4 bytes</span></span>                                               |
| <span data-ttu-id="e2e55-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e2e55-117">Update Privilege</span></span>  | <span data-ttu-id="e2e55-118">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="e2e55-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="e2e55-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e2e55-119">Update Frequency</span></span>  | <span data-ttu-id="e2e55-120">Cuando el usuario desea cambiar el idioma predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e2e55-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="e2e55-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e2e55-121">Attribute-Id</span></span>      | <span data-ttu-id="e2e55-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="e2e55-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="e2e55-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e2e55-123">System-Id-Guid</span></span>    | <span data-ttu-id="e2e55-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e2e55-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="e2e55-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2e55-125">Syntax</span></span>            | [<span data-ttu-id="e2e55-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="e2e55-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="e2e55-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e2e55-127">Implementations</span></span>

-   [<span data-ttu-id="e2e55-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e2e55-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e2e55-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e2e55-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e2e55-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e2e55-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e2e55-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e2e55-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e2e55-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e2e55-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e2e55-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e2e55-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e2e55-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2e55-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e2e55-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="e2e55-135">Entry</span></span> | <span data-ttu-id="e2e55-136">Value</span><span class="sxs-lookup"><span data-stu-id="e2e55-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e2e55-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e2e55-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2e55-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2e55-139">System-Only</span></span>            | <span data-ttu-id="e2e55-140">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-140">False</span></span>                             |
| <span data-ttu-id="e2e55-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e2e55-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e2e55-142">True</span><span class="sxs-lookup"><span data-stu-id="e2e55-142">True</span></span>                              |
| <span data-ttu-id="e2e55-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e2e55-143">Is Indexed</span></span>             | <span data-ttu-id="e2e55-144">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-144">False</span></span>                             |
| <span data-ttu-id="e2e55-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e2e55-145">In Global Catalog</span></span>      | <span data-ttu-id="e2e55-146">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-146">False</span></span>                             |
| <span data-ttu-id="e2e55-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e2e55-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2e55-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2e55-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e2e55-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2e55-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e2e55-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2e55-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e2e55-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-151">Search-Flags</span></span>           | <span data-ttu-id="e2e55-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-152">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-153">System-Flags</span></span>           | <span data-ttu-id="e2e55-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-154">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e2e55-155">Classes used in</span></span>        | [<span data-ttu-id="e2e55-156">**User**</span><span class="sxs-lookup"><span data-stu-id="e2e55-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e2e55-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e2e55-157">Windows Server 2003</span></span>



| <span data-ttu-id="e2e55-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="e2e55-158">Entry</span></span> | <span data-ttu-id="e2e55-159">Value</span><span class="sxs-lookup"><span data-stu-id="e2e55-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e2e55-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e2e55-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2e55-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2e55-162">System-Only</span></span>            | <span data-ttu-id="e2e55-163">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-163">False</span></span>                             |
| <span data-ttu-id="e2e55-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e2e55-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e2e55-165">True</span><span class="sxs-lookup"><span data-stu-id="e2e55-165">True</span></span>                              |
| <span data-ttu-id="e2e55-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e2e55-166">Is Indexed</span></span>             | <span data-ttu-id="e2e55-167">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-167">False</span></span>                             |
| <span data-ttu-id="e2e55-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e2e55-168">In Global Catalog</span></span>      | <span data-ttu-id="e2e55-169">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-169">False</span></span>                             |
| <span data-ttu-id="e2e55-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e2e55-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2e55-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2e55-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e2e55-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2e55-172">Range-Lower</span></span>            | <span data-ttu-id="e2e55-173">0</span><span class="sxs-lookup"><span data-stu-id="e2e55-173">0</span></span>                                 |
| <span data-ttu-id="e2e55-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2e55-174">Range-Upper</span></span>            | <span data-ttu-id="e2e55-175">65535</span><span class="sxs-lookup"><span data-stu-id="e2e55-175">65535</span></span>                             |
| <span data-ttu-id="e2e55-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-176">Search-Flags</span></span>           | <span data-ttu-id="e2e55-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-177">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-178">System-Flags</span></span>           | <span data-ttu-id="e2e55-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-179">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e2e55-180">Classes used in</span></span>        | [<span data-ttu-id="e2e55-181">**User**</span><span class="sxs-lookup"><span data-stu-id="e2e55-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e2e55-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e2e55-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e2e55-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="e2e55-183">Entry</span></span> | <span data-ttu-id="e2e55-184">Value</span><span class="sxs-lookup"><span data-stu-id="e2e55-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e2e55-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e2e55-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2e55-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2e55-187">System-Only</span></span>            | <span data-ttu-id="e2e55-188">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-188">False</span></span>                             |
| <span data-ttu-id="e2e55-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e2e55-189">Is-Single-Valued</span></span>       | <span data-ttu-id="e2e55-190">True</span><span class="sxs-lookup"><span data-stu-id="e2e55-190">True</span></span>                              |
| <span data-ttu-id="e2e55-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e2e55-191">Is Indexed</span></span>             | <span data-ttu-id="e2e55-192">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-192">False</span></span>                             |
| <span data-ttu-id="e2e55-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e2e55-193">In Global Catalog</span></span>      | <span data-ttu-id="e2e55-194">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-194">False</span></span>                             |
| <span data-ttu-id="e2e55-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e2e55-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2e55-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2e55-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e2e55-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2e55-197">Range-Lower</span></span>            | <span data-ttu-id="e2e55-198">0</span><span class="sxs-lookup"><span data-stu-id="e2e55-198">0</span></span>                                 |
| <span data-ttu-id="e2e55-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2e55-199">Range-Upper</span></span>            | <span data-ttu-id="e2e55-200">65535</span><span class="sxs-lookup"><span data-stu-id="e2e55-200">65535</span></span>                             |
| <span data-ttu-id="e2e55-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-201">Search-Flags</span></span>           | <span data-ttu-id="e2e55-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-202">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-203">System-Flags</span></span>           | <span data-ttu-id="e2e55-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-204">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e2e55-205">Classes used in</span></span>        | [<span data-ttu-id="e2e55-206">**User**</span><span class="sxs-lookup"><span data-stu-id="e2e55-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e2e55-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2e55-207">Windows Server 2008</span></span>



| <span data-ttu-id="e2e55-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="e2e55-208">Entry</span></span> | <span data-ttu-id="e2e55-209">Value</span><span class="sxs-lookup"><span data-stu-id="e2e55-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e2e55-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e2e55-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2e55-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2e55-212">System-Only</span></span>            | <span data-ttu-id="e2e55-213">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-213">False</span></span>                             |
| <span data-ttu-id="e2e55-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e2e55-214">Is-Single-Valued</span></span>       | <span data-ttu-id="e2e55-215">True</span><span class="sxs-lookup"><span data-stu-id="e2e55-215">True</span></span>                              |
| <span data-ttu-id="e2e55-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e2e55-216">Is Indexed</span></span>             | <span data-ttu-id="e2e55-217">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-217">False</span></span>                             |
| <span data-ttu-id="e2e55-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e2e55-218">In Global Catalog</span></span>      | <span data-ttu-id="e2e55-219">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-219">False</span></span>                             |
| <span data-ttu-id="e2e55-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e2e55-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2e55-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2e55-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e2e55-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2e55-222">Range-Lower</span></span>            | <span data-ttu-id="e2e55-223">0</span><span class="sxs-lookup"><span data-stu-id="e2e55-223">0</span></span>                                 |
| <span data-ttu-id="e2e55-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2e55-224">Range-Upper</span></span>            | <span data-ttu-id="e2e55-225">65535</span><span class="sxs-lookup"><span data-stu-id="e2e55-225">65535</span></span>                             |
| <span data-ttu-id="e2e55-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-226">Search-Flags</span></span>           | <span data-ttu-id="e2e55-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-227">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-228">System-Flags</span></span>           | <span data-ttu-id="e2e55-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-229">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e2e55-230">Classes used in</span></span>        | [<span data-ttu-id="e2e55-231">**User**</span><span class="sxs-lookup"><span data-stu-id="e2e55-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e2e55-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2e55-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e2e55-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="e2e55-233">Entry</span></span> | <span data-ttu-id="e2e55-234">Value</span><span class="sxs-lookup"><span data-stu-id="e2e55-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e2e55-235">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e2e55-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2e55-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2e55-237">System-Only</span></span>            | <span data-ttu-id="e2e55-238">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-238">False</span></span>                             |
| <span data-ttu-id="e2e55-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e2e55-239">Is-Single-Valued</span></span>       | <span data-ttu-id="e2e55-240">True</span><span class="sxs-lookup"><span data-stu-id="e2e55-240">True</span></span>                              |
| <span data-ttu-id="e2e55-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e2e55-241">Is Indexed</span></span>             | <span data-ttu-id="e2e55-242">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-242">False</span></span>                             |
| <span data-ttu-id="e2e55-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e2e55-243">In Global Catalog</span></span>      | <span data-ttu-id="e2e55-244">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-244">False</span></span>                             |
| <span data-ttu-id="e2e55-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e2e55-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2e55-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2e55-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e2e55-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2e55-247">Range-Lower</span></span>            | <span data-ttu-id="e2e55-248">0</span><span class="sxs-lookup"><span data-stu-id="e2e55-248">0</span></span>                                 |
| <span data-ttu-id="e2e55-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2e55-249">Range-Upper</span></span>            | <span data-ttu-id="e2e55-250">65535</span><span class="sxs-lookup"><span data-stu-id="e2e55-250">65535</span></span>                             |
| <span data-ttu-id="e2e55-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-251">Search-Flags</span></span>           | <span data-ttu-id="e2e55-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-252">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-253">System-Flags</span></span>           | <span data-ttu-id="e2e55-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-254">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-255">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e2e55-255">Classes used in</span></span>        | [<span data-ttu-id="e2e55-256">**User**</span><span class="sxs-lookup"><span data-stu-id="e2e55-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e2e55-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2e55-257">Windows Server 2012</span></span>



| <span data-ttu-id="e2e55-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="e2e55-258">Entry</span></span> | <span data-ttu-id="e2e55-259">Value</span><span class="sxs-lookup"><span data-stu-id="e2e55-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e2e55-260">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e2e55-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e2e55-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e2e55-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="e2e55-262">System-Only</span></span>            | <span data-ttu-id="e2e55-263">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-263">False</span></span>                             |
| <span data-ttu-id="e2e55-264">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e2e55-264">Is-Single-Valued</span></span>       | <span data-ttu-id="e2e55-265">True</span><span class="sxs-lookup"><span data-stu-id="e2e55-265">True</span></span>                              |
| <span data-ttu-id="e2e55-266">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e2e55-266">Is Indexed</span></span>             | <span data-ttu-id="e2e55-267">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-267">False</span></span>                             |
| <span data-ttu-id="e2e55-268">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e2e55-268">In Global Catalog</span></span>      | <span data-ttu-id="e2e55-269">False</span><span class="sxs-lookup"><span data-stu-id="e2e55-269">False</span></span>                             |
| <span data-ttu-id="e2e55-270">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e2e55-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="e2e55-271">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e2e55-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e2e55-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e2e55-272">Range-Lower</span></span>            | <span data-ttu-id="e2e55-273">0</span><span class="sxs-lookup"><span data-stu-id="e2e55-273">0</span></span>                                 |
| <span data-ttu-id="e2e55-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e2e55-274">Range-Upper</span></span>            | <span data-ttu-id="e2e55-275">65535</span><span class="sxs-lookup"><span data-stu-id="e2e55-275">65535</span></span>                             |
| <span data-ttu-id="e2e55-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-276">Search-Flags</span></span>           | <span data-ttu-id="e2e55-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-277">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e2e55-278">System-Flags</span></span>           | <span data-ttu-id="e2e55-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2e55-279">0x00000010</span></span>                        |
| <span data-ttu-id="e2e55-280">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e2e55-280">Classes used in</span></span>        | [<span data-ttu-id="e2e55-281">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="e2e55-281">**User**</span></span>](c-user.md)<br/> |



 

 






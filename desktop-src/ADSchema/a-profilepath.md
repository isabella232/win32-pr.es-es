---
title: Profile-Path atributo)
description: Especifica una ruta de acceso al perfil del usuario. Este valor puede ser una cadena nula, una ruta de acceso absoluta local o una ruta de acceso UNC.
ms.assetid: 03891152-52c6-4799-ae79-3be284204391
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Profile-Path
- profilePath esquema de AD de atributos
topic_type:
- apiref
api_name:
- Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d1c255843cf578301ce330b79f3ca983030952
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997516"
---
# <a name="profile-path-attribute"></a><span data-ttu-id="51740-106">Profile-Path atributo)</span><span class="sxs-lookup"><span data-stu-id="51740-106">Profile-Path attribute</span></span>

<span data-ttu-id="51740-107">Especifica una ruta de acceso al perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="51740-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="51740-108">Este valor puede ser una cadena nula, una ruta de acceso absoluta local o una ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="51740-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="51740-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="51740-109">Entry</span></span> | <span data-ttu-id="51740-110">Value</span><span class="sxs-lookup"><span data-stu-id="51740-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="51740-111">CN</span><span class="sxs-lookup"><span data-stu-id="51740-111">CN</span></span>                | <span data-ttu-id="51740-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="51740-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="51740-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="51740-113">Ldap-Display-Name</span></span> | <span data-ttu-id="51740-114">profilePath</span><span class="sxs-lookup"><span data-stu-id="51740-114">profilePath</span></span>                                                              |
| <span data-ttu-id="51740-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="51740-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="51740-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="51740-116">Update Privilege</span></span>  | <span data-ttu-id="51740-117">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="51740-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="51740-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="51740-118">Update Frequency</span></span>  | <span data-ttu-id="51740-119">Cuando se crea el registro del usuario y cada vez que es necesario cambiar la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="51740-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="51740-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="51740-120">Attribute-Id</span></span>      | <span data-ttu-id="51740-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="51740-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="51740-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="51740-122">System-Id-Guid</span></span>    | <span data-ttu-id="51740-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="51740-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="51740-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51740-124">Syntax</span></span>            | [<span data-ttu-id="51740-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="51740-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="51740-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="51740-126">Implementations</span></span>

-   [<span data-ttu-id="51740-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="51740-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="51740-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="51740-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="51740-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="51740-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="51740-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="51740-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="51740-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="51740-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="51740-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="51740-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="51740-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="51740-133">Windows 2000 Server</span></span>



| <span data-ttu-id="51740-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="51740-134">Entry</span></span> | <span data-ttu-id="51740-135">Value</span><span class="sxs-lookup"><span data-stu-id="51740-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51740-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="51740-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51740-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="51740-138">System-Only</span></span>            | <span data-ttu-id="51740-139">False</span><span class="sxs-lookup"><span data-stu-id="51740-139">False</span></span>                             |
| <span data-ttu-id="51740-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="51740-140">Is-Single-Valued</span></span>       | <span data-ttu-id="51740-141">True</span><span class="sxs-lookup"><span data-stu-id="51740-141">True</span></span>                              |
| <span data-ttu-id="51740-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="51740-142">Is Indexed</span></span>             | <span data-ttu-id="51740-143">False</span><span class="sxs-lookup"><span data-stu-id="51740-143">False</span></span>                             |
| <span data-ttu-id="51740-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="51740-144">In Global Catalog</span></span>      | <span data-ttu-id="51740-145">False</span><span class="sxs-lookup"><span data-stu-id="51740-145">False</span></span>                             |
| <span data-ttu-id="51740-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="51740-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="51740-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51740-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51740-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51740-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51740-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51740-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51740-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-150">Search-Flags</span></span>           | <span data-ttu-id="51740-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-151">0x00000010</span></span>                        |
| <span data-ttu-id="51740-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-152">System-Flags</span></span>           | <span data-ttu-id="51740-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-153">0x00000010</span></span>                        |
| <span data-ttu-id="51740-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="51740-154">Classes used in</span></span>        | [<span data-ttu-id="51740-155">**User**</span><span class="sxs-lookup"><span data-stu-id="51740-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="51740-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51740-156">Windows Server 2003</span></span>



| <span data-ttu-id="51740-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="51740-157">Entry</span></span> | <span data-ttu-id="51740-158">Value</span><span class="sxs-lookup"><span data-stu-id="51740-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51740-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="51740-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51740-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="51740-161">System-Only</span></span>            | <span data-ttu-id="51740-162">False</span><span class="sxs-lookup"><span data-stu-id="51740-162">False</span></span>                             |
| <span data-ttu-id="51740-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="51740-163">Is-Single-Valued</span></span>       | <span data-ttu-id="51740-164">True</span><span class="sxs-lookup"><span data-stu-id="51740-164">True</span></span>                              |
| <span data-ttu-id="51740-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="51740-165">Is Indexed</span></span>             | <span data-ttu-id="51740-166">False</span><span class="sxs-lookup"><span data-stu-id="51740-166">False</span></span>                             |
| <span data-ttu-id="51740-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="51740-167">In Global Catalog</span></span>      | <span data-ttu-id="51740-168">False</span><span class="sxs-lookup"><span data-stu-id="51740-168">False</span></span>                             |
| <span data-ttu-id="51740-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="51740-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="51740-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51740-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51740-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51740-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51740-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51740-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51740-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-173">Search-Flags</span></span>           | <span data-ttu-id="51740-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-174">0x00000010</span></span>                        |
| <span data-ttu-id="51740-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-175">System-Flags</span></span>           | <span data-ttu-id="51740-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-176">0x00000010</span></span>                        |
| <span data-ttu-id="51740-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="51740-177">Classes used in</span></span>        | [<span data-ttu-id="51740-178">**User**</span><span class="sxs-lookup"><span data-stu-id="51740-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="51740-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="51740-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="51740-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="51740-180">Entry</span></span> | <span data-ttu-id="51740-181">Value</span><span class="sxs-lookup"><span data-stu-id="51740-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51740-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="51740-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51740-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="51740-184">System-Only</span></span>            | <span data-ttu-id="51740-185">False</span><span class="sxs-lookup"><span data-stu-id="51740-185">False</span></span>                             |
| <span data-ttu-id="51740-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="51740-186">Is-Single-Valued</span></span>       | <span data-ttu-id="51740-187">True</span><span class="sxs-lookup"><span data-stu-id="51740-187">True</span></span>                              |
| <span data-ttu-id="51740-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="51740-188">Is Indexed</span></span>             | <span data-ttu-id="51740-189">False</span><span class="sxs-lookup"><span data-stu-id="51740-189">False</span></span>                             |
| <span data-ttu-id="51740-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="51740-190">In Global Catalog</span></span>      | <span data-ttu-id="51740-191">False</span><span class="sxs-lookup"><span data-stu-id="51740-191">False</span></span>                             |
| <span data-ttu-id="51740-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="51740-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="51740-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51740-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51740-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51740-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51740-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51740-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51740-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-196">Search-Flags</span></span>           | <span data-ttu-id="51740-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-197">0x00000010</span></span>                        |
| <span data-ttu-id="51740-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-198">System-Flags</span></span>           | <span data-ttu-id="51740-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-199">0x00000010</span></span>                        |
| <span data-ttu-id="51740-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="51740-200">Classes used in</span></span>        | [<span data-ttu-id="51740-201">**User**</span><span class="sxs-lookup"><span data-stu-id="51740-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="51740-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51740-202">Windows Server 2008</span></span>



| <span data-ttu-id="51740-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="51740-203">Entry</span></span> | <span data-ttu-id="51740-204">Value</span><span class="sxs-lookup"><span data-stu-id="51740-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51740-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="51740-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51740-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="51740-207">System-Only</span></span>            | <span data-ttu-id="51740-208">False</span><span class="sxs-lookup"><span data-stu-id="51740-208">False</span></span>                             |
| <span data-ttu-id="51740-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="51740-209">Is-Single-Valued</span></span>       | <span data-ttu-id="51740-210">True</span><span class="sxs-lookup"><span data-stu-id="51740-210">True</span></span>                              |
| <span data-ttu-id="51740-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="51740-211">Is Indexed</span></span>             | <span data-ttu-id="51740-212">False</span><span class="sxs-lookup"><span data-stu-id="51740-212">False</span></span>                             |
| <span data-ttu-id="51740-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="51740-213">In Global Catalog</span></span>      | <span data-ttu-id="51740-214">False</span><span class="sxs-lookup"><span data-stu-id="51740-214">False</span></span>                             |
| <span data-ttu-id="51740-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="51740-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="51740-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51740-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51740-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51740-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51740-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51740-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51740-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-219">Search-Flags</span></span>           | <span data-ttu-id="51740-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-220">0x00000010</span></span>                        |
| <span data-ttu-id="51740-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-221">System-Flags</span></span>           | <span data-ttu-id="51740-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-222">0x00000010</span></span>                        |
| <span data-ttu-id="51740-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="51740-223">Classes used in</span></span>        | [<span data-ttu-id="51740-224">**User**</span><span class="sxs-lookup"><span data-stu-id="51740-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="51740-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="51740-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="51740-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="51740-226">Entry</span></span> | <span data-ttu-id="51740-227">Value</span><span class="sxs-lookup"><span data-stu-id="51740-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51740-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="51740-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51740-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="51740-230">System-Only</span></span>            | <span data-ttu-id="51740-231">False</span><span class="sxs-lookup"><span data-stu-id="51740-231">False</span></span>                             |
| <span data-ttu-id="51740-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="51740-232">Is-Single-Valued</span></span>       | <span data-ttu-id="51740-233">True</span><span class="sxs-lookup"><span data-stu-id="51740-233">True</span></span>                              |
| <span data-ttu-id="51740-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="51740-234">Is Indexed</span></span>             | <span data-ttu-id="51740-235">False</span><span class="sxs-lookup"><span data-stu-id="51740-235">False</span></span>                             |
| <span data-ttu-id="51740-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="51740-236">In Global Catalog</span></span>      | <span data-ttu-id="51740-237">False</span><span class="sxs-lookup"><span data-stu-id="51740-237">False</span></span>                             |
| <span data-ttu-id="51740-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="51740-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="51740-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51740-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51740-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51740-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51740-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51740-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51740-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-242">Search-Flags</span></span>           | <span data-ttu-id="51740-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-243">0x00000010</span></span>                        |
| <span data-ttu-id="51740-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-244">System-Flags</span></span>           | <span data-ttu-id="51740-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-245">0x00000010</span></span>                        |
| <span data-ttu-id="51740-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="51740-246">Classes used in</span></span>        | [<span data-ttu-id="51740-247">**User**</span><span class="sxs-lookup"><span data-stu-id="51740-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="51740-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51740-248">Windows Server 2012</span></span>



| <span data-ttu-id="51740-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="51740-249">Entry</span></span> | <span data-ttu-id="51740-250">Value</span><span class="sxs-lookup"><span data-stu-id="51740-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="51740-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="51740-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="51740-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="51740-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="51740-253">System-Only</span></span>            | <span data-ttu-id="51740-254">False</span><span class="sxs-lookup"><span data-stu-id="51740-254">False</span></span>                             |
| <span data-ttu-id="51740-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="51740-255">Is-Single-Valued</span></span>       | <span data-ttu-id="51740-256">True</span><span class="sxs-lookup"><span data-stu-id="51740-256">True</span></span>                              |
| <span data-ttu-id="51740-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="51740-257">Is Indexed</span></span>             | <span data-ttu-id="51740-258">False</span><span class="sxs-lookup"><span data-stu-id="51740-258">False</span></span>                             |
| <span data-ttu-id="51740-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="51740-259">In Global Catalog</span></span>      | <span data-ttu-id="51740-260">False</span><span class="sxs-lookup"><span data-stu-id="51740-260">False</span></span>                             |
| <span data-ttu-id="51740-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="51740-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="51740-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="51740-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="51740-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="51740-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="51740-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="51740-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="51740-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-265">Search-Flags</span></span>           | <span data-ttu-id="51740-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-266">0x00000010</span></span>                        |
| <span data-ttu-id="51740-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="51740-267">System-Flags</span></span>           | <span data-ttu-id="51740-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51740-268">0x00000010</span></span>                        |
| <span data-ttu-id="51740-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="51740-269">Classes used in</span></span>        | [<span data-ttu-id="51740-270">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="51740-270">**User**</span></span>](c-user.md)<br/> |



 

 






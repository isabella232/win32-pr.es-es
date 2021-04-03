---
title: Atributo de nombre principal de usuario
description: Este atributo contiene el UPN que es un nombre de inicio de sesión de estilo Internet para un usuario basado en el estándar de Internet RFC 822.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre principal de usuario
- atributo userPrincipalName esquema de AD
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997356"
---
# <a name="user-principal-name-attribute"></a><span data-ttu-id="30934-105">Atributo de nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="30934-105">User-Principal-Name attribute</span></span>

<span data-ttu-id="30934-106">Este atributo contiene el UPN que es un nombre de inicio de sesión de estilo Internet para un usuario basado en el estándar de Internet [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span><span class="sxs-lookup"><span data-stu-id="30934-106">This attribute contains the UPN that is an Internet-style login name for a user based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt).</span></span> <span data-ttu-id="30934-107">El UPN es más corto que el nombre distintivo y más fácil de recordar.</span><span class="sxs-lookup"><span data-stu-id="30934-107">The UPN is shorter than the distinguished name and easier to remember.</span></span> <span data-ttu-id="30934-108">Por Convención, se debe asignar al nombre de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="30934-108">By convention, this should map to the user email name.</span></span> <span data-ttu-id="30934-109">El valor establecido para este atributo es igual a la longitud del identificador del usuario y el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="30934-109">The value set for this attribute is equal to the length of the user's ID and the domain name.</span></span> <span data-ttu-id="30934-110">Para obtener más información sobre este atributo, vea [atributos de asignación de nombres de usuario](/windows/desktop/AD/naming-properties).</span><span class="sxs-lookup"><span data-stu-id="30934-110">For more information about this attribute, see [User Naming Attributes](/windows/desktop/AD/naming-properties).</span></span>



| <span data-ttu-id="30934-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="30934-111">Entry</span></span> | <span data-ttu-id="30934-112">Value</span><span class="sxs-lookup"><span data-stu-id="30934-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="30934-113">CN</span><span class="sxs-lookup"><span data-stu-id="30934-113">CN</span></span>                | <span data-ttu-id="30934-114">User-Principal-Name</span><span class="sxs-lookup"><span data-stu-id="30934-114">User-Principal-Name</span></span>                         |
| <span data-ttu-id="30934-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="30934-115">Ldap-Display-Name</span></span> | <span data-ttu-id="30934-116">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="30934-116">userPrincipalName</span></span>                           |
| <span data-ttu-id="30934-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="30934-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="30934-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="30934-118">Update Privilege</span></span>  | <span data-ttu-id="30934-119">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="30934-119">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="30934-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="30934-120">Update Frequency</span></span>  | <span data-ttu-id="30934-121">En teoría, esto nunca debería cambiar.</span><span class="sxs-lookup"><span data-stu-id="30934-121">In theory this should never change.</span></span>         |
| <span data-ttu-id="30934-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="30934-122">Attribute-Id</span></span>      | <span data-ttu-id="30934-123">1.2.840.113556.1.4.656</span><span class="sxs-lookup"><span data-stu-id="30934-123">1.2.840.113556.1.4.656</span></span>                      |
| <span data-ttu-id="30934-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="30934-124">System-Id-Guid</span></span>    | <span data-ttu-id="30934-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="30934-125">28630ebb-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="30934-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30934-126">Syntax</span></span>            | [<span data-ttu-id="30934-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="30934-127">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="30934-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="30934-128">Implementations</span></span>

-   [<span data-ttu-id="30934-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="30934-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="30934-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="30934-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="30934-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="30934-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="30934-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="30934-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="30934-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="30934-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="30934-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="30934-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="30934-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="30934-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="30934-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="30934-136">Windows 2000 Server</span></span>



| <span data-ttu-id="30934-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="30934-137">Entry</span></span> | <span data-ttu-id="30934-138">Value</span><span class="sxs-lookup"><span data-stu-id="30934-138">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30934-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30934-139">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30934-140">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="30934-141">System-Only</span></span>            | <span data-ttu-id="30934-142">False</span><span class="sxs-lookup"><span data-stu-id="30934-142">False</span></span>                             |
| <span data-ttu-id="30934-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30934-143">Is-Single-Valued</span></span>       | <span data-ttu-id="30934-144">True</span><span class="sxs-lookup"><span data-stu-id="30934-144">True</span></span>                              |
| <span data-ttu-id="30934-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30934-145">Is Indexed</span></span>             | <span data-ttu-id="30934-146">True</span><span class="sxs-lookup"><span data-stu-id="30934-146">True</span></span>                              |
| <span data-ttu-id="30934-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30934-147">In Global Catalog</span></span>      | <span data-ttu-id="30934-148">True</span><span class="sxs-lookup"><span data-stu-id="30934-148">True</span></span>                              |
| <span data-ttu-id="30934-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30934-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="30934-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30934-150">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30934-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30934-151">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30934-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30934-152">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30934-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-153">Search-Flags</span></span>           | <span data-ttu-id="30934-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30934-154">0x00000001</span></span>                        |
| <span data-ttu-id="30934-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-155">System-Flags</span></span>           | <span data-ttu-id="30934-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="30934-156">0x00000012</span></span>                        |
| <span data-ttu-id="30934-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30934-157">Classes used in</span></span>        | [<span data-ttu-id="30934-158">**User**</span><span class="sxs-lookup"><span data-stu-id="30934-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="30934-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30934-159">Windows Server 2003</span></span>



| <span data-ttu-id="30934-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="30934-160">Entry</span></span> | <span data-ttu-id="30934-161">Value</span><span class="sxs-lookup"><span data-stu-id="30934-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30934-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30934-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30934-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="30934-164">System-Only</span></span>            | <span data-ttu-id="30934-165">False</span><span class="sxs-lookup"><span data-stu-id="30934-165">False</span></span>                             |
| <span data-ttu-id="30934-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30934-166">Is-Single-Valued</span></span>       | <span data-ttu-id="30934-167">True</span><span class="sxs-lookup"><span data-stu-id="30934-167">True</span></span>                              |
| <span data-ttu-id="30934-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30934-168">Is Indexed</span></span>             | <span data-ttu-id="30934-169">True</span><span class="sxs-lookup"><span data-stu-id="30934-169">True</span></span>                              |
| <span data-ttu-id="30934-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30934-170">In Global Catalog</span></span>      | <span data-ttu-id="30934-171">True</span><span class="sxs-lookup"><span data-stu-id="30934-171">True</span></span>                              |
| <span data-ttu-id="30934-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30934-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="30934-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30934-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30934-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30934-174">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30934-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30934-175">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30934-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-176">Search-Flags</span></span>           | <span data-ttu-id="30934-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30934-177">0x00000001</span></span>                        |
| <span data-ttu-id="30934-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-178">System-Flags</span></span>           | <span data-ttu-id="30934-179">0x00000012</span><span class="sxs-lookup"><span data-stu-id="30934-179">0x00000012</span></span>                        |
| <span data-ttu-id="30934-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30934-180">Classes used in</span></span>        | [<span data-ttu-id="30934-181">**User**</span><span class="sxs-lookup"><span data-stu-id="30934-181">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="30934-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="30934-182">ADAM</span></span>



| <span data-ttu-id="30934-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="30934-183">Entry</span></span> | <span data-ttu-id="30934-184">Value</span><span class="sxs-lookup"><span data-stu-id="30934-184">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="30934-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30934-185">Link-Id</span></span>                | \-           |
| <span data-ttu-id="30934-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30934-186">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="30934-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="30934-187">System-Only</span></span>            | <span data-ttu-id="30934-188">False</span><span class="sxs-lookup"><span data-stu-id="30934-188">False</span></span>        |
| <span data-ttu-id="30934-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30934-189">Is-Single-Valued</span></span>       | <span data-ttu-id="30934-190">True</span><span class="sxs-lookup"><span data-stu-id="30934-190">True</span></span>         |
| <span data-ttu-id="30934-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30934-191">Is Indexed</span></span>             | <span data-ttu-id="30934-192">True</span><span class="sxs-lookup"><span data-stu-id="30934-192">True</span></span>         |
| <span data-ttu-id="30934-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30934-193">In Global Catalog</span></span>      | <span data-ttu-id="30934-194">True</span><span class="sxs-lookup"><span data-stu-id="30934-194">True</span></span>         |
| <span data-ttu-id="30934-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30934-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="30934-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30934-196">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="30934-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30934-197">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="30934-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30934-198">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="30934-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-199">Search-Flags</span></span>           | <span data-ttu-id="30934-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30934-200">0x00000001</span></span>   |
| <span data-ttu-id="30934-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-201">System-Flags</span></span>           | <span data-ttu-id="30934-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="30934-202">0x00000012</span></span>   |
| <span data-ttu-id="30934-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30934-203">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="30934-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="30934-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="30934-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="30934-205">Entry</span></span> | <span data-ttu-id="30934-206">Value</span><span class="sxs-lookup"><span data-stu-id="30934-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30934-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30934-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30934-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="30934-209">System-Only</span></span>            | <span data-ttu-id="30934-210">False</span><span class="sxs-lookup"><span data-stu-id="30934-210">False</span></span>                             |
| <span data-ttu-id="30934-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30934-211">Is-Single-Valued</span></span>       | <span data-ttu-id="30934-212">True</span><span class="sxs-lookup"><span data-stu-id="30934-212">True</span></span>                              |
| <span data-ttu-id="30934-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30934-213">Is Indexed</span></span>             | <span data-ttu-id="30934-214">True</span><span class="sxs-lookup"><span data-stu-id="30934-214">True</span></span>                              |
| <span data-ttu-id="30934-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30934-215">In Global Catalog</span></span>      | <span data-ttu-id="30934-216">True</span><span class="sxs-lookup"><span data-stu-id="30934-216">True</span></span>                              |
| <span data-ttu-id="30934-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30934-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="30934-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30934-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30934-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30934-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30934-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30934-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30934-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-221">Search-Flags</span></span>           | <span data-ttu-id="30934-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30934-222">0x00000001</span></span>                        |
| <span data-ttu-id="30934-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-223">System-Flags</span></span>           | <span data-ttu-id="30934-224">0x00000012</span><span class="sxs-lookup"><span data-stu-id="30934-224">0x00000012</span></span>                        |
| <span data-ttu-id="30934-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30934-225">Classes used in</span></span>        | [<span data-ttu-id="30934-226">**User**</span><span class="sxs-lookup"><span data-stu-id="30934-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="30934-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30934-227">Windows Server 2008</span></span>



| <span data-ttu-id="30934-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="30934-228">Entry</span></span> | <span data-ttu-id="30934-229">Value</span><span class="sxs-lookup"><span data-stu-id="30934-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30934-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30934-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30934-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="30934-232">System-Only</span></span>            | <span data-ttu-id="30934-233">False</span><span class="sxs-lookup"><span data-stu-id="30934-233">False</span></span>                             |
| <span data-ttu-id="30934-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30934-234">Is-Single-Valued</span></span>       | <span data-ttu-id="30934-235">True</span><span class="sxs-lookup"><span data-stu-id="30934-235">True</span></span>                              |
| <span data-ttu-id="30934-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30934-236">Is Indexed</span></span>             | <span data-ttu-id="30934-237">True</span><span class="sxs-lookup"><span data-stu-id="30934-237">True</span></span>                              |
| <span data-ttu-id="30934-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30934-238">In Global Catalog</span></span>      | <span data-ttu-id="30934-239">True</span><span class="sxs-lookup"><span data-stu-id="30934-239">True</span></span>                              |
| <span data-ttu-id="30934-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30934-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="30934-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30934-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30934-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30934-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30934-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30934-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30934-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-244">Search-Flags</span></span>           | <span data-ttu-id="30934-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30934-245">0x00000001</span></span>                        |
| <span data-ttu-id="30934-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-246">System-Flags</span></span>           | <span data-ttu-id="30934-247">0x00000012</span><span class="sxs-lookup"><span data-stu-id="30934-247">0x00000012</span></span>                        |
| <span data-ttu-id="30934-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30934-248">Classes used in</span></span>        | [<span data-ttu-id="30934-249">**User**</span><span class="sxs-lookup"><span data-stu-id="30934-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="30934-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30934-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="30934-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="30934-251">Entry</span></span> | <span data-ttu-id="30934-252">Value</span><span class="sxs-lookup"><span data-stu-id="30934-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30934-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30934-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30934-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="30934-255">System-Only</span></span>            | <span data-ttu-id="30934-256">False</span><span class="sxs-lookup"><span data-stu-id="30934-256">False</span></span>                             |
| <span data-ttu-id="30934-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30934-257">Is-Single-Valued</span></span>       | <span data-ttu-id="30934-258">True</span><span class="sxs-lookup"><span data-stu-id="30934-258">True</span></span>                              |
| <span data-ttu-id="30934-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30934-259">Is Indexed</span></span>             | <span data-ttu-id="30934-260">True</span><span class="sxs-lookup"><span data-stu-id="30934-260">True</span></span>                              |
| <span data-ttu-id="30934-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30934-261">In Global Catalog</span></span>      | <span data-ttu-id="30934-262">True</span><span class="sxs-lookup"><span data-stu-id="30934-262">True</span></span>                              |
| <span data-ttu-id="30934-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30934-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="30934-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30934-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30934-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30934-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30934-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30934-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30934-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-267">Search-Flags</span></span>           | <span data-ttu-id="30934-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30934-268">0x00000001</span></span>                        |
| <span data-ttu-id="30934-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-269">System-Flags</span></span>           | <span data-ttu-id="30934-270">0x00000012</span><span class="sxs-lookup"><span data-stu-id="30934-270">0x00000012</span></span>                        |
| <span data-ttu-id="30934-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30934-271">Classes used in</span></span>        | [<span data-ttu-id="30934-272">**User**</span><span class="sxs-lookup"><span data-stu-id="30934-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="30934-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30934-273">Windows Server 2012</span></span>



| <span data-ttu-id="30934-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="30934-274">Entry</span></span> | <span data-ttu-id="30934-275">Value</span><span class="sxs-lookup"><span data-stu-id="30934-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30934-276">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30934-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30934-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30934-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="30934-278">System-Only</span></span>            | <span data-ttu-id="30934-279">False</span><span class="sxs-lookup"><span data-stu-id="30934-279">False</span></span>                             |
| <span data-ttu-id="30934-280">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30934-280">Is-Single-Valued</span></span>       | <span data-ttu-id="30934-281">True</span><span class="sxs-lookup"><span data-stu-id="30934-281">True</span></span>                              |
| <span data-ttu-id="30934-282">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30934-282">Is Indexed</span></span>             | <span data-ttu-id="30934-283">True</span><span class="sxs-lookup"><span data-stu-id="30934-283">True</span></span>                              |
| <span data-ttu-id="30934-284">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30934-284">In Global Catalog</span></span>      | <span data-ttu-id="30934-285">True</span><span class="sxs-lookup"><span data-stu-id="30934-285">True</span></span>                              |
| <span data-ttu-id="30934-286">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30934-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="30934-287">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30934-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30934-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30934-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="30934-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30934-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="30934-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-290">Search-Flags</span></span>           | <span data-ttu-id="30934-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30934-291">0x00000001</span></span>                        |
| <span data-ttu-id="30934-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30934-292">System-Flags</span></span>           | <span data-ttu-id="30934-293">0x00000012</span><span class="sxs-lookup"><span data-stu-id="30934-293">0x00000012</span></span>                        |
| <span data-ttu-id="30934-294">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30934-294">Classes used in</span></span>        | [<span data-ttu-id="30934-295">**User**</span><span class="sxs-lookup"><span data-stu-id="30934-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="30934-296">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30934-296">Remarks</span></span>

<span data-ttu-id="30934-297">En ADAM, no es necesario que este atributo tenga el formato estándar de Internet RFC 822. puede ser un nombre simple.</span><span class="sxs-lookup"><span data-stu-id="30934-297">In ADAM, this attribute is not required to be in the Internet standard RFC 822 format; it can be a simple name.</span></span>

 


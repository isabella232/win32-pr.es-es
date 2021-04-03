---
title: Logon-Count atributo)
description: El número de veces que la cuenta ha iniciado sesión correctamente. Un valor de 0 indica que el valor es desconocido.
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Logon-Count
- logonCount esquema de AD de atributos
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ba7865cb3b90f42ede71b169f98f8ce45e722d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906071"
---
# <a name="logon-count-attribute"></a><span data-ttu-id="04390-106">Logon-Count atributo)</span><span class="sxs-lookup"><span data-stu-id="04390-106">Logon-Count attribute</span></span>

<span data-ttu-id="04390-107">El número de veces que la cuenta ha iniciado sesión correctamente.</span><span class="sxs-lookup"><span data-stu-id="04390-107">The number of times the account has successfully logged on.</span></span> <span data-ttu-id="04390-108">Un valor de 0 indica que el valor es desconocido.</span><span class="sxs-lookup"><span data-stu-id="04390-108">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="04390-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="04390-109">Entry</span></span> | <span data-ttu-id="04390-110">Value</span><span class="sxs-lookup"><span data-stu-id="04390-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="04390-111">CN</span><span class="sxs-lookup"><span data-stu-id="04390-111">CN</span></span>                | <span data-ttu-id="04390-112">Logon-Count</span><span class="sxs-lookup"><span data-stu-id="04390-112">Logon-Count</span></span>                          |
| <span data-ttu-id="04390-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="04390-113">Ldap-Display-Name</span></span> | <span data-ttu-id="04390-114">logonCount</span><span class="sxs-lookup"><span data-stu-id="04390-114">logonCount</span></span>                           |
| <span data-ttu-id="04390-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="04390-115">Size</span></span>              | <span data-ttu-id="04390-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="04390-116">4 bytes</span></span>                              |
| <span data-ttu-id="04390-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="04390-117">Update Privilege</span></span>  | <span data-ttu-id="04390-118">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="04390-118">Domain administrator</span></span>                 |
| <span data-ttu-id="04390-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="04390-119">Update Frequency</span></span>  | <span data-ttu-id="04390-120">Cada vez que el usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="04390-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="04390-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04390-121">Attribute-Id</span></span>      | <span data-ttu-id="04390-122">1.2.840.113556.1.4.169</span><span class="sxs-lookup"><span data-stu-id="04390-122">1.2.840.113556.1.4.169</span></span>               |
| <span data-ttu-id="04390-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="04390-123">System-Id-Guid</span></span>    | <span data-ttu-id="04390-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="04390-124">bf9679aa-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="04390-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04390-125">Syntax</span></span>            | [<span data-ttu-id="04390-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="04390-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="04390-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="04390-127">Implementations</span></span>

-   [<span data-ttu-id="04390-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04390-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04390-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04390-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04390-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04390-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04390-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04390-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04390-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04390-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04390-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04390-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04390-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04390-134">Windows 2000 Server</span></span>



| <span data-ttu-id="04390-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="04390-135">Entry</span></span> | <span data-ttu-id="04390-136">Value</span><span class="sxs-lookup"><span data-stu-id="04390-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="04390-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="04390-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04390-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="04390-139">System-Only</span></span>            | <span data-ttu-id="04390-140">False</span><span class="sxs-lookup"><span data-stu-id="04390-140">False</span></span>                             |
| <span data-ttu-id="04390-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="04390-141">Is-Single-Valued</span></span>       | <span data-ttu-id="04390-142">True</span><span class="sxs-lookup"><span data-stu-id="04390-142">True</span></span>                              |
| <span data-ttu-id="04390-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="04390-143">Is Indexed</span></span>             | <span data-ttu-id="04390-144">False</span><span class="sxs-lookup"><span data-stu-id="04390-144">False</span></span>                             |
| <span data-ttu-id="04390-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="04390-145">In Global Catalog</span></span>      | <span data-ttu-id="04390-146">False</span><span class="sxs-lookup"><span data-stu-id="04390-146">False</span></span>                             |
| <span data-ttu-id="04390-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="04390-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="04390-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04390-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="04390-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04390-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="04390-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04390-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="04390-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-151">Search-Flags</span></span>           | <span data-ttu-id="04390-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04390-152">0x00000000</span></span>                        |
| <span data-ttu-id="04390-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-153">System-Flags</span></span>           | <span data-ttu-id="04390-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04390-154">0x00000011</span></span>                        |
| <span data-ttu-id="04390-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="04390-155">Classes used in</span></span>        | [<span data-ttu-id="04390-156">**User**</span><span class="sxs-lookup"><span data-stu-id="04390-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04390-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04390-157">Windows Server 2003</span></span>



| <span data-ttu-id="04390-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="04390-158">Entry</span></span> | <span data-ttu-id="04390-159">Value</span><span class="sxs-lookup"><span data-stu-id="04390-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="04390-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="04390-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04390-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="04390-162">System-Only</span></span>            | <span data-ttu-id="04390-163">False</span><span class="sxs-lookup"><span data-stu-id="04390-163">False</span></span>                             |
| <span data-ttu-id="04390-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="04390-164">Is-Single-Valued</span></span>       | <span data-ttu-id="04390-165">True</span><span class="sxs-lookup"><span data-stu-id="04390-165">True</span></span>                              |
| <span data-ttu-id="04390-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="04390-166">Is Indexed</span></span>             | <span data-ttu-id="04390-167">False</span><span class="sxs-lookup"><span data-stu-id="04390-167">False</span></span>                             |
| <span data-ttu-id="04390-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="04390-168">In Global Catalog</span></span>      | <span data-ttu-id="04390-169">False</span><span class="sxs-lookup"><span data-stu-id="04390-169">False</span></span>                             |
| <span data-ttu-id="04390-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="04390-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="04390-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04390-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="04390-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04390-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="04390-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04390-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="04390-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-174">Search-Flags</span></span>           | <span data-ttu-id="04390-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04390-175">0x00000000</span></span>                        |
| <span data-ttu-id="04390-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-176">System-Flags</span></span>           | <span data-ttu-id="04390-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04390-177">0x00000011</span></span>                        |
| <span data-ttu-id="04390-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="04390-178">Classes used in</span></span>        | [<span data-ttu-id="04390-179">**User**</span><span class="sxs-lookup"><span data-stu-id="04390-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04390-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04390-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04390-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="04390-181">Entry</span></span> | <span data-ttu-id="04390-182">Value</span><span class="sxs-lookup"><span data-stu-id="04390-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="04390-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="04390-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04390-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="04390-185">System-Only</span></span>            | <span data-ttu-id="04390-186">False</span><span class="sxs-lookup"><span data-stu-id="04390-186">False</span></span>                             |
| <span data-ttu-id="04390-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="04390-187">Is-Single-Valued</span></span>       | <span data-ttu-id="04390-188">True</span><span class="sxs-lookup"><span data-stu-id="04390-188">True</span></span>                              |
| <span data-ttu-id="04390-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="04390-189">Is Indexed</span></span>             | <span data-ttu-id="04390-190">False</span><span class="sxs-lookup"><span data-stu-id="04390-190">False</span></span>                             |
| <span data-ttu-id="04390-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="04390-191">In Global Catalog</span></span>      | <span data-ttu-id="04390-192">False</span><span class="sxs-lookup"><span data-stu-id="04390-192">False</span></span>                             |
| <span data-ttu-id="04390-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="04390-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="04390-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04390-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="04390-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04390-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="04390-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04390-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="04390-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-197">Search-Flags</span></span>           | <span data-ttu-id="04390-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04390-198">0x00000000</span></span>                        |
| <span data-ttu-id="04390-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-199">System-Flags</span></span>           | <span data-ttu-id="04390-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04390-200">0x00000011</span></span>                        |
| <span data-ttu-id="04390-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="04390-201">Classes used in</span></span>        | [<span data-ttu-id="04390-202">**User**</span><span class="sxs-lookup"><span data-stu-id="04390-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04390-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04390-203">Windows Server 2008</span></span>



| <span data-ttu-id="04390-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="04390-204">Entry</span></span> | <span data-ttu-id="04390-205">Value</span><span class="sxs-lookup"><span data-stu-id="04390-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="04390-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="04390-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04390-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="04390-208">System-Only</span></span>            | <span data-ttu-id="04390-209">False</span><span class="sxs-lookup"><span data-stu-id="04390-209">False</span></span>                             |
| <span data-ttu-id="04390-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="04390-210">Is-Single-Valued</span></span>       | <span data-ttu-id="04390-211">True</span><span class="sxs-lookup"><span data-stu-id="04390-211">True</span></span>                              |
| <span data-ttu-id="04390-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="04390-212">Is Indexed</span></span>             | <span data-ttu-id="04390-213">False</span><span class="sxs-lookup"><span data-stu-id="04390-213">False</span></span>                             |
| <span data-ttu-id="04390-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="04390-214">In Global Catalog</span></span>      | <span data-ttu-id="04390-215">False</span><span class="sxs-lookup"><span data-stu-id="04390-215">False</span></span>                             |
| <span data-ttu-id="04390-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="04390-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="04390-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04390-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="04390-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04390-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="04390-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04390-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="04390-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-220">Search-Flags</span></span>           | <span data-ttu-id="04390-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04390-221">0x00000000</span></span>                        |
| <span data-ttu-id="04390-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-222">System-Flags</span></span>           | <span data-ttu-id="04390-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04390-223">0x00000011</span></span>                        |
| <span data-ttu-id="04390-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="04390-224">Classes used in</span></span>        | [<span data-ttu-id="04390-225">**User**</span><span class="sxs-lookup"><span data-stu-id="04390-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04390-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04390-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04390-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="04390-227">Entry</span></span> | <span data-ttu-id="04390-228">Value</span><span class="sxs-lookup"><span data-stu-id="04390-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="04390-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="04390-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04390-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="04390-231">System-Only</span></span>            | <span data-ttu-id="04390-232">False</span><span class="sxs-lookup"><span data-stu-id="04390-232">False</span></span>                             |
| <span data-ttu-id="04390-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="04390-233">Is-Single-Valued</span></span>       | <span data-ttu-id="04390-234">True</span><span class="sxs-lookup"><span data-stu-id="04390-234">True</span></span>                              |
| <span data-ttu-id="04390-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="04390-235">Is Indexed</span></span>             | <span data-ttu-id="04390-236">False</span><span class="sxs-lookup"><span data-stu-id="04390-236">False</span></span>                             |
| <span data-ttu-id="04390-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="04390-237">In Global Catalog</span></span>      | <span data-ttu-id="04390-238">False</span><span class="sxs-lookup"><span data-stu-id="04390-238">False</span></span>                             |
| <span data-ttu-id="04390-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="04390-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="04390-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04390-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="04390-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04390-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="04390-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04390-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="04390-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-243">Search-Flags</span></span>           | <span data-ttu-id="04390-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04390-244">0x00000000</span></span>                        |
| <span data-ttu-id="04390-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-245">System-Flags</span></span>           | <span data-ttu-id="04390-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04390-246">0x00000011</span></span>                        |
| <span data-ttu-id="04390-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="04390-247">Classes used in</span></span>        | [<span data-ttu-id="04390-248">**User**</span><span class="sxs-lookup"><span data-stu-id="04390-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04390-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04390-249">Windows Server 2012</span></span>



| <span data-ttu-id="04390-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="04390-250">Entry</span></span> | <span data-ttu-id="04390-251">Value</span><span class="sxs-lookup"><span data-stu-id="04390-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="04390-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="04390-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04390-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="04390-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="04390-254">System-Only</span></span>            | <span data-ttu-id="04390-255">False</span><span class="sxs-lookup"><span data-stu-id="04390-255">False</span></span>                             |
| <span data-ttu-id="04390-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="04390-256">Is-Single-Valued</span></span>       | <span data-ttu-id="04390-257">True</span><span class="sxs-lookup"><span data-stu-id="04390-257">True</span></span>                              |
| <span data-ttu-id="04390-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="04390-258">Is Indexed</span></span>             | <span data-ttu-id="04390-259">False</span><span class="sxs-lookup"><span data-stu-id="04390-259">False</span></span>                             |
| <span data-ttu-id="04390-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="04390-260">In Global Catalog</span></span>      | <span data-ttu-id="04390-261">False</span><span class="sxs-lookup"><span data-stu-id="04390-261">False</span></span>                             |
| <span data-ttu-id="04390-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="04390-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="04390-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="04390-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="04390-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04390-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="04390-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04390-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="04390-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-266">Search-Flags</span></span>           | <span data-ttu-id="04390-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04390-267">0x00000000</span></span>                        |
| <span data-ttu-id="04390-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04390-268">System-Flags</span></span>           | <span data-ttu-id="04390-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04390-269">0x00000011</span></span>                        |
| <span data-ttu-id="04390-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="04390-270">Classes used in</span></span>        | [<span data-ttu-id="04390-271">**User**</span><span class="sxs-lookup"><span data-stu-id="04390-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="04390-272">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04390-272">Remarks</span></span>

<span data-ttu-id="04390-273">Este atributo no se replica y se mantiene en cada controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="04390-273">This attribute is not replicated and is maintained on each domain controller in the domain.</span></span> <span data-ttu-id="04390-274">Para obtener un valor preciso para el número total de intentos de inicio de sesión correctos del usuario en el dominio, se deben consultar todos los controladores de dominio del dominio y se debe usar la suma de los valores.</span><span class="sxs-lookup"><span data-stu-id="04390-274">To get an accurate value for the user's total number of successful logon attempts in the domain, each domain controller in the domain must be queried and the sum of the values should be used.</span></span> <span data-ttu-id="04390-275">Tenga en cuenta que el atributo no se replica, por lo tanto, los controladores de dominio que se retiran también pueden haber contado los inicios de sesión del usuario y estos no aparecerán en el recuento.</span><span class="sxs-lookup"><span data-stu-id="04390-275">Keep in mind that the attribute is not replicated, therefore domain controllers that are retired may have counted logons for the user as well, and these will be missing from the count.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04390-276">Debido a la compatibilidad con las versiones de 16 bits de LAN Manager, el atributo tiene un límite superior de 65535.</span><span class="sxs-lookup"><span data-stu-id="04390-276">Due to compatibility with 16-bit versions of LAN Manager, the attribute has an upper limit of 65535.</span></span> <span data-ttu-id="04390-277">Una vez alcanzado este límite, no se puede usar como un indicador de la actividad del usuario en este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="04390-277">After this limit has been reached, you cannot use it as an indicator of user activity on this domain controller.</span></span>

 

 

 






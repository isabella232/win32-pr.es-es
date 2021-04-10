---
title: Atributo Bad-pwd-Count
description: El número de veces que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo incorrecto-pwd-Count
- badPwdCount esquema de AD de atributos
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3a406058737773781874a81e9968786e1523d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151487"
---
# <a name="bad-pwd-count-attribute"></a><span data-ttu-id="66201-105">Atributo Bad-pwd-Count</span><span class="sxs-lookup"><span data-stu-id="66201-105">Bad-Pwd-Count attribute</span></span>

<span data-ttu-id="66201-106">El número de veces que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta.</span><span class="sxs-lookup"><span data-stu-id="66201-106">The number of times the user tried to log on to the account using an incorrect password.</span></span> <span data-ttu-id="66201-107">Un valor de 0 indica que el valor es desconocido.</span><span class="sxs-lookup"><span data-stu-id="66201-107">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="66201-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="66201-108">Entry</span></span> | <span data-ttu-id="66201-109">Value</span><span class="sxs-lookup"><span data-stu-id="66201-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="66201-110">CN</span><span class="sxs-lookup"><span data-stu-id="66201-110">CN</span></span>                | <span data-ttu-id="66201-111">Incorrecto: PWD-Count</span><span class="sxs-lookup"><span data-stu-id="66201-111">Bad-Pwd-Count</span></span>                             |
| <span data-ttu-id="66201-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="66201-112">Ldap-Display-Name</span></span> | <span data-ttu-id="66201-113">badPwdCount</span><span class="sxs-lookup"><span data-stu-id="66201-113">badPwdCount</span></span>                               |
| <span data-ttu-id="66201-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="66201-114">Size</span></span>              | <span data-ttu-id="66201-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="66201-115">4 bytes</span></span>                                   |
| <span data-ttu-id="66201-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="66201-116">Update Privilege</span></span>  | <span data-ttu-id="66201-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="66201-117">This value is set by the system.</span></span>          |
| <span data-ttu-id="66201-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="66201-118">Update Frequency</span></span>  | <span data-ttu-id="66201-119">Cada vez que el usuario escribe una contraseña incorrecta.</span><span class="sxs-lookup"><span data-stu-id="66201-119">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="66201-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="66201-120">Attribute-Id</span></span>      | <span data-ttu-id="66201-121">1.2.840.113556.1.4.12</span><span class="sxs-lookup"><span data-stu-id="66201-121">1.2.840.113556.1.4.12</span></span>                     |
| <span data-ttu-id="66201-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="66201-122">System-Id-Guid</span></span>    | <span data-ttu-id="66201-123">bf96792e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="66201-123">bf96792e-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="66201-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66201-124">Syntax</span></span>            | [<span data-ttu-id="66201-125">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="66201-125">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="66201-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="66201-126">Implementations</span></span>

-   [<span data-ttu-id="66201-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="66201-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="66201-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="66201-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="66201-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="66201-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="66201-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="66201-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="66201-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="66201-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="66201-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="66201-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="66201-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="66201-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="66201-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66201-134">Windows 2000 Server</span></span>



| <span data-ttu-id="66201-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="66201-135">Entry</span></span> | <span data-ttu-id="66201-136">Value</span><span class="sxs-lookup"><span data-stu-id="66201-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="66201-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66201-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66201-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="66201-139">System-Only</span></span>            | <span data-ttu-id="66201-140">False</span><span class="sxs-lookup"><span data-stu-id="66201-140">False</span></span>                             |
| <span data-ttu-id="66201-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66201-141">Is-Single-Valued</span></span>       | <span data-ttu-id="66201-142">True</span><span class="sxs-lookup"><span data-stu-id="66201-142">True</span></span>                              |
| <span data-ttu-id="66201-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66201-143">Is Indexed</span></span>             | <span data-ttu-id="66201-144">False</span><span class="sxs-lookup"><span data-stu-id="66201-144">False</span></span>                             |
| <span data-ttu-id="66201-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66201-145">In Global Catalog</span></span>      | <span data-ttu-id="66201-146">False</span><span class="sxs-lookup"><span data-stu-id="66201-146">False</span></span>                             |
| <span data-ttu-id="66201-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66201-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="66201-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66201-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="66201-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66201-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="66201-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66201-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="66201-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-151">Search-Flags</span></span>           | <span data-ttu-id="66201-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66201-152">0x00000000</span></span>                        |
| <span data-ttu-id="66201-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-153">System-Flags</span></span>           | <span data-ttu-id="66201-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66201-154">0x00000011</span></span>                        |
| <span data-ttu-id="66201-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66201-155">Classes used in</span></span>        | [<span data-ttu-id="66201-156">**User**</span><span class="sxs-lookup"><span data-stu-id="66201-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="66201-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66201-157">Windows Server 2003</span></span>



| <span data-ttu-id="66201-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="66201-158">Entry</span></span> | <span data-ttu-id="66201-159">Value</span><span class="sxs-lookup"><span data-stu-id="66201-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="66201-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66201-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66201-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="66201-162">System-Only</span></span>            | <span data-ttu-id="66201-163">False</span><span class="sxs-lookup"><span data-stu-id="66201-163">False</span></span>                             |
| <span data-ttu-id="66201-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66201-164">Is-Single-Valued</span></span>       | <span data-ttu-id="66201-165">True</span><span class="sxs-lookup"><span data-stu-id="66201-165">True</span></span>                              |
| <span data-ttu-id="66201-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66201-166">Is Indexed</span></span>             | <span data-ttu-id="66201-167">False</span><span class="sxs-lookup"><span data-stu-id="66201-167">False</span></span>                             |
| <span data-ttu-id="66201-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66201-168">In Global Catalog</span></span>      | <span data-ttu-id="66201-169">False</span><span class="sxs-lookup"><span data-stu-id="66201-169">False</span></span>                             |
| <span data-ttu-id="66201-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66201-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="66201-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66201-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="66201-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66201-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="66201-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66201-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="66201-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-174">Search-Flags</span></span>           | <span data-ttu-id="66201-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66201-175">0x00000000</span></span>                        |
| <span data-ttu-id="66201-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-176">System-Flags</span></span>           | <span data-ttu-id="66201-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66201-177">0x00000011</span></span>                        |
| <span data-ttu-id="66201-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66201-178">Classes used in</span></span>        | [<span data-ttu-id="66201-179">**User**</span><span class="sxs-lookup"><span data-stu-id="66201-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="66201-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="66201-180">ADAM</span></span>



| <span data-ttu-id="66201-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="66201-181">Entry</span></span> | <span data-ttu-id="66201-182">Value</span><span class="sxs-lookup"><span data-stu-id="66201-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="66201-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66201-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="66201-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66201-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="66201-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="66201-185">System-Only</span></span>            | <span data-ttu-id="66201-186">True</span><span class="sxs-lookup"><span data-stu-id="66201-186">True</span></span>                                                              |
| <span data-ttu-id="66201-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66201-187">Is-Single-Valued</span></span>       | <span data-ttu-id="66201-188">True</span><span class="sxs-lookup"><span data-stu-id="66201-188">True</span></span>                                                              |
| <span data-ttu-id="66201-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66201-189">Is Indexed</span></span>             | <span data-ttu-id="66201-190">False</span><span class="sxs-lookup"><span data-stu-id="66201-190">False</span></span>                                                             |
| <span data-ttu-id="66201-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66201-191">In Global Catalog</span></span>      | <span data-ttu-id="66201-192">False</span><span class="sxs-lookup"><span data-stu-id="66201-192">False</span></span>                                                             |
| <span data-ttu-id="66201-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66201-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="66201-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66201-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="66201-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66201-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="66201-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66201-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="66201-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-197">Search-Flags</span></span>           | <span data-ttu-id="66201-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66201-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="66201-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-199">System-Flags</span></span>           | <span data-ttu-id="66201-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66201-200">0x00000011</span></span>                                                        |
| <span data-ttu-id="66201-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66201-201">Classes used in</span></span>        | [<span data-ttu-id="66201-202">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="66201-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="66201-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="66201-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="66201-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="66201-204">Entry</span></span> | <span data-ttu-id="66201-205">Value</span><span class="sxs-lookup"><span data-stu-id="66201-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="66201-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66201-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66201-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="66201-208">System-Only</span></span>            | <span data-ttu-id="66201-209">False</span><span class="sxs-lookup"><span data-stu-id="66201-209">False</span></span>                             |
| <span data-ttu-id="66201-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66201-210">Is-Single-Valued</span></span>       | <span data-ttu-id="66201-211">True</span><span class="sxs-lookup"><span data-stu-id="66201-211">True</span></span>                              |
| <span data-ttu-id="66201-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66201-212">Is Indexed</span></span>             | <span data-ttu-id="66201-213">False</span><span class="sxs-lookup"><span data-stu-id="66201-213">False</span></span>                             |
| <span data-ttu-id="66201-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66201-214">In Global Catalog</span></span>      | <span data-ttu-id="66201-215">False</span><span class="sxs-lookup"><span data-stu-id="66201-215">False</span></span>                             |
| <span data-ttu-id="66201-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66201-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="66201-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66201-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="66201-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66201-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="66201-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66201-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="66201-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-220">Search-Flags</span></span>           | <span data-ttu-id="66201-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66201-221">0x00000000</span></span>                        |
| <span data-ttu-id="66201-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-222">System-Flags</span></span>           | <span data-ttu-id="66201-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66201-223">0x00000011</span></span>                        |
| <span data-ttu-id="66201-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66201-224">Classes used in</span></span>        | [<span data-ttu-id="66201-225">**User**</span><span class="sxs-lookup"><span data-stu-id="66201-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="66201-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66201-226">Windows Server 2008</span></span>



| <span data-ttu-id="66201-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="66201-227">Entry</span></span> | <span data-ttu-id="66201-228">Value</span><span class="sxs-lookup"><span data-stu-id="66201-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="66201-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66201-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66201-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="66201-231">System-Only</span></span>            | <span data-ttu-id="66201-232">False</span><span class="sxs-lookup"><span data-stu-id="66201-232">False</span></span>                             |
| <span data-ttu-id="66201-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66201-233">Is-Single-Valued</span></span>       | <span data-ttu-id="66201-234">True</span><span class="sxs-lookup"><span data-stu-id="66201-234">True</span></span>                              |
| <span data-ttu-id="66201-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66201-235">Is Indexed</span></span>             | <span data-ttu-id="66201-236">False</span><span class="sxs-lookup"><span data-stu-id="66201-236">False</span></span>                             |
| <span data-ttu-id="66201-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66201-237">In Global Catalog</span></span>      | <span data-ttu-id="66201-238">False</span><span class="sxs-lookup"><span data-stu-id="66201-238">False</span></span>                             |
| <span data-ttu-id="66201-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66201-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="66201-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66201-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="66201-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66201-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="66201-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66201-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="66201-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-243">Search-Flags</span></span>           | <span data-ttu-id="66201-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66201-244">0x00000000</span></span>                        |
| <span data-ttu-id="66201-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-245">System-Flags</span></span>           | <span data-ttu-id="66201-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66201-246">0x00000011</span></span>                        |
| <span data-ttu-id="66201-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66201-247">Classes used in</span></span>        | [<span data-ttu-id="66201-248">**User**</span><span class="sxs-lookup"><span data-stu-id="66201-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="66201-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66201-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="66201-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="66201-250">Entry</span></span> | <span data-ttu-id="66201-251">Value</span><span class="sxs-lookup"><span data-stu-id="66201-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="66201-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66201-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66201-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="66201-254">System-Only</span></span>            | <span data-ttu-id="66201-255">False</span><span class="sxs-lookup"><span data-stu-id="66201-255">False</span></span>                             |
| <span data-ttu-id="66201-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66201-256">Is-Single-Valued</span></span>       | <span data-ttu-id="66201-257">True</span><span class="sxs-lookup"><span data-stu-id="66201-257">True</span></span>                              |
| <span data-ttu-id="66201-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66201-258">Is Indexed</span></span>             | <span data-ttu-id="66201-259">False</span><span class="sxs-lookup"><span data-stu-id="66201-259">False</span></span>                             |
| <span data-ttu-id="66201-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66201-260">In Global Catalog</span></span>      | <span data-ttu-id="66201-261">False</span><span class="sxs-lookup"><span data-stu-id="66201-261">False</span></span>                             |
| <span data-ttu-id="66201-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66201-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="66201-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66201-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="66201-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66201-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="66201-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66201-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="66201-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-266">Search-Flags</span></span>           | <span data-ttu-id="66201-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66201-267">0x00000000</span></span>                        |
| <span data-ttu-id="66201-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-268">System-Flags</span></span>           | <span data-ttu-id="66201-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66201-269">0x00000011</span></span>                        |
| <span data-ttu-id="66201-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66201-270">Classes used in</span></span>        | [<span data-ttu-id="66201-271">**User**</span><span class="sxs-lookup"><span data-stu-id="66201-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="66201-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66201-272">Windows Server 2012</span></span>



| <span data-ttu-id="66201-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="66201-273">Entry</span></span> | <span data-ttu-id="66201-274">Value</span><span class="sxs-lookup"><span data-stu-id="66201-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="66201-275">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="66201-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66201-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="66201-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="66201-277">System-Only</span></span>            | <span data-ttu-id="66201-278">False</span><span class="sxs-lookup"><span data-stu-id="66201-278">False</span></span>                             |
| <span data-ttu-id="66201-279">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="66201-279">Is-Single-Valued</span></span>       | <span data-ttu-id="66201-280">True</span><span class="sxs-lookup"><span data-stu-id="66201-280">True</span></span>                              |
| <span data-ttu-id="66201-281">Está indexado</span><span class="sxs-lookup"><span data-stu-id="66201-281">Is Indexed</span></span>             | <span data-ttu-id="66201-282">False</span><span class="sxs-lookup"><span data-stu-id="66201-282">False</span></span>                             |
| <span data-ttu-id="66201-283">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="66201-283">In Global Catalog</span></span>      | <span data-ttu-id="66201-284">False</span><span class="sxs-lookup"><span data-stu-id="66201-284">False</span></span>                             |
| <span data-ttu-id="66201-285">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="66201-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="66201-286">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66201-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="66201-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66201-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="66201-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66201-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="66201-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-289">Search-Flags</span></span>           | <span data-ttu-id="66201-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66201-290">0x00000000</span></span>                        |
| <span data-ttu-id="66201-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66201-291">System-Flags</span></span>           | <span data-ttu-id="66201-292">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66201-292">0x00000011</span></span>                        |
| <span data-ttu-id="66201-293">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="66201-293">Classes used in</span></span>        | [<span data-ttu-id="66201-294">**User**</span><span class="sxs-lookup"><span data-stu-id="66201-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="66201-295">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66201-295">Remarks</span></span>

<span data-ttu-id="66201-296">Este atributo no se replica y se mantiene por separado en cada controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="66201-296">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span>

<span data-ttu-id="66201-297">Este atributo se restablece en un controlador de dominio específico cuando el usuario inicia sesión correctamente en ese controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="66201-297">This attribute is reset on a specific domain controller when the user successfully logs onto that domain controller.</span></span>

 

 






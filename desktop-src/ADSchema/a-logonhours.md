---
title: Logon-Hours atributo)
description: Las horas en las que el usuario puede iniciar sesión en el dominio.
ms.assetid: b97cc8b0-7f26-45c1-b1c9-bae6467bdfb6
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Logon-Hours
- logonHours esquema de AD de atributos
topic_type:
- apiref
api_name:
- Logon-Hours
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f764192ac57efdb1f14d55f691183240f0eddfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493577"
---
# <a name="logon-hours-attribute"></a><span data-ttu-id="731de-105">Logon-Hours atributo)</span><span class="sxs-lookup"><span data-stu-id="731de-105">Logon-Hours attribute</span></span>

<span data-ttu-id="731de-106">Las horas en las que el usuario puede iniciar sesión en el dominio.</span><span class="sxs-lookup"><span data-stu-id="731de-106">The hours that the user is allowed to logon to the domain.</span></span>



| <span data-ttu-id="731de-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="731de-107">Entry</span></span> | <span data-ttu-id="731de-108">Value</span><span class="sxs-lookup"><span data-stu-id="731de-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="731de-109">CN</span><span class="sxs-lookup"><span data-stu-id="731de-109">CN</span></span>                | <span data-ttu-id="731de-110">Logon-Hours</span><span class="sxs-lookup"><span data-stu-id="731de-110">Logon-Hours</span></span>                                           |
| <span data-ttu-id="731de-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="731de-111">Ldap-Display-Name</span></span> | <span data-ttu-id="731de-112">logonHours</span><span class="sxs-lookup"><span data-stu-id="731de-112">logonHours</span></span>                                            |
| <span data-ttu-id="731de-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="731de-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="731de-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="731de-114">Update Privilege</span></span>  | <span data-ttu-id="731de-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="731de-115">Domain administrator</span></span>                                  |
| <span data-ttu-id="731de-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="731de-116">Update Frequency</span></span>  | <span data-ttu-id="731de-117">Siempre que sea necesario cambiar las horas de inicio de sesión de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="731de-117">Whenever the account's logon hours needs to change.</span></span>   |
| <span data-ttu-id="731de-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="731de-118">Attribute-Id</span></span>      | <span data-ttu-id="731de-119">1.2.840.113556.1.4.64</span><span class="sxs-lookup"><span data-stu-id="731de-119">1.2.840.113556.1.4.64</span></span>                                 |
| <span data-ttu-id="731de-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="731de-120">System-Id-Guid</span></span>    | <span data-ttu-id="731de-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="731de-121">bf9679ab-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="731de-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="731de-122">Syntax</span></span>            | [<span data-ttu-id="731de-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="731de-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="731de-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="731de-124">Implementations</span></span>

-   [<span data-ttu-id="731de-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="731de-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="731de-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="731de-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="731de-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="731de-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="731de-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="731de-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="731de-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="731de-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="731de-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="731de-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="731de-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="731de-131">Windows 2000 Server</span></span>



| <span data-ttu-id="731de-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="731de-132">Entry</span></span> | <span data-ttu-id="731de-133">Value</span><span class="sxs-lookup"><span data-stu-id="731de-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="731de-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="731de-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="731de-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="731de-136">System-Only</span></span>            | <span data-ttu-id="731de-137">False</span><span class="sxs-lookup"><span data-stu-id="731de-137">False</span></span>                             |
| <span data-ttu-id="731de-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="731de-138">Is-Single-Valued</span></span>       | <span data-ttu-id="731de-139">True</span><span class="sxs-lookup"><span data-stu-id="731de-139">True</span></span>                              |
| <span data-ttu-id="731de-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="731de-140">Is Indexed</span></span>             | <span data-ttu-id="731de-141">False</span><span class="sxs-lookup"><span data-stu-id="731de-141">False</span></span>                             |
| <span data-ttu-id="731de-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="731de-142">In Global Catalog</span></span>      | <span data-ttu-id="731de-143">False</span><span class="sxs-lookup"><span data-stu-id="731de-143">False</span></span>                             |
| <span data-ttu-id="731de-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="731de-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="731de-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="731de-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="731de-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="731de-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="731de-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="731de-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="731de-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-148">Search-Flags</span></span>           | <span data-ttu-id="731de-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-149">0x00000010</span></span>                        |
| <span data-ttu-id="731de-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-150">System-Flags</span></span>           | <span data-ttu-id="731de-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-151">0x00000010</span></span>                        |
| <span data-ttu-id="731de-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="731de-152">Classes used in</span></span>        | [<span data-ttu-id="731de-153">**User**</span><span class="sxs-lookup"><span data-stu-id="731de-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="731de-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="731de-154">Windows Server 2003</span></span>



| <span data-ttu-id="731de-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="731de-155">Entry</span></span> | <span data-ttu-id="731de-156">Value</span><span class="sxs-lookup"><span data-stu-id="731de-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="731de-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="731de-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="731de-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="731de-159">System-Only</span></span>            | <span data-ttu-id="731de-160">False</span><span class="sxs-lookup"><span data-stu-id="731de-160">False</span></span>                             |
| <span data-ttu-id="731de-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="731de-161">Is-Single-Valued</span></span>       | <span data-ttu-id="731de-162">True</span><span class="sxs-lookup"><span data-stu-id="731de-162">True</span></span>                              |
| <span data-ttu-id="731de-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="731de-163">Is Indexed</span></span>             | <span data-ttu-id="731de-164">False</span><span class="sxs-lookup"><span data-stu-id="731de-164">False</span></span>                             |
| <span data-ttu-id="731de-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="731de-165">In Global Catalog</span></span>      | <span data-ttu-id="731de-166">False</span><span class="sxs-lookup"><span data-stu-id="731de-166">False</span></span>                             |
| <span data-ttu-id="731de-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="731de-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="731de-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="731de-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="731de-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="731de-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="731de-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="731de-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="731de-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-171">Search-Flags</span></span>           | <span data-ttu-id="731de-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-172">0x00000010</span></span>                        |
| <span data-ttu-id="731de-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-173">System-Flags</span></span>           | <span data-ttu-id="731de-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-174">0x00000010</span></span>                        |
| <span data-ttu-id="731de-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="731de-175">Classes used in</span></span>        | [<span data-ttu-id="731de-176">**User**</span><span class="sxs-lookup"><span data-stu-id="731de-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="731de-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="731de-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="731de-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="731de-178">Entry</span></span> | <span data-ttu-id="731de-179">Value</span><span class="sxs-lookup"><span data-stu-id="731de-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="731de-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="731de-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="731de-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="731de-182">System-Only</span></span>            | <span data-ttu-id="731de-183">False</span><span class="sxs-lookup"><span data-stu-id="731de-183">False</span></span>                             |
| <span data-ttu-id="731de-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="731de-184">Is-Single-Valued</span></span>       | <span data-ttu-id="731de-185">True</span><span class="sxs-lookup"><span data-stu-id="731de-185">True</span></span>                              |
| <span data-ttu-id="731de-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="731de-186">Is Indexed</span></span>             | <span data-ttu-id="731de-187">False</span><span class="sxs-lookup"><span data-stu-id="731de-187">False</span></span>                             |
| <span data-ttu-id="731de-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="731de-188">In Global Catalog</span></span>      | <span data-ttu-id="731de-189">False</span><span class="sxs-lookup"><span data-stu-id="731de-189">False</span></span>                             |
| <span data-ttu-id="731de-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="731de-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="731de-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="731de-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="731de-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="731de-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="731de-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="731de-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="731de-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-194">Search-Flags</span></span>           | <span data-ttu-id="731de-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-195">0x00000010</span></span>                        |
| <span data-ttu-id="731de-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-196">System-Flags</span></span>           | <span data-ttu-id="731de-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-197">0x00000010</span></span>                        |
| <span data-ttu-id="731de-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="731de-198">Classes used in</span></span>        | [<span data-ttu-id="731de-199">**User**</span><span class="sxs-lookup"><span data-stu-id="731de-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="731de-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="731de-200">Windows Server 2008</span></span>



| <span data-ttu-id="731de-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="731de-201">Entry</span></span> | <span data-ttu-id="731de-202">Value</span><span class="sxs-lookup"><span data-stu-id="731de-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="731de-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="731de-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="731de-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="731de-205">System-Only</span></span>            | <span data-ttu-id="731de-206">False</span><span class="sxs-lookup"><span data-stu-id="731de-206">False</span></span>                             |
| <span data-ttu-id="731de-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="731de-207">Is-Single-Valued</span></span>       | <span data-ttu-id="731de-208">True</span><span class="sxs-lookup"><span data-stu-id="731de-208">True</span></span>                              |
| <span data-ttu-id="731de-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="731de-209">Is Indexed</span></span>             | <span data-ttu-id="731de-210">False</span><span class="sxs-lookup"><span data-stu-id="731de-210">False</span></span>                             |
| <span data-ttu-id="731de-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="731de-211">In Global Catalog</span></span>      | <span data-ttu-id="731de-212">False</span><span class="sxs-lookup"><span data-stu-id="731de-212">False</span></span>                             |
| <span data-ttu-id="731de-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="731de-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="731de-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="731de-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="731de-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="731de-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="731de-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="731de-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="731de-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-217">Search-Flags</span></span>           | <span data-ttu-id="731de-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-218">0x00000010</span></span>                        |
| <span data-ttu-id="731de-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-219">System-Flags</span></span>           | <span data-ttu-id="731de-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-220">0x00000010</span></span>                        |
| <span data-ttu-id="731de-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="731de-221">Classes used in</span></span>        | [<span data-ttu-id="731de-222">**User**</span><span class="sxs-lookup"><span data-stu-id="731de-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="731de-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="731de-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="731de-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="731de-224">Entry</span></span> | <span data-ttu-id="731de-225">Value</span><span class="sxs-lookup"><span data-stu-id="731de-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="731de-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="731de-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="731de-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="731de-228">System-Only</span></span>            | <span data-ttu-id="731de-229">False</span><span class="sxs-lookup"><span data-stu-id="731de-229">False</span></span>                             |
| <span data-ttu-id="731de-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="731de-230">Is-Single-Valued</span></span>       | <span data-ttu-id="731de-231">True</span><span class="sxs-lookup"><span data-stu-id="731de-231">True</span></span>                              |
| <span data-ttu-id="731de-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="731de-232">Is Indexed</span></span>             | <span data-ttu-id="731de-233">False</span><span class="sxs-lookup"><span data-stu-id="731de-233">False</span></span>                             |
| <span data-ttu-id="731de-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="731de-234">In Global Catalog</span></span>      | <span data-ttu-id="731de-235">False</span><span class="sxs-lookup"><span data-stu-id="731de-235">False</span></span>                             |
| <span data-ttu-id="731de-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="731de-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="731de-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="731de-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="731de-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="731de-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="731de-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="731de-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="731de-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-240">Search-Flags</span></span>           | <span data-ttu-id="731de-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-241">0x00000010</span></span>                        |
| <span data-ttu-id="731de-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-242">System-Flags</span></span>           | <span data-ttu-id="731de-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-243">0x00000010</span></span>                        |
| <span data-ttu-id="731de-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="731de-244">Classes used in</span></span>        | [<span data-ttu-id="731de-245">**User**</span><span class="sxs-lookup"><span data-stu-id="731de-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="731de-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="731de-246">Windows Server 2012</span></span>



| <span data-ttu-id="731de-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="731de-247">Entry</span></span> | <span data-ttu-id="731de-248">Value</span><span class="sxs-lookup"><span data-stu-id="731de-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="731de-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="731de-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="731de-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="731de-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="731de-251">System-Only</span></span>            | <span data-ttu-id="731de-252">False</span><span class="sxs-lookup"><span data-stu-id="731de-252">False</span></span>                             |
| <span data-ttu-id="731de-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="731de-253">Is-Single-Valued</span></span>       | <span data-ttu-id="731de-254">True</span><span class="sxs-lookup"><span data-stu-id="731de-254">True</span></span>                              |
| <span data-ttu-id="731de-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="731de-255">Is Indexed</span></span>             | <span data-ttu-id="731de-256">False</span><span class="sxs-lookup"><span data-stu-id="731de-256">False</span></span>                             |
| <span data-ttu-id="731de-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="731de-257">In Global Catalog</span></span>      | <span data-ttu-id="731de-258">False</span><span class="sxs-lookup"><span data-stu-id="731de-258">False</span></span>                             |
| <span data-ttu-id="731de-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="731de-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="731de-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="731de-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="731de-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="731de-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="731de-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="731de-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="731de-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-263">Search-Flags</span></span>           | <span data-ttu-id="731de-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-264">0x00000010</span></span>                        |
| <span data-ttu-id="731de-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="731de-265">System-Flags</span></span>           | <span data-ttu-id="731de-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="731de-266">0x00000010</span></span>                        |
| <span data-ttu-id="731de-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="731de-267">Classes used in</span></span>        | [<span data-ttu-id="731de-268">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="731de-268">**User**</span></span>](c-user.md)<br/> |



 

 






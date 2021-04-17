---
title: Atributo NT-pwd-History
description: El historial de contraseñas del usuario en el formato unidireccional de Windows NT (OWF). Windows 2000 usa las OWF de Windows NT.
ms.assetid: 7c6a0fe2-561e-43a2-af46-7505e7e13288
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo NT-pwd-History
- ntPwdHistory esquema de AD de atributos
topic_type:
- apiref
api_name:
- Nt-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41ed3196109d13d4fb6cfae7e23be7ffdfb8c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536196"
---
# <a name="nt-pwd-history-attribute"></a><span data-ttu-id="9da93-106">Atributo NT-pwd-History</span><span class="sxs-lookup"><span data-stu-id="9da93-106">Nt-Pwd-History attribute</span></span>

<span data-ttu-id="9da93-107">El historial de contraseñas del usuario en el formato unidireccional de Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="9da93-107">The password history of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="9da93-108">Windows 2000 usa las OWF de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="9da93-108">Windows 2000 uses the Windows NT OWF.</span></span>



| <span data-ttu-id="9da93-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="9da93-109">Entry</span></span> | <span data-ttu-id="9da93-110">Value</span><span class="sxs-lookup"><span data-stu-id="9da93-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9da93-111">CN</span><span class="sxs-lookup"><span data-stu-id="9da93-111">CN</span></span>                | <span data-ttu-id="9da93-112">NT-pwd-History</span><span class="sxs-lookup"><span data-stu-id="9da93-112">Nt-Pwd-History</span></span>                                        |
| <span data-ttu-id="9da93-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="9da93-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9da93-114">ntPwdHistory</span><span class="sxs-lookup"><span data-stu-id="9da93-114">ntPwdHistory</span></span>                                          |
| <span data-ttu-id="9da93-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9da93-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="9da93-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="9da93-116">Update Privilege</span></span>  | <span data-ttu-id="9da93-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="9da93-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="9da93-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="9da93-118">Update Frequency</span></span>  | <span data-ttu-id="9da93-119">Cada vez que el usuario cambia las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="9da93-119">Each time the user changes passwords.</span></span>                 |
| <span data-ttu-id="9da93-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9da93-120">Attribute-Id</span></span>      | <span data-ttu-id="9da93-121">1.2.840.113556.1.4.94</span><span class="sxs-lookup"><span data-stu-id="9da93-121">1.2.840.113556.1.4.94</span></span>                                 |
| <span data-ttu-id="9da93-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9da93-122">System-Id-Guid</span></span>    | <span data-ttu-id="9da93-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9da93-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="9da93-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9da93-124">Syntax</span></span>            | [<span data-ttu-id="9da93-125">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="9da93-125">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="9da93-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="9da93-126">Implementations</span></span>

-   [<span data-ttu-id="9da93-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9da93-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9da93-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9da93-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9da93-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9da93-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9da93-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9da93-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9da93-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9da93-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9da93-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9da93-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9da93-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9da93-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9da93-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9da93-134">Windows 2000 Server</span></span>



| <span data-ttu-id="9da93-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="9da93-135">Entry</span></span> | <span data-ttu-id="9da93-136">Value</span><span class="sxs-lookup"><span data-stu-id="9da93-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9da93-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9da93-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9da93-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="9da93-139">System-Only</span></span>            | <span data-ttu-id="9da93-140">False</span><span class="sxs-lookup"><span data-stu-id="9da93-140">False</span></span>                             |
| <span data-ttu-id="9da93-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9da93-141">Is-Single-Valued</span></span>       | <span data-ttu-id="9da93-142">False</span><span class="sxs-lookup"><span data-stu-id="9da93-142">False</span></span>                             |
| <span data-ttu-id="9da93-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9da93-143">Is Indexed</span></span>             | <span data-ttu-id="9da93-144">False</span><span class="sxs-lookup"><span data-stu-id="9da93-144">False</span></span>                             |
| <span data-ttu-id="9da93-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9da93-145">In Global Catalog</span></span>      | <span data-ttu-id="9da93-146">False</span><span class="sxs-lookup"><span data-stu-id="9da93-146">False</span></span>                             |
| <span data-ttu-id="9da93-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9da93-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="9da93-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9da93-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9da93-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9da93-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9da93-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9da93-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9da93-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-151">Search-Flags</span></span>           | <span data-ttu-id="9da93-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9da93-152">0x00000000</span></span>                        |
| <span data-ttu-id="9da93-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-153">System-Flags</span></span>           | <span data-ttu-id="9da93-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9da93-154">0x00000010</span></span>                        |
| <span data-ttu-id="9da93-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9da93-155">Classes used in</span></span>        | [<span data-ttu-id="9da93-156">**User**</span><span class="sxs-lookup"><span data-stu-id="9da93-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9da93-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9da93-157">Windows Server 2003</span></span>



| <span data-ttu-id="9da93-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="9da93-158">Entry</span></span> | <span data-ttu-id="9da93-159">Value</span><span class="sxs-lookup"><span data-stu-id="9da93-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9da93-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9da93-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9da93-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="9da93-162">System-Only</span></span>            | <span data-ttu-id="9da93-163">False</span><span class="sxs-lookup"><span data-stu-id="9da93-163">False</span></span>                             |
| <span data-ttu-id="9da93-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9da93-164">Is-Single-Valued</span></span>       | <span data-ttu-id="9da93-165">False</span><span class="sxs-lookup"><span data-stu-id="9da93-165">False</span></span>                             |
| <span data-ttu-id="9da93-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9da93-166">Is Indexed</span></span>             | <span data-ttu-id="9da93-167">False</span><span class="sxs-lookup"><span data-stu-id="9da93-167">False</span></span>                             |
| <span data-ttu-id="9da93-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9da93-168">In Global Catalog</span></span>      | <span data-ttu-id="9da93-169">False</span><span class="sxs-lookup"><span data-stu-id="9da93-169">False</span></span>                             |
| <span data-ttu-id="9da93-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9da93-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="9da93-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9da93-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9da93-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9da93-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9da93-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9da93-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9da93-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-174">Search-Flags</span></span>           | <span data-ttu-id="9da93-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9da93-175">0x00000000</span></span>                        |
| <span data-ttu-id="9da93-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-176">System-Flags</span></span>           | <span data-ttu-id="9da93-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9da93-177">0x00000010</span></span>                        |
| <span data-ttu-id="9da93-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9da93-178">Classes used in</span></span>        | [<span data-ttu-id="9da93-179">**User**</span><span class="sxs-lookup"><span data-stu-id="9da93-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9da93-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="9da93-180">ADAM</span></span>



| <span data-ttu-id="9da93-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="9da93-181">Entry</span></span> | <span data-ttu-id="9da93-182">Value</span><span class="sxs-lookup"><span data-stu-id="9da93-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9da93-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9da93-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9da93-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9da93-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9da93-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="9da93-185">System-Only</span></span>            | <span data-ttu-id="9da93-186">False</span><span class="sxs-lookup"><span data-stu-id="9da93-186">False</span></span>                                                             |
| <span data-ttu-id="9da93-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9da93-187">Is-Single-Valued</span></span>       | <span data-ttu-id="9da93-188">False</span><span class="sxs-lookup"><span data-stu-id="9da93-188">False</span></span>                                                             |
| <span data-ttu-id="9da93-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9da93-189">Is Indexed</span></span>             | <span data-ttu-id="9da93-190">False</span><span class="sxs-lookup"><span data-stu-id="9da93-190">False</span></span>                                                             |
| <span data-ttu-id="9da93-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9da93-191">In Global Catalog</span></span>      | <span data-ttu-id="9da93-192">False</span><span class="sxs-lookup"><span data-stu-id="9da93-192">False</span></span>                                                             |
| <span data-ttu-id="9da93-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9da93-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="9da93-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9da93-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9da93-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9da93-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9da93-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9da93-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9da93-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-197">Search-Flags</span></span>           | <span data-ttu-id="9da93-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9da93-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="9da93-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-199">System-Flags</span></span>           | <span data-ttu-id="9da93-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9da93-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="9da93-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9da93-201">Classes used in</span></span>        | [<span data-ttu-id="9da93-202">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="9da93-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9da93-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9da93-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9da93-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="9da93-204">Entry</span></span> | <span data-ttu-id="9da93-205">Value</span><span class="sxs-lookup"><span data-stu-id="9da93-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9da93-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9da93-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9da93-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="9da93-208">System-Only</span></span>            | <span data-ttu-id="9da93-209">False</span><span class="sxs-lookup"><span data-stu-id="9da93-209">False</span></span>                             |
| <span data-ttu-id="9da93-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9da93-210">Is-Single-Valued</span></span>       | <span data-ttu-id="9da93-211">False</span><span class="sxs-lookup"><span data-stu-id="9da93-211">False</span></span>                             |
| <span data-ttu-id="9da93-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9da93-212">Is Indexed</span></span>             | <span data-ttu-id="9da93-213">False</span><span class="sxs-lookup"><span data-stu-id="9da93-213">False</span></span>                             |
| <span data-ttu-id="9da93-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9da93-214">In Global Catalog</span></span>      | <span data-ttu-id="9da93-215">False</span><span class="sxs-lookup"><span data-stu-id="9da93-215">False</span></span>                             |
| <span data-ttu-id="9da93-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9da93-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="9da93-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9da93-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9da93-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9da93-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9da93-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9da93-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9da93-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-220">Search-Flags</span></span>           | <span data-ttu-id="9da93-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9da93-221">0x00000000</span></span>                        |
| <span data-ttu-id="9da93-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-222">System-Flags</span></span>           | <span data-ttu-id="9da93-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9da93-223">0x00000010</span></span>                        |
| <span data-ttu-id="9da93-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9da93-224">Classes used in</span></span>        | [<span data-ttu-id="9da93-225">**User**</span><span class="sxs-lookup"><span data-stu-id="9da93-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9da93-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9da93-226">Windows Server 2008</span></span>



| <span data-ttu-id="9da93-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="9da93-227">Entry</span></span> | <span data-ttu-id="9da93-228">Value</span><span class="sxs-lookup"><span data-stu-id="9da93-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9da93-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9da93-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9da93-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="9da93-231">System-Only</span></span>            | <span data-ttu-id="9da93-232">False</span><span class="sxs-lookup"><span data-stu-id="9da93-232">False</span></span>                             |
| <span data-ttu-id="9da93-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9da93-233">Is-Single-Valued</span></span>       | <span data-ttu-id="9da93-234">False</span><span class="sxs-lookup"><span data-stu-id="9da93-234">False</span></span>                             |
| <span data-ttu-id="9da93-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9da93-235">Is Indexed</span></span>             | <span data-ttu-id="9da93-236">False</span><span class="sxs-lookup"><span data-stu-id="9da93-236">False</span></span>                             |
| <span data-ttu-id="9da93-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9da93-237">In Global Catalog</span></span>      | <span data-ttu-id="9da93-238">False</span><span class="sxs-lookup"><span data-stu-id="9da93-238">False</span></span>                             |
| <span data-ttu-id="9da93-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9da93-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="9da93-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9da93-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9da93-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9da93-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9da93-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9da93-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9da93-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-243">Search-Flags</span></span>           | <span data-ttu-id="9da93-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9da93-244">0x00000000</span></span>                        |
| <span data-ttu-id="9da93-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-245">System-Flags</span></span>           | <span data-ttu-id="9da93-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9da93-246">0x00000010</span></span>                        |
| <span data-ttu-id="9da93-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9da93-247">Classes used in</span></span>        | [<span data-ttu-id="9da93-248">**User**</span><span class="sxs-lookup"><span data-stu-id="9da93-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9da93-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9da93-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9da93-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="9da93-250">Entry</span></span> | <span data-ttu-id="9da93-251">Value</span><span class="sxs-lookup"><span data-stu-id="9da93-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9da93-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9da93-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9da93-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="9da93-254">System-Only</span></span>            | <span data-ttu-id="9da93-255">False</span><span class="sxs-lookup"><span data-stu-id="9da93-255">False</span></span>                             |
| <span data-ttu-id="9da93-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9da93-256">Is-Single-Valued</span></span>       | <span data-ttu-id="9da93-257">False</span><span class="sxs-lookup"><span data-stu-id="9da93-257">False</span></span>                             |
| <span data-ttu-id="9da93-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9da93-258">Is Indexed</span></span>             | <span data-ttu-id="9da93-259">False</span><span class="sxs-lookup"><span data-stu-id="9da93-259">False</span></span>                             |
| <span data-ttu-id="9da93-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9da93-260">In Global Catalog</span></span>      | <span data-ttu-id="9da93-261">False</span><span class="sxs-lookup"><span data-stu-id="9da93-261">False</span></span>                             |
| <span data-ttu-id="9da93-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9da93-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="9da93-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9da93-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9da93-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9da93-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9da93-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9da93-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9da93-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-266">Search-Flags</span></span>           | <span data-ttu-id="9da93-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9da93-267">0x00000000</span></span>                        |
| <span data-ttu-id="9da93-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-268">System-Flags</span></span>           | <span data-ttu-id="9da93-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9da93-269">0x00000010</span></span>                        |
| <span data-ttu-id="9da93-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9da93-270">Classes used in</span></span>        | [<span data-ttu-id="9da93-271">**User**</span><span class="sxs-lookup"><span data-stu-id="9da93-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9da93-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9da93-272">Windows Server 2012</span></span>



| <span data-ttu-id="9da93-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="9da93-273">Entry</span></span> | <span data-ttu-id="9da93-274">Value</span><span class="sxs-lookup"><span data-stu-id="9da93-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9da93-275">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9da93-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9da93-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9da93-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="9da93-277">System-Only</span></span>            | <span data-ttu-id="9da93-278">False</span><span class="sxs-lookup"><span data-stu-id="9da93-278">False</span></span>                             |
| <span data-ttu-id="9da93-279">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9da93-279">Is-Single-Valued</span></span>       | <span data-ttu-id="9da93-280">False</span><span class="sxs-lookup"><span data-stu-id="9da93-280">False</span></span>                             |
| <span data-ttu-id="9da93-281">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9da93-281">Is Indexed</span></span>             | <span data-ttu-id="9da93-282">False</span><span class="sxs-lookup"><span data-stu-id="9da93-282">False</span></span>                             |
| <span data-ttu-id="9da93-283">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9da93-283">In Global Catalog</span></span>      | <span data-ttu-id="9da93-284">False</span><span class="sxs-lookup"><span data-stu-id="9da93-284">False</span></span>                             |
| <span data-ttu-id="9da93-285">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9da93-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="9da93-286">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9da93-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9da93-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9da93-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9da93-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9da93-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9da93-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-289">Search-Flags</span></span>           | <span data-ttu-id="9da93-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9da93-290">0x00000000</span></span>                        |
| <span data-ttu-id="9da93-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9da93-291">System-Flags</span></span>           | <span data-ttu-id="9da93-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9da93-292">0x00000010</span></span>                        |
| <span data-ttu-id="9da93-293">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9da93-293">Classes used in</span></span>        | [<span data-ttu-id="9da93-294">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="9da93-294">**User**</span></span>](c-user.md)<br/> |



 

 






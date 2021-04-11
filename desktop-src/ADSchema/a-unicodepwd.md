---
title: Unicode-Pwd atributo)
description: Contraseña del usuario en formato unidireccional (OWF) de Windows NT. Windows 2000 usa las OWF de Windows NT. Esta propiedad solo la utiliza el sistema operativo. Tenga en cuenta que no puede volver a derivar la contraseña sin cifrar desde el formulario OWF de la contraseña.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Unicode-Pwd
- atributo unicodePwd esquema de AD
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d00a1df180b7a30b56bdf198a78edc77cc99755
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151710"
---
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="f8844-108">Unicode-Pwd atributo)</span><span class="sxs-lookup"><span data-stu-id="f8844-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="f8844-109">Contraseña del usuario en formato unidireccional (OWF) de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="f8844-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="f8844-110">Windows 2000 usa las OWF de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="f8844-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="f8844-111">Esta propiedad solo la utiliza el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f8844-111">This property is used only by the operating system.</span></span> <span data-ttu-id="f8844-112">Tenga en cuenta que no puede volver a derivar la contraseña sin cifrar desde el formulario OWF de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f8844-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="f8844-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8844-113">Entry</span></span> | <span data-ttu-id="f8844-114">Value</span><span class="sxs-lookup"><span data-stu-id="f8844-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f8844-115">CN</span><span class="sxs-lookup"><span data-stu-id="f8844-115">CN</span></span>                | <span data-ttu-id="f8844-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="f8844-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="f8844-117">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f8844-117">Ldap-Display-Name</span></span> | <span data-ttu-id="f8844-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="f8844-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="f8844-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f8844-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="f8844-120">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f8844-120">Update Privilege</span></span>  | <span data-ttu-id="f8844-121">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="f8844-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="f8844-122">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f8844-122">Update Frequency</span></span>  | <span data-ttu-id="f8844-123">Cuando se crea el registro del usuario y cada vez que es necesario cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f8844-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="f8844-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f8844-124">Attribute-Id</span></span>      | <span data-ttu-id="f8844-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="f8844-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="f8844-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f8844-126">System-Id-Guid</span></span>    | <span data-ttu-id="f8844-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f8844-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="f8844-128">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8844-128">Syntax</span></span>            | [<span data-ttu-id="f8844-129">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f8844-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="f8844-130">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f8844-130">Implementations</span></span>

-   [<span data-ttu-id="f8844-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f8844-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f8844-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f8844-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f8844-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f8844-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f8844-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f8844-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f8844-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f8844-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f8844-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f8844-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f8844-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f8844-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f8844-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8844-138">Windows 2000 Server</span></span>



| <span data-ttu-id="f8844-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8844-139">Entry</span></span> | <span data-ttu-id="f8844-140">Value</span><span class="sxs-lookup"><span data-stu-id="f8844-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f8844-141">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f8844-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8844-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8844-143">System-Only</span></span>            | <span data-ttu-id="f8844-144">False</span><span class="sxs-lookup"><span data-stu-id="f8844-144">False</span></span>                             |
| <span data-ttu-id="f8844-145">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f8844-145">Is-Single-Valued</span></span>       | <span data-ttu-id="f8844-146">True</span><span class="sxs-lookup"><span data-stu-id="f8844-146">True</span></span>                              |
| <span data-ttu-id="f8844-147">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f8844-147">Is Indexed</span></span>             | <span data-ttu-id="f8844-148">False</span><span class="sxs-lookup"><span data-stu-id="f8844-148">False</span></span>                             |
| <span data-ttu-id="f8844-149">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8844-149">In Global Catalog</span></span>      | <span data-ttu-id="f8844-150">False</span><span class="sxs-lookup"><span data-stu-id="f8844-150">False</span></span>                             |
| <span data-ttu-id="f8844-151">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f8844-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8844-152">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f8844-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f8844-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8844-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f8844-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8844-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f8844-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-155">Search-Flags</span></span>           | <span data-ttu-id="f8844-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8844-156">0x00000000</span></span>                        |
| <span data-ttu-id="f8844-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-157">System-Flags</span></span>           | <span data-ttu-id="f8844-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8844-158">0x00000010</span></span>                        |
| <span data-ttu-id="f8844-159">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f8844-159">Classes used in</span></span>        | [<span data-ttu-id="f8844-160">**User**</span><span class="sxs-lookup"><span data-stu-id="f8844-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f8844-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8844-161">Windows Server 2003</span></span>



| <span data-ttu-id="f8844-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8844-162">Entry</span></span> | <span data-ttu-id="f8844-163">Value</span><span class="sxs-lookup"><span data-stu-id="f8844-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f8844-164">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f8844-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8844-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8844-166">System-Only</span></span>            | <span data-ttu-id="f8844-167">False</span><span class="sxs-lookup"><span data-stu-id="f8844-167">False</span></span>                             |
| <span data-ttu-id="f8844-168">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f8844-168">Is-Single-Valued</span></span>       | <span data-ttu-id="f8844-169">True</span><span class="sxs-lookup"><span data-stu-id="f8844-169">True</span></span>                              |
| <span data-ttu-id="f8844-170">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f8844-170">Is Indexed</span></span>             | <span data-ttu-id="f8844-171">False</span><span class="sxs-lookup"><span data-stu-id="f8844-171">False</span></span>                             |
| <span data-ttu-id="f8844-172">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8844-172">In Global Catalog</span></span>      | <span data-ttu-id="f8844-173">False</span><span class="sxs-lookup"><span data-stu-id="f8844-173">False</span></span>                             |
| <span data-ttu-id="f8844-174">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f8844-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8844-175">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f8844-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f8844-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8844-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f8844-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8844-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f8844-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-178">Search-Flags</span></span>           | <span data-ttu-id="f8844-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8844-179">0x00000000</span></span>                        |
| <span data-ttu-id="f8844-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-180">System-Flags</span></span>           | <span data-ttu-id="f8844-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8844-181">0x00000010</span></span>                        |
| <span data-ttu-id="f8844-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f8844-182">Classes used in</span></span>        | [<span data-ttu-id="f8844-183">**User**</span><span class="sxs-lookup"><span data-stu-id="f8844-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f8844-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="f8844-184">ADAM</span></span>



| <span data-ttu-id="f8844-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8844-185">Entry</span></span> | <span data-ttu-id="f8844-186">Value</span><span class="sxs-lookup"><span data-stu-id="f8844-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f8844-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f8844-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f8844-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8844-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f8844-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8844-189">System-Only</span></span>            | <span data-ttu-id="f8844-190">False</span><span class="sxs-lookup"><span data-stu-id="f8844-190">False</span></span>                                                             |
| <span data-ttu-id="f8844-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f8844-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f8844-192">True</span><span class="sxs-lookup"><span data-stu-id="f8844-192">True</span></span>                                                              |
| <span data-ttu-id="f8844-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f8844-193">Is Indexed</span></span>             | <span data-ttu-id="f8844-194">False</span><span class="sxs-lookup"><span data-stu-id="f8844-194">False</span></span>                                                             |
| <span data-ttu-id="f8844-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8844-195">In Global Catalog</span></span>      | <span data-ttu-id="f8844-196">False</span><span class="sxs-lookup"><span data-stu-id="f8844-196">False</span></span>                                                             |
| <span data-ttu-id="f8844-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f8844-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8844-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f8844-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f8844-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8844-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f8844-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8844-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f8844-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-201">Search-Flags</span></span>           | <span data-ttu-id="f8844-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8844-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="f8844-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-203">System-Flags</span></span>           | <span data-ttu-id="f8844-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8844-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="f8844-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f8844-205">Classes used in</span></span>        | [<span data-ttu-id="f8844-206">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="f8844-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f8844-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f8844-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f8844-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8844-208">Entry</span></span> | <span data-ttu-id="f8844-209">Value</span><span class="sxs-lookup"><span data-stu-id="f8844-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f8844-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f8844-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8844-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8844-212">System-Only</span></span>            | <span data-ttu-id="f8844-213">False</span><span class="sxs-lookup"><span data-stu-id="f8844-213">False</span></span>                             |
| <span data-ttu-id="f8844-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f8844-214">Is-Single-Valued</span></span>       | <span data-ttu-id="f8844-215">True</span><span class="sxs-lookup"><span data-stu-id="f8844-215">True</span></span>                              |
| <span data-ttu-id="f8844-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f8844-216">Is Indexed</span></span>             | <span data-ttu-id="f8844-217">False</span><span class="sxs-lookup"><span data-stu-id="f8844-217">False</span></span>                             |
| <span data-ttu-id="f8844-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8844-218">In Global Catalog</span></span>      | <span data-ttu-id="f8844-219">False</span><span class="sxs-lookup"><span data-stu-id="f8844-219">False</span></span>                             |
| <span data-ttu-id="f8844-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f8844-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8844-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f8844-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f8844-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8844-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f8844-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8844-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f8844-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-224">Search-Flags</span></span>           | <span data-ttu-id="f8844-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8844-225">0x00000000</span></span>                        |
| <span data-ttu-id="f8844-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-226">System-Flags</span></span>           | <span data-ttu-id="f8844-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8844-227">0x00000010</span></span>                        |
| <span data-ttu-id="f8844-228">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f8844-228">Classes used in</span></span>        | [<span data-ttu-id="f8844-229">**User**</span><span class="sxs-lookup"><span data-stu-id="f8844-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f8844-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8844-230">Windows Server 2008</span></span>



| <span data-ttu-id="f8844-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8844-231">Entry</span></span> | <span data-ttu-id="f8844-232">Value</span><span class="sxs-lookup"><span data-stu-id="f8844-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f8844-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f8844-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8844-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8844-235">System-Only</span></span>            | <span data-ttu-id="f8844-236">False</span><span class="sxs-lookup"><span data-stu-id="f8844-236">False</span></span>                             |
| <span data-ttu-id="f8844-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f8844-237">Is-Single-Valued</span></span>       | <span data-ttu-id="f8844-238">True</span><span class="sxs-lookup"><span data-stu-id="f8844-238">True</span></span>                              |
| <span data-ttu-id="f8844-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f8844-239">Is Indexed</span></span>             | <span data-ttu-id="f8844-240">False</span><span class="sxs-lookup"><span data-stu-id="f8844-240">False</span></span>                             |
| <span data-ttu-id="f8844-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8844-241">In Global Catalog</span></span>      | <span data-ttu-id="f8844-242">False</span><span class="sxs-lookup"><span data-stu-id="f8844-242">False</span></span>                             |
| <span data-ttu-id="f8844-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f8844-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8844-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f8844-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f8844-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8844-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f8844-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8844-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f8844-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-247">Search-Flags</span></span>           | <span data-ttu-id="f8844-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8844-248">0x00000000</span></span>                        |
| <span data-ttu-id="f8844-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-249">System-Flags</span></span>           | <span data-ttu-id="f8844-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8844-250">0x00000010</span></span>                        |
| <span data-ttu-id="f8844-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f8844-251">Classes used in</span></span>        | [<span data-ttu-id="f8844-252">**User**</span><span class="sxs-lookup"><span data-stu-id="f8844-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f8844-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f8844-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f8844-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8844-254">Entry</span></span> | <span data-ttu-id="f8844-255">Value</span><span class="sxs-lookup"><span data-stu-id="f8844-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f8844-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f8844-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8844-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8844-258">System-Only</span></span>            | <span data-ttu-id="f8844-259">False</span><span class="sxs-lookup"><span data-stu-id="f8844-259">False</span></span>                             |
| <span data-ttu-id="f8844-260">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f8844-260">Is-Single-Valued</span></span>       | <span data-ttu-id="f8844-261">True</span><span class="sxs-lookup"><span data-stu-id="f8844-261">True</span></span>                              |
| <span data-ttu-id="f8844-262">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f8844-262">Is Indexed</span></span>             | <span data-ttu-id="f8844-263">False</span><span class="sxs-lookup"><span data-stu-id="f8844-263">False</span></span>                             |
| <span data-ttu-id="f8844-264">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8844-264">In Global Catalog</span></span>      | <span data-ttu-id="f8844-265">False</span><span class="sxs-lookup"><span data-stu-id="f8844-265">False</span></span>                             |
| <span data-ttu-id="f8844-266">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f8844-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8844-267">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f8844-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f8844-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8844-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f8844-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8844-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f8844-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-270">Search-Flags</span></span>           | <span data-ttu-id="f8844-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8844-271">0x00000000</span></span>                        |
| <span data-ttu-id="f8844-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-272">System-Flags</span></span>           | <span data-ttu-id="f8844-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8844-273">0x00000010</span></span>                        |
| <span data-ttu-id="f8844-274">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f8844-274">Classes used in</span></span>        | [<span data-ttu-id="f8844-275">**User**</span><span class="sxs-lookup"><span data-stu-id="f8844-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f8844-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f8844-276">Windows Server 2012</span></span>



| <span data-ttu-id="f8844-277">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8844-277">Entry</span></span> | <span data-ttu-id="f8844-278">Value</span><span class="sxs-lookup"><span data-stu-id="f8844-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f8844-279">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f8844-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8844-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f8844-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8844-281">System-Only</span></span>            | <span data-ttu-id="f8844-282">False</span><span class="sxs-lookup"><span data-stu-id="f8844-282">False</span></span>                             |
| <span data-ttu-id="f8844-283">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f8844-283">Is-Single-Valued</span></span>       | <span data-ttu-id="f8844-284">True</span><span class="sxs-lookup"><span data-stu-id="f8844-284">True</span></span>                              |
| <span data-ttu-id="f8844-285">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f8844-285">Is Indexed</span></span>             | <span data-ttu-id="f8844-286">False</span><span class="sxs-lookup"><span data-stu-id="f8844-286">False</span></span>                             |
| <span data-ttu-id="f8844-287">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8844-287">In Global Catalog</span></span>      | <span data-ttu-id="f8844-288">False</span><span class="sxs-lookup"><span data-stu-id="f8844-288">False</span></span>                             |
| <span data-ttu-id="f8844-289">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f8844-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8844-290">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f8844-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f8844-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8844-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f8844-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8844-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f8844-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-293">Search-Flags</span></span>           | <span data-ttu-id="f8844-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8844-294">0x00000000</span></span>                        |
| <span data-ttu-id="f8844-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8844-295">System-Flags</span></span>           | <span data-ttu-id="f8844-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8844-296">0x00000010</span></span>                        |
| <span data-ttu-id="f8844-297">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f8844-297">Classes used in</span></span>        | [<span data-ttu-id="f8844-298">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="f8844-298">**User**</span></span>](c-user.md)<br/> |



 

 






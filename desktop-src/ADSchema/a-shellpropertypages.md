---
title: Atributo Shell-Property-pages
description: El número de orden y el GUID de las páginas de propiedades para administrar objetos de Active Directory. Se puede tener acceso a estas páginas de propiedades desde el shell de Windows. Para obtener más información, vea el documento extender la interfaz de usuario para objetos de directorio.
ms.assetid: e0edd91b-bdb6-47aa-9be2-8a23a89adb26
ms.tgt_platform: multiple
keywords:
- Shell-propiedad-pages atributo AD Schema
- shellPropertyPages esquema de AD de atributos
topic_type:
- apiref
api_name:
- Shell-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: befad2334a754843fa0ae412565db8c82260f7cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151567"
---
# <a name="shell-property-pages-attribute"></a><span data-ttu-id="80a77-107">Atributo Shell-Property-pages</span><span class="sxs-lookup"><span data-stu-id="80a77-107">Shell-Property-Pages attribute</span></span>

<span data-ttu-id="80a77-108">El número de orden y el GUID de las páginas de propiedades para administrar objetos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="80a77-108">The order number and GUID of property pages for managing Active Directory objects.</span></span> <span data-ttu-id="80a77-109">Se puede tener acceso a estas páginas de propiedades desde el shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="80a77-109">These property pages can be accessed from the Windows shell.</span></span> <span data-ttu-id="80a77-110">Para obtener más información, vea el documento extender la interfaz de usuario para objetos de directorio.</span><span class="sxs-lookup"><span data-stu-id="80a77-110">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="80a77-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="80a77-111">Entry</span></span> | <span data-ttu-id="80a77-112">Value</span><span class="sxs-lookup"><span data-stu-id="80a77-112">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="80a77-113">CN</span><span class="sxs-lookup"><span data-stu-id="80a77-113">CN</span></span>                | <span data-ttu-id="80a77-114">Shell-propiedades-páginas</span><span class="sxs-lookup"><span data-stu-id="80a77-114">Shell-Property-Pages</span></span>                           |
| <span data-ttu-id="80a77-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="80a77-115">Ldap-Display-Name</span></span> | <span data-ttu-id="80a77-116">shellPropertyPages</span><span class="sxs-lookup"><span data-stu-id="80a77-116">shellPropertyPages</span></span>                             |
| <span data-ttu-id="80a77-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="80a77-117">Size</span></span>              | \-                                             |
| <span data-ttu-id="80a77-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="80a77-118">Update Privilege</span></span>  | <span data-ttu-id="80a77-119">Administrador de dominio o desarrollador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="80a77-119">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="80a77-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="80a77-120">Update Frequency</span></span>  | <span data-ttu-id="80a77-121">Siempre que se agrega o se quita una página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="80a77-121">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="80a77-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80a77-122">Attribute-Id</span></span>      | <span data-ttu-id="80a77-123">1.2.840.113556.1.4.563</span><span class="sxs-lookup"><span data-stu-id="80a77-123">1.2.840.113556.1.4.563</span></span>                         |
| <span data-ttu-id="80a77-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="80a77-124">System-Id-Guid</span></span>    | <span data-ttu-id="80a77-125">52458039-ca6a-11d0-AFFF-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="80a77-125">52458039-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="80a77-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80a77-126">Syntax</span></span>            | [<span data-ttu-id="80a77-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="80a77-127">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="80a77-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="80a77-128">Implementations</span></span>

-   [<span data-ttu-id="80a77-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80a77-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80a77-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80a77-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80a77-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80a77-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80a77-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80a77-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80a77-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80a77-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80a77-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80a77-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80a77-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80a77-135">Windows 2000 Server</span></span>



| <span data-ttu-id="80a77-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="80a77-136">Entry</span></span> | <span data-ttu-id="80a77-137">Value</span><span class="sxs-lookup"><span data-stu-id="80a77-137">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="80a77-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80a77-138">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80a77-139">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="80a77-140">System-Only</span></span>            | <span data-ttu-id="80a77-141">False</span><span class="sxs-lookup"><span data-stu-id="80a77-141">False</span></span>                                                      |
| <span data-ttu-id="80a77-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80a77-142">Is-Single-Valued</span></span>       | <span data-ttu-id="80a77-143">False</span><span class="sxs-lookup"><span data-stu-id="80a77-143">False</span></span>                                                      |
| <span data-ttu-id="80a77-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80a77-144">Is Indexed</span></span>             | <span data-ttu-id="80a77-145">False</span><span class="sxs-lookup"><span data-stu-id="80a77-145">False</span></span>                                                      |
| <span data-ttu-id="80a77-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80a77-146">In Global Catalog</span></span>      | <span data-ttu-id="80a77-147">False</span><span class="sxs-lookup"><span data-stu-id="80a77-147">False</span></span>                                                      |
| <span data-ttu-id="80a77-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80a77-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="80a77-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80a77-149">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="80a77-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80a77-150">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80a77-151">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-152">Search-Flags</span></span>           | <span data-ttu-id="80a77-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80a77-153">0x00000000</span></span>                                                 |
| <span data-ttu-id="80a77-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-154">System-Flags</span></span>           | <span data-ttu-id="80a77-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80a77-155">0x00000010</span></span>                                                 |
| <span data-ttu-id="80a77-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80a77-156">Classes used in</span></span>        | [<span data-ttu-id="80a77-157">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="80a77-157">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80a77-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80a77-158">Windows Server 2003</span></span>



| <span data-ttu-id="80a77-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="80a77-159">Entry</span></span> | <span data-ttu-id="80a77-160">Value</span><span class="sxs-lookup"><span data-stu-id="80a77-160">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="80a77-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80a77-161">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80a77-162">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="80a77-163">System-Only</span></span>            | <span data-ttu-id="80a77-164">False</span><span class="sxs-lookup"><span data-stu-id="80a77-164">False</span></span>                                                      |
| <span data-ttu-id="80a77-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80a77-165">Is-Single-Valued</span></span>       | <span data-ttu-id="80a77-166">False</span><span class="sxs-lookup"><span data-stu-id="80a77-166">False</span></span>                                                      |
| <span data-ttu-id="80a77-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80a77-167">Is Indexed</span></span>             | <span data-ttu-id="80a77-168">False</span><span class="sxs-lookup"><span data-stu-id="80a77-168">False</span></span>                                                      |
| <span data-ttu-id="80a77-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80a77-169">In Global Catalog</span></span>      | <span data-ttu-id="80a77-170">False</span><span class="sxs-lookup"><span data-stu-id="80a77-170">False</span></span>                                                      |
| <span data-ttu-id="80a77-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80a77-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="80a77-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80a77-172">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="80a77-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80a77-173">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80a77-174">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-175">Search-Flags</span></span>           | <span data-ttu-id="80a77-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80a77-176">0x00000000</span></span>                                                 |
| <span data-ttu-id="80a77-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-177">System-Flags</span></span>           | <span data-ttu-id="80a77-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80a77-178">0x00000010</span></span>                                                 |
| <span data-ttu-id="80a77-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80a77-179">Classes used in</span></span>        | [<span data-ttu-id="80a77-180">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="80a77-180">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80a77-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80a77-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80a77-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="80a77-182">Entry</span></span> | <span data-ttu-id="80a77-183">Value</span><span class="sxs-lookup"><span data-stu-id="80a77-183">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="80a77-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80a77-184">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80a77-185">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="80a77-186">System-Only</span></span>            | <span data-ttu-id="80a77-187">False</span><span class="sxs-lookup"><span data-stu-id="80a77-187">False</span></span>                                                      |
| <span data-ttu-id="80a77-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80a77-188">Is-Single-Valued</span></span>       | <span data-ttu-id="80a77-189">False</span><span class="sxs-lookup"><span data-stu-id="80a77-189">False</span></span>                                                      |
| <span data-ttu-id="80a77-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80a77-190">Is Indexed</span></span>             | <span data-ttu-id="80a77-191">False</span><span class="sxs-lookup"><span data-stu-id="80a77-191">False</span></span>                                                      |
| <span data-ttu-id="80a77-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80a77-192">In Global Catalog</span></span>      | <span data-ttu-id="80a77-193">False</span><span class="sxs-lookup"><span data-stu-id="80a77-193">False</span></span>                                                      |
| <span data-ttu-id="80a77-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80a77-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="80a77-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80a77-195">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="80a77-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80a77-196">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80a77-197">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-198">Search-Flags</span></span>           | <span data-ttu-id="80a77-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80a77-199">0x00000000</span></span>                                                 |
| <span data-ttu-id="80a77-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-200">System-Flags</span></span>           | <span data-ttu-id="80a77-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80a77-201">0x00000010</span></span>                                                 |
| <span data-ttu-id="80a77-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80a77-202">Classes used in</span></span>        | [<span data-ttu-id="80a77-203">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="80a77-203">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80a77-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80a77-204">Windows Server 2008</span></span>



| <span data-ttu-id="80a77-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="80a77-205">Entry</span></span> | <span data-ttu-id="80a77-206">Value</span><span class="sxs-lookup"><span data-stu-id="80a77-206">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="80a77-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80a77-207">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80a77-208">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="80a77-209">System-Only</span></span>            | <span data-ttu-id="80a77-210">False</span><span class="sxs-lookup"><span data-stu-id="80a77-210">False</span></span>                                                      |
| <span data-ttu-id="80a77-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80a77-211">Is-Single-Valued</span></span>       | <span data-ttu-id="80a77-212">False</span><span class="sxs-lookup"><span data-stu-id="80a77-212">False</span></span>                                                      |
| <span data-ttu-id="80a77-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80a77-213">Is Indexed</span></span>             | <span data-ttu-id="80a77-214">False</span><span class="sxs-lookup"><span data-stu-id="80a77-214">False</span></span>                                                      |
| <span data-ttu-id="80a77-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80a77-215">In Global Catalog</span></span>      | <span data-ttu-id="80a77-216">False</span><span class="sxs-lookup"><span data-stu-id="80a77-216">False</span></span>                                                      |
| <span data-ttu-id="80a77-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80a77-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="80a77-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80a77-218">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="80a77-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80a77-219">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80a77-220">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-221">Search-Flags</span></span>           | <span data-ttu-id="80a77-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80a77-222">0x00000000</span></span>                                                 |
| <span data-ttu-id="80a77-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-223">System-Flags</span></span>           | <span data-ttu-id="80a77-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80a77-224">0x00000010</span></span>                                                 |
| <span data-ttu-id="80a77-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80a77-225">Classes used in</span></span>        | [<span data-ttu-id="80a77-226">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="80a77-226">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80a77-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80a77-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80a77-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="80a77-228">Entry</span></span> | <span data-ttu-id="80a77-229">Value</span><span class="sxs-lookup"><span data-stu-id="80a77-229">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="80a77-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80a77-230">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80a77-231">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="80a77-232">System-Only</span></span>            | <span data-ttu-id="80a77-233">False</span><span class="sxs-lookup"><span data-stu-id="80a77-233">False</span></span>                                                      |
| <span data-ttu-id="80a77-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80a77-234">Is-Single-Valued</span></span>       | <span data-ttu-id="80a77-235">False</span><span class="sxs-lookup"><span data-stu-id="80a77-235">False</span></span>                                                      |
| <span data-ttu-id="80a77-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80a77-236">Is Indexed</span></span>             | <span data-ttu-id="80a77-237">False</span><span class="sxs-lookup"><span data-stu-id="80a77-237">False</span></span>                                                      |
| <span data-ttu-id="80a77-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80a77-238">In Global Catalog</span></span>      | <span data-ttu-id="80a77-239">False</span><span class="sxs-lookup"><span data-stu-id="80a77-239">False</span></span>                                                      |
| <span data-ttu-id="80a77-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80a77-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="80a77-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80a77-241">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="80a77-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80a77-242">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80a77-243">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-244">Search-Flags</span></span>           | <span data-ttu-id="80a77-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80a77-245">0x00000000</span></span>                                                 |
| <span data-ttu-id="80a77-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-246">System-Flags</span></span>           | <span data-ttu-id="80a77-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80a77-247">0x00000010</span></span>                                                 |
| <span data-ttu-id="80a77-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80a77-248">Classes used in</span></span>        | [<span data-ttu-id="80a77-249">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="80a77-249">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80a77-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80a77-250">Windows Server 2012</span></span>



| <span data-ttu-id="80a77-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="80a77-251">Entry</span></span> | <span data-ttu-id="80a77-252">Value</span><span class="sxs-lookup"><span data-stu-id="80a77-252">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="80a77-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="80a77-253">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80a77-254">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="80a77-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="80a77-255">System-Only</span></span>            | <span data-ttu-id="80a77-256">False</span><span class="sxs-lookup"><span data-stu-id="80a77-256">False</span></span>                                                      |
| <span data-ttu-id="80a77-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="80a77-257">Is-Single-Valued</span></span>       | <span data-ttu-id="80a77-258">False</span><span class="sxs-lookup"><span data-stu-id="80a77-258">False</span></span>                                                      |
| <span data-ttu-id="80a77-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="80a77-259">Is Indexed</span></span>             | <span data-ttu-id="80a77-260">False</span><span class="sxs-lookup"><span data-stu-id="80a77-260">False</span></span>                                                      |
| <span data-ttu-id="80a77-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="80a77-261">In Global Catalog</span></span>      | <span data-ttu-id="80a77-262">False</span><span class="sxs-lookup"><span data-stu-id="80a77-262">False</span></span>                                                      |
| <span data-ttu-id="80a77-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="80a77-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="80a77-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80a77-264">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="80a77-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80a77-265">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80a77-266">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="80a77-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-267">Search-Flags</span></span>           | <span data-ttu-id="80a77-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80a77-268">0x00000000</span></span>                                                 |
| <span data-ttu-id="80a77-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80a77-269">System-Flags</span></span>           | <span data-ttu-id="80a77-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80a77-270">0x00000010</span></span>                                                 |
| <span data-ttu-id="80a77-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="80a77-271">Classes used in</span></span>        | [<span data-ttu-id="80a77-272">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="80a77-272">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 






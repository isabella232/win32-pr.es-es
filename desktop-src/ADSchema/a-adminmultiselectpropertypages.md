---
title: Admin-MultiSelect-Property-Pages (atributo)
description: Se trata de un atributo multivalor cuyos valores son un número que representa el orden en el que se agregan las páginas y un GUID de un objeto COM que implementa páginas de propiedades de selección múltiple para el complemento usuarios y equipos de AD.
ms.assetid: b2b4aafe-ac2d-44b3-80eb-910ba9852bb0
ms.tgt_platform: multiple
keywords:
- Admin-MultiSelect-Property-pages atributo AD Schema
- adminMultiselectPropertyPages esquema de AD de atributos
topic_type:
- apiref
api_name:
- Admin-Multiselect-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e653568d4f8f6653e4c7dc939c91a7d3cd8b83c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658675"
---
# <a name="admin-multiselect-property-pages-attribute"></a><span data-ttu-id="4c877-105">Admin-MultiSelect-Property-Pages (atributo)</span><span class="sxs-lookup"><span data-stu-id="4c877-105">Admin-Multiselect-Property-Pages attribute</span></span>

<span data-ttu-id="4c877-106">Se trata de un atributo multivalor cuyos valores son un número que representa el orden en el que se agregan las páginas y un GUID de un objeto COM que implementa páginas de propiedades de selección múltiple para el complemento usuarios y equipos de AD.</span><span class="sxs-lookup"><span data-stu-id="4c877-106">This is a multivalued attribute whose values are a number that represents the order in which the pages are added and a GUID of a COM object that implements multi-select property pages for the AD Users and Computers snap-in.</span></span>



| <span data-ttu-id="4c877-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4c877-107">Entry</span></span> | <span data-ttu-id="4c877-108">Value</span><span class="sxs-lookup"><span data-stu-id="4c877-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c877-109">CN</span><span class="sxs-lookup"><span data-stu-id="4c877-109">CN</span></span>                | <span data-ttu-id="4c877-110">Admin-MultiSelect-Property-pages</span><span class="sxs-lookup"><span data-stu-id="4c877-110">Admin-Multiselect-Property-Pages</span></span>                                                                                                            |
| <span data-ttu-id="4c877-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="4c877-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4c877-112">adminMultiselectPropertyPages</span><span class="sxs-lookup"><span data-stu-id="4c877-112">adminMultiselectPropertyPages</span></span>                                                                                                               |
| <span data-ttu-id="4c877-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="4c877-113">Size</span></span>              | <span data-ttu-id="4c877-114">40 bytes</span><span class="sxs-lookup"><span data-stu-id="4c877-114">40 bytes</span></span>                                                                                                                                    |
| <span data-ttu-id="4c877-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="4c877-115">Update Privilege</span></span>  | <span data-ttu-id="4c877-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="4c877-116">Domain administrator</span></span>                                                                                                                        |
| <span data-ttu-id="4c877-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="4c877-117">Update Frequency</span></span>  | <span data-ttu-id="4c877-118">Solo se actualizará si se ha instalado un servicio como Exchange o Terminal Server que implementa sus propias páginas de propiedades de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="4c877-118">This will only be updated if a service like Exchange or Terminal Server is installed that implements their own multi-select property pages.</span></span> |
| <span data-ttu-id="4c877-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4c877-119">Attribute-Id</span></span>      | <span data-ttu-id="4c877-120">1.2.840.113556.1.4.1690</span><span class="sxs-lookup"><span data-stu-id="4c877-120">1.2.840.113556.1.4.1690</span></span>                                                                                                                     |
| <span data-ttu-id="4c877-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4c877-121">System-Id-Guid</span></span>    | <span data-ttu-id="4c877-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span><span class="sxs-lookup"><span data-stu-id="4c877-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span></span>                                                                                                        |
| <span data-ttu-id="4c877-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c877-123">Syntax</span></span>            | [<span data-ttu-id="4c877-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4c877-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                 |



## <a name="implementations"></a><span data-ttu-id="4c877-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="4c877-125">Implementations</span></span>

-   [<span data-ttu-id="4c877-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4c877-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4c877-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4c877-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4c877-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4c877-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4c877-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4c877-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4c877-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4c877-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4c877-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c877-131">Windows Server 2003</span></span>



| <span data-ttu-id="4c877-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="4c877-132">Entry</span></span> | <span data-ttu-id="4c877-133">Value</span><span class="sxs-lookup"><span data-stu-id="4c877-133">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4c877-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4c877-134">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c877-135">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c877-136">System-Only</span></span>            | <span data-ttu-id="4c877-137">False</span><span class="sxs-lookup"><span data-stu-id="4c877-137">False</span></span>                                                      |
| <span data-ttu-id="4c877-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4c877-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4c877-139">False</span><span class="sxs-lookup"><span data-stu-id="4c877-139">False</span></span>                                                      |
| <span data-ttu-id="4c877-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4c877-140">Is Indexed</span></span>             | <span data-ttu-id="4c877-141">False</span><span class="sxs-lookup"><span data-stu-id="4c877-141">False</span></span>                                                      |
| <span data-ttu-id="4c877-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4c877-142">In Global Catalog</span></span>      | <span data-ttu-id="4c877-143">False</span><span class="sxs-lookup"><span data-stu-id="4c877-143">False</span></span>                                                      |
| <span data-ttu-id="4c877-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4c877-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c877-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c877-145">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4c877-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c877-146">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c877-147">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-148">Search-Flags</span></span>           | <span data-ttu-id="4c877-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c877-149">0x00000000</span></span>                                                 |
| <span data-ttu-id="4c877-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-150">System-Flags</span></span>           | <span data-ttu-id="4c877-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c877-151">0x00000010</span></span>                                                 |
| <span data-ttu-id="4c877-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4c877-152">Classes used in</span></span>        | [<span data-ttu-id="4c877-153">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="4c877-153">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4c877-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4c877-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4c877-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="4c877-155">Entry</span></span> | <span data-ttu-id="4c877-156">Value</span><span class="sxs-lookup"><span data-stu-id="4c877-156">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4c877-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4c877-157">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c877-158">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c877-159">System-Only</span></span>            | <span data-ttu-id="4c877-160">False</span><span class="sxs-lookup"><span data-stu-id="4c877-160">False</span></span>                                                      |
| <span data-ttu-id="4c877-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4c877-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4c877-162">False</span><span class="sxs-lookup"><span data-stu-id="4c877-162">False</span></span>                                                      |
| <span data-ttu-id="4c877-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4c877-163">Is Indexed</span></span>             | <span data-ttu-id="4c877-164">False</span><span class="sxs-lookup"><span data-stu-id="4c877-164">False</span></span>                                                      |
| <span data-ttu-id="4c877-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4c877-165">In Global Catalog</span></span>      | <span data-ttu-id="4c877-166">False</span><span class="sxs-lookup"><span data-stu-id="4c877-166">False</span></span>                                                      |
| <span data-ttu-id="4c877-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4c877-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c877-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c877-168">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4c877-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c877-169">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c877-170">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-171">Search-Flags</span></span>           | <span data-ttu-id="4c877-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c877-172">0x00000000</span></span>                                                 |
| <span data-ttu-id="4c877-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-173">System-Flags</span></span>           | <span data-ttu-id="4c877-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c877-174">0x00000010</span></span>                                                 |
| <span data-ttu-id="4c877-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4c877-175">Classes used in</span></span>        | [<span data-ttu-id="4c877-176">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="4c877-176">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4c877-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c877-177">Windows Server 2008</span></span>



| <span data-ttu-id="4c877-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="4c877-178">Entry</span></span> | <span data-ttu-id="4c877-179">Value</span><span class="sxs-lookup"><span data-stu-id="4c877-179">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4c877-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4c877-180">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c877-181">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c877-182">System-Only</span></span>            | <span data-ttu-id="4c877-183">False</span><span class="sxs-lookup"><span data-stu-id="4c877-183">False</span></span>                                                      |
| <span data-ttu-id="4c877-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4c877-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4c877-185">False</span><span class="sxs-lookup"><span data-stu-id="4c877-185">False</span></span>                                                      |
| <span data-ttu-id="4c877-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4c877-186">Is Indexed</span></span>             | <span data-ttu-id="4c877-187">False</span><span class="sxs-lookup"><span data-stu-id="4c877-187">False</span></span>                                                      |
| <span data-ttu-id="4c877-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4c877-188">In Global Catalog</span></span>      | <span data-ttu-id="4c877-189">False</span><span class="sxs-lookup"><span data-stu-id="4c877-189">False</span></span>                                                      |
| <span data-ttu-id="4c877-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4c877-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c877-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c877-191">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4c877-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c877-192">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c877-193">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-194">Search-Flags</span></span>           | <span data-ttu-id="4c877-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c877-195">0x00000000</span></span>                                                 |
| <span data-ttu-id="4c877-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-196">System-Flags</span></span>           | <span data-ttu-id="4c877-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c877-197">0x00000010</span></span>                                                 |
| <span data-ttu-id="4c877-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4c877-198">Classes used in</span></span>        | [<span data-ttu-id="4c877-199">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="4c877-199">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4c877-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c877-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4c877-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="4c877-201">Entry</span></span> | <span data-ttu-id="4c877-202">Value</span><span class="sxs-lookup"><span data-stu-id="4c877-202">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4c877-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4c877-203">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c877-204">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c877-205">System-Only</span></span>            | <span data-ttu-id="4c877-206">False</span><span class="sxs-lookup"><span data-stu-id="4c877-206">False</span></span>                                                      |
| <span data-ttu-id="4c877-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4c877-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4c877-208">False</span><span class="sxs-lookup"><span data-stu-id="4c877-208">False</span></span>                                                      |
| <span data-ttu-id="4c877-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4c877-209">Is Indexed</span></span>             | <span data-ttu-id="4c877-210">False</span><span class="sxs-lookup"><span data-stu-id="4c877-210">False</span></span>                                                      |
| <span data-ttu-id="4c877-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4c877-211">In Global Catalog</span></span>      | <span data-ttu-id="4c877-212">False</span><span class="sxs-lookup"><span data-stu-id="4c877-212">False</span></span>                                                      |
| <span data-ttu-id="4c877-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4c877-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c877-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c877-214">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4c877-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c877-215">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c877-216">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-217">Search-Flags</span></span>           | <span data-ttu-id="4c877-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c877-218">0x00000000</span></span>                                                 |
| <span data-ttu-id="4c877-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-219">System-Flags</span></span>           | <span data-ttu-id="4c877-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c877-220">0x00000010</span></span>                                                 |
| <span data-ttu-id="4c877-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4c877-221">Classes used in</span></span>        | [<span data-ttu-id="4c877-222">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="4c877-222">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4c877-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c877-223">Windows Server 2012</span></span>



| <span data-ttu-id="4c877-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="4c877-224">Entry</span></span> | <span data-ttu-id="4c877-225">Value</span><span class="sxs-lookup"><span data-stu-id="4c877-225">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="4c877-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4c877-226">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c877-227">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="4c877-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c877-228">System-Only</span></span>            | <span data-ttu-id="4c877-229">False</span><span class="sxs-lookup"><span data-stu-id="4c877-229">False</span></span>                                                      |
| <span data-ttu-id="4c877-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4c877-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4c877-231">False</span><span class="sxs-lookup"><span data-stu-id="4c877-231">False</span></span>                                                      |
| <span data-ttu-id="4c877-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4c877-232">Is Indexed</span></span>             | <span data-ttu-id="4c877-233">False</span><span class="sxs-lookup"><span data-stu-id="4c877-233">False</span></span>                                                      |
| <span data-ttu-id="4c877-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4c877-234">In Global Catalog</span></span>      | <span data-ttu-id="4c877-235">False</span><span class="sxs-lookup"><span data-stu-id="4c877-235">False</span></span>                                                      |
| <span data-ttu-id="4c877-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4c877-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c877-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c877-237">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="4c877-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c877-238">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c877-239">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="4c877-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-240">Search-Flags</span></span>           | <span data-ttu-id="4c877-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4c877-241">0x00000000</span></span>                                                 |
| <span data-ttu-id="4c877-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c877-242">System-Flags</span></span>           | <span data-ttu-id="4c877-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c877-243">0x00000010</span></span>                                                 |
| <span data-ttu-id="4c877-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4c877-244">Classes used in</span></span>        | [<span data-ttu-id="4c877-245">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="4c877-245">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 






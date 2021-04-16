---
title: 'GPC: atributo User-Extension-names'
description: Lo usa el objeto directiva de grupo para las directivas de usuario.
ms.assetid: 3c6fa679-7597-4286-bd79-7a0030212810
ms.tgt_platform: multiple
keywords:
- GPC-User-Extension-names atributo AD Schema
- gPCUserExtensionNames esquema de AD de atributos
topic_type:
- apiref
api_name:
- GPC-User-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12de39539af6ee523838f8081aa04a5d21b8a1d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493516"
---
# <a name="gpc-user-extension-names-attribute"></a><span data-ttu-id="ed29b-105">GPC: atributo User-Extension-names</span><span class="sxs-lookup"><span data-stu-id="ed29b-105">GPC-User-Extension-Names attribute</span></span>

<span data-ttu-id="ed29b-106">Lo usa el objeto directiva de grupo para las directivas de usuario.</span><span class="sxs-lookup"><span data-stu-id="ed29b-106">Used by the Group Policy Object for user policies.</span></span>



| <span data-ttu-id="ed29b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed29b-107">Entry</span></span> | <span data-ttu-id="ed29b-108">Value</span><span class="sxs-lookup"><span data-stu-id="ed29b-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="ed29b-109">CN</span><span class="sxs-lookup"><span data-stu-id="ed29b-109">CN</span></span>                | <span data-ttu-id="ed29b-110">GPC-User-Extension-names</span><span class="sxs-lookup"><span data-stu-id="ed29b-110">GPC-User-Extension-Names</span></span>                                                        |
| <span data-ttu-id="ed29b-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ed29b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ed29b-112">gPCUserExtensionNames</span><span class="sxs-lookup"><span data-stu-id="ed29b-112">gPCUserExtensionNames</span></span>                                                           |
| <span data-ttu-id="ed29b-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ed29b-113">Size</span></span>              | <span data-ttu-id="ed29b-114">Depende del número de extensiones del lado cliente que tienen una directiva en este GPO.</span><span class="sxs-lookup"><span data-stu-id="ed29b-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="ed29b-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ed29b-115">Update Privilege</span></span>  | <span data-ttu-id="ed29b-116">Administrador de dominio o de directivas.</span><span class="sxs-lookup"><span data-stu-id="ed29b-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="ed29b-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ed29b-117">Update Frequency</span></span>  | <span data-ttu-id="ed29b-118">Cada vez que se actualiza un GPO a través de GPE.</span><span class="sxs-lookup"><span data-stu-id="ed29b-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="ed29b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ed29b-119">Attribute-Id</span></span>      | <span data-ttu-id="ed29b-120">1.2.840.113556.1.4.1349</span><span class="sxs-lookup"><span data-stu-id="ed29b-120">1.2.840.113556.1.4.1349</span></span>                                                         |
| <span data-ttu-id="ed29b-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ed29b-121">System-Id-Guid</span></span>    | <span data-ttu-id="ed29b-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="ed29b-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="ed29b-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed29b-123">Syntax</span></span>            | [<span data-ttu-id="ed29b-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ed29b-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="ed29b-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ed29b-125">Implementations</span></span>

-   [<span data-ttu-id="ed29b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ed29b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ed29b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ed29b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ed29b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ed29b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ed29b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ed29b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ed29b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ed29b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ed29b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ed29b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ed29b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ed29b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ed29b-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed29b-133">Entry</span></span> | <span data-ttu-id="ed29b-134">Value</span><span class="sxs-lookup"><span data-stu-id="ed29b-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed29b-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ed29b-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed29b-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed29b-137">System-Only</span></span>            | <span data-ttu-id="ed29b-138">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-138">False</span></span>                                                               |
| <span data-ttu-id="ed29b-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ed29b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ed29b-140">True</span><span class="sxs-lookup"><span data-stu-id="ed29b-140">True</span></span>                                                                |
| <span data-ttu-id="ed29b-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ed29b-141">Is Indexed</span></span>             | <span data-ttu-id="ed29b-142">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-142">False</span></span>                                                               |
| <span data-ttu-id="ed29b-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ed29b-143">In Global Catalog</span></span>      | <span data-ttu-id="ed29b-144">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-144">False</span></span>                                                               |
| <span data-ttu-id="ed29b-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ed29b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed29b-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed29b-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ed29b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed29b-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed29b-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-149">Search-Flags</span></span>           | <span data-ttu-id="ed29b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed29b-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="ed29b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-151">System-Flags</span></span>           | <span data-ttu-id="ed29b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed29b-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="ed29b-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ed29b-153">Classes used in</span></span>        | [<span data-ttu-id="ed29b-154">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="ed29b-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ed29b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ed29b-155">Windows Server 2003</span></span>



| <span data-ttu-id="ed29b-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed29b-156">Entry</span></span> | <span data-ttu-id="ed29b-157">Value</span><span class="sxs-lookup"><span data-stu-id="ed29b-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed29b-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ed29b-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed29b-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed29b-160">System-Only</span></span>            | <span data-ttu-id="ed29b-161">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-161">False</span></span>                                                               |
| <span data-ttu-id="ed29b-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ed29b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ed29b-163">True</span><span class="sxs-lookup"><span data-stu-id="ed29b-163">True</span></span>                                                                |
| <span data-ttu-id="ed29b-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ed29b-164">Is Indexed</span></span>             | <span data-ttu-id="ed29b-165">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-165">False</span></span>                                                               |
| <span data-ttu-id="ed29b-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ed29b-166">In Global Catalog</span></span>      | <span data-ttu-id="ed29b-167">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-167">False</span></span>                                                               |
| <span data-ttu-id="ed29b-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ed29b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed29b-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed29b-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ed29b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed29b-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed29b-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-172">Search-Flags</span></span>           | <span data-ttu-id="ed29b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed29b-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="ed29b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-174">System-Flags</span></span>           | <span data-ttu-id="ed29b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed29b-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="ed29b-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ed29b-176">Classes used in</span></span>        | [<span data-ttu-id="ed29b-177">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="ed29b-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ed29b-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ed29b-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ed29b-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed29b-179">Entry</span></span> | <span data-ttu-id="ed29b-180">Value</span><span class="sxs-lookup"><span data-stu-id="ed29b-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed29b-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ed29b-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed29b-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed29b-183">System-Only</span></span>            | <span data-ttu-id="ed29b-184">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-184">False</span></span>                                                               |
| <span data-ttu-id="ed29b-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ed29b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ed29b-186">True</span><span class="sxs-lookup"><span data-stu-id="ed29b-186">True</span></span>                                                                |
| <span data-ttu-id="ed29b-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ed29b-187">Is Indexed</span></span>             | <span data-ttu-id="ed29b-188">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-188">False</span></span>                                                               |
| <span data-ttu-id="ed29b-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ed29b-189">In Global Catalog</span></span>      | <span data-ttu-id="ed29b-190">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-190">False</span></span>                                                               |
| <span data-ttu-id="ed29b-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ed29b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed29b-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed29b-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ed29b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed29b-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed29b-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-195">Search-Flags</span></span>           | <span data-ttu-id="ed29b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed29b-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="ed29b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-197">System-Flags</span></span>           | <span data-ttu-id="ed29b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed29b-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="ed29b-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ed29b-199">Classes used in</span></span>        | [<span data-ttu-id="ed29b-200">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="ed29b-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ed29b-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed29b-201">Windows Server 2008</span></span>



| <span data-ttu-id="ed29b-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed29b-202">Entry</span></span> | <span data-ttu-id="ed29b-203">Value</span><span class="sxs-lookup"><span data-stu-id="ed29b-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed29b-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ed29b-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed29b-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed29b-206">System-Only</span></span>            | <span data-ttu-id="ed29b-207">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-207">False</span></span>                                                               |
| <span data-ttu-id="ed29b-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ed29b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ed29b-209">True</span><span class="sxs-lookup"><span data-stu-id="ed29b-209">True</span></span>                                                                |
| <span data-ttu-id="ed29b-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ed29b-210">Is Indexed</span></span>             | <span data-ttu-id="ed29b-211">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-211">False</span></span>                                                               |
| <span data-ttu-id="ed29b-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ed29b-212">In Global Catalog</span></span>      | <span data-ttu-id="ed29b-213">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-213">False</span></span>                                                               |
| <span data-ttu-id="ed29b-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ed29b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed29b-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed29b-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ed29b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed29b-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed29b-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-218">Search-Flags</span></span>           | <span data-ttu-id="ed29b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed29b-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="ed29b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-220">System-Flags</span></span>           | <span data-ttu-id="ed29b-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed29b-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="ed29b-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ed29b-222">Classes used in</span></span>        | [<span data-ttu-id="ed29b-223">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="ed29b-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ed29b-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed29b-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ed29b-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed29b-225">Entry</span></span> | <span data-ttu-id="ed29b-226">Value</span><span class="sxs-lookup"><span data-stu-id="ed29b-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed29b-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ed29b-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed29b-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed29b-229">System-Only</span></span>            | <span data-ttu-id="ed29b-230">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-230">False</span></span>                                                               |
| <span data-ttu-id="ed29b-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ed29b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ed29b-232">True</span><span class="sxs-lookup"><span data-stu-id="ed29b-232">True</span></span>                                                                |
| <span data-ttu-id="ed29b-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ed29b-233">Is Indexed</span></span>             | <span data-ttu-id="ed29b-234">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-234">False</span></span>                                                               |
| <span data-ttu-id="ed29b-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ed29b-235">In Global Catalog</span></span>      | <span data-ttu-id="ed29b-236">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-236">False</span></span>                                                               |
| <span data-ttu-id="ed29b-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ed29b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed29b-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed29b-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ed29b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed29b-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed29b-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-241">Search-Flags</span></span>           | <span data-ttu-id="ed29b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed29b-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="ed29b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-243">System-Flags</span></span>           | <span data-ttu-id="ed29b-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed29b-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="ed29b-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ed29b-245">Classes used in</span></span>        | [<span data-ttu-id="ed29b-246">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="ed29b-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ed29b-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed29b-247">Windows Server 2012</span></span>



| <span data-ttu-id="ed29b-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="ed29b-248">Entry</span></span> | <span data-ttu-id="ed29b-249">Value</span><span class="sxs-lookup"><span data-stu-id="ed29b-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed29b-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ed29b-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed29b-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="ed29b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed29b-252">System-Only</span></span>            | <span data-ttu-id="ed29b-253">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-253">False</span></span>                                                               |
| <span data-ttu-id="ed29b-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ed29b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="ed29b-255">True</span><span class="sxs-lookup"><span data-stu-id="ed29b-255">True</span></span>                                                                |
| <span data-ttu-id="ed29b-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ed29b-256">Is Indexed</span></span>             | <span data-ttu-id="ed29b-257">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-257">False</span></span>                                                               |
| <span data-ttu-id="ed29b-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ed29b-258">In Global Catalog</span></span>      | <span data-ttu-id="ed29b-259">False</span><span class="sxs-lookup"><span data-stu-id="ed29b-259">False</span></span>                                                               |
| <span data-ttu-id="ed29b-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ed29b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed29b-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed29b-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="ed29b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed29b-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed29b-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="ed29b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-264">Search-Flags</span></span>           | <span data-ttu-id="ed29b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed29b-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="ed29b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed29b-266">System-Flags</span></span>           | <span data-ttu-id="ed29b-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ed29b-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="ed29b-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ed29b-268">Classes used in</span></span>        | [<span data-ttu-id="ed29b-269">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="ed29b-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 






---
title: GPC-Machine-Extension-names (atributo)
description: Lo usa el objeto directiva de grupo para las directivas de equipo.
ms.assetid: a5e00bf6-d311-4ccd-a2cf-4f7506fec419
ms.tgt_platform: multiple
keywords:
- GPC-Machine-Extension-names atributo AD Schema
- gPCMachineExtensionNames esquema de AD de atributos
topic_type:
- apiref
api_name:
- GPC-Machine-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9d9c1ce435a017bfefe88d728004f619e193f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997477"
---
# <a name="gpc-machine-extension-names-attribute"></a><span data-ttu-id="923f8-105">GPC-Machine-Extension-names (atributo)</span><span class="sxs-lookup"><span data-stu-id="923f8-105">GPC-Machine-Extension-Names attribute</span></span>

<span data-ttu-id="923f8-106">Lo usa el objeto directiva de grupo para las directivas de equipo.</span><span class="sxs-lookup"><span data-stu-id="923f8-106">Used by the Group Policy Object for computer policies.</span></span>



| <span data-ttu-id="923f8-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="923f8-107">Entry</span></span> | <span data-ttu-id="923f8-108">Value</span><span class="sxs-lookup"><span data-stu-id="923f8-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="923f8-109">CN</span><span class="sxs-lookup"><span data-stu-id="923f8-109">CN</span></span>                | <span data-ttu-id="923f8-110">GPC-Machine-Extension-names</span><span class="sxs-lookup"><span data-stu-id="923f8-110">GPC-Machine-Extension-Names</span></span>                                                     |
| <span data-ttu-id="923f8-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="923f8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="923f8-112">gPCMachineExtensionNames</span><span class="sxs-lookup"><span data-stu-id="923f8-112">gPCMachineExtensionNames</span></span>                                                        |
| <span data-ttu-id="923f8-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="923f8-113">Size</span></span>              | <span data-ttu-id="923f8-114">Depende del número de extensiones del lado cliente que tienen una directiva en este GPO.</span><span class="sxs-lookup"><span data-stu-id="923f8-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="923f8-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="923f8-115">Update Privilege</span></span>  | <span data-ttu-id="923f8-116">Administrador de dominio o de directivas.</span><span class="sxs-lookup"><span data-stu-id="923f8-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="923f8-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="923f8-117">Update Frequency</span></span>  | <span data-ttu-id="923f8-118">Cada vez que se actualiza un GPO a través de GPE.</span><span class="sxs-lookup"><span data-stu-id="923f8-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="923f8-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="923f8-119">Attribute-Id</span></span>      | <span data-ttu-id="923f8-120">1.2.840.113556.1.4.1348</span><span class="sxs-lookup"><span data-stu-id="923f8-120">1.2.840.113556.1.4.1348</span></span>                                                         |
| <span data-ttu-id="923f8-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="923f8-121">System-Id-Guid</span></span>    | <span data-ttu-id="923f8-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="923f8-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="923f8-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="923f8-123">Syntax</span></span>            | [<span data-ttu-id="923f8-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="923f8-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="923f8-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="923f8-125">Implementations</span></span>

-   [<span data-ttu-id="923f8-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="923f8-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="923f8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="923f8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="923f8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="923f8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="923f8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="923f8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="923f8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="923f8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="923f8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="923f8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="923f8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="923f8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="923f8-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="923f8-133">Entry</span></span> | <span data-ttu-id="923f8-134">Value</span><span class="sxs-lookup"><span data-stu-id="923f8-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="923f8-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="923f8-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="923f8-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="923f8-137">System-Only</span></span>            | <span data-ttu-id="923f8-138">False</span><span class="sxs-lookup"><span data-stu-id="923f8-138">False</span></span>                                                               |
| <span data-ttu-id="923f8-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="923f8-139">Is-Single-Valued</span></span>       | <span data-ttu-id="923f8-140">True</span><span class="sxs-lookup"><span data-stu-id="923f8-140">True</span></span>                                                                |
| <span data-ttu-id="923f8-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="923f8-141">Is Indexed</span></span>             | <span data-ttu-id="923f8-142">False</span><span class="sxs-lookup"><span data-stu-id="923f8-142">False</span></span>                                                               |
| <span data-ttu-id="923f8-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="923f8-143">In Global Catalog</span></span>      | <span data-ttu-id="923f8-144">False</span><span class="sxs-lookup"><span data-stu-id="923f8-144">False</span></span>                                                               |
| <span data-ttu-id="923f8-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="923f8-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="923f8-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="923f8-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="923f8-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="923f8-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="923f8-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-149">Search-Flags</span></span>           | <span data-ttu-id="923f8-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="923f8-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="923f8-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-151">System-Flags</span></span>           | <span data-ttu-id="923f8-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="923f8-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="923f8-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="923f8-153">Classes used in</span></span>        | [<span data-ttu-id="923f8-154">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="923f8-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="923f8-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="923f8-155">Windows Server 2003</span></span>



| <span data-ttu-id="923f8-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="923f8-156">Entry</span></span> | <span data-ttu-id="923f8-157">Value</span><span class="sxs-lookup"><span data-stu-id="923f8-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="923f8-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="923f8-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="923f8-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="923f8-160">System-Only</span></span>            | <span data-ttu-id="923f8-161">False</span><span class="sxs-lookup"><span data-stu-id="923f8-161">False</span></span>                                                               |
| <span data-ttu-id="923f8-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="923f8-162">Is-Single-Valued</span></span>       | <span data-ttu-id="923f8-163">True</span><span class="sxs-lookup"><span data-stu-id="923f8-163">True</span></span>                                                                |
| <span data-ttu-id="923f8-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="923f8-164">Is Indexed</span></span>             | <span data-ttu-id="923f8-165">False</span><span class="sxs-lookup"><span data-stu-id="923f8-165">False</span></span>                                                               |
| <span data-ttu-id="923f8-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="923f8-166">In Global Catalog</span></span>      | <span data-ttu-id="923f8-167">False</span><span class="sxs-lookup"><span data-stu-id="923f8-167">False</span></span>                                                               |
| <span data-ttu-id="923f8-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="923f8-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="923f8-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="923f8-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="923f8-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="923f8-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="923f8-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-172">Search-Flags</span></span>           | <span data-ttu-id="923f8-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="923f8-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="923f8-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-174">System-Flags</span></span>           | <span data-ttu-id="923f8-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="923f8-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="923f8-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="923f8-176">Classes used in</span></span>        | [<span data-ttu-id="923f8-177">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="923f8-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="923f8-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="923f8-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="923f8-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="923f8-179">Entry</span></span> | <span data-ttu-id="923f8-180">Value</span><span class="sxs-lookup"><span data-stu-id="923f8-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="923f8-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="923f8-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="923f8-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="923f8-183">System-Only</span></span>            | <span data-ttu-id="923f8-184">False</span><span class="sxs-lookup"><span data-stu-id="923f8-184">False</span></span>                                                               |
| <span data-ttu-id="923f8-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="923f8-185">Is-Single-Valued</span></span>       | <span data-ttu-id="923f8-186">True</span><span class="sxs-lookup"><span data-stu-id="923f8-186">True</span></span>                                                                |
| <span data-ttu-id="923f8-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="923f8-187">Is Indexed</span></span>             | <span data-ttu-id="923f8-188">False</span><span class="sxs-lookup"><span data-stu-id="923f8-188">False</span></span>                                                               |
| <span data-ttu-id="923f8-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="923f8-189">In Global Catalog</span></span>      | <span data-ttu-id="923f8-190">False</span><span class="sxs-lookup"><span data-stu-id="923f8-190">False</span></span>                                                               |
| <span data-ttu-id="923f8-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="923f8-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="923f8-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="923f8-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="923f8-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="923f8-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="923f8-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-195">Search-Flags</span></span>           | <span data-ttu-id="923f8-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="923f8-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="923f8-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-197">System-Flags</span></span>           | <span data-ttu-id="923f8-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="923f8-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="923f8-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="923f8-199">Classes used in</span></span>        | [<span data-ttu-id="923f8-200">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="923f8-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="923f8-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="923f8-201">Windows Server 2008</span></span>



| <span data-ttu-id="923f8-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="923f8-202">Entry</span></span> | <span data-ttu-id="923f8-203">Value</span><span class="sxs-lookup"><span data-stu-id="923f8-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="923f8-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="923f8-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="923f8-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="923f8-206">System-Only</span></span>            | <span data-ttu-id="923f8-207">False</span><span class="sxs-lookup"><span data-stu-id="923f8-207">False</span></span>                                                               |
| <span data-ttu-id="923f8-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="923f8-208">Is-Single-Valued</span></span>       | <span data-ttu-id="923f8-209">True</span><span class="sxs-lookup"><span data-stu-id="923f8-209">True</span></span>                                                                |
| <span data-ttu-id="923f8-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="923f8-210">Is Indexed</span></span>             | <span data-ttu-id="923f8-211">False</span><span class="sxs-lookup"><span data-stu-id="923f8-211">False</span></span>                                                               |
| <span data-ttu-id="923f8-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="923f8-212">In Global Catalog</span></span>      | <span data-ttu-id="923f8-213">False</span><span class="sxs-lookup"><span data-stu-id="923f8-213">False</span></span>                                                               |
| <span data-ttu-id="923f8-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="923f8-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="923f8-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="923f8-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="923f8-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="923f8-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="923f8-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-218">Search-Flags</span></span>           | <span data-ttu-id="923f8-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="923f8-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="923f8-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-220">System-Flags</span></span>           | <span data-ttu-id="923f8-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="923f8-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="923f8-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="923f8-222">Classes used in</span></span>        | [<span data-ttu-id="923f8-223">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="923f8-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="923f8-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="923f8-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="923f8-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="923f8-225">Entry</span></span> | <span data-ttu-id="923f8-226">Value</span><span class="sxs-lookup"><span data-stu-id="923f8-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="923f8-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="923f8-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="923f8-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="923f8-229">System-Only</span></span>            | <span data-ttu-id="923f8-230">False</span><span class="sxs-lookup"><span data-stu-id="923f8-230">False</span></span>                                                               |
| <span data-ttu-id="923f8-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="923f8-231">Is-Single-Valued</span></span>       | <span data-ttu-id="923f8-232">True</span><span class="sxs-lookup"><span data-stu-id="923f8-232">True</span></span>                                                                |
| <span data-ttu-id="923f8-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="923f8-233">Is Indexed</span></span>             | <span data-ttu-id="923f8-234">False</span><span class="sxs-lookup"><span data-stu-id="923f8-234">False</span></span>                                                               |
| <span data-ttu-id="923f8-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="923f8-235">In Global Catalog</span></span>      | <span data-ttu-id="923f8-236">False</span><span class="sxs-lookup"><span data-stu-id="923f8-236">False</span></span>                                                               |
| <span data-ttu-id="923f8-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="923f8-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="923f8-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="923f8-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="923f8-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="923f8-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="923f8-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-241">Search-Flags</span></span>           | <span data-ttu-id="923f8-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="923f8-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="923f8-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-243">System-Flags</span></span>           | <span data-ttu-id="923f8-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="923f8-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="923f8-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="923f8-245">Classes used in</span></span>        | [<span data-ttu-id="923f8-246">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="923f8-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="923f8-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="923f8-247">Windows Server 2012</span></span>



| <span data-ttu-id="923f8-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="923f8-248">Entry</span></span> | <span data-ttu-id="923f8-249">Value</span><span class="sxs-lookup"><span data-stu-id="923f8-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="923f8-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="923f8-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="923f8-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="923f8-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="923f8-252">System-Only</span></span>            | <span data-ttu-id="923f8-253">False</span><span class="sxs-lookup"><span data-stu-id="923f8-253">False</span></span>                                                               |
| <span data-ttu-id="923f8-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="923f8-254">Is-Single-Valued</span></span>       | <span data-ttu-id="923f8-255">True</span><span class="sxs-lookup"><span data-stu-id="923f8-255">True</span></span>                                                                |
| <span data-ttu-id="923f8-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="923f8-256">Is Indexed</span></span>             | <span data-ttu-id="923f8-257">False</span><span class="sxs-lookup"><span data-stu-id="923f8-257">False</span></span>                                                               |
| <span data-ttu-id="923f8-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="923f8-258">In Global Catalog</span></span>      | <span data-ttu-id="923f8-259">False</span><span class="sxs-lookup"><span data-stu-id="923f8-259">False</span></span>                                                               |
| <span data-ttu-id="923f8-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="923f8-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="923f8-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="923f8-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="923f8-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="923f8-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="923f8-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="923f8-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-264">Search-Flags</span></span>           | <span data-ttu-id="923f8-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="923f8-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="923f8-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="923f8-266">System-Flags</span></span>           | <span data-ttu-id="923f8-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="923f8-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="923f8-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="923f8-268">Classes used in</span></span>        | [<span data-ttu-id="923f8-269">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="923f8-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 






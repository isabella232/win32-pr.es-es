---
title: GPC-WQL-Filter (atributo)
description: Se utiliza para almacenar una cadena que contiene un GUID para el filtro y una ruta de acceso del espacio de nombres WMI.
ms.assetid: ea76239b-79e2-49b2-a848-a924450d332a
ms.tgt_platform: multiple
keywords:
- GPC-WQL-esquema de AD de atributos de filtro
- gPCWQLFilter esquema de AD de atributos
topic_type:
- apiref
api_name:
- GPC-WQL-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9a6b8d3715c1692e93579d3c94cdfa44f4192e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906081"
---
# <a name="gpc-wql-filter-attribute"></a><span data-ttu-id="11c02-105">GPC-WQL-Filter (atributo)</span><span class="sxs-lookup"><span data-stu-id="11c02-105">GPC-WQL-Filter attribute</span></span>

<span data-ttu-id="11c02-106">Se utiliza para almacenar una cadena que contiene un GUID para el filtro y una ruta de acceso del espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="11c02-106">Used to store a string that contains a GUID for the filter and a WMI namespace path.</span></span>



| <span data-ttu-id="11c02-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="11c02-107">Entry</span></span> | <span data-ttu-id="11c02-108">Value</span><span class="sxs-lookup"><span data-stu-id="11c02-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="11c02-109">CN</span><span class="sxs-lookup"><span data-stu-id="11c02-109">CN</span></span>                | <span data-ttu-id="11c02-110">GPC-WQL-filtro</span><span class="sxs-lookup"><span data-stu-id="11c02-110">GPC-WQL-Filter</span></span>                                                                  |
| <span data-ttu-id="11c02-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="11c02-111">Ldap-Display-Name</span></span> | <span data-ttu-id="11c02-112">gPCWQLFilter</span><span class="sxs-lookup"><span data-stu-id="11c02-112">gPCWQLFilter</span></span>                                                                    |
| <span data-ttu-id="11c02-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="11c02-113">Size</span></span>              | \-                                                                              |
| <span data-ttu-id="11c02-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="11c02-114">Update Privilege</span></span>  | <span data-ttu-id="11c02-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="11c02-115">Domain administrator</span></span>                                                            |
| <span data-ttu-id="11c02-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="11c02-116">Update Frequency</span></span>  | <span data-ttu-id="11c02-117">Solo cuando el administrador cambia la propiedad de filtro en la interfaz de usuario de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="11c02-117">Only when the administrator changes the filter property in the Group Policy UI.</span></span> |
| <span data-ttu-id="11c02-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="11c02-118">Attribute-Id</span></span>      | <span data-ttu-id="11c02-119">1.2.840.113556.1.4.1694</span><span class="sxs-lookup"><span data-stu-id="11c02-119">1.2.840.113556.1.4.1694</span></span>                                                         |
| <span data-ttu-id="11c02-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="11c02-120">System-Id-Guid</span></span>    | <span data-ttu-id="11c02-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span><span class="sxs-lookup"><span data-stu-id="11c02-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span></span>                                            |
| <span data-ttu-id="11c02-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11c02-122">Syntax</span></span>            | [<span data-ttu-id="11c02-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="11c02-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="11c02-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="11c02-124">Implementations</span></span>

-   [<span data-ttu-id="11c02-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="11c02-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="11c02-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="11c02-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="11c02-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="11c02-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="11c02-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="11c02-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="11c02-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="11c02-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="11c02-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11c02-130">Windows Server 2003</span></span>



| <span data-ttu-id="11c02-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="11c02-131">Entry</span></span> | <span data-ttu-id="11c02-132">Value</span><span class="sxs-lookup"><span data-stu-id="11c02-132">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="11c02-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11c02-133">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c02-134">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c02-135">System-Only</span></span>            | <span data-ttu-id="11c02-136">False</span><span class="sxs-lookup"><span data-stu-id="11c02-136">False</span></span>                                                               |
| <span data-ttu-id="11c02-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11c02-137">Is-Single-Valued</span></span>       | <span data-ttu-id="11c02-138">True</span><span class="sxs-lookup"><span data-stu-id="11c02-138">True</span></span>                                                                |
| <span data-ttu-id="11c02-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11c02-139">Is Indexed</span></span>             | <span data-ttu-id="11c02-140">False</span><span class="sxs-lookup"><span data-stu-id="11c02-140">False</span></span>                                                               |
| <span data-ttu-id="11c02-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11c02-141">In Global Catalog</span></span>      | <span data-ttu-id="11c02-142">False</span><span class="sxs-lookup"><span data-stu-id="11c02-142">False</span></span>                                                               |
| <span data-ttu-id="11c02-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11c02-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c02-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11c02-144">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="11c02-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c02-145">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c02-146">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-147">Search-Flags</span></span>           | <span data-ttu-id="11c02-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c02-148">0x00000000</span></span>                                                          |
| <span data-ttu-id="11c02-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-149">System-Flags</span></span>           | <span data-ttu-id="11c02-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c02-150">0x00000010</span></span>                                                          |
| <span data-ttu-id="11c02-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11c02-151">Classes used in</span></span>        | [<span data-ttu-id="11c02-152">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="11c02-152">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="11c02-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="11c02-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="11c02-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="11c02-154">Entry</span></span> | <span data-ttu-id="11c02-155">Value</span><span class="sxs-lookup"><span data-stu-id="11c02-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="11c02-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11c02-156">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c02-157">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c02-158">System-Only</span></span>            | <span data-ttu-id="11c02-159">False</span><span class="sxs-lookup"><span data-stu-id="11c02-159">False</span></span>                                                               |
| <span data-ttu-id="11c02-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11c02-160">Is-Single-Valued</span></span>       | <span data-ttu-id="11c02-161">True</span><span class="sxs-lookup"><span data-stu-id="11c02-161">True</span></span>                                                                |
| <span data-ttu-id="11c02-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11c02-162">Is Indexed</span></span>             | <span data-ttu-id="11c02-163">False</span><span class="sxs-lookup"><span data-stu-id="11c02-163">False</span></span>                                                               |
| <span data-ttu-id="11c02-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11c02-164">In Global Catalog</span></span>      | <span data-ttu-id="11c02-165">False</span><span class="sxs-lookup"><span data-stu-id="11c02-165">False</span></span>                                                               |
| <span data-ttu-id="11c02-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11c02-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c02-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11c02-167">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="11c02-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c02-168">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c02-169">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-170">Search-Flags</span></span>           | <span data-ttu-id="11c02-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c02-171">0x00000000</span></span>                                                          |
| <span data-ttu-id="11c02-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-172">System-Flags</span></span>           | <span data-ttu-id="11c02-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c02-173">0x00000010</span></span>                                                          |
| <span data-ttu-id="11c02-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11c02-174">Classes used in</span></span>        | [<span data-ttu-id="11c02-175">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="11c02-175">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="11c02-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11c02-176">Windows Server 2008</span></span>



| <span data-ttu-id="11c02-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="11c02-177">Entry</span></span> | <span data-ttu-id="11c02-178">Value</span><span class="sxs-lookup"><span data-stu-id="11c02-178">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="11c02-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11c02-179">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c02-180">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c02-181">System-Only</span></span>            | <span data-ttu-id="11c02-182">False</span><span class="sxs-lookup"><span data-stu-id="11c02-182">False</span></span>                                                               |
| <span data-ttu-id="11c02-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11c02-183">Is-Single-Valued</span></span>       | <span data-ttu-id="11c02-184">True</span><span class="sxs-lookup"><span data-stu-id="11c02-184">True</span></span>                                                                |
| <span data-ttu-id="11c02-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11c02-185">Is Indexed</span></span>             | <span data-ttu-id="11c02-186">False</span><span class="sxs-lookup"><span data-stu-id="11c02-186">False</span></span>                                                               |
| <span data-ttu-id="11c02-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11c02-187">In Global Catalog</span></span>      | <span data-ttu-id="11c02-188">False</span><span class="sxs-lookup"><span data-stu-id="11c02-188">False</span></span>                                                               |
| <span data-ttu-id="11c02-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11c02-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c02-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11c02-190">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="11c02-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c02-191">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c02-192">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-193">Search-Flags</span></span>           | <span data-ttu-id="11c02-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c02-194">0x00000000</span></span>                                                          |
| <span data-ttu-id="11c02-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-195">System-Flags</span></span>           | <span data-ttu-id="11c02-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c02-196">0x00000010</span></span>                                                          |
| <span data-ttu-id="11c02-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11c02-197">Classes used in</span></span>        | [<span data-ttu-id="11c02-198">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="11c02-198">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="11c02-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11c02-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="11c02-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="11c02-200">Entry</span></span> | <span data-ttu-id="11c02-201">Value</span><span class="sxs-lookup"><span data-stu-id="11c02-201">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="11c02-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11c02-202">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c02-203">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c02-204">System-Only</span></span>            | <span data-ttu-id="11c02-205">False</span><span class="sxs-lookup"><span data-stu-id="11c02-205">False</span></span>                                                               |
| <span data-ttu-id="11c02-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11c02-206">Is-Single-Valued</span></span>       | <span data-ttu-id="11c02-207">True</span><span class="sxs-lookup"><span data-stu-id="11c02-207">True</span></span>                                                                |
| <span data-ttu-id="11c02-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11c02-208">Is Indexed</span></span>             | <span data-ttu-id="11c02-209">False</span><span class="sxs-lookup"><span data-stu-id="11c02-209">False</span></span>                                                               |
| <span data-ttu-id="11c02-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11c02-210">In Global Catalog</span></span>      | <span data-ttu-id="11c02-211">False</span><span class="sxs-lookup"><span data-stu-id="11c02-211">False</span></span>                                                               |
| <span data-ttu-id="11c02-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11c02-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c02-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11c02-213">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="11c02-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c02-214">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c02-215">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-216">Search-Flags</span></span>           | <span data-ttu-id="11c02-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c02-217">0x00000000</span></span>                                                          |
| <span data-ttu-id="11c02-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-218">System-Flags</span></span>           | <span data-ttu-id="11c02-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c02-219">0x00000010</span></span>                                                          |
| <span data-ttu-id="11c02-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11c02-220">Classes used in</span></span>        | [<span data-ttu-id="11c02-221">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="11c02-221">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="11c02-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11c02-222">Windows Server 2012</span></span>



| <span data-ttu-id="11c02-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="11c02-223">Entry</span></span> | <span data-ttu-id="11c02-224">Value</span><span class="sxs-lookup"><span data-stu-id="11c02-224">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="11c02-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="11c02-225">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11c02-226">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="11c02-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="11c02-227">System-Only</span></span>            | <span data-ttu-id="11c02-228">False</span><span class="sxs-lookup"><span data-stu-id="11c02-228">False</span></span>                                                               |
| <span data-ttu-id="11c02-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="11c02-229">Is-Single-Valued</span></span>       | <span data-ttu-id="11c02-230">True</span><span class="sxs-lookup"><span data-stu-id="11c02-230">True</span></span>                                                                |
| <span data-ttu-id="11c02-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="11c02-231">Is Indexed</span></span>             | <span data-ttu-id="11c02-232">False</span><span class="sxs-lookup"><span data-stu-id="11c02-232">False</span></span>                                                               |
| <span data-ttu-id="11c02-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="11c02-233">In Global Catalog</span></span>      | <span data-ttu-id="11c02-234">False</span><span class="sxs-lookup"><span data-stu-id="11c02-234">False</span></span>                                                               |
| <span data-ttu-id="11c02-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="11c02-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="11c02-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="11c02-236">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="11c02-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11c02-237">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11c02-238">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="11c02-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-239">Search-Flags</span></span>           | <span data-ttu-id="11c02-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11c02-240">0x00000000</span></span>                                                          |
| <span data-ttu-id="11c02-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11c02-241">System-Flags</span></span>           | <span data-ttu-id="11c02-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11c02-242">0x00000010</span></span>                                                          |
| <span data-ttu-id="11c02-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="11c02-243">Classes used in</span></span>        | [<span data-ttu-id="11c02-244">**Contenedor de directivas de grupo**</span><span class="sxs-lookup"><span data-stu-id="11c02-244">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 






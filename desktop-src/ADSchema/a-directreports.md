---
title: Atributo Reports
description: Contiene la lista de usuarios que notifican directamente al usuario. Los usuarios que aparecen como informes son aquellos que tienen la propiedad administrador de propiedades establecida en este usuario. Cada elemento de la lista es una referencia vinculada al objeto que representa al usuario.
ms.assetid: 369fc457-685c-4875-aed3-0a246a219512
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de informes
- directReports esquema de AD de atributos
topic_type:
- apiref
api_name:
- Reports
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef5a555b7c1d48fdb337f2c876abf3f15ae8daa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659190"
---
# <a name="reports-attribute"></a><span data-ttu-id="a960c-107">Atributo Reports</span><span class="sxs-lookup"><span data-stu-id="a960c-107">Reports attribute</span></span>

<span data-ttu-id="a960c-108">Contiene la lista de usuarios que notifican directamente al usuario.</span><span class="sxs-lookup"><span data-stu-id="a960c-108">Contains the list of users that directly report to the user.</span></span> <span data-ttu-id="a960c-109">Los usuarios que aparecen como informes son aquellos que tienen la propiedad administrador de propiedades establecida en este usuario.</span><span class="sxs-lookup"><span data-stu-id="a960c-109">The users listed as reports are those that have the property manager property set to this user.</span></span> <span data-ttu-id="a960c-110">Cada elemento de la lista es una referencia vinculada al objeto que representa al usuario.</span><span class="sxs-lookup"><span data-stu-id="a960c-110">Each item in the list is a linked reference to the object that represents the user.</span></span>



| <span data-ttu-id="a960c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="a960c-111">Entry</span></span> | <span data-ttu-id="a960c-112">Value</span><span class="sxs-lookup"><span data-stu-id="a960c-112">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="a960c-113">CN</span><span class="sxs-lookup"><span data-stu-id="a960c-113">CN</span></span>                | <span data-ttu-id="a960c-114">Informes</span><span class="sxs-lookup"><span data-stu-id="a960c-114">Reports</span></span>                                         |
| <span data-ttu-id="a960c-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a960c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="a960c-116">directReports</span><span class="sxs-lookup"><span data-stu-id="a960c-116">directReports</span></span>                                   |
| <span data-ttu-id="a960c-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a960c-117">Size</span></span>              | \-                                              |
| <span data-ttu-id="a960c-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a960c-118">Update Privilege</span></span>  | <span data-ttu-id="a960c-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a960c-119">This value is set by the system.</span></span>                |
| <span data-ttu-id="a960c-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a960c-120">Update Frequency</span></span>  | <span data-ttu-id="a960c-121">Siempre que los informes directos para un usuario cambien.</span><span class="sxs-lookup"><span data-stu-id="a960c-121">Whenever the direct reports for a user changes.</span></span> |
| <span data-ttu-id="a960c-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a960c-122">Attribute-Id</span></span>      | <span data-ttu-id="a960c-123">1.2.840.113556.1.2.436</span><span class="sxs-lookup"><span data-stu-id="a960c-123">1.2.840.113556.1.2.436</span></span>                          |
| <span data-ttu-id="a960c-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a960c-124">System-Id-Guid</span></span>    | <span data-ttu-id="a960c-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a960c-125">bf967a1c-0de6-11d0-a285-00aa003049e2</span></span>            |
| <span data-ttu-id="a960c-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a960c-126">Syntax</span></span>            | [<span data-ttu-id="a960c-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a960c-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)         |



## <a name="implementations"></a><span data-ttu-id="a960c-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a960c-128">Implementations</span></span>

-   [<span data-ttu-id="a960c-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a960c-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a960c-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a960c-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a960c-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a960c-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a960c-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a960c-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a960c-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a960c-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a960c-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a960c-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a960c-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a960c-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a960c-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="a960c-136">Entry</span></span> | <span data-ttu-id="a960c-137">Value</span><span class="sxs-lookup"><span data-stu-id="a960c-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a960c-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a960c-138">Link-Id</span></span>                | <span data-ttu-id="a960c-139">43</span><span class="sxs-lookup"><span data-stu-id="a960c-139">43</span></span>                              |
| <span data-ttu-id="a960c-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a960c-140">MAPI-Id</span></span>                | <span data-ttu-id="a960c-141">0x800E</span><span class="sxs-lookup"><span data-stu-id="a960c-141">0x800E</span></span>                          |
| <span data-ttu-id="a960c-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="a960c-142">System-Only</span></span>            | <span data-ttu-id="a960c-143">True</span><span class="sxs-lookup"><span data-stu-id="a960c-143">True</span></span>                            |
| <span data-ttu-id="a960c-144">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a960c-144">Is-Single-Valued</span></span>       | <span data-ttu-id="a960c-145">False</span><span class="sxs-lookup"><span data-stu-id="a960c-145">False</span></span>                           |
| <span data-ttu-id="a960c-146">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a960c-146">Is Indexed</span></span>             | <span data-ttu-id="a960c-147">False</span><span class="sxs-lookup"><span data-stu-id="a960c-147">False</span></span>                           |
| <span data-ttu-id="a960c-148">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a960c-148">In Global Catalog</span></span>      | <span data-ttu-id="a960c-149">False</span><span class="sxs-lookup"><span data-stu-id="a960c-149">False</span></span>                           |
| <span data-ttu-id="a960c-150">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a960c-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="a960c-151">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a960c-151">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a960c-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a960c-152">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a960c-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a960c-153">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a960c-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-154">Search-Flags</span></span>           | <span data-ttu-id="a960c-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a960c-155">0x00000000</span></span>                      |
| <span data-ttu-id="a960c-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-156">System-Flags</span></span>           | <span data-ttu-id="a960c-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a960c-157">0x00000010</span></span>                      |
| <span data-ttu-id="a960c-158">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a960c-158">Classes used in</span></span>        | [<span data-ttu-id="a960c-159">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a960c-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a960c-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a960c-160">Windows Server 2003</span></span>



| <span data-ttu-id="a960c-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="a960c-161">Entry</span></span> | <span data-ttu-id="a960c-162">Value</span><span class="sxs-lookup"><span data-stu-id="a960c-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a960c-163">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a960c-163">Link-Id</span></span>                | <span data-ttu-id="a960c-164">43</span><span class="sxs-lookup"><span data-stu-id="a960c-164">43</span></span>                              |
| <span data-ttu-id="a960c-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a960c-165">MAPI-Id</span></span>                | <span data-ttu-id="a960c-166">0x800E</span><span class="sxs-lookup"><span data-stu-id="a960c-166">0x800E</span></span>                          |
| <span data-ttu-id="a960c-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="a960c-167">System-Only</span></span>            | <span data-ttu-id="a960c-168">True</span><span class="sxs-lookup"><span data-stu-id="a960c-168">True</span></span>                            |
| <span data-ttu-id="a960c-169">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a960c-169">Is-Single-Valued</span></span>       | <span data-ttu-id="a960c-170">False</span><span class="sxs-lookup"><span data-stu-id="a960c-170">False</span></span>                           |
| <span data-ttu-id="a960c-171">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a960c-171">Is Indexed</span></span>             | <span data-ttu-id="a960c-172">False</span><span class="sxs-lookup"><span data-stu-id="a960c-172">False</span></span>                           |
| <span data-ttu-id="a960c-173">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a960c-173">In Global Catalog</span></span>      | <span data-ttu-id="a960c-174">False</span><span class="sxs-lookup"><span data-stu-id="a960c-174">False</span></span>                           |
| <span data-ttu-id="a960c-175">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a960c-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="a960c-176">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a960c-176">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a960c-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a960c-177">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a960c-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a960c-178">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a960c-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-179">Search-Flags</span></span>           | <span data-ttu-id="a960c-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a960c-180">0x00000000</span></span>                      |
| <span data-ttu-id="a960c-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-181">System-Flags</span></span>           | <span data-ttu-id="a960c-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a960c-182">0x00000010</span></span>                      |
| <span data-ttu-id="a960c-183">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a960c-183">Classes used in</span></span>        | [<span data-ttu-id="a960c-184">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a960c-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a960c-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a960c-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a960c-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="a960c-186">Entry</span></span> | <span data-ttu-id="a960c-187">Value</span><span class="sxs-lookup"><span data-stu-id="a960c-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a960c-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a960c-188">Link-Id</span></span>                | <span data-ttu-id="a960c-189">43</span><span class="sxs-lookup"><span data-stu-id="a960c-189">43</span></span>                              |
| <span data-ttu-id="a960c-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a960c-190">MAPI-Id</span></span>                | <span data-ttu-id="a960c-191">0x800E</span><span class="sxs-lookup"><span data-stu-id="a960c-191">0x800E</span></span>                          |
| <span data-ttu-id="a960c-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="a960c-192">System-Only</span></span>            | <span data-ttu-id="a960c-193">True</span><span class="sxs-lookup"><span data-stu-id="a960c-193">True</span></span>                            |
| <span data-ttu-id="a960c-194">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a960c-194">Is-Single-Valued</span></span>       | <span data-ttu-id="a960c-195">False</span><span class="sxs-lookup"><span data-stu-id="a960c-195">False</span></span>                           |
| <span data-ttu-id="a960c-196">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a960c-196">Is Indexed</span></span>             | <span data-ttu-id="a960c-197">False</span><span class="sxs-lookup"><span data-stu-id="a960c-197">False</span></span>                           |
| <span data-ttu-id="a960c-198">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a960c-198">In Global Catalog</span></span>      | <span data-ttu-id="a960c-199">False</span><span class="sxs-lookup"><span data-stu-id="a960c-199">False</span></span>                           |
| <span data-ttu-id="a960c-200">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a960c-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="a960c-201">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a960c-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a960c-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a960c-202">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a960c-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a960c-203">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a960c-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-204">Search-Flags</span></span>           | <span data-ttu-id="a960c-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a960c-205">0x00000000</span></span>                      |
| <span data-ttu-id="a960c-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-206">System-Flags</span></span>           | <span data-ttu-id="a960c-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a960c-207">0x00000010</span></span>                      |
| <span data-ttu-id="a960c-208">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a960c-208">Classes used in</span></span>        | [<span data-ttu-id="a960c-209">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a960c-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a960c-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a960c-210">Windows Server 2008</span></span>



| <span data-ttu-id="a960c-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="a960c-211">Entry</span></span> | <span data-ttu-id="a960c-212">Value</span><span class="sxs-lookup"><span data-stu-id="a960c-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a960c-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a960c-213">Link-Id</span></span>                | <span data-ttu-id="a960c-214">43</span><span class="sxs-lookup"><span data-stu-id="a960c-214">43</span></span>                              |
| <span data-ttu-id="a960c-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a960c-215">MAPI-Id</span></span>                | <span data-ttu-id="a960c-216">0x800E</span><span class="sxs-lookup"><span data-stu-id="a960c-216">0x800E</span></span>                          |
| <span data-ttu-id="a960c-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="a960c-217">System-Only</span></span>            | <span data-ttu-id="a960c-218">True</span><span class="sxs-lookup"><span data-stu-id="a960c-218">True</span></span>                            |
| <span data-ttu-id="a960c-219">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a960c-219">Is-Single-Valued</span></span>       | <span data-ttu-id="a960c-220">False</span><span class="sxs-lookup"><span data-stu-id="a960c-220">False</span></span>                           |
| <span data-ttu-id="a960c-221">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a960c-221">Is Indexed</span></span>             | <span data-ttu-id="a960c-222">False</span><span class="sxs-lookup"><span data-stu-id="a960c-222">False</span></span>                           |
| <span data-ttu-id="a960c-223">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a960c-223">In Global Catalog</span></span>      | <span data-ttu-id="a960c-224">False</span><span class="sxs-lookup"><span data-stu-id="a960c-224">False</span></span>                           |
| <span data-ttu-id="a960c-225">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a960c-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="a960c-226">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a960c-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a960c-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a960c-227">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a960c-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a960c-228">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a960c-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-229">Search-Flags</span></span>           | <span data-ttu-id="a960c-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a960c-230">0x00000000</span></span>                      |
| <span data-ttu-id="a960c-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-231">System-Flags</span></span>           | <span data-ttu-id="a960c-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a960c-232">0x00000010</span></span>                      |
| <span data-ttu-id="a960c-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a960c-233">Classes used in</span></span>        | [<span data-ttu-id="a960c-234">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a960c-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a960c-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a960c-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a960c-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="a960c-236">Entry</span></span> | <span data-ttu-id="a960c-237">Value</span><span class="sxs-lookup"><span data-stu-id="a960c-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a960c-238">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a960c-238">Link-Id</span></span>                | <span data-ttu-id="a960c-239">43</span><span class="sxs-lookup"><span data-stu-id="a960c-239">43</span></span>                              |
| <span data-ttu-id="a960c-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a960c-240">MAPI-Id</span></span>                | <span data-ttu-id="a960c-241">0x800E</span><span class="sxs-lookup"><span data-stu-id="a960c-241">0x800E</span></span>                          |
| <span data-ttu-id="a960c-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="a960c-242">System-Only</span></span>            | <span data-ttu-id="a960c-243">True</span><span class="sxs-lookup"><span data-stu-id="a960c-243">True</span></span>                            |
| <span data-ttu-id="a960c-244">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a960c-244">Is-Single-Valued</span></span>       | <span data-ttu-id="a960c-245">False</span><span class="sxs-lookup"><span data-stu-id="a960c-245">False</span></span>                           |
| <span data-ttu-id="a960c-246">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a960c-246">Is Indexed</span></span>             | <span data-ttu-id="a960c-247">False</span><span class="sxs-lookup"><span data-stu-id="a960c-247">False</span></span>                           |
| <span data-ttu-id="a960c-248">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a960c-248">In Global Catalog</span></span>      | <span data-ttu-id="a960c-249">False</span><span class="sxs-lookup"><span data-stu-id="a960c-249">False</span></span>                           |
| <span data-ttu-id="a960c-250">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a960c-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="a960c-251">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a960c-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a960c-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a960c-252">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a960c-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a960c-253">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a960c-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-254">Search-Flags</span></span>           | <span data-ttu-id="a960c-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a960c-255">0x00000000</span></span>                      |
| <span data-ttu-id="a960c-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-256">System-Flags</span></span>           | <span data-ttu-id="a960c-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a960c-257">0x00000010</span></span>                      |
| <span data-ttu-id="a960c-258">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a960c-258">Classes used in</span></span>        | [<span data-ttu-id="a960c-259">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a960c-259">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a960c-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a960c-260">Windows Server 2012</span></span>



| <span data-ttu-id="a960c-261">Entrada</span><span class="sxs-lookup"><span data-stu-id="a960c-261">Entry</span></span> | <span data-ttu-id="a960c-262">Value</span><span class="sxs-lookup"><span data-stu-id="a960c-262">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a960c-263">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a960c-263">Link-Id</span></span>                | <span data-ttu-id="a960c-264">43</span><span class="sxs-lookup"><span data-stu-id="a960c-264">43</span></span>                              |
| <span data-ttu-id="a960c-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a960c-265">MAPI-Id</span></span>                | <span data-ttu-id="a960c-266">0x800E</span><span class="sxs-lookup"><span data-stu-id="a960c-266">0x800E</span></span>                          |
| <span data-ttu-id="a960c-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="a960c-267">System-Only</span></span>            | <span data-ttu-id="a960c-268">True</span><span class="sxs-lookup"><span data-stu-id="a960c-268">True</span></span>                            |
| <span data-ttu-id="a960c-269">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a960c-269">Is-Single-Valued</span></span>       | <span data-ttu-id="a960c-270">False</span><span class="sxs-lookup"><span data-stu-id="a960c-270">False</span></span>                           |
| <span data-ttu-id="a960c-271">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a960c-271">Is Indexed</span></span>             | <span data-ttu-id="a960c-272">False</span><span class="sxs-lookup"><span data-stu-id="a960c-272">False</span></span>                           |
| <span data-ttu-id="a960c-273">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a960c-273">In Global Catalog</span></span>      | <span data-ttu-id="a960c-274">False</span><span class="sxs-lookup"><span data-stu-id="a960c-274">False</span></span>                           |
| <span data-ttu-id="a960c-275">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a960c-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="a960c-276">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a960c-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a960c-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a960c-277">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a960c-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a960c-278">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a960c-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-279">Search-Flags</span></span>           | <span data-ttu-id="a960c-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a960c-280">0x00000000</span></span>                      |
| <span data-ttu-id="a960c-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a960c-281">System-Flags</span></span>           | <span data-ttu-id="a960c-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a960c-282">0x00000010</span></span>                      |
| <span data-ttu-id="a960c-283">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a960c-283">Classes used in</span></span>        | [<span data-ttu-id="a960c-284">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="a960c-284">**Top**</span></span>](c-top.md)<br/> |



 

 






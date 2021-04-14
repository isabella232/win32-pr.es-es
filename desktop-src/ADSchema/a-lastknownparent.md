---
title: Último atributo primario conocido
description: Nombre distintivo (DN) del último elemento primario conocido de un objeto huérfano.
ms.assetid: 6cf7be1a-8ff0-42f7-9e7a-c15cbc652ec5
ms.tgt_platform: multiple
keywords:
- Último esquema de AD de atributo primario conocido
- lastKnownParent esquema de AD de atributos
topic_type:
- apiref
api_name:
- Last-Known-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d83ae15f910d2e2f2dbc23ff39bb28cd27d56b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658935"
---
# <a name="last-known-parent-attribute"></a><span data-ttu-id="d9267-105">Último atributo primario conocido</span><span class="sxs-lookup"><span data-stu-id="d9267-105">Last-Known-Parent attribute</span></span>

<span data-ttu-id="d9267-106">Nombre distintivo (DN) del último elemento primario conocido de un objeto huérfano.</span><span class="sxs-lookup"><span data-stu-id="d9267-106">The Distinguished Name (DN) of the last known parent of an orphaned object.</span></span>



| <span data-ttu-id="d9267-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9267-107">Entry</span></span> | <span data-ttu-id="d9267-108">Value</span><span class="sxs-lookup"><span data-stu-id="d9267-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d9267-109">CN</span><span class="sxs-lookup"><span data-stu-id="d9267-109">CN</span></span>                | <span data-ttu-id="d9267-110">Último conocido-primario</span><span class="sxs-lookup"><span data-stu-id="d9267-110">Last-Known-Parent</span></span>                       |
| <span data-ttu-id="d9267-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d9267-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d9267-112">lastKnownParent</span><span class="sxs-lookup"><span data-stu-id="d9267-112">lastKnownParent</span></span>                         |
| <span data-ttu-id="d9267-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d9267-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d9267-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d9267-114">Update Privilege</span></span>  | <span data-ttu-id="d9267-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="d9267-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="d9267-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d9267-116">Update Frequency</span></span>  | <span data-ttu-id="d9267-117">Cada vez que un objeto está huérfano.</span><span class="sxs-lookup"><span data-stu-id="d9267-117">Whenever an object is orphaned.</span></span>         |
| <span data-ttu-id="d9267-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d9267-118">Attribute-Id</span></span>      | <span data-ttu-id="d9267-119">1.2.840.113556.1.4.781</span><span class="sxs-lookup"><span data-stu-id="d9267-119">1.2.840.113556.1.4.781</span></span>                  |
| <span data-ttu-id="d9267-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d9267-120">System-Id-Guid</span></span>    | <span data-ttu-id="d9267-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d9267-121">52ab8670-5709-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="d9267-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9267-122">Syntax</span></span>            | [<span data-ttu-id="d9267-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d9267-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d9267-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d9267-124">Implementations</span></span>

-   [<span data-ttu-id="d9267-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d9267-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d9267-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d9267-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d9267-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d9267-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d9267-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d9267-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d9267-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d9267-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d9267-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d9267-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d9267-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d9267-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d9267-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d9267-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d9267-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9267-133">Entry</span></span> | <span data-ttu-id="d9267-134">Value</span><span class="sxs-lookup"><span data-stu-id="d9267-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9267-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9267-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9267-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9267-137">System-Only</span></span>            | <span data-ttu-id="d9267-138">False</span><span class="sxs-lookup"><span data-stu-id="d9267-138">False</span></span>                           |
| <span data-ttu-id="d9267-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9267-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d9267-140">True</span><span class="sxs-lookup"><span data-stu-id="d9267-140">True</span></span>                            |
| <span data-ttu-id="d9267-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9267-141">Is Indexed</span></span>             | <span data-ttu-id="d9267-142">False</span><span class="sxs-lookup"><span data-stu-id="d9267-142">False</span></span>                           |
| <span data-ttu-id="d9267-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9267-143">In Global Catalog</span></span>      | <span data-ttu-id="d9267-144">False</span><span class="sxs-lookup"><span data-stu-id="d9267-144">False</span></span>                           |
| <span data-ttu-id="d9267-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9267-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9267-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9267-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9267-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9267-147">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d9267-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9267-148">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d9267-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-149">Search-Flags</span></span>           | <span data-ttu-id="d9267-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9267-150">0x00000000</span></span>                      |
| <span data-ttu-id="d9267-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-151">System-Flags</span></span>           | <span data-ttu-id="d9267-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9267-152">0x00000010</span></span>                      |
| <span data-ttu-id="d9267-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9267-153">Classes used in</span></span>        | [<span data-ttu-id="d9267-154">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9267-154">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d9267-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d9267-155">Windows Server 2003</span></span>



| <span data-ttu-id="d9267-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9267-156">Entry</span></span> | <span data-ttu-id="d9267-157">Value</span><span class="sxs-lookup"><span data-stu-id="d9267-157">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9267-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9267-158">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9267-159">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9267-160">System-Only</span></span>            | <span data-ttu-id="d9267-161">False</span><span class="sxs-lookup"><span data-stu-id="d9267-161">False</span></span>                           |
| <span data-ttu-id="d9267-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9267-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d9267-163">True</span><span class="sxs-lookup"><span data-stu-id="d9267-163">True</span></span>                            |
| <span data-ttu-id="d9267-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9267-164">Is Indexed</span></span>             | <span data-ttu-id="d9267-165">False</span><span class="sxs-lookup"><span data-stu-id="d9267-165">False</span></span>                           |
| <span data-ttu-id="d9267-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9267-166">In Global Catalog</span></span>      | <span data-ttu-id="d9267-167">False</span><span class="sxs-lookup"><span data-stu-id="d9267-167">False</span></span>                           |
| <span data-ttu-id="d9267-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9267-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9267-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9267-169">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9267-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9267-170">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d9267-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9267-171">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d9267-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-172">Search-Flags</span></span>           | <span data-ttu-id="d9267-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9267-173">0x00000000</span></span>                      |
| <span data-ttu-id="d9267-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-174">System-Flags</span></span>           | <span data-ttu-id="d9267-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9267-175">0x00000010</span></span>                      |
| <span data-ttu-id="d9267-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9267-176">Classes used in</span></span>        | [<span data-ttu-id="d9267-177">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9267-177">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d9267-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="d9267-178">ADAM</span></span>



| <span data-ttu-id="d9267-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9267-179">Entry</span></span> | <span data-ttu-id="d9267-180">Value</span><span class="sxs-lookup"><span data-stu-id="d9267-180">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9267-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9267-181">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9267-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9267-183">System-Only</span></span>            | <span data-ttu-id="d9267-184">False</span><span class="sxs-lookup"><span data-stu-id="d9267-184">False</span></span>                           |
| <span data-ttu-id="d9267-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9267-185">Is-Single-Valued</span></span>       | <span data-ttu-id="d9267-186">True</span><span class="sxs-lookup"><span data-stu-id="d9267-186">True</span></span>                            |
| <span data-ttu-id="d9267-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9267-187">Is Indexed</span></span>             | <span data-ttu-id="d9267-188">False</span><span class="sxs-lookup"><span data-stu-id="d9267-188">False</span></span>                           |
| <span data-ttu-id="d9267-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9267-189">In Global Catalog</span></span>      | <span data-ttu-id="d9267-190">False</span><span class="sxs-lookup"><span data-stu-id="d9267-190">False</span></span>                           |
| <span data-ttu-id="d9267-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9267-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9267-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9267-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9267-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9267-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d9267-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9267-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d9267-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-195">Search-Flags</span></span>           | <span data-ttu-id="d9267-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9267-196">0x00000000</span></span>                      |
| <span data-ttu-id="d9267-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-197">System-Flags</span></span>           | <span data-ttu-id="d9267-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9267-198">0x00000010</span></span>                      |
| <span data-ttu-id="d9267-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9267-199">Classes used in</span></span>        | [<span data-ttu-id="d9267-200">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9267-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d9267-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d9267-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d9267-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9267-202">Entry</span></span> | <span data-ttu-id="d9267-203">Value</span><span class="sxs-lookup"><span data-stu-id="d9267-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9267-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9267-204">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9267-205">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9267-206">System-Only</span></span>            | <span data-ttu-id="d9267-207">False</span><span class="sxs-lookup"><span data-stu-id="d9267-207">False</span></span>                           |
| <span data-ttu-id="d9267-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9267-208">Is-Single-Valued</span></span>       | <span data-ttu-id="d9267-209">True</span><span class="sxs-lookup"><span data-stu-id="d9267-209">True</span></span>                            |
| <span data-ttu-id="d9267-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9267-210">Is Indexed</span></span>             | <span data-ttu-id="d9267-211">False</span><span class="sxs-lookup"><span data-stu-id="d9267-211">False</span></span>                           |
| <span data-ttu-id="d9267-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9267-212">In Global Catalog</span></span>      | <span data-ttu-id="d9267-213">False</span><span class="sxs-lookup"><span data-stu-id="d9267-213">False</span></span>                           |
| <span data-ttu-id="d9267-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9267-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9267-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9267-215">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9267-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9267-216">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d9267-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9267-217">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d9267-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-218">Search-Flags</span></span>           | <span data-ttu-id="d9267-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9267-219">0x00000000</span></span>                      |
| <span data-ttu-id="d9267-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-220">System-Flags</span></span>           | <span data-ttu-id="d9267-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9267-221">0x00000010</span></span>                      |
| <span data-ttu-id="d9267-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9267-222">Classes used in</span></span>        | [<span data-ttu-id="d9267-223">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9267-223">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d9267-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9267-224">Windows Server 2008</span></span>



| <span data-ttu-id="d9267-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9267-225">Entry</span></span> | <span data-ttu-id="d9267-226">Value</span><span class="sxs-lookup"><span data-stu-id="d9267-226">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9267-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9267-227">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9267-228">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9267-229">System-Only</span></span>            | <span data-ttu-id="d9267-230">False</span><span class="sxs-lookup"><span data-stu-id="d9267-230">False</span></span>                           |
| <span data-ttu-id="d9267-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9267-231">Is-Single-Valued</span></span>       | <span data-ttu-id="d9267-232">True</span><span class="sxs-lookup"><span data-stu-id="d9267-232">True</span></span>                            |
| <span data-ttu-id="d9267-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9267-233">Is Indexed</span></span>             | <span data-ttu-id="d9267-234">False</span><span class="sxs-lookup"><span data-stu-id="d9267-234">False</span></span>                           |
| <span data-ttu-id="d9267-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9267-235">In Global Catalog</span></span>      | <span data-ttu-id="d9267-236">False</span><span class="sxs-lookup"><span data-stu-id="d9267-236">False</span></span>                           |
| <span data-ttu-id="d9267-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9267-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9267-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9267-238">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9267-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9267-239">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d9267-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9267-240">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d9267-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-241">Search-Flags</span></span>           | <span data-ttu-id="d9267-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9267-242">0x00000000</span></span>                      |
| <span data-ttu-id="d9267-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-243">System-Flags</span></span>           | <span data-ttu-id="d9267-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9267-244">0x00000010</span></span>                      |
| <span data-ttu-id="d9267-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9267-245">Classes used in</span></span>        | [<span data-ttu-id="d9267-246">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9267-246">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d9267-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9267-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d9267-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9267-248">Entry</span></span> | <span data-ttu-id="d9267-249">Value</span><span class="sxs-lookup"><span data-stu-id="d9267-249">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9267-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9267-250">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9267-251">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9267-252">System-Only</span></span>            | <span data-ttu-id="d9267-253">False</span><span class="sxs-lookup"><span data-stu-id="d9267-253">False</span></span>                           |
| <span data-ttu-id="d9267-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9267-254">Is-Single-Valued</span></span>       | <span data-ttu-id="d9267-255">True</span><span class="sxs-lookup"><span data-stu-id="d9267-255">True</span></span>                            |
| <span data-ttu-id="d9267-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9267-256">Is Indexed</span></span>             | <span data-ttu-id="d9267-257">False</span><span class="sxs-lookup"><span data-stu-id="d9267-257">False</span></span>                           |
| <span data-ttu-id="d9267-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9267-258">In Global Catalog</span></span>      | <span data-ttu-id="d9267-259">False</span><span class="sxs-lookup"><span data-stu-id="d9267-259">False</span></span>                           |
| <span data-ttu-id="d9267-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9267-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9267-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9267-261">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9267-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9267-262">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d9267-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9267-263">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d9267-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-264">Search-Flags</span></span>           | <span data-ttu-id="d9267-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9267-265">0x00000000</span></span>                      |
| <span data-ttu-id="d9267-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-266">System-Flags</span></span>           | <span data-ttu-id="d9267-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9267-267">0x00000010</span></span>                      |
| <span data-ttu-id="d9267-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9267-268">Classes used in</span></span>        | [<span data-ttu-id="d9267-269">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9267-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d9267-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9267-270">Windows Server 2012</span></span>



| <span data-ttu-id="d9267-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9267-271">Entry</span></span> | <span data-ttu-id="d9267-272">Value</span><span class="sxs-lookup"><span data-stu-id="d9267-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9267-273">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9267-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9267-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d9267-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9267-275">System-Only</span></span>            | <span data-ttu-id="d9267-276">False</span><span class="sxs-lookup"><span data-stu-id="d9267-276">False</span></span>                           |
| <span data-ttu-id="d9267-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9267-277">Is-Single-Valued</span></span>       | <span data-ttu-id="d9267-278">True</span><span class="sxs-lookup"><span data-stu-id="d9267-278">True</span></span>                            |
| <span data-ttu-id="d9267-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9267-279">Is Indexed</span></span>             | <span data-ttu-id="d9267-280">False</span><span class="sxs-lookup"><span data-stu-id="d9267-280">False</span></span>                           |
| <span data-ttu-id="d9267-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9267-281">In Global Catalog</span></span>      | <span data-ttu-id="d9267-282">False</span><span class="sxs-lookup"><span data-stu-id="d9267-282">False</span></span>                           |
| <span data-ttu-id="d9267-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9267-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9267-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9267-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9267-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9267-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d9267-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9267-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d9267-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-287">Search-Flags</span></span>           | <span data-ttu-id="d9267-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9267-288">0x00000000</span></span>                      |
| <span data-ttu-id="d9267-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9267-289">System-Flags</span></span>           | <span data-ttu-id="d9267-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9267-290">0x00000010</span></span>                      |
| <span data-ttu-id="d9267-291">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9267-291">Classes used in</span></span>        | [<span data-ttu-id="d9267-292">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9267-292">**Top**</span></span>](c-top.md)<br/> |



 

 






---
title: Atributo Obj-Dist-Name
description: Igual que el nombre distintivo de un objeto. Utilizado por Exchange.
ms.assetid: 0dc2855c-2707-49d8-80e6-27f163a59bc8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Obj-Dist-Name
- atributo distinguishedName esquema de AD
topic_type:
- apiref
api_name:
- Obj-Dist-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42cd118f38de78546b7b792bca3c8c9ef6d229cb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905799"
---
# <a name="obj-dist-name-attribute"></a><span data-ttu-id="08f6c-106">Atributo Obj-Dist-Name</span><span class="sxs-lookup"><span data-stu-id="08f6c-106">Obj-Dist-Name attribute</span></span>

<span data-ttu-id="08f6c-107">Igual que el nombre distintivo de un objeto.</span><span class="sxs-lookup"><span data-stu-id="08f6c-107">Same as the Distinguished Name for an object.</span></span> <span data-ttu-id="08f6c-108">Utilizado por Exchange.</span><span class="sxs-lookup"><span data-stu-id="08f6c-108">Used by Exchange.</span></span>



| <span data-ttu-id="08f6c-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="08f6c-109">Entry</span></span> | <span data-ttu-id="08f6c-110">Value</span><span class="sxs-lookup"><span data-stu-id="08f6c-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="08f6c-111">CN</span><span class="sxs-lookup"><span data-stu-id="08f6c-111">CN</span></span>                | <span data-ttu-id="08f6c-112">Obj-Dist-nombre</span><span class="sxs-lookup"><span data-stu-id="08f6c-112">Obj-Dist-Name</span></span>                           |
| <span data-ttu-id="08f6c-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="08f6c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="08f6c-114">distinguishedName</span><span class="sxs-lookup"><span data-stu-id="08f6c-114">distinguishedName</span></span>                       |
| <span data-ttu-id="08f6c-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="08f6c-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="08f6c-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="08f6c-116">Update Privilege</span></span>  | <span data-ttu-id="08f6c-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="08f6c-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="08f6c-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="08f6c-118">Update Frequency</span></span>  | <span data-ttu-id="08f6c-119">Cada vez que se crea o se mueve un objeto.</span><span class="sxs-lookup"><span data-stu-id="08f6c-119">Whenever an object is created or moved.</span></span> |
| <span data-ttu-id="08f6c-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="08f6c-120">Attribute-Id</span></span>      | <span data-ttu-id="08f6c-121">2.5.4.49</span><span class="sxs-lookup"><span data-stu-id="08f6c-121">2.5.4.49</span></span>                                |
| <span data-ttu-id="08f6c-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="08f6c-122">System-Id-Guid</span></span>    | <span data-ttu-id="08f6c-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="08f6c-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="08f6c-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08f6c-124">Syntax</span></span>            | [<span data-ttu-id="08f6c-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="08f6c-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="08f6c-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="08f6c-126">Implementations</span></span>

-   [<span data-ttu-id="08f6c-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="08f6c-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="08f6c-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="08f6c-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="08f6c-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="08f6c-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="08f6c-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="08f6c-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="08f6c-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="08f6c-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="08f6c-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="08f6c-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="08f6c-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="08f6c-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="08f6c-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08f6c-134">Windows 2000 Server</span></span>



| <span data-ttu-id="08f6c-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="08f6c-135">Entry</span></span> | <span data-ttu-id="08f6c-136">Value</span><span class="sxs-lookup"><span data-stu-id="08f6c-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="08f6c-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08f6c-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="08f6c-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08f6c-138">MAPI-Id</span></span>                | <span data-ttu-id="08f6c-139">0x803C</span><span class="sxs-lookup"><span data-stu-id="08f6c-139">0x803C</span></span>                          |
| <span data-ttu-id="08f6c-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="08f6c-140">System-Only</span></span>            | <span data-ttu-id="08f6c-141">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-141">True</span></span>                            |
| <span data-ttu-id="08f6c-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08f6c-142">Is-Single-Valued</span></span>       | <span data-ttu-id="08f6c-143">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-143">True</span></span>                            |
| <span data-ttu-id="08f6c-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08f6c-144">Is Indexed</span></span>             | <span data-ttu-id="08f6c-145">False</span><span class="sxs-lookup"><span data-stu-id="08f6c-145">False</span></span>                           |
| <span data-ttu-id="08f6c-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08f6c-146">In Global Catalog</span></span>      | <span data-ttu-id="08f6c-147">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-147">True</span></span>                            |
| <span data-ttu-id="08f6c-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08f6c-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="08f6c-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08f6c-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="08f6c-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08f6c-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="08f6c-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08f6c-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="08f6c-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-152">Search-Flags</span></span>           | <span data-ttu-id="08f6c-153">0x00000008</span><span class="sxs-lookup"><span data-stu-id="08f6c-153">0x00000008</span></span>                      |
| <span data-ttu-id="08f6c-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-154">System-Flags</span></span>           | <span data-ttu-id="08f6c-155">0x00000013</span><span class="sxs-lookup"><span data-stu-id="08f6c-155">0x00000013</span></span>                      |
| <span data-ttu-id="08f6c-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08f6c-156">Classes used in</span></span>        | [<span data-ttu-id="08f6c-157">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="08f6c-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="08f6c-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08f6c-158">Windows Server 2003</span></span>



| <span data-ttu-id="08f6c-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="08f6c-159">Entry</span></span> | <span data-ttu-id="08f6c-160">Value</span><span class="sxs-lookup"><span data-stu-id="08f6c-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="08f6c-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08f6c-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="08f6c-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08f6c-162">MAPI-Id</span></span>                | <span data-ttu-id="08f6c-163">0x803C</span><span class="sxs-lookup"><span data-stu-id="08f6c-163">0x803C</span></span>                          |
| <span data-ttu-id="08f6c-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="08f6c-164">System-Only</span></span>            | <span data-ttu-id="08f6c-165">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-165">True</span></span>                            |
| <span data-ttu-id="08f6c-166">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08f6c-166">Is-Single-Valued</span></span>       | <span data-ttu-id="08f6c-167">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-167">True</span></span>                            |
| <span data-ttu-id="08f6c-168">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08f6c-168">Is Indexed</span></span>             | <span data-ttu-id="08f6c-169">False</span><span class="sxs-lookup"><span data-stu-id="08f6c-169">False</span></span>                           |
| <span data-ttu-id="08f6c-170">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08f6c-170">In Global Catalog</span></span>      | <span data-ttu-id="08f6c-171">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-171">True</span></span>                            |
| <span data-ttu-id="08f6c-172">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08f6c-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="08f6c-173">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08f6c-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="08f6c-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08f6c-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="08f6c-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08f6c-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="08f6c-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-176">Search-Flags</span></span>           | <span data-ttu-id="08f6c-177">0x00000008</span><span class="sxs-lookup"><span data-stu-id="08f6c-177">0x00000008</span></span>                      |
| <span data-ttu-id="08f6c-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-178">System-Flags</span></span>           | <span data-ttu-id="08f6c-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="08f6c-179">0x00000013</span></span>                      |
| <span data-ttu-id="08f6c-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08f6c-180">Classes used in</span></span>        | [<span data-ttu-id="08f6c-181">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="08f6c-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="08f6c-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="08f6c-182">ADAM</span></span>



| <span data-ttu-id="08f6c-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="08f6c-183">Entry</span></span> | <span data-ttu-id="08f6c-184">Value</span><span class="sxs-lookup"><span data-stu-id="08f6c-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="08f6c-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08f6c-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="08f6c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08f6c-186">MAPI-Id</span></span>                | <span data-ttu-id="08f6c-187">0x803C</span><span class="sxs-lookup"><span data-stu-id="08f6c-187">0x803C</span></span>                          |
| <span data-ttu-id="08f6c-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="08f6c-188">System-Only</span></span>            | <span data-ttu-id="08f6c-189">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-189">True</span></span>                            |
| <span data-ttu-id="08f6c-190">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08f6c-190">Is-Single-Valued</span></span>       | <span data-ttu-id="08f6c-191">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-191">True</span></span>                            |
| <span data-ttu-id="08f6c-192">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08f6c-192">Is Indexed</span></span>             | <span data-ttu-id="08f6c-193">False</span><span class="sxs-lookup"><span data-stu-id="08f6c-193">False</span></span>                           |
| <span data-ttu-id="08f6c-194">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08f6c-194">In Global Catalog</span></span>      | <span data-ttu-id="08f6c-195">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-195">True</span></span>                            |
| <span data-ttu-id="08f6c-196">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08f6c-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="08f6c-197">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08f6c-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="08f6c-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08f6c-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="08f6c-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08f6c-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="08f6c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-200">Search-Flags</span></span>           | <span data-ttu-id="08f6c-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="08f6c-201">0x00000008</span></span>                      |
| <span data-ttu-id="08f6c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-202">System-Flags</span></span>           | <span data-ttu-id="08f6c-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="08f6c-203">0x00000013</span></span>                      |
| <span data-ttu-id="08f6c-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08f6c-204">Classes used in</span></span>        | [<span data-ttu-id="08f6c-205">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="08f6c-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="08f6c-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="08f6c-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="08f6c-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="08f6c-207">Entry</span></span> | <span data-ttu-id="08f6c-208">Value</span><span class="sxs-lookup"><span data-stu-id="08f6c-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="08f6c-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08f6c-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="08f6c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08f6c-210">MAPI-Id</span></span>                | <span data-ttu-id="08f6c-211">0x803C</span><span class="sxs-lookup"><span data-stu-id="08f6c-211">0x803C</span></span>                          |
| <span data-ttu-id="08f6c-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="08f6c-212">System-Only</span></span>            | <span data-ttu-id="08f6c-213">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-213">True</span></span>                            |
| <span data-ttu-id="08f6c-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08f6c-214">Is-Single-Valued</span></span>       | <span data-ttu-id="08f6c-215">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-215">True</span></span>                            |
| <span data-ttu-id="08f6c-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08f6c-216">Is Indexed</span></span>             | <span data-ttu-id="08f6c-217">False</span><span class="sxs-lookup"><span data-stu-id="08f6c-217">False</span></span>                           |
| <span data-ttu-id="08f6c-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08f6c-218">In Global Catalog</span></span>      | <span data-ttu-id="08f6c-219">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-219">True</span></span>                            |
| <span data-ttu-id="08f6c-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08f6c-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="08f6c-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08f6c-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="08f6c-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08f6c-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="08f6c-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08f6c-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="08f6c-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-224">Search-Flags</span></span>           | <span data-ttu-id="08f6c-225">0x00000008</span><span class="sxs-lookup"><span data-stu-id="08f6c-225">0x00000008</span></span>                      |
| <span data-ttu-id="08f6c-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-226">System-Flags</span></span>           | <span data-ttu-id="08f6c-227">0x00000013</span><span class="sxs-lookup"><span data-stu-id="08f6c-227">0x00000013</span></span>                      |
| <span data-ttu-id="08f6c-228">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08f6c-228">Classes used in</span></span>        | [<span data-ttu-id="08f6c-229">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="08f6c-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="08f6c-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08f6c-230">Windows Server 2008</span></span>



| <span data-ttu-id="08f6c-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="08f6c-231">Entry</span></span> | <span data-ttu-id="08f6c-232">Value</span><span class="sxs-lookup"><span data-stu-id="08f6c-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="08f6c-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08f6c-233">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="08f6c-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08f6c-234">MAPI-Id</span></span>                | <span data-ttu-id="08f6c-235">0x803C</span><span class="sxs-lookup"><span data-stu-id="08f6c-235">0x803C</span></span>                          |
| <span data-ttu-id="08f6c-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="08f6c-236">System-Only</span></span>            | <span data-ttu-id="08f6c-237">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-237">True</span></span>                            |
| <span data-ttu-id="08f6c-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08f6c-238">Is-Single-Valued</span></span>       | <span data-ttu-id="08f6c-239">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-239">True</span></span>                            |
| <span data-ttu-id="08f6c-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08f6c-240">Is Indexed</span></span>             | <span data-ttu-id="08f6c-241">False</span><span class="sxs-lookup"><span data-stu-id="08f6c-241">False</span></span>                           |
| <span data-ttu-id="08f6c-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08f6c-242">In Global Catalog</span></span>      | <span data-ttu-id="08f6c-243">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-243">True</span></span>                            |
| <span data-ttu-id="08f6c-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08f6c-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="08f6c-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08f6c-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="08f6c-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08f6c-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="08f6c-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08f6c-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="08f6c-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-248">Search-Flags</span></span>           | <span data-ttu-id="08f6c-249">0x00000008</span><span class="sxs-lookup"><span data-stu-id="08f6c-249">0x00000008</span></span>                      |
| <span data-ttu-id="08f6c-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-250">System-Flags</span></span>           | <span data-ttu-id="08f6c-251">0x00000013</span><span class="sxs-lookup"><span data-stu-id="08f6c-251">0x00000013</span></span>                      |
| <span data-ttu-id="08f6c-252">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08f6c-252">Classes used in</span></span>        | [<span data-ttu-id="08f6c-253">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="08f6c-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="08f6c-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08f6c-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="08f6c-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="08f6c-255">Entry</span></span> | <span data-ttu-id="08f6c-256">Value</span><span class="sxs-lookup"><span data-stu-id="08f6c-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="08f6c-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08f6c-257">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="08f6c-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08f6c-258">MAPI-Id</span></span>                | <span data-ttu-id="08f6c-259">0x803C</span><span class="sxs-lookup"><span data-stu-id="08f6c-259">0x803C</span></span>                          |
| <span data-ttu-id="08f6c-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="08f6c-260">System-Only</span></span>            | <span data-ttu-id="08f6c-261">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-261">True</span></span>                            |
| <span data-ttu-id="08f6c-262">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08f6c-262">Is-Single-Valued</span></span>       | <span data-ttu-id="08f6c-263">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-263">True</span></span>                            |
| <span data-ttu-id="08f6c-264">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08f6c-264">Is Indexed</span></span>             | <span data-ttu-id="08f6c-265">False</span><span class="sxs-lookup"><span data-stu-id="08f6c-265">False</span></span>                           |
| <span data-ttu-id="08f6c-266">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08f6c-266">In Global Catalog</span></span>      | <span data-ttu-id="08f6c-267">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-267">True</span></span>                            |
| <span data-ttu-id="08f6c-268">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08f6c-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="08f6c-269">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08f6c-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="08f6c-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08f6c-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="08f6c-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08f6c-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="08f6c-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-272">Search-Flags</span></span>           | <span data-ttu-id="08f6c-273">0x00000008</span><span class="sxs-lookup"><span data-stu-id="08f6c-273">0x00000008</span></span>                      |
| <span data-ttu-id="08f6c-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-274">System-Flags</span></span>           | <span data-ttu-id="08f6c-275">0x00000013</span><span class="sxs-lookup"><span data-stu-id="08f6c-275">0x00000013</span></span>                      |
| <span data-ttu-id="08f6c-276">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08f6c-276">Classes used in</span></span>        | [<span data-ttu-id="08f6c-277">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="08f6c-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="08f6c-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08f6c-278">Windows Server 2012</span></span>



| <span data-ttu-id="08f6c-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="08f6c-279">Entry</span></span> | <span data-ttu-id="08f6c-280">Value</span><span class="sxs-lookup"><span data-stu-id="08f6c-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="08f6c-281">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08f6c-281">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="08f6c-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08f6c-282">MAPI-Id</span></span>                | <span data-ttu-id="08f6c-283">0x803C</span><span class="sxs-lookup"><span data-stu-id="08f6c-283">0x803C</span></span>                          |
| <span data-ttu-id="08f6c-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="08f6c-284">System-Only</span></span>            | <span data-ttu-id="08f6c-285">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-285">True</span></span>                            |
| <span data-ttu-id="08f6c-286">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08f6c-286">Is-Single-Valued</span></span>       | <span data-ttu-id="08f6c-287">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-287">True</span></span>                            |
| <span data-ttu-id="08f6c-288">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08f6c-288">Is Indexed</span></span>             | <span data-ttu-id="08f6c-289">False</span><span class="sxs-lookup"><span data-stu-id="08f6c-289">False</span></span>                           |
| <span data-ttu-id="08f6c-290">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08f6c-290">In Global Catalog</span></span>      | <span data-ttu-id="08f6c-291">True</span><span class="sxs-lookup"><span data-stu-id="08f6c-291">True</span></span>                            |
| <span data-ttu-id="08f6c-292">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08f6c-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="08f6c-293">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08f6c-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="08f6c-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08f6c-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="08f6c-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08f6c-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="08f6c-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-296">Search-Flags</span></span>           | <span data-ttu-id="08f6c-297">0x00000008</span><span class="sxs-lookup"><span data-stu-id="08f6c-297">0x00000008</span></span>                      |
| <span data-ttu-id="08f6c-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08f6c-298">System-Flags</span></span>           | <span data-ttu-id="08f6c-299">0x00000013</span><span class="sxs-lookup"><span data-stu-id="08f6c-299">0x00000013</span></span>                      |
| <span data-ttu-id="08f6c-300">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08f6c-300">Classes used in</span></span>        | [<span data-ttu-id="08f6c-301">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="08f6c-301">**Top**</span></span>](c-top.md)<br/> |



 

 






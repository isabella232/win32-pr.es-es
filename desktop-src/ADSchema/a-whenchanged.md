---
title: When-Changed atributo)
description: Fecha en que se modificó por última vez este objeto. Este valor no se replica y existe en el catálogo global.
ms.assetid: 32dc9458-5692-4bce-abc1-7bea3ea680a9
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de When-Changed
- Esquema de AD de atributo whenChanged
topic_type:
- apiref
api_name:
- When-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c3608a33aa5d5ac52b226cd7a3d94ff0b95520
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905727"
---
# <a name="when-changed-attribute"></a><span data-ttu-id="3ce65-106">When-Changed atributo)</span><span class="sxs-lookup"><span data-stu-id="3ce65-106">When-Changed attribute</span></span>

<span data-ttu-id="3ce65-107">Fecha en que se modificó por última vez este objeto.</span><span class="sxs-lookup"><span data-stu-id="3ce65-107">The date when this object was last changed.</span></span> <span data-ttu-id="3ce65-108">Este valor no se replica y existe en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="3ce65-108">This value is not replicated and exists in the global catalog.</span></span>



| <span data-ttu-id="3ce65-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ce65-109">Entry</span></span> | <span data-ttu-id="3ce65-110">Value</span><span class="sxs-lookup"><span data-stu-id="3ce65-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="3ce65-111">CN</span><span class="sxs-lookup"><span data-stu-id="3ce65-111">CN</span></span>                | <span data-ttu-id="3ce65-112">When-Changed</span><span class="sxs-lookup"><span data-stu-id="3ce65-112">When-Changed</span></span>                                                  |
| <span data-ttu-id="3ce65-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="3ce65-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3ce65-114">whenChanged</span><span class="sxs-lookup"><span data-stu-id="3ce65-114">whenChanged</span></span>                                                   |
| <span data-ttu-id="3ce65-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="3ce65-115">Size</span></span>              | <span data-ttu-id="3ce65-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="3ce65-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="3ce65-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="3ce65-117">Update Privilege</span></span>  | <span data-ttu-id="3ce65-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="3ce65-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="3ce65-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="3ce65-119">Update Frequency</span></span>  | <span data-ttu-id="3ce65-120">Cada vez que se cambia el objeto.</span><span class="sxs-lookup"><span data-stu-id="3ce65-120">Each time the object is changed.</span></span>                              |
| <span data-ttu-id="3ce65-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3ce65-121">Attribute-Id</span></span>      | <span data-ttu-id="3ce65-122">1.2.840.113556.1.2.3</span><span class="sxs-lookup"><span data-stu-id="3ce65-122">1.2.840.113556.1.2.3</span></span>                                          |
| <span data-ttu-id="3ce65-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3ce65-123">System-Id-Guid</span></span>    | <span data-ttu-id="3ce65-124">bf967a77-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3ce65-124">bf967a77-0de6-11d0-a285-00aa003049e2</span></span>                          |
| <span data-ttu-id="3ce65-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ce65-125">Syntax</span></span>            | [<span data-ttu-id="3ce65-126">**String(Generalized-Time)**</span><span class="sxs-lookup"><span data-stu-id="3ce65-126">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="3ce65-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="3ce65-127">Implementations</span></span>

-   [<span data-ttu-id="3ce65-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3ce65-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3ce65-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3ce65-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3ce65-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3ce65-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3ce65-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3ce65-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3ce65-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3ce65-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3ce65-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3ce65-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3ce65-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3ce65-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3ce65-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3ce65-135">Windows 2000 Server</span></span>



| <span data-ttu-id="3ce65-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ce65-136">Entry</span></span> | <span data-ttu-id="3ce65-137">Value</span><span class="sxs-lookup"><span data-stu-id="3ce65-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3ce65-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3ce65-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3ce65-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ce65-139">MAPI-Id</span></span>                | <span data-ttu-id="3ce65-140">0x3008</span><span class="sxs-lookup"><span data-stu-id="3ce65-140">0x3008</span></span>                          |
| <span data-ttu-id="3ce65-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ce65-141">System-Only</span></span>            | <span data-ttu-id="3ce65-142">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-142">True</span></span>                            |
| <span data-ttu-id="3ce65-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3ce65-143">Is-Single-Valued</span></span>       | <span data-ttu-id="3ce65-144">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-144">True</span></span>                            |
| <span data-ttu-id="3ce65-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3ce65-145">Is Indexed</span></span>             | <span data-ttu-id="3ce65-146">False</span><span class="sxs-lookup"><span data-stu-id="3ce65-146">False</span></span>                           |
| <span data-ttu-id="3ce65-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ce65-147">In Global Catalog</span></span>      | <span data-ttu-id="3ce65-148">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-148">True</span></span>                            |
| <span data-ttu-id="3ce65-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3ce65-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ce65-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ce65-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3ce65-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ce65-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3ce65-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ce65-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3ce65-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-153">Search-Flags</span></span>           | <span data-ttu-id="3ce65-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ce65-154">0x00000000</span></span>                      |
| <span data-ttu-id="3ce65-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-155">System-Flags</span></span>           | <span data-ttu-id="3ce65-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3ce65-156">0x00000013</span></span>                      |
| <span data-ttu-id="3ce65-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3ce65-157">Classes used in</span></span>        | [<span data-ttu-id="3ce65-158">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="3ce65-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3ce65-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ce65-159">Windows Server 2003</span></span>



| <span data-ttu-id="3ce65-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ce65-160">Entry</span></span> | <span data-ttu-id="3ce65-161">Value</span><span class="sxs-lookup"><span data-stu-id="3ce65-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3ce65-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3ce65-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3ce65-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ce65-163">MAPI-Id</span></span>                | <span data-ttu-id="3ce65-164">0x3008</span><span class="sxs-lookup"><span data-stu-id="3ce65-164">0x3008</span></span>                          |
| <span data-ttu-id="3ce65-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ce65-165">System-Only</span></span>            | <span data-ttu-id="3ce65-166">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-166">True</span></span>                            |
| <span data-ttu-id="3ce65-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3ce65-167">Is-Single-Valued</span></span>       | <span data-ttu-id="3ce65-168">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-168">True</span></span>                            |
| <span data-ttu-id="3ce65-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3ce65-169">Is Indexed</span></span>             | <span data-ttu-id="3ce65-170">False</span><span class="sxs-lookup"><span data-stu-id="3ce65-170">False</span></span>                           |
| <span data-ttu-id="3ce65-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ce65-171">In Global Catalog</span></span>      | <span data-ttu-id="3ce65-172">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-172">True</span></span>                            |
| <span data-ttu-id="3ce65-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3ce65-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ce65-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ce65-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3ce65-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ce65-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3ce65-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ce65-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3ce65-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-177">Search-Flags</span></span>           | <span data-ttu-id="3ce65-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ce65-178">0x00000000</span></span>                      |
| <span data-ttu-id="3ce65-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-179">System-Flags</span></span>           | <span data-ttu-id="3ce65-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3ce65-180">0x00000013</span></span>                      |
| <span data-ttu-id="3ce65-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3ce65-181">Classes used in</span></span>        | [<span data-ttu-id="3ce65-182">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="3ce65-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3ce65-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="3ce65-183">ADAM</span></span>



| <span data-ttu-id="3ce65-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ce65-184">Entry</span></span> | <span data-ttu-id="3ce65-185">Value</span><span class="sxs-lookup"><span data-stu-id="3ce65-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3ce65-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3ce65-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3ce65-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ce65-187">MAPI-Id</span></span>                | <span data-ttu-id="3ce65-188">0x3008</span><span class="sxs-lookup"><span data-stu-id="3ce65-188">0x3008</span></span>                          |
| <span data-ttu-id="3ce65-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ce65-189">System-Only</span></span>            | <span data-ttu-id="3ce65-190">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-190">True</span></span>                            |
| <span data-ttu-id="3ce65-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3ce65-191">Is-Single-Valued</span></span>       | <span data-ttu-id="3ce65-192">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-192">True</span></span>                            |
| <span data-ttu-id="3ce65-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3ce65-193">Is Indexed</span></span>             | <span data-ttu-id="3ce65-194">False</span><span class="sxs-lookup"><span data-stu-id="3ce65-194">False</span></span>                           |
| <span data-ttu-id="3ce65-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ce65-195">In Global Catalog</span></span>      | <span data-ttu-id="3ce65-196">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-196">True</span></span>                            |
| <span data-ttu-id="3ce65-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3ce65-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ce65-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ce65-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3ce65-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ce65-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3ce65-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ce65-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3ce65-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-201">Search-Flags</span></span>           | <span data-ttu-id="3ce65-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ce65-202">0x00000000</span></span>                      |
| <span data-ttu-id="3ce65-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-203">System-Flags</span></span>           | <span data-ttu-id="3ce65-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3ce65-204">0x00000013</span></span>                      |
| <span data-ttu-id="3ce65-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3ce65-205">Classes used in</span></span>        | [<span data-ttu-id="3ce65-206">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="3ce65-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3ce65-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3ce65-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3ce65-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ce65-208">Entry</span></span> | <span data-ttu-id="3ce65-209">Value</span><span class="sxs-lookup"><span data-stu-id="3ce65-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3ce65-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3ce65-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3ce65-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ce65-211">MAPI-Id</span></span>                | <span data-ttu-id="3ce65-212">0x3008</span><span class="sxs-lookup"><span data-stu-id="3ce65-212">0x3008</span></span>                          |
| <span data-ttu-id="3ce65-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ce65-213">System-Only</span></span>            | <span data-ttu-id="3ce65-214">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-214">True</span></span>                            |
| <span data-ttu-id="3ce65-215">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3ce65-215">Is-Single-Valued</span></span>       | <span data-ttu-id="3ce65-216">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-216">True</span></span>                            |
| <span data-ttu-id="3ce65-217">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3ce65-217">Is Indexed</span></span>             | <span data-ttu-id="3ce65-218">False</span><span class="sxs-lookup"><span data-stu-id="3ce65-218">False</span></span>                           |
| <span data-ttu-id="3ce65-219">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ce65-219">In Global Catalog</span></span>      | <span data-ttu-id="3ce65-220">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-220">True</span></span>                            |
| <span data-ttu-id="3ce65-221">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3ce65-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ce65-222">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ce65-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3ce65-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ce65-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3ce65-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ce65-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3ce65-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-225">Search-Flags</span></span>           | <span data-ttu-id="3ce65-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ce65-226">0x00000000</span></span>                      |
| <span data-ttu-id="3ce65-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-227">System-Flags</span></span>           | <span data-ttu-id="3ce65-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3ce65-228">0x00000013</span></span>                      |
| <span data-ttu-id="3ce65-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3ce65-229">Classes used in</span></span>        | [<span data-ttu-id="3ce65-230">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="3ce65-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3ce65-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ce65-231">Windows Server 2008</span></span>



| <span data-ttu-id="3ce65-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ce65-232">Entry</span></span> | <span data-ttu-id="3ce65-233">Value</span><span class="sxs-lookup"><span data-stu-id="3ce65-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3ce65-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3ce65-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3ce65-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ce65-235">MAPI-Id</span></span>                | <span data-ttu-id="3ce65-236">0x3008</span><span class="sxs-lookup"><span data-stu-id="3ce65-236">0x3008</span></span>                          |
| <span data-ttu-id="3ce65-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ce65-237">System-Only</span></span>            | <span data-ttu-id="3ce65-238">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-238">True</span></span>                            |
| <span data-ttu-id="3ce65-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3ce65-239">Is-Single-Valued</span></span>       | <span data-ttu-id="3ce65-240">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-240">True</span></span>                            |
| <span data-ttu-id="3ce65-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3ce65-241">Is Indexed</span></span>             | <span data-ttu-id="3ce65-242">False</span><span class="sxs-lookup"><span data-stu-id="3ce65-242">False</span></span>                           |
| <span data-ttu-id="3ce65-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ce65-243">In Global Catalog</span></span>      | <span data-ttu-id="3ce65-244">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-244">True</span></span>                            |
| <span data-ttu-id="3ce65-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3ce65-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ce65-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ce65-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3ce65-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ce65-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3ce65-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ce65-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3ce65-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-249">Search-Flags</span></span>           | <span data-ttu-id="3ce65-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ce65-250">0x00000000</span></span>                      |
| <span data-ttu-id="3ce65-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-251">System-Flags</span></span>           | <span data-ttu-id="3ce65-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3ce65-252">0x00000013</span></span>                      |
| <span data-ttu-id="3ce65-253">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3ce65-253">Classes used in</span></span>        | [<span data-ttu-id="3ce65-254">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="3ce65-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3ce65-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ce65-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3ce65-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ce65-256">Entry</span></span> | <span data-ttu-id="3ce65-257">Value</span><span class="sxs-lookup"><span data-stu-id="3ce65-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3ce65-258">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3ce65-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3ce65-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ce65-259">MAPI-Id</span></span>                | <span data-ttu-id="3ce65-260">0x3008</span><span class="sxs-lookup"><span data-stu-id="3ce65-260">0x3008</span></span>                          |
| <span data-ttu-id="3ce65-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ce65-261">System-Only</span></span>            | <span data-ttu-id="3ce65-262">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-262">True</span></span>                            |
| <span data-ttu-id="3ce65-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3ce65-263">Is-Single-Valued</span></span>       | <span data-ttu-id="3ce65-264">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-264">True</span></span>                            |
| <span data-ttu-id="3ce65-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3ce65-265">Is Indexed</span></span>             | <span data-ttu-id="3ce65-266">False</span><span class="sxs-lookup"><span data-stu-id="3ce65-266">False</span></span>                           |
| <span data-ttu-id="3ce65-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ce65-267">In Global Catalog</span></span>      | <span data-ttu-id="3ce65-268">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-268">True</span></span>                            |
| <span data-ttu-id="3ce65-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3ce65-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ce65-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ce65-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3ce65-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ce65-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3ce65-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ce65-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3ce65-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-273">Search-Flags</span></span>           | <span data-ttu-id="3ce65-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ce65-274">0x00000000</span></span>                      |
| <span data-ttu-id="3ce65-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-275">System-Flags</span></span>           | <span data-ttu-id="3ce65-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3ce65-276">0x00000013</span></span>                      |
| <span data-ttu-id="3ce65-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3ce65-277">Classes used in</span></span>        | [<span data-ttu-id="3ce65-278">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="3ce65-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3ce65-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3ce65-279">Windows Server 2012</span></span>



| <span data-ttu-id="3ce65-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ce65-280">Entry</span></span> | <span data-ttu-id="3ce65-281">Value</span><span class="sxs-lookup"><span data-stu-id="3ce65-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3ce65-282">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="3ce65-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3ce65-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3ce65-283">MAPI-Id</span></span>                | <span data-ttu-id="3ce65-284">0x3008</span><span class="sxs-lookup"><span data-stu-id="3ce65-284">0x3008</span></span>                          |
| <span data-ttu-id="3ce65-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="3ce65-285">System-Only</span></span>            | <span data-ttu-id="3ce65-286">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-286">True</span></span>                            |
| <span data-ttu-id="3ce65-287">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="3ce65-287">Is-Single-Valued</span></span>       | <span data-ttu-id="3ce65-288">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-288">True</span></span>                            |
| <span data-ttu-id="3ce65-289">Está indexado</span><span class="sxs-lookup"><span data-stu-id="3ce65-289">Is Indexed</span></span>             | <span data-ttu-id="3ce65-290">False</span><span class="sxs-lookup"><span data-stu-id="3ce65-290">False</span></span>                           |
| <span data-ttu-id="3ce65-291">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="3ce65-291">In Global Catalog</span></span>      | <span data-ttu-id="3ce65-292">True</span><span class="sxs-lookup"><span data-stu-id="3ce65-292">True</span></span>                            |
| <span data-ttu-id="3ce65-293">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="3ce65-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="3ce65-294">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3ce65-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3ce65-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3ce65-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3ce65-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3ce65-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3ce65-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-297">Search-Flags</span></span>           | <span data-ttu-id="3ce65-298">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3ce65-298">0x00000000</span></span>                      |
| <span data-ttu-id="3ce65-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3ce65-299">System-Flags</span></span>           | <span data-ttu-id="3ce65-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3ce65-300">0x00000013</span></span>                      |
| <span data-ttu-id="3ce65-301">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="3ce65-301">Classes used in</span></span>        | [<span data-ttu-id="3ce65-302">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="3ce65-302">**Top**</span></span>](c-top.md)<br/> |



 

 






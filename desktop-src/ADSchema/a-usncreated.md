---
title: USN-Created atributo)
description: Número de secuencia de actualización (USN) asignado durante la creación del objeto. Vea también, USN-Changed.
ms.assetid: c38456b8-fc8f-4ea0-8f3d-e2bb3b44ff50
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de USN-Created
- uSNCreated esquema de AD de atributos
topic_type:
- apiref
api_name:
- USN-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b950ddfe261de5d46980e51b236da0f775fcb01b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658717"
---
# <a name="usn-created-attribute"></a><span data-ttu-id="f9020-106">USN-Created atributo)</span><span class="sxs-lookup"><span data-stu-id="f9020-106">USN-Created attribute</span></span>

<span data-ttu-id="f9020-107">Número de secuencia de actualización (USN) asignado durante la creación del objeto.</span><span class="sxs-lookup"><span data-stu-id="f9020-107">The update sequence number (USN) assigned at object creation.</span></span> <span data-ttu-id="f9020-108">Vea también, [**USN-Changed**](a-usnchanged.md).</span><span class="sxs-lookup"><span data-stu-id="f9020-108">See also, [**USN-Changed**](a-usnchanged.md).</span></span>



| <span data-ttu-id="f9020-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9020-109">Entry</span></span> | <span data-ttu-id="f9020-110">Value</span><span class="sxs-lookup"><span data-stu-id="f9020-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f9020-111">CN</span><span class="sxs-lookup"><span data-stu-id="f9020-111">CN</span></span>                | <span data-ttu-id="f9020-112">USN-Created</span><span class="sxs-lookup"><span data-stu-id="f9020-112">USN-Created</span></span>                          |
| <span data-ttu-id="f9020-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f9020-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f9020-114">uSNCreated</span><span class="sxs-lookup"><span data-stu-id="f9020-114">uSNCreated</span></span>                           |
| <span data-ttu-id="f9020-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f9020-115">Size</span></span>              | <span data-ttu-id="f9020-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="f9020-116">8 bytes</span></span>                              |
| <span data-ttu-id="f9020-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f9020-117">Update Privilege</span></span>  | <span data-ttu-id="f9020-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="f9020-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="f9020-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f9020-119">Update Frequency</span></span>  | <span data-ttu-id="f9020-120">Cuando se crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="f9020-120">When the object is created.</span></span>          |
| <span data-ttu-id="f9020-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f9020-121">Attribute-Id</span></span>      | <span data-ttu-id="f9020-122">1.2.840.113556.1.2.19</span><span class="sxs-lookup"><span data-stu-id="f9020-122">1.2.840.113556.1.2.19</span></span>                |
| <span data-ttu-id="f9020-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f9020-123">System-Id-Guid</span></span>    | <span data-ttu-id="f9020-124">bf967a70-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f9020-124">bf967a70-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="f9020-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9020-125">Syntax</span></span>            | [<span data-ttu-id="f9020-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="f9020-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f9020-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f9020-127">Implementations</span></span>

-   [<span data-ttu-id="f9020-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f9020-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f9020-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f9020-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f9020-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f9020-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f9020-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f9020-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f9020-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f9020-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f9020-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f9020-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f9020-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f9020-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f9020-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9020-135">Windows 2000 Server</span></span>



| <span data-ttu-id="f9020-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9020-136">Entry</span></span> | <span data-ttu-id="f9020-137">Value</span><span class="sxs-lookup"><span data-stu-id="f9020-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9020-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f9020-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9020-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9020-139">MAPI-Id</span></span>                | <span data-ttu-id="f9020-140">0x8154</span><span class="sxs-lookup"><span data-stu-id="f9020-140">0x8154</span></span>                          |
| <span data-ttu-id="f9020-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9020-141">System-Only</span></span>            | <span data-ttu-id="f9020-142">True</span><span class="sxs-lookup"><span data-stu-id="f9020-142">True</span></span>                            |
| <span data-ttu-id="f9020-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f9020-143">Is-Single-Valued</span></span>       | <span data-ttu-id="f9020-144">True</span><span class="sxs-lookup"><span data-stu-id="f9020-144">True</span></span>                            |
| <span data-ttu-id="f9020-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f9020-145">Is Indexed</span></span>             | <span data-ttu-id="f9020-146">True</span><span class="sxs-lookup"><span data-stu-id="f9020-146">True</span></span>                            |
| <span data-ttu-id="f9020-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9020-147">In Global Catalog</span></span>      | <span data-ttu-id="f9020-148">True</span><span class="sxs-lookup"><span data-stu-id="f9020-148">True</span></span>                            |
| <span data-ttu-id="f9020-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f9020-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9020-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9020-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9020-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9020-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f9020-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9020-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f9020-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-153">Search-Flags</span></span>           | <span data-ttu-id="f9020-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f9020-154">0x00000009</span></span>                      |
| <span data-ttu-id="f9020-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-155">System-Flags</span></span>           | <span data-ttu-id="f9020-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f9020-156">0x00000013</span></span>                      |
| <span data-ttu-id="f9020-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f9020-157">Classes used in</span></span>        | [<span data-ttu-id="f9020-158">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="f9020-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f9020-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9020-159">Windows Server 2003</span></span>



| <span data-ttu-id="f9020-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9020-160">Entry</span></span> | <span data-ttu-id="f9020-161">Value</span><span class="sxs-lookup"><span data-stu-id="f9020-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9020-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f9020-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9020-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9020-163">MAPI-Id</span></span>                | <span data-ttu-id="f9020-164">0x8154</span><span class="sxs-lookup"><span data-stu-id="f9020-164">0x8154</span></span>                          |
| <span data-ttu-id="f9020-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9020-165">System-Only</span></span>            | <span data-ttu-id="f9020-166">True</span><span class="sxs-lookup"><span data-stu-id="f9020-166">True</span></span>                            |
| <span data-ttu-id="f9020-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f9020-167">Is-Single-Valued</span></span>       | <span data-ttu-id="f9020-168">True</span><span class="sxs-lookup"><span data-stu-id="f9020-168">True</span></span>                            |
| <span data-ttu-id="f9020-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f9020-169">Is Indexed</span></span>             | <span data-ttu-id="f9020-170">True</span><span class="sxs-lookup"><span data-stu-id="f9020-170">True</span></span>                            |
| <span data-ttu-id="f9020-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9020-171">In Global Catalog</span></span>      | <span data-ttu-id="f9020-172">True</span><span class="sxs-lookup"><span data-stu-id="f9020-172">True</span></span>                            |
| <span data-ttu-id="f9020-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f9020-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9020-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9020-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9020-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9020-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f9020-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9020-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f9020-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-177">Search-Flags</span></span>           | <span data-ttu-id="f9020-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f9020-178">0x00000009</span></span>                      |
| <span data-ttu-id="f9020-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-179">System-Flags</span></span>           | <span data-ttu-id="f9020-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f9020-180">0x00000013</span></span>                      |
| <span data-ttu-id="f9020-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f9020-181">Classes used in</span></span>        | [<span data-ttu-id="f9020-182">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="f9020-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f9020-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="f9020-183">ADAM</span></span>



| <span data-ttu-id="f9020-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9020-184">Entry</span></span> | <span data-ttu-id="f9020-185">Value</span><span class="sxs-lookup"><span data-stu-id="f9020-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9020-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f9020-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9020-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9020-187">MAPI-Id</span></span>                | <span data-ttu-id="f9020-188">0x8154</span><span class="sxs-lookup"><span data-stu-id="f9020-188">0x8154</span></span>                          |
| <span data-ttu-id="f9020-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9020-189">System-Only</span></span>            | <span data-ttu-id="f9020-190">True</span><span class="sxs-lookup"><span data-stu-id="f9020-190">True</span></span>                            |
| <span data-ttu-id="f9020-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f9020-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f9020-192">True</span><span class="sxs-lookup"><span data-stu-id="f9020-192">True</span></span>                            |
| <span data-ttu-id="f9020-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f9020-193">Is Indexed</span></span>             | <span data-ttu-id="f9020-194">True</span><span class="sxs-lookup"><span data-stu-id="f9020-194">True</span></span>                            |
| <span data-ttu-id="f9020-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9020-195">In Global Catalog</span></span>      | <span data-ttu-id="f9020-196">True</span><span class="sxs-lookup"><span data-stu-id="f9020-196">True</span></span>                            |
| <span data-ttu-id="f9020-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f9020-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9020-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9020-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9020-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9020-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f9020-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9020-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f9020-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-201">Search-Flags</span></span>           | <span data-ttu-id="f9020-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f9020-202">0x00000009</span></span>                      |
| <span data-ttu-id="f9020-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-203">System-Flags</span></span>           | <span data-ttu-id="f9020-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f9020-204">0x00000013</span></span>                      |
| <span data-ttu-id="f9020-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f9020-205">Classes used in</span></span>        | [<span data-ttu-id="f9020-206">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="f9020-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f9020-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f9020-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f9020-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9020-208">Entry</span></span> | <span data-ttu-id="f9020-209">Value</span><span class="sxs-lookup"><span data-stu-id="f9020-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9020-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f9020-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9020-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9020-211">MAPI-Id</span></span>                | <span data-ttu-id="f9020-212">0x8154</span><span class="sxs-lookup"><span data-stu-id="f9020-212">0x8154</span></span>                          |
| <span data-ttu-id="f9020-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9020-213">System-Only</span></span>            | <span data-ttu-id="f9020-214">True</span><span class="sxs-lookup"><span data-stu-id="f9020-214">True</span></span>                            |
| <span data-ttu-id="f9020-215">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f9020-215">Is-Single-Valued</span></span>       | <span data-ttu-id="f9020-216">True</span><span class="sxs-lookup"><span data-stu-id="f9020-216">True</span></span>                            |
| <span data-ttu-id="f9020-217">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f9020-217">Is Indexed</span></span>             | <span data-ttu-id="f9020-218">True</span><span class="sxs-lookup"><span data-stu-id="f9020-218">True</span></span>                            |
| <span data-ttu-id="f9020-219">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9020-219">In Global Catalog</span></span>      | <span data-ttu-id="f9020-220">True</span><span class="sxs-lookup"><span data-stu-id="f9020-220">True</span></span>                            |
| <span data-ttu-id="f9020-221">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f9020-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9020-222">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9020-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9020-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9020-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f9020-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9020-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f9020-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-225">Search-Flags</span></span>           | <span data-ttu-id="f9020-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f9020-226">0x00000009</span></span>                      |
| <span data-ttu-id="f9020-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-227">System-Flags</span></span>           | <span data-ttu-id="f9020-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f9020-228">0x00000013</span></span>                      |
| <span data-ttu-id="f9020-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f9020-229">Classes used in</span></span>        | [<span data-ttu-id="f9020-230">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="f9020-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f9020-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9020-231">Windows Server 2008</span></span>



| <span data-ttu-id="f9020-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9020-232">Entry</span></span> | <span data-ttu-id="f9020-233">Value</span><span class="sxs-lookup"><span data-stu-id="f9020-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9020-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f9020-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9020-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9020-235">MAPI-Id</span></span>                | <span data-ttu-id="f9020-236">0x8154</span><span class="sxs-lookup"><span data-stu-id="f9020-236">0x8154</span></span>                          |
| <span data-ttu-id="f9020-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9020-237">System-Only</span></span>            | <span data-ttu-id="f9020-238">True</span><span class="sxs-lookup"><span data-stu-id="f9020-238">True</span></span>                            |
| <span data-ttu-id="f9020-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f9020-239">Is-Single-Valued</span></span>       | <span data-ttu-id="f9020-240">True</span><span class="sxs-lookup"><span data-stu-id="f9020-240">True</span></span>                            |
| <span data-ttu-id="f9020-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f9020-241">Is Indexed</span></span>             | <span data-ttu-id="f9020-242">True</span><span class="sxs-lookup"><span data-stu-id="f9020-242">True</span></span>                            |
| <span data-ttu-id="f9020-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9020-243">In Global Catalog</span></span>      | <span data-ttu-id="f9020-244">True</span><span class="sxs-lookup"><span data-stu-id="f9020-244">True</span></span>                            |
| <span data-ttu-id="f9020-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f9020-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9020-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9020-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9020-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9020-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f9020-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9020-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f9020-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-249">Search-Flags</span></span>           | <span data-ttu-id="f9020-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f9020-250">0x00000009</span></span>                      |
| <span data-ttu-id="f9020-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-251">System-Flags</span></span>           | <span data-ttu-id="f9020-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f9020-252">0x00000013</span></span>                      |
| <span data-ttu-id="f9020-253">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f9020-253">Classes used in</span></span>        | [<span data-ttu-id="f9020-254">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="f9020-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f9020-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9020-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f9020-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9020-256">Entry</span></span> | <span data-ttu-id="f9020-257">Value</span><span class="sxs-lookup"><span data-stu-id="f9020-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9020-258">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f9020-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9020-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9020-259">MAPI-Id</span></span>                | <span data-ttu-id="f9020-260">0x8154</span><span class="sxs-lookup"><span data-stu-id="f9020-260">0x8154</span></span>                          |
| <span data-ttu-id="f9020-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9020-261">System-Only</span></span>            | <span data-ttu-id="f9020-262">True</span><span class="sxs-lookup"><span data-stu-id="f9020-262">True</span></span>                            |
| <span data-ttu-id="f9020-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f9020-263">Is-Single-Valued</span></span>       | <span data-ttu-id="f9020-264">True</span><span class="sxs-lookup"><span data-stu-id="f9020-264">True</span></span>                            |
| <span data-ttu-id="f9020-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f9020-265">Is Indexed</span></span>             | <span data-ttu-id="f9020-266">True</span><span class="sxs-lookup"><span data-stu-id="f9020-266">True</span></span>                            |
| <span data-ttu-id="f9020-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9020-267">In Global Catalog</span></span>      | <span data-ttu-id="f9020-268">True</span><span class="sxs-lookup"><span data-stu-id="f9020-268">True</span></span>                            |
| <span data-ttu-id="f9020-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f9020-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9020-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9020-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9020-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9020-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f9020-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9020-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f9020-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-273">Search-Flags</span></span>           | <span data-ttu-id="f9020-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f9020-274">0x00000009</span></span>                      |
| <span data-ttu-id="f9020-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-275">System-Flags</span></span>           | <span data-ttu-id="f9020-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f9020-276">0x00000013</span></span>                      |
| <span data-ttu-id="f9020-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f9020-277">Classes used in</span></span>        | [<span data-ttu-id="f9020-278">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="f9020-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f9020-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9020-279">Windows Server 2012</span></span>



| <span data-ttu-id="f9020-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9020-280">Entry</span></span> | <span data-ttu-id="f9020-281">Value</span><span class="sxs-lookup"><span data-stu-id="f9020-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f9020-282">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f9020-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f9020-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9020-283">MAPI-Id</span></span>                | <span data-ttu-id="f9020-284">0x8154</span><span class="sxs-lookup"><span data-stu-id="f9020-284">0x8154</span></span>                          |
| <span data-ttu-id="f9020-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9020-285">System-Only</span></span>            | <span data-ttu-id="f9020-286">True</span><span class="sxs-lookup"><span data-stu-id="f9020-286">True</span></span>                            |
| <span data-ttu-id="f9020-287">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f9020-287">Is-Single-Valued</span></span>       | <span data-ttu-id="f9020-288">True</span><span class="sxs-lookup"><span data-stu-id="f9020-288">True</span></span>                            |
| <span data-ttu-id="f9020-289">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f9020-289">Is Indexed</span></span>             | <span data-ttu-id="f9020-290">True</span><span class="sxs-lookup"><span data-stu-id="f9020-290">True</span></span>                            |
| <span data-ttu-id="f9020-291">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f9020-291">In Global Catalog</span></span>      | <span data-ttu-id="f9020-292">True</span><span class="sxs-lookup"><span data-stu-id="f9020-292">True</span></span>                            |
| <span data-ttu-id="f9020-293">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f9020-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9020-294">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9020-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f9020-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9020-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f9020-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9020-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f9020-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-297">Search-Flags</span></span>           | <span data-ttu-id="f9020-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="f9020-298">0x00000009</span></span>                      |
| <span data-ttu-id="f9020-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9020-299">System-Flags</span></span>           | <span data-ttu-id="f9020-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="f9020-300">0x00000013</span></span>                      |
| <span data-ttu-id="f9020-301">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f9020-301">Classes used in</span></span>        | [<span data-ttu-id="f9020-302">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="f9020-302">**Top**</span></span>](c-top.md)<br/> |



 

 






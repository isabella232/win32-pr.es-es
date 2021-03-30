---
title: USN-Changed atributo)
description: El número de secuencia de actualización (USN) asignado por el directorio local para el cambio más reciente, incluida la creación. Vea también USN-created.
ms.assetid: ccd61940-2c0a-4d46-af9f-5f23f577a1ad
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de USN-Changed
- Esquema de AD de atributo uSNChanged
topic_type:
- apiref
api_name:
- USN-Changed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c00f30a2ba7ca38f78246cd14b33ea358da6fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804801"
---
# <a name="usn-changed-attribute"></a><span data-ttu-id="6c115-106">USN-Changed atributo)</span><span class="sxs-lookup"><span data-stu-id="6c115-106">USN-Changed attribute</span></span>

<span data-ttu-id="6c115-107">El número de secuencia de actualización (USN) asignado por el directorio local para el cambio más reciente, incluida la creación.</span><span class="sxs-lookup"><span data-stu-id="6c115-107">The update sequence number (USN) assigned by the local directory for the latest change, including creation.</span></span> <span data-ttu-id="6c115-108">Vea también [**USN-created**](a-usncreated.md).</span><span class="sxs-lookup"><span data-stu-id="6c115-108">See also , [**USN-Created**](a-usncreated.md).</span></span>



| <span data-ttu-id="6c115-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c115-109">Entry</span></span> | <span data-ttu-id="6c115-110">Value</span><span class="sxs-lookup"><span data-stu-id="6c115-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6c115-111">CN</span><span class="sxs-lookup"><span data-stu-id="6c115-111">CN</span></span>                | <span data-ttu-id="6c115-112">USN-Changed</span><span class="sxs-lookup"><span data-stu-id="6c115-112">USN-Changed</span></span>                          |
| <span data-ttu-id="6c115-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6c115-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6c115-114">uSNChanged</span><span class="sxs-lookup"><span data-stu-id="6c115-114">uSNChanged</span></span>                           |
| <span data-ttu-id="6c115-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6c115-115">Size</span></span>              | <span data-ttu-id="6c115-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="6c115-116">8 bytes</span></span>                              |
| <span data-ttu-id="6c115-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6c115-117">Update Privilege</span></span>  | <span data-ttu-id="6c115-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="6c115-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="6c115-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6c115-119">Update Frequency</span></span>  | <span data-ttu-id="6c115-120">Cuando se cambia el objeto.</span><span class="sxs-lookup"><span data-stu-id="6c115-120">When the object is changed.</span></span>          |
| <span data-ttu-id="6c115-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c115-121">Attribute-Id</span></span>      | <span data-ttu-id="6c115-122">1.2.840.113556.1.2.120</span><span class="sxs-lookup"><span data-stu-id="6c115-122">1.2.840.113556.1.2.120</span></span>               |
| <span data-ttu-id="6c115-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6c115-123">System-Id-Guid</span></span>    | <span data-ttu-id="6c115-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6c115-124">bf967a6f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="6c115-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c115-125">Syntax</span></span>            | [<span data-ttu-id="6c115-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="6c115-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="6c115-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6c115-127">Implementations</span></span>

-   [<span data-ttu-id="6c115-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6c115-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6c115-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6c115-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6c115-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6c115-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6c115-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c115-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c115-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c115-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c115-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c115-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c115-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c115-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6c115-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c115-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6c115-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c115-136">Entry</span></span> | <span data-ttu-id="6c115-137">Value</span><span class="sxs-lookup"><span data-stu-id="6c115-137">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c115-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c115-138">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c115-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c115-139">MAPI-Id</span></span>                | <span data-ttu-id="6c115-140">0x8029</span><span class="sxs-lookup"><span data-stu-id="6c115-140">0x8029</span></span>                          |
| <span data-ttu-id="6c115-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c115-141">System-Only</span></span>            | <span data-ttu-id="6c115-142">True</span><span class="sxs-lookup"><span data-stu-id="6c115-142">True</span></span>                            |
| <span data-ttu-id="6c115-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c115-143">Is-Single-Valued</span></span>       | <span data-ttu-id="6c115-144">True</span><span class="sxs-lookup"><span data-stu-id="6c115-144">True</span></span>                            |
| <span data-ttu-id="6c115-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c115-145">Is Indexed</span></span>             | <span data-ttu-id="6c115-146">True</span><span class="sxs-lookup"><span data-stu-id="6c115-146">True</span></span>                            |
| <span data-ttu-id="6c115-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c115-147">In Global Catalog</span></span>      | <span data-ttu-id="6c115-148">True</span><span class="sxs-lookup"><span data-stu-id="6c115-148">True</span></span>                            |
| <span data-ttu-id="6c115-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c115-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c115-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c115-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c115-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c115-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6c115-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c115-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6c115-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-153">Search-Flags</span></span>           | <span data-ttu-id="6c115-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6c115-154">0x00000009</span></span>                      |
| <span data-ttu-id="6c115-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-155">System-Flags</span></span>           | <span data-ttu-id="6c115-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6c115-156">0x00000013</span></span>                      |
| <span data-ttu-id="6c115-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c115-157">Classes used in</span></span>        | [<span data-ttu-id="6c115-158">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6c115-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6c115-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c115-159">Windows Server 2003</span></span>



| <span data-ttu-id="6c115-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c115-160">Entry</span></span> | <span data-ttu-id="6c115-161">Value</span><span class="sxs-lookup"><span data-stu-id="6c115-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c115-162">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c115-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c115-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c115-163">MAPI-Id</span></span>                | <span data-ttu-id="6c115-164">0x8029</span><span class="sxs-lookup"><span data-stu-id="6c115-164">0x8029</span></span>                          |
| <span data-ttu-id="6c115-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c115-165">System-Only</span></span>            | <span data-ttu-id="6c115-166">True</span><span class="sxs-lookup"><span data-stu-id="6c115-166">True</span></span>                            |
| <span data-ttu-id="6c115-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c115-167">Is-Single-Valued</span></span>       | <span data-ttu-id="6c115-168">True</span><span class="sxs-lookup"><span data-stu-id="6c115-168">True</span></span>                            |
| <span data-ttu-id="6c115-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c115-169">Is Indexed</span></span>             | <span data-ttu-id="6c115-170">True</span><span class="sxs-lookup"><span data-stu-id="6c115-170">True</span></span>                            |
| <span data-ttu-id="6c115-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c115-171">In Global Catalog</span></span>      | <span data-ttu-id="6c115-172">True</span><span class="sxs-lookup"><span data-stu-id="6c115-172">True</span></span>                            |
| <span data-ttu-id="6c115-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c115-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c115-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c115-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c115-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c115-175">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6c115-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c115-176">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6c115-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-177">Search-Flags</span></span>           | <span data-ttu-id="6c115-178">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6c115-178">0x00000009</span></span>                      |
| <span data-ttu-id="6c115-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-179">System-Flags</span></span>           | <span data-ttu-id="6c115-180">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6c115-180">0x00000013</span></span>                      |
| <span data-ttu-id="6c115-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c115-181">Classes used in</span></span>        | [<span data-ttu-id="6c115-182">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6c115-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6c115-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="6c115-183">ADAM</span></span>



| <span data-ttu-id="6c115-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c115-184">Entry</span></span> | <span data-ttu-id="6c115-185">Value</span><span class="sxs-lookup"><span data-stu-id="6c115-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c115-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c115-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c115-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c115-187">MAPI-Id</span></span>                | <span data-ttu-id="6c115-188">0x8029</span><span class="sxs-lookup"><span data-stu-id="6c115-188">0x8029</span></span>                          |
| <span data-ttu-id="6c115-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c115-189">System-Only</span></span>            | <span data-ttu-id="6c115-190">True</span><span class="sxs-lookup"><span data-stu-id="6c115-190">True</span></span>                            |
| <span data-ttu-id="6c115-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c115-191">Is-Single-Valued</span></span>       | <span data-ttu-id="6c115-192">True</span><span class="sxs-lookup"><span data-stu-id="6c115-192">True</span></span>                            |
| <span data-ttu-id="6c115-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c115-193">Is Indexed</span></span>             | <span data-ttu-id="6c115-194">True</span><span class="sxs-lookup"><span data-stu-id="6c115-194">True</span></span>                            |
| <span data-ttu-id="6c115-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c115-195">In Global Catalog</span></span>      | <span data-ttu-id="6c115-196">True</span><span class="sxs-lookup"><span data-stu-id="6c115-196">True</span></span>                            |
| <span data-ttu-id="6c115-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c115-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c115-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c115-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c115-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c115-199">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6c115-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c115-200">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6c115-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-201">Search-Flags</span></span>           | <span data-ttu-id="6c115-202">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6c115-202">0x00000009</span></span>                      |
| <span data-ttu-id="6c115-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-203">System-Flags</span></span>           | <span data-ttu-id="6c115-204">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6c115-204">0x00000013</span></span>                      |
| <span data-ttu-id="6c115-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c115-205">Classes used in</span></span>        | [<span data-ttu-id="6c115-206">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6c115-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c115-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c115-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c115-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c115-208">Entry</span></span> | <span data-ttu-id="6c115-209">Value</span><span class="sxs-lookup"><span data-stu-id="6c115-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c115-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c115-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c115-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c115-211">MAPI-Id</span></span>                | <span data-ttu-id="6c115-212">0x8029</span><span class="sxs-lookup"><span data-stu-id="6c115-212">0x8029</span></span>                          |
| <span data-ttu-id="6c115-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c115-213">System-Only</span></span>            | <span data-ttu-id="6c115-214">True</span><span class="sxs-lookup"><span data-stu-id="6c115-214">True</span></span>                            |
| <span data-ttu-id="6c115-215">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c115-215">Is-Single-Valued</span></span>       | <span data-ttu-id="6c115-216">True</span><span class="sxs-lookup"><span data-stu-id="6c115-216">True</span></span>                            |
| <span data-ttu-id="6c115-217">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c115-217">Is Indexed</span></span>             | <span data-ttu-id="6c115-218">True</span><span class="sxs-lookup"><span data-stu-id="6c115-218">True</span></span>                            |
| <span data-ttu-id="6c115-219">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c115-219">In Global Catalog</span></span>      | <span data-ttu-id="6c115-220">True</span><span class="sxs-lookup"><span data-stu-id="6c115-220">True</span></span>                            |
| <span data-ttu-id="6c115-221">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c115-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c115-222">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c115-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c115-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c115-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6c115-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c115-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6c115-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-225">Search-Flags</span></span>           | <span data-ttu-id="6c115-226">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6c115-226">0x00000009</span></span>                      |
| <span data-ttu-id="6c115-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-227">System-Flags</span></span>           | <span data-ttu-id="6c115-228">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6c115-228">0x00000013</span></span>                      |
| <span data-ttu-id="6c115-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c115-229">Classes used in</span></span>        | [<span data-ttu-id="6c115-230">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6c115-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c115-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c115-231">Windows Server 2008</span></span>



| <span data-ttu-id="6c115-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c115-232">Entry</span></span> | <span data-ttu-id="6c115-233">Value</span><span class="sxs-lookup"><span data-stu-id="6c115-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c115-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c115-234">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c115-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c115-235">MAPI-Id</span></span>                | <span data-ttu-id="6c115-236">0x8029</span><span class="sxs-lookup"><span data-stu-id="6c115-236">0x8029</span></span>                          |
| <span data-ttu-id="6c115-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c115-237">System-Only</span></span>            | <span data-ttu-id="6c115-238">True</span><span class="sxs-lookup"><span data-stu-id="6c115-238">True</span></span>                            |
| <span data-ttu-id="6c115-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c115-239">Is-Single-Valued</span></span>       | <span data-ttu-id="6c115-240">True</span><span class="sxs-lookup"><span data-stu-id="6c115-240">True</span></span>                            |
| <span data-ttu-id="6c115-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c115-241">Is Indexed</span></span>             | <span data-ttu-id="6c115-242">True</span><span class="sxs-lookup"><span data-stu-id="6c115-242">True</span></span>                            |
| <span data-ttu-id="6c115-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c115-243">In Global Catalog</span></span>      | <span data-ttu-id="6c115-244">True</span><span class="sxs-lookup"><span data-stu-id="6c115-244">True</span></span>                            |
| <span data-ttu-id="6c115-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c115-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c115-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c115-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c115-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c115-247">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6c115-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c115-248">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6c115-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-249">Search-Flags</span></span>           | <span data-ttu-id="6c115-250">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6c115-250">0x00000009</span></span>                      |
| <span data-ttu-id="6c115-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-251">System-Flags</span></span>           | <span data-ttu-id="6c115-252">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6c115-252">0x00000013</span></span>                      |
| <span data-ttu-id="6c115-253">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c115-253">Classes used in</span></span>        | [<span data-ttu-id="6c115-254">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6c115-254">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c115-255">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c115-255">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c115-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c115-256">Entry</span></span> | <span data-ttu-id="6c115-257">Value</span><span class="sxs-lookup"><span data-stu-id="6c115-257">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c115-258">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c115-258">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c115-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c115-259">MAPI-Id</span></span>                | <span data-ttu-id="6c115-260">0x8029</span><span class="sxs-lookup"><span data-stu-id="6c115-260">0x8029</span></span>                          |
| <span data-ttu-id="6c115-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c115-261">System-Only</span></span>            | <span data-ttu-id="6c115-262">True</span><span class="sxs-lookup"><span data-stu-id="6c115-262">True</span></span>                            |
| <span data-ttu-id="6c115-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c115-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6c115-264">True</span><span class="sxs-lookup"><span data-stu-id="6c115-264">True</span></span>                            |
| <span data-ttu-id="6c115-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c115-265">Is Indexed</span></span>             | <span data-ttu-id="6c115-266">True</span><span class="sxs-lookup"><span data-stu-id="6c115-266">True</span></span>                            |
| <span data-ttu-id="6c115-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c115-267">In Global Catalog</span></span>      | <span data-ttu-id="6c115-268">True</span><span class="sxs-lookup"><span data-stu-id="6c115-268">True</span></span>                            |
| <span data-ttu-id="6c115-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c115-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c115-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c115-270">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c115-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c115-271">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6c115-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c115-272">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6c115-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-273">Search-Flags</span></span>           | <span data-ttu-id="6c115-274">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6c115-274">0x00000009</span></span>                      |
| <span data-ttu-id="6c115-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-275">System-Flags</span></span>           | <span data-ttu-id="6c115-276">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6c115-276">0x00000013</span></span>                      |
| <span data-ttu-id="6c115-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c115-277">Classes used in</span></span>        | [<span data-ttu-id="6c115-278">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6c115-278">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c115-279">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c115-279">Windows Server 2012</span></span>



| <span data-ttu-id="6c115-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c115-280">Entry</span></span> | <span data-ttu-id="6c115-281">Value</span><span class="sxs-lookup"><span data-stu-id="6c115-281">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c115-282">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6c115-282">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c115-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c115-283">MAPI-Id</span></span>                | <span data-ttu-id="6c115-284">0x8029</span><span class="sxs-lookup"><span data-stu-id="6c115-284">0x8029</span></span>                          |
| <span data-ttu-id="6c115-285">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c115-285">System-Only</span></span>            | <span data-ttu-id="6c115-286">True</span><span class="sxs-lookup"><span data-stu-id="6c115-286">True</span></span>                            |
| <span data-ttu-id="6c115-287">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6c115-287">Is-Single-Valued</span></span>       | <span data-ttu-id="6c115-288">True</span><span class="sxs-lookup"><span data-stu-id="6c115-288">True</span></span>                            |
| <span data-ttu-id="6c115-289">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6c115-289">Is Indexed</span></span>             | <span data-ttu-id="6c115-290">True</span><span class="sxs-lookup"><span data-stu-id="6c115-290">True</span></span>                            |
| <span data-ttu-id="6c115-291">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c115-291">In Global Catalog</span></span>      | <span data-ttu-id="6c115-292">True</span><span class="sxs-lookup"><span data-stu-id="6c115-292">True</span></span>                            |
| <span data-ttu-id="6c115-293">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6c115-293">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c115-294">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c115-294">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c115-295">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c115-295">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="6c115-296">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c115-296">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="6c115-297">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-297">Search-Flags</span></span>           | <span data-ttu-id="6c115-298">0x00000009</span><span class="sxs-lookup"><span data-stu-id="6c115-298">0x00000009</span></span>                      |
| <span data-ttu-id="6c115-299">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c115-299">System-Flags</span></span>           | <span data-ttu-id="6c115-300">0x00000013</span><span class="sxs-lookup"><span data-stu-id="6c115-300">0x00000013</span></span>                      |
| <span data-ttu-id="6c115-301">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6c115-301">Classes used in</span></span>        | [<span data-ttu-id="6c115-302">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="6c115-302">**Top**</span></span>](c-top.md)<br/> |



 

 






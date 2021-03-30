---
title: Atributo Last-set-time
description: La última vez que se modificó el secreto.
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- Esquema de AD del último atributo de tiempo de establecimiento
- lastSetTime esquema de AD de atributos
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce123377fac6e67de1ba84b906c9498d0a064936
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422691"
---
# <a name="last-set-time-attribute"></a><span data-ttu-id="fde7c-105">Atributo Last-set-time</span><span class="sxs-lookup"><span data-stu-id="fde7c-105">Last-Set-Time attribute</span></span>

<span data-ttu-id="fde7c-106">La última vez que se modificó el secreto.</span><span class="sxs-lookup"><span data-stu-id="fde7c-106">The last time the secret was changed.</span></span> <span data-ttu-id="fde7c-107">Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="fde7c-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span>



| <span data-ttu-id="fde7c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="fde7c-108">Entry</span></span> | <span data-ttu-id="fde7c-109">Value</span><span class="sxs-lookup"><span data-stu-id="fde7c-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fde7c-110">CN</span><span class="sxs-lookup"><span data-stu-id="fde7c-110">CN</span></span>                | <span data-ttu-id="fde7c-111">Hora del último conjunto</span><span class="sxs-lookup"><span data-stu-id="fde7c-111">Last-Set-Time</span></span>                        |
| <span data-ttu-id="fde7c-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="fde7c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="fde7c-113">lastSetTime</span><span class="sxs-lookup"><span data-stu-id="fde7c-113">lastSetTime</span></span>                          |
| <span data-ttu-id="fde7c-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="fde7c-114">Size</span></span>              | <span data-ttu-id="fde7c-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="fde7c-115">8 bytes</span></span>                              |
| <span data-ttu-id="fde7c-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="fde7c-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fde7c-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="fde7c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fde7c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fde7c-118">Attribute-Id</span></span>      | <span data-ttu-id="fde7c-119">1.2.840.113556.1.4.53</span><span class="sxs-lookup"><span data-stu-id="fde7c-119">1.2.840.113556.1.4.53</span></span>                |
| <span data-ttu-id="fde7c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fde7c-120">System-Id-Guid</span></span>    | <span data-ttu-id="fde7c-121">bf967998-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="fde7c-121">bf967998-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="fde7c-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fde7c-122">Syntax</span></span>            | [<span data-ttu-id="fde7c-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="fde7c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="fde7c-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="fde7c-124">Implementations</span></span>

-   [<span data-ttu-id="fde7c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fde7c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fde7c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fde7c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fde7c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fde7c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fde7c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fde7c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fde7c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fde7c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fde7c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fde7c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fde7c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fde7c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="fde7c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="fde7c-132">Entry</span></span> | <span data-ttu-id="fde7c-133">Value</span><span class="sxs-lookup"><span data-stu-id="fde7c-133">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="fde7c-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fde7c-134">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fde7c-135">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fde7c-136">System-Only</span></span>            | <span data-ttu-id="fde7c-137">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-137">False</span></span>                                 |
| <span data-ttu-id="fde7c-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fde7c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fde7c-139">True</span><span class="sxs-lookup"><span data-stu-id="fde7c-139">True</span></span>                                  |
| <span data-ttu-id="fde7c-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fde7c-140">Is Indexed</span></span>             | <span data-ttu-id="fde7c-141">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-141">False</span></span>                                 |
| <span data-ttu-id="fde7c-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fde7c-142">In Global Catalog</span></span>      | <span data-ttu-id="fde7c-143">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-143">False</span></span>                                 |
| <span data-ttu-id="fde7c-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fde7c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fde7c-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fde7c-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="fde7c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fde7c-146">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fde7c-147">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-148">Search-Flags</span></span>           | <span data-ttu-id="fde7c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fde7c-149">0x00000000</span></span>                            |
| <span data-ttu-id="fde7c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-150">System-Flags</span></span>           | <span data-ttu-id="fde7c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fde7c-151">0x00000010</span></span>                            |
| <span data-ttu-id="fde7c-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fde7c-152">Classes used in</span></span>        | [<span data-ttu-id="fde7c-153">**Secreto**</span><span class="sxs-lookup"><span data-stu-id="fde7c-153">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fde7c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fde7c-154">Windows Server 2003</span></span>



| <span data-ttu-id="fde7c-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="fde7c-155">Entry</span></span> | <span data-ttu-id="fde7c-156">Value</span><span class="sxs-lookup"><span data-stu-id="fde7c-156">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="fde7c-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fde7c-157">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fde7c-158">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fde7c-159">System-Only</span></span>            | <span data-ttu-id="fde7c-160">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-160">False</span></span>                                 |
| <span data-ttu-id="fde7c-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fde7c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fde7c-162">True</span><span class="sxs-lookup"><span data-stu-id="fde7c-162">True</span></span>                                  |
| <span data-ttu-id="fde7c-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fde7c-163">Is Indexed</span></span>             | <span data-ttu-id="fde7c-164">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-164">False</span></span>                                 |
| <span data-ttu-id="fde7c-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fde7c-165">In Global Catalog</span></span>      | <span data-ttu-id="fde7c-166">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-166">False</span></span>                                 |
| <span data-ttu-id="fde7c-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fde7c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fde7c-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fde7c-168">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="fde7c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fde7c-169">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fde7c-170">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-171">Search-Flags</span></span>           | <span data-ttu-id="fde7c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fde7c-172">0x00000000</span></span>                            |
| <span data-ttu-id="fde7c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-173">System-Flags</span></span>           | <span data-ttu-id="fde7c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fde7c-174">0x00000010</span></span>                            |
| <span data-ttu-id="fde7c-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fde7c-175">Classes used in</span></span>        | [<span data-ttu-id="fde7c-176">**Secreto**</span><span class="sxs-lookup"><span data-stu-id="fde7c-176">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fde7c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fde7c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fde7c-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="fde7c-178">Entry</span></span> | <span data-ttu-id="fde7c-179">Value</span><span class="sxs-lookup"><span data-stu-id="fde7c-179">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="fde7c-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fde7c-180">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fde7c-181">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fde7c-182">System-Only</span></span>            | <span data-ttu-id="fde7c-183">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-183">False</span></span>                                 |
| <span data-ttu-id="fde7c-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fde7c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fde7c-185">True</span><span class="sxs-lookup"><span data-stu-id="fde7c-185">True</span></span>                                  |
| <span data-ttu-id="fde7c-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fde7c-186">Is Indexed</span></span>             | <span data-ttu-id="fde7c-187">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-187">False</span></span>                                 |
| <span data-ttu-id="fde7c-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fde7c-188">In Global Catalog</span></span>      | <span data-ttu-id="fde7c-189">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-189">False</span></span>                                 |
| <span data-ttu-id="fde7c-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fde7c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fde7c-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fde7c-191">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="fde7c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fde7c-192">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fde7c-193">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-194">Search-Flags</span></span>           | <span data-ttu-id="fde7c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fde7c-195">0x00000000</span></span>                            |
| <span data-ttu-id="fde7c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-196">System-Flags</span></span>           | <span data-ttu-id="fde7c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fde7c-197">0x00000010</span></span>                            |
| <span data-ttu-id="fde7c-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fde7c-198">Classes used in</span></span>        | [<span data-ttu-id="fde7c-199">**Secreto**</span><span class="sxs-lookup"><span data-stu-id="fde7c-199">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fde7c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fde7c-200">Windows Server 2008</span></span>



| <span data-ttu-id="fde7c-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="fde7c-201">Entry</span></span> | <span data-ttu-id="fde7c-202">Value</span><span class="sxs-lookup"><span data-stu-id="fde7c-202">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="fde7c-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fde7c-203">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fde7c-204">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="fde7c-205">System-Only</span></span>            | <span data-ttu-id="fde7c-206">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-206">False</span></span>                                 |
| <span data-ttu-id="fde7c-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fde7c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="fde7c-208">True</span><span class="sxs-lookup"><span data-stu-id="fde7c-208">True</span></span>                                  |
| <span data-ttu-id="fde7c-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fde7c-209">Is Indexed</span></span>             | <span data-ttu-id="fde7c-210">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-210">False</span></span>                                 |
| <span data-ttu-id="fde7c-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fde7c-211">In Global Catalog</span></span>      | <span data-ttu-id="fde7c-212">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-212">False</span></span>                                 |
| <span data-ttu-id="fde7c-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fde7c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="fde7c-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fde7c-214">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="fde7c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fde7c-215">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fde7c-216">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-217">Search-Flags</span></span>           | <span data-ttu-id="fde7c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fde7c-218">0x00000000</span></span>                            |
| <span data-ttu-id="fde7c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-219">System-Flags</span></span>           | <span data-ttu-id="fde7c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fde7c-220">0x00000010</span></span>                            |
| <span data-ttu-id="fde7c-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fde7c-221">Classes used in</span></span>        | [<span data-ttu-id="fde7c-222">**Secreto**</span><span class="sxs-lookup"><span data-stu-id="fde7c-222">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fde7c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fde7c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fde7c-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="fde7c-224">Entry</span></span> | <span data-ttu-id="fde7c-225">Value</span><span class="sxs-lookup"><span data-stu-id="fde7c-225">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="fde7c-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fde7c-226">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fde7c-227">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="fde7c-228">System-Only</span></span>            | <span data-ttu-id="fde7c-229">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-229">False</span></span>                                 |
| <span data-ttu-id="fde7c-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fde7c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="fde7c-231">True</span><span class="sxs-lookup"><span data-stu-id="fde7c-231">True</span></span>                                  |
| <span data-ttu-id="fde7c-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fde7c-232">Is Indexed</span></span>             | <span data-ttu-id="fde7c-233">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-233">False</span></span>                                 |
| <span data-ttu-id="fde7c-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fde7c-234">In Global Catalog</span></span>      | <span data-ttu-id="fde7c-235">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-235">False</span></span>                                 |
| <span data-ttu-id="fde7c-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fde7c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="fde7c-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fde7c-237">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="fde7c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fde7c-238">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fde7c-239">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-240">Search-Flags</span></span>           | <span data-ttu-id="fde7c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fde7c-241">0x00000000</span></span>                            |
| <span data-ttu-id="fde7c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-242">System-Flags</span></span>           | <span data-ttu-id="fde7c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fde7c-243">0x00000010</span></span>                            |
| <span data-ttu-id="fde7c-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fde7c-244">Classes used in</span></span>        | [<span data-ttu-id="fde7c-245">**Secreto**</span><span class="sxs-lookup"><span data-stu-id="fde7c-245">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fde7c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fde7c-246">Windows Server 2012</span></span>



| <span data-ttu-id="fde7c-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="fde7c-247">Entry</span></span> | <span data-ttu-id="fde7c-248">Value</span><span class="sxs-lookup"><span data-stu-id="fde7c-248">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="fde7c-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="fde7c-249">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fde7c-250">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="fde7c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="fde7c-251">System-Only</span></span>            | <span data-ttu-id="fde7c-252">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-252">False</span></span>                                 |
| <span data-ttu-id="fde7c-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="fde7c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="fde7c-254">True</span><span class="sxs-lookup"><span data-stu-id="fde7c-254">True</span></span>                                  |
| <span data-ttu-id="fde7c-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="fde7c-255">Is Indexed</span></span>             | <span data-ttu-id="fde7c-256">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-256">False</span></span>                                 |
| <span data-ttu-id="fde7c-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="fde7c-257">In Global Catalog</span></span>      | <span data-ttu-id="fde7c-258">False</span><span class="sxs-lookup"><span data-stu-id="fde7c-258">False</span></span>                                 |
| <span data-ttu-id="fde7c-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="fde7c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="fde7c-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fde7c-260">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="fde7c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fde7c-261">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fde7c-262">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="fde7c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-263">Search-Flags</span></span>           | <span data-ttu-id="fde7c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fde7c-264">0x00000000</span></span>                            |
| <span data-ttu-id="fde7c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fde7c-265">System-Flags</span></span>           | <span data-ttu-id="fde7c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fde7c-266">0x00000010</span></span>                            |
| <span data-ttu-id="fde7c-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="fde7c-267">Classes used in</span></span>        | [<span data-ttu-id="fde7c-268">**Secreto**</span><span class="sxs-lookup"><span data-stu-id="fde7c-268">**Secret**</span></span>](c-secret.md)<br/> |



 

 






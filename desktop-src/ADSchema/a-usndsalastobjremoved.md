---
title: USN-DSA-Last-obj-atributo quitado
description: Contiene el número de secuencia de actualización (USN) para el último objeto del sistema que se ha quitado de un servidor.
ms.assetid: af0afd80-fe4a-4bc6-84e3-14c2900bec93
ms.tgt_platform: multiple
keywords:
- 'USN-DSA-Last-OBJ: esquema de AD de atributos quitados'
- uSNDSALastObjRemoved esquema de AD de atributos
topic_type:
- apiref
api_name:
- USN-DSA-Last-Obj-Removed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbc246aa1a0f7c794b9dc0a9d2a725273a918e3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997486"
---
# <a name="usn-dsa-last-obj-removed-attribute"></a><span data-ttu-id="65caa-105">USN-DSA-Last-obj-atributo quitado</span><span class="sxs-lookup"><span data-stu-id="65caa-105">USN-DSA-Last-Obj-Removed attribute</span></span>

<span data-ttu-id="65caa-106">Contiene el número de secuencia de actualización (USN) para el último objeto del sistema que se ha quitado de un servidor.</span><span class="sxs-lookup"><span data-stu-id="65caa-106">Contains the update sequence number (USN) for the last system object that was removed from a server.</span></span>



| <span data-ttu-id="65caa-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="65caa-107">Entry</span></span> | <span data-ttu-id="65caa-108">Value</span><span class="sxs-lookup"><span data-stu-id="65caa-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="65caa-109">CN</span><span class="sxs-lookup"><span data-stu-id="65caa-109">CN</span></span>                | <span data-ttu-id="65caa-110">USN-DSA-Last-obj-quitado</span><span class="sxs-lookup"><span data-stu-id="65caa-110">USN-DSA-Last-Obj-Removed</span></span>             |
| <span data-ttu-id="65caa-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="65caa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="65caa-112">uSNDSALastObjRemoved</span><span class="sxs-lookup"><span data-stu-id="65caa-112">uSNDSALastObjRemoved</span></span>                 |
| <span data-ttu-id="65caa-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="65caa-113">Size</span></span>              | <span data-ttu-id="65caa-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="65caa-114">8 bytes</span></span>                              |
| <span data-ttu-id="65caa-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="65caa-115">Update Privilege</span></span>  | <span data-ttu-id="65caa-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="65caa-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="65caa-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="65caa-117">Update Frequency</span></span>  | <span data-ttu-id="65caa-118">Cada vez que cambia un objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="65caa-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="65caa-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="65caa-119">Attribute-Id</span></span>      | <span data-ttu-id="65caa-120">1.2.840.113556.1.2.267</span><span class="sxs-lookup"><span data-stu-id="65caa-120">1.2.840.113556.1.2.267</span></span>               |
| <span data-ttu-id="65caa-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="65caa-121">System-Id-Guid</span></span>    | <span data-ttu-id="65caa-122">bf967a71-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="65caa-122">bf967a71-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="65caa-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65caa-123">Syntax</span></span>            | [<span data-ttu-id="65caa-124">**Interval**</span><span class="sxs-lookup"><span data-stu-id="65caa-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="65caa-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="65caa-125">Implementations</span></span>

-   [<span data-ttu-id="65caa-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="65caa-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="65caa-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="65caa-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="65caa-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="65caa-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="65caa-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="65caa-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="65caa-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="65caa-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="65caa-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="65caa-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="65caa-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="65caa-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="65caa-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65caa-133">Windows 2000 Server</span></span>



| <span data-ttu-id="65caa-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="65caa-134">Entry</span></span> | <span data-ttu-id="65caa-135">Value</span><span class="sxs-lookup"><span data-stu-id="65caa-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65caa-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65caa-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65caa-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65caa-137">MAPI-Id</span></span>                | <span data-ttu-id="65caa-138">0x8155</span><span class="sxs-lookup"><span data-stu-id="65caa-138">0x8155</span></span>                          |
| <span data-ttu-id="65caa-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="65caa-139">System-Only</span></span>            | <span data-ttu-id="65caa-140">True</span><span class="sxs-lookup"><span data-stu-id="65caa-140">True</span></span>                            |
| <span data-ttu-id="65caa-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65caa-141">Is-Single-Valued</span></span>       | <span data-ttu-id="65caa-142">True</span><span class="sxs-lookup"><span data-stu-id="65caa-142">True</span></span>                            |
| <span data-ttu-id="65caa-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65caa-143">Is Indexed</span></span>             | <span data-ttu-id="65caa-144">False</span><span class="sxs-lookup"><span data-stu-id="65caa-144">False</span></span>                           |
| <span data-ttu-id="65caa-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65caa-145">In Global Catalog</span></span>      | <span data-ttu-id="65caa-146">False</span><span class="sxs-lookup"><span data-stu-id="65caa-146">False</span></span>                           |
| <span data-ttu-id="65caa-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65caa-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="65caa-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65caa-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65caa-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65caa-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65caa-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65caa-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65caa-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-151">Search-Flags</span></span>           | <span data-ttu-id="65caa-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65caa-152">0x00000000</span></span>                      |
| <span data-ttu-id="65caa-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-153">System-Flags</span></span>           | <span data-ttu-id="65caa-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65caa-154">0x00000010</span></span>                      |
| <span data-ttu-id="65caa-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65caa-155">Classes used in</span></span>        | [<span data-ttu-id="65caa-156">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="65caa-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="65caa-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65caa-157">Windows Server 2003</span></span>



| <span data-ttu-id="65caa-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="65caa-158">Entry</span></span> | <span data-ttu-id="65caa-159">Value</span><span class="sxs-lookup"><span data-stu-id="65caa-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65caa-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65caa-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65caa-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65caa-161">MAPI-Id</span></span>                | <span data-ttu-id="65caa-162">0x8155</span><span class="sxs-lookup"><span data-stu-id="65caa-162">0x8155</span></span>                          |
| <span data-ttu-id="65caa-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="65caa-163">System-Only</span></span>            | <span data-ttu-id="65caa-164">True</span><span class="sxs-lookup"><span data-stu-id="65caa-164">True</span></span>                            |
| <span data-ttu-id="65caa-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65caa-165">Is-Single-Valued</span></span>       | <span data-ttu-id="65caa-166">True</span><span class="sxs-lookup"><span data-stu-id="65caa-166">True</span></span>                            |
| <span data-ttu-id="65caa-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65caa-167">Is Indexed</span></span>             | <span data-ttu-id="65caa-168">False</span><span class="sxs-lookup"><span data-stu-id="65caa-168">False</span></span>                           |
| <span data-ttu-id="65caa-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65caa-169">In Global Catalog</span></span>      | <span data-ttu-id="65caa-170">False</span><span class="sxs-lookup"><span data-stu-id="65caa-170">False</span></span>                           |
| <span data-ttu-id="65caa-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65caa-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="65caa-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65caa-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65caa-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65caa-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65caa-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65caa-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65caa-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-175">Search-Flags</span></span>           | <span data-ttu-id="65caa-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65caa-176">0x00000000</span></span>                      |
| <span data-ttu-id="65caa-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-177">System-Flags</span></span>           | <span data-ttu-id="65caa-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65caa-178">0x00000010</span></span>                      |
| <span data-ttu-id="65caa-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65caa-179">Classes used in</span></span>        | [<span data-ttu-id="65caa-180">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="65caa-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="65caa-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="65caa-181">ADAM</span></span>



| <span data-ttu-id="65caa-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="65caa-182">Entry</span></span> | <span data-ttu-id="65caa-183">Value</span><span class="sxs-lookup"><span data-stu-id="65caa-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65caa-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65caa-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65caa-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65caa-185">MAPI-Id</span></span>                | <span data-ttu-id="65caa-186">0x8155</span><span class="sxs-lookup"><span data-stu-id="65caa-186">0x8155</span></span>                          |
| <span data-ttu-id="65caa-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="65caa-187">System-Only</span></span>            | <span data-ttu-id="65caa-188">True</span><span class="sxs-lookup"><span data-stu-id="65caa-188">True</span></span>                            |
| <span data-ttu-id="65caa-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65caa-189">Is-Single-Valued</span></span>       | <span data-ttu-id="65caa-190">True</span><span class="sxs-lookup"><span data-stu-id="65caa-190">True</span></span>                            |
| <span data-ttu-id="65caa-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65caa-191">Is Indexed</span></span>             | <span data-ttu-id="65caa-192">False</span><span class="sxs-lookup"><span data-stu-id="65caa-192">False</span></span>                           |
| <span data-ttu-id="65caa-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65caa-193">In Global Catalog</span></span>      | <span data-ttu-id="65caa-194">False</span><span class="sxs-lookup"><span data-stu-id="65caa-194">False</span></span>                           |
| <span data-ttu-id="65caa-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65caa-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="65caa-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65caa-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65caa-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65caa-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65caa-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65caa-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65caa-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-199">Search-Flags</span></span>           | <span data-ttu-id="65caa-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65caa-200">0x00000000</span></span>                      |
| <span data-ttu-id="65caa-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-201">System-Flags</span></span>           | <span data-ttu-id="65caa-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65caa-202">0x00000010</span></span>                      |
| <span data-ttu-id="65caa-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65caa-203">Classes used in</span></span>        | [<span data-ttu-id="65caa-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="65caa-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="65caa-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="65caa-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="65caa-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="65caa-206">Entry</span></span> | <span data-ttu-id="65caa-207">Value</span><span class="sxs-lookup"><span data-stu-id="65caa-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65caa-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65caa-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65caa-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65caa-209">MAPI-Id</span></span>                | <span data-ttu-id="65caa-210">0x8155</span><span class="sxs-lookup"><span data-stu-id="65caa-210">0x8155</span></span>                          |
| <span data-ttu-id="65caa-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="65caa-211">System-Only</span></span>            | <span data-ttu-id="65caa-212">True</span><span class="sxs-lookup"><span data-stu-id="65caa-212">True</span></span>                            |
| <span data-ttu-id="65caa-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65caa-213">Is-Single-Valued</span></span>       | <span data-ttu-id="65caa-214">True</span><span class="sxs-lookup"><span data-stu-id="65caa-214">True</span></span>                            |
| <span data-ttu-id="65caa-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65caa-215">Is Indexed</span></span>             | <span data-ttu-id="65caa-216">False</span><span class="sxs-lookup"><span data-stu-id="65caa-216">False</span></span>                           |
| <span data-ttu-id="65caa-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65caa-217">In Global Catalog</span></span>      | <span data-ttu-id="65caa-218">False</span><span class="sxs-lookup"><span data-stu-id="65caa-218">False</span></span>                           |
| <span data-ttu-id="65caa-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65caa-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="65caa-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65caa-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65caa-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65caa-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65caa-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65caa-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65caa-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-223">Search-Flags</span></span>           | <span data-ttu-id="65caa-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65caa-224">0x00000000</span></span>                      |
| <span data-ttu-id="65caa-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-225">System-Flags</span></span>           | <span data-ttu-id="65caa-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65caa-226">0x00000010</span></span>                      |
| <span data-ttu-id="65caa-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65caa-227">Classes used in</span></span>        | [<span data-ttu-id="65caa-228">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="65caa-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="65caa-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65caa-229">Windows Server 2008</span></span>



| <span data-ttu-id="65caa-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="65caa-230">Entry</span></span> | <span data-ttu-id="65caa-231">Value</span><span class="sxs-lookup"><span data-stu-id="65caa-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65caa-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65caa-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65caa-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65caa-233">MAPI-Id</span></span>                | <span data-ttu-id="65caa-234">0x8155</span><span class="sxs-lookup"><span data-stu-id="65caa-234">0x8155</span></span>                          |
| <span data-ttu-id="65caa-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="65caa-235">System-Only</span></span>            | <span data-ttu-id="65caa-236">True</span><span class="sxs-lookup"><span data-stu-id="65caa-236">True</span></span>                            |
| <span data-ttu-id="65caa-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65caa-237">Is-Single-Valued</span></span>       | <span data-ttu-id="65caa-238">True</span><span class="sxs-lookup"><span data-stu-id="65caa-238">True</span></span>                            |
| <span data-ttu-id="65caa-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65caa-239">Is Indexed</span></span>             | <span data-ttu-id="65caa-240">False</span><span class="sxs-lookup"><span data-stu-id="65caa-240">False</span></span>                           |
| <span data-ttu-id="65caa-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65caa-241">In Global Catalog</span></span>      | <span data-ttu-id="65caa-242">False</span><span class="sxs-lookup"><span data-stu-id="65caa-242">False</span></span>                           |
| <span data-ttu-id="65caa-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65caa-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="65caa-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65caa-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65caa-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65caa-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65caa-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65caa-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65caa-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-247">Search-Flags</span></span>           | <span data-ttu-id="65caa-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65caa-248">0x00000000</span></span>                      |
| <span data-ttu-id="65caa-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-249">System-Flags</span></span>           | <span data-ttu-id="65caa-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65caa-250">0x00000010</span></span>                      |
| <span data-ttu-id="65caa-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65caa-251">Classes used in</span></span>        | [<span data-ttu-id="65caa-252">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="65caa-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="65caa-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65caa-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="65caa-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="65caa-254">Entry</span></span> | <span data-ttu-id="65caa-255">Value</span><span class="sxs-lookup"><span data-stu-id="65caa-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65caa-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65caa-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65caa-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65caa-257">MAPI-Id</span></span>                | <span data-ttu-id="65caa-258">0x8155</span><span class="sxs-lookup"><span data-stu-id="65caa-258">0x8155</span></span>                          |
| <span data-ttu-id="65caa-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="65caa-259">System-Only</span></span>            | <span data-ttu-id="65caa-260">True</span><span class="sxs-lookup"><span data-stu-id="65caa-260">True</span></span>                            |
| <span data-ttu-id="65caa-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65caa-261">Is-Single-Valued</span></span>       | <span data-ttu-id="65caa-262">True</span><span class="sxs-lookup"><span data-stu-id="65caa-262">True</span></span>                            |
| <span data-ttu-id="65caa-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65caa-263">Is Indexed</span></span>             | <span data-ttu-id="65caa-264">False</span><span class="sxs-lookup"><span data-stu-id="65caa-264">False</span></span>                           |
| <span data-ttu-id="65caa-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65caa-265">In Global Catalog</span></span>      | <span data-ttu-id="65caa-266">False</span><span class="sxs-lookup"><span data-stu-id="65caa-266">False</span></span>                           |
| <span data-ttu-id="65caa-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65caa-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="65caa-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65caa-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65caa-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65caa-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65caa-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65caa-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65caa-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-271">Search-Flags</span></span>           | <span data-ttu-id="65caa-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65caa-272">0x00000000</span></span>                      |
| <span data-ttu-id="65caa-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-273">System-Flags</span></span>           | <span data-ttu-id="65caa-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65caa-274">0x00000010</span></span>                      |
| <span data-ttu-id="65caa-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65caa-275">Classes used in</span></span>        | [<span data-ttu-id="65caa-276">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="65caa-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="65caa-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65caa-277">Windows Server 2012</span></span>



| <span data-ttu-id="65caa-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="65caa-278">Entry</span></span> | <span data-ttu-id="65caa-279">Value</span><span class="sxs-lookup"><span data-stu-id="65caa-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65caa-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="65caa-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65caa-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65caa-281">MAPI-Id</span></span>                | <span data-ttu-id="65caa-282">0x8155</span><span class="sxs-lookup"><span data-stu-id="65caa-282">0x8155</span></span>                          |
| <span data-ttu-id="65caa-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="65caa-283">System-Only</span></span>            | <span data-ttu-id="65caa-284">True</span><span class="sxs-lookup"><span data-stu-id="65caa-284">True</span></span>                            |
| <span data-ttu-id="65caa-285">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="65caa-285">Is-Single-Valued</span></span>       | <span data-ttu-id="65caa-286">True</span><span class="sxs-lookup"><span data-stu-id="65caa-286">True</span></span>                            |
| <span data-ttu-id="65caa-287">Está indexado</span><span class="sxs-lookup"><span data-stu-id="65caa-287">Is Indexed</span></span>             | <span data-ttu-id="65caa-288">False</span><span class="sxs-lookup"><span data-stu-id="65caa-288">False</span></span>                           |
| <span data-ttu-id="65caa-289">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="65caa-289">In Global Catalog</span></span>      | <span data-ttu-id="65caa-290">False</span><span class="sxs-lookup"><span data-stu-id="65caa-290">False</span></span>                           |
| <span data-ttu-id="65caa-291">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="65caa-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="65caa-292">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65caa-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65caa-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65caa-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="65caa-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65caa-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="65caa-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-295">Search-Flags</span></span>           | <span data-ttu-id="65caa-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65caa-296">0x00000000</span></span>                      |
| <span data-ttu-id="65caa-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65caa-297">System-Flags</span></span>           | <span data-ttu-id="65caa-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65caa-298">0x00000010</span></span>                      |
| <span data-ttu-id="65caa-299">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="65caa-299">Classes used in</span></span>        | [<span data-ttu-id="65caa-300">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="65caa-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="65caa-301">Vea también</span><span class="sxs-lookup"><span data-stu-id="65caa-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65caa-302">**USN-Last-obj-REM**</span><span class="sxs-lookup"><span data-stu-id="65caa-302">**USN-Last-Obj-Rem**</span></span>](a-usnlastobjrem.md)
</dt> </dl>

 

 






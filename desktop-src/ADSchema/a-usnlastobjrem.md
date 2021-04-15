---
title: USN-Last-obj-REM atributo
description: Contiene el número de secuencia de actualización (USN) para el último objeto que no es del sistema que se ha quitado de un servidor.
ms.assetid: 34718bea-fa19-4084-b97f-d72a1681c3f4
ms.tgt_platform: multiple
keywords:
- USN-Last-obj-REM atributo AD Schema
- uSNLastObjRem esquema de AD de atributos
topic_type:
- apiref
api_name:
- USN-Last-Obj-Rem
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9836bd93ca065fdfa53b0246a5bab0142e84ced6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536111"
---
# <a name="usn-last-obj-rem-attribute"></a><span data-ttu-id="60cce-105">USN-Last-obj-REM atributo</span><span class="sxs-lookup"><span data-stu-id="60cce-105">USN-Last-Obj-Rem attribute</span></span>

<span data-ttu-id="60cce-106">Contiene el número de secuencia de actualización (USN) para el último objeto que no es del sistema que se ha quitado de un servidor.</span><span class="sxs-lookup"><span data-stu-id="60cce-106">Contains the update sequence number (USN) for the last non-system object that was removed from a server.</span></span>



| <span data-ttu-id="60cce-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="60cce-107">Entry</span></span> | <span data-ttu-id="60cce-108">Value</span><span class="sxs-lookup"><span data-stu-id="60cce-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="60cce-109">CN</span><span class="sxs-lookup"><span data-stu-id="60cce-109">CN</span></span>                | <span data-ttu-id="60cce-110">USN-Last-obj-REM</span><span class="sxs-lookup"><span data-stu-id="60cce-110">USN-Last-Obj-Rem</span></span>                     |
| <span data-ttu-id="60cce-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="60cce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="60cce-112">uSNLastObjRem</span><span class="sxs-lookup"><span data-stu-id="60cce-112">uSNLastObjRem</span></span>                        |
| <span data-ttu-id="60cce-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="60cce-113">Size</span></span>              | <span data-ttu-id="60cce-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="60cce-114">8 bytes</span></span>                              |
| <span data-ttu-id="60cce-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="60cce-115">Update Privilege</span></span>  | <span data-ttu-id="60cce-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="60cce-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="60cce-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="60cce-117">Update Frequency</span></span>  | <span data-ttu-id="60cce-118">Cada vez que cambia un objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="60cce-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="60cce-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="60cce-119">Attribute-Id</span></span>      | <span data-ttu-id="60cce-120">1.2.840.113556.1.2.121</span><span class="sxs-lookup"><span data-stu-id="60cce-120">1.2.840.113556.1.2.121</span></span>               |
| <span data-ttu-id="60cce-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="60cce-121">System-Id-Guid</span></span>    | <span data-ttu-id="60cce-122">bf967a73-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="60cce-122">bf967a73-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="60cce-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60cce-123">Syntax</span></span>            | [<span data-ttu-id="60cce-124">**Interval**</span><span class="sxs-lookup"><span data-stu-id="60cce-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="60cce-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="60cce-125">Implementations</span></span>

-   [<span data-ttu-id="60cce-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="60cce-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="60cce-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="60cce-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="60cce-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="60cce-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="60cce-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="60cce-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="60cce-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="60cce-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="60cce-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="60cce-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="60cce-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="60cce-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="60cce-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="60cce-133">Windows 2000 Server</span></span>



| <span data-ttu-id="60cce-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="60cce-134">Entry</span></span> | <span data-ttu-id="60cce-135">Value</span><span class="sxs-lookup"><span data-stu-id="60cce-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60cce-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60cce-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60cce-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60cce-137">MAPI-Id</span></span>                | <span data-ttu-id="60cce-138">0x8156</span><span class="sxs-lookup"><span data-stu-id="60cce-138">0x8156</span></span>                          |
| <span data-ttu-id="60cce-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="60cce-139">System-Only</span></span>            | <span data-ttu-id="60cce-140">True</span><span class="sxs-lookup"><span data-stu-id="60cce-140">True</span></span>                            |
| <span data-ttu-id="60cce-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60cce-141">Is-Single-Valued</span></span>       | <span data-ttu-id="60cce-142">True</span><span class="sxs-lookup"><span data-stu-id="60cce-142">True</span></span>                            |
| <span data-ttu-id="60cce-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60cce-143">Is Indexed</span></span>             | <span data-ttu-id="60cce-144">False</span><span class="sxs-lookup"><span data-stu-id="60cce-144">False</span></span>                           |
| <span data-ttu-id="60cce-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60cce-145">In Global Catalog</span></span>      | <span data-ttu-id="60cce-146">True</span><span class="sxs-lookup"><span data-stu-id="60cce-146">True</span></span>                            |
| <span data-ttu-id="60cce-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60cce-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="60cce-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60cce-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60cce-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60cce-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60cce-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60cce-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60cce-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-151">Search-Flags</span></span>           | <span data-ttu-id="60cce-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60cce-152">0x00000000</span></span>                      |
| <span data-ttu-id="60cce-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-153">System-Flags</span></span>           | <span data-ttu-id="60cce-154">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60cce-154">0x00000013</span></span>                      |
| <span data-ttu-id="60cce-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60cce-155">Classes used in</span></span>        | [<span data-ttu-id="60cce-156">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60cce-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="60cce-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60cce-157">Windows Server 2003</span></span>



| <span data-ttu-id="60cce-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="60cce-158">Entry</span></span> | <span data-ttu-id="60cce-159">Value</span><span class="sxs-lookup"><span data-stu-id="60cce-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60cce-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60cce-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60cce-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60cce-161">MAPI-Id</span></span>                | <span data-ttu-id="60cce-162">0x8156</span><span class="sxs-lookup"><span data-stu-id="60cce-162">0x8156</span></span>                          |
| <span data-ttu-id="60cce-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="60cce-163">System-Only</span></span>            | <span data-ttu-id="60cce-164">True</span><span class="sxs-lookup"><span data-stu-id="60cce-164">True</span></span>                            |
| <span data-ttu-id="60cce-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60cce-165">Is-Single-Valued</span></span>       | <span data-ttu-id="60cce-166">True</span><span class="sxs-lookup"><span data-stu-id="60cce-166">True</span></span>                            |
| <span data-ttu-id="60cce-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60cce-167">Is Indexed</span></span>             | <span data-ttu-id="60cce-168">False</span><span class="sxs-lookup"><span data-stu-id="60cce-168">False</span></span>                           |
| <span data-ttu-id="60cce-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60cce-169">In Global Catalog</span></span>      | <span data-ttu-id="60cce-170">True</span><span class="sxs-lookup"><span data-stu-id="60cce-170">True</span></span>                            |
| <span data-ttu-id="60cce-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60cce-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="60cce-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60cce-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60cce-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60cce-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60cce-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60cce-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60cce-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-175">Search-Flags</span></span>           | <span data-ttu-id="60cce-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60cce-176">0x00000000</span></span>                      |
| <span data-ttu-id="60cce-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-177">System-Flags</span></span>           | <span data-ttu-id="60cce-178">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60cce-178">0x00000013</span></span>                      |
| <span data-ttu-id="60cce-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60cce-179">Classes used in</span></span>        | [<span data-ttu-id="60cce-180">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60cce-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="60cce-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="60cce-181">ADAM</span></span>



| <span data-ttu-id="60cce-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="60cce-182">Entry</span></span> | <span data-ttu-id="60cce-183">Value</span><span class="sxs-lookup"><span data-stu-id="60cce-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60cce-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60cce-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60cce-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60cce-185">MAPI-Id</span></span>                | <span data-ttu-id="60cce-186">0x8156</span><span class="sxs-lookup"><span data-stu-id="60cce-186">0x8156</span></span>                          |
| <span data-ttu-id="60cce-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="60cce-187">System-Only</span></span>            | <span data-ttu-id="60cce-188">True</span><span class="sxs-lookup"><span data-stu-id="60cce-188">True</span></span>                            |
| <span data-ttu-id="60cce-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60cce-189">Is-Single-Valued</span></span>       | <span data-ttu-id="60cce-190">True</span><span class="sxs-lookup"><span data-stu-id="60cce-190">True</span></span>                            |
| <span data-ttu-id="60cce-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60cce-191">Is Indexed</span></span>             | <span data-ttu-id="60cce-192">False</span><span class="sxs-lookup"><span data-stu-id="60cce-192">False</span></span>                           |
| <span data-ttu-id="60cce-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60cce-193">In Global Catalog</span></span>      | <span data-ttu-id="60cce-194">True</span><span class="sxs-lookup"><span data-stu-id="60cce-194">True</span></span>                            |
| <span data-ttu-id="60cce-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60cce-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="60cce-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60cce-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60cce-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60cce-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60cce-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60cce-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60cce-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-199">Search-Flags</span></span>           | <span data-ttu-id="60cce-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60cce-200">0x00000000</span></span>                      |
| <span data-ttu-id="60cce-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-201">System-Flags</span></span>           | <span data-ttu-id="60cce-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60cce-202">0x00000013</span></span>                      |
| <span data-ttu-id="60cce-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60cce-203">Classes used in</span></span>        | [<span data-ttu-id="60cce-204">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60cce-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="60cce-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="60cce-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="60cce-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="60cce-206">Entry</span></span> | <span data-ttu-id="60cce-207">Value</span><span class="sxs-lookup"><span data-stu-id="60cce-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60cce-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60cce-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60cce-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60cce-209">MAPI-Id</span></span>                | <span data-ttu-id="60cce-210">0x8156</span><span class="sxs-lookup"><span data-stu-id="60cce-210">0x8156</span></span>                          |
| <span data-ttu-id="60cce-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="60cce-211">System-Only</span></span>            | <span data-ttu-id="60cce-212">True</span><span class="sxs-lookup"><span data-stu-id="60cce-212">True</span></span>                            |
| <span data-ttu-id="60cce-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60cce-213">Is-Single-Valued</span></span>       | <span data-ttu-id="60cce-214">True</span><span class="sxs-lookup"><span data-stu-id="60cce-214">True</span></span>                            |
| <span data-ttu-id="60cce-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60cce-215">Is Indexed</span></span>             | <span data-ttu-id="60cce-216">False</span><span class="sxs-lookup"><span data-stu-id="60cce-216">False</span></span>                           |
| <span data-ttu-id="60cce-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60cce-217">In Global Catalog</span></span>      | <span data-ttu-id="60cce-218">True</span><span class="sxs-lookup"><span data-stu-id="60cce-218">True</span></span>                            |
| <span data-ttu-id="60cce-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60cce-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="60cce-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60cce-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60cce-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60cce-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60cce-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60cce-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60cce-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-223">Search-Flags</span></span>           | <span data-ttu-id="60cce-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60cce-224">0x00000000</span></span>                      |
| <span data-ttu-id="60cce-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-225">System-Flags</span></span>           | <span data-ttu-id="60cce-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60cce-226">0x00000013</span></span>                      |
| <span data-ttu-id="60cce-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60cce-227">Classes used in</span></span>        | [<span data-ttu-id="60cce-228">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60cce-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="60cce-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60cce-229">Windows Server 2008</span></span>



| <span data-ttu-id="60cce-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="60cce-230">Entry</span></span> | <span data-ttu-id="60cce-231">Value</span><span class="sxs-lookup"><span data-stu-id="60cce-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60cce-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60cce-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60cce-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60cce-233">MAPI-Id</span></span>                | <span data-ttu-id="60cce-234">0x8156</span><span class="sxs-lookup"><span data-stu-id="60cce-234">0x8156</span></span>                          |
| <span data-ttu-id="60cce-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="60cce-235">System-Only</span></span>            | <span data-ttu-id="60cce-236">True</span><span class="sxs-lookup"><span data-stu-id="60cce-236">True</span></span>                            |
| <span data-ttu-id="60cce-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60cce-237">Is-Single-Valued</span></span>       | <span data-ttu-id="60cce-238">True</span><span class="sxs-lookup"><span data-stu-id="60cce-238">True</span></span>                            |
| <span data-ttu-id="60cce-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60cce-239">Is Indexed</span></span>             | <span data-ttu-id="60cce-240">False</span><span class="sxs-lookup"><span data-stu-id="60cce-240">False</span></span>                           |
| <span data-ttu-id="60cce-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60cce-241">In Global Catalog</span></span>      | <span data-ttu-id="60cce-242">True</span><span class="sxs-lookup"><span data-stu-id="60cce-242">True</span></span>                            |
| <span data-ttu-id="60cce-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60cce-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="60cce-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60cce-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60cce-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60cce-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60cce-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60cce-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60cce-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-247">Search-Flags</span></span>           | <span data-ttu-id="60cce-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60cce-248">0x00000000</span></span>                      |
| <span data-ttu-id="60cce-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-249">System-Flags</span></span>           | <span data-ttu-id="60cce-250">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60cce-250">0x00000013</span></span>                      |
| <span data-ttu-id="60cce-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60cce-251">Classes used in</span></span>        | [<span data-ttu-id="60cce-252">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60cce-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="60cce-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60cce-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="60cce-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="60cce-254">Entry</span></span> | <span data-ttu-id="60cce-255">Value</span><span class="sxs-lookup"><span data-stu-id="60cce-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60cce-256">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60cce-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60cce-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60cce-257">MAPI-Id</span></span>                | <span data-ttu-id="60cce-258">0x8156</span><span class="sxs-lookup"><span data-stu-id="60cce-258">0x8156</span></span>                          |
| <span data-ttu-id="60cce-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="60cce-259">System-Only</span></span>            | <span data-ttu-id="60cce-260">True</span><span class="sxs-lookup"><span data-stu-id="60cce-260">True</span></span>                            |
| <span data-ttu-id="60cce-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60cce-261">Is-Single-Valued</span></span>       | <span data-ttu-id="60cce-262">True</span><span class="sxs-lookup"><span data-stu-id="60cce-262">True</span></span>                            |
| <span data-ttu-id="60cce-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60cce-263">Is Indexed</span></span>             | <span data-ttu-id="60cce-264">False</span><span class="sxs-lookup"><span data-stu-id="60cce-264">False</span></span>                           |
| <span data-ttu-id="60cce-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60cce-265">In Global Catalog</span></span>      | <span data-ttu-id="60cce-266">True</span><span class="sxs-lookup"><span data-stu-id="60cce-266">True</span></span>                            |
| <span data-ttu-id="60cce-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60cce-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="60cce-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60cce-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60cce-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60cce-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60cce-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60cce-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60cce-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-271">Search-Flags</span></span>           | <span data-ttu-id="60cce-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60cce-272">0x00000000</span></span>                      |
| <span data-ttu-id="60cce-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-273">System-Flags</span></span>           | <span data-ttu-id="60cce-274">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60cce-274">0x00000013</span></span>                      |
| <span data-ttu-id="60cce-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60cce-275">Classes used in</span></span>        | [<span data-ttu-id="60cce-276">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60cce-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="60cce-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60cce-277">Windows Server 2012</span></span>



| <span data-ttu-id="60cce-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="60cce-278">Entry</span></span> | <span data-ttu-id="60cce-279">Value</span><span class="sxs-lookup"><span data-stu-id="60cce-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="60cce-280">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="60cce-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="60cce-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60cce-281">MAPI-Id</span></span>                | <span data-ttu-id="60cce-282">0x8156</span><span class="sxs-lookup"><span data-stu-id="60cce-282">0x8156</span></span>                          |
| <span data-ttu-id="60cce-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="60cce-283">System-Only</span></span>            | <span data-ttu-id="60cce-284">True</span><span class="sxs-lookup"><span data-stu-id="60cce-284">True</span></span>                            |
| <span data-ttu-id="60cce-285">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="60cce-285">Is-Single-Valued</span></span>       | <span data-ttu-id="60cce-286">True</span><span class="sxs-lookup"><span data-stu-id="60cce-286">True</span></span>                            |
| <span data-ttu-id="60cce-287">Está indexado</span><span class="sxs-lookup"><span data-stu-id="60cce-287">Is Indexed</span></span>             | <span data-ttu-id="60cce-288">False</span><span class="sxs-lookup"><span data-stu-id="60cce-288">False</span></span>                           |
| <span data-ttu-id="60cce-289">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="60cce-289">In Global Catalog</span></span>      | <span data-ttu-id="60cce-290">True</span><span class="sxs-lookup"><span data-stu-id="60cce-290">True</span></span>                            |
| <span data-ttu-id="60cce-291">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="60cce-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="60cce-292">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="60cce-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="60cce-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60cce-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="60cce-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60cce-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="60cce-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-295">Search-Flags</span></span>           | <span data-ttu-id="60cce-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60cce-296">0x00000000</span></span>                      |
| <span data-ttu-id="60cce-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60cce-297">System-Flags</span></span>           | <span data-ttu-id="60cce-298">0x00000013</span><span class="sxs-lookup"><span data-stu-id="60cce-298">0x00000013</span></span>                      |
| <span data-ttu-id="60cce-299">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="60cce-299">Classes used in</span></span>        | [<span data-ttu-id="60cce-300">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="60cce-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="60cce-301">Vea también</span><span class="sxs-lookup"><span data-stu-id="60cce-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60cce-302">**USN-DSA-Last-obj-quitado**</span><span class="sxs-lookup"><span data-stu-id="60cce-302">**USN-DSA-Last-Obj-Removed**</span></span>](a-usndsalastobjremoved.md)
</dt> </dl>

 

 






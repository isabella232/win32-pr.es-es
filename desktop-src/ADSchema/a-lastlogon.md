---
title: Last-Logon atributo)
description: La última vez que el usuario inició sesión.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Last-Logon
- lastLogon esquema de AD de atributos
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906075"
---
# <a name="last-logon-attribute"></a><span data-ttu-id="c01da-105">Last-Logon atributo)</span><span class="sxs-lookup"><span data-stu-id="c01da-105">Last-Logon attribute</span></span>

<span data-ttu-id="c01da-106">La última vez que el usuario inició sesión.</span><span class="sxs-lookup"><span data-stu-id="c01da-106">The last time the user logged on.</span></span> <span data-ttu-id="c01da-107">Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="c01da-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="c01da-108">Un valor de cero significa que la hora del último inicio de sesión es desconocida.</span><span class="sxs-lookup"><span data-stu-id="c01da-108">A value of zero means that the last logon time is unknown.</span></span>



| <span data-ttu-id="c01da-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c01da-109">Entry</span></span> | <span data-ttu-id="c01da-110">Value</span><span class="sxs-lookup"><span data-stu-id="c01da-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c01da-111">CN</span><span class="sxs-lookup"><span data-stu-id="c01da-111">CN</span></span>                | <span data-ttu-id="c01da-112">Last-Logon</span><span class="sxs-lookup"><span data-stu-id="c01da-112">Last-Logon</span></span>                           |
| <span data-ttu-id="c01da-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c01da-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c01da-114">lastLogon</span><span class="sxs-lookup"><span data-stu-id="c01da-114">lastLogon</span></span>                            |
| <span data-ttu-id="c01da-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c01da-115">Size</span></span>              | <span data-ttu-id="c01da-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="c01da-116">8 bytes</span></span>                              |
| <span data-ttu-id="c01da-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c01da-117">Update Privilege</span></span>  | <span data-ttu-id="c01da-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="c01da-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="c01da-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c01da-119">Update Frequency</span></span>  | <span data-ttu-id="c01da-120">Cada vez que el usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="c01da-120">Each time the user logs on.</span></span>          |
| <span data-ttu-id="c01da-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c01da-121">Attribute-Id</span></span>      | <span data-ttu-id="c01da-122">1.2.840.113556.1.4.52</span><span class="sxs-lookup"><span data-stu-id="c01da-122">1.2.840.113556.1.4.52</span></span>                |
| <span data-ttu-id="c01da-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c01da-123">System-Id-Guid</span></span>    | <span data-ttu-id="c01da-124">bf967997-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c01da-124">bf967997-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="c01da-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c01da-125">Syntax</span></span>            | [<span data-ttu-id="c01da-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="c01da-126">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c01da-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c01da-127">Implementations</span></span>

-   [<span data-ttu-id="c01da-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c01da-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c01da-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c01da-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c01da-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c01da-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c01da-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c01da-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c01da-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c01da-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c01da-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c01da-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c01da-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c01da-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c01da-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="c01da-135">Entry</span></span> | <span data-ttu-id="c01da-136">Value</span><span class="sxs-lookup"><span data-stu-id="c01da-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c01da-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c01da-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c01da-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c01da-139">System-Only</span></span>            | <span data-ttu-id="c01da-140">False</span><span class="sxs-lookup"><span data-stu-id="c01da-140">False</span></span>                             |
| <span data-ttu-id="c01da-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c01da-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c01da-142">True</span><span class="sxs-lookup"><span data-stu-id="c01da-142">True</span></span>                              |
| <span data-ttu-id="c01da-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c01da-143">Is Indexed</span></span>             | <span data-ttu-id="c01da-144">False</span><span class="sxs-lookup"><span data-stu-id="c01da-144">False</span></span>                             |
| <span data-ttu-id="c01da-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c01da-145">In Global Catalog</span></span>      | <span data-ttu-id="c01da-146">False</span><span class="sxs-lookup"><span data-stu-id="c01da-146">False</span></span>                             |
| <span data-ttu-id="c01da-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c01da-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c01da-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c01da-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c01da-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c01da-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c01da-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c01da-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c01da-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-151">Search-Flags</span></span>           | <span data-ttu-id="c01da-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c01da-152">0x00000000</span></span>                        |
| <span data-ttu-id="c01da-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-153">System-Flags</span></span>           | <span data-ttu-id="c01da-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c01da-154">0x00000011</span></span>                        |
| <span data-ttu-id="c01da-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c01da-155">Classes used in</span></span>        | [<span data-ttu-id="c01da-156">**User**</span><span class="sxs-lookup"><span data-stu-id="c01da-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c01da-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c01da-157">Windows Server 2003</span></span>



| <span data-ttu-id="c01da-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="c01da-158">Entry</span></span> | <span data-ttu-id="c01da-159">Value</span><span class="sxs-lookup"><span data-stu-id="c01da-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c01da-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c01da-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c01da-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c01da-162">System-Only</span></span>            | <span data-ttu-id="c01da-163">False</span><span class="sxs-lookup"><span data-stu-id="c01da-163">False</span></span>                             |
| <span data-ttu-id="c01da-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c01da-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c01da-165">True</span><span class="sxs-lookup"><span data-stu-id="c01da-165">True</span></span>                              |
| <span data-ttu-id="c01da-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c01da-166">Is Indexed</span></span>             | <span data-ttu-id="c01da-167">False</span><span class="sxs-lookup"><span data-stu-id="c01da-167">False</span></span>                             |
| <span data-ttu-id="c01da-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c01da-168">In Global Catalog</span></span>      | <span data-ttu-id="c01da-169">False</span><span class="sxs-lookup"><span data-stu-id="c01da-169">False</span></span>                             |
| <span data-ttu-id="c01da-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c01da-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c01da-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c01da-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c01da-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c01da-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c01da-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c01da-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c01da-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-174">Search-Flags</span></span>           | <span data-ttu-id="c01da-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c01da-175">0x00000000</span></span>                        |
| <span data-ttu-id="c01da-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-176">System-Flags</span></span>           | <span data-ttu-id="c01da-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c01da-177">0x00000011</span></span>                        |
| <span data-ttu-id="c01da-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c01da-178">Classes used in</span></span>        | [<span data-ttu-id="c01da-179">**User**</span><span class="sxs-lookup"><span data-stu-id="c01da-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c01da-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c01da-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c01da-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="c01da-181">Entry</span></span> | <span data-ttu-id="c01da-182">Value</span><span class="sxs-lookup"><span data-stu-id="c01da-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c01da-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c01da-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c01da-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c01da-185">System-Only</span></span>            | <span data-ttu-id="c01da-186">False</span><span class="sxs-lookup"><span data-stu-id="c01da-186">False</span></span>                             |
| <span data-ttu-id="c01da-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c01da-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c01da-188">True</span><span class="sxs-lookup"><span data-stu-id="c01da-188">True</span></span>                              |
| <span data-ttu-id="c01da-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c01da-189">Is Indexed</span></span>             | <span data-ttu-id="c01da-190">False</span><span class="sxs-lookup"><span data-stu-id="c01da-190">False</span></span>                             |
| <span data-ttu-id="c01da-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c01da-191">In Global Catalog</span></span>      | <span data-ttu-id="c01da-192">False</span><span class="sxs-lookup"><span data-stu-id="c01da-192">False</span></span>                             |
| <span data-ttu-id="c01da-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c01da-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c01da-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c01da-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c01da-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c01da-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c01da-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c01da-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c01da-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-197">Search-Flags</span></span>           | <span data-ttu-id="c01da-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c01da-198">0x00000000</span></span>                        |
| <span data-ttu-id="c01da-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-199">System-Flags</span></span>           | <span data-ttu-id="c01da-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c01da-200">0x00000011</span></span>                        |
| <span data-ttu-id="c01da-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c01da-201">Classes used in</span></span>        | [<span data-ttu-id="c01da-202">**User**</span><span class="sxs-lookup"><span data-stu-id="c01da-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c01da-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c01da-203">Windows Server 2008</span></span>



| <span data-ttu-id="c01da-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="c01da-204">Entry</span></span> | <span data-ttu-id="c01da-205">Value</span><span class="sxs-lookup"><span data-stu-id="c01da-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c01da-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c01da-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c01da-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c01da-208">System-Only</span></span>            | <span data-ttu-id="c01da-209">False</span><span class="sxs-lookup"><span data-stu-id="c01da-209">False</span></span>                             |
| <span data-ttu-id="c01da-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c01da-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c01da-211">True</span><span class="sxs-lookup"><span data-stu-id="c01da-211">True</span></span>                              |
| <span data-ttu-id="c01da-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c01da-212">Is Indexed</span></span>             | <span data-ttu-id="c01da-213">False</span><span class="sxs-lookup"><span data-stu-id="c01da-213">False</span></span>                             |
| <span data-ttu-id="c01da-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c01da-214">In Global Catalog</span></span>      | <span data-ttu-id="c01da-215">False</span><span class="sxs-lookup"><span data-stu-id="c01da-215">False</span></span>                             |
| <span data-ttu-id="c01da-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c01da-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c01da-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c01da-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c01da-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c01da-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c01da-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c01da-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c01da-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-220">Search-Flags</span></span>           | <span data-ttu-id="c01da-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c01da-221">0x00000000</span></span>                        |
| <span data-ttu-id="c01da-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-222">System-Flags</span></span>           | <span data-ttu-id="c01da-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c01da-223">0x00000011</span></span>                        |
| <span data-ttu-id="c01da-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c01da-224">Classes used in</span></span>        | [<span data-ttu-id="c01da-225">**User**</span><span class="sxs-lookup"><span data-stu-id="c01da-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c01da-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c01da-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c01da-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="c01da-227">Entry</span></span> | <span data-ttu-id="c01da-228">Value</span><span class="sxs-lookup"><span data-stu-id="c01da-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c01da-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c01da-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c01da-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c01da-231">System-Only</span></span>            | <span data-ttu-id="c01da-232">False</span><span class="sxs-lookup"><span data-stu-id="c01da-232">False</span></span>                             |
| <span data-ttu-id="c01da-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c01da-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c01da-234">True</span><span class="sxs-lookup"><span data-stu-id="c01da-234">True</span></span>                              |
| <span data-ttu-id="c01da-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c01da-235">Is Indexed</span></span>             | <span data-ttu-id="c01da-236">False</span><span class="sxs-lookup"><span data-stu-id="c01da-236">False</span></span>                             |
| <span data-ttu-id="c01da-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c01da-237">In Global Catalog</span></span>      | <span data-ttu-id="c01da-238">False</span><span class="sxs-lookup"><span data-stu-id="c01da-238">False</span></span>                             |
| <span data-ttu-id="c01da-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c01da-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c01da-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c01da-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c01da-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c01da-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c01da-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c01da-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c01da-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-243">Search-Flags</span></span>           | <span data-ttu-id="c01da-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c01da-244">0x00000000</span></span>                        |
| <span data-ttu-id="c01da-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-245">System-Flags</span></span>           | <span data-ttu-id="c01da-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c01da-246">0x00000011</span></span>                        |
| <span data-ttu-id="c01da-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c01da-247">Classes used in</span></span>        | [<span data-ttu-id="c01da-248">**User**</span><span class="sxs-lookup"><span data-stu-id="c01da-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c01da-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c01da-249">Windows Server 2012</span></span>



| <span data-ttu-id="c01da-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="c01da-250">Entry</span></span> | <span data-ttu-id="c01da-251">Value</span><span class="sxs-lookup"><span data-stu-id="c01da-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c01da-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c01da-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c01da-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c01da-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c01da-254">System-Only</span></span>            | <span data-ttu-id="c01da-255">False</span><span class="sxs-lookup"><span data-stu-id="c01da-255">False</span></span>                             |
| <span data-ttu-id="c01da-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c01da-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c01da-257">True</span><span class="sxs-lookup"><span data-stu-id="c01da-257">True</span></span>                              |
| <span data-ttu-id="c01da-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c01da-258">Is Indexed</span></span>             | <span data-ttu-id="c01da-259">False</span><span class="sxs-lookup"><span data-stu-id="c01da-259">False</span></span>                             |
| <span data-ttu-id="c01da-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c01da-260">In Global Catalog</span></span>      | <span data-ttu-id="c01da-261">False</span><span class="sxs-lookup"><span data-stu-id="c01da-261">False</span></span>                             |
| <span data-ttu-id="c01da-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c01da-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c01da-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c01da-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c01da-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c01da-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c01da-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c01da-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c01da-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-266">Search-Flags</span></span>           | <span data-ttu-id="c01da-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c01da-267">0x00000000</span></span>                        |
| <span data-ttu-id="c01da-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c01da-268">System-Flags</span></span>           | <span data-ttu-id="c01da-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="c01da-269">0x00000011</span></span>                        |
| <span data-ttu-id="c01da-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c01da-270">Classes used in</span></span>        | [<span data-ttu-id="c01da-271">**User**</span><span class="sxs-lookup"><span data-stu-id="c01da-271">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c01da-272">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c01da-272">Remarks</span></span>

<span data-ttu-id="c01da-273">La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="c01da-273">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="c01da-274">Este atributo no se replica y se mantiene por separado en cada controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="c01da-274">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="c01da-275">Para obtener un valor preciso para el último inicio de sesión del usuario en el dominio, el atributo **Last-Logon** del usuario se debe recuperar de cada controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="c01da-275">To get an accurate value for the user's last logon in the domain, the **Last-Logon** attribute for the user must be retrieved from every domain controller in the domain.</span></span> <span data-ttu-id="c01da-276">El valor más grande que se recupera es la hora real del último inicio de sesión de ese usuario.</span><span class="sxs-lookup"><span data-stu-id="c01da-276">The largest value that is retrieved is the true last logon time for that user.</span></span>

## <a name="see-also"></a><span data-ttu-id="c01da-277">Vea también</span><span class="sxs-lookup"><span data-stu-id="c01da-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01da-278">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="c01da-278">**FILETIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 


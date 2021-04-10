---
title: atributo msNPAllowDialin
description: Indica si la cuenta tiene permiso para conectarse al servidor RAS.
ms.assetid: 8e0d98b4-93b1-4a76-a8b7-d6017028b48a
ms.tgt_platform: multiple
keywords:
- msNPAllowDialin esquema de AD de atributos
topic_type:
- apiref
api_name:
- msNPAllowDialin
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e56f9fe3817053e3e1e49611fb76934acbbcba9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151784"
---
# <a name="msnpallowdialin-attribute"></a><span data-ttu-id="f2ee7-104">atributo msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="f2ee7-104">msNPAllowDialin attribute</span></span>

<span data-ttu-id="f2ee7-105">Indica si la cuenta tiene permiso para conectarse al servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="f2ee7-105">Indicates whether the account has permission to dial in to the RAS server.</span></span> <span data-ttu-id="f2ee7-106">No modifique este valor directamente.</span><span class="sxs-lookup"><span data-stu-id="f2ee7-106">Do not modify this value directly.</span></span> <span data-ttu-id="f2ee7-107">Utilice la [función de administración ras](/windows/desktop/RRAS/ras-administration-functions) adecuada para modificar este valor.</span><span class="sxs-lookup"><span data-stu-id="f2ee7-107">Use the appropriate [RAS administration function](/windows/desktop/RRAS/ras-administration-functions) to modify this value.</span></span>



| <span data-ttu-id="f2ee7-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2ee7-108">Entry</span></span> | <span data-ttu-id="f2ee7-109">Value</span><span class="sxs-lookup"><span data-stu-id="f2ee7-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f2ee7-110">CN</span><span class="sxs-lookup"><span data-stu-id="f2ee7-110">CN</span></span>                | <span data-ttu-id="f2ee7-111">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="f2ee7-111">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="f2ee7-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f2ee7-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f2ee7-113">msNPAllowDialin</span><span class="sxs-lookup"><span data-stu-id="f2ee7-113">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="f2ee7-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f2ee7-114">Size</span></span>              | <span data-ttu-id="f2ee7-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="f2ee7-115">4 bytes</span></span>                              |
| <span data-ttu-id="f2ee7-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f2ee7-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f2ee7-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f2ee7-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f2ee7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f2ee7-118">Attribute-Id</span></span>      | <span data-ttu-id="f2ee7-119">1.2.840.113556.1.4.1119</span><span class="sxs-lookup"><span data-stu-id="f2ee7-119">1.2.840.113556.1.4.1119</span></span>              |
| <span data-ttu-id="f2ee7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f2ee7-120">System-Id-Guid</span></span>    | <span data-ttu-id="f2ee7-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="f2ee7-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="f2ee7-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2ee7-122">Syntax</span></span>            | [<span data-ttu-id="f2ee7-123">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="f2ee7-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f2ee7-124">Implementations</span></span>

-   [<span data-ttu-id="f2ee7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f2ee7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f2ee7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f2ee7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f2ee7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f2ee7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f2ee7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2ee7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f2ee7-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2ee7-132">Entry</span></span> | <span data-ttu-id="f2ee7-133">Value</span><span class="sxs-lookup"><span data-stu-id="f2ee7-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2ee7-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f2ee7-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ee7-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ee7-136">System-Only</span></span>            | <span data-ttu-id="f2ee7-137">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-137">False</span></span>                             |
| <span data-ttu-id="f2ee7-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f2ee7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ee7-139">True</span><span class="sxs-lookup"><span data-stu-id="f2ee7-139">True</span></span>                              |
| <span data-ttu-id="f2ee7-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f2ee7-140">Is Indexed</span></span>             | <span data-ttu-id="f2ee7-141">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-141">False</span></span>                             |
| <span data-ttu-id="f2ee7-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f2ee7-142">In Global Catalog</span></span>      | <span data-ttu-id="f2ee7-143">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-143">False</span></span>                             |
| <span data-ttu-id="f2ee7-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f2ee7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ee7-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ee7-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2ee7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ee7-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ee7-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-148">Search-Flags</span></span>           | <span data-ttu-id="f2ee7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ee7-149">0x00000000</span></span>                        |
| <span data-ttu-id="f2ee7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-150">System-Flags</span></span>           | <span data-ttu-id="f2ee7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-151">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f2ee7-152">Classes used in</span></span>        | [<span data-ttu-id="f2ee7-153">**User**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f2ee7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2ee7-154">Windows Server 2003</span></span>



| <span data-ttu-id="f2ee7-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2ee7-155">Entry</span></span> | <span data-ttu-id="f2ee7-156">Value</span><span class="sxs-lookup"><span data-stu-id="f2ee7-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2ee7-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f2ee7-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ee7-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ee7-159">System-Only</span></span>            | <span data-ttu-id="f2ee7-160">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-160">False</span></span>                             |
| <span data-ttu-id="f2ee7-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f2ee7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ee7-162">True</span><span class="sxs-lookup"><span data-stu-id="f2ee7-162">True</span></span>                              |
| <span data-ttu-id="f2ee7-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f2ee7-163">Is Indexed</span></span>             | <span data-ttu-id="f2ee7-164">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-164">False</span></span>                             |
| <span data-ttu-id="f2ee7-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f2ee7-165">In Global Catalog</span></span>      | <span data-ttu-id="f2ee7-166">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-166">False</span></span>                             |
| <span data-ttu-id="f2ee7-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f2ee7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ee7-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ee7-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2ee7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ee7-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ee7-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-171">Search-Flags</span></span>           | <span data-ttu-id="f2ee7-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ee7-172">0x00000000</span></span>                        |
| <span data-ttu-id="f2ee7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-173">System-Flags</span></span>           | <span data-ttu-id="f2ee7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-174">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f2ee7-175">Classes used in</span></span>        | [<span data-ttu-id="f2ee7-176">**User**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f2ee7-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2ee7-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f2ee7-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2ee7-178">Entry</span></span> | <span data-ttu-id="f2ee7-179">Value</span><span class="sxs-lookup"><span data-stu-id="f2ee7-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2ee7-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f2ee7-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ee7-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ee7-182">System-Only</span></span>            | <span data-ttu-id="f2ee7-183">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-183">False</span></span>                             |
| <span data-ttu-id="f2ee7-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f2ee7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ee7-185">True</span><span class="sxs-lookup"><span data-stu-id="f2ee7-185">True</span></span>                              |
| <span data-ttu-id="f2ee7-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f2ee7-186">Is Indexed</span></span>             | <span data-ttu-id="f2ee7-187">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-187">False</span></span>                             |
| <span data-ttu-id="f2ee7-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f2ee7-188">In Global Catalog</span></span>      | <span data-ttu-id="f2ee7-189">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-189">False</span></span>                             |
| <span data-ttu-id="f2ee7-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f2ee7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ee7-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ee7-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2ee7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ee7-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ee7-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-194">Search-Flags</span></span>           | <span data-ttu-id="f2ee7-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ee7-195">0x00000000</span></span>                        |
| <span data-ttu-id="f2ee7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-196">System-Flags</span></span>           | <span data-ttu-id="f2ee7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-197">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f2ee7-198">Classes used in</span></span>        | [<span data-ttu-id="f2ee7-199">**User**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f2ee7-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2ee7-200">Windows Server 2008</span></span>



| <span data-ttu-id="f2ee7-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2ee7-201">Entry</span></span> | <span data-ttu-id="f2ee7-202">Value</span><span class="sxs-lookup"><span data-stu-id="f2ee7-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2ee7-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f2ee7-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ee7-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ee7-205">System-Only</span></span>            | <span data-ttu-id="f2ee7-206">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-206">False</span></span>                             |
| <span data-ttu-id="f2ee7-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f2ee7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ee7-208">True</span><span class="sxs-lookup"><span data-stu-id="f2ee7-208">True</span></span>                              |
| <span data-ttu-id="f2ee7-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f2ee7-209">Is Indexed</span></span>             | <span data-ttu-id="f2ee7-210">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-210">False</span></span>                             |
| <span data-ttu-id="f2ee7-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f2ee7-211">In Global Catalog</span></span>      | <span data-ttu-id="f2ee7-212">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-212">False</span></span>                             |
| <span data-ttu-id="f2ee7-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f2ee7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ee7-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ee7-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2ee7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ee7-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ee7-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-217">Search-Flags</span></span>           | <span data-ttu-id="f2ee7-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-218">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-219">System-Flags</span></span>           | <span data-ttu-id="f2ee7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-220">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f2ee7-221">Classes used in</span></span>        | [<span data-ttu-id="f2ee7-222">**User**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f2ee7-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2ee7-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f2ee7-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2ee7-224">Entry</span></span> | <span data-ttu-id="f2ee7-225">Value</span><span class="sxs-lookup"><span data-stu-id="f2ee7-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2ee7-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f2ee7-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ee7-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ee7-228">System-Only</span></span>            | <span data-ttu-id="f2ee7-229">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-229">False</span></span>                             |
| <span data-ttu-id="f2ee7-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f2ee7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ee7-231">True</span><span class="sxs-lookup"><span data-stu-id="f2ee7-231">True</span></span>                              |
| <span data-ttu-id="f2ee7-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f2ee7-232">Is Indexed</span></span>             | <span data-ttu-id="f2ee7-233">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-233">False</span></span>                             |
| <span data-ttu-id="f2ee7-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f2ee7-234">In Global Catalog</span></span>      | <span data-ttu-id="f2ee7-235">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-235">False</span></span>                             |
| <span data-ttu-id="f2ee7-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f2ee7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ee7-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ee7-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2ee7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ee7-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ee7-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-240">Search-Flags</span></span>           | <span data-ttu-id="f2ee7-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-241">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-242">System-Flags</span></span>           | <span data-ttu-id="f2ee7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-243">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f2ee7-244">Classes used in</span></span>        | [<span data-ttu-id="f2ee7-245">**User**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f2ee7-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2ee7-246">Windows Server 2012</span></span>



| <span data-ttu-id="f2ee7-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="f2ee7-247">Entry</span></span> | <span data-ttu-id="f2ee7-248">Value</span><span class="sxs-lookup"><span data-stu-id="f2ee7-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f2ee7-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f2ee7-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ee7-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f2ee7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ee7-251">System-Only</span></span>            | <span data-ttu-id="f2ee7-252">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-252">False</span></span>                             |
| <span data-ttu-id="f2ee7-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f2ee7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ee7-254">True</span><span class="sxs-lookup"><span data-stu-id="f2ee7-254">True</span></span>                              |
| <span data-ttu-id="f2ee7-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f2ee7-255">Is Indexed</span></span>             | <span data-ttu-id="f2ee7-256">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-256">False</span></span>                             |
| <span data-ttu-id="f2ee7-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f2ee7-257">In Global Catalog</span></span>      | <span data-ttu-id="f2ee7-258">False</span><span class="sxs-lookup"><span data-stu-id="f2ee7-258">False</span></span>                             |
| <span data-ttu-id="f2ee7-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f2ee7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ee7-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ee7-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f2ee7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ee7-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ee7-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f2ee7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-263">Search-Flags</span></span>           | <span data-ttu-id="f2ee7-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-264">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ee7-265">System-Flags</span></span>           | <span data-ttu-id="f2ee7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ee7-266">0x00000010</span></span>                        |
| <span data-ttu-id="f2ee7-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f2ee7-267">Classes used in</span></span>        | [<span data-ttu-id="f2ee7-268">**User**</span><span class="sxs-lookup"><span data-stu-id="f2ee7-268">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="f2ee7-269">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2ee7-269">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ee7-270">Funciones de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="f2ee7-270">RAS Administration Functions</span></span>](/windows/desktop/RRAS/ras-administration-functions)
</dt> </dl>

 


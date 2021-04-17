---
title: Server-State atributo)
description: Indica si el servidor está habilitado o deshabilitado.
ms.assetid: e062cbcf-c845-4dfd-9e9b-e21079276a3c
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Server-State
- serverState esquema de AD de atributos
topic_type:
- apiref
api_name:
- Server-State
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be4e236254486cd512eed480b380058048061fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658739"
---
# <a name="server-state-attribute"></a><span data-ttu-id="b598f-105">Server-State atributo)</span><span class="sxs-lookup"><span data-stu-id="b598f-105">Server-State attribute</span></span>

<span data-ttu-id="b598f-106">Indica si el servidor está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b598f-106">Indicates whether the server is enabled or disabled.</span></span> <span data-ttu-id="b598f-107">Un valor de 1 indica que el servidor está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b598f-107">A value of 1 indicates that the server is enabled.</span></span> <span data-ttu-id="b598f-108">Un valor de 2 indica que el servidor está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b598f-108">A value of 2 indicates that the server is disabled.</span></span> <span data-ttu-id="b598f-109">Los demás valores no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b598f-109">All other values are invalid.</span></span>



| <span data-ttu-id="b598f-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="b598f-110">Entry</span></span> | <span data-ttu-id="b598f-111">Value</span><span class="sxs-lookup"><span data-stu-id="b598f-111">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b598f-112">CN</span><span class="sxs-lookup"><span data-stu-id="b598f-112">CN</span></span>                | <span data-ttu-id="b598f-113">Server-State</span><span class="sxs-lookup"><span data-stu-id="b598f-113">Server-State</span></span>                         |
| <span data-ttu-id="b598f-114">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b598f-114">Ldap-Display-Name</span></span> | <span data-ttu-id="b598f-115">serverState</span><span class="sxs-lookup"><span data-stu-id="b598f-115">serverState</span></span>                          |
| <span data-ttu-id="b598f-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b598f-116">Size</span></span>              | \-                                   |
| <span data-ttu-id="b598f-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b598f-117">Update Privilege</span></span>  | <span data-ttu-id="b598f-118">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="b598f-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="b598f-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b598f-119">Update Frequency</span></span>  | <span data-ttu-id="b598f-120">Cuando cambia la Directiva de un usuario.</span><span class="sxs-lookup"><span data-stu-id="b598f-120">When the policy for a user changes.</span></span>  |
| <span data-ttu-id="b598f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b598f-121">Attribute-Id</span></span>      | <span data-ttu-id="b598f-122">1.2.840.113556.1.4.154</span><span class="sxs-lookup"><span data-stu-id="b598f-122">1.2.840.113556.1.4.154</span></span>               |
| <span data-ttu-id="b598f-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b598f-123">System-Id-Guid</span></span>    | <span data-ttu-id="b598f-124">bf967a34-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b598f-124">bf967a34-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b598f-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b598f-125">Syntax</span></span>            | [<span data-ttu-id="b598f-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="b598f-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b598f-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b598f-127">Implementations</span></span>

-   [<span data-ttu-id="b598f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b598f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b598f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b598f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b598f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b598f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b598f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b598f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b598f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b598f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b598f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b598f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b598f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b598f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="b598f-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="b598f-135">Entry</span></span> | <span data-ttu-id="b598f-136">Value</span><span class="sxs-lookup"><span data-stu-id="b598f-136">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b598f-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b598f-137">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b598f-138">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b598f-139">System-Only</span></span>            | <span data-ttu-id="b598f-140">False</span><span class="sxs-lookup"><span data-stu-id="b598f-140">False</span></span>                                                 |
| <span data-ttu-id="b598f-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b598f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b598f-142">True</span><span class="sxs-lookup"><span data-stu-id="b598f-142">True</span></span>                                                  |
| <span data-ttu-id="b598f-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b598f-143">Is Indexed</span></span>             | <span data-ttu-id="b598f-144">False</span><span class="sxs-lookup"><span data-stu-id="b598f-144">False</span></span>                                                 |
| <span data-ttu-id="b598f-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b598f-145">In Global Catalog</span></span>      | <span data-ttu-id="b598f-146">False</span><span class="sxs-lookup"><span data-stu-id="b598f-146">False</span></span>                                                 |
| <span data-ttu-id="b598f-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b598f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b598f-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b598f-148">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b598f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b598f-149">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b598f-150">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-151">Search-Flags</span></span>           | <span data-ttu-id="b598f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b598f-152">0x00000000</span></span>                                            |
| <span data-ttu-id="b598f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-153">System-Flags</span></span>           | <span data-ttu-id="b598f-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b598f-154">0x00000011</span></span>                                            |
| <span data-ttu-id="b598f-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b598f-155">Classes used in</span></span>        | [<span data-ttu-id="b598f-156">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b598f-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b598f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b598f-157">Windows Server 2003</span></span>



| <span data-ttu-id="b598f-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="b598f-158">Entry</span></span> | <span data-ttu-id="b598f-159">Value</span><span class="sxs-lookup"><span data-stu-id="b598f-159">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b598f-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b598f-160">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b598f-161">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b598f-162">System-Only</span></span>            | <span data-ttu-id="b598f-163">False</span><span class="sxs-lookup"><span data-stu-id="b598f-163">False</span></span>                                                 |
| <span data-ttu-id="b598f-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b598f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b598f-165">True</span><span class="sxs-lookup"><span data-stu-id="b598f-165">True</span></span>                                                  |
| <span data-ttu-id="b598f-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b598f-166">Is Indexed</span></span>             | <span data-ttu-id="b598f-167">False</span><span class="sxs-lookup"><span data-stu-id="b598f-167">False</span></span>                                                 |
| <span data-ttu-id="b598f-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b598f-168">In Global Catalog</span></span>      | <span data-ttu-id="b598f-169">False</span><span class="sxs-lookup"><span data-stu-id="b598f-169">False</span></span>                                                 |
| <span data-ttu-id="b598f-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b598f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b598f-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b598f-171">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b598f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b598f-172">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b598f-173">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-174">Search-Flags</span></span>           | <span data-ttu-id="b598f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b598f-175">0x00000000</span></span>                                            |
| <span data-ttu-id="b598f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-176">System-Flags</span></span>           | <span data-ttu-id="b598f-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b598f-177">0x00000011</span></span>                                            |
| <span data-ttu-id="b598f-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b598f-178">Classes used in</span></span>        | [<span data-ttu-id="b598f-179">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b598f-179">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b598f-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b598f-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b598f-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="b598f-181">Entry</span></span> | <span data-ttu-id="b598f-182">Value</span><span class="sxs-lookup"><span data-stu-id="b598f-182">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b598f-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b598f-183">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b598f-184">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b598f-185">System-Only</span></span>            | <span data-ttu-id="b598f-186">False</span><span class="sxs-lookup"><span data-stu-id="b598f-186">False</span></span>                                                 |
| <span data-ttu-id="b598f-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b598f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b598f-188">True</span><span class="sxs-lookup"><span data-stu-id="b598f-188">True</span></span>                                                  |
| <span data-ttu-id="b598f-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b598f-189">Is Indexed</span></span>             | <span data-ttu-id="b598f-190">False</span><span class="sxs-lookup"><span data-stu-id="b598f-190">False</span></span>                                                 |
| <span data-ttu-id="b598f-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b598f-191">In Global Catalog</span></span>      | <span data-ttu-id="b598f-192">False</span><span class="sxs-lookup"><span data-stu-id="b598f-192">False</span></span>                                                 |
| <span data-ttu-id="b598f-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b598f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b598f-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b598f-194">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b598f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b598f-195">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b598f-196">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-197">Search-Flags</span></span>           | <span data-ttu-id="b598f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b598f-198">0x00000000</span></span>                                            |
| <span data-ttu-id="b598f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-199">System-Flags</span></span>           | <span data-ttu-id="b598f-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b598f-200">0x00000011</span></span>                                            |
| <span data-ttu-id="b598f-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b598f-201">Classes used in</span></span>        | [<span data-ttu-id="b598f-202">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b598f-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b598f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b598f-203">Windows Server 2008</span></span>



| <span data-ttu-id="b598f-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="b598f-204">Entry</span></span> | <span data-ttu-id="b598f-205">Value</span><span class="sxs-lookup"><span data-stu-id="b598f-205">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b598f-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b598f-206">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b598f-207">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="b598f-208">System-Only</span></span>            | <span data-ttu-id="b598f-209">False</span><span class="sxs-lookup"><span data-stu-id="b598f-209">False</span></span>                                                 |
| <span data-ttu-id="b598f-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b598f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="b598f-211">True</span><span class="sxs-lookup"><span data-stu-id="b598f-211">True</span></span>                                                  |
| <span data-ttu-id="b598f-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b598f-212">Is Indexed</span></span>             | <span data-ttu-id="b598f-213">False</span><span class="sxs-lookup"><span data-stu-id="b598f-213">False</span></span>                                                 |
| <span data-ttu-id="b598f-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b598f-214">In Global Catalog</span></span>      | <span data-ttu-id="b598f-215">False</span><span class="sxs-lookup"><span data-stu-id="b598f-215">False</span></span>                                                 |
| <span data-ttu-id="b598f-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b598f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="b598f-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b598f-217">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b598f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b598f-218">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b598f-219">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-220">Search-Flags</span></span>           | <span data-ttu-id="b598f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b598f-221">0x00000000</span></span>                                            |
| <span data-ttu-id="b598f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-222">System-Flags</span></span>           | <span data-ttu-id="b598f-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b598f-223">0x00000011</span></span>                                            |
| <span data-ttu-id="b598f-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b598f-224">Classes used in</span></span>        | [<span data-ttu-id="b598f-225">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b598f-225">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b598f-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b598f-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b598f-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="b598f-227">Entry</span></span> | <span data-ttu-id="b598f-228">Value</span><span class="sxs-lookup"><span data-stu-id="b598f-228">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b598f-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b598f-229">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b598f-230">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="b598f-231">System-Only</span></span>            | <span data-ttu-id="b598f-232">False</span><span class="sxs-lookup"><span data-stu-id="b598f-232">False</span></span>                                                 |
| <span data-ttu-id="b598f-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b598f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="b598f-234">True</span><span class="sxs-lookup"><span data-stu-id="b598f-234">True</span></span>                                                  |
| <span data-ttu-id="b598f-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b598f-235">Is Indexed</span></span>             | <span data-ttu-id="b598f-236">False</span><span class="sxs-lookup"><span data-stu-id="b598f-236">False</span></span>                                                 |
| <span data-ttu-id="b598f-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b598f-237">In Global Catalog</span></span>      | <span data-ttu-id="b598f-238">False</span><span class="sxs-lookup"><span data-stu-id="b598f-238">False</span></span>                                                 |
| <span data-ttu-id="b598f-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b598f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="b598f-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b598f-240">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b598f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b598f-241">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b598f-242">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-243">Search-Flags</span></span>           | <span data-ttu-id="b598f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b598f-244">0x00000000</span></span>                                            |
| <span data-ttu-id="b598f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-245">System-Flags</span></span>           | <span data-ttu-id="b598f-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b598f-246">0x00000011</span></span>                                            |
| <span data-ttu-id="b598f-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b598f-247">Classes used in</span></span>        | [<span data-ttu-id="b598f-248">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b598f-248">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b598f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b598f-249">Windows Server 2012</span></span>



| <span data-ttu-id="b598f-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="b598f-250">Entry</span></span> | <span data-ttu-id="b598f-251">Value</span><span class="sxs-lookup"><span data-stu-id="b598f-251">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b598f-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b598f-252">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b598f-253">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b598f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="b598f-254">System-Only</span></span>            | <span data-ttu-id="b598f-255">False</span><span class="sxs-lookup"><span data-stu-id="b598f-255">False</span></span>                                                 |
| <span data-ttu-id="b598f-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b598f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="b598f-257">True</span><span class="sxs-lookup"><span data-stu-id="b598f-257">True</span></span>                                                  |
| <span data-ttu-id="b598f-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b598f-258">Is Indexed</span></span>             | <span data-ttu-id="b598f-259">False</span><span class="sxs-lookup"><span data-stu-id="b598f-259">False</span></span>                                                 |
| <span data-ttu-id="b598f-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b598f-260">In Global Catalog</span></span>      | <span data-ttu-id="b598f-261">False</span><span class="sxs-lookup"><span data-stu-id="b598f-261">False</span></span>                                                 |
| <span data-ttu-id="b598f-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b598f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="b598f-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b598f-263">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b598f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b598f-264">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b598f-265">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b598f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-266">Search-Flags</span></span>           | <span data-ttu-id="b598f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b598f-267">0x00000000</span></span>                                            |
| <span data-ttu-id="b598f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b598f-268">System-Flags</span></span>           | <span data-ttu-id="b598f-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="b598f-269">0x00000011</span></span>                                            |
| <span data-ttu-id="b598f-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b598f-270">Classes used in</span></span>        | [<span data-ttu-id="b598f-271">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b598f-271">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 






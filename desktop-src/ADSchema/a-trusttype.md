---
title: Trust-Type atributo)
description: El tipo de confianza, por ejemplo, Windows NT o MIT.
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Trust-Type
- trustType esquema de AD de atributos
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b8a8f59f7df976f968bb4f2915e667a06e95bb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997361"
---
# <a name="trust-type-attribute"></a><span data-ttu-id="2b939-105">Trust-Type atributo)</span><span class="sxs-lookup"><span data-stu-id="2b939-105">Trust-Type attribute</span></span>

<span data-ttu-id="2b939-106">El tipo de confianza, por ejemplo, Windows NT o MIT.</span><span class="sxs-lookup"><span data-stu-id="2b939-106">The type of trust, for example, Windows NT or MIT.</span></span>



| <span data-ttu-id="2b939-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b939-107">Entry</span></span> | <span data-ttu-id="2b939-108">Value</span><span class="sxs-lookup"><span data-stu-id="2b939-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2b939-109">CN</span><span class="sxs-lookup"><span data-stu-id="2b939-109">CN</span></span>                | <span data-ttu-id="2b939-110">Trust-Type</span><span class="sxs-lookup"><span data-stu-id="2b939-110">Trust-Type</span></span>                           |
| <span data-ttu-id="2b939-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="2b939-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2b939-112">trustType</span><span class="sxs-lookup"><span data-stu-id="2b939-112">trustType</span></span>                            |
| <span data-ttu-id="2b939-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2b939-113">Size</span></span>              | <span data-ttu-id="2b939-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="2b939-114">4 bytes</span></span>                              |
| <span data-ttu-id="2b939-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="2b939-115">Update Privilege</span></span>  | <span data-ttu-id="2b939-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="2b939-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="2b939-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="2b939-117">Update Frequency</span></span>  | <span data-ttu-id="2b939-118">Cuando se crea una nueva confianza.</span><span class="sxs-lookup"><span data-stu-id="2b939-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="2b939-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2b939-119">Attribute-Id</span></span>      | <span data-ttu-id="2b939-120">1.2.840.113556.1.4.136</span><span class="sxs-lookup"><span data-stu-id="2b939-120">1.2.840.113556.1.4.136</span></span>               |
| <span data-ttu-id="2b939-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2b939-121">System-Id-Guid</span></span>    | <span data-ttu-id="2b939-122">bf967a60-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2b939-122">bf967a60-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2b939-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b939-123">Syntax</span></span>            | [<span data-ttu-id="2b939-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="2b939-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="2b939-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="2b939-125">Implementations</span></span>

-   [<span data-ttu-id="2b939-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2b939-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2b939-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2b939-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2b939-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2b939-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2b939-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2b939-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2b939-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2b939-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2b939-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2b939-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2b939-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b939-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2b939-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b939-133">Entry</span></span> | <span data-ttu-id="2b939-134">Value</span><span class="sxs-lookup"><span data-stu-id="2b939-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2b939-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2b939-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b939-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b939-137">System-Only</span></span>            | <span data-ttu-id="2b939-138">False</span><span class="sxs-lookup"><span data-stu-id="2b939-138">False</span></span>                                                |
| <span data-ttu-id="2b939-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2b939-139">Is-Single-Valued</span></span>       | <span data-ttu-id="2b939-140">True</span><span class="sxs-lookup"><span data-stu-id="2b939-140">True</span></span>                                                 |
| <span data-ttu-id="2b939-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2b939-141">Is Indexed</span></span>             | <span data-ttu-id="2b939-142">False</span><span class="sxs-lookup"><span data-stu-id="2b939-142">False</span></span>                                                |
| <span data-ttu-id="2b939-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2b939-143">In Global Catalog</span></span>      | <span data-ttu-id="2b939-144">False</span><span class="sxs-lookup"><span data-stu-id="2b939-144">False</span></span>                                                |
| <span data-ttu-id="2b939-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2b939-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b939-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b939-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2b939-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b939-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b939-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-149">Search-Flags</span></span>           | <span data-ttu-id="2b939-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b939-150">0x00000000</span></span>                                           |
| <span data-ttu-id="2b939-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-151">System-Flags</span></span>           | <span data-ttu-id="2b939-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b939-152">0x00000010</span></span>                                           |
| <span data-ttu-id="2b939-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2b939-153">Classes used in</span></span>        | [<span data-ttu-id="2b939-154">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2b939-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2b939-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b939-155">Windows Server 2003</span></span>



| <span data-ttu-id="2b939-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b939-156">Entry</span></span> | <span data-ttu-id="2b939-157">Value</span><span class="sxs-lookup"><span data-stu-id="2b939-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2b939-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2b939-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b939-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b939-160">System-Only</span></span>            | <span data-ttu-id="2b939-161">False</span><span class="sxs-lookup"><span data-stu-id="2b939-161">False</span></span>                                                |
| <span data-ttu-id="2b939-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2b939-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2b939-163">True</span><span class="sxs-lookup"><span data-stu-id="2b939-163">True</span></span>                                                 |
| <span data-ttu-id="2b939-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2b939-164">Is Indexed</span></span>             | <span data-ttu-id="2b939-165">False</span><span class="sxs-lookup"><span data-stu-id="2b939-165">False</span></span>                                                |
| <span data-ttu-id="2b939-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2b939-166">In Global Catalog</span></span>      | <span data-ttu-id="2b939-167">True</span><span class="sxs-lookup"><span data-stu-id="2b939-167">True</span></span>                                                 |
| <span data-ttu-id="2b939-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2b939-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b939-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b939-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2b939-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b939-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b939-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-172">Search-Flags</span></span>           | <span data-ttu-id="2b939-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b939-173">0x00000000</span></span>                                           |
| <span data-ttu-id="2b939-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-174">System-Flags</span></span>           | <span data-ttu-id="2b939-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b939-175">0x00000010</span></span>                                           |
| <span data-ttu-id="2b939-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2b939-176">Classes used in</span></span>        | [<span data-ttu-id="2b939-177">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2b939-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2b939-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2b939-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2b939-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b939-179">Entry</span></span> | <span data-ttu-id="2b939-180">Value</span><span class="sxs-lookup"><span data-stu-id="2b939-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2b939-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2b939-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b939-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b939-183">System-Only</span></span>            | <span data-ttu-id="2b939-184">False</span><span class="sxs-lookup"><span data-stu-id="2b939-184">False</span></span>                                                |
| <span data-ttu-id="2b939-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2b939-185">Is-Single-Valued</span></span>       | <span data-ttu-id="2b939-186">True</span><span class="sxs-lookup"><span data-stu-id="2b939-186">True</span></span>                                                 |
| <span data-ttu-id="2b939-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2b939-187">Is Indexed</span></span>             | <span data-ttu-id="2b939-188">False</span><span class="sxs-lookup"><span data-stu-id="2b939-188">False</span></span>                                                |
| <span data-ttu-id="2b939-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2b939-189">In Global Catalog</span></span>      | <span data-ttu-id="2b939-190">True</span><span class="sxs-lookup"><span data-stu-id="2b939-190">True</span></span>                                                 |
| <span data-ttu-id="2b939-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2b939-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b939-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b939-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2b939-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b939-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b939-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-195">Search-Flags</span></span>           | <span data-ttu-id="2b939-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b939-196">0x00000000</span></span>                                           |
| <span data-ttu-id="2b939-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-197">System-Flags</span></span>           | <span data-ttu-id="2b939-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b939-198">0x00000010</span></span>                                           |
| <span data-ttu-id="2b939-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2b939-199">Classes used in</span></span>        | [<span data-ttu-id="2b939-200">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2b939-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2b939-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b939-201">Windows Server 2008</span></span>



| <span data-ttu-id="2b939-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b939-202">Entry</span></span> | <span data-ttu-id="2b939-203">Value</span><span class="sxs-lookup"><span data-stu-id="2b939-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2b939-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2b939-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b939-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b939-206">System-Only</span></span>            | <span data-ttu-id="2b939-207">False</span><span class="sxs-lookup"><span data-stu-id="2b939-207">False</span></span>                                                |
| <span data-ttu-id="2b939-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2b939-208">Is-Single-Valued</span></span>       | <span data-ttu-id="2b939-209">True</span><span class="sxs-lookup"><span data-stu-id="2b939-209">True</span></span>                                                 |
| <span data-ttu-id="2b939-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2b939-210">Is Indexed</span></span>             | <span data-ttu-id="2b939-211">False</span><span class="sxs-lookup"><span data-stu-id="2b939-211">False</span></span>                                                |
| <span data-ttu-id="2b939-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2b939-212">In Global Catalog</span></span>      | <span data-ttu-id="2b939-213">True</span><span class="sxs-lookup"><span data-stu-id="2b939-213">True</span></span>                                                 |
| <span data-ttu-id="2b939-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2b939-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b939-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b939-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2b939-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b939-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b939-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-218">Search-Flags</span></span>           | <span data-ttu-id="2b939-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b939-219">0x00000000</span></span>                                           |
| <span data-ttu-id="2b939-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-220">System-Flags</span></span>           | <span data-ttu-id="2b939-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b939-221">0x00000010</span></span>                                           |
| <span data-ttu-id="2b939-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2b939-222">Classes used in</span></span>        | [<span data-ttu-id="2b939-223">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2b939-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2b939-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b939-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2b939-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b939-225">Entry</span></span> | <span data-ttu-id="2b939-226">Value</span><span class="sxs-lookup"><span data-stu-id="2b939-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2b939-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2b939-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b939-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b939-229">System-Only</span></span>            | <span data-ttu-id="2b939-230">False</span><span class="sxs-lookup"><span data-stu-id="2b939-230">False</span></span>                                                |
| <span data-ttu-id="2b939-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2b939-231">Is-Single-Valued</span></span>       | <span data-ttu-id="2b939-232">True</span><span class="sxs-lookup"><span data-stu-id="2b939-232">True</span></span>                                                 |
| <span data-ttu-id="2b939-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2b939-233">Is Indexed</span></span>             | <span data-ttu-id="2b939-234">False</span><span class="sxs-lookup"><span data-stu-id="2b939-234">False</span></span>                                                |
| <span data-ttu-id="2b939-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2b939-235">In Global Catalog</span></span>      | <span data-ttu-id="2b939-236">True</span><span class="sxs-lookup"><span data-stu-id="2b939-236">True</span></span>                                                 |
| <span data-ttu-id="2b939-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2b939-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b939-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b939-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2b939-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b939-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b939-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-241">Search-Flags</span></span>           | <span data-ttu-id="2b939-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b939-242">0x00000000</span></span>                                           |
| <span data-ttu-id="2b939-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-243">System-Flags</span></span>           | <span data-ttu-id="2b939-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b939-244">0x00000010</span></span>                                           |
| <span data-ttu-id="2b939-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2b939-245">Classes used in</span></span>        | [<span data-ttu-id="2b939-246">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2b939-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2b939-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b939-247">Windows Server 2012</span></span>



| <span data-ttu-id="2b939-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="2b939-248">Entry</span></span> | <span data-ttu-id="2b939-249">Value</span><span class="sxs-lookup"><span data-stu-id="2b939-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2b939-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2b939-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b939-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2b939-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b939-252">System-Only</span></span>            | <span data-ttu-id="2b939-253">False</span><span class="sxs-lookup"><span data-stu-id="2b939-253">False</span></span>                                                |
| <span data-ttu-id="2b939-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2b939-254">Is-Single-Valued</span></span>       | <span data-ttu-id="2b939-255">True</span><span class="sxs-lookup"><span data-stu-id="2b939-255">True</span></span>                                                 |
| <span data-ttu-id="2b939-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2b939-256">Is Indexed</span></span>             | <span data-ttu-id="2b939-257">False</span><span class="sxs-lookup"><span data-stu-id="2b939-257">False</span></span>                                                |
| <span data-ttu-id="2b939-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2b939-258">In Global Catalog</span></span>      | <span data-ttu-id="2b939-259">True</span><span class="sxs-lookup"><span data-stu-id="2b939-259">True</span></span>                                                 |
| <span data-ttu-id="2b939-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2b939-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b939-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b939-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2b939-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b939-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b939-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2b939-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-264">Search-Flags</span></span>           | <span data-ttu-id="2b939-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b939-265">0x00000000</span></span>                                           |
| <span data-ttu-id="2b939-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b939-266">System-Flags</span></span>           | <span data-ttu-id="2b939-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b939-267">0x00000010</span></span>                                           |
| <span data-ttu-id="2b939-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2b939-268">Classes used in</span></span>        | [<span data-ttu-id="2b939-269">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2b939-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






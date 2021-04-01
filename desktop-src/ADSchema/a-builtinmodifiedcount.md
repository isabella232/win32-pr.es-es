---
title: Atributo Builtin-Modified-Count
description: El atributo Builtin-Modified-Count se usa para admitir la replicación en los dominios de Windows NT 4,0.
ms.assetid: e5a0f299-1e69-4b47-a0b1-e5bcf7bd47eb
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Builtin-Modified-Count
- builtinModifiedCount esquema de AD de atributos
topic_type:
- apiref
api_name:
- Builtin-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731cd27ef5cb5d25dcd4bced4dbc5932225ba5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151861"
---
# <a name="builtin-modified-count-attribute"></a><span data-ttu-id="36a1d-105">Atributo Builtin-Modified-Count</span><span class="sxs-lookup"><span data-stu-id="36a1d-105">Builtin-Modified-Count attribute</span></span>

<span data-ttu-id="36a1d-106">El atributo **Builtin-Modified-Count** se usa para admitir la replicación en los dominios de Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="36a1d-106">The **Builtin-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="36a1d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="36a1d-107">Entry</span></span> | <span data-ttu-id="36a1d-108">Value</span><span class="sxs-lookup"><span data-stu-id="36a1d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="36a1d-109">CN</span><span class="sxs-lookup"><span data-stu-id="36a1d-109">CN</span></span>                | <span data-ttu-id="36a1d-110">Builtin-Modified-Count</span><span class="sxs-lookup"><span data-stu-id="36a1d-110">Builtin-Modified-Count</span></span>               |
| <span data-ttu-id="36a1d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="36a1d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="36a1d-112">builtinModifiedCount</span><span class="sxs-lookup"><span data-stu-id="36a1d-112">builtinModifiedCount</span></span>                 |
| <span data-ttu-id="36a1d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="36a1d-113">Size</span></span>              | <span data-ttu-id="36a1d-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="36a1d-114">8 bytes</span></span>                              |
| <span data-ttu-id="36a1d-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="36a1d-115">Update Privilege</span></span>  | <span data-ttu-id="36a1d-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="36a1d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="36a1d-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="36a1d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="36a1d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36a1d-118">Attribute-Id</span></span>      | <span data-ttu-id="36a1d-119">1.2.840.113556.1.4.14</span><span class="sxs-lookup"><span data-stu-id="36a1d-119">1.2.840.113556.1.4.14</span></span>                |
| <span data-ttu-id="36a1d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="36a1d-120">System-Id-Guid</span></span>    | <span data-ttu-id="36a1d-121">bf967930-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="36a1d-121">bf967930-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="36a1d-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36a1d-122">Syntax</span></span>            | [<span data-ttu-id="36a1d-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="36a1d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="36a1d-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="36a1d-124">Implementations</span></span>

-   [<span data-ttu-id="36a1d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="36a1d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="36a1d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="36a1d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="36a1d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="36a1d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="36a1d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36a1d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36a1d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36a1d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36a1d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36a1d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="36a1d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36a1d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="36a1d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="36a1d-132">Entry</span></span> | <span data-ttu-id="36a1d-133">Value</span><span class="sxs-lookup"><span data-stu-id="36a1d-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="36a1d-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="36a1d-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a1d-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a1d-136">System-Only</span></span>            | <span data-ttu-id="36a1d-137">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-137">False</span></span>                                        |
| <span data-ttu-id="36a1d-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="36a1d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="36a1d-139">True</span><span class="sxs-lookup"><span data-stu-id="36a1d-139">True</span></span>                                         |
| <span data-ttu-id="36a1d-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="36a1d-140">Is Indexed</span></span>             | <span data-ttu-id="36a1d-141">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-141">False</span></span>                                        |
| <span data-ttu-id="36a1d-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="36a1d-142">In Global Catalog</span></span>      | <span data-ttu-id="36a1d-143">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-143">False</span></span>                                        |
| <span data-ttu-id="36a1d-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="36a1d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a1d-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a1d-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="36a1d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a1d-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a1d-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-148">Search-Flags</span></span>           | <span data-ttu-id="36a1d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36a1d-149">0x00000000</span></span>                                   |
| <span data-ttu-id="36a1d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-150">System-Flags</span></span>           | <span data-ttu-id="36a1d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a1d-151">0x00000010</span></span>                                   |
| <span data-ttu-id="36a1d-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="36a1d-152">Classes used in</span></span>        | [<span data-ttu-id="36a1d-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="36a1d-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="36a1d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36a1d-154">Windows Server 2003</span></span>



| <span data-ttu-id="36a1d-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="36a1d-155">Entry</span></span> | <span data-ttu-id="36a1d-156">Value</span><span class="sxs-lookup"><span data-stu-id="36a1d-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="36a1d-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="36a1d-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a1d-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a1d-159">System-Only</span></span>            | <span data-ttu-id="36a1d-160">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-160">False</span></span>                                        |
| <span data-ttu-id="36a1d-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="36a1d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="36a1d-162">True</span><span class="sxs-lookup"><span data-stu-id="36a1d-162">True</span></span>                                         |
| <span data-ttu-id="36a1d-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="36a1d-163">Is Indexed</span></span>             | <span data-ttu-id="36a1d-164">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-164">False</span></span>                                        |
| <span data-ttu-id="36a1d-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="36a1d-165">In Global Catalog</span></span>      | <span data-ttu-id="36a1d-166">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-166">False</span></span>                                        |
| <span data-ttu-id="36a1d-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="36a1d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a1d-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a1d-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="36a1d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a1d-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a1d-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-171">Search-Flags</span></span>           | <span data-ttu-id="36a1d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36a1d-172">0x00000000</span></span>                                   |
| <span data-ttu-id="36a1d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-173">System-Flags</span></span>           | <span data-ttu-id="36a1d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a1d-174">0x00000010</span></span>                                   |
| <span data-ttu-id="36a1d-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="36a1d-175">Classes used in</span></span>        | [<span data-ttu-id="36a1d-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="36a1d-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="36a1d-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="36a1d-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="36a1d-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="36a1d-178">Entry</span></span> | <span data-ttu-id="36a1d-179">Value</span><span class="sxs-lookup"><span data-stu-id="36a1d-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="36a1d-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="36a1d-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a1d-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a1d-182">System-Only</span></span>            | <span data-ttu-id="36a1d-183">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-183">False</span></span>                                        |
| <span data-ttu-id="36a1d-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="36a1d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="36a1d-185">True</span><span class="sxs-lookup"><span data-stu-id="36a1d-185">True</span></span>                                         |
| <span data-ttu-id="36a1d-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="36a1d-186">Is Indexed</span></span>             | <span data-ttu-id="36a1d-187">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-187">False</span></span>                                        |
| <span data-ttu-id="36a1d-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="36a1d-188">In Global Catalog</span></span>      | <span data-ttu-id="36a1d-189">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-189">False</span></span>                                        |
| <span data-ttu-id="36a1d-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="36a1d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a1d-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a1d-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="36a1d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a1d-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a1d-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-194">Search-Flags</span></span>           | <span data-ttu-id="36a1d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36a1d-195">0x00000000</span></span>                                   |
| <span data-ttu-id="36a1d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-196">System-Flags</span></span>           | <span data-ttu-id="36a1d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a1d-197">0x00000010</span></span>                                   |
| <span data-ttu-id="36a1d-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="36a1d-198">Classes used in</span></span>        | [<span data-ttu-id="36a1d-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="36a1d-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="36a1d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36a1d-200">Windows Server 2008</span></span>



| <span data-ttu-id="36a1d-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="36a1d-201">Entry</span></span> | <span data-ttu-id="36a1d-202">Value</span><span class="sxs-lookup"><span data-stu-id="36a1d-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="36a1d-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="36a1d-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a1d-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a1d-205">System-Only</span></span>            | <span data-ttu-id="36a1d-206">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-206">False</span></span>                                        |
| <span data-ttu-id="36a1d-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="36a1d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="36a1d-208">True</span><span class="sxs-lookup"><span data-stu-id="36a1d-208">True</span></span>                                         |
| <span data-ttu-id="36a1d-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="36a1d-209">Is Indexed</span></span>             | <span data-ttu-id="36a1d-210">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-210">False</span></span>                                        |
| <span data-ttu-id="36a1d-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="36a1d-211">In Global Catalog</span></span>      | <span data-ttu-id="36a1d-212">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-212">False</span></span>                                        |
| <span data-ttu-id="36a1d-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="36a1d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a1d-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a1d-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="36a1d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a1d-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a1d-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-217">Search-Flags</span></span>           | <span data-ttu-id="36a1d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36a1d-218">0x00000000</span></span>                                   |
| <span data-ttu-id="36a1d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-219">System-Flags</span></span>           | <span data-ttu-id="36a1d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a1d-220">0x00000010</span></span>                                   |
| <span data-ttu-id="36a1d-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="36a1d-221">Classes used in</span></span>        | [<span data-ttu-id="36a1d-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="36a1d-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36a1d-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36a1d-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36a1d-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="36a1d-224">Entry</span></span> | <span data-ttu-id="36a1d-225">Value</span><span class="sxs-lookup"><span data-stu-id="36a1d-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="36a1d-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="36a1d-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a1d-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a1d-228">System-Only</span></span>            | <span data-ttu-id="36a1d-229">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-229">False</span></span>                                        |
| <span data-ttu-id="36a1d-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="36a1d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="36a1d-231">True</span><span class="sxs-lookup"><span data-stu-id="36a1d-231">True</span></span>                                         |
| <span data-ttu-id="36a1d-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="36a1d-232">Is Indexed</span></span>             | <span data-ttu-id="36a1d-233">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-233">False</span></span>                                        |
| <span data-ttu-id="36a1d-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="36a1d-234">In Global Catalog</span></span>      | <span data-ttu-id="36a1d-235">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-235">False</span></span>                                        |
| <span data-ttu-id="36a1d-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="36a1d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a1d-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a1d-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="36a1d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a1d-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a1d-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-240">Search-Flags</span></span>           | <span data-ttu-id="36a1d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36a1d-241">0x00000000</span></span>                                   |
| <span data-ttu-id="36a1d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-242">System-Flags</span></span>           | <span data-ttu-id="36a1d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a1d-243">0x00000010</span></span>                                   |
| <span data-ttu-id="36a1d-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="36a1d-244">Classes used in</span></span>        | [<span data-ttu-id="36a1d-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="36a1d-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36a1d-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36a1d-246">Windows Server 2012</span></span>



| <span data-ttu-id="36a1d-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="36a1d-247">Entry</span></span> | <span data-ttu-id="36a1d-248">Value</span><span class="sxs-lookup"><span data-stu-id="36a1d-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="36a1d-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="36a1d-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a1d-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="36a1d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a1d-251">System-Only</span></span>            | <span data-ttu-id="36a1d-252">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-252">False</span></span>                                        |
| <span data-ttu-id="36a1d-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="36a1d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="36a1d-254">True</span><span class="sxs-lookup"><span data-stu-id="36a1d-254">True</span></span>                                         |
| <span data-ttu-id="36a1d-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="36a1d-255">Is Indexed</span></span>             | <span data-ttu-id="36a1d-256">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-256">False</span></span>                                        |
| <span data-ttu-id="36a1d-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="36a1d-257">In Global Catalog</span></span>      | <span data-ttu-id="36a1d-258">False</span><span class="sxs-lookup"><span data-stu-id="36a1d-258">False</span></span>                                        |
| <span data-ttu-id="36a1d-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="36a1d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a1d-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a1d-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="36a1d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a1d-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a1d-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="36a1d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-263">Search-Flags</span></span>           | <span data-ttu-id="36a1d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36a1d-264">0x00000000</span></span>                                   |
| <span data-ttu-id="36a1d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a1d-265">System-Flags</span></span>           | <span data-ttu-id="36a1d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a1d-266">0x00000010</span></span>                                   |
| <span data-ttu-id="36a1d-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="36a1d-267">Classes used in</span></span>        | [<span data-ttu-id="36a1d-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="36a1d-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






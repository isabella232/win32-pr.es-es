---
title: Atributo Builtin-Creation-time
description: El atributo Builtin-Creation-time se usa para admitir la replicación en los dominios de Windows NT 4,0.
ms.assetid: b3da9913-8c7b-481b-ae47-6b124544f1e2
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos integrados en tiempo de creación
- builtinCreationTime esquema de AD de atributos
topic_type:
- apiref
api_name:
- Builtin-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d5b6d37ee0242999afd47415cb067abe26e7fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906268"
---
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="e508d-105">Atributo Builtin-Creation-time</span><span class="sxs-lookup"><span data-stu-id="e508d-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="e508d-106">El atributo **Builtin-Creation-time** se usa para admitir la replicación en los dominios de Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="e508d-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="e508d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e508d-107">Entry</span></span> | <span data-ttu-id="e508d-108">Value</span><span class="sxs-lookup"><span data-stu-id="e508d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e508d-109">CN</span><span class="sxs-lookup"><span data-stu-id="e508d-109">CN</span></span>                | <span data-ttu-id="e508d-110">Integrado en tiempo de creación</span><span class="sxs-lookup"><span data-stu-id="e508d-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="e508d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e508d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e508d-112">builtinCreationTime</span><span class="sxs-lookup"><span data-stu-id="e508d-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="e508d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e508d-113">Size</span></span>              | <span data-ttu-id="e508d-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="e508d-114">8 bytes</span></span>                              |
| <span data-ttu-id="e508d-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e508d-115">Update Privilege</span></span>  | <span data-ttu-id="e508d-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="e508d-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="e508d-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e508d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e508d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e508d-118">Attribute-Id</span></span>      | <span data-ttu-id="e508d-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="e508d-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="e508d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e508d-120">System-Id-Guid</span></span>    | <span data-ttu-id="e508d-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e508d-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e508d-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e508d-122">Syntax</span></span>            | [<span data-ttu-id="e508d-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="e508d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e508d-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e508d-124">Implementations</span></span>

-   [<span data-ttu-id="e508d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e508d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e508d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e508d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e508d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e508d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e508d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e508d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e508d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e508d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e508d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e508d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e508d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e508d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e508d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e508d-132">Entry</span></span> | <span data-ttu-id="e508d-133">Value</span><span class="sxs-lookup"><span data-stu-id="e508d-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e508d-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e508d-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e508d-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e508d-136">System-Only</span></span>            | <span data-ttu-id="e508d-137">False</span><span class="sxs-lookup"><span data-stu-id="e508d-137">False</span></span>                                        |
| <span data-ttu-id="e508d-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e508d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e508d-139">True</span><span class="sxs-lookup"><span data-stu-id="e508d-139">True</span></span>                                         |
| <span data-ttu-id="e508d-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e508d-140">Is Indexed</span></span>             | <span data-ttu-id="e508d-141">False</span><span class="sxs-lookup"><span data-stu-id="e508d-141">False</span></span>                                        |
| <span data-ttu-id="e508d-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e508d-142">In Global Catalog</span></span>      | <span data-ttu-id="e508d-143">False</span><span class="sxs-lookup"><span data-stu-id="e508d-143">False</span></span>                                        |
| <span data-ttu-id="e508d-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e508d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e508d-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e508d-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e508d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e508d-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e508d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e508d-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e508d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-148">Search-Flags</span></span>           | <span data-ttu-id="e508d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e508d-149">0x00000000</span></span>                                   |
| <span data-ttu-id="e508d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-150">System-Flags</span></span>           | <span data-ttu-id="e508d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e508d-151">0x00000010</span></span>                                   |
| <span data-ttu-id="e508d-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e508d-152">Classes used in</span></span>        | [<span data-ttu-id="e508d-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="e508d-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e508d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e508d-154">Windows Server 2003</span></span>



| <span data-ttu-id="e508d-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="e508d-155">Entry</span></span> | <span data-ttu-id="e508d-156">Value</span><span class="sxs-lookup"><span data-stu-id="e508d-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e508d-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e508d-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e508d-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e508d-159">System-Only</span></span>            | <span data-ttu-id="e508d-160">False</span><span class="sxs-lookup"><span data-stu-id="e508d-160">False</span></span>                                        |
| <span data-ttu-id="e508d-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e508d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e508d-162">True</span><span class="sxs-lookup"><span data-stu-id="e508d-162">True</span></span>                                         |
| <span data-ttu-id="e508d-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e508d-163">Is Indexed</span></span>             | <span data-ttu-id="e508d-164">False</span><span class="sxs-lookup"><span data-stu-id="e508d-164">False</span></span>                                        |
| <span data-ttu-id="e508d-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e508d-165">In Global Catalog</span></span>      | <span data-ttu-id="e508d-166">False</span><span class="sxs-lookup"><span data-stu-id="e508d-166">False</span></span>                                        |
| <span data-ttu-id="e508d-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e508d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e508d-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e508d-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e508d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e508d-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e508d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e508d-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e508d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-171">Search-Flags</span></span>           | <span data-ttu-id="e508d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e508d-172">0x00000000</span></span>                                   |
| <span data-ttu-id="e508d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-173">System-Flags</span></span>           | <span data-ttu-id="e508d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e508d-174">0x00000010</span></span>                                   |
| <span data-ttu-id="e508d-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e508d-175">Classes used in</span></span>        | [<span data-ttu-id="e508d-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="e508d-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e508d-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e508d-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e508d-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="e508d-178">Entry</span></span> | <span data-ttu-id="e508d-179">Value</span><span class="sxs-lookup"><span data-stu-id="e508d-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e508d-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e508d-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e508d-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e508d-182">System-Only</span></span>            | <span data-ttu-id="e508d-183">False</span><span class="sxs-lookup"><span data-stu-id="e508d-183">False</span></span>                                        |
| <span data-ttu-id="e508d-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e508d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e508d-185">True</span><span class="sxs-lookup"><span data-stu-id="e508d-185">True</span></span>                                         |
| <span data-ttu-id="e508d-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e508d-186">Is Indexed</span></span>             | <span data-ttu-id="e508d-187">False</span><span class="sxs-lookup"><span data-stu-id="e508d-187">False</span></span>                                        |
| <span data-ttu-id="e508d-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e508d-188">In Global Catalog</span></span>      | <span data-ttu-id="e508d-189">False</span><span class="sxs-lookup"><span data-stu-id="e508d-189">False</span></span>                                        |
| <span data-ttu-id="e508d-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e508d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e508d-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e508d-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e508d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e508d-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e508d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e508d-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e508d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-194">Search-Flags</span></span>           | <span data-ttu-id="e508d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e508d-195">0x00000000</span></span>                                   |
| <span data-ttu-id="e508d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-196">System-Flags</span></span>           | <span data-ttu-id="e508d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e508d-197">0x00000010</span></span>                                   |
| <span data-ttu-id="e508d-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e508d-198">Classes used in</span></span>        | [<span data-ttu-id="e508d-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="e508d-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e508d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e508d-200">Windows Server 2008</span></span>



| <span data-ttu-id="e508d-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="e508d-201">Entry</span></span> | <span data-ttu-id="e508d-202">Value</span><span class="sxs-lookup"><span data-stu-id="e508d-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e508d-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e508d-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e508d-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e508d-205">System-Only</span></span>            | <span data-ttu-id="e508d-206">False</span><span class="sxs-lookup"><span data-stu-id="e508d-206">False</span></span>                                        |
| <span data-ttu-id="e508d-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e508d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e508d-208">True</span><span class="sxs-lookup"><span data-stu-id="e508d-208">True</span></span>                                         |
| <span data-ttu-id="e508d-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e508d-209">Is Indexed</span></span>             | <span data-ttu-id="e508d-210">False</span><span class="sxs-lookup"><span data-stu-id="e508d-210">False</span></span>                                        |
| <span data-ttu-id="e508d-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e508d-211">In Global Catalog</span></span>      | <span data-ttu-id="e508d-212">False</span><span class="sxs-lookup"><span data-stu-id="e508d-212">False</span></span>                                        |
| <span data-ttu-id="e508d-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e508d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e508d-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e508d-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e508d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e508d-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e508d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e508d-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e508d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-217">Search-Flags</span></span>           | <span data-ttu-id="e508d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e508d-218">0x00000000</span></span>                                   |
| <span data-ttu-id="e508d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-219">System-Flags</span></span>           | <span data-ttu-id="e508d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e508d-220">0x00000010</span></span>                                   |
| <span data-ttu-id="e508d-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e508d-221">Classes used in</span></span>        | [<span data-ttu-id="e508d-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="e508d-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e508d-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e508d-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e508d-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="e508d-224">Entry</span></span> | <span data-ttu-id="e508d-225">Value</span><span class="sxs-lookup"><span data-stu-id="e508d-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e508d-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e508d-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e508d-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e508d-228">System-Only</span></span>            | <span data-ttu-id="e508d-229">False</span><span class="sxs-lookup"><span data-stu-id="e508d-229">False</span></span>                                        |
| <span data-ttu-id="e508d-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e508d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e508d-231">True</span><span class="sxs-lookup"><span data-stu-id="e508d-231">True</span></span>                                         |
| <span data-ttu-id="e508d-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e508d-232">Is Indexed</span></span>             | <span data-ttu-id="e508d-233">False</span><span class="sxs-lookup"><span data-stu-id="e508d-233">False</span></span>                                        |
| <span data-ttu-id="e508d-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e508d-234">In Global Catalog</span></span>      | <span data-ttu-id="e508d-235">False</span><span class="sxs-lookup"><span data-stu-id="e508d-235">False</span></span>                                        |
| <span data-ttu-id="e508d-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e508d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e508d-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e508d-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e508d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e508d-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e508d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e508d-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e508d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-240">Search-Flags</span></span>           | <span data-ttu-id="e508d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e508d-241">0x00000000</span></span>                                   |
| <span data-ttu-id="e508d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-242">System-Flags</span></span>           | <span data-ttu-id="e508d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e508d-243">0x00000010</span></span>                                   |
| <span data-ttu-id="e508d-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e508d-244">Classes used in</span></span>        | [<span data-ttu-id="e508d-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="e508d-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e508d-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e508d-246">Windows Server 2012</span></span>



| <span data-ttu-id="e508d-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="e508d-247">Entry</span></span> | <span data-ttu-id="e508d-248">Value</span><span class="sxs-lookup"><span data-stu-id="e508d-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e508d-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e508d-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e508d-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e508d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e508d-251">System-Only</span></span>            | <span data-ttu-id="e508d-252">False</span><span class="sxs-lookup"><span data-stu-id="e508d-252">False</span></span>                                        |
| <span data-ttu-id="e508d-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e508d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e508d-254">True</span><span class="sxs-lookup"><span data-stu-id="e508d-254">True</span></span>                                         |
| <span data-ttu-id="e508d-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e508d-255">Is Indexed</span></span>             | <span data-ttu-id="e508d-256">False</span><span class="sxs-lookup"><span data-stu-id="e508d-256">False</span></span>                                        |
| <span data-ttu-id="e508d-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e508d-257">In Global Catalog</span></span>      | <span data-ttu-id="e508d-258">False</span><span class="sxs-lookup"><span data-stu-id="e508d-258">False</span></span>                                        |
| <span data-ttu-id="e508d-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e508d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e508d-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e508d-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e508d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e508d-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e508d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e508d-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e508d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-263">Search-Flags</span></span>           | <span data-ttu-id="e508d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e508d-264">0x00000000</span></span>                                   |
| <span data-ttu-id="e508d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e508d-265">System-Flags</span></span>           | <span data-ttu-id="e508d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e508d-266">0x00000010</span></span>                                   |
| <span data-ttu-id="e508d-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e508d-267">Classes used in</span></span>        | [<span data-ttu-id="e508d-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="e508d-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






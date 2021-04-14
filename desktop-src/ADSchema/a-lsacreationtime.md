---
title: Atributo de hora de creación de LSA
description: El atributo LSA-Creation-time se usa para admitir la replicación en dominios de Windows NT 4,0.
ms.assetid: a5446cbf-aa35-4ea6-a2e0-9d0ea58edaf1
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de hora de creación de LSA
- lSACreationTime esquema de AD de atributos
topic_type:
- apiref
api_name:
- LSA-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f32092e7d71d02807f4700d381da0ce099ccaf7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422655"
---
# <a name="lsa-creation-time-attribute"></a><span data-ttu-id="9b715-105">Atributo de hora de creación de LSA</span><span class="sxs-lookup"><span data-stu-id="9b715-105">LSA-Creation-Time attribute</span></span>

<span data-ttu-id="9b715-106">El atributo **LSA-Creation-time** se usa para admitir la replicación en dominios de Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="9b715-106">The **LSA-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="9b715-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b715-107">Entry</span></span> | <span data-ttu-id="9b715-108">Value</span><span class="sxs-lookup"><span data-stu-id="9b715-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9b715-109">CN</span><span class="sxs-lookup"><span data-stu-id="9b715-109">CN</span></span>                | <span data-ttu-id="9b715-110">En tiempo de creación de LSA</span><span class="sxs-lookup"><span data-stu-id="9b715-110">LSA-Creation-Time</span></span>                    |
| <span data-ttu-id="9b715-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="9b715-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9b715-112">lSACreationTime</span><span class="sxs-lookup"><span data-stu-id="9b715-112">lSACreationTime</span></span>                      |
| <span data-ttu-id="9b715-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9b715-113">Size</span></span>              | <span data-ttu-id="9b715-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="9b715-114">8 bytes</span></span>                              |
| <span data-ttu-id="9b715-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="9b715-115">Update Privilege</span></span>  | <span data-ttu-id="9b715-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="9b715-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="9b715-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="9b715-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9b715-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9b715-118">Attribute-Id</span></span>      | <span data-ttu-id="9b715-119">1.2.840.113556.1.4.66</span><span class="sxs-lookup"><span data-stu-id="9b715-119">1.2.840.113556.1.4.66</span></span>                |
| <span data-ttu-id="9b715-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9b715-120">System-Id-Guid</span></span>    | <span data-ttu-id="9b715-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9b715-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="9b715-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b715-122">Syntax</span></span>            | [<span data-ttu-id="9b715-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="9b715-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="9b715-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="9b715-124">Implementations</span></span>

-   [<span data-ttu-id="9b715-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9b715-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9b715-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9b715-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9b715-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9b715-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9b715-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9b715-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9b715-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9b715-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9b715-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9b715-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9b715-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9b715-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9b715-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b715-132">Entry</span></span> | <span data-ttu-id="9b715-133">Value</span><span class="sxs-lookup"><span data-stu-id="9b715-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b715-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b715-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b715-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b715-136">System-Only</span></span>            | <span data-ttu-id="9b715-137">False</span><span class="sxs-lookup"><span data-stu-id="9b715-137">False</span></span>                                        |
| <span data-ttu-id="9b715-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b715-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9b715-139">True</span><span class="sxs-lookup"><span data-stu-id="9b715-139">True</span></span>                                         |
| <span data-ttu-id="9b715-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b715-140">Is Indexed</span></span>             | <span data-ttu-id="9b715-141">False</span><span class="sxs-lookup"><span data-stu-id="9b715-141">False</span></span>                                        |
| <span data-ttu-id="9b715-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b715-142">In Global Catalog</span></span>      | <span data-ttu-id="9b715-143">False</span><span class="sxs-lookup"><span data-stu-id="9b715-143">False</span></span>                                        |
| <span data-ttu-id="9b715-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b715-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b715-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b715-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b715-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b715-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b715-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b715-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b715-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-148">Search-Flags</span></span>           | <span data-ttu-id="9b715-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b715-149">0x00000000</span></span>                                   |
| <span data-ttu-id="9b715-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-150">System-Flags</span></span>           | <span data-ttu-id="9b715-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b715-151">0x00000010</span></span>                                   |
| <span data-ttu-id="9b715-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b715-152">Classes used in</span></span>        | [<span data-ttu-id="9b715-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="9b715-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9b715-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b715-154">Windows Server 2003</span></span>



| <span data-ttu-id="9b715-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b715-155">Entry</span></span> | <span data-ttu-id="9b715-156">Value</span><span class="sxs-lookup"><span data-stu-id="9b715-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b715-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b715-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b715-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b715-159">System-Only</span></span>            | <span data-ttu-id="9b715-160">False</span><span class="sxs-lookup"><span data-stu-id="9b715-160">False</span></span>                                        |
| <span data-ttu-id="9b715-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b715-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9b715-162">True</span><span class="sxs-lookup"><span data-stu-id="9b715-162">True</span></span>                                         |
| <span data-ttu-id="9b715-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b715-163">Is Indexed</span></span>             | <span data-ttu-id="9b715-164">False</span><span class="sxs-lookup"><span data-stu-id="9b715-164">False</span></span>                                        |
| <span data-ttu-id="9b715-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b715-165">In Global Catalog</span></span>      | <span data-ttu-id="9b715-166">False</span><span class="sxs-lookup"><span data-stu-id="9b715-166">False</span></span>                                        |
| <span data-ttu-id="9b715-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b715-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b715-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b715-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b715-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b715-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b715-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b715-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b715-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-171">Search-Flags</span></span>           | <span data-ttu-id="9b715-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b715-172">0x00000000</span></span>                                   |
| <span data-ttu-id="9b715-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-173">System-Flags</span></span>           | <span data-ttu-id="9b715-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b715-174">0x00000010</span></span>                                   |
| <span data-ttu-id="9b715-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b715-175">Classes used in</span></span>        | [<span data-ttu-id="9b715-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="9b715-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9b715-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9b715-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9b715-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b715-178">Entry</span></span> | <span data-ttu-id="9b715-179">Value</span><span class="sxs-lookup"><span data-stu-id="9b715-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b715-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b715-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b715-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b715-182">System-Only</span></span>            | <span data-ttu-id="9b715-183">False</span><span class="sxs-lookup"><span data-stu-id="9b715-183">False</span></span>                                        |
| <span data-ttu-id="9b715-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b715-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9b715-185">True</span><span class="sxs-lookup"><span data-stu-id="9b715-185">True</span></span>                                         |
| <span data-ttu-id="9b715-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b715-186">Is Indexed</span></span>             | <span data-ttu-id="9b715-187">False</span><span class="sxs-lookup"><span data-stu-id="9b715-187">False</span></span>                                        |
| <span data-ttu-id="9b715-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b715-188">In Global Catalog</span></span>      | <span data-ttu-id="9b715-189">False</span><span class="sxs-lookup"><span data-stu-id="9b715-189">False</span></span>                                        |
| <span data-ttu-id="9b715-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b715-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b715-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b715-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b715-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b715-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b715-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b715-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b715-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-194">Search-Flags</span></span>           | <span data-ttu-id="9b715-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b715-195">0x00000000</span></span>                                   |
| <span data-ttu-id="9b715-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-196">System-Flags</span></span>           | <span data-ttu-id="9b715-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b715-197">0x00000010</span></span>                                   |
| <span data-ttu-id="9b715-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b715-198">Classes used in</span></span>        | [<span data-ttu-id="9b715-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="9b715-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9b715-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b715-200">Windows Server 2008</span></span>



| <span data-ttu-id="9b715-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b715-201">Entry</span></span> | <span data-ttu-id="9b715-202">Value</span><span class="sxs-lookup"><span data-stu-id="9b715-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b715-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b715-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b715-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b715-205">System-Only</span></span>            | <span data-ttu-id="9b715-206">False</span><span class="sxs-lookup"><span data-stu-id="9b715-206">False</span></span>                                        |
| <span data-ttu-id="9b715-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b715-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9b715-208">True</span><span class="sxs-lookup"><span data-stu-id="9b715-208">True</span></span>                                         |
| <span data-ttu-id="9b715-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b715-209">Is Indexed</span></span>             | <span data-ttu-id="9b715-210">False</span><span class="sxs-lookup"><span data-stu-id="9b715-210">False</span></span>                                        |
| <span data-ttu-id="9b715-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b715-211">In Global Catalog</span></span>      | <span data-ttu-id="9b715-212">False</span><span class="sxs-lookup"><span data-stu-id="9b715-212">False</span></span>                                        |
| <span data-ttu-id="9b715-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b715-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b715-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b715-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b715-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b715-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b715-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b715-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b715-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-217">Search-Flags</span></span>           | <span data-ttu-id="9b715-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b715-218">0x00000000</span></span>                                   |
| <span data-ttu-id="9b715-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-219">System-Flags</span></span>           | <span data-ttu-id="9b715-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b715-220">0x00000010</span></span>                                   |
| <span data-ttu-id="9b715-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b715-221">Classes used in</span></span>        | [<span data-ttu-id="9b715-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="9b715-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9b715-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b715-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9b715-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b715-224">Entry</span></span> | <span data-ttu-id="9b715-225">Value</span><span class="sxs-lookup"><span data-stu-id="9b715-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b715-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b715-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b715-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b715-228">System-Only</span></span>            | <span data-ttu-id="9b715-229">False</span><span class="sxs-lookup"><span data-stu-id="9b715-229">False</span></span>                                        |
| <span data-ttu-id="9b715-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b715-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9b715-231">True</span><span class="sxs-lookup"><span data-stu-id="9b715-231">True</span></span>                                         |
| <span data-ttu-id="9b715-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b715-232">Is Indexed</span></span>             | <span data-ttu-id="9b715-233">False</span><span class="sxs-lookup"><span data-stu-id="9b715-233">False</span></span>                                        |
| <span data-ttu-id="9b715-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b715-234">In Global Catalog</span></span>      | <span data-ttu-id="9b715-235">False</span><span class="sxs-lookup"><span data-stu-id="9b715-235">False</span></span>                                        |
| <span data-ttu-id="9b715-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b715-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b715-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b715-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b715-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b715-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b715-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b715-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b715-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-240">Search-Flags</span></span>           | <span data-ttu-id="9b715-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b715-241">0x00000000</span></span>                                   |
| <span data-ttu-id="9b715-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-242">System-Flags</span></span>           | <span data-ttu-id="9b715-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b715-243">0x00000010</span></span>                                   |
| <span data-ttu-id="9b715-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b715-244">Classes used in</span></span>        | [<span data-ttu-id="9b715-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="9b715-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9b715-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b715-246">Windows Server 2012</span></span>



| <span data-ttu-id="9b715-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b715-247">Entry</span></span> | <span data-ttu-id="9b715-248">Value</span><span class="sxs-lookup"><span data-stu-id="9b715-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9b715-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b715-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b715-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9b715-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b715-251">System-Only</span></span>            | <span data-ttu-id="9b715-252">False</span><span class="sxs-lookup"><span data-stu-id="9b715-252">False</span></span>                                        |
| <span data-ttu-id="9b715-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b715-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9b715-254">True</span><span class="sxs-lookup"><span data-stu-id="9b715-254">True</span></span>                                         |
| <span data-ttu-id="9b715-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b715-255">Is Indexed</span></span>             | <span data-ttu-id="9b715-256">False</span><span class="sxs-lookup"><span data-stu-id="9b715-256">False</span></span>                                        |
| <span data-ttu-id="9b715-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b715-257">In Global Catalog</span></span>      | <span data-ttu-id="9b715-258">False</span><span class="sxs-lookup"><span data-stu-id="9b715-258">False</span></span>                                        |
| <span data-ttu-id="9b715-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b715-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b715-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b715-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9b715-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b715-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9b715-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b715-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9b715-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-263">Search-Flags</span></span>           | <span data-ttu-id="9b715-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b715-264">0x00000000</span></span>                                   |
| <span data-ttu-id="9b715-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b715-265">System-Flags</span></span>           | <span data-ttu-id="9b715-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b715-266">0x00000010</span></span>                                   |
| <span data-ttu-id="9b715-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b715-267">Classes used in</span></span>        | [<span data-ttu-id="9b715-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="9b715-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






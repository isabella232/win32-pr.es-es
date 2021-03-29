---
title: Atributo LSA-Modified-Count
description: El atributo LSA-Modified-Count se usa para admitir la replicación en los dominios de Windows NT 4,0.
ms.assetid: 6af5931c-5d4f-4061-81a1-e8947d760abc
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo LSA-Modified-Count
- lSAModifiedCount esquema de AD de atributos
topic_type:
- apiref
api_name:
- LSA-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042d4d52974457eb1853a3705adb87cc24a7dc3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658926"
---
# <a name="lsa-modified-count-attribute"></a><span data-ttu-id="5f23a-105">Atributo LSA-Modified-Count</span><span class="sxs-lookup"><span data-stu-id="5f23a-105">LSA-Modified-Count attribute</span></span>

<span data-ttu-id="5f23a-106">El atributo **LSA-Modified-Count** se usa para admitir la replicación en los dominios de Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="5f23a-106">The **LSA-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="5f23a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f23a-107">Entry</span></span> | <span data-ttu-id="5f23a-108">Value</span><span class="sxs-lookup"><span data-stu-id="5f23a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5f23a-109">CN</span><span class="sxs-lookup"><span data-stu-id="5f23a-109">CN</span></span>                | <span data-ttu-id="5f23a-110">LSA-modificado-recuento</span><span class="sxs-lookup"><span data-stu-id="5f23a-110">LSA-Modified-Count</span></span>                   |
| <span data-ttu-id="5f23a-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5f23a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5f23a-112">lSAModifiedCount</span><span class="sxs-lookup"><span data-stu-id="5f23a-112">lSAModifiedCount</span></span>                     |
| <span data-ttu-id="5f23a-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5f23a-113">Size</span></span>              | <span data-ttu-id="5f23a-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="5f23a-114">8 bytes</span></span>                              |
| <span data-ttu-id="5f23a-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5f23a-115">Update Privilege</span></span>  | <span data-ttu-id="5f23a-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="5f23a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="5f23a-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5f23a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="5f23a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5f23a-118">Attribute-Id</span></span>      | <span data-ttu-id="5f23a-119">1.2.840.113556.1.4.67</span><span class="sxs-lookup"><span data-stu-id="5f23a-119">1.2.840.113556.1.4.67</span></span>                |
| <span data-ttu-id="5f23a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5f23a-120">System-Id-Guid</span></span>    | <span data-ttu-id="5f23a-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5f23a-121">bf9679ae-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="5f23a-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f23a-122">Syntax</span></span>            | [<span data-ttu-id="5f23a-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="5f23a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="5f23a-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5f23a-124">Implementations</span></span>

-   [<span data-ttu-id="5f23a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5f23a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5f23a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5f23a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5f23a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5f23a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5f23a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5f23a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5f23a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5f23a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5f23a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5f23a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5f23a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f23a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5f23a-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f23a-132">Entry</span></span> | <span data-ttu-id="5f23a-133">Value</span><span class="sxs-lookup"><span data-stu-id="5f23a-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f23a-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f23a-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f23a-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f23a-136">System-Only</span></span>            | <span data-ttu-id="5f23a-137">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-137">False</span></span>                                        |
| <span data-ttu-id="5f23a-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f23a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="5f23a-139">True</span><span class="sxs-lookup"><span data-stu-id="5f23a-139">True</span></span>                                         |
| <span data-ttu-id="5f23a-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f23a-140">Is Indexed</span></span>             | <span data-ttu-id="5f23a-141">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-141">False</span></span>                                        |
| <span data-ttu-id="5f23a-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f23a-142">In Global Catalog</span></span>      | <span data-ttu-id="5f23a-143">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-143">False</span></span>                                        |
| <span data-ttu-id="5f23a-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f23a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f23a-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f23a-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f23a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f23a-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f23a-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-148">Search-Flags</span></span>           | <span data-ttu-id="5f23a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f23a-149">0x00000000</span></span>                                   |
| <span data-ttu-id="5f23a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-150">System-Flags</span></span>           | <span data-ttu-id="5f23a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f23a-151">0x00000010</span></span>                                   |
| <span data-ttu-id="5f23a-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f23a-152">Classes used in</span></span>        | [<span data-ttu-id="5f23a-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="5f23a-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5f23a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f23a-154">Windows Server 2003</span></span>



| <span data-ttu-id="5f23a-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f23a-155">Entry</span></span> | <span data-ttu-id="5f23a-156">Value</span><span class="sxs-lookup"><span data-stu-id="5f23a-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f23a-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f23a-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f23a-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f23a-159">System-Only</span></span>            | <span data-ttu-id="5f23a-160">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-160">False</span></span>                                        |
| <span data-ttu-id="5f23a-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f23a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5f23a-162">True</span><span class="sxs-lookup"><span data-stu-id="5f23a-162">True</span></span>                                         |
| <span data-ttu-id="5f23a-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f23a-163">Is Indexed</span></span>             | <span data-ttu-id="5f23a-164">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-164">False</span></span>                                        |
| <span data-ttu-id="5f23a-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f23a-165">In Global Catalog</span></span>      | <span data-ttu-id="5f23a-166">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-166">False</span></span>                                        |
| <span data-ttu-id="5f23a-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f23a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f23a-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f23a-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f23a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f23a-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f23a-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-171">Search-Flags</span></span>           | <span data-ttu-id="5f23a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f23a-172">0x00000000</span></span>                                   |
| <span data-ttu-id="5f23a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-173">System-Flags</span></span>           | <span data-ttu-id="5f23a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f23a-174">0x00000010</span></span>                                   |
| <span data-ttu-id="5f23a-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f23a-175">Classes used in</span></span>        | [<span data-ttu-id="5f23a-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="5f23a-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5f23a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5f23a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5f23a-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f23a-178">Entry</span></span> | <span data-ttu-id="5f23a-179">Value</span><span class="sxs-lookup"><span data-stu-id="5f23a-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f23a-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f23a-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f23a-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f23a-182">System-Only</span></span>            | <span data-ttu-id="5f23a-183">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-183">False</span></span>                                        |
| <span data-ttu-id="5f23a-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f23a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="5f23a-185">True</span><span class="sxs-lookup"><span data-stu-id="5f23a-185">True</span></span>                                         |
| <span data-ttu-id="5f23a-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f23a-186">Is Indexed</span></span>             | <span data-ttu-id="5f23a-187">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-187">False</span></span>                                        |
| <span data-ttu-id="5f23a-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f23a-188">In Global Catalog</span></span>      | <span data-ttu-id="5f23a-189">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-189">False</span></span>                                        |
| <span data-ttu-id="5f23a-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f23a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f23a-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f23a-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f23a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f23a-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f23a-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-194">Search-Flags</span></span>           | <span data-ttu-id="5f23a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f23a-195">0x00000000</span></span>                                   |
| <span data-ttu-id="5f23a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-196">System-Flags</span></span>           | <span data-ttu-id="5f23a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f23a-197">0x00000010</span></span>                                   |
| <span data-ttu-id="5f23a-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f23a-198">Classes used in</span></span>        | [<span data-ttu-id="5f23a-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="5f23a-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5f23a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f23a-200">Windows Server 2008</span></span>



| <span data-ttu-id="5f23a-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f23a-201">Entry</span></span> | <span data-ttu-id="5f23a-202">Value</span><span class="sxs-lookup"><span data-stu-id="5f23a-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f23a-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f23a-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f23a-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f23a-205">System-Only</span></span>            | <span data-ttu-id="5f23a-206">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-206">False</span></span>                                        |
| <span data-ttu-id="5f23a-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f23a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="5f23a-208">True</span><span class="sxs-lookup"><span data-stu-id="5f23a-208">True</span></span>                                         |
| <span data-ttu-id="5f23a-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f23a-209">Is Indexed</span></span>             | <span data-ttu-id="5f23a-210">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-210">False</span></span>                                        |
| <span data-ttu-id="5f23a-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f23a-211">In Global Catalog</span></span>      | <span data-ttu-id="5f23a-212">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-212">False</span></span>                                        |
| <span data-ttu-id="5f23a-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f23a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f23a-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f23a-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f23a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f23a-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f23a-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-217">Search-Flags</span></span>           | <span data-ttu-id="5f23a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f23a-218">0x00000000</span></span>                                   |
| <span data-ttu-id="5f23a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-219">System-Flags</span></span>           | <span data-ttu-id="5f23a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f23a-220">0x00000010</span></span>                                   |
| <span data-ttu-id="5f23a-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f23a-221">Classes used in</span></span>        | [<span data-ttu-id="5f23a-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="5f23a-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5f23a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f23a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5f23a-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f23a-224">Entry</span></span> | <span data-ttu-id="5f23a-225">Value</span><span class="sxs-lookup"><span data-stu-id="5f23a-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f23a-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f23a-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f23a-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f23a-228">System-Only</span></span>            | <span data-ttu-id="5f23a-229">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-229">False</span></span>                                        |
| <span data-ttu-id="5f23a-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f23a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="5f23a-231">True</span><span class="sxs-lookup"><span data-stu-id="5f23a-231">True</span></span>                                         |
| <span data-ttu-id="5f23a-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f23a-232">Is Indexed</span></span>             | <span data-ttu-id="5f23a-233">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-233">False</span></span>                                        |
| <span data-ttu-id="5f23a-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f23a-234">In Global Catalog</span></span>      | <span data-ttu-id="5f23a-235">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-235">False</span></span>                                        |
| <span data-ttu-id="5f23a-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f23a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f23a-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f23a-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f23a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f23a-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f23a-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-240">Search-Flags</span></span>           | <span data-ttu-id="5f23a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f23a-241">0x00000000</span></span>                                   |
| <span data-ttu-id="5f23a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-242">System-Flags</span></span>           | <span data-ttu-id="5f23a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f23a-243">0x00000010</span></span>                                   |
| <span data-ttu-id="5f23a-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f23a-244">Classes used in</span></span>        | [<span data-ttu-id="5f23a-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="5f23a-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5f23a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f23a-246">Windows Server 2012</span></span>



| <span data-ttu-id="5f23a-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f23a-247">Entry</span></span> | <span data-ttu-id="5f23a-248">Value</span><span class="sxs-lookup"><span data-stu-id="5f23a-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="5f23a-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f23a-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f23a-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="5f23a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f23a-251">System-Only</span></span>            | <span data-ttu-id="5f23a-252">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-252">False</span></span>                                        |
| <span data-ttu-id="5f23a-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f23a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="5f23a-254">True</span><span class="sxs-lookup"><span data-stu-id="5f23a-254">True</span></span>                                         |
| <span data-ttu-id="5f23a-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f23a-255">Is Indexed</span></span>             | <span data-ttu-id="5f23a-256">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-256">False</span></span>                                        |
| <span data-ttu-id="5f23a-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f23a-257">In Global Catalog</span></span>      | <span data-ttu-id="5f23a-258">False</span><span class="sxs-lookup"><span data-stu-id="5f23a-258">False</span></span>                                        |
| <span data-ttu-id="5f23a-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f23a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f23a-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f23a-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="5f23a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f23a-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f23a-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="5f23a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-263">Search-Flags</span></span>           | <span data-ttu-id="5f23a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f23a-264">0x00000000</span></span>                                   |
| <span data-ttu-id="5f23a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f23a-265">System-Flags</span></span>           | <span data-ttu-id="5f23a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f23a-266">0x00000010</span></span>                                   |
| <span data-ttu-id="5f23a-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f23a-267">Classes used in</span></span>        | [<span data-ttu-id="5f23a-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="5f23a-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






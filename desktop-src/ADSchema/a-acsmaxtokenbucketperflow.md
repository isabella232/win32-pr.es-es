---
title: Atributo ACS-Max-token-bucket-por flujo
description: El atributo ACS-Max-token-bucket-por flujo solo es para uso interno.
ms.assetid: 2c269bda-7b0d-4ef4-8c67-9f5e7c52e3ae
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo ACS-Max-token-bucket-por flujo
- aCSMaxTokenBucketPerFlow esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-Max-Token-Bucket-Per-Flow
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb323af82b270c20478e8af4aafc3ee4142125ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151901"
---
# <a name="acs-max-token-bucket-per-flow-attribute"></a><span data-ttu-id="e7c07-105">Atributo ACS-Max-token-bucket-por flujo</span><span class="sxs-lookup"><span data-stu-id="e7c07-105">ACS-Max-Token-Bucket-Per-Flow attribute</span></span>

<span data-ttu-id="e7c07-106">El atributo **ACS-Max-token-bucket-por flujo** solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="e7c07-106">The **ACS-Max-Token-Bucket-Per-Flow** attribute is for internal use only.</span></span> <span data-ttu-id="e7c07-107">Basado en RFC2210.</span><span class="sxs-lookup"><span data-stu-id="e7c07-107">Based on RFC2210.</span></span>



| <span data-ttu-id="e7c07-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c07-108">Entry</span></span> | <span data-ttu-id="e7c07-109">Value</span><span class="sxs-lookup"><span data-stu-id="e7c07-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e7c07-110">CN</span><span class="sxs-lookup"><span data-stu-id="e7c07-110">CN</span></span>                | <span data-ttu-id="e7c07-111">ACS-Max-token-bucket-por flujo</span><span class="sxs-lookup"><span data-stu-id="e7c07-111">ACS-Max-Token-Bucket-Per-Flow</span></span>        |
| <span data-ttu-id="e7c07-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="e7c07-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e7c07-113">aCSMaxTokenBucketPerFlow</span><span class="sxs-lookup"><span data-stu-id="e7c07-113">aCSMaxTokenBucketPerFlow</span></span>             |
| <span data-ttu-id="e7c07-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e7c07-114">Size</span></span>              | <span data-ttu-id="e7c07-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="e7c07-115">8 bytes</span></span>                              |
| <span data-ttu-id="e7c07-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="e7c07-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e7c07-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="e7c07-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e7c07-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e7c07-118">Attribute-Id</span></span>      | <span data-ttu-id="e7c07-119">1.2.840.113556.1.4.1313</span><span class="sxs-lookup"><span data-stu-id="e7c07-119">1.2.840.113556.1.4.1313</span></span>              |
| <span data-ttu-id="e7c07-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e7c07-120">System-Id-Guid</span></span>    | <span data-ttu-id="e7c07-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="e7c07-121">81f6e0df-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="e7c07-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7c07-122">Syntax</span></span>            | [<span data-ttu-id="e7c07-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="e7c07-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="e7c07-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="e7c07-124">Implementations</span></span>

-   [<span data-ttu-id="e7c07-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e7c07-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e7c07-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e7c07-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e7c07-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e7c07-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e7c07-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e7c07-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e7c07-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e7c07-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e7c07-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e7c07-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e7c07-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7c07-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e7c07-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c07-132">Entry</span></span> | <span data-ttu-id="e7c07-133">Value</span><span class="sxs-lookup"><span data-stu-id="e7c07-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7c07-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e7c07-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7c07-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7c07-136">System-Only</span></span>            | <span data-ttu-id="e7c07-137">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-137">False</span></span>                                        |
| <span data-ttu-id="e7c07-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e7c07-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e7c07-139">True</span><span class="sxs-lookup"><span data-stu-id="e7c07-139">True</span></span>                                         |
| <span data-ttu-id="e7c07-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e7c07-140">Is Indexed</span></span>             | <span data-ttu-id="e7c07-141">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-141">False</span></span>                                        |
| <span data-ttu-id="e7c07-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e7c07-142">In Global Catalog</span></span>      | <span data-ttu-id="e7c07-143">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-143">False</span></span>                                        |
| <span data-ttu-id="e7c07-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e7c07-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7c07-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7c07-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7c07-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7c07-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7c07-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-148">Search-Flags</span></span>           | <span data-ttu-id="e7c07-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7c07-149">0x00000000</span></span>                                   |
| <span data-ttu-id="e7c07-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-150">System-Flags</span></span>           | <span data-ttu-id="e7c07-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7c07-151">0x00000010</span></span>                                   |
| <span data-ttu-id="e7c07-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e7c07-152">Classes used in</span></span>        | [<span data-ttu-id="e7c07-153">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="e7c07-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e7c07-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7c07-154">Windows Server 2003</span></span>



| <span data-ttu-id="e7c07-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c07-155">Entry</span></span> | <span data-ttu-id="e7c07-156">Value</span><span class="sxs-lookup"><span data-stu-id="e7c07-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7c07-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e7c07-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7c07-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7c07-159">System-Only</span></span>            | <span data-ttu-id="e7c07-160">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-160">False</span></span>                                        |
| <span data-ttu-id="e7c07-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e7c07-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e7c07-162">True</span><span class="sxs-lookup"><span data-stu-id="e7c07-162">True</span></span>                                         |
| <span data-ttu-id="e7c07-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e7c07-163">Is Indexed</span></span>             | <span data-ttu-id="e7c07-164">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-164">False</span></span>                                        |
| <span data-ttu-id="e7c07-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e7c07-165">In Global Catalog</span></span>      | <span data-ttu-id="e7c07-166">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-166">False</span></span>                                        |
| <span data-ttu-id="e7c07-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e7c07-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7c07-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7c07-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7c07-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7c07-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7c07-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-171">Search-Flags</span></span>           | <span data-ttu-id="e7c07-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7c07-172">0x00000000</span></span>                                   |
| <span data-ttu-id="e7c07-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-173">System-Flags</span></span>           | <span data-ttu-id="e7c07-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7c07-174">0x00000010</span></span>                                   |
| <span data-ttu-id="e7c07-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e7c07-175">Classes used in</span></span>        | [<span data-ttu-id="e7c07-176">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="e7c07-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e7c07-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e7c07-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e7c07-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c07-178">Entry</span></span> | <span data-ttu-id="e7c07-179">Value</span><span class="sxs-lookup"><span data-stu-id="e7c07-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7c07-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e7c07-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7c07-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7c07-182">System-Only</span></span>            | <span data-ttu-id="e7c07-183">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-183">False</span></span>                                        |
| <span data-ttu-id="e7c07-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e7c07-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e7c07-185">True</span><span class="sxs-lookup"><span data-stu-id="e7c07-185">True</span></span>                                         |
| <span data-ttu-id="e7c07-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e7c07-186">Is Indexed</span></span>             | <span data-ttu-id="e7c07-187">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-187">False</span></span>                                        |
| <span data-ttu-id="e7c07-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e7c07-188">In Global Catalog</span></span>      | <span data-ttu-id="e7c07-189">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-189">False</span></span>                                        |
| <span data-ttu-id="e7c07-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e7c07-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7c07-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7c07-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7c07-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7c07-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7c07-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-194">Search-Flags</span></span>           | <span data-ttu-id="e7c07-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7c07-195">0x00000000</span></span>                                   |
| <span data-ttu-id="e7c07-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-196">System-Flags</span></span>           | <span data-ttu-id="e7c07-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7c07-197">0x00000010</span></span>                                   |
| <span data-ttu-id="e7c07-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e7c07-198">Classes used in</span></span>        | [<span data-ttu-id="e7c07-199">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="e7c07-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e7c07-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7c07-200">Windows Server 2008</span></span>



| <span data-ttu-id="e7c07-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c07-201">Entry</span></span> | <span data-ttu-id="e7c07-202">Value</span><span class="sxs-lookup"><span data-stu-id="e7c07-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7c07-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e7c07-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7c07-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7c07-205">System-Only</span></span>            | <span data-ttu-id="e7c07-206">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-206">False</span></span>                                        |
| <span data-ttu-id="e7c07-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e7c07-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e7c07-208">True</span><span class="sxs-lookup"><span data-stu-id="e7c07-208">True</span></span>                                         |
| <span data-ttu-id="e7c07-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e7c07-209">Is Indexed</span></span>             | <span data-ttu-id="e7c07-210">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-210">False</span></span>                                        |
| <span data-ttu-id="e7c07-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e7c07-211">In Global Catalog</span></span>      | <span data-ttu-id="e7c07-212">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-212">False</span></span>                                        |
| <span data-ttu-id="e7c07-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e7c07-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7c07-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7c07-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7c07-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7c07-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7c07-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-217">Search-Flags</span></span>           | <span data-ttu-id="e7c07-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7c07-218">0x00000000</span></span>                                   |
| <span data-ttu-id="e7c07-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-219">System-Flags</span></span>           | <span data-ttu-id="e7c07-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7c07-220">0x00000010</span></span>                                   |
| <span data-ttu-id="e7c07-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e7c07-221">Classes used in</span></span>        | [<span data-ttu-id="e7c07-222">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="e7c07-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e7c07-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7c07-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e7c07-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c07-224">Entry</span></span> | <span data-ttu-id="e7c07-225">Value</span><span class="sxs-lookup"><span data-stu-id="e7c07-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7c07-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e7c07-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7c07-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7c07-228">System-Only</span></span>            | <span data-ttu-id="e7c07-229">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-229">False</span></span>                                        |
| <span data-ttu-id="e7c07-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e7c07-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e7c07-231">True</span><span class="sxs-lookup"><span data-stu-id="e7c07-231">True</span></span>                                         |
| <span data-ttu-id="e7c07-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e7c07-232">Is Indexed</span></span>             | <span data-ttu-id="e7c07-233">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-233">False</span></span>                                        |
| <span data-ttu-id="e7c07-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e7c07-234">In Global Catalog</span></span>      | <span data-ttu-id="e7c07-235">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-235">False</span></span>                                        |
| <span data-ttu-id="e7c07-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e7c07-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7c07-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7c07-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7c07-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7c07-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7c07-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-240">Search-Flags</span></span>           | <span data-ttu-id="e7c07-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7c07-241">0x00000000</span></span>                                   |
| <span data-ttu-id="e7c07-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-242">System-Flags</span></span>           | <span data-ttu-id="e7c07-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7c07-243">0x00000010</span></span>                                   |
| <span data-ttu-id="e7c07-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e7c07-244">Classes used in</span></span>        | [<span data-ttu-id="e7c07-245">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="e7c07-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e7c07-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7c07-246">Windows Server 2012</span></span>



| <span data-ttu-id="e7c07-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="e7c07-247">Entry</span></span> | <span data-ttu-id="e7c07-248">Value</span><span class="sxs-lookup"><span data-stu-id="e7c07-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e7c07-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="e7c07-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7c07-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e7c07-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7c07-251">System-Only</span></span>            | <span data-ttu-id="e7c07-252">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-252">False</span></span>                                        |
| <span data-ttu-id="e7c07-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="e7c07-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e7c07-254">True</span><span class="sxs-lookup"><span data-stu-id="e7c07-254">True</span></span>                                         |
| <span data-ttu-id="e7c07-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="e7c07-255">Is Indexed</span></span>             | <span data-ttu-id="e7c07-256">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-256">False</span></span>                                        |
| <span data-ttu-id="e7c07-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="e7c07-257">In Global Catalog</span></span>      | <span data-ttu-id="e7c07-258">False</span><span class="sxs-lookup"><span data-stu-id="e7c07-258">False</span></span>                                        |
| <span data-ttu-id="e7c07-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="e7c07-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7c07-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7c07-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e7c07-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7c07-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7c07-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e7c07-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-263">Search-Flags</span></span>           | <span data-ttu-id="e7c07-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7c07-264">0x00000000</span></span>                                   |
| <span data-ttu-id="e7c07-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7c07-265">System-Flags</span></span>           | <span data-ttu-id="e7c07-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e7c07-266">0x00000010</span></span>                                   |
| <span data-ttu-id="e7c07-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="e7c07-267">Classes used in</span></span>        | [<span data-ttu-id="e7c07-268">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="e7c07-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






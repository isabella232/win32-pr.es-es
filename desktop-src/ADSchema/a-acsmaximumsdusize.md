---
title: Atributo ACS-Maximum-SDU-size
description: El atributo ACS-Maximum-SDU-size solo es para uso interno.
ms.assetid: 60dc8b92-888f-4eaf-8c7a-70d1ee12b490
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos ACS-Maximum-SDU-size
- aCSMaximumSDUSize esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-Maximum-SDU-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9fa6260b3e0370f8a3d6e0ddfdab206d41db02
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804466"
---
# <a name="acs-maximum-sdu-size-attribute"></a><span data-ttu-id="32a22-105">Atributo ACS-Maximum-SDU-size</span><span class="sxs-lookup"><span data-stu-id="32a22-105">ACS-Maximum-SDU-Size attribute</span></span>

<span data-ttu-id="32a22-106">El atributo **ACS-Maximum-SDU-size** solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="32a22-106">The **ACS-Maximum-SDU-Size** attribute is for internal use only.</span></span> <span data-ttu-id="32a22-107">Basado en RFC2210.</span><span class="sxs-lookup"><span data-stu-id="32a22-107">Based on RFC2210.</span></span>



| <span data-ttu-id="32a22-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="32a22-108">Entry</span></span> | <span data-ttu-id="32a22-109">Value</span><span class="sxs-lookup"><span data-stu-id="32a22-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="32a22-110">CN</span><span class="sxs-lookup"><span data-stu-id="32a22-110">CN</span></span>                | <span data-ttu-id="32a22-111">ACS-Maximum-SDU-size</span><span class="sxs-lookup"><span data-stu-id="32a22-111">ACS-Maximum-SDU-Size</span></span>                 |
| <span data-ttu-id="32a22-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="32a22-112">Ldap-Display-Name</span></span> | <span data-ttu-id="32a22-113">aCSMaximumSDUSize</span><span class="sxs-lookup"><span data-stu-id="32a22-113">aCSMaximumSDUSize</span></span>                    |
| <span data-ttu-id="32a22-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="32a22-114">Size</span></span>              | <span data-ttu-id="32a22-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="32a22-115">8 bytes</span></span>                              |
| <span data-ttu-id="32a22-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="32a22-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="32a22-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="32a22-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="32a22-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="32a22-118">Attribute-Id</span></span>      | <span data-ttu-id="32a22-119">1.2.840.113556.1.4.1314</span><span class="sxs-lookup"><span data-stu-id="32a22-119">1.2.840.113556.1.4.1314</span></span>              |
| <span data-ttu-id="32a22-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="32a22-120">System-Id-Guid</span></span>    | <span data-ttu-id="32a22-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="32a22-121">87a2d8f9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="32a22-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32a22-122">Syntax</span></span>            | [<span data-ttu-id="32a22-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="32a22-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="32a22-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="32a22-124">Implementations</span></span>

-   [<span data-ttu-id="32a22-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="32a22-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="32a22-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="32a22-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="32a22-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="32a22-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="32a22-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="32a22-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="32a22-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="32a22-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="32a22-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="32a22-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="32a22-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32a22-131">Windows 2000 Server</span></span>



| <span data-ttu-id="32a22-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="32a22-132">Entry</span></span> | <span data-ttu-id="32a22-133">Value</span><span class="sxs-lookup"><span data-stu-id="32a22-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="32a22-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="32a22-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a22-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a22-136">System-Only</span></span>            | <span data-ttu-id="32a22-137">False</span><span class="sxs-lookup"><span data-stu-id="32a22-137">False</span></span>                                        |
| <span data-ttu-id="32a22-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="32a22-138">Is-Single-Valued</span></span>       | <span data-ttu-id="32a22-139">True</span><span class="sxs-lookup"><span data-stu-id="32a22-139">True</span></span>                                         |
| <span data-ttu-id="32a22-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="32a22-140">Is Indexed</span></span>             | <span data-ttu-id="32a22-141">False</span><span class="sxs-lookup"><span data-stu-id="32a22-141">False</span></span>                                        |
| <span data-ttu-id="32a22-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="32a22-142">In Global Catalog</span></span>      | <span data-ttu-id="32a22-143">False</span><span class="sxs-lookup"><span data-stu-id="32a22-143">False</span></span>                                        |
| <span data-ttu-id="32a22-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="32a22-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a22-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="32a22-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="32a22-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a22-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="32a22-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a22-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="32a22-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-148">Search-Flags</span></span>           | <span data-ttu-id="32a22-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a22-149">0x00000000</span></span>                                   |
| <span data-ttu-id="32a22-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-150">System-Flags</span></span>           | <span data-ttu-id="32a22-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a22-151">0x00000010</span></span>                                   |
| <span data-ttu-id="32a22-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="32a22-152">Classes used in</span></span>        | [<span data-ttu-id="32a22-153">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="32a22-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="32a22-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32a22-154">Windows Server 2003</span></span>



| <span data-ttu-id="32a22-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="32a22-155">Entry</span></span> | <span data-ttu-id="32a22-156">Value</span><span class="sxs-lookup"><span data-stu-id="32a22-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="32a22-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="32a22-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a22-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a22-159">System-Only</span></span>            | <span data-ttu-id="32a22-160">False</span><span class="sxs-lookup"><span data-stu-id="32a22-160">False</span></span>                                        |
| <span data-ttu-id="32a22-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="32a22-161">Is-Single-Valued</span></span>       | <span data-ttu-id="32a22-162">True</span><span class="sxs-lookup"><span data-stu-id="32a22-162">True</span></span>                                         |
| <span data-ttu-id="32a22-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="32a22-163">Is Indexed</span></span>             | <span data-ttu-id="32a22-164">False</span><span class="sxs-lookup"><span data-stu-id="32a22-164">False</span></span>                                        |
| <span data-ttu-id="32a22-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="32a22-165">In Global Catalog</span></span>      | <span data-ttu-id="32a22-166">False</span><span class="sxs-lookup"><span data-stu-id="32a22-166">False</span></span>                                        |
| <span data-ttu-id="32a22-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="32a22-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a22-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="32a22-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="32a22-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a22-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="32a22-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a22-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="32a22-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-171">Search-Flags</span></span>           | <span data-ttu-id="32a22-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a22-172">0x00000000</span></span>                                   |
| <span data-ttu-id="32a22-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-173">System-Flags</span></span>           | <span data-ttu-id="32a22-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a22-174">0x00000010</span></span>                                   |
| <span data-ttu-id="32a22-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="32a22-175">Classes used in</span></span>        | [<span data-ttu-id="32a22-176">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="32a22-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="32a22-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="32a22-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="32a22-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="32a22-178">Entry</span></span> | <span data-ttu-id="32a22-179">Value</span><span class="sxs-lookup"><span data-stu-id="32a22-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="32a22-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="32a22-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a22-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a22-182">System-Only</span></span>            | <span data-ttu-id="32a22-183">False</span><span class="sxs-lookup"><span data-stu-id="32a22-183">False</span></span>                                        |
| <span data-ttu-id="32a22-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="32a22-184">Is-Single-Valued</span></span>       | <span data-ttu-id="32a22-185">True</span><span class="sxs-lookup"><span data-stu-id="32a22-185">True</span></span>                                         |
| <span data-ttu-id="32a22-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="32a22-186">Is Indexed</span></span>             | <span data-ttu-id="32a22-187">False</span><span class="sxs-lookup"><span data-stu-id="32a22-187">False</span></span>                                        |
| <span data-ttu-id="32a22-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="32a22-188">In Global Catalog</span></span>      | <span data-ttu-id="32a22-189">False</span><span class="sxs-lookup"><span data-stu-id="32a22-189">False</span></span>                                        |
| <span data-ttu-id="32a22-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="32a22-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a22-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="32a22-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="32a22-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a22-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="32a22-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a22-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="32a22-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-194">Search-Flags</span></span>           | <span data-ttu-id="32a22-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a22-195">0x00000000</span></span>                                   |
| <span data-ttu-id="32a22-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-196">System-Flags</span></span>           | <span data-ttu-id="32a22-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a22-197">0x00000010</span></span>                                   |
| <span data-ttu-id="32a22-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="32a22-198">Classes used in</span></span>        | [<span data-ttu-id="32a22-199">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="32a22-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="32a22-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32a22-200">Windows Server 2008</span></span>



| <span data-ttu-id="32a22-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="32a22-201">Entry</span></span> | <span data-ttu-id="32a22-202">Value</span><span class="sxs-lookup"><span data-stu-id="32a22-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="32a22-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="32a22-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a22-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a22-205">System-Only</span></span>            | <span data-ttu-id="32a22-206">False</span><span class="sxs-lookup"><span data-stu-id="32a22-206">False</span></span>                                        |
| <span data-ttu-id="32a22-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="32a22-207">Is-Single-Valued</span></span>       | <span data-ttu-id="32a22-208">True</span><span class="sxs-lookup"><span data-stu-id="32a22-208">True</span></span>                                         |
| <span data-ttu-id="32a22-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="32a22-209">Is Indexed</span></span>             | <span data-ttu-id="32a22-210">False</span><span class="sxs-lookup"><span data-stu-id="32a22-210">False</span></span>                                        |
| <span data-ttu-id="32a22-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="32a22-211">In Global Catalog</span></span>      | <span data-ttu-id="32a22-212">False</span><span class="sxs-lookup"><span data-stu-id="32a22-212">False</span></span>                                        |
| <span data-ttu-id="32a22-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="32a22-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a22-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="32a22-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="32a22-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a22-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="32a22-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a22-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="32a22-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-217">Search-Flags</span></span>           | <span data-ttu-id="32a22-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a22-218">0x00000000</span></span>                                   |
| <span data-ttu-id="32a22-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-219">System-Flags</span></span>           | <span data-ttu-id="32a22-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a22-220">0x00000010</span></span>                                   |
| <span data-ttu-id="32a22-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="32a22-221">Classes used in</span></span>        | [<span data-ttu-id="32a22-222">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="32a22-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="32a22-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32a22-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="32a22-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="32a22-224">Entry</span></span> | <span data-ttu-id="32a22-225">Value</span><span class="sxs-lookup"><span data-stu-id="32a22-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="32a22-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="32a22-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a22-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a22-228">System-Only</span></span>            | <span data-ttu-id="32a22-229">False</span><span class="sxs-lookup"><span data-stu-id="32a22-229">False</span></span>                                        |
| <span data-ttu-id="32a22-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="32a22-230">Is-Single-Valued</span></span>       | <span data-ttu-id="32a22-231">True</span><span class="sxs-lookup"><span data-stu-id="32a22-231">True</span></span>                                         |
| <span data-ttu-id="32a22-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="32a22-232">Is Indexed</span></span>             | <span data-ttu-id="32a22-233">False</span><span class="sxs-lookup"><span data-stu-id="32a22-233">False</span></span>                                        |
| <span data-ttu-id="32a22-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="32a22-234">In Global Catalog</span></span>      | <span data-ttu-id="32a22-235">False</span><span class="sxs-lookup"><span data-stu-id="32a22-235">False</span></span>                                        |
| <span data-ttu-id="32a22-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="32a22-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a22-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="32a22-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="32a22-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a22-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="32a22-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a22-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="32a22-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-240">Search-Flags</span></span>           | <span data-ttu-id="32a22-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a22-241">0x00000000</span></span>                                   |
| <span data-ttu-id="32a22-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-242">System-Flags</span></span>           | <span data-ttu-id="32a22-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a22-243">0x00000010</span></span>                                   |
| <span data-ttu-id="32a22-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="32a22-244">Classes used in</span></span>        | [<span data-ttu-id="32a22-245">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="32a22-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="32a22-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32a22-246">Windows Server 2012</span></span>



| <span data-ttu-id="32a22-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="32a22-247">Entry</span></span> | <span data-ttu-id="32a22-248">Value</span><span class="sxs-lookup"><span data-stu-id="32a22-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="32a22-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="32a22-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32a22-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="32a22-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="32a22-251">System-Only</span></span>            | <span data-ttu-id="32a22-252">False</span><span class="sxs-lookup"><span data-stu-id="32a22-252">False</span></span>                                        |
| <span data-ttu-id="32a22-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="32a22-253">Is-Single-Valued</span></span>       | <span data-ttu-id="32a22-254">True</span><span class="sxs-lookup"><span data-stu-id="32a22-254">True</span></span>                                         |
| <span data-ttu-id="32a22-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="32a22-255">Is Indexed</span></span>             | <span data-ttu-id="32a22-256">False</span><span class="sxs-lookup"><span data-stu-id="32a22-256">False</span></span>                                        |
| <span data-ttu-id="32a22-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="32a22-257">In Global Catalog</span></span>      | <span data-ttu-id="32a22-258">False</span><span class="sxs-lookup"><span data-stu-id="32a22-258">False</span></span>                                        |
| <span data-ttu-id="32a22-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="32a22-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="32a22-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="32a22-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="32a22-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32a22-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="32a22-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32a22-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="32a22-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-263">Search-Flags</span></span>           | <span data-ttu-id="32a22-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32a22-264">0x00000000</span></span>                                   |
| <span data-ttu-id="32a22-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32a22-265">System-Flags</span></span>           | <span data-ttu-id="32a22-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32a22-266">0x00000010</span></span>                                   |
| <span data-ttu-id="32a22-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="32a22-267">Classes used in</span></span>        | [<span data-ttu-id="32a22-268">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="32a22-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






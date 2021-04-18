---
title: ACS-atributo de tamaño mínimo de directivas
description: El atributo ACS-Minimum-Policialed-size solo es para uso interno.
ms.assetid: 27b4273a-a625-430b-baa0-a6037e2aac1e
ms.tgt_platform: multiple
keywords:
- 'ACS: esquema de AD de atributo de tamaño mínimo de directivas'
- aCSMinimumPolicedSize esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-Minimum-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3de4bb2b33a45ab7d10bad72ba286d1695b980a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659239"
---
# <a name="acs-minimum-policed-size-attribute"></a><span data-ttu-id="a0a8c-105">ACS-atributo de tamaño mínimo de directivas</span><span class="sxs-lookup"><span data-stu-id="a0a8c-105">ACS-Minimum-Policed-Size attribute</span></span>

<span data-ttu-id="a0a8c-106">El atributo **ACS-Minimum-policialed-size** solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="a0a8c-106">The **ACS-Minimum-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="a0a8c-107">Basado en RFC2210.</span><span class="sxs-lookup"><span data-stu-id="a0a8c-107">Based on RFC2210.</span></span>



| <span data-ttu-id="a0a8c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0a8c-108">Entry</span></span> | <span data-ttu-id="a0a8c-109">Value</span><span class="sxs-lookup"><span data-stu-id="a0a8c-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a0a8c-110">CN</span><span class="sxs-lookup"><span data-stu-id="a0a8c-110">CN</span></span>                | <span data-ttu-id="a0a8c-111">ACS: tamaño mínimo de directivas</span><span class="sxs-lookup"><span data-stu-id="a0a8c-111">ACS-Minimum-Policed-Size</span></span>             |
| <span data-ttu-id="a0a8c-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a0a8c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a0a8c-113">aCSMinimumPolicedSize</span><span class="sxs-lookup"><span data-stu-id="a0a8c-113">aCSMinimumPolicedSize</span></span>                |
| <span data-ttu-id="a0a8c-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a0a8c-114">Size</span></span>              | <span data-ttu-id="a0a8c-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="a0a8c-115">8 bytes</span></span>                              |
| <span data-ttu-id="a0a8c-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a0a8c-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a0a8c-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a0a8c-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a0a8c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a0a8c-118">Attribute-Id</span></span>      | <span data-ttu-id="a0a8c-119">1.2.840.113556.1.4.1315</span><span class="sxs-lookup"><span data-stu-id="a0a8c-119">1.2.840.113556.1.4.1315</span></span>              |
| <span data-ttu-id="a0a8c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a0a8c-120">System-Id-Guid</span></span>    | <span data-ttu-id="a0a8c-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="a0a8c-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="a0a8c-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0a8c-122">Syntax</span></span>            | [<span data-ttu-id="a0a8c-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="a0a8c-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a0a8c-124">Implementations</span></span>

-   [<span data-ttu-id="a0a8c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a0a8c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a0a8c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a0a8c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a0a8c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a0a8c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a0a8c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0a8c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a0a8c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0a8c-132">Entry</span></span> | <span data-ttu-id="a0a8c-133">Value</span><span class="sxs-lookup"><span data-stu-id="a0a8c-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a0a8c-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a0a8c-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a8c-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a8c-136">System-Only</span></span>            | <span data-ttu-id="a0a8c-137">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-137">False</span></span>                                        |
| <span data-ttu-id="a0a8c-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a0a8c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a8c-139">True</span><span class="sxs-lookup"><span data-stu-id="a0a8c-139">True</span></span>                                         |
| <span data-ttu-id="a0a8c-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a0a8c-140">Is Indexed</span></span>             | <span data-ttu-id="a0a8c-141">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-141">False</span></span>                                        |
| <span data-ttu-id="a0a8c-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a0a8c-142">In Global Catalog</span></span>      | <span data-ttu-id="a0a8c-143">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-143">False</span></span>                                        |
| <span data-ttu-id="a0a8c-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a0a8c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a8c-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0a8c-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a0a8c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a8c-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a8c-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-148">Search-Flags</span></span>           | <span data-ttu-id="a0a8c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a8c-149">0x00000000</span></span>                                   |
| <span data-ttu-id="a0a8c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-150">System-Flags</span></span>           | <span data-ttu-id="a0a8c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0a8c-151">0x00000010</span></span>                                   |
| <span data-ttu-id="a0a8c-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a0a8c-152">Classes used in</span></span>        | [<span data-ttu-id="a0a8c-153">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a0a8c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0a8c-154">Windows Server 2003</span></span>



| <span data-ttu-id="a0a8c-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0a8c-155">Entry</span></span> | <span data-ttu-id="a0a8c-156">Value</span><span class="sxs-lookup"><span data-stu-id="a0a8c-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a0a8c-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a0a8c-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a8c-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a8c-159">System-Only</span></span>            | <span data-ttu-id="a0a8c-160">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-160">False</span></span>                                        |
| <span data-ttu-id="a0a8c-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a0a8c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a8c-162">True</span><span class="sxs-lookup"><span data-stu-id="a0a8c-162">True</span></span>                                         |
| <span data-ttu-id="a0a8c-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a0a8c-163">Is Indexed</span></span>             | <span data-ttu-id="a0a8c-164">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-164">False</span></span>                                        |
| <span data-ttu-id="a0a8c-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a0a8c-165">In Global Catalog</span></span>      | <span data-ttu-id="a0a8c-166">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-166">False</span></span>                                        |
| <span data-ttu-id="a0a8c-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a0a8c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a8c-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0a8c-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a0a8c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a8c-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a8c-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-171">Search-Flags</span></span>           | <span data-ttu-id="a0a8c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a8c-172">0x00000000</span></span>                                   |
| <span data-ttu-id="a0a8c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-173">System-Flags</span></span>           | <span data-ttu-id="a0a8c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0a8c-174">0x00000010</span></span>                                   |
| <span data-ttu-id="a0a8c-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a0a8c-175">Classes used in</span></span>        | [<span data-ttu-id="a0a8c-176">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a0a8c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a0a8c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a0a8c-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0a8c-178">Entry</span></span> | <span data-ttu-id="a0a8c-179">Value</span><span class="sxs-lookup"><span data-stu-id="a0a8c-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a0a8c-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a0a8c-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a8c-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a8c-182">System-Only</span></span>            | <span data-ttu-id="a0a8c-183">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-183">False</span></span>                                        |
| <span data-ttu-id="a0a8c-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a0a8c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a8c-185">True</span><span class="sxs-lookup"><span data-stu-id="a0a8c-185">True</span></span>                                         |
| <span data-ttu-id="a0a8c-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a0a8c-186">Is Indexed</span></span>             | <span data-ttu-id="a0a8c-187">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-187">False</span></span>                                        |
| <span data-ttu-id="a0a8c-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a0a8c-188">In Global Catalog</span></span>      | <span data-ttu-id="a0a8c-189">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-189">False</span></span>                                        |
| <span data-ttu-id="a0a8c-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a0a8c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a8c-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0a8c-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a0a8c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a8c-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a8c-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-194">Search-Flags</span></span>           | <span data-ttu-id="a0a8c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a8c-195">0x00000000</span></span>                                   |
| <span data-ttu-id="a0a8c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-196">System-Flags</span></span>           | <span data-ttu-id="a0a8c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0a8c-197">0x00000010</span></span>                                   |
| <span data-ttu-id="a0a8c-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a0a8c-198">Classes used in</span></span>        | [<span data-ttu-id="a0a8c-199">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a0a8c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0a8c-200">Windows Server 2008</span></span>



| <span data-ttu-id="a0a8c-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0a8c-201">Entry</span></span> | <span data-ttu-id="a0a8c-202">Value</span><span class="sxs-lookup"><span data-stu-id="a0a8c-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a0a8c-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a0a8c-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a8c-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a8c-205">System-Only</span></span>            | <span data-ttu-id="a0a8c-206">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-206">False</span></span>                                        |
| <span data-ttu-id="a0a8c-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a0a8c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a8c-208">True</span><span class="sxs-lookup"><span data-stu-id="a0a8c-208">True</span></span>                                         |
| <span data-ttu-id="a0a8c-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a0a8c-209">Is Indexed</span></span>             | <span data-ttu-id="a0a8c-210">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-210">False</span></span>                                        |
| <span data-ttu-id="a0a8c-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a0a8c-211">In Global Catalog</span></span>      | <span data-ttu-id="a0a8c-212">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-212">False</span></span>                                        |
| <span data-ttu-id="a0a8c-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a0a8c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a8c-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0a8c-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a0a8c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a8c-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a8c-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-217">Search-Flags</span></span>           | <span data-ttu-id="a0a8c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a8c-218">0x00000000</span></span>                                   |
| <span data-ttu-id="a0a8c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-219">System-Flags</span></span>           | <span data-ttu-id="a0a8c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0a8c-220">0x00000010</span></span>                                   |
| <span data-ttu-id="a0a8c-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a0a8c-221">Classes used in</span></span>        | [<span data-ttu-id="a0a8c-222">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a0a8c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0a8c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a0a8c-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0a8c-224">Entry</span></span> | <span data-ttu-id="a0a8c-225">Value</span><span class="sxs-lookup"><span data-stu-id="a0a8c-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a0a8c-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a0a8c-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a8c-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a8c-228">System-Only</span></span>            | <span data-ttu-id="a0a8c-229">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-229">False</span></span>                                        |
| <span data-ttu-id="a0a8c-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a0a8c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a8c-231">True</span><span class="sxs-lookup"><span data-stu-id="a0a8c-231">True</span></span>                                         |
| <span data-ttu-id="a0a8c-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a0a8c-232">Is Indexed</span></span>             | <span data-ttu-id="a0a8c-233">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-233">False</span></span>                                        |
| <span data-ttu-id="a0a8c-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a0a8c-234">In Global Catalog</span></span>      | <span data-ttu-id="a0a8c-235">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-235">False</span></span>                                        |
| <span data-ttu-id="a0a8c-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a0a8c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a8c-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0a8c-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a0a8c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a8c-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a8c-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-240">Search-Flags</span></span>           | <span data-ttu-id="a0a8c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a8c-241">0x00000000</span></span>                                   |
| <span data-ttu-id="a0a8c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-242">System-Flags</span></span>           | <span data-ttu-id="a0a8c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0a8c-243">0x00000010</span></span>                                   |
| <span data-ttu-id="a0a8c-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a0a8c-244">Classes used in</span></span>        | [<span data-ttu-id="a0a8c-245">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a0a8c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0a8c-246">Windows Server 2012</span></span>



| <span data-ttu-id="a0a8c-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="a0a8c-247">Entry</span></span> | <span data-ttu-id="a0a8c-248">Value</span><span class="sxs-lookup"><span data-stu-id="a0a8c-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="a0a8c-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a0a8c-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a0a8c-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="a0a8c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a0a8c-251">System-Only</span></span>            | <span data-ttu-id="a0a8c-252">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-252">False</span></span>                                        |
| <span data-ttu-id="a0a8c-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a0a8c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a0a8c-254">True</span><span class="sxs-lookup"><span data-stu-id="a0a8c-254">True</span></span>                                         |
| <span data-ttu-id="a0a8c-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a0a8c-255">Is Indexed</span></span>             | <span data-ttu-id="a0a8c-256">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-256">False</span></span>                                        |
| <span data-ttu-id="a0a8c-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a0a8c-257">In Global Catalog</span></span>      | <span data-ttu-id="a0a8c-258">False</span><span class="sxs-lookup"><span data-stu-id="a0a8c-258">False</span></span>                                        |
| <span data-ttu-id="a0a8c-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a0a8c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a0a8c-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a0a8c-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="a0a8c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a0a8c-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a0a8c-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="a0a8c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-263">Search-Flags</span></span>           | <span data-ttu-id="a0a8c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0a8c-264">0x00000000</span></span>                                   |
| <span data-ttu-id="a0a8c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a0a8c-265">System-Flags</span></span>           | <span data-ttu-id="a0a8c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a0a8c-266">0x00000010</span></span>                                   |
| <span data-ttu-id="a0a8c-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a0a8c-267">Classes used in</span></span>        | [<span data-ttu-id="a0a8c-268">**ACS-Directiva**</span><span class="sxs-lookup"><span data-stu-id="a0a8c-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 






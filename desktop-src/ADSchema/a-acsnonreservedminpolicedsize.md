---
title: 'ACS: atributo de tamaño no reservado-mínimo-con directivas'
description: El atributo ACS-non-Reserved-min-Policialed-size solo es para uso interno.
ms.assetid: f5ee29ec-d2a9-4026-a4d1-0484d353efdc
ms.tgt_platform: multiple
keywords:
- 'ACS: esquema de AD de atributo de tamaño mínimo y no reservado-min-policía'
- aCSNonReservedMinPolicedSize esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Min-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9fa7794343929aa0f7d7d86f4fc1f1e9a8a5b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659240"
---
# <a name="acs-non-reserved-min-policed-size-attribute"></a><span data-ttu-id="ac7fb-105">ACS: atributo de tamaño no reservado-mínimo-con directivas</span><span class="sxs-lookup"><span data-stu-id="ac7fb-105">ACS-Non-Reserved-Min-Policed-Size attribute</span></span>

<span data-ttu-id="ac7fb-106">El atributo **ACS-non-Reserved-min-policialed-size** solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="ac7fb-106">The **ACS-Non-Reserved-Min-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="ac7fb-107">Basado en RFC2814.</span><span class="sxs-lookup"><span data-stu-id="ac7fb-107">Based on RFC2814.</span></span>



| <span data-ttu-id="ac7fb-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac7fb-108">Entry</span></span> | <span data-ttu-id="ac7fb-109">Value</span><span class="sxs-lookup"><span data-stu-id="ac7fb-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ac7fb-110">CN</span><span class="sxs-lookup"><span data-stu-id="ac7fb-110">CN</span></span>                | <span data-ttu-id="ac7fb-111">ACS-no reservado-número mínimo de directivas</span><span class="sxs-lookup"><span data-stu-id="ac7fb-111">ACS-Non-Reserved-Min-Policed-Size</span></span>    |
| <span data-ttu-id="ac7fb-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ac7fb-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ac7fb-113">aCSNonReservedMinPolicedSize</span><span class="sxs-lookup"><span data-stu-id="ac7fb-113">aCSNonReservedMinPolicedSize</span></span>         |
| <span data-ttu-id="ac7fb-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ac7fb-114">Size</span></span>              | <span data-ttu-id="ac7fb-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="ac7fb-115">8 bytes</span></span>                              |
| <span data-ttu-id="ac7fb-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ac7fb-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ac7fb-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ac7fb-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ac7fb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac7fb-118">Attribute-Id</span></span>      | <span data-ttu-id="ac7fb-119">1.2.840.113556.1.4.1321</span><span class="sxs-lookup"><span data-stu-id="ac7fb-119">1.2.840.113556.1.4.1321</span></span>              |
| <span data-ttu-id="ac7fb-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ac7fb-120">System-Id-Guid</span></span>    | <span data-ttu-id="ac7fb-121">b6873917-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="ac7fb-121">b6873917-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="ac7fb-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac7fb-122">Syntax</span></span>            | [<span data-ttu-id="ac7fb-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ac7fb-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ac7fb-124">Implementations</span></span>

-   [<span data-ttu-id="ac7fb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac7fb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac7fb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac7fb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac7fb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac7fb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac7fb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac7fb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ac7fb-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac7fb-132">Entry</span></span> | <span data-ttu-id="ac7fb-133">Value</span><span class="sxs-lookup"><span data-stu-id="ac7fb-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ac7fb-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ac7fb-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac7fb-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac7fb-136">System-Only</span></span>            | <span data-ttu-id="ac7fb-137">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-137">False</span></span>                                        |
| <span data-ttu-id="ac7fb-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ac7fb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ac7fb-139">True</span><span class="sxs-lookup"><span data-stu-id="ac7fb-139">True</span></span>                                         |
| <span data-ttu-id="ac7fb-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ac7fb-140">Is Indexed</span></span>             | <span data-ttu-id="ac7fb-141">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-141">False</span></span>                                        |
| <span data-ttu-id="ac7fb-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ac7fb-142">In Global Catalog</span></span>      | <span data-ttu-id="ac7fb-143">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-143">False</span></span>                                        |
| <span data-ttu-id="ac7fb-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ac7fb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac7fb-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac7fb-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ac7fb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac7fb-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac7fb-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-148">Search-Flags</span></span>           | <span data-ttu-id="ac7fb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac7fb-149">0x00000000</span></span>                                   |
| <span data-ttu-id="ac7fb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-150">System-Flags</span></span>           | <span data-ttu-id="ac7fb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac7fb-151">0x00000010</span></span>                                   |
| <span data-ttu-id="ac7fb-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ac7fb-152">Classes used in</span></span>        | [<span data-ttu-id="ac7fb-153">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac7fb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac7fb-154">Windows Server 2003</span></span>



| <span data-ttu-id="ac7fb-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac7fb-155">Entry</span></span> | <span data-ttu-id="ac7fb-156">Value</span><span class="sxs-lookup"><span data-stu-id="ac7fb-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ac7fb-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ac7fb-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac7fb-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac7fb-159">System-Only</span></span>            | <span data-ttu-id="ac7fb-160">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-160">False</span></span>                                        |
| <span data-ttu-id="ac7fb-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ac7fb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ac7fb-162">True</span><span class="sxs-lookup"><span data-stu-id="ac7fb-162">True</span></span>                                         |
| <span data-ttu-id="ac7fb-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ac7fb-163">Is Indexed</span></span>             | <span data-ttu-id="ac7fb-164">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-164">False</span></span>                                        |
| <span data-ttu-id="ac7fb-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ac7fb-165">In Global Catalog</span></span>      | <span data-ttu-id="ac7fb-166">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-166">False</span></span>                                        |
| <span data-ttu-id="ac7fb-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ac7fb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac7fb-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac7fb-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ac7fb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac7fb-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac7fb-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-171">Search-Flags</span></span>           | <span data-ttu-id="ac7fb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac7fb-172">0x00000000</span></span>                                   |
| <span data-ttu-id="ac7fb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-173">System-Flags</span></span>           | <span data-ttu-id="ac7fb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac7fb-174">0x00000010</span></span>                                   |
| <span data-ttu-id="ac7fb-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ac7fb-175">Classes used in</span></span>        | [<span data-ttu-id="ac7fb-176">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac7fb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac7fb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac7fb-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac7fb-178">Entry</span></span> | <span data-ttu-id="ac7fb-179">Value</span><span class="sxs-lookup"><span data-stu-id="ac7fb-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ac7fb-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ac7fb-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac7fb-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac7fb-182">System-Only</span></span>            | <span data-ttu-id="ac7fb-183">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-183">False</span></span>                                        |
| <span data-ttu-id="ac7fb-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ac7fb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ac7fb-185">True</span><span class="sxs-lookup"><span data-stu-id="ac7fb-185">True</span></span>                                         |
| <span data-ttu-id="ac7fb-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ac7fb-186">Is Indexed</span></span>             | <span data-ttu-id="ac7fb-187">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-187">False</span></span>                                        |
| <span data-ttu-id="ac7fb-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ac7fb-188">In Global Catalog</span></span>      | <span data-ttu-id="ac7fb-189">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-189">False</span></span>                                        |
| <span data-ttu-id="ac7fb-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ac7fb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac7fb-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac7fb-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ac7fb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac7fb-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac7fb-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-194">Search-Flags</span></span>           | <span data-ttu-id="ac7fb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac7fb-195">0x00000000</span></span>                                   |
| <span data-ttu-id="ac7fb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-196">System-Flags</span></span>           | <span data-ttu-id="ac7fb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac7fb-197">0x00000010</span></span>                                   |
| <span data-ttu-id="ac7fb-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ac7fb-198">Classes used in</span></span>        | [<span data-ttu-id="ac7fb-199">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac7fb-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac7fb-200">Windows Server 2008</span></span>



| <span data-ttu-id="ac7fb-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac7fb-201">Entry</span></span> | <span data-ttu-id="ac7fb-202">Value</span><span class="sxs-lookup"><span data-stu-id="ac7fb-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ac7fb-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ac7fb-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac7fb-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac7fb-205">System-Only</span></span>            | <span data-ttu-id="ac7fb-206">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-206">False</span></span>                                        |
| <span data-ttu-id="ac7fb-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ac7fb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ac7fb-208">True</span><span class="sxs-lookup"><span data-stu-id="ac7fb-208">True</span></span>                                         |
| <span data-ttu-id="ac7fb-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ac7fb-209">Is Indexed</span></span>             | <span data-ttu-id="ac7fb-210">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-210">False</span></span>                                        |
| <span data-ttu-id="ac7fb-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ac7fb-211">In Global Catalog</span></span>      | <span data-ttu-id="ac7fb-212">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-212">False</span></span>                                        |
| <span data-ttu-id="ac7fb-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ac7fb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac7fb-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac7fb-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ac7fb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac7fb-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac7fb-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-217">Search-Flags</span></span>           | <span data-ttu-id="ac7fb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac7fb-218">0x00000000</span></span>                                   |
| <span data-ttu-id="ac7fb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-219">System-Flags</span></span>           | <span data-ttu-id="ac7fb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac7fb-220">0x00000010</span></span>                                   |
| <span data-ttu-id="ac7fb-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ac7fb-221">Classes used in</span></span>        | [<span data-ttu-id="ac7fb-222">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac7fb-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac7fb-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac7fb-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac7fb-224">Entry</span></span> | <span data-ttu-id="ac7fb-225">Value</span><span class="sxs-lookup"><span data-stu-id="ac7fb-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ac7fb-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ac7fb-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac7fb-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac7fb-228">System-Only</span></span>            | <span data-ttu-id="ac7fb-229">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-229">False</span></span>                                        |
| <span data-ttu-id="ac7fb-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ac7fb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ac7fb-231">True</span><span class="sxs-lookup"><span data-stu-id="ac7fb-231">True</span></span>                                         |
| <span data-ttu-id="ac7fb-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ac7fb-232">Is Indexed</span></span>             | <span data-ttu-id="ac7fb-233">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-233">False</span></span>                                        |
| <span data-ttu-id="ac7fb-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ac7fb-234">In Global Catalog</span></span>      | <span data-ttu-id="ac7fb-235">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-235">False</span></span>                                        |
| <span data-ttu-id="ac7fb-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ac7fb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac7fb-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac7fb-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ac7fb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac7fb-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac7fb-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-240">Search-Flags</span></span>           | <span data-ttu-id="ac7fb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac7fb-241">0x00000000</span></span>                                   |
| <span data-ttu-id="ac7fb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-242">System-Flags</span></span>           | <span data-ttu-id="ac7fb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac7fb-243">0x00000010</span></span>                                   |
| <span data-ttu-id="ac7fb-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ac7fb-244">Classes used in</span></span>        | [<span data-ttu-id="ac7fb-245">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac7fb-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac7fb-246">Windows Server 2012</span></span>



| <span data-ttu-id="ac7fb-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac7fb-247">Entry</span></span> | <span data-ttu-id="ac7fb-248">Value</span><span class="sxs-lookup"><span data-stu-id="ac7fb-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ac7fb-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ac7fb-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac7fb-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ac7fb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac7fb-251">System-Only</span></span>            | <span data-ttu-id="ac7fb-252">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-252">False</span></span>                                        |
| <span data-ttu-id="ac7fb-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ac7fb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ac7fb-254">True</span><span class="sxs-lookup"><span data-stu-id="ac7fb-254">True</span></span>                                         |
| <span data-ttu-id="ac7fb-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ac7fb-255">Is Indexed</span></span>             | <span data-ttu-id="ac7fb-256">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-256">False</span></span>                                        |
| <span data-ttu-id="ac7fb-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ac7fb-257">In Global Catalog</span></span>      | <span data-ttu-id="ac7fb-258">False</span><span class="sxs-lookup"><span data-stu-id="ac7fb-258">False</span></span>                                        |
| <span data-ttu-id="ac7fb-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ac7fb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac7fb-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac7fb-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ac7fb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac7fb-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac7fb-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ac7fb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-263">Search-Flags</span></span>           | <span data-ttu-id="ac7fb-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac7fb-264">0x00000000</span></span>                                   |
| <span data-ttu-id="ac7fb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac7fb-265">System-Flags</span></span>           | <span data-ttu-id="ac7fb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac7fb-266">0x00000010</span></span>                                   |
| <span data-ttu-id="ac7fb-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ac7fb-267">Classes used in</span></span>        | [<span data-ttu-id="ac7fb-268">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="ac7fb-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






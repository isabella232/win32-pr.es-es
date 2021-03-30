---
title: Atributo ACS-no reservado-tasa máxima
description: El atributo ACS-non-Reserved-Rate-Rate solo es para uso interno.
ms.assetid: 4080839c-d99e-4527-8c81-6d23ab0d3d70
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de tasa de picos (no reservado) de ACS
- aCSNonReservedPeakRate esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Peak-Rate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3d2075e90648388a9a1277dbbe768a3fc616f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151501"
---
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="dc4b2-105">Atributo ACS-no reservado-tasa máxima</span><span class="sxs-lookup"><span data-stu-id="dc4b2-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="dc4b2-106">El atributo **ACS-non-Reserved-Rate-Rate** solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="dc4b2-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="dc4b2-107">Basado en RFC2814.</span><span class="sxs-lookup"><span data-stu-id="dc4b2-107">Based on RFC2814.</span></span>



| <span data-ttu-id="dc4b2-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc4b2-108">Entry</span></span> | <span data-ttu-id="dc4b2-109">Value</span><span class="sxs-lookup"><span data-stu-id="dc4b2-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="dc4b2-110">CN</span><span class="sxs-lookup"><span data-stu-id="dc4b2-110">CN</span></span>                | <span data-ttu-id="dc4b2-111">ACS-no reservado-tasa máxima</span><span class="sxs-lookup"><span data-stu-id="dc4b2-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="dc4b2-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="dc4b2-112">Ldap-Display-Name</span></span> | <span data-ttu-id="dc4b2-113">aCSNonReservedPeakRate</span><span class="sxs-lookup"><span data-stu-id="dc4b2-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="dc4b2-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="dc4b2-114">Size</span></span>              | <span data-ttu-id="dc4b2-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="dc4b2-115">8 bytes</span></span>                              |
| <span data-ttu-id="dc4b2-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="dc4b2-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="dc4b2-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="dc4b2-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="dc4b2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dc4b2-118">Attribute-Id</span></span>      | <span data-ttu-id="dc4b2-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="dc4b2-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="dc4b2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dc4b2-120">System-Id-Guid</span></span>    | <span data-ttu-id="dc4b2-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="dc4b2-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="dc4b2-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc4b2-122">Syntax</span></span>            | [<span data-ttu-id="dc4b2-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="dc4b2-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="dc4b2-124">Implementations</span></span>

-   [<span data-ttu-id="dc4b2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dc4b2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dc4b2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dc4b2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dc4b2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dc4b2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dc4b2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc4b2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="dc4b2-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc4b2-132">Entry</span></span> | <span data-ttu-id="dc4b2-133">Value</span><span class="sxs-lookup"><span data-stu-id="dc4b2-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dc4b2-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc4b2-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc4b2-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc4b2-136">System-Only</span></span>            | <span data-ttu-id="dc4b2-137">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-137">False</span></span>                                        |
| <span data-ttu-id="dc4b2-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc4b2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="dc4b2-139">True</span><span class="sxs-lookup"><span data-stu-id="dc4b2-139">True</span></span>                                         |
| <span data-ttu-id="dc4b2-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc4b2-140">Is Indexed</span></span>             | <span data-ttu-id="dc4b2-141">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-141">False</span></span>                                        |
| <span data-ttu-id="dc4b2-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc4b2-142">In Global Catalog</span></span>      | <span data-ttu-id="dc4b2-143">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-143">False</span></span>                                        |
| <span data-ttu-id="dc4b2-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc4b2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc4b2-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc4b2-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dc4b2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc4b2-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc4b2-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-148">Search-Flags</span></span>           | <span data-ttu-id="dc4b2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc4b2-149">0x00000000</span></span>                                   |
| <span data-ttu-id="dc4b2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-150">System-Flags</span></span>           | <span data-ttu-id="dc4b2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc4b2-151">0x00000010</span></span>                                   |
| <span data-ttu-id="dc4b2-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc4b2-152">Classes used in</span></span>        | [<span data-ttu-id="dc4b2-153">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dc4b2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc4b2-154">Windows Server 2003</span></span>



| <span data-ttu-id="dc4b2-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc4b2-155">Entry</span></span> | <span data-ttu-id="dc4b2-156">Value</span><span class="sxs-lookup"><span data-stu-id="dc4b2-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dc4b2-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc4b2-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc4b2-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc4b2-159">System-Only</span></span>            | <span data-ttu-id="dc4b2-160">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-160">False</span></span>                                        |
| <span data-ttu-id="dc4b2-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc4b2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="dc4b2-162">True</span><span class="sxs-lookup"><span data-stu-id="dc4b2-162">True</span></span>                                         |
| <span data-ttu-id="dc4b2-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc4b2-163">Is Indexed</span></span>             | <span data-ttu-id="dc4b2-164">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-164">False</span></span>                                        |
| <span data-ttu-id="dc4b2-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc4b2-165">In Global Catalog</span></span>      | <span data-ttu-id="dc4b2-166">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-166">False</span></span>                                        |
| <span data-ttu-id="dc4b2-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc4b2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc4b2-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc4b2-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dc4b2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc4b2-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc4b2-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-171">Search-Flags</span></span>           | <span data-ttu-id="dc4b2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc4b2-172">0x00000000</span></span>                                   |
| <span data-ttu-id="dc4b2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-173">System-Flags</span></span>           | <span data-ttu-id="dc4b2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc4b2-174">0x00000010</span></span>                                   |
| <span data-ttu-id="dc4b2-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc4b2-175">Classes used in</span></span>        | [<span data-ttu-id="dc4b2-176">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dc4b2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dc4b2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dc4b2-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc4b2-178">Entry</span></span> | <span data-ttu-id="dc4b2-179">Value</span><span class="sxs-lookup"><span data-stu-id="dc4b2-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dc4b2-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc4b2-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc4b2-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc4b2-182">System-Only</span></span>            | <span data-ttu-id="dc4b2-183">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-183">False</span></span>                                        |
| <span data-ttu-id="dc4b2-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc4b2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="dc4b2-185">True</span><span class="sxs-lookup"><span data-stu-id="dc4b2-185">True</span></span>                                         |
| <span data-ttu-id="dc4b2-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc4b2-186">Is Indexed</span></span>             | <span data-ttu-id="dc4b2-187">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-187">False</span></span>                                        |
| <span data-ttu-id="dc4b2-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc4b2-188">In Global Catalog</span></span>      | <span data-ttu-id="dc4b2-189">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-189">False</span></span>                                        |
| <span data-ttu-id="dc4b2-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc4b2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc4b2-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc4b2-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dc4b2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc4b2-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc4b2-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-194">Search-Flags</span></span>           | <span data-ttu-id="dc4b2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc4b2-195">0x00000000</span></span>                                   |
| <span data-ttu-id="dc4b2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-196">System-Flags</span></span>           | <span data-ttu-id="dc4b2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc4b2-197">0x00000010</span></span>                                   |
| <span data-ttu-id="dc4b2-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc4b2-198">Classes used in</span></span>        | [<span data-ttu-id="dc4b2-199">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dc4b2-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc4b2-200">Windows Server 2008</span></span>



| <span data-ttu-id="dc4b2-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc4b2-201">Entry</span></span> | <span data-ttu-id="dc4b2-202">Value</span><span class="sxs-lookup"><span data-stu-id="dc4b2-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dc4b2-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc4b2-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc4b2-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc4b2-205">System-Only</span></span>            | <span data-ttu-id="dc4b2-206">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-206">False</span></span>                                        |
| <span data-ttu-id="dc4b2-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc4b2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="dc4b2-208">True</span><span class="sxs-lookup"><span data-stu-id="dc4b2-208">True</span></span>                                         |
| <span data-ttu-id="dc4b2-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc4b2-209">Is Indexed</span></span>             | <span data-ttu-id="dc4b2-210">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-210">False</span></span>                                        |
| <span data-ttu-id="dc4b2-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc4b2-211">In Global Catalog</span></span>      | <span data-ttu-id="dc4b2-212">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-212">False</span></span>                                        |
| <span data-ttu-id="dc4b2-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc4b2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc4b2-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc4b2-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dc4b2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc4b2-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc4b2-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-217">Search-Flags</span></span>           | <span data-ttu-id="dc4b2-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc4b2-218">0x00000000</span></span>                                   |
| <span data-ttu-id="dc4b2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-219">System-Flags</span></span>           | <span data-ttu-id="dc4b2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc4b2-220">0x00000010</span></span>                                   |
| <span data-ttu-id="dc4b2-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc4b2-221">Classes used in</span></span>        | [<span data-ttu-id="dc4b2-222">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dc4b2-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc4b2-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dc4b2-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc4b2-224">Entry</span></span> | <span data-ttu-id="dc4b2-225">Value</span><span class="sxs-lookup"><span data-stu-id="dc4b2-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dc4b2-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc4b2-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc4b2-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc4b2-228">System-Only</span></span>            | <span data-ttu-id="dc4b2-229">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-229">False</span></span>                                        |
| <span data-ttu-id="dc4b2-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc4b2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="dc4b2-231">True</span><span class="sxs-lookup"><span data-stu-id="dc4b2-231">True</span></span>                                         |
| <span data-ttu-id="dc4b2-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc4b2-232">Is Indexed</span></span>             | <span data-ttu-id="dc4b2-233">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-233">False</span></span>                                        |
| <span data-ttu-id="dc4b2-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc4b2-234">In Global Catalog</span></span>      | <span data-ttu-id="dc4b2-235">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-235">False</span></span>                                        |
| <span data-ttu-id="dc4b2-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc4b2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc4b2-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc4b2-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dc4b2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc4b2-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc4b2-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-240">Search-Flags</span></span>           | <span data-ttu-id="dc4b2-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc4b2-241">0x00000000</span></span>                                   |
| <span data-ttu-id="dc4b2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-242">System-Flags</span></span>           | <span data-ttu-id="dc4b2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc4b2-243">0x00000010</span></span>                                   |
| <span data-ttu-id="dc4b2-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc4b2-244">Classes used in</span></span>        | [<span data-ttu-id="dc4b2-245">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dc4b2-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc4b2-246">Windows Server 2012</span></span>



| <span data-ttu-id="dc4b2-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc4b2-247">Entry</span></span> | <span data-ttu-id="dc4b2-248">Value</span><span class="sxs-lookup"><span data-stu-id="dc4b2-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dc4b2-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc4b2-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc4b2-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dc4b2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc4b2-251">System-Only</span></span>            | <span data-ttu-id="dc4b2-252">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-252">False</span></span>                                        |
| <span data-ttu-id="dc4b2-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc4b2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="dc4b2-254">True</span><span class="sxs-lookup"><span data-stu-id="dc4b2-254">True</span></span>                                         |
| <span data-ttu-id="dc4b2-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc4b2-255">Is Indexed</span></span>             | <span data-ttu-id="dc4b2-256">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-256">False</span></span>                                        |
| <span data-ttu-id="dc4b2-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc4b2-257">In Global Catalog</span></span>      | <span data-ttu-id="dc4b2-258">False</span><span class="sxs-lookup"><span data-stu-id="dc4b2-258">False</span></span>                                        |
| <span data-ttu-id="dc4b2-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc4b2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc4b2-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc4b2-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dc4b2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc4b2-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc4b2-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dc4b2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-263">Search-Flags</span></span>           | <span data-ttu-id="dc4b2-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc4b2-264">0x00000000</span></span>                                   |
| <span data-ttu-id="dc4b2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc4b2-265">System-Flags</span></span>           | <span data-ttu-id="dc4b2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc4b2-266">0x00000010</span></span>                                   |
| <span data-ttu-id="dc4b2-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc4b2-267">Classes used in</span></span>        | [<span data-ttu-id="dc4b2-268">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="dc4b2-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






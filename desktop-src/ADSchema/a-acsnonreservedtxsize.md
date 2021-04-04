---
title: Atributo ACS-no reservado-TX-size
description: El tamaño del depósito de tokens que puede usar una aplicación antes de que se realice una reserva.
ms.assetid: 67a0d6fd-b556-49d2-8c5b-6efebf1052c3
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de tamaño de TX no reservado de ACS
- aCSNonReservedTxSize esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cd19dde97e3a9fc6ef58165c8dbcbfbebba729
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906281"
---
# <a name="acs-non-reserved-tx-size-attribute"></a><span data-ttu-id="8d610-105">Atributo ACS-no reservado-TX-size</span><span class="sxs-lookup"><span data-stu-id="8d610-105">ACS-Non-Reserved-Tx-Size attribute</span></span>

<span data-ttu-id="8d610-106">El tamaño del depósito de tokens que puede usar una aplicación antes de que se realice una reserva.</span><span class="sxs-lookup"><span data-stu-id="8d610-106">The token bucket size an application can use before a reservation is in place.</span></span>



| <span data-ttu-id="8d610-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d610-107">Entry</span></span> | <span data-ttu-id="8d610-108">Value</span><span class="sxs-lookup"><span data-stu-id="8d610-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8d610-109">CN</span><span class="sxs-lookup"><span data-stu-id="8d610-109">CN</span></span>                | <span data-ttu-id="8d610-110">ACS-no reservado-TX-size</span><span class="sxs-lookup"><span data-stu-id="8d610-110">ACS-Non-Reserved-Tx-Size</span></span>             |
| <span data-ttu-id="8d610-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8d610-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8d610-112">aCSNonReservedTxSize</span><span class="sxs-lookup"><span data-stu-id="8d610-112">aCSNonReservedTxSize</span></span>                 |
| <span data-ttu-id="8d610-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8d610-113">Size</span></span>              | <span data-ttu-id="8d610-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="8d610-114">8 bytes</span></span>                              |
| <span data-ttu-id="8d610-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8d610-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8d610-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8d610-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8d610-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8d610-117">Attribute-Id</span></span>      | <span data-ttu-id="8d610-118">1.2.840.113556.1.4.898</span><span class="sxs-lookup"><span data-stu-id="8d610-118">1.2.840.113556.1.4.898</span></span>               |
| <span data-ttu-id="8d610-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8d610-119">System-Id-Guid</span></span>    | <span data-ttu-id="8d610-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8d610-120">f072230d-aef5-11d1-bdcf-0000f80367c1</span></span> |
| <span data-ttu-id="8d610-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d610-121">Syntax</span></span>            | [<span data-ttu-id="8d610-122">**Interval**</span><span class="sxs-lookup"><span data-stu-id="8d610-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="8d610-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8d610-123">Implementations</span></span>

-   [<span data-ttu-id="8d610-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8d610-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8d610-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8d610-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8d610-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8d610-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8d610-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8d610-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8d610-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8d610-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8d610-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8d610-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8d610-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d610-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8d610-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d610-131">Entry</span></span> | <span data-ttu-id="8d610-132">Value</span><span class="sxs-lookup"><span data-stu-id="8d610-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8d610-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8d610-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d610-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d610-135">System-Only</span></span>            | <span data-ttu-id="8d610-136">False</span><span class="sxs-lookup"><span data-stu-id="8d610-136">False</span></span>                                        |
| <span data-ttu-id="8d610-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8d610-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8d610-138">True</span><span class="sxs-lookup"><span data-stu-id="8d610-138">True</span></span>                                         |
| <span data-ttu-id="8d610-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8d610-139">Is Indexed</span></span>             | <span data-ttu-id="8d610-140">False</span><span class="sxs-lookup"><span data-stu-id="8d610-140">False</span></span>                                        |
| <span data-ttu-id="8d610-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8d610-141">In Global Catalog</span></span>      | <span data-ttu-id="8d610-142">False</span><span class="sxs-lookup"><span data-stu-id="8d610-142">False</span></span>                                        |
| <span data-ttu-id="8d610-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8d610-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d610-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d610-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8d610-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d610-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8d610-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d610-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8d610-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-147">Search-Flags</span></span>           | <span data-ttu-id="8d610-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d610-148">0x00000000</span></span>                                   |
| <span data-ttu-id="8d610-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-149">System-Flags</span></span>           | <span data-ttu-id="8d610-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d610-150">0x00000010</span></span>                                   |
| <span data-ttu-id="8d610-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8d610-151">Classes used in</span></span>        | [<span data-ttu-id="8d610-152">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="8d610-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8d610-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d610-153">Windows Server 2003</span></span>



| <span data-ttu-id="8d610-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d610-154">Entry</span></span> | <span data-ttu-id="8d610-155">Value</span><span class="sxs-lookup"><span data-stu-id="8d610-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8d610-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8d610-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d610-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d610-158">System-Only</span></span>            | <span data-ttu-id="8d610-159">False</span><span class="sxs-lookup"><span data-stu-id="8d610-159">False</span></span>                                        |
| <span data-ttu-id="8d610-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8d610-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8d610-161">True</span><span class="sxs-lookup"><span data-stu-id="8d610-161">True</span></span>                                         |
| <span data-ttu-id="8d610-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8d610-162">Is Indexed</span></span>             | <span data-ttu-id="8d610-163">False</span><span class="sxs-lookup"><span data-stu-id="8d610-163">False</span></span>                                        |
| <span data-ttu-id="8d610-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8d610-164">In Global Catalog</span></span>      | <span data-ttu-id="8d610-165">False</span><span class="sxs-lookup"><span data-stu-id="8d610-165">False</span></span>                                        |
| <span data-ttu-id="8d610-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8d610-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d610-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d610-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8d610-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d610-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8d610-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d610-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8d610-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-170">Search-Flags</span></span>           | <span data-ttu-id="8d610-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d610-171">0x00000000</span></span>                                   |
| <span data-ttu-id="8d610-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-172">System-Flags</span></span>           | <span data-ttu-id="8d610-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d610-173">0x00000010</span></span>                                   |
| <span data-ttu-id="8d610-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8d610-174">Classes used in</span></span>        | [<span data-ttu-id="8d610-175">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="8d610-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8d610-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8d610-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8d610-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d610-177">Entry</span></span> | <span data-ttu-id="8d610-178">Value</span><span class="sxs-lookup"><span data-stu-id="8d610-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8d610-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8d610-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d610-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d610-181">System-Only</span></span>            | <span data-ttu-id="8d610-182">False</span><span class="sxs-lookup"><span data-stu-id="8d610-182">False</span></span>                                        |
| <span data-ttu-id="8d610-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8d610-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8d610-184">True</span><span class="sxs-lookup"><span data-stu-id="8d610-184">True</span></span>                                         |
| <span data-ttu-id="8d610-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8d610-185">Is Indexed</span></span>             | <span data-ttu-id="8d610-186">False</span><span class="sxs-lookup"><span data-stu-id="8d610-186">False</span></span>                                        |
| <span data-ttu-id="8d610-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8d610-187">In Global Catalog</span></span>      | <span data-ttu-id="8d610-188">False</span><span class="sxs-lookup"><span data-stu-id="8d610-188">False</span></span>                                        |
| <span data-ttu-id="8d610-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8d610-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d610-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d610-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8d610-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d610-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8d610-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d610-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8d610-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-193">Search-Flags</span></span>           | <span data-ttu-id="8d610-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d610-194">0x00000000</span></span>                                   |
| <span data-ttu-id="8d610-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-195">System-Flags</span></span>           | <span data-ttu-id="8d610-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d610-196">0x00000010</span></span>                                   |
| <span data-ttu-id="8d610-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8d610-197">Classes used in</span></span>        | [<span data-ttu-id="8d610-198">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="8d610-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8d610-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d610-199">Windows Server 2008</span></span>



| <span data-ttu-id="8d610-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d610-200">Entry</span></span> | <span data-ttu-id="8d610-201">Value</span><span class="sxs-lookup"><span data-stu-id="8d610-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8d610-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8d610-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d610-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d610-204">System-Only</span></span>            | <span data-ttu-id="8d610-205">False</span><span class="sxs-lookup"><span data-stu-id="8d610-205">False</span></span>                                        |
| <span data-ttu-id="8d610-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8d610-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8d610-207">True</span><span class="sxs-lookup"><span data-stu-id="8d610-207">True</span></span>                                         |
| <span data-ttu-id="8d610-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8d610-208">Is Indexed</span></span>             | <span data-ttu-id="8d610-209">False</span><span class="sxs-lookup"><span data-stu-id="8d610-209">False</span></span>                                        |
| <span data-ttu-id="8d610-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8d610-210">In Global Catalog</span></span>      | <span data-ttu-id="8d610-211">False</span><span class="sxs-lookup"><span data-stu-id="8d610-211">False</span></span>                                        |
| <span data-ttu-id="8d610-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8d610-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d610-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d610-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8d610-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d610-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8d610-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d610-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8d610-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-216">Search-Flags</span></span>           | <span data-ttu-id="8d610-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d610-217">0x00000000</span></span>                                   |
| <span data-ttu-id="8d610-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-218">System-Flags</span></span>           | <span data-ttu-id="8d610-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d610-219">0x00000010</span></span>                                   |
| <span data-ttu-id="8d610-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8d610-220">Classes used in</span></span>        | [<span data-ttu-id="8d610-221">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="8d610-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8d610-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d610-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8d610-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d610-223">Entry</span></span> | <span data-ttu-id="8d610-224">Value</span><span class="sxs-lookup"><span data-stu-id="8d610-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8d610-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8d610-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d610-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d610-227">System-Only</span></span>            | <span data-ttu-id="8d610-228">False</span><span class="sxs-lookup"><span data-stu-id="8d610-228">False</span></span>                                        |
| <span data-ttu-id="8d610-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8d610-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8d610-230">True</span><span class="sxs-lookup"><span data-stu-id="8d610-230">True</span></span>                                         |
| <span data-ttu-id="8d610-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8d610-231">Is Indexed</span></span>             | <span data-ttu-id="8d610-232">False</span><span class="sxs-lookup"><span data-stu-id="8d610-232">False</span></span>                                        |
| <span data-ttu-id="8d610-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8d610-233">In Global Catalog</span></span>      | <span data-ttu-id="8d610-234">False</span><span class="sxs-lookup"><span data-stu-id="8d610-234">False</span></span>                                        |
| <span data-ttu-id="8d610-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8d610-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d610-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d610-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8d610-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d610-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8d610-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d610-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8d610-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-239">Search-Flags</span></span>           | <span data-ttu-id="8d610-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d610-240">0x00000000</span></span>                                   |
| <span data-ttu-id="8d610-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-241">System-Flags</span></span>           | <span data-ttu-id="8d610-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d610-242">0x00000010</span></span>                                   |
| <span data-ttu-id="8d610-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8d610-243">Classes used in</span></span>        | [<span data-ttu-id="8d610-244">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="8d610-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8d610-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d610-245">Windows Server 2012</span></span>



| <span data-ttu-id="8d610-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d610-246">Entry</span></span> | <span data-ttu-id="8d610-247">Value</span><span class="sxs-lookup"><span data-stu-id="8d610-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8d610-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8d610-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d610-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8d610-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d610-250">System-Only</span></span>            | <span data-ttu-id="8d610-251">False</span><span class="sxs-lookup"><span data-stu-id="8d610-251">False</span></span>                                        |
| <span data-ttu-id="8d610-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8d610-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8d610-253">True</span><span class="sxs-lookup"><span data-stu-id="8d610-253">True</span></span>                                         |
| <span data-ttu-id="8d610-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8d610-254">Is Indexed</span></span>             | <span data-ttu-id="8d610-255">False</span><span class="sxs-lookup"><span data-stu-id="8d610-255">False</span></span>                                        |
| <span data-ttu-id="8d610-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8d610-256">In Global Catalog</span></span>      | <span data-ttu-id="8d610-257">False</span><span class="sxs-lookup"><span data-stu-id="8d610-257">False</span></span>                                        |
| <span data-ttu-id="8d610-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8d610-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d610-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d610-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8d610-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d610-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8d610-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d610-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8d610-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-262">Search-Flags</span></span>           | <span data-ttu-id="8d610-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d610-263">0x00000000</span></span>                                   |
| <span data-ttu-id="8d610-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d610-264">System-Flags</span></span>           | <span data-ttu-id="8d610-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d610-265">0x00000010</span></span>                                   |
| <span data-ttu-id="8d610-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8d610-266">Classes used in</span></span>        | [<span data-ttu-id="8d610-267">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="8d610-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






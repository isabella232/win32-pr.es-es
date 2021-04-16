---
title: Atributo ACS-unreserved-TX-Limit
description: El ancho de banda máximo que una aplicación de usuario puede transmitir antes de que se realice una reserva.
ms.assetid: 5ead8e5b-31e8-438e-8d1b-9aae8601dfc9
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de límite de TX no reservado de ACS
- aCSNonReservedTxLimit esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999b1775640624b7825b38ae1632d70773bc75b3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658682"
---
# <a name="acs-non-reserved-tx-limit-attribute"></a><span data-ttu-id="b84da-105">Atributo ACS-unreserved-TX-Limit</span><span class="sxs-lookup"><span data-stu-id="b84da-105">ACS-Non-Reserved-Tx-Limit attribute</span></span>

<span data-ttu-id="b84da-106">El ancho de banda máximo que una aplicación de usuario puede transmitir antes de que se realice una reserva.</span><span class="sxs-lookup"><span data-stu-id="b84da-106">The maximum bandwidth a user application can transmit before a reservation is in place.</span></span>



| <span data-ttu-id="b84da-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b84da-107">Entry</span></span> | <span data-ttu-id="b84da-108">Value</span><span class="sxs-lookup"><span data-stu-id="b84da-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b84da-109">CN</span><span class="sxs-lookup"><span data-stu-id="b84da-109">CN</span></span>                | <span data-ttu-id="b84da-110">ACS-no reservado-TX-límite</span><span class="sxs-lookup"><span data-stu-id="b84da-110">ACS-Non-Reserved-Tx-Limit</span></span>            |
| <span data-ttu-id="b84da-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b84da-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b84da-112">aCSNonReservedTxLimit</span><span class="sxs-lookup"><span data-stu-id="b84da-112">aCSNonReservedTxLimit</span></span>                |
| <span data-ttu-id="b84da-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b84da-113">Size</span></span>              | <span data-ttu-id="b84da-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="b84da-114">8 bytes</span></span>                              |
| <span data-ttu-id="b84da-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b84da-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b84da-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b84da-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b84da-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b84da-117">Attribute-Id</span></span>      | <span data-ttu-id="b84da-118">1.2.840.113556.1.4.780</span><span class="sxs-lookup"><span data-stu-id="b84da-118">1.2.840.113556.1.4.780</span></span>               |
| <span data-ttu-id="b84da-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b84da-119">System-Id-Guid</span></span>    | <span data-ttu-id="b84da-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b84da-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="b84da-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b84da-121">Syntax</span></span>            | [<span data-ttu-id="b84da-122">**Interval**</span><span class="sxs-lookup"><span data-stu-id="b84da-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b84da-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b84da-123">Implementations</span></span>

-   [<span data-ttu-id="b84da-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b84da-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b84da-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b84da-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b84da-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b84da-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b84da-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b84da-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b84da-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b84da-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b84da-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b84da-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b84da-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b84da-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b84da-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="b84da-131">Entry</span></span> | <span data-ttu-id="b84da-132">Value</span><span class="sxs-lookup"><span data-stu-id="b84da-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b84da-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b84da-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b84da-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b84da-135">System-Only</span></span>            | <span data-ttu-id="b84da-136">False</span><span class="sxs-lookup"><span data-stu-id="b84da-136">False</span></span>                                        |
| <span data-ttu-id="b84da-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b84da-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b84da-138">True</span><span class="sxs-lookup"><span data-stu-id="b84da-138">True</span></span>                                         |
| <span data-ttu-id="b84da-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b84da-139">Is Indexed</span></span>             | <span data-ttu-id="b84da-140">False</span><span class="sxs-lookup"><span data-stu-id="b84da-140">False</span></span>                                        |
| <span data-ttu-id="b84da-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b84da-141">In Global Catalog</span></span>      | <span data-ttu-id="b84da-142">False</span><span class="sxs-lookup"><span data-stu-id="b84da-142">False</span></span>                                        |
| <span data-ttu-id="b84da-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b84da-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b84da-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b84da-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b84da-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b84da-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b84da-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b84da-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b84da-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-147">Search-Flags</span></span>           | <span data-ttu-id="b84da-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b84da-148">0x00000000</span></span>                                   |
| <span data-ttu-id="b84da-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-149">System-Flags</span></span>           | <span data-ttu-id="b84da-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b84da-150">0x00000010</span></span>                                   |
| <span data-ttu-id="b84da-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b84da-151">Classes used in</span></span>        | [<span data-ttu-id="b84da-152">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="b84da-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b84da-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b84da-153">Windows Server 2003</span></span>



| <span data-ttu-id="b84da-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="b84da-154">Entry</span></span> | <span data-ttu-id="b84da-155">Value</span><span class="sxs-lookup"><span data-stu-id="b84da-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b84da-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b84da-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b84da-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b84da-158">System-Only</span></span>            | <span data-ttu-id="b84da-159">False</span><span class="sxs-lookup"><span data-stu-id="b84da-159">False</span></span>                                        |
| <span data-ttu-id="b84da-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b84da-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b84da-161">True</span><span class="sxs-lookup"><span data-stu-id="b84da-161">True</span></span>                                         |
| <span data-ttu-id="b84da-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b84da-162">Is Indexed</span></span>             | <span data-ttu-id="b84da-163">False</span><span class="sxs-lookup"><span data-stu-id="b84da-163">False</span></span>                                        |
| <span data-ttu-id="b84da-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b84da-164">In Global Catalog</span></span>      | <span data-ttu-id="b84da-165">False</span><span class="sxs-lookup"><span data-stu-id="b84da-165">False</span></span>                                        |
| <span data-ttu-id="b84da-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b84da-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b84da-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b84da-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b84da-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b84da-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b84da-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b84da-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b84da-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-170">Search-Flags</span></span>           | <span data-ttu-id="b84da-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b84da-171">0x00000000</span></span>                                   |
| <span data-ttu-id="b84da-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-172">System-Flags</span></span>           | <span data-ttu-id="b84da-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b84da-173">0x00000010</span></span>                                   |
| <span data-ttu-id="b84da-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b84da-174">Classes used in</span></span>        | [<span data-ttu-id="b84da-175">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="b84da-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b84da-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b84da-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b84da-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="b84da-177">Entry</span></span> | <span data-ttu-id="b84da-178">Value</span><span class="sxs-lookup"><span data-stu-id="b84da-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b84da-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b84da-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b84da-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b84da-181">System-Only</span></span>            | <span data-ttu-id="b84da-182">False</span><span class="sxs-lookup"><span data-stu-id="b84da-182">False</span></span>                                        |
| <span data-ttu-id="b84da-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b84da-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b84da-184">True</span><span class="sxs-lookup"><span data-stu-id="b84da-184">True</span></span>                                         |
| <span data-ttu-id="b84da-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b84da-185">Is Indexed</span></span>             | <span data-ttu-id="b84da-186">False</span><span class="sxs-lookup"><span data-stu-id="b84da-186">False</span></span>                                        |
| <span data-ttu-id="b84da-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b84da-187">In Global Catalog</span></span>      | <span data-ttu-id="b84da-188">False</span><span class="sxs-lookup"><span data-stu-id="b84da-188">False</span></span>                                        |
| <span data-ttu-id="b84da-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b84da-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b84da-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b84da-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b84da-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b84da-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b84da-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b84da-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b84da-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-193">Search-Flags</span></span>           | <span data-ttu-id="b84da-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b84da-194">0x00000000</span></span>                                   |
| <span data-ttu-id="b84da-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-195">System-Flags</span></span>           | <span data-ttu-id="b84da-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b84da-196">0x00000010</span></span>                                   |
| <span data-ttu-id="b84da-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b84da-197">Classes used in</span></span>        | [<span data-ttu-id="b84da-198">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="b84da-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b84da-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b84da-199">Windows Server 2008</span></span>



| <span data-ttu-id="b84da-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="b84da-200">Entry</span></span> | <span data-ttu-id="b84da-201">Value</span><span class="sxs-lookup"><span data-stu-id="b84da-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b84da-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b84da-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b84da-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b84da-204">System-Only</span></span>            | <span data-ttu-id="b84da-205">False</span><span class="sxs-lookup"><span data-stu-id="b84da-205">False</span></span>                                        |
| <span data-ttu-id="b84da-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b84da-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b84da-207">True</span><span class="sxs-lookup"><span data-stu-id="b84da-207">True</span></span>                                         |
| <span data-ttu-id="b84da-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b84da-208">Is Indexed</span></span>             | <span data-ttu-id="b84da-209">False</span><span class="sxs-lookup"><span data-stu-id="b84da-209">False</span></span>                                        |
| <span data-ttu-id="b84da-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b84da-210">In Global Catalog</span></span>      | <span data-ttu-id="b84da-211">False</span><span class="sxs-lookup"><span data-stu-id="b84da-211">False</span></span>                                        |
| <span data-ttu-id="b84da-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b84da-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b84da-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b84da-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b84da-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b84da-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b84da-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b84da-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b84da-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-216">Search-Flags</span></span>           | <span data-ttu-id="b84da-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b84da-217">0x00000000</span></span>                                   |
| <span data-ttu-id="b84da-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-218">System-Flags</span></span>           | <span data-ttu-id="b84da-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b84da-219">0x00000010</span></span>                                   |
| <span data-ttu-id="b84da-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b84da-220">Classes used in</span></span>        | [<span data-ttu-id="b84da-221">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="b84da-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b84da-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b84da-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b84da-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="b84da-223">Entry</span></span> | <span data-ttu-id="b84da-224">Value</span><span class="sxs-lookup"><span data-stu-id="b84da-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b84da-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b84da-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b84da-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b84da-227">System-Only</span></span>            | <span data-ttu-id="b84da-228">False</span><span class="sxs-lookup"><span data-stu-id="b84da-228">False</span></span>                                        |
| <span data-ttu-id="b84da-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b84da-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b84da-230">True</span><span class="sxs-lookup"><span data-stu-id="b84da-230">True</span></span>                                         |
| <span data-ttu-id="b84da-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b84da-231">Is Indexed</span></span>             | <span data-ttu-id="b84da-232">False</span><span class="sxs-lookup"><span data-stu-id="b84da-232">False</span></span>                                        |
| <span data-ttu-id="b84da-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b84da-233">In Global Catalog</span></span>      | <span data-ttu-id="b84da-234">False</span><span class="sxs-lookup"><span data-stu-id="b84da-234">False</span></span>                                        |
| <span data-ttu-id="b84da-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b84da-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b84da-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b84da-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b84da-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b84da-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b84da-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b84da-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b84da-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-239">Search-Flags</span></span>           | <span data-ttu-id="b84da-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b84da-240">0x00000000</span></span>                                   |
| <span data-ttu-id="b84da-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-241">System-Flags</span></span>           | <span data-ttu-id="b84da-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b84da-242">0x00000010</span></span>                                   |
| <span data-ttu-id="b84da-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b84da-243">Classes used in</span></span>        | [<span data-ttu-id="b84da-244">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="b84da-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b84da-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b84da-245">Windows Server 2012</span></span>



| <span data-ttu-id="b84da-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="b84da-246">Entry</span></span> | <span data-ttu-id="b84da-247">Value</span><span class="sxs-lookup"><span data-stu-id="b84da-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="b84da-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b84da-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b84da-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="b84da-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b84da-250">System-Only</span></span>            | <span data-ttu-id="b84da-251">False</span><span class="sxs-lookup"><span data-stu-id="b84da-251">False</span></span>                                        |
| <span data-ttu-id="b84da-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b84da-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b84da-253">True</span><span class="sxs-lookup"><span data-stu-id="b84da-253">True</span></span>                                         |
| <span data-ttu-id="b84da-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b84da-254">Is Indexed</span></span>             | <span data-ttu-id="b84da-255">False</span><span class="sxs-lookup"><span data-stu-id="b84da-255">False</span></span>                                        |
| <span data-ttu-id="b84da-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b84da-256">In Global Catalog</span></span>      | <span data-ttu-id="b84da-257">False</span><span class="sxs-lookup"><span data-stu-id="b84da-257">False</span></span>                                        |
| <span data-ttu-id="b84da-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b84da-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b84da-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b84da-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="b84da-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b84da-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="b84da-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b84da-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="b84da-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-262">Search-Flags</span></span>           | <span data-ttu-id="b84da-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b84da-263">0x00000000</span></span>                                   |
| <span data-ttu-id="b84da-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b84da-264">System-Flags</span></span>           | <span data-ttu-id="b84da-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b84da-265">0x00000010</span></span>                                   |
| <span data-ttu-id="b84da-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b84da-266">Classes used in</span></span>        | [<span data-ttu-id="b84da-267">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="b84da-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






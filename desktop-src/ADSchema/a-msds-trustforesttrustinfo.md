---
title: atributo MS-DS-Trust-Forest-Trust-info
description: Contiene información de confianza de bosque (un BLOB binario) utilizada por el sistema para un objeto Trusted-Domain.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Trust-Forest-Trust-info
- Esquema de AD de atributo msDS-TrustForestTrustInfo
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804658"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="b99a7-105">atributo MS-DS-Trust-Forest-Trust-info</span><span class="sxs-lookup"><span data-stu-id="b99a7-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="b99a7-106">Contiene información de confianza de bosque (un BLOB binario) utilizada por el sistema para un objeto Trusted-Domain.</span><span class="sxs-lookup"><span data-stu-id="b99a7-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="b99a7-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b99a7-107">Entry</span></span> | <span data-ttu-id="b99a7-108">Value</span><span class="sxs-lookup"><span data-stu-id="b99a7-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b99a7-109">CN</span><span class="sxs-lookup"><span data-stu-id="b99a7-109">CN</span></span>                | <span data-ttu-id="b99a7-110">MS-DS-Trust-Forest-Trust-info</span><span class="sxs-lookup"><span data-stu-id="b99a7-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="b99a7-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b99a7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b99a7-112">msDS-TrustForestTrustInfo</span><span class="sxs-lookup"><span data-stu-id="b99a7-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="b99a7-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b99a7-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="b99a7-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b99a7-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="b99a7-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b99a7-115">Update Frequency</span></span>  | <span data-ttu-id="b99a7-116">Solo cuando se cambia la relación de confianza entre bosques.</span><span class="sxs-lookup"><span data-stu-id="b99a7-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="b99a7-117">Esto puede ocurrir si cambia la topología de un bosque de confianza.</span><span class="sxs-lookup"><span data-stu-id="b99a7-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="b99a7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b99a7-118">Attribute-Id</span></span>      | <span data-ttu-id="b99a7-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="b99a7-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="b99a7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b99a7-120">System-Id-Guid</span></span>    | <span data-ttu-id="b99a7-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="b99a7-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="b99a7-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b99a7-122">Syntax</span></span>            | [<span data-ttu-id="b99a7-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b99a7-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="b99a7-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b99a7-124">Implementations</span></span>

-   [<span data-ttu-id="b99a7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b99a7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b99a7-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b99a7-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b99a7-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b99a7-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b99a7-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b99a7-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b99a7-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b99a7-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b99a7-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b99a7-130">Windows Server 2003</span></span>



| <span data-ttu-id="b99a7-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="b99a7-131">Entry</span></span> | <span data-ttu-id="b99a7-132">Value</span><span class="sxs-lookup"><span data-stu-id="b99a7-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b99a7-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b99a7-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b99a7-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b99a7-135">System-Only</span></span>            | <span data-ttu-id="b99a7-136">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-136">False</span></span>                                                |
| <span data-ttu-id="b99a7-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b99a7-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b99a7-138">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-138">True</span></span>                                                 |
| <span data-ttu-id="b99a7-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b99a7-139">Is Indexed</span></span>             | <span data-ttu-id="b99a7-140">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-140">False</span></span>                                                |
| <span data-ttu-id="b99a7-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b99a7-141">In Global Catalog</span></span>      | <span data-ttu-id="b99a7-142">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-142">True</span></span>                                                 |
| <span data-ttu-id="b99a7-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b99a7-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b99a7-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b99a7-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b99a7-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b99a7-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b99a7-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-147">Search-Flags</span></span>           | <span data-ttu-id="b99a7-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b99a7-148">0x00000000</span></span>                                           |
| <span data-ttu-id="b99a7-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-149">System-Flags</span></span>           | <span data-ttu-id="b99a7-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b99a7-150">0x00000010</span></span>                                           |
| <span data-ttu-id="b99a7-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b99a7-151">Classes used in</span></span>        | [<span data-ttu-id="b99a7-152">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b99a7-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b99a7-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b99a7-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b99a7-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="b99a7-154">Entry</span></span> | <span data-ttu-id="b99a7-155">Value</span><span class="sxs-lookup"><span data-stu-id="b99a7-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b99a7-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b99a7-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b99a7-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b99a7-158">System-Only</span></span>            | <span data-ttu-id="b99a7-159">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-159">False</span></span>                                                |
| <span data-ttu-id="b99a7-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b99a7-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b99a7-161">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-161">True</span></span>                                                 |
| <span data-ttu-id="b99a7-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b99a7-162">Is Indexed</span></span>             | <span data-ttu-id="b99a7-163">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-163">False</span></span>                                                |
| <span data-ttu-id="b99a7-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b99a7-164">In Global Catalog</span></span>      | <span data-ttu-id="b99a7-165">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-165">True</span></span>                                                 |
| <span data-ttu-id="b99a7-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b99a7-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b99a7-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b99a7-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b99a7-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b99a7-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b99a7-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-170">Search-Flags</span></span>           | <span data-ttu-id="b99a7-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b99a7-171">0x00000000</span></span>                                           |
| <span data-ttu-id="b99a7-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-172">System-Flags</span></span>           | <span data-ttu-id="b99a7-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b99a7-173">0x00000010</span></span>                                           |
| <span data-ttu-id="b99a7-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b99a7-174">Classes used in</span></span>        | [<span data-ttu-id="b99a7-175">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b99a7-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b99a7-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b99a7-176">Windows Server 2008</span></span>



| <span data-ttu-id="b99a7-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="b99a7-177">Entry</span></span> | <span data-ttu-id="b99a7-178">Value</span><span class="sxs-lookup"><span data-stu-id="b99a7-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b99a7-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b99a7-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b99a7-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b99a7-181">System-Only</span></span>            | <span data-ttu-id="b99a7-182">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-182">False</span></span>                                                |
| <span data-ttu-id="b99a7-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b99a7-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b99a7-184">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-184">True</span></span>                                                 |
| <span data-ttu-id="b99a7-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b99a7-185">Is Indexed</span></span>             | <span data-ttu-id="b99a7-186">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-186">False</span></span>                                                |
| <span data-ttu-id="b99a7-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b99a7-187">In Global Catalog</span></span>      | <span data-ttu-id="b99a7-188">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-188">True</span></span>                                                 |
| <span data-ttu-id="b99a7-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b99a7-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b99a7-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b99a7-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b99a7-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b99a7-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b99a7-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-193">Search-Flags</span></span>           | <span data-ttu-id="b99a7-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b99a7-194">0x00000000</span></span>                                           |
| <span data-ttu-id="b99a7-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-195">System-Flags</span></span>           | <span data-ttu-id="b99a7-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b99a7-196">0x00000010</span></span>                                           |
| <span data-ttu-id="b99a7-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b99a7-197">Classes used in</span></span>        | [<span data-ttu-id="b99a7-198">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b99a7-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b99a7-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b99a7-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b99a7-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="b99a7-200">Entry</span></span> | <span data-ttu-id="b99a7-201">Value</span><span class="sxs-lookup"><span data-stu-id="b99a7-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b99a7-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b99a7-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b99a7-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b99a7-204">System-Only</span></span>            | <span data-ttu-id="b99a7-205">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-205">False</span></span>                                                |
| <span data-ttu-id="b99a7-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b99a7-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b99a7-207">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-207">True</span></span>                                                 |
| <span data-ttu-id="b99a7-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b99a7-208">Is Indexed</span></span>             | <span data-ttu-id="b99a7-209">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-209">False</span></span>                                                |
| <span data-ttu-id="b99a7-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b99a7-210">In Global Catalog</span></span>      | <span data-ttu-id="b99a7-211">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-211">True</span></span>                                                 |
| <span data-ttu-id="b99a7-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b99a7-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b99a7-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b99a7-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b99a7-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b99a7-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b99a7-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-216">Search-Flags</span></span>           | <span data-ttu-id="b99a7-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b99a7-217">0x00000000</span></span>                                           |
| <span data-ttu-id="b99a7-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-218">System-Flags</span></span>           | <span data-ttu-id="b99a7-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b99a7-219">0x00000010</span></span>                                           |
| <span data-ttu-id="b99a7-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b99a7-220">Classes used in</span></span>        | [<span data-ttu-id="b99a7-221">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b99a7-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b99a7-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b99a7-222">Windows Server 2012</span></span>



| <span data-ttu-id="b99a7-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="b99a7-223">Entry</span></span> | <span data-ttu-id="b99a7-224">Value</span><span class="sxs-lookup"><span data-stu-id="b99a7-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b99a7-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b99a7-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b99a7-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b99a7-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b99a7-227">System-Only</span></span>            | <span data-ttu-id="b99a7-228">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-228">False</span></span>                                                |
| <span data-ttu-id="b99a7-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b99a7-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b99a7-230">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-230">True</span></span>                                                 |
| <span data-ttu-id="b99a7-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b99a7-231">Is Indexed</span></span>             | <span data-ttu-id="b99a7-232">False</span><span class="sxs-lookup"><span data-stu-id="b99a7-232">False</span></span>                                                |
| <span data-ttu-id="b99a7-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b99a7-233">In Global Catalog</span></span>      | <span data-ttu-id="b99a7-234">True</span><span class="sxs-lookup"><span data-stu-id="b99a7-234">True</span></span>                                                 |
| <span data-ttu-id="b99a7-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b99a7-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b99a7-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b99a7-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b99a7-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b99a7-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b99a7-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="b99a7-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-239">Search-Flags</span></span>           | <span data-ttu-id="b99a7-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b99a7-240">0x00000000</span></span>                                           |
| <span data-ttu-id="b99a7-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b99a7-241">System-Flags</span></span>           | <span data-ttu-id="b99a7-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b99a7-242">0x00000010</span></span>                                           |
| <span data-ttu-id="b99a7-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b99a7-243">Classes used in</span></span>        | [<span data-ttu-id="b99a7-244">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="b99a7-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






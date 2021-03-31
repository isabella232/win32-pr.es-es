---
title: atributo MS-DS-allowed-DNS-Suffixs
description: La lista de sufijos permitidos para el atributo dNSHostName en objetos de equipo.
ms.assetid: acd57af8-a021-4704-8a56-304126cd3d4b
ms.tgt_platform: multiple
keywords:
- MS-DS-allowed-DNS-sufijos atributo AD Schema
- Esquema de AD del atributo msDS-AllowedDNSSuffixes
topic_type:
- apiref
api_name:
- ms-DS-Allowed-DNS-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46c3e4848f96c68041bfdc5f3f1cc9533b52d3e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804711"
---
# <a name="ms-ds-allowed-dns-suffixes-attribute"></a><span data-ttu-id="7e3c8-105">atributo MS-DS-allowed-DNS-Suffixs</span><span class="sxs-lookup"><span data-stu-id="7e3c8-105">ms-DS-Allowed-DNS-Suffixes attribute</span></span>

<span data-ttu-id="7e3c8-106">La lista de sufijos permitidos para el atributo dNSHostName en objetos de equipo.</span><span class="sxs-lookup"><span data-stu-id="7e3c8-106">The list of allowed suffixes for the dNSHostName attribute in computer objects.</span></span>



| <span data-ttu-id="7e3c8-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e3c8-107">Entry</span></span> | <span data-ttu-id="7e3c8-108">Value</span><span class="sxs-lookup"><span data-stu-id="7e3c8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7e3c8-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e3c8-109">CN</span></span>                | <span data-ttu-id="7e3c8-110">MS-DS-allowed-DNS-sufijos</span><span class="sxs-lookup"><span data-stu-id="7e3c8-110">ms-DS-Allowed-DNS-Suffixes</span></span>                  |
| <span data-ttu-id="7e3c8-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7e3c8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e3c8-112">msDS-AllowedDNSSuffixes</span><span class="sxs-lookup"><span data-stu-id="7e3c8-112">msDS-AllowedDNSSuffixes</span></span>                     |
| <span data-ttu-id="7e3c8-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7e3c8-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7e3c8-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7e3c8-114">Update Privilege</span></span>  | <span data-ttu-id="7e3c8-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="7e3c8-115">Domain administrator</span></span>                        |
| <span data-ttu-id="7e3c8-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7e3c8-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="7e3c8-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e3c8-117">Attribute-Id</span></span>      | <span data-ttu-id="7e3c8-118">1.2.840.113556.1.4.1710</span><span class="sxs-lookup"><span data-stu-id="7e3c8-118">1.2.840.113556.1.4.1710</span></span>                     |
| <span data-ttu-id="7e3c8-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7e3c8-119">System-Id-Guid</span></span>    | <span data-ttu-id="7e3c8-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span><span class="sxs-lookup"><span data-stu-id="7e3c8-120">8469441b-9ac4-4e45-8205-bd219dbf672d</span></span>        |
| <span data-ttu-id="7e3c8-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e3c8-121">Syntax</span></span>            | [<span data-ttu-id="7e3c8-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7e3c8-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7e3c8-123">Implementations</span></span>

-   [<span data-ttu-id="7e3c8-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e3c8-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7e3c8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e3c8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e3c8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e3c8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7e3c8-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e3c8-130">Windows Server 2003</span></span>



| <span data-ttu-id="7e3c8-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e3c8-131">Entry</span></span> | <span data-ttu-id="7e3c8-132">Value</span><span class="sxs-lookup"><span data-stu-id="7e3c8-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7e3c8-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e3c8-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3c8-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3c8-135">System-Only</span></span>            | <span data-ttu-id="7e3c8-136">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-136">False</span></span>                                        |
| <span data-ttu-id="7e3c8-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e3c8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3c8-138">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-138">False</span></span>                                        |
| <span data-ttu-id="7e3c8-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e3c8-139">Is Indexed</span></span>             | <span data-ttu-id="7e3c8-140">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-140">False</span></span>                                        |
| <span data-ttu-id="7e3c8-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e3c8-141">In Global Catalog</span></span>      | <span data-ttu-id="7e3c8-142">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-142">False</span></span>                                        |
| <span data-ttu-id="7e3c8-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e3c8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3c8-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3c8-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7e3c8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3c8-145">Range-Lower</span></span>            | <span data-ttu-id="7e3c8-146">0</span><span class="sxs-lookup"><span data-stu-id="7e3c8-146">0</span></span>                                            |
| <span data-ttu-id="7e3c8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3c8-147">Range-Upper</span></span>            | <span data-ttu-id="7e3c8-148">2048</span><span class="sxs-lookup"><span data-stu-id="7e3c8-148">2048</span></span>                                         |
| <span data-ttu-id="7e3c8-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-149">Search-Flags</span></span>           | <span data-ttu-id="7e3c8-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3c8-150">0x00000000</span></span>                                   |
| <span data-ttu-id="7e3c8-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-151">System-Flags</span></span>           | <span data-ttu-id="7e3c8-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3c8-152">0x00000010</span></span>                                   |
| <span data-ttu-id="7e3c8-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e3c8-153">Classes used in</span></span>        | [<span data-ttu-id="7e3c8-154">**Dominio DNS**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-154">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7e3c8-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="7e3c8-155">ADAM</span></span>



| <span data-ttu-id="7e3c8-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e3c8-156">Entry</span></span> | <span data-ttu-id="7e3c8-157">Value</span><span class="sxs-lookup"><span data-stu-id="7e3c8-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7e3c8-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e3c8-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3c8-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3c8-160">System-Only</span></span>            | <span data-ttu-id="7e3c8-161">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-161">False</span></span>                                        |
| <span data-ttu-id="7e3c8-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e3c8-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3c8-163">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-163">False</span></span>                                        |
| <span data-ttu-id="7e3c8-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e3c8-164">Is Indexed</span></span>             | <span data-ttu-id="7e3c8-165">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-165">False</span></span>                                        |
| <span data-ttu-id="7e3c8-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e3c8-166">In Global Catalog</span></span>      | <span data-ttu-id="7e3c8-167">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-167">False</span></span>                                        |
| <span data-ttu-id="7e3c8-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e3c8-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3c8-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3c8-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7e3c8-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3c8-170">Range-Lower</span></span>            | <span data-ttu-id="7e3c8-171">0</span><span class="sxs-lookup"><span data-stu-id="7e3c8-171">0</span></span>                                            |
| <span data-ttu-id="7e3c8-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3c8-172">Range-Upper</span></span>            | <span data-ttu-id="7e3c8-173">2048</span><span class="sxs-lookup"><span data-stu-id="7e3c8-173">2048</span></span>                                         |
| <span data-ttu-id="7e3c8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-174">Search-Flags</span></span>           | <span data-ttu-id="7e3c8-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3c8-175">0x00000000</span></span>                                   |
| <span data-ttu-id="7e3c8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-176">System-Flags</span></span>           | <span data-ttu-id="7e3c8-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3c8-177">0x00000010</span></span>                                   |
| <span data-ttu-id="7e3c8-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e3c8-178">Classes used in</span></span>        | [<span data-ttu-id="7e3c8-179">**Dominio DNS**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-179">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e3c8-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e3c8-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e3c8-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e3c8-181">Entry</span></span> | <span data-ttu-id="7e3c8-182">Value</span><span class="sxs-lookup"><span data-stu-id="7e3c8-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7e3c8-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e3c8-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3c8-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3c8-185">System-Only</span></span>            | <span data-ttu-id="7e3c8-186">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-186">False</span></span>                                        |
| <span data-ttu-id="7e3c8-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e3c8-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3c8-188">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-188">False</span></span>                                        |
| <span data-ttu-id="7e3c8-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e3c8-189">Is Indexed</span></span>             | <span data-ttu-id="7e3c8-190">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-190">False</span></span>                                        |
| <span data-ttu-id="7e3c8-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e3c8-191">In Global Catalog</span></span>      | <span data-ttu-id="7e3c8-192">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-192">False</span></span>                                        |
| <span data-ttu-id="7e3c8-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e3c8-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3c8-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3c8-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7e3c8-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3c8-195">Range-Lower</span></span>            | <span data-ttu-id="7e3c8-196">0</span><span class="sxs-lookup"><span data-stu-id="7e3c8-196">0</span></span>                                            |
| <span data-ttu-id="7e3c8-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3c8-197">Range-Upper</span></span>            | <span data-ttu-id="7e3c8-198">2048</span><span class="sxs-lookup"><span data-stu-id="7e3c8-198">2048</span></span>                                         |
| <span data-ttu-id="7e3c8-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-199">Search-Flags</span></span>           | <span data-ttu-id="7e3c8-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3c8-200">0x00000000</span></span>                                   |
| <span data-ttu-id="7e3c8-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-201">System-Flags</span></span>           | <span data-ttu-id="7e3c8-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3c8-202">0x00000010</span></span>                                   |
| <span data-ttu-id="7e3c8-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e3c8-203">Classes used in</span></span>        | [<span data-ttu-id="7e3c8-204">**Dominio DNS**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-204">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e3c8-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e3c8-205">Windows Server 2008</span></span>



| <span data-ttu-id="7e3c8-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e3c8-206">Entry</span></span> | <span data-ttu-id="7e3c8-207">Value</span><span class="sxs-lookup"><span data-stu-id="7e3c8-207">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7e3c8-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e3c8-208">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3c8-209">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3c8-210">System-Only</span></span>            | <span data-ttu-id="7e3c8-211">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-211">False</span></span>                                        |
| <span data-ttu-id="7e3c8-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e3c8-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3c8-213">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-213">False</span></span>                                        |
| <span data-ttu-id="7e3c8-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e3c8-214">Is Indexed</span></span>             | <span data-ttu-id="7e3c8-215">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-215">False</span></span>                                        |
| <span data-ttu-id="7e3c8-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e3c8-216">In Global Catalog</span></span>      | <span data-ttu-id="7e3c8-217">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-217">False</span></span>                                        |
| <span data-ttu-id="7e3c8-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e3c8-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3c8-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3c8-219">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7e3c8-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3c8-220">Range-Lower</span></span>            | <span data-ttu-id="7e3c8-221">0</span><span class="sxs-lookup"><span data-stu-id="7e3c8-221">0</span></span>                                            |
| <span data-ttu-id="7e3c8-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3c8-222">Range-Upper</span></span>            | <span data-ttu-id="7e3c8-223">2048</span><span class="sxs-lookup"><span data-stu-id="7e3c8-223">2048</span></span>                                         |
| <span data-ttu-id="7e3c8-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-224">Search-Flags</span></span>           | <span data-ttu-id="7e3c8-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3c8-225">0x00000000</span></span>                                   |
| <span data-ttu-id="7e3c8-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-226">System-Flags</span></span>           | <span data-ttu-id="7e3c8-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3c8-227">0x00000010</span></span>                                   |
| <span data-ttu-id="7e3c8-228">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e3c8-228">Classes used in</span></span>        | [<span data-ttu-id="7e3c8-229">**Dominio DNS**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-229">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e3c8-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e3c8-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e3c8-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e3c8-231">Entry</span></span> | <span data-ttu-id="7e3c8-232">Value</span><span class="sxs-lookup"><span data-stu-id="7e3c8-232">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7e3c8-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e3c8-233">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3c8-234">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3c8-235">System-Only</span></span>            | <span data-ttu-id="7e3c8-236">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-236">False</span></span>                                        |
| <span data-ttu-id="7e3c8-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e3c8-237">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3c8-238">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-238">False</span></span>                                        |
| <span data-ttu-id="7e3c8-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e3c8-239">Is Indexed</span></span>             | <span data-ttu-id="7e3c8-240">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-240">False</span></span>                                        |
| <span data-ttu-id="7e3c8-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e3c8-241">In Global Catalog</span></span>      | <span data-ttu-id="7e3c8-242">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-242">False</span></span>                                        |
| <span data-ttu-id="7e3c8-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e3c8-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3c8-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3c8-244">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7e3c8-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3c8-245">Range-Lower</span></span>            | <span data-ttu-id="7e3c8-246">0</span><span class="sxs-lookup"><span data-stu-id="7e3c8-246">0</span></span>                                            |
| <span data-ttu-id="7e3c8-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3c8-247">Range-Upper</span></span>            | <span data-ttu-id="7e3c8-248">2048</span><span class="sxs-lookup"><span data-stu-id="7e3c8-248">2048</span></span>                                         |
| <span data-ttu-id="7e3c8-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-249">Search-Flags</span></span>           | <span data-ttu-id="7e3c8-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3c8-250">0x00000000</span></span>                                   |
| <span data-ttu-id="7e3c8-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-251">System-Flags</span></span>           | <span data-ttu-id="7e3c8-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3c8-252">0x00000010</span></span>                                   |
| <span data-ttu-id="7e3c8-253">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e3c8-253">Classes used in</span></span>        | [<span data-ttu-id="7e3c8-254">**Dominio DNS**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-254">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e3c8-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e3c8-255">Windows Server 2012</span></span>



| <span data-ttu-id="7e3c8-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="7e3c8-256">Entry</span></span> | <span data-ttu-id="7e3c8-257">Value</span><span class="sxs-lookup"><span data-stu-id="7e3c8-257">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7e3c8-258">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7e3c8-258">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3c8-259">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7e3c8-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3c8-260">System-Only</span></span>            | <span data-ttu-id="7e3c8-261">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-261">False</span></span>                                        |
| <span data-ttu-id="7e3c8-262">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7e3c8-262">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3c8-263">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-263">False</span></span>                                        |
| <span data-ttu-id="7e3c8-264">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7e3c8-264">Is Indexed</span></span>             | <span data-ttu-id="7e3c8-265">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-265">False</span></span>                                        |
| <span data-ttu-id="7e3c8-266">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7e3c8-266">In Global Catalog</span></span>      | <span data-ttu-id="7e3c8-267">False</span><span class="sxs-lookup"><span data-stu-id="7e3c8-267">False</span></span>                                        |
| <span data-ttu-id="7e3c8-268">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7e3c8-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3c8-269">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3c8-269">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7e3c8-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3c8-270">Range-Lower</span></span>            | <span data-ttu-id="7e3c8-271">0</span><span class="sxs-lookup"><span data-stu-id="7e3c8-271">0</span></span>                                            |
| <span data-ttu-id="7e3c8-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3c8-272">Range-Upper</span></span>            | <span data-ttu-id="7e3c8-273">2048</span><span class="sxs-lookup"><span data-stu-id="7e3c8-273">2048</span></span>                                         |
| <span data-ttu-id="7e3c8-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-274">Search-Flags</span></span>           | <span data-ttu-id="7e3c8-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3c8-275">0x00000000</span></span>                                   |
| <span data-ttu-id="7e3c8-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3c8-276">System-Flags</span></span>           | <span data-ttu-id="7e3c8-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3c8-277">0x00000010</span></span>                                   |
| <span data-ttu-id="7e3c8-278">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7e3c8-278">Classes used in</span></span>        | [<span data-ttu-id="7e3c8-279">**Dominio DNS**</span><span class="sxs-lookup"><span data-stu-id="7e3c8-279">**Domain-DNS**</span></span>](c-domaindns.md)<br/> |



 

 






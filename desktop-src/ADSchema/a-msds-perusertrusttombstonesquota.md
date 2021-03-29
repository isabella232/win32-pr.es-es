---
title: Atributo de cuota MS-DS-per-user-Trust-distinción
description: Se utiliza para exigir una cuota por usuario para eliminar Trusted-Domain objetos cuando la autorización se basa en la coincidencia del SID del usuario.
ms.assetid: 4db98754-a2d1-43a4-b9cb-0e3fcbbf3ed9
ms.tgt_platform: multiple
keywords:
- MS-DS-per-user-Trust-distinción-esquema de AD de atributo de cuota
- Esquema de AD de atributo msDS-PerUserTrustTombstonesQuota
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Tombstones-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c94bb62b822552a863df99dac83e98462514c42
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658861"
---
# <a name="ms-ds-per-user-trust-tombstones-quota-attribute"></a><span data-ttu-id="ab060-105">Atributo de cuota MS-DS-per-user-Trust-distinción</span><span class="sxs-lookup"><span data-stu-id="ab060-105">MS-DS-Per-User-Trust-Tombstones-Quota attribute</span></span>

<span data-ttu-id="ab060-106">Se utiliza para exigir una cuota por usuario para eliminar Trusted-Domain objetos cuando la autorización se basa en la coincidencia del SID del usuario.</span><span class="sxs-lookup"><span data-stu-id="ab060-106">Used to enforce a per-user quota for deleting Trusted-Domain objects when authorization is based on matching the user's SID.</span></span>



| <span data-ttu-id="ab060-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab060-107">Entry</span></span> | <span data-ttu-id="ab060-108">Value</span><span class="sxs-lookup"><span data-stu-id="ab060-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="ab060-109">CN</span><span class="sxs-lookup"><span data-stu-id="ab060-109">CN</span></span>                | <span data-ttu-id="ab060-110">MS-DS-per-user-Trust-distinción-quota</span><span class="sxs-lookup"><span data-stu-id="ab060-110">MS-DS-Per-User-Trust-Tombstones-Quota</span></span>     |
| <span data-ttu-id="ab060-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ab060-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ab060-112">msDS-PerUserTrustTombstonesQuota</span><span class="sxs-lookup"><span data-stu-id="ab060-112">msDS-PerUserTrustTombstonesQuota</span></span>          |
| <span data-ttu-id="ab060-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ab060-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="ab060-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ab060-114">Update Privilege</span></span>  | <span data-ttu-id="ab060-115">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="ab060-115">Domain administrator</span></span>                      |
| <span data-ttu-id="ab060-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ab060-116">Update Frequency</span></span>  | <span data-ttu-id="ab060-117">Al crear el bosque y raramente después.</span><span class="sxs-lookup"><span data-stu-id="ab060-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="ab060-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ab060-118">Attribute-Id</span></span>      | <span data-ttu-id="ab060-119">1.2.840.113556.1.4.1790</span><span class="sxs-lookup"><span data-stu-id="ab060-119">1.2.840.113556.1.4.1790</span></span>                   |
| <span data-ttu-id="ab060-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ab060-120">System-Id-Guid</span></span>    | <span data-ttu-id="ab060-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span><span class="sxs-lookup"><span data-stu-id="ab060-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span></span>      |
| <span data-ttu-id="ab060-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab060-122">Syntax</span></span>            | [<span data-ttu-id="ab060-123">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="ab060-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="ab060-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ab060-124">Implementations</span></span>

-   [<span data-ttu-id="ab060-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ab060-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ab060-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ab060-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ab060-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ab060-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ab060-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ab060-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ab060-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ab060-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ab060-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab060-130">Windows Server 2003</span></span>



| <span data-ttu-id="ab060-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab060-131">Entry</span></span> | <span data-ttu-id="ab060-132">Value</span><span class="sxs-lookup"><span data-stu-id="ab060-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab060-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab060-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab060-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab060-135">System-Only</span></span>            | <span data-ttu-id="ab060-136">False</span><span class="sxs-lookup"><span data-stu-id="ab060-136">False</span></span>                                        |
| <span data-ttu-id="ab060-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab060-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ab060-138">True</span><span class="sxs-lookup"><span data-stu-id="ab060-138">True</span></span>                                         |
| <span data-ttu-id="ab060-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab060-139">Is Indexed</span></span>             | <span data-ttu-id="ab060-140">False</span><span class="sxs-lookup"><span data-stu-id="ab060-140">False</span></span>                                        |
| <span data-ttu-id="ab060-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab060-141">In Global Catalog</span></span>      | <span data-ttu-id="ab060-142">False</span><span class="sxs-lookup"><span data-stu-id="ab060-142">False</span></span>                                        |
| <span data-ttu-id="ab060-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab060-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab060-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab060-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab060-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab060-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab060-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab060-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab060-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-147">Search-Flags</span></span>           | <span data-ttu-id="ab060-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab060-148">0x00000000</span></span>                                   |
| <span data-ttu-id="ab060-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-149">System-Flags</span></span>           | <span data-ttu-id="ab060-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab060-150">0x00000010</span></span>                                   |
| <span data-ttu-id="ab060-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab060-151">Classes used in</span></span>        | [<span data-ttu-id="ab060-152">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ab060-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ab060-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ab060-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ab060-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab060-154">Entry</span></span> | <span data-ttu-id="ab060-155">Value</span><span class="sxs-lookup"><span data-stu-id="ab060-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab060-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab060-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab060-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab060-158">System-Only</span></span>            | <span data-ttu-id="ab060-159">False</span><span class="sxs-lookup"><span data-stu-id="ab060-159">False</span></span>                                        |
| <span data-ttu-id="ab060-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab060-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ab060-161">True</span><span class="sxs-lookup"><span data-stu-id="ab060-161">True</span></span>                                         |
| <span data-ttu-id="ab060-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab060-162">Is Indexed</span></span>             | <span data-ttu-id="ab060-163">False</span><span class="sxs-lookup"><span data-stu-id="ab060-163">False</span></span>                                        |
| <span data-ttu-id="ab060-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab060-164">In Global Catalog</span></span>      | <span data-ttu-id="ab060-165">False</span><span class="sxs-lookup"><span data-stu-id="ab060-165">False</span></span>                                        |
| <span data-ttu-id="ab060-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab060-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab060-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab060-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab060-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab060-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab060-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab060-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab060-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-170">Search-Flags</span></span>           | <span data-ttu-id="ab060-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab060-171">0x00000000</span></span>                                   |
| <span data-ttu-id="ab060-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-172">System-Flags</span></span>           | <span data-ttu-id="ab060-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab060-173">0x00000010</span></span>                                   |
| <span data-ttu-id="ab060-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab060-174">Classes used in</span></span>        | [<span data-ttu-id="ab060-175">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ab060-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ab060-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab060-176">Windows Server 2008</span></span>



| <span data-ttu-id="ab060-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab060-177">Entry</span></span> | <span data-ttu-id="ab060-178">Value</span><span class="sxs-lookup"><span data-stu-id="ab060-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab060-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab060-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab060-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab060-181">System-Only</span></span>            | <span data-ttu-id="ab060-182">False</span><span class="sxs-lookup"><span data-stu-id="ab060-182">False</span></span>                                        |
| <span data-ttu-id="ab060-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab060-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ab060-184">True</span><span class="sxs-lookup"><span data-stu-id="ab060-184">True</span></span>                                         |
| <span data-ttu-id="ab060-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab060-185">Is Indexed</span></span>             | <span data-ttu-id="ab060-186">False</span><span class="sxs-lookup"><span data-stu-id="ab060-186">False</span></span>                                        |
| <span data-ttu-id="ab060-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab060-187">In Global Catalog</span></span>      | <span data-ttu-id="ab060-188">False</span><span class="sxs-lookup"><span data-stu-id="ab060-188">False</span></span>                                        |
| <span data-ttu-id="ab060-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab060-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab060-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab060-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab060-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab060-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab060-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab060-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab060-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-193">Search-Flags</span></span>           | <span data-ttu-id="ab060-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab060-194">0x00000000</span></span>                                   |
| <span data-ttu-id="ab060-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-195">System-Flags</span></span>           | <span data-ttu-id="ab060-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab060-196">0x00000010</span></span>                                   |
| <span data-ttu-id="ab060-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab060-197">Classes used in</span></span>        | [<span data-ttu-id="ab060-198">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ab060-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ab060-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ab060-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ab060-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab060-200">Entry</span></span> | <span data-ttu-id="ab060-201">Value</span><span class="sxs-lookup"><span data-stu-id="ab060-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab060-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab060-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab060-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab060-204">System-Only</span></span>            | <span data-ttu-id="ab060-205">False</span><span class="sxs-lookup"><span data-stu-id="ab060-205">False</span></span>                                        |
| <span data-ttu-id="ab060-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab060-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ab060-207">True</span><span class="sxs-lookup"><span data-stu-id="ab060-207">True</span></span>                                         |
| <span data-ttu-id="ab060-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab060-208">Is Indexed</span></span>             | <span data-ttu-id="ab060-209">False</span><span class="sxs-lookup"><span data-stu-id="ab060-209">False</span></span>                                        |
| <span data-ttu-id="ab060-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab060-210">In Global Catalog</span></span>      | <span data-ttu-id="ab060-211">False</span><span class="sxs-lookup"><span data-stu-id="ab060-211">False</span></span>                                        |
| <span data-ttu-id="ab060-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab060-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab060-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab060-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab060-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab060-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab060-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab060-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab060-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-216">Search-Flags</span></span>           | <span data-ttu-id="ab060-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab060-217">0x00000000</span></span>                                   |
| <span data-ttu-id="ab060-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-218">System-Flags</span></span>           | <span data-ttu-id="ab060-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab060-219">0x00000010</span></span>                                   |
| <span data-ttu-id="ab060-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab060-220">Classes used in</span></span>        | [<span data-ttu-id="ab060-221">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ab060-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ab060-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab060-222">Windows Server 2012</span></span>



| <span data-ttu-id="ab060-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="ab060-223">Entry</span></span> | <span data-ttu-id="ab060-224">Value</span><span class="sxs-lookup"><span data-stu-id="ab060-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab060-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ab060-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab060-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab060-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab060-227">System-Only</span></span>            | <span data-ttu-id="ab060-228">False</span><span class="sxs-lookup"><span data-stu-id="ab060-228">False</span></span>                                        |
| <span data-ttu-id="ab060-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ab060-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ab060-230">True</span><span class="sxs-lookup"><span data-stu-id="ab060-230">True</span></span>                                         |
| <span data-ttu-id="ab060-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ab060-231">Is Indexed</span></span>             | <span data-ttu-id="ab060-232">False</span><span class="sxs-lookup"><span data-stu-id="ab060-232">False</span></span>                                        |
| <span data-ttu-id="ab060-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ab060-233">In Global Catalog</span></span>      | <span data-ttu-id="ab060-234">False</span><span class="sxs-lookup"><span data-stu-id="ab060-234">False</span></span>                                        |
| <span data-ttu-id="ab060-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ab060-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab060-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab060-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab060-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab060-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab060-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab060-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab060-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-239">Search-Flags</span></span>           | <span data-ttu-id="ab060-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab060-240">0x00000000</span></span>                                   |
| <span data-ttu-id="ab060-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab060-241">System-Flags</span></span>           | <span data-ttu-id="ab060-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab060-242">0x00000010</span></span>                                   |
| <span data-ttu-id="ab060-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ab060-243">Classes used in</span></span>        | [<span data-ttu-id="ab060-244">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="ab060-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






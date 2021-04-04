---
title: atributo MS-DS-default-quota
description: La cuota predeterminada que se aplicará a una entidad de seguridad que crea un objeto en el NC si no existe ninguna especificación de cuota que cubra la entidad de seguridad.
ms.assetid: 48074aaa-3997-40ac-92fe-b3112408ab45
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de cuota MS-DS-default-
- Esquema de AD de atributo msDS-DefaultQuota
topic_type:
- apiref
api_name:
- ms-DS-Default-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96f1429be72c623843608856da88729b1240c38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997564"
---
# <a name="ms-ds-default-quota-attribute"></a><span data-ttu-id="9b169-105">atributo MS-DS-default-quota</span><span class="sxs-lookup"><span data-stu-id="9b169-105">ms-DS-Default-Quota attribute</span></span>

<span data-ttu-id="9b169-106">La cuota predeterminada que se aplicará a una entidad de seguridad que crea un objeto en el NC si no existe ninguna especificación de cuota que cubra la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9b169-106">The default quota that will apply to a security principal that creates an object in the NC if no quota specification exists that covers the security principal.</span></span>



| <span data-ttu-id="9b169-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b169-107">Entry</span></span> | <span data-ttu-id="9b169-108">Value</span><span class="sxs-lookup"><span data-stu-id="9b169-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9b169-109">CN</span><span class="sxs-lookup"><span data-stu-id="9b169-109">CN</span></span>                | <span data-ttu-id="9b169-110">MS-DS-default-quota</span><span class="sxs-lookup"><span data-stu-id="9b169-110">ms-DS-Default-Quota</span></span>                  |
| <span data-ttu-id="9b169-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="9b169-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9b169-112">msDS-DefaultQuota</span><span class="sxs-lookup"><span data-stu-id="9b169-112">msDS-DefaultQuota</span></span>                    |
| <span data-ttu-id="9b169-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9b169-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9b169-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="9b169-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9b169-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="9b169-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9b169-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9b169-116">Attribute-Id</span></span>      | <span data-ttu-id="9b169-117">1.2.840.113556.1.4.1846</span><span class="sxs-lookup"><span data-stu-id="9b169-117">1.2.840.113556.1.4.1846</span></span>              |
| <span data-ttu-id="9b169-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9b169-118">System-Id-Guid</span></span>    | <span data-ttu-id="9b169-119">6818f726-674b-441b-8a3a-f40596374cea</span><span class="sxs-lookup"><span data-stu-id="9b169-119">6818f726-674b-441b-8a3a-f40596374cea</span></span> |
| <span data-ttu-id="9b169-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b169-120">Syntax</span></span>            | [<span data-ttu-id="9b169-121">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="9b169-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="9b169-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="9b169-122">Implementations</span></span>

-   [<span data-ttu-id="9b169-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9b169-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9b169-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9b169-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9b169-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9b169-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9b169-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9b169-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9b169-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9b169-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9b169-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9b169-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9b169-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b169-129">Windows Server 2003</span></span>



| <span data-ttu-id="9b169-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b169-130">Entry</span></span> | <span data-ttu-id="9b169-131">Value</span><span class="sxs-lookup"><span data-stu-id="9b169-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9b169-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b169-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b169-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b169-134">System-Only</span></span>            | <span data-ttu-id="9b169-135">False</span><span class="sxs-lookup"><span data-stu-id="9b169-135">False</span></span>                                                             |
| <span data-ttu-id="9b169-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b169-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9b169-137">True</span><span class="sxs-lookup"><span data-stu-id="9b169-137">True</span></span>                                                              |
| <span data-ttu-id="9b169-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b169-138">Is Indexed</span></span>             | <span data-ttu-id="9b169-139">False</span><span class="sxs-lookup"><span data-stu-id="9b169-139">False</span></span>                                                             |
| <span data-ttu-id="9b169-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b169-140">In Global Catalog</span></span>      | <span data-ttu-id="9b169-141">False</span><span class="sxs-lookup"><span data-stu-id="9b169-141">False</span></span>                                                             |
| <span data-ttu-id="9b169-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b169-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b169-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b169-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9b169-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b169-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b169-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-146">Search-Flags</span></span>           | <span data-ttu-id="9b169-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b169-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="9b169-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-148">System-Flags</span></span>           | <span data-ttu-id="9b169-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b169-149">0x00000010</span></span>                                                        |
| <span data-ttu-id="9b169-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b169-150">Classes used in</span></span>        | [<span data-ttu-id="9b169-151">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="9b169-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9b169-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="9b169-152">ADAM</span></span>



| <span data-ttu-id="9b169-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b169-153">Entry</span></span> | <span data-ttu-id="9b169-154">Value</span><span class="sxs-lookup"><span data-stu-id="9b169-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9b169-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b169-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b169-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b169-157">System-Only</span></span>            | <span data-ttu-id="9b169-158">False</span><span class="sxs-lookup"><span data-stu-id="9b169-158">False</span></span>                                                             |
| <span data-ttu-id="9b169-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b169-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9b169-160">True</span><span class="sxs-lookup"><span data-stu-id="9b169-160">True</span></span>                                                              |
| <span data-ttu-id="9b169-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b169-161">Is Indexed</span></span>             | <span data-ttu-id="9b169-162">False</span><span class="sxs-lookup"><span data-stu-id="9b169-162">False</span></span>                                                             |
| <span data-ttu-id="9b169-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b169-163">In Global Catalog</span></span>      | <span data-ttu-id="9b169-164">False</span><span class="sxs-lookup"><span data-stu-id="9b169-164">False</span></span>                                                             |
| <span data-ttu-id="9b169-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b169-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b169-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b169-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9b169-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b169-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b169-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-169">Search-Flags</span></span>           | <span data-ttu-id="9b169-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b169-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="9b169-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-171">System-Flags</span></span>           | <span data-ttu-id="9b169-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b169-172">0x00000010</span></span>                                                        |
| <span data-ttu-id="9b169-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b169-173">Classes used in</span></span>        | [<span data-ttu-id="9b169-174">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="9b169-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9b169-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9b169-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9b169-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b169-176">Entry</span></span> | <span data-ttu-id="9b169-177">Value</span><span class="sxs-lookup"><span data-stu-id="9b169-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9b169-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b169-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b169-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b169-180">System-Only</span></span>            | <span data-ttu-id="9b169-181">False</span><span class="sxs-lookup"><span data-stu-id="9b169-181">False</span></span>                                                             |
| <span data-ttu-id="9b169-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b169-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9b169-183">True</span><span class="sxs-lookup"><span data-stu-id="9b169-183">True</span></span>                                                              |
| <span data-ttu-id="9b169-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b169-184">Is Indexed</span></span>             | <span data-ttu-id="9b169-185">False</span><span class="sxs-lookup"><span data-stu-id="9b169-185">False</span></span>                                                             |
| <span data-ttu-id="9b169-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b169-186">In Global Catalog</span></span>      | <span data-ttu-id="9b169-187">False</span><span class="sxs-lookup"><span data-stu-id="9b169-187">False</span></span>                                                             |
| <span data-ttu-id="9b169-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b169-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b169-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b169-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9b169-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b169-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b169-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-192">Search-Flags</span></span>           | <span data-ttu-id="9b169-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b169-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="9b169-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-194">System-Flags</span></span>           | <span data-ttu-id="9b169-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b169-195">0x00000010</span></span>                                                        |
| <span data-ttu-id="9b169-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b169-196">Classes used in</span></span>        | [<span data-ttu-id="9b169-197">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="9b169-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9b169-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b169-198">Windows Server 2008</span></span>



| <span data-ttu-id="9b169-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b169-199">Entry</span></span> | <span data-ttu-id="9b169-200">Value</span><span class="sxs-lookup"><span data-stu-id="9b169-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9b169-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b169-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b169-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b169-203">System-Only</span></span>            | <span data-ttu-id="9b169-204">False</span><span class="sxs-lookup"><span data-stu-id="9b169-204">False</span></span>                                                             |
| <span data-ttu-id="9b169-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b169-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9b169-206">True</span><span class="sxs-lookup"><span data-stu-id="9b169-206">True</span></span>                                                              |
| <span data-ttu-id="9b169-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b169-207">Is Indexed</span></span>             | <span data-ttu-id="9b169-208">False</span><span class="sxs-lookup"><span data-stu-id="9b169-208">False</span></span>                                                             |
| <span data-ttu-id="9b169-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b169-209">In Global Catalog</span></span>      | <span data-ttu-id="9b169-210">False</span><span class="sxs-lookup"><span data-stu-id="9b169-210">False</span></span>                                                             |
| <span data-ttu-id="9b169-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b169-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b169-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b169-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9b169-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b169-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b169-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-215">Search-Flags</span></span>           | <span data-ttu-id="9b169-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b169-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="9b169-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-217">System-Flags</span></span>           | <span data-ttu-id="9b169-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b169-218">0x00000010</span></span>                                                        |
| <span data-ttu-id="9b169-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b169-219">Classes used in</span></span>        | [<span data-ttu-id="9b169-220">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="9b169-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9b169-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b169-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9b169-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b169-222">Entry</span></span> | <span data-ttu-id="9b169-223">Value</span><span class="sxs-lookup"><span data-stu-id="9b169-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9b169-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b169-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b169-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b169-226">System-Only</span></span>            | <span data-ttu-id="9b169-227">False</span><span class="sxs-lookup"><span data-stu-id="9b169-227">False</span></span>                                                             |
| <span data-ttu-id="9b169-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b169-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9b169-229">True</span><span class="sxs-lookup"><span data-stu-id="9b169-229">True</span></span>                                                              |
| <span data-ttu-id="9b169-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b169-230">Is Indexed</span></span>             | <span data-ttu-id="9b169-231">False</span><span class="sxs-lookup"><span data-stu-id="9b169-231">False</span></span>                                                             |
| <span data-ttu-id="9b169-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b169-232">In Global Catalog</span></span>      | <span data-ttu-id="9b169-233">False</span><span class="sxs-lookup"><span data-stu-id="9b169-233">False</span></span>                                                             |
| <span data-ttu-id="9b169-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b169-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b169-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b169-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9b169-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b169-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b169-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-238">Search-Flags</span></span>           | <span data-ttu-id="9b169-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b169-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="9b169-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-240">System-Flags</span></span>           | <span data-ttu-id="9b169-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b169-241">0x00000010</span></span>                                                        |
| <span data-ttu-id="9b169-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b169-242">Classes used in</span></span>        | [<span data-ttu-id="9b169-243">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="9b169-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9b169-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b169-244">Windows Server 2012</span></span>



| <span data-ttu-id="9b169-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="9b169-245">Entry</span></span> | <span data-ttu-id="9b169-246">Value</span><span class="sxs-lookup"><span data-stu-id="9b169-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9b169-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9b169-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b169-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9b169-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b169-249">System-Only</span></span>            | <span data-ttu-id="9b169-250">False</span><span class="sxs-lookup"><span data-stu-id="9b169-250">False</span></span>                                                             |
| <span data-ttu-id="9b169-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9b169-251">Is-Single-Valued</span></span>       | <span data-ttu-id="9b169-252">True</span><span class="sxs-lookup"><span data-stu-id="9b169-252">True</span></span>                                                              |
| <span data-ttu-id="9b169-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9b169-253">Is Indexed</span></span>             | <span data-ttu-id="9b169-254">False</span><span class="sxs-lookup"><span data-stu-id="9b169-254">False</span></span>                                                             |
| <span data-ttu-id="9b169-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9b169-255">In Global Catalog</span></span>      | <span data-ttu-id="9b169-256">False</span><span class="sxs-lookup"><span data-stu-id="9b169-256">False</span></span>                                                             |
| <span data-ttu-id="9b169-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9b169-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b169-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9b169-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9b169-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b169-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b169-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9b169-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-261">Search-Flags</span></span>           | <span data-ttu-id="9b169-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9b169-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="9b169-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b169-263">System-Flags</span></span>           | <span data-ttu-id="9b169-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b169-264">0x00000010</span></span>                                                        |
| <span data-ttu-id="9b169-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9b169-265">Classes used in</span></span>        | [<span data-ttu-id="9b169-266">**Contenedor de Microsoft-DS-quota**</span><span class="sxs-lookup"><span data-stu-id="9b169-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 






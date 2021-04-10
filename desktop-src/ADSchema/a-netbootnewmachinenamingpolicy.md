---
title: netboot-New-Machine-naming-atributo de Directiva
description: Indica el esquema de nomenclatura que utilizarán las nuevas cuentas de equipo cliente.
ms.assetid: e8ffc9b1-b2a2-4216-8498-85cb6c8cc7ae
ms.tgt_platform: multiple
keywords:
- netboot-New-Machine-naming-esquema de AD de atributo de Directiva
- netbootNewMachineNamingPolicy esquema de AD de atributos
topic_type:
- apiref
api_name:
- netboot-New-Machine-Naming-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da6cb51ced16da6510f3fb85ec80e4fa641603b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151748"
---
# <a name="netboot-new-machine-naming-policy-attribute"></a><span data-ttu-id="d2f9e-105">netboot-New-Machine-naming-atributo de Directiva</span><span class="sxs-lookup"><span data-stu-id="d2f9e-105">netboot-New-Machine-Naming-Policy attribute</span></span>

<span data-ttu-id="d2f9e-106">Indica el esquema de nomenclatura que utilizarán las nuevas cuentas de equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="d2f9e-106">Indicates the naming scheme which new client computer accounts will use.</span></span>



| <span data-ttu-id="d2f9e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d2f9e-107">Entry</span></span> | <span data-ttu-id="d2f9e-108">Value</span><span class="sxs-lookup"><span data-stu-id="d2f9e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d2f9e-109">CN</span><span class="sxs-lookup"><span data-stu-id="d2f9e-109">CN</span></span>                | <span data-ttu-id="d2f9e-110">netboot-New-Machine-naming-Policy</span><span class="sxs-lookup"><span data-stu-id="d2f9e-110">netboot-New-Machine-Naming-Policy</span></span>           |
| <span data-ttu-id="d2f9e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d2f9e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d2f9e-112">netbootNewMachineNamingPolicy</span><span class="sxs-lookup"><span data-stu-id="d2f9e-112">netbootNewMachineNamingPolicy</span></span>               |
| <span data-ttu-id="d2f9e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d2f9e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d2f9e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d2f9e-114">Update Privilege</span></span>  | <span data-ttu-id="d2f9e-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="d2f9e-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="d2f9e-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d2f9e-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d2f9e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d2f9e-117">Attribute-Id</span></span>      | <span data-ttu-id="d2f9e-118">1.2.840.113556.1.4.855</span><span class="sxs-lookup"><span data-stu-id="d2f9e-118">1.2.840.113556.1.4.855</span></span>                      |
| <span data-ttu-id="d2f9e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d2f9e-119">System-Id-Guid</span></span>    | <span data-ttu-id="d2f9e-120">0738307c-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d2f9e-120">0738307c-91df-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="d2f9e-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2f9e-121">Syntax</span></span>            | [<span data-ttu-id="d2f9e-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d2f9e-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d2f9e-123">Implementations</span></span>

-   [<span data-ttu-id="d2f9e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d2f9e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d2f9e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d2f9e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d2f9e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d2f9e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d2f9e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2f9e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d2f9e-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="d2f9e-131">Entry</span></span> | <span data-ttu-id="d2f9e-132">Value</span><span class="sxs-lookup"><span data-stu-id="d2f9e-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2f9e-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d2f9e-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f9e-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f9e-135">System-Only</span></span>            | <span data-ttu-id="d2f9e-136">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-136">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d2f9e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f9e-138">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-138">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d2f9e-139">Is Indexed</span></span>             | <span data-ttu-id="d2f9e-140">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-140">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d2f9e-141">In Global Catalog</span></span>      | <span data-ttu-id="d2f9e-142">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-142">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d2f9e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f9e-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2f9e-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d2f9e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f9e-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f9e-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-147">Search-Flags</span></span>           | <span data-ttu-id="d2f9e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f9e-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="d2f9e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-149">System-Flags</span></span>           | <span data-ttu-id="d2f9e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f9e-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="d2f9e-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d2f9e-151">Classes used in</span></span>        | [<span data-ttu-id="d2f9e-152">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d2f9e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2f9e-153">Windows Server 2003</span></span>



| <span data-ttu-id="d2f9e-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="d2f9e-154">Entry</span></span> | <span data-ttu-id="d2f9e-155">Value</span><span class="sxs-lookup"><span data-stu-id="d2f9e-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2f9e-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d2f9e-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f9e-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f9e-158">System-Only</span></span>            | <span data-ttu-id="d2f9e-159">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-159">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d2f9e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f9e-161">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-161">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d2f9e-162">Is Indexed</span></span>             | <span data-ttu-id="d2f9e-163">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-163">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d2f9e-164">In Global Catalog</span></span>      | <span data-ttu-id="d2f9e-165">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-165">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d2f9e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f9e-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2f9e-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d2f9e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f9e-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f9e-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-170">Search-Flags</span></span>           | <span data-ttu-id="d2f9e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f9e-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="d2f9e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-172">System-Flags</span></span>           | <span data-ttu-id="d2f9e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f9e-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="d2f9e-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d2f9e-174">Classes used in</span></span>        | [<span data-ttu-id="d2f9e-175">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d2f9e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d2f9e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d2f9e-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="d2f9e-177">Entry</span></span> | <span data-ttu-id="d2f9e-178">Value</span><span class="sxs-lookup"><span data-stu-id="d2f9e-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2f9e-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d2f9e-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f9e-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f9e-181">System-Only</span></span>            | <span data-ttu-id="d2f9e-182">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-182">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d2f9e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f9e-184">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-184">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d2f9e-185">Is Indexed</span></span>             | <span data-ttu-id="d2f9e-186">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-186">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d2f9e-187">In Global Catalog</span></span>      | <span data-ttu-id="d2f9e-188">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-188">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d2f9e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f9e-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2f9e-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d2f9e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f9e-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f9e-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-193">Search-Flags</span></span>           | <span data-ttu-id="d2f9e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f9e-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="d2f9e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-195">System-Flags</span></span>           | <span data-ttu-id="d2f9e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f9e-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="d2f9e-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d2f9e-197">Classes used in</span></span>        | [<span data-ttu-id="d2f9e-198">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d2f9e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2f9e-199">Windows Server 2008</span></span>



| <span data-ttu-id="d2f9e-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="d2f9e-200">Entry</span></span> | <span data-ttu-id="d2f9e-201">Value</span><span class="sxs-lookup"><span data-stu-id="d2f9e-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2f9e-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d2f9e-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f9e-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f9e-204">System-Only</span></span>            | <span data-ttu-id="d2f9e-205">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-205">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d2f9e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f9e-207">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-207">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d2f9e-208">Is Indexed</span></span>             | <span data-ttu-id="d2f9e-209">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-209">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d2f9e-210">In Global Catalog</span></span>      | <span data-ttu-id="d2f9e-211">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-211">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d2f9e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f9e-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2f9e-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d2f9e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f9e-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f9e-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-216">Search-Flags</span></span>           | <span data-ttu-id="d2f9e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f9e-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="d2f9e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-218">System-Flags</span></span>           | <span data-ttu-id="d2f9e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f9e-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="d2f9e-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d2f9e-220">Classes used in</span></span>        | [<span data-ttu-id="d2f9e-221">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d2f9e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2f9e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d2f9e-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="d2f9e-223">Entry</span></span> | <span data-ttu-id="d2f9e-224">Value</span><span class="sxs-lookup"><span data-stu-id="d2f9e-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2f9e-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d2f9e-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f9e-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f9e-227">System-Only</span></span>            | <span data-ttu-id="d2f9e-228">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-228">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d2f9e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f9e-230">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-230">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d2f9e-231">Is Indexed</span></span>             | <span data-ttu-id="d2f9e-232">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-232">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d2f9e-233">In Global Catalog</span></span>      | <span data-ttu-id="d2f9e-234">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-234">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d2f9e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f9e-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2f9e-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d2f9e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f9e-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f9e-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-239">Search-Flags</span></span>           | <span data-ttu-id="d2f9e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f9e-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="d2f9e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-241">System-Flags</span></span>           | <span data-ttu-id="d2f9e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f9e-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="d2f9e-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d2f9e-243">Classes used in</span></span>        | [<span data-ttu-id="d2f9e-244">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d2f9e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2f9e-245">Windows Server 2012</span></span>



| <span data-ttu-id="d2f9e-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="d2f9e-246">Entry</span></span> | <span data-ttu-id="d2f9e-247">Value</span><span class="sxs-lookup"><span data-stu-id="d2f9e-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2f9e-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d2f9e-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d2f9e-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d2f9e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d2f9e-250">System-Only</span></span>            | <span data-ttu-id="d2f9e-251">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-251">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d2f9e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d2f9e-253">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-253">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d2f9e-254">Is Indexed</span></span>             | <span data-ttu-id="d2f9e-255">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-255">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d2f9e-256">In Global Catalog</span></span>      | <span data-ttu-id="d2f9e-257">False</span><span class="sxs-lookup"><span data-stu-id="d2f9e-257">False</span></span>                                                      |
| <span data-ttu-id="d2f9e-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d2f9e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d2f9e-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d2f9e-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d2f9e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d2f9e-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d2f9e-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d2f9e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-262">Search-Flags</span></span>           | <span data-ttu-id="d2f9e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d2f9e-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="d2f9e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d2f9e-264">System-Flags</span></span>           | <span data-ttu-id="d2f9e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d2f9e-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="d2f9e-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d2f9e-266">Classes used in</span></span>        | [<span data-ttu-id="d2f9e-267">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="d2f9e-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 






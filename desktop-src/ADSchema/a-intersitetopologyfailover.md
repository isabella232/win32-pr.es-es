---
title: 'Inter-site-Topology: atributo de conmutación por error'
description: Indica cuánto tiempo debe transcurrir desde la última conexión de mantenimiento para que el generador de topología entre sitios se considere inactivo.
ms.assetid: d351dbec-d5a3-46e1-87a9-0856d19e07c6
ms.tgt_platform: multiple
keywords:
- 'Inter-site-Topology: esquema de AD de atributos de conmutación por error'
- interSiteTopologyFailover esquema de AD de atributos
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Failover
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4e9cad98bade7fd69178a8fce795d0b92f35b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493894"
---
# <a name="inter-site-topology-failover-attribute"></a><span data-ttu-id="942a4-105">Inter-site-Topology: atributo de conmutación por error</span><span class="sxs-lookup"><span data-stu-id="942a4-105">Inter-Site-Topology-Failover attribute</span></span>

<span data-ttu-id="942a4-106">Indica cuánto tiempo debe transcurrir desde la última conexión de mantenimiento para que el generador de topología entre sitios se considere inactivo.</span><span class="sxs-lookup"><span data-stu-id="942a4-106">Indicates how much time must transpire since the last keep-alive for the inter-site topology generator to be considered dead.</span></span>



| <span data-ttu-id="942a4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="942a4-107">Entry</span></span> | <span data-ttu-id="942a4-108">Value</span><span class="sxs-lookup"><span data-stu-id="942a4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="942a4-109">CN</span><span class="sxs-lookup"><span data-stu-id="942a4-109">CN</span></span>                | <span data-ttu-id="942a4-110">Entre sitios: topología: conmutación por error</span><span class="sxs-lookup"><span data-stu-id="942a4-110">Inter-Site-Topology-Failover</span></span>         |
| <span data-ttu-id="942a4-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="942a4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="942a4-112">interSiteTopologyFailover</span><span class="sxs-lookup"><span data-stu-id="942a4-112">interSiteTopologyFailover</span></span>            |
| <span data-ttu-id="942a4-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="942a4-113">Size</span></span>              | <span data-ttu-id="942a4-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="942a4-114">4 bytes</span></span>                              |
| <span data-ttu-id="942a4-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="942a4-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="942a4-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="942a4-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="942a4-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="942a4-117">Attribute-Id</span></span>      | <span data-ttu-id="942a4-118">1.2.840.113556.1.4.1248</span><span class="sxs-lookup"><span data-stu-id="942a4-118">1.2.840.113556.1.4.1248</span></span>              |
| <span data-ttu-id="942a4-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="942a4-119">System-Id-Guid</span></span>    | <span data-ttu-id="942a4-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="942a4-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="942a4-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="942a4-121">Syntax</span></span>            | [<span data-ttu-id="942a4-122">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="942a4-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="942a4-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="942a4-123">Implementations</span></span>

-   [<span data-ttu-id="942a4-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="942a4-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="942a4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="942a4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="942a4-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="942a4-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="942a4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="942a4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="942a4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="942a4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="942a4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="942a4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="942a4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="942a4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="942a4-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="942a4-131">Windows 2000 Server</span></span>



| <span data-ttu-id="942a4-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="942a4-132">Entry</span></span> | <span data-ttu-id="942a4-133">Value</span><span class="sxs-lookup"><span data-stu-id="942a4-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="942a4-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="942a4-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="942a4-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="942a4-136">System-Only</span></span>            | <span data-ttu-id="942a4-137">False</span><span class="sxs-lookup"><span data-stu-id="942a4-137">False</span></span>                                                       |
| <span data-ttu-id="942a4-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="942a4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="942a4-139">True</span><span class="sxs-lookup"><span data-stu-id="942a4-139">True</span></span>                                                        |
| <span data-ttu-id="942a4-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="942a4-140">Is Indexed</span></span>             | <span data-ttu-id="942a4-141">False</span><span class="sxs-lookup"><span data-stu-id="942a4-141">False</span></span>                                                       |
| <span data-ttu-id="942a4-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="942a4-142">In Global Catalog</span></span>      | <span data-ttu-id="942a4-143">False</span><span class="sxs-lookup"><span data-stu-id="942a4-143">False</span></span>                                                       |
| <span data-ttu-id="942a4-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="942a4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="942a4-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="942a4-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="942a4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="942a4-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="942a4-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-148">Search-Flags</span></span>           | <span data-ttu-id="942a4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="942a4-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="942a4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-150">System-Flags</span></span>           | <span data-ttu-id="942a4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="942a4-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="942a4-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="942a4-152">Classes used in</span></span>        | [<span data-ttu-id="942a4-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="942a4-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="942a4-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="942a4-154">Windows Server 2003</span></span>



| <span data-ttu-id="942a4-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="942a4-155">Entry</span></span> | <span data-ttu-id="942a4-156">Value</span><span class="sxs-lookup"><span data-stu-id="942a4-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="942a4-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="942a4-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="942a4-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="942a4-159">System-Only</span></span>            | <span data-ttu-id="942a4-160">False</span><span class="sxs-lookup"><span data-stu-id="942a4-160">False</span></span>                                                       |
| <span data-ttu-id="942a4-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="942a4-161">Is-Single-Valued</span></span>       | <span data-ttu-id="942a4-162">True</span><span class="sxs-lookup"><span data-stu-id="942a4-162">True</span></span>                                                        |
| <span data-ttu-id="942a4-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="942a4-163">Is Indexed</span></span>             | <span data-ttu-id="942a4-164">False</span><span class="sxs-lookup"><span data-stu-id="942a4-164">False</span></span>                                                       |
| <span data-ttu-id="942a4-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="942a4-165">In Global Catalog</span></span>      | <span data-ttu-id="942a4-166">False</span><span class="sxs-lookup"><span data-stu-id="942a4-166">False</span></span>                                                       |
| <span data-ttu-id="942a4-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="942a4-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="942a4-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="942a4-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="942a4-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="942a4-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="942a4-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-171">Search-Flags</span></span>           | <span data-ttu-id="942a4-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="942a4-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="942a4-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-173">System-Flags</span></span>           | <span data-ttu-id="942a4-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="942a4-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="942a4-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="942a4-175">Classes used in</span></span>        | [<span data-ttu-id="942a4-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="942a4-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="942a4-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="942a4-177">ADAM</span></span>



| <span data-ttu-id="942a4-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="942a4-178">Entry</span></span> | <span data-ttu-id="942a4-179">Value</span><span class="sxs-lookup"><span data-stu-id="942a4-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="942a4-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="942a4-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="942a4-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="942a4-182">System-Only</span></span>            | <span data-ttu-id="942a4-183">False</span><span class="sxs-lookup"><span data-stu-id="942a4-183">False</span></span>                                                       |
| <span data-ttu-id="942a4-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="942a4-184">Is-Single-Valued</span></span>       | <span data-ttu-id="942a4-185">True</span><span class="sxs-lookup"><span data-stu-id="942a4-185">True</span></span>                                                        |
| <span data-ttu-id="942a4-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="942a4-186">Is Indexed</span></span>             | <span data-ttu-id="942a4-187">False</span><span class="sxs-lookup"><span data-stu-id="942a4-187">False</span></span>                                                       |
| <span data-ttu-id="942a4-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="942a4-188">In Global Catalog</span></span>      | <span data-ttu-id="942a4-189">False</span><span class="sxs-lookup"><span data-stu-id="942a4-189">False</span></span>                                                       |
| <span data-ttu-id="942a4-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="942a4-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="942a4-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="942a4-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="942a4-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="942a4-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="942a4-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-194">Search-Flags</span></span>           | <span data-ttu-id="942a4-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="942a4-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="942a4-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-196">System-Flags</span></span>           | <span data-ttu-id="942a4-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="942a4-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="942a4-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="942a4-198">Classes used in</span></span>        | [<span data-ttu-id="942a4-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="942a4-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="942a4-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="942a4-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="942a4-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="942a4-201">Entry</span></span> | <span data-ttu-id="942a4-202">Value</span><span class="sxs-lookup"><span data-stu-id="942a4-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="942a4-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="942a4-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="942a4-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="942a4-205">System-Only</span></span>            | <span data-ttu-id="942a4-206">False</span><span class="sxs-lookup"><span data-stu-id="942a4-206">False</span></span>                                                       |
| <span data-ttu-id="942a4-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="942a4-207">Is-Single-Valued</span></span>       | <span data-ttu-id="942a4-208">True</span><span class="sxs-lookup"><span data-stu-id="942a4-208">True</span></span>                                                        |
| <span data-ttu-id="942a4-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="942a4-209">Is Indexed</span></span>             | <span data-ttu-id="942a4-210">False</span><span class="sxs-lookup"><span data-stu-id="942a4-210">False</span></span>                                                       |
| <span data-ttu-id="942a4-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="942a4-211">In Global Catalog</span></span>      | <span data-ttu-id="942a4-212">False</span><span class="sxs-lookup"><span data-stu-id="942a4-212">False</span></span>                                                       |
| <span data-ttu-id="942a4-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="942a4-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="942a4-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="942a4-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="942a4-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="942a4-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="942a4-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-217">Search-Flags</span></span>           | <span data-ttu-id="942a4-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="942a4-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="942a4-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-219">System-Flags</span></span>           | <span data-ttu-id="942a4-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="942a4-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="942a4-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="942a4-221">Classes used in</span></span>        | [<span data-ttu-id="942a4-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="942a4-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="942a4-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="942a4-223">Windows Server 2008</span></span>



| <span data-ttu-id="942a4-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="942a4-224">Entry</span></span> | <span data-ttu-id="942a4-225">Value</span><span class="sxs-lookup"><span data-stu-id="942a4-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="942a4-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="942a4-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="942a4-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="942a4-228">System-Only</span></span>            | <span data-ttu-id="942a4-229">False</span><span class="sxs-lookup"><span data-stu-id="942a4-229">False</span></span>                                                       |
| <span data-ttu-id="942a4-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="942a4-230">Is-Single-Valued</span></span>       | <span data-ttu-id="942a4-231">True</span><span class="sxs-lookup"><span data-stu-id="942a4-231">True</span></span>                                                        |
| <span data-ttu-id="942a4-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="942a4-232">Is Indexed</span></span>             | <span data-ttu-id="942a4-233">False</span><span class="sxs-lookup"><span data-stu-id="942a4-233">False</span></span>                                                       |
| <span data-ttu-id="942a4-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="942a4-234">In Global Catalog</span></span>      | <span data-ttu-id="942a4-235">False</span><span class="sxs-lookup"><span data-stu-id="942a4-235">False</span></span>                                                       |
| <span data-ttu-id="942a4-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="942a4-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="942a4-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="942a4-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="942a4-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="942a4-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="942a4-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-240">Search-Flags</span></span>           | <span data-ttu-id="942a4-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="942a4-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="942a4-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-242">System-Flags</span></span>           | <span data-ttu-id="942a4-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="942a4-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="942a4-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="942a4-244">Classes used in</span></span>        | [<span data-ttu-id="942a4-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="942a4-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="942a4-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="942a4-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="942a4-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="942a4-247">Entry</span></span> | <span data-ttu-id="942a4-248">Value</span><span class="sxs-lookup"><span data-stu-id="942a4-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="942a4-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="942a4-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="942a4-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="942a4-251">System-Only</span></span>            | <span data-ttu-id="942a4-252">False</span><span class="sxs-lookup"><span data-stu-id="942a4-252">False</span></span>                                                       |
| <span data-ttu-id="942a4-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="942a4-253">Is-Single-Valued</span></span>       | <span data-ttu-id="942a4-254">True</span><span class="sxs-lookup"><span data-stu-id="942a4-254">True</span></span>                                                        |
| <span data-ttu-id="942a4-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="942a4-255">Is Indexed</span></span>             | <span data-ttu-id="942a4-256">False</span><span class="sxs-lookup"><span data-stu-id="942a4-256">False</span></span>                                                       |
| <span data-ttu-id="942a4-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="942a4-257">In Global Catalog</span></span>      | <span data-ttu-id="942a4-258">False</span><span class="sxs-lookup"><span data-stu-id="942a4-258">False</span></span>                                                       |
| <span data-ttu-id="942a4-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="942a4-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="942a4-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="942a4-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="942a4-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="942a4-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="942a4-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-263">Search-Flags</span></span>           | <span data-ttu-id="942a4-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="942a4-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="942a4-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-265">System-Flags</span></span>           | <span data-ttu-id="942a4-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="942a4-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="942a4-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="942a4-267">Classes used in</span></span>        | [<span data-ttu-id="942a4-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="942a4-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="942a4-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="942a4-269">Windows Server 2012</span></span>



| <span data-ttu-id="942a4-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="942a4-270">Entry</span></span> | <span data-ttu-id="942a4-271">Value</span><span class="sxs-lookup"><span data-stu-id="942a4-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="942a4-272">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="942a4-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="942a4-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="942a4-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="942a4-274">System-Only</span></span>            | <span data-ttu-id="942a4-275">False</span><span class="sxs-lookup"><span data-stu-id="942a4-275">False</span></span>                                                       |
| <span data-ttu-id="942a4-276">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="942a4-276">Is-Single-Valued</span></span>       | <span data-ttu-id="942a4-277">True</span><span class="sxs-lookup"><span data-stu-id="942a4-277">True</span></span>                                                        |
| <span data-ttu-id="942a4-278">Está indexado</span><span class="sxs-lookup"><span data-stu-id="942a4-278">Is Indexed</span></span>             | <span data-ttu-id="942a4-279">False</span><span class="sxs-lookup"><span data-stu-id="942a4-279">False</span></span>                                                       |
| <span data-ttu-id="942a4-280">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="942a4-280">In Global Catalog</span></span>      | <span data-ttu-id="942a4-281">False</span><span class="sxs-lookup"><span data-stu-id="942a4-281">False</span></span>                                                       |
| <span data-ttu-id="942a4-282">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="942a4-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="942a4-283">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="942a4-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="942a4-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="942a4-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="942a4-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="942a4-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-286">Search-Flags</span></span>           | <span data-ttu-id="942a4-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="942a4-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="942a4-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="942a4-288">System-Flags</span></span>           | <span data-ttu-id="942a4-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="942a4-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="942a4-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="942a4-290">Classes used in</span></span>        | [<span data-ttu-id="942a4-291">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="942a4-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 






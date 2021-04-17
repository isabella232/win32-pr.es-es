---
title: 'Inter-site-Topology: renovar atributo'
description: Esta clase indica la frecuencia con la que el generador de topología entre sitios actualiza el mensaje Keep-Alive que se envía a los controladores de dominio contenidos en el mismo sitio.
ms.assetid: 523d8161-0678-482f-8d66-55a112995fe5
ms.tgt_platform: multiple
keywords:
- 'Inter-site-Topology: renueve atributo AD Schema'
- interSiteTopologyRenew esquema de AD de atributos
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Renew
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821bd294f777fd29738ff102955cd170a42205e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658950"
---
# <a name="inter-site-topology-renew-attribute"></a><span data-ttu-id="b4526-105">Inter-site-Topology: renovar atributo</span><span class="sxs-lookup"><span data-stu-id="b4526-105">Inter-Site-Topology-Renew attribute</span></span>

<span data-ttu-id="b4526-106">Esta clase indica la frecuencia con la que el generador de topología entre sitios actualiza el mensaje Keep-Alive que se envía a los controladores de dominio contenidos en el mismo sitio.</span><span class="sxs-lookup"><span data-stu-id="b4526-106">This class indicates how often the intersite topology generator updates the keep-alive message that is sent to domain controllers contained in the same site.</span></span>



| <span data-ttu-id="b4526-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4526-107">Entry</span></span> | <span data-ttu-id="b4526-108">Value</span><span class="sxs-lookup"><span data-stu-id="b4526-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b4526-109">CN</span><span class="sxs-lookup"><span data-stu-id="b4526-109">CN</span></span>                | <span data-ttu-id="b4526-110">Entre sitios-topología: renovación</span><span class="sxs-lookup"><span data-stu-id="b4526-110">Inter-Site-Topology-Renew</span></span>            |
| <span data-ttu-id="b4526-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b4526-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b4526-112">interSiteTopologyRenew</span><span class="sxs-lookup"><span data-stu-id="b4526-112">interSiteTopologyRenew</span></span>               |
| <span data-ttu-id="b4526-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b4526-113">Size</span></span>              | <span data-ttu-id="b4526-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="b4526-114">4 bytes</span></span>                              |
| <span data-ttu-id="b4526-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b4526-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b4526-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b4526-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b4526-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4526-117">Attribute-Id</span></span>      | <span data-ttu-id="b4526-118">1.2.840.113556.1.4.1247</span><span class="sxs-lookup"><span data-stu-id="b4526-118">1.2.840.113556.1.4.1247</span></span>              |
| <span data-ttu-id="b4526-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b4526-119">System-Id-Guid</span></span>    | <span data-ttu-id="b4526-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="b4526-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="b4526-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4526-121">Syntax</span></span>            | [<span data-ttu-id="b4526-122">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="b4526-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b4526-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b4526-123">Implementations</span></span>

-   [<span data-ttu-id="b4526-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4526-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4526-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4526-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4526-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b4526-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b4526-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4526-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4526-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4526-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4526-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4526-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4526-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4526-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4526-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4526-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b4526-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4526-132">Entry</span></span> | <span data-ttu-id="b4526-133">Value</span><span class="sxs-lookup"><span data-stu-id="b4526-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b4526-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b4526-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4526-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4526-136">System-Only</span></span>            | <span data-ttu-id="b4526-137">False</span><span class="sxs-lookup"><span data-stu-id="b4526-137">False</span></span>                                                       |
| <span data-ttu-id="b4526-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b4526-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b4526-139">True</span><span class="sxs-lookup"><span data-stu-id="b4526-139">True</span></span>                                                        |
| <span data-ttu-id="b4526-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b4526-140">Is Indexed</span></span>             | <span data-ttu-id="b4526-141">False</span><span class="sxs-lookup"><span data-stu-id="b4526-141">False</span></span>                                                       |
| <span data-ttu-id="b4526-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b4526-142">In Global Catalog</span></span>      | <span data-ttu-id="b4526-143">False</span><span class="sxs-lookup"><span data-stu-id="b4526-143">False</span></span>                                                       |
| <span data-ttu-id="b4526-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b4526-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4526-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4526-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="b4526-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4526-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4526-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-148">Search-Flags</span></span>           | <span data-ttu-id="b4526-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4526-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="b4526-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-150">System-Flags</span></span>           | <span data-ttu-id="b4526-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4526-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="b4526-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b4526-152">Classes used in</span></span>        | [<span data-ttu-id="b4526-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="b4526-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4526-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4526-154">Windows Server 2003</span></span>



| <span data-ttu-id="b4526-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4526-155">Entry</span></span> | <span data-ttu-id="b4526-156">Value</span><span class="sxs-lookup"><span data-stu-id="b4526-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b4526-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b4526-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4526-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4526-159">System-Only</span></span>            | <span data-ttu-id="b4526-160">False</span><span class="sxs-lookup"><span data-stu-id="b4526-160">False</span></span>                                                       |
| <span data-ttu-id="b4526-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b4526-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b4526-162">True</span><span class="sxs-lookup"><span data-stu-id="b4526-162">True</span></span>                                                        |
| <span data-ttu-id="b4526-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b4526-163">Is Indexed</span></span>             | <span data-ttu-id="b4526-164">False</span><span class="sxs-lookup"><span data-stu-id="b4526-164">False</span></span>                                                       |
| <span data-ttu-id="b4526-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b4526-165">In Global Catalog</span></span>      | <span data-ttu-id="b4526-166">False</span><span class="sxs-lookup"><span data-stu-id="b4526-166">False</span></span>                                                       |
| <span data-ttu-id="b4526-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b4526-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4526-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4526-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="b4526-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4526-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4526-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-171">Search-Flags</span></span>           | <span data-ttu-id="b4526-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4526-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="b4526-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-173">System-Flags</span></span>           | <span data-ttu-id="b4526-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4526-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="b4526-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b4526-175">Classes used in</span></span>        | [<span data-ttu-id="b4526-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="b4526-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b4526-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="b4526-177">ADAM</span></span>



| <span data-ttu-id="b4526-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4526-178">Entry</span></span> | <span data-ttu-id="b4526-179">Value</span><span class="sxs-lookup"><span data-stu-id="b4526-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b4526-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b4526-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4526-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4526-182">System-Only</span></span>            | <span data-ttu-id="b4526-183">False</span><span class="sxs-lookup"><span data-stu-id="b4526-183">False</span></span>                                                       |
| <span data-ttu-id="b4526-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b4526-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b4526-185">True</span><span class="sxs-lookup"><span data-stu-id="b4526-185">True</span></span>                                                        |
| <span data-ttu-id="b4526-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b4526-186">Is Indexed</span></span>             | <span data-ttu-id="b4526-187">False</span><span class="sxs-lookup"><span data-stu-id="b4526-187">False</span></span>                                                       |
| <span data-ttu-id="b4526-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b4526-188">In Global Catalog</span></span>      | <span data-ttu-id="b4526-189">False</span><span class="sxs-lookup"><span data-stu-id="b4526-189">False</span></span>                                                       |
| <span data-ttu-id="b4526-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b4526-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4526-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4526-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="b4526-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4526-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4526-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-194">Search-Flags</span></span>           | <span data-ttu-id="b4526-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4526-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="b4526-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-196">System-Flags</span></span>           | <span data-ttu-id="b4526-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4526-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="b4526-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b4526-198">Classes used in</span></span>        | [<span data-ttu-id="b4526-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="b4526-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4526-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4526-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4526-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4526-201">Entry</span></span> | <span data-ttu-id="b4526-202">Value</span><span class="sxs-lookup"><span data-stu-id="b4526-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b4526-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b4526-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4526-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4526-205">System-Only</span></span>            | <span data-ttu-id="b4526-206">False</span><span class="sxs-lookup"><span data-stu-id="b4526-206">False</span></span>                                                       |
| <span data-ttu-id="b4526-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b4526-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b4526-208">True</span><span class="sxs-lookup"><span data-stu-id="b4526-208">True</span></span>                                                        |
| <span data-ttu-id="b4526-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b4526-209">Is Indexed</span></span>             | <span data-ttu-id="b4526-210">False</span><span class="sxs-lookup"><span data-stu-id="b4526-210">False</span></span>                                                       |
| <span data-ttu-id="b4526-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b4526-211">In Global Catalog</span></span>      | <span data-ttu-id="b4526-212">False</span><span class="sxs-lookup"><span data-stu-id="b4526-212">False</span></span>                                                       |
| <span data-ttu-id="b4526-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b4526-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4526-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4526-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="b4526-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4526-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4526-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-217">Search-Flags</span></span>           | <span data-ttu-id="b4526-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4526-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="b4526-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-219">System-Flags</span></span>           | <span data-ttu-id="b4526-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4526-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="b4526-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b4526-221">Classes used in</span></span>        | [<span data-ttu-id="b4526-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="b4526-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4526-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4526-223">Windows Server 2008</span></span>



| <span data-ttu-id="b4526-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4526-224">Entry</span></span> | <span data-ttu-id="b4526-225">Value</span><span class="sxs-lookup"><span data-stu-id="b4526-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b4526-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b4526-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4526-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4526-228">System-Only</span></span>            | <span data-ttu-id="b4526-229">False</span><span class="sxs-lookup"><span data-stu-id="b4526-229">False</span></span>                                                       |
| <span data-ttu-id="b4526-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b4526-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b4526-231">True</span><span class="sxs-lookup"><span data-stu-id="b4526-231">True</span></span>                                                        |
| <span data-ttu-id="b4526-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b4526-232">Is Indexed</span></span>             | <span data-ttu-id="b4526-233">False</span><span class="sxs-lookup"><span data-stu-id="b4526-233">False</span></span>                                                       |
| <span data-ttu-id="b4526-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b4526-234">In Global Catalog</span></span>      | <span data-ttu-id="b4526-235">False</span><span class="sxs-lookup"><span data-stu-id="b4526-235">False</span></span>                                                       |
| <span data-ttu-id="b4526-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b4526-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4526-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4526-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="b4526-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4526-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4526-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-240">Search-Flags</span></span>           | <span data-ttu-id="b4526-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4526-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="b4526-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-242">System-Flags</span></span>           | <span data-ttu-id="b4526-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4526-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="b4526-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b4526-244">Classes used in</span></span>        | [<span data-ttu-id="b4526-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="b4526-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4526-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4526-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4526-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4526-247">Entry</span></span> | <span data-ttu-id="b4526-248">Value</span><span class="sxs-lookup"><span data-stu-id="b4526-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b4526-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b4526-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4526-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4526-251">System-Only</span></span>            | <span data-ttu-id="b4526-252">False</span><span class="sxs-lookup"><span data-stu-id="b4526-252">False</span></span>                                                       |
| <span data-ttu-id="b4526-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b4526-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b4526-254">True</span><span class="sxs-lookup"><span data-stu-id="b4526-254">True</span></span>                                                        |
| <span data-ttu-id="b4526-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b4526-255">Is Indexed</span></span>             | <span data-ttu-id="b4526-256">False</span><span class="sxs-lookup"><span data-stu-id="b4526-256">False</span></span>                                                       |
| <span data-ttu-id="b4526-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b4526-257">In Global Catalog</span></span>      | <span data-ttu-id="b4526-258">False</span><span class="sxs-lookup"><span data-stu-id="b4526-258">False</span></span>                                                       |
| <span data-ttu-id="b4526-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b4526-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4526-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4526-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="b4526-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4526-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4526-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-263">Search-Flags</span></span>           | <span data-ttu-id="b4526-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4526-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="b4526-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-265">System-Flags</span></span>           | <span data-ttu-id="b4526-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4526-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="b4526-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b4526-267">Classes used in</span></span>        | [<span data-ttu-id="b4526-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="b4526-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4526-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4526-269">Windows Server 2012</span></span>



| <span data-ttu-id="b4526-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="b4526-270">Entry</span></span> | <span data-ttu-id="b4526-271">Value</span><span class="sxs-lookup"><span data-stu-id="b4526-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b4526-272">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b4526-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4526-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="b4526-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4526-274">System-Only</span></span>            | <span data-ttu-id="b4526-275">False</span><span class="sxs-lookup"><span data-stu-id="b4526-275">False</span></span>                                                       |
| <span data-ttu-id="b4526-276">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b4526-276">Is-Single-Valued</span></span>       | <span data-ttu-id="b4526-277">True</span><span class="sxs-lookup"><span data-stu-id="b4526-277">True</span></span>                                                        |
| <span data-ttu-id="b4526-278">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b4526-278">Is Indexed</span></span>             | <span data-ttu-id="b4526-279">False</span><span class="sxs-lookup"><span data-stu-id="b4526-279">False</span></span>                                                       |
| <span data-ttu-id="b4526-280">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b4526-280">In Global Catalog</span></span>      | <span data-ttu-id="b4526-281">False</span><span class="sxs-lookup"><span data-stu-id="b4526-281">False</span></span>                                                       |
| <span data-ttu-id="b4526-282">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b4526-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4526-283">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4526-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="b4526-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4526-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4526-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="b4526-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-286">Search-Flags</span></span>           | <span data-ttu-id="b4526-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4526-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="b4526-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4526-288">System-Flags</span></span>           | <span data-ttu-id="b4526-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b4526-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="b4526-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b4526-290">Classes used in</span></span>        | [<span data-ttu-id="b4526-291">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="b4526-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 






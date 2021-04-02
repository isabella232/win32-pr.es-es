---
title: 'Inter-site-Topology: atributo generator'
description: Este atributo se usará para admitir la conmutación por error para el equipo designado como el que ejecuta la generación de topología entre sitios del comprobador de coherencia de la información en un sitio determinado.
ms.assetid: 077f4331-ead9-4f17-942e-d55cf253d03b
ms.tgt_platform: multiple
keywords:
- El esquema de AD de atributo de generador de topología entre sitios
- interSiteTopologyGenerator esquema de AD de atributos
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Generator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7b354d05e882373715e4c49498c9daff41652
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151401"
---
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="6859d-105">Inter-site-Topology: atributo generator</span><span class="sxs-lookup"><span data-stu-id="6859d-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="6859d-106">Este atributo se usará para admitir la conmutación por error para el equipo designado como el que ejecuta la generación de topología entre sitios del comprobador de coherencia de la información en un sitio determinado.</span><span class="sxs-lookup"><span data-stu-id="6859d-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="6859d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="6859d-107">Entry</span></span> | <span data-ttu-id="6859d-108">Value</span><span class="sxs-lookup"><span data-stu-id="6859d-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6859d-109">CN</span><span class="sxs-lookup"><span data-stu-id="6859d-109">CN</span></span>                | <span data-ttu-id="6859d-110">Inter-site-Topology-generator</span><span class="sxs-lookup"><span data-stu-id="6859d-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="6859d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6859d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6859d-112">interSiteTopologyGenerator</span><span class="sxs-lookup"><span data-stu-id="6859d-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="6859d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6859d-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="6859d-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6859d-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="6859d-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6859d-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="6859d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6859d-116">Attribute-Id</span></span>      | <span data-ttu-id="6859d-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="6859d-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="6859d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6859d-118">System-Id-Guid</span></span>    | <span data-ttu-id="6859d-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="6859d-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="6859d-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6859d-120">Syntax</span></span>            | [<span data-ttu-id="6859d-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6859d-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="6859d-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6859d-122">Implementations</span></span>

-   [<span data-ttu-id="6859d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6859d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6859d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6859d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6859d-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6859d-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6859d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6859d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6859d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6859d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6859d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6859d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6859d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6859d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6859d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6859d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="6859d-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="6859d-131">Entry</span></span> | <span data-ttu-id="6859d-132">Value</span><span class="sxs-lookup"><span data-stu-id="6859d-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="6859d-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6859d-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6859d-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6859d-135">System-Only</span></span>            | <span data-ttu-id="6859d-136">False</span><span class="sxs-lookup"><span data-stu-id="6859d-136">False</span></span>                                                       |
| <span data-ttu-id="6859d-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6859d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6859d-138">True</span><span class="sxs-lookup"><span data-stu-id="6859d-138">True</span></span>                                                        |
| <span data-ttu-id="6859d-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6859d-139">Is Indexed</span></span>             | <span data-ttu-id="6859d-140">False</span><span class="sxs-lookup"><span data-stu-id="6859d-140">False</span></span>                                                       |
| <span data-ttu-id="6859d-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6859d-141">In Global Catalog</span></span>      | <span data-ttu-id="6859d-142">False</span><span class="sxs-lookup"><span data-stu-id="6859d-142">False</span></span>                                                       |
| <span data-ttu-id="6859d-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6859d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6859d-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6859d-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="6859d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6859d-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6859d-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-147">Search-Flags</span></span>           | <span data-ttu-id="6859d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6859d-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="6859d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-149">System-Flags</span></span>           | <span data-ttu-id="6859d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6859d-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="6859d-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6859d-151">Classes used in</span></span>        | [<span data-ttu-id="6859d-152">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="6859d-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6859d-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6859d-153">Windows Server 2003</span></span>



| <span data-ttu-id="6859d-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="6859d-154">Entry</span></span> | <span data-ttu-id="6859d-155">Value</span><span class="sxs-lookup"><span data-stu-id="6859d-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="6859d-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6859d-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6859d-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="6859d-158">System-Only</span></span>            | <span data-ttu-id="6859d-159">False</span><span class="sxs-lookup"><span data-stu-id="6859d-159">False</span></span>                                                       |
| <span data-ttu-id="6859d-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6859d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="6859d-161">True</span><span class="sxs-lookup"><span data-stu-id="6859d-161">True</span></span>                                                        |
| <span data-ttu-id="6859d-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6859d-162">Is Indexed</span></span>             | <span data-ttu-id="6859d-163">False</span><span class="sxs-lookup"><span data-stu-id="6859d-163">False</span></span>                                                       |
| <span data-ttu-id="6859d-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6859d-164">In Global Catalog</span></span>      | <span data-ttu-id="6859d-165">False</span><span class="sxs-lookup"><span data-stu-id="6859d-165">False</span></span>                                                       |
| <span data-ttu-id="6859d-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6859d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="6859d-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6859d-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="6859d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6859d-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6859d-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-170">Search-Flags</span></span>           | <span data-ttu-id="6859d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6859d-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="6859d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-172">System-Flags</span></span>           | <span data-ttu-id="6859d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6859d-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="6859d-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6859d-174">Classes used in</span></span>        | [<span data-ttu-id="6859d-175">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="6859d-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6859d-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="6859d-176">ADAM</span></span>



| <span data-ttu-id="6859d-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="6859d-177">Entry</span></span> | <span data-ttu-id="6859d-178">Value</span><span class="sxs-lookup"><span data-stu-id="6859d-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="6859d-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6859d-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6859d-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="6859d-181">System-Only</span></span>            | <span data-ttu-id="6859d-182">False</span><span class="sxs-lookup"><span data-stu-id="6859d-182">False</span></span>                                                       |
| <span data-ttu-id="6859d-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6859d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="6859d-184">True</span><span class="sxs-lookup"><span data-stu-id="6859d-184">True</span></span>                                                        |
| <span data-ttu-id="6859d-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6859d-185">Is Indexed</span></span>             | <span data-ttu-id="6859d-186">False</span><span class="sxs-lookup"><span data-stu-id="6859d-186">False</span></span>                                                       |
| <span data-ttu-id="6859d-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6859d-187">In Global Catalog</span></span>      | <span data-ttu-id="6859d-188">False</span><span class="sxs-lookup"><span data-stu-id="6859d-188">False</span></span>                                                       |
| <span data-ttu-id="6859d-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6859d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="6859d-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6859d-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="6859d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6859d-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6859d-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-193">Search-Flags</span></span>           | <span data-ttu-id="6859d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6859d-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="6859d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-195">System-Flags</span></span>           | <span data-ttu-id="6859d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6859d-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="6859d-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6859d-197">Classes used in</span></span>        | [<span data-ttu-id="6859d-198">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="6859d-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6859d-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6859d-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6859d-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="6859d-200">Entry</span></span> | <span data-ttu-id="6859d-201">Value</span><span class="sxs-lookup"><span data-stu-id="6859d-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="6859d-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6859d-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6859d-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="6859d-204">System-Only</span></span>            | <span data-ttu-id="6859d-205">False</span><span class="sxs-lookup"><span data-stu-id="6859d-205">False</span></span>                                                       |
| <span data-ttu-id="6859d-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6859d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="6859d-207">True</span><span class="sxs-lookup"><span data-stu-id="6859d-207">True</span></span>                                                        |
| <span data-ttu-id="6859d-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6859d-208">Is Indexed</span></span>             | <span data-ttu-id="6859d-209">False</span><span class="sxs-lookup"><span data-stu-id="6859d-209">False</span></span>                                                       |
| <span data-ttu-id="6859d-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6859d-210">In Global Catalog</span></span>      | <span data-ttu-id="6859d-211">False</span><span class="sxs-lookup"><span data-stu-id="6859d-211">False</span></span>                                                       |
| <span data-ttu-id="6859d-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6859d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="6859d-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6859d-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="6859d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6859d-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6859d-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-216">Search-Flags</span></span>           | <span data-ttu-id="6859d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6859d-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="6859d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-218">System-Flags</span></span>           | <span data-ttu-id="6859d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6859d-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="6859d-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6859d-220">Classes used in</span></span>        | [<span data-ttu-id="6859d-221">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="6859d-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6859d-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6859d-222">Windows Server 2008</span></span>



| <span data-ttu-id="6859d-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="6859d-223">Entry</span></span> | <span data-ttu-id="6859d-224">Value</span><span class="sxs-lookup"><span data-stu-id="6859d-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="6859d-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6859d-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6859d-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="6859d-227">System-Only</span></span>            | <span data-ttu-id="6859d-228">False</span><span class="sxs-lookup"><span data-stu-id="6859d-228">False</span></span>                                                       |
| <span data-ttu-id="6859d-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6859d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="6859d-230">True</span><span class="sxs-lookup"><span data-stu-id="6859d-230">True</span></span>                                                        |
| <span data-ttu-id="6859d-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6859d-231">Is Indexed</span></span>             | <span data-ttu-id="6859d-232">False</span><span class="sxs-lookup"><span data-stu-id="6859d-232">False</span></span>                                                       |
| <span data-ttu-id="6859d-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6859d-233">In Global Catalog</span></span>      | <span data-ttu-id="6859d-234">False</span><span class="sxs-lookup"><span data-stu-id="6859d-234">False</span></span>                                                       |
| <span data-ttu-id="6859d-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6859d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="6859d-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6859d-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="6859d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6859d-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6859d-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-239">Search-Flags</span></span>           | <span data-ttu-id="6859d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6859d-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="6859d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-241">System-Flags</span></span>           | <span data-ttu-id="6859d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6859d-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="6859d-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6859d-243">Classes used in</span></span>        | [<span data-ttu-id="6859d-244">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="6859d-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6859d-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6859d-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6859d-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="6859d-246">Entry</span></span> | <span data-ttu-id="6859d-247">Value</span><span class="sxs-lookup"><span data-stu-id="6859d-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="6859d-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6859d-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6859d-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="6859d-250">System-Only</span></span>            | <span data-ttu-id="6859d-251">False</span><span class="sxs-lookup"><span data-stu-id="6859d-251">False</span></span>                                                       |
| <span data-ttu-id="6859d-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6859d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="6859d-253">True</span><span class="sxs-lookup"><span data-stu-id="6859d-253">True</span></span>                                                        |
| <span data-ttu-id="6859d-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6859d-254">Is Indexed</span></span>             | <span data-ttu-id="6859d-255">False</span><span class="sxs-lookup"><span data-stu-id="6859d-255">False</span></span>                                                       |
| <span data-ttu-id="6859d-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6859d-256">In Global Catalog</span></span>      | <span data-ttu-id="6859d-257">False</span><span class="sxs-lookup"><span data-stu-id="6859d-257">False</span></span>                                                       |
| <span data-ttu-id="6859d-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6859d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="6859d-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6859d-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="6859d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6859d-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6859d-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-262">Search-Flags</span></span>           | <span data-ttu-id="6859d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6859d-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="6859d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-264">System-Flags</span></span>           | <span data-ttu-id="6859d-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6859d-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="6859d-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6859d-266">Classes used in</span></span>        | [<span data-ttu-id="6859d-267">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="6859d-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6859d-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6859d-268">Windows Server 2012</span></span>



| <span data-ttu-id="6859d-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="6859d-269">Entry</span></span> | <span data-ttu-id="6859d-270">Value</span><span class="sxs-lookup"><span data-stu-id="6859d-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="6859d-271">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6859d-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6859d-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="6859d-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="6859d-273">System-Only</span></span>            | <span data-ttu-id="6859d-274">False</span><span class="sxs-lookup"><span data-stu-id="6859d-274">False</span></span>                                                       |
| <span data-ttu-id="6859d-275">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6859d-275">Is-Single-Valued</span></span>       | <span data-ttu-id="6859d-276">True</span><span class="sxs-lookup"><span data-stu-id="6859d-276">True</span></span>                                                        |
| <span data-ttu-id="6859d-277">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6859d-277">Is Indexed</span></span>             | <span data-ttu-id="6859d-278">False</span><span class="sxs-lookup"><span data-stu-id="6859d-278">False</span></span>                                                       |
| <span data-ttu-id="6859d-279">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6859d-279">In Global Catalog</span></span>      | <span data-ttu-id="6859d-280">False</span><span class="sxs-lookup"><span data-stu-id="6859d-280">False</span></span>                                                       |
| <span data-ttu-id="6859d-281">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6859d-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="6859d-282">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6859d-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="6859d-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6859d-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6859d-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="6859d-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-285">Search-Flags</span></span>           | <span data-ttu-id="6859d-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6859d-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="6859d-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6859d-287">System-Flags</span></span>           | <span data-ttu-id="6859d-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6859d-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="6859d-289">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6859d-289">Classes used in</span></span>        | [<span data-ttu-id="6859d-290">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="6859d-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 






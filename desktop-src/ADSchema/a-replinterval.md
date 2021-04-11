---
title: Repl-Interval atributo)
description: El atributo de Site-Link objetos que define el intervalo, en minutos, entre los ciclos de replicación entre los sitios de la lista de sitios.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Repl-Interval
- replInterval esquema de AD de atributos
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151589"
---
# <a name="repl-interval-attribute"></a><span data-ttu-id="adf4b-105">Repl-Interval atributo)</span><span class="sxs-lookup"><span data-stu-id="adf4b-105">Repl-Interval attribute</span></span>

<span data-ttu-id="adf4b-106">El atributo de Site-Link objetos que define el intervalo, en minutos, entre los ciclos de replicación entre los sitios de la lista de sitios.</span><span class="sxs-lookup"><span data-stu-id="adf4b-106">The attribute of Site-Link objects that defines the interval, in minutes, between replication cycles between the sites in the Site-List.</span></span> <span data-ttu-id="adf4b-107">Debe ser un múltiplo de 15 minutos (la granularidad de la replicación de DS entre sitios), un mínimo de 15 minutos y un máximo de 10.080 minutos (una semana).</span><span class="sxs-lookup"><span data-stu-id="adf4b-107">Must be a multiple of 15 minutes (the granularity of cross-site DS replication), a minimum of 15 minutes, and a maximum of 10,080 minutes (one week).</span></span>



| <span data-ttu-id="adf4b-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="adf4b-108">Entry</span></span> | <span data-ttu-id="adf4b-109">Value</span><span class="sxs-lookup"><span data-stu-id="adf4b-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="adf4b-110">CN</span><span class="sxs-lookup"><span data-stu-id="adf4b-110">CN</span></span>                | <span data-ttu-id="adf4b-111">Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="adf4b-111">Repl-Interval</span></span>                                  |
| <span data-ttu-id="adf4b-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="adf4b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="adf4b-113">replInterval</span><span class="sxs-lookup"><span data-stu-id="adf4b-113">replInterval</span></span>                                   |
| <span data-ttu-id="adf4b-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="adf4b-114">Size</span></span>              | <span data-ttu-id="adf4b-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="adf4b-115">4 bytes</span></span>                                        |
| <span data-ttu-id="adf4b-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="adf4b-116">Update Privilege</span></span>  | <span data-ttu-id="adf4b-117">Administrador de empresa</span><span class="sxs-lookup"><span data-stu-id="adf4b-117">Enterprise administrator</span></span>                       |
| <span data-ttu-id="adf4b-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="adf4b-118">Update Frequency</span></span>  | <span data-ttu-id="adf4b-119">Cuándo es necesario cambiar el intervalo de replicación.</span><span class="sxs-lookup"><span data-stu-id="adf4b-119">When the replication interval needs to change.</span></span> |
| <span data-ttu-id="adf4b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="adf4b-120">Attribute-Id</span></span>      | <span data-ttu-id="adf4b-121">1.2.840.113556.1.4.1336</span><span class="sxs-lookup"><span data-stu-id="adf4b-121">1.2.840.113556.1.4.1336</span></span>                        |
| <span data-ttu-id="adf4b-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="adf4b-122">System-Id-Guid</span></span>    | <span data-ttu-id="adf4b-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="adf4b-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span></span>           |
| <span data-ttu-id="adf4b-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="adf4b-124">Syntax</span></span>            | [<span data-ttu-id="adf4b-125">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="adf4b-125">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="adf4b-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="adf4b-126">Implementations</span></span>

-   [<span data-ttu-id="adf4b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="adf4b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="adf4b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="adf4b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="adf4b-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="adf4b-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="adf4b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="adf4b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="adf4b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="adf4b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="adf4b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="adf4b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="adf4b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="adf4b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="adf4b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="adf4b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="adf4b-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="adf4b-135">Entry</span></span> | <span data-ttu-id="adf4b-136">Value</span><span class="sxs-lookup"><span data-stu-id="adf4b-136">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4b-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adf4b-137">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf4b-138">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf4b-139">System-Only</span></span>            | <span data-ttu-id="adf4b-140">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-140">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adf4b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="adf4b-142">True</span><span class="sxs-lookup"><span data-stu-id="adf4b-142">True</span></span>                                                                                                       |
| <span data-ttu-id="adf4b-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adf4b-143">Is Indexed</span></span>             | <span data-ttu-id="adf4b-144">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-144">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adf4b-145">In Global Catalog</span></span>      | <span data-ttu-id="adf4b-146">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-146">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adf4b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf4b-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf4b-148">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="adf4b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf4b-149">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf4b-150">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-151">Search-Flags</span></span>           | <span data-ttu-id="adf4b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf4b-152">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-153">System-Flags</span></span>           | <span data-ttu-id="adf4b-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf4b-154">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adf4b-155">Classes used in</span></span>        | [<span data-ttu-id="adf4b-156">**Transporte entre sitios**</span><span class="sxs-lookup"><span data-stu-id="adf4b-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="adf4b-157">**Sitio-vínculo**</span><span class="sxs-lookup"><span data-stu-id="adf4b-157">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="adf4b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="adf4b-158">Windows Server 2003</span></span>



| <span data-ttu-id="adf4b-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="adf4b-159">Entry</span></span> | <span data-ttu-id="adf4b-160">Value</span><span class="sxs-lookup"><span data-stu-id="adf4b-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4b-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adf4b-161">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf4b-162">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf4b-163">System-Only</span></span>            | <span data-ttu-id="adf4b-164">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-164">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adf4b-165">Is-Single-Valued</span></span>       | <span data-ttu-id="adf4b-166">True</span><span class="sxs-lookup"><span data-stu-id="adf4b-166">True</span></span>                                                                                                       |
| <span data-ttu-id="adf4b-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adf4b-167">Is Indexed</span></span>             | <span data-ttu-id="adf4b-168">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-168">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adf4b-169">In Global Catalog</span></span>      | <span data-ttu-id="adf4b-170">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-170">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adf4b-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf4b-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf4b-172">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="adf4b-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf4b-173">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf4b-174">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-175">Search-Flags</span></span>           | <span data-ttu-id="adf4b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf4b-176">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-177">System-Flags</span></span>           | <span data-ttu-id="adf4b-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf4b-178">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adf4b-179">Classes used in</span></span>        | [<span data-ttu-id="adf4b-180">**Transporte entre sitios**</span><span class="sxs-lookup"><span data-stu-id="adf4b-180">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="adf4b-181">**Sitio-vínculo**</span><span class="sxs-lookup"><span data-stu-id="adf4b-181">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="adf4b-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="adf4b-182">ADAM</span></span>



| <span data-ttu-id="adf4b-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="adf4b-183">Entry</span></span> | <span data-ttu-id="adf4b-184">Value</span><span class="sxs-lookup"><span data-stu-id="adf4b-184">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4b-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adf4b-185">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf4b-186">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf4b-187">System-Only</span></span>            | <span data-ttu-id="adf4b-188">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-188">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adf4b-189">Is-Single-Valued</span></span>       | <span data-ttu-id="adf4b-190">True</span><span class="sxs-lookup"><span data-stu-id="adf4b-190">True</span></span>                                                                                                       |
| <span data-ttu-id="adf4b-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adf4b-191">Is Indexed</span></span>             | <span data-ttu-id="adf4b-192">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-192">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adf4b-193">In Global Catalog</span></span>      | <span data-ttu-id="adf4b-194">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-194">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adf4b-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf4b-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf4b-196">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="adf4b-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf4b-197">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf4b-198">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-199">Search-Flags</span></span>           | <span data-ttu-id="adf4b-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf4b-200">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-201">System-Flags</span></span>           | <span data-ttu-id="adf4b-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf4b-202">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adf4b-203">Classes used in</span></span>        | [<span data-ttu-id="adf4b-204">**Transporte entre sitios**</span><span class="sxs-lookup"><span data-stu-id="adf4b-204">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="adf4b-205">**Sitio-vínculo**</span><span class="sxs-lookup"><span data-stu-id="adf4b-205">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="adf4b-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="adf4b-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="adf4b-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="adf4b-207">Entry</span></span> | <span data-ttu-id="adf4b-208">Value</span><span class="sxs-lookup"><span data-stu-id="adf4b-208">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4b-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adf4b-209">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf4b-210">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf4b-211">System-Only</span></span>            | <span data-ttu-id="adf4b-212">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-212">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adf4b-213">Is-Single-Valued</span></span>       | <span data-ttu-id="adf4b-214">True</span><span class="sxs-lookup"><span data-stu-id="adf4b-214">True</span></span>                                                                                                       |
| <span data-ttu-id="adf4b-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adf4b-215">Is Indexed</span></span>             | <span data-ttu-id="adf4b-216">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-216">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adf4b-217">In Global Catalog</span></span>      | <span data-ttu-id="adf4b-218">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-218">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adf4b-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf4b-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf4b-220">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="adf4b-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf4b-221">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf4b-222">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-223">Search-Flags</span></span>           | <span data-ttu-id="adf4b-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf4b-224">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-225">System-Flags</span></span>           | <span data-ttu-id="adf4b-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf4b-226">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adf4b-227">Classes used in</span></span>        | [<span data-ttu-id="adf4b-228">**Transporte entre sitios**</span><span class="sxs-lookup"><span data-stu-id="adf4b-228">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="adf4b-229">**Sitio-vínculo**</span><span class="sxs-lookup"><span data-stu-id="adf4b-229">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="adf4b-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adf4b-230">Windows Server 2008</span></span>



| <span data-ttu-id="adf4b-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="adf4b-231">Entry</span></span> | <span data-ttu-id="adf4b-232">Value</span><span class="sxs-lookup"><span data-stu-id="adf4b-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4b-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adf4b-233">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf4b-234">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf4b-235">System-Only</span></span>            | <span data-ttu-id="adf4b-236">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-236">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adf4b-237">Is-Single-Valued</span></span>       | <span data-ttu-id="adf4b-238">True</span><span class="sxs-lookup"><span data-stu-id="adf4b-238">True</span></span>                                                                                                       |
| <span data-ttu-id="adf4b-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adf4b-239">Is Indexed</span></span>             | <span data-ttu-id="adf4b-240">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-240">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adf4b-241">In Global Catalog</span></span>      | <span data-ttu-id="adf4b-242">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-242">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adf4b-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf4b-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf4b-244">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="adf4b-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf4b-245">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf4b-246">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-247">Search-Flags</span></span>           | <span data-ttu-id="adf4b-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf4b-248">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-249">System-Flags</span></span>           | <span data-ttu-id="adf4b-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf4b-250">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adf4b-251">Classes used in</span></span>        | [<span data-ttu-id="adf4b-252">**Transporte entre sitios**</span><span class="sxs-lookup"><span data-stu-id="adf4b-252">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="adf4b-253">**Sitio-vínculo**</span><span class="sxs-lookup"><span data-stu-id="adf4b-253">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="adf4b-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="adf4b-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="adf4b-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="adf4b-255">Entry</span></span> | <span data-ttu-id="adf4b-256">Value</span><span class="sxs-lookup"><span data-stu-id="adf4b-256">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4b-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adf4b-257">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf4b-258">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf4b-259">System-Only</span></span>            | <span data-ttu-id="adf4b-260">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-260">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-261">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adf4b-261">Is-Single-Valued</span></span>       | <span data-ttu-id="adf4b-262">True</span><span class="sxs-lookup"><span data-stu-id="adf4b-262">True</span></span>                                                                                                       |
| <span data-ttu-id="adf4b-263">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adf4b-263">Is Indexed</span></span>             | <span data-ttu-id="adf4b-264">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-264">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-265">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adf4b-265">In Global Catalog</span></span>      | <span data-ttu-id="adf4b-266">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-266">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-267">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adf4b-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf4b-268">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf4b-268">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="adf4b-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf4b-269">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf4b-270">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-271">Search-Flags</span></span>           | <span data-ttu-id="adf4b-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf4b-272">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-273">System-Flags</span></span>           | <span data-ttu-id="adf4b-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf4b-274">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-275">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adf4b-275">Classes used in</span></span>        | [<span data-ttu-id="adf4b-276">**Transporte entre sitios**</span><span class="sxs-lookup"><span data-stu-id="adf4b-276">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="adf4b-277">**Sitio-vínculo**</span><span class="sxs-lookup"><span data-stu-id="adf4b-277">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="adf4b-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="adf4b-278">Windows Server 2012</span></span>



| <span data-ttu-id="adf4b-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="adf4b-279">Entry</span></span> | <span data-ttu-id="adf4b-280">Value</span><span class="sxs-lookup"><span data-stu-id="adf4b-280">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4b-281">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adf4b-281">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf4b-282">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="adf4b-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf4b-283">System-Only</span></span>            | <span data-ttu-id="adf4b-284">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-284">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-285">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="adf4b-285">Is-Single-Valued</span></span>       | <span data-ttu-id="adf4b-286">True</span><span class="sxs-lookup"><span data-stu-id="adf4b-286">True</span></span>                                                                                                       |
| <span data-ttu-id="adf4b-287">Está indexado</span><span class="sxs-lookup"><span data-stu-id="adf4b-287">Is Indexed</span></span>             | <span data-ttu-id="adf4b-288">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-288">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-289">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="adf4b-289">In Global Catalog</span></span>      | <span data-ttu-id="adf4b-290">False</span><span class="sxs-lookup"><span data-stu-id="adf4b-290">False</span></span>                                                                                                      |
| <span data-ttu-id="adf4b-291">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="adf4b-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf4b-292">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf4b-292">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="adf4b-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf4b-293">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf4b-294">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="adf4b-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-295">Search-Flags</span></span>           | <span data-ttu-id="adf4b-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf4b-296">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf4b-297">System-Flags</span></span>           | <span data-ttu-id="adf4b-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf4b-298">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="adf4b-299">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="adf4b-299">Classes used in</span></span>        | [<span data-ttu-id="adf4b-300">**Transporte entre sitios**</span><span class="sxs-lookup"><span data-stu-id="adf4b-300">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="adf4b-301">**Sitio-vínculo**</span><span class="sxs-lookup"><span data-stu-id="adf4b-301">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 






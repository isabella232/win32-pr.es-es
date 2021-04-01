---
title: Atributo MSMQ-out-Routing-servers
description: Los vínculos DN a los servidores de enrutamiento de MSMQ a través de los cuales se debe enrutar todo el tráfico saliente para este equipo.
ms.assetid: 169558e4-d2a6-4555-bc5f-7e6a89e51789
ms.tgt_platform: multiple
keywords:
- Message Queue-out-Routing-Servers atributo AD Schema
- mSMQOutRoutingServers esquema de AD de atributos
topic_type:
- apiref
api_name:
- MSMQ-Out-Routing-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc2265b2d809b7a73cd19faace87473552471a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906003"
---
# <a name="msmq-out-routing-servers-attribute"></a><span data-ttu-id="d1e66-105">Atributo MSMQ-out-Routing-servers</span><span class="sxs-lookup"><span data-stu-id="d1e66-105">MSMQ-Out-Routing-Servers attribute</span></span>

<span data-ttu-id="d1e66-106">Los vínculos DN a los servidores de enrutamiento de MSMQ a través de los cuales se debe enrutar todo el tráfico saliente para este equipo.</span><span class="sxs-lookup"><span data-stu-id="d1e66-106">DN links to MSMQ routing servers through which all outgoing traffic for this computer should be routed.</span></span>



| <span data-ttu-id="d1e66-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1e66-107">Entry</span></span> | <span data-ttu-id="d1e66-108">Value</span><span class="sxs-lookup"><span data-stu-id="d1e66-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d1e66-109">CN</span><span class="sxs-lookup"><span data-stu-id="d1e66-109">CN</span></span>                | <span data-ttu-id="d1e66-110">MSMQ-out-Routing-servers</span><span class="sxs-lookup"><span data-stu-id="d1e66-110">MSMQ-Out-Routing-Servers</span></span>                |
| <span data-ttu-id="d1e66-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d1e66-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d1e66-112">mSMQOutRoutingServers</span><span class="sxs-lookup"><span data-stu-id="d1e66-112">mSMQOutRoutingServers</span></span>                   |
| <span data-ttu-id="d1e66-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d1e66-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d1e66-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d1e66-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="d1e66-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d1e66-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="d1e66-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d1e66-116">Attribute-Id</span></span>      | <span data-ttu-id="d1e66-117">1.2.840.113556.1.4.928</span><span class="sxs-lookup"><span data-stu-id="d1e66-117">1.2.840.113556.1.4.928</span></span>                  |
| <span data-ttu-id="d1e66-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d1e66-118">System-Id-Guid</span></span>    | <span data-ttu-id="d1e66-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="d1e66-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="d1e66-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1e66-120">Syntax</span></span>            | [<span data-ttu-id="d1e66-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d1e66-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d1e66-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d1e66-122">Implementations</span></span>

-   [<span data-ttu-id="d1e66-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d1e66-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d1e66-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d1e66-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d1e66-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d1e66-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d1e66-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d1e66-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d1e66-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d1e66-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d1e66-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d1e66-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d1e66-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1e66-129">Windows 2000 Server</span></span>



| <span data-ttu-id="d1e66-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1e66-130">Entry</span></span> | <span data-ttu-id="d1e66-131">Value</span><span class="sxs-lookup"><span data-stu-id="d1e66-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d1e66-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1e66-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1e66-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1e66-134">System-Only</span></span>            | <span data-ttu-id="d1e66-135">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-135">False</span></span>                                                        |
| <span data-ttu-id="d1e66-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1e66-136">Is-Single-Valued</span></span>       | <span data-ttu-id="d1e66-137">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-137">False</span></span>                                                        |
| <span data-ttu-id="d1e66-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1e66-138">Is Indexed</span></span>             | <span data-ttu-id="d1e66-139">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-139">False</span></span>                                                        |
| <span data-ttu-id="d1e66-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1e66-140">In Global Catalog</span></span>      | <span data-ttu-id="d1e66-141">True</span><span class="sxs-lookup"><span data-stu-id="d1e66-141">True</span></span>                                                         |
| <span data-ttu-id="d1e66-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1e66-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1e66-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1e66-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d1e66-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1e66-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1e66-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-146">Search-Flags</span></span>           | <span data-ttu-id="d1e66-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1e66-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="d1e66-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-148">System-Flags</span></span>           | <span data-ttu-id="d1e66-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1e66-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="d1e66-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1e66-150">Classes used in</span></span>        | [<span data-ttu-id="d1e66-151">**MSMQ-configuración**</span><span class="sxs-lookup"><span data-stu-id="d1e66-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d1e66-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1e66-152">Windows Server 2003</span></span>



| <span data-ttu-id="d1e66-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1e66-153">Entry</span></span> | <span data-ttu-id="d1e66-154">Value</span><span class="sxs-lookup"><span data-stu-id="d1e66-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d1e66-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1e66-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1e66-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1e66-157">System-Only</span></span>            | <span data-ttu-id="d1e66-158">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-158">False</span></span>                                                        |
| <span data-ttu-id="d1e66-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1e66-159">Is-Single-Valued</span></span>       | <span data-ttu-id="d1e66-160">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-160">False</span></span>                                                        |
| <span data-ttu-id="d1e66-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1e66-161">Is Indexed</span></span>             | <span data-ttu-id="d1e66-162">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-162">False</span></span>                                                        |
| <span data-ttu-id="d1e66-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1e66-163">In Global Catalog</span></span>      | <span data-ttu-id="d1e66-164">True</span><span class="sxs-lookup"><span data-stu-id="d1e66-164">True</span></span>                                                         |
| <span data-ttu-id="d1e66-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1e66-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1e66-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1e66-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d1e66-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1e66-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1e66-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-169">Search-Flags</span></span>           | <span data-ttu-id="d1e66-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1e66-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="d1e66-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-171">System-Flags</span></span>           | <span data-ttu-id="d1e66-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1e66-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="d1e66-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1e66-173">Classes used in</span></span>        | [<span data-ttu-id="d1e66-174">**MSMQ-configuración**</span><span class="sxs-lookup"><span data-stu-id="d1e66-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d1e66-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d1e66-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d1e66-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1e66-176">Entry</span></span> | <span data-ttu-id="d1e66-177">Value</span><span class="sxs-lookup"><span data-stu-id="d1e66-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d1e66-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1e66-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1e66-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1e66-180">System-Only</span></span>            | <span data-ttu-id="d1e66-181">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-181">False</span></span>                                                        |
| <span data-ttu-id="d1e66-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1e66-182">Is-Single-Valued</span></span>       | <span data-ttu-id="d1e66-183">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-183">False</span></span>                                                        |
| <span data-ttu-id="d1e66-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1e66-184">Is Indexed</span></span>             | <span data-ttu-id="d1e66-185">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-185">False</span></span>                                                        |
| <span data-ttu-id="d1e66-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1e66-186">In Global Catalog</span></span>      | <span data-ttu-id="d1e66-187">True</span><span class="sxs-lookup"><span data-stu-id="d1e66-187">True</span></span>                                                         |
| <span data-ttu-id="d1e66-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1e66-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1e66-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1e66-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d1e66-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1e66-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1e66-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-192">Search-Flags</span></span>           | <span data-ttu-id="d1e66-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1e66-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="d1e66-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-194">System-Flags</span></span>           | <span data-ttu-id="d1e66-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1e66-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="d1e66-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1e66-196">Classes used in</span></span>        | [<span data-ttu-id="d1e66-197">**MSMQ-configuración**</span><span class="sxs-lookup"><span data-stu-id="d1e66-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d1e66-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1e66-198">Windows Server 2008</span></span>



| <span data-ttu-id="d1e66-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1e66-199">Entry</span></span> | <span data-ttu-id="d1e66-200">Value</span><span class="sxs-lookup"><span data-stu-id="d1e66-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d1e66-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1e66-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1e66-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1e66-203">System-Only</span></span>            | <span data-ttu-id="d1e66-204">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-204">False</span></span>                                                        |
| <span data-ttu-id="d1e66-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1e66-205">Is-Single-Valued</span></span>       | <span data-ttu-id="d1e66-206">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-206">False</span></span>                                                        |
| <span data-ttu-id="d1e66-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1e66-207">Is Indexed</span></span>             | <span data-ttu-id="d1e66-208">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-208">False</span></span>                                                        |
| <span data-ttu-id="d1e66-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1e66-209">In Global Catalog</span></span>      | <span data-ttu-id="d1e66-210">True</span><span class="sxs-lookup"><span data-stu-id="d1e66-210">True</span></span>                                                         |
| <span data-ttu-id="d1e66-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1e66-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1e66-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1e66-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d1e66-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1e66-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1e66-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-215">Search-Flags</span></span>           | <span data-ttu-id="d1e66-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1e66-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="d1e66-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-217">System-Flags</span></span>           | <span data-ttu-id="d1e66-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1e66-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="d1e66-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1e66-219">Classes used in</span></span>        | [<span data-ttu-id="d1e66-220">**MSMQ-configuración**</span><span class="sxs-lookup"><span data-stu-id="d1e66-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d1e66-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1e66-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d1e66-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1e66-222">Entry</span></span> | <span data-ttu-id="d1e66-223">Value</span><span class="sxs-lookup"><span data-stu-id="d1e66-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d1e66-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1e66-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1e66-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1e66-226">System-Only</span></span>            | <span data-ttu-id="d1e66-227">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-227">False</span></span>                                                        |
| <span data-ttu-id="d1e66-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1e66-228">Is-Single-Valued</span></span>       | <span data-ttu-id="d1e66-229">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-229">False</span></span>                                                        |
| <span data-ttu-id="d1e66-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1e66-230">Is Indexed</span></span>             | <span data-ttu-id="d1e66-231">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-231">False</span></span>                                                        |
| <span data-ttu-id="d1e66-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1e66-232">In Global Catalog</span></span>      | <span data-ttu-id="d1e66-233">True</span><span class="sxs-lookup"><span data-stu-id="d1e66-233">True</span></span>                                                         |
| <span data-ttu-id="d1e66-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1e66-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1e66-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1e66-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d1e66-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1e66-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1e66-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-238">Search-Flags</span></span>           | <span data-ttu-id="d1e66-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1e66-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="d1e66-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-240">System-Flags</span></span>           | <span data-ttu-id="d1e66-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1e66-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="d1e66-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1e66-242">Classes used in</span></span>        | [<span data-ttu-id="d1e66-243">**MSMQ-configuración**</span><span class="sxs-lookup"><span data-stu-id="d1e66-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d1e66-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1e66-244">Windows Server 2012</span></span>



| <span data-ttu-id="d1e66-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1e66-245">Entry</span></span> | <span data-ttu-id="d1e66-246">Value</span><span class="sxs-lookup"><span data-stu-id="d1e66-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d1e66-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d1e66-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1e66-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="d1e66-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1e66-249">System-Only</span></span>            | <span data-ttu-id="d1e66-250">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-250">False</span></span>                                                        |
| <span data-ttu-id="d1e66-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d1e66-251">Is-Single-Valued</span></span>       | <span data-ttu-id="d1e66-252">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-252">False</span></span>                                                        |
| <span data-ttu-id="d1e66-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d1e66-253">Is Indexed</span></span>             | <span data-ttu-id="d1e66-254">False</span><span class="sxs-lookup"><span data-stu-id="d1e66-254">False</span></span>                                                        |
| <span data-ttu-id="d1e66-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1e66-255">In Global Catalog</span></span>      | <span data-ttu-id="d1e66-256">True</span><span class="sxs-lookup"><span data-stu-id="d1e66-256">True</span></span>                                                         |
| <span data-ttu-id="d1e66-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d1e66-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1e66-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d1e66-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="d1e66-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1e66-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1e66-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="d1e66-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-261">Search-Flags</span></span>           | <span data-ttu-id="d1e66-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1e66-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="d1e66-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1e66-263">System-Flags</span></span>           | <span data-ttu-id="d1e66-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1e66-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="d1e66-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d1e66-265">Classes used in</span></span>        | [<span data-ttu-id="d1e66-266">**MSMQ-configuración**</span><span class="sxs-lookup"><span data-stu-id="d1e66-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 






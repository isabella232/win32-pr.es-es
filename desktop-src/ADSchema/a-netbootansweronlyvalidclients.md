---
title: netboot-respuesta-solo-atributo válido-clients
description: Determina si el servidor responde a todos los equipos cliente o solo preconfigurados.
ms.assetid: b02438ba-11b3-497c-b57f-bd9a0045e6b0
ms.tgt_platform: multiple
keywords:
- netboot-solo respuesta-válido-esquema de AD de atributos de clientes
- netbootAnswerOnlyValidClients esquema de AD de atributos
topic_type:
- apiref
api_name:
- netboot-Answer-Only-Valid-Clients
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e28f7ecfaa569f47d79249606029760b914b5ac
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151611"
---
# <a name="netboot-answer-only-valid-clients-attribute"></a><span data-ttu-id="f032b-105">netboot-respuesta-solo-atributo válido-clients</span><span class="sxs-lookup"><span data-stu-id="f032b-105">netboot-Answer-Only-Valid-Clients attribute</span></span>

<span data-ttu-id="f032b-106">Determina si el servidor responde a todos los equipos cliente o solo preconfigurados.</span><span class="sxs-lookup"><span data-stu-id="f032b-106">Determines whether the server answers all, or only pre-staged, client computers.</span></span>



| <span data-ttu-id="f032b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f032b-107">Entry</span></span> | <span data-ttu-id="f032b-108">Value</span><span class="sxs-lookup"><span data-stu-id="f032b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f032b-109">CN</span><span class="sxs-lookup"><span data-stu-id="f032b-109">CN</span></span>                | <span data-ttu-id="f032b-110">netboot-solo respuesta-válido-clientes</span><span class="sxs-lookup"><span data-stu-id="f032b-110">netboot-Answer-Only-Valid-Clients</span></span>    |
| <span data-ttu-id="f032b-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f032b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f032b-112">netbootAnswerOnlyValidClients</span><span class="sxs-lookup"><span data-stu-id="f032b-112">netbootAnswerOnlyValidClients</span></span>        |
| <span data-ttu-id="f032b-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f032b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="f032b-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f032b-114">Update Privilege</span></span>  | <span data-ttu-id="f032b-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="f032b-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="f032b-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f032b-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f032b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f032b-117">Attribute-Id</span></span>      | <span data-ttu-id="f032b-118">1.2.840.113556.1.4.854</span><span class="sxs-lookup"><span data-stu-id="f032b-118">1.2.840.113556.1.4.854</span></span>               |
| <span data-ttu-id="f032b-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f032b-119">System-Id-Guid</span></span>    | <span data-ttu-id="f032b-120">0738307b-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f032b-120">0738307b-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="f032b-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f032b-121">Syntax</span></span>            | [<span data-ttu-id="f032b-122">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="f032b-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="f032b-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f032b-123">Implementations</span></span>

-   [<span data-ttu-id="f032b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f032b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f032b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f032b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f032b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f032b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f032b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f032b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f032b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f032b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f032b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f032b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f032b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f032b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="f032b-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="f032b-131">Entry</span></span> | <span data-ttu-id="f032b-132">Value</span><span class="sxs-lookup"><span data-stu-id="f032b-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f032b-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f032b-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f032b-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f032b-135">System-Only</span></span>            | <span data-ttu-id="f032b-136">False</span><span class="sxs-lookup"><span data-stu-id="f032b-136">False</span></span>                                                      |
| <span data-ttu-id="f032b-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f032b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f032b-138">True</span><span class="sxs-lookup"><span data-stu-id="f032b-138">True</span></span>                                                       |
| <span data-ttu-id="f032b-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f032b-139">Is Indexed</span></span>             | <span data-ttu-id="f032b-140">False</span><span class="sxs-lookup"><span data-stu-id="f032b-140">False</span></span>                                                      |
| <span data-ttu-id="f032b-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f032b-141">In Global Catalog</span></span>      | <span data-ttu-id="f032b-142">False</span><span class="sxs-lookup"><span data-stu-id="f032b-142">False</span></span>                                                      |
| <span data-ttu-id="f032b-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f032b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f032b-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f032b-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f032b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f032b-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f032b-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-147">Search-Flags</span></span>           | <span data-ttu-id="f032b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f032b-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="f032b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-149">System-Flags</span></span>           | <span data-ttu-id="f032b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f032b-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="f032b-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f032b-151">Classes used in</span></span>        | [<span data-ttu-id="f032b-152">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="f032b-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f032b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f032b-153">Windows Server 2003</span></span>



| <span data-ttu-id="f032b-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="f032b-154">Entry</span></span> | <span data-ttu-id="f032b-155">Value</span><span class="sxs-lookup"><span data-stu-id="f032b-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f032b-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f032b-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f032b-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f032b-158">System-Only</span></span>            | <span data-ttu-id="f032b-159">False</span><span class="sxs-lookup"><span data-stu-id="f032b-159">False</span></span>                                                      |
| <span data-ttu-id="f032b-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f032b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f032b-161">True</span><span class="sxs-lookup"><span data-stu-id="f032b-161">True</span></span>                                                       |
| <span data-ttu-id="f032b-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f032b-162">Is Indexed</span></span>             | <span data-ttu-id="f032b-163">False</span><span class="sxs-lookup"><span data-stu-id="f032b-163">False</span></span>                                                      |
| <span data-ttu-id="f032b-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f032b-164">In Global Catalog</span></span>      | <span data-ttu-id="f032b-165">False</span><span class="sxs-lookup"><span data-stu-id="f032b-165">False</span></span>                                                      |
| <span data-ttu-id="f032b-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f032b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f032b-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f032b-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f032b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f032b-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f032b-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-170">Search-Flags</span></span>           | <span data-ttu-id="f032b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f032b-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="f032b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-172">System-Flags</span></span>           | <span data-ttu-id="f032b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f032b-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="f032b-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f032b-174">Classes used in</span></span>        | [<span data-ttu-id="f032b-175">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="f032b-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f032b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f032b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f032b-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="f032b-177">Entry</span></span> | <span data-ttu-id="f032b-178">Value</span><span class="sxs-lookup"><span data-stu-id="f032b-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f032b-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f032b-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f032b-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="f032b-181">System-Only</span></span>            | <span data-ttu-id="f032b-182">False</span><span class="sxs-lookup"><span data-stu-id="f032b-182">False</span></span>                                                      |
| <span data-ttu-id="f032b-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f032b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="f032b-184">True</span><span class="sxs-lookup"><span data-stu-id="f032b-184">True</span></span>                                                       |
| <span data-ttu-id="f032b-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f032b-185">Is Indexed</span></span>             | <span data-ttu-id="f032b-186">False</span><span class="sxs-lookup"><span data-stu-id="f032b-186">False</span></span>                                                      |
| <span data-ttu-id="f032b-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f032b-187">In Global Catalog</span></span>      | <span data-ttu-id="f032b-188">False</span><span class="sxs-lookup"><span data-stu-id="f032b-188">False</span></span>                                                      |
| <span data-ttu-id="f032b-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f032b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="f032b-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f032b-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f032b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f032b-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f032b-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-193">Search-Flags</span></span>           | <span data-ttu-id="f032b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f032b-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="f032b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-195">System-Flags</span></span>           | <span data-ttu-id="f032b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f032b-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="f032b-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f032b-197">Classes used in</span></span>        | [<span data-ttu-id="f032b-198">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="f032b-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f032b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f032b-199">Windows Server 2008</span></span>



| <span data-ttu-id="f032b-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="f032b-200">Entry</span></span> | <span data-ttu-id="f032b-201">Value</span><span class="sxs-lookup"><span data-stu-id="f032b-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f032b-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f032b-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f032b-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="f032b-204">System-Only</span></span>            | <span data-ttu-id="f032b-205">False</span><span class="sxs-lookup"><span data-stu-id="f032b-205">False</span></span>                                                      |
| <span data-ttu-id="f032b-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f032b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="f032b-207">True</span><span class="sxs-lookup"><span data-stu-id="f032b-207">True</span></span>                                                       |
| <span data-ttu-id="f032b-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f032b-208">Is Indexed</span></span>             | <span data-ttu-id="f032b-209">False</span><span class="sxs-lookup"><span data-stu-id="f032b-209">False</span></span>                                                      |
| <span data-ttu-id="f032b-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f032b-210">In Global Catalog</span></span>      | <span data-ttu-id="f032b-211">False</span><span class="sxs-lookup"><span data-stu-id="f032b-211">False</span></span>                                                      |
| <span data-ttu-id="f032b-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f032b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="f032b-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f032b-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f032b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f032b-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f032b-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-216">Search-Flags</span></span>           | <span data-ttu-id="f032b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f032b-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="f032b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-218">System-Flags</span></span>           | <span data-ttu-id="f032b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f032b-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="f032b-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f032b-220">Classes used in</span></span>        | [<span data-ttu-id="f032b-221">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="f032b-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f032b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f032b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f032b-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="f032b-223">Entry</span></span> | <span data-ttu-id="f032b-224">Value</span><span class="sxs-lookup"><span data-stu-id="f032b-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f032b-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f032b-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f032b-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="f032b-227">System-Only</span></span>            | <span data-ttu-id="f032b-228">False</span><span class="sxs-lookup"><span data-stu-id="f032b-228">False</span></span>                                                      |
| <span data-ttu-id="f032b-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f032b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="f032b-230">True</span><span class="sxs-lookup"><span data-stu-id="f032b-230">True</span></span>                                                       |
| <span data-ttu-id="f032b-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f032b-231">Is Indexed</span></span>             | <span data-ttu-id="f032b-232">False</span><span class="sxs-lookup"><span data-stu-id="f032b-232">False</span></span>                                                      |
| <span data-ttu-id="f032b-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f032b-233">In Global Catalog</span></span>      | <span data-ttu-id="f032b-234">False</span><span class="sxs-lookup"><span data-stu-id="f032b-234">False</span></span>                                                      |
| <span data-ttu-id="f032b-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f032b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="f032b-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f032b-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f032b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f032b-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f032b-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-239">Search-Flags</span></span>           | <span data-ttu-id="f032b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f032b-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="f032b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-241">System-Flags</span></span>           | <span data-ttu-id="f032b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f032b-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="f032b-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f032b-243">Classes used in</span></span>        | [<span data-ttu-id="f032b-244">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="f032b-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f032b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f032b-245">Windows Server 2012</span></span>



| <span data-ttu-id="f032b-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="f032b-246">Entry</span></span> | <span data-ttu-id="f032b-247">Value</span><span class="sxs-lookup"><span data-stu-id="f032b-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="f032b-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f032b-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f032b-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="f032b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="f032b-250">System-Only</span></span>            | <span data-ttu-id="f032b-251">False</span><span class="sxs-lookup"><span data-stu-id="f032b-251">False</span></span>                                                      |
| <span data-ttu-id="f032b-252">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f032b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="f032b-253">True</span><span class="sxs-lookup"><span data-stu-id="f032b-253">True</span></span>                                                       |
| <span data-ttu-id="f032b-254">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f032b-254">Is Indexed</span></span>             | <span data-ttu-id="f032b-255">False</span><span class="sxs-lookup"><span data-stu-id="f032b-255">False</span></span>                                                      |
| <span data-ttu-id="f032b-256">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f032b-256">In Global Catalog</span></span>      | <span data-ttu-id="f032b-257">False</span><span class="sxs-lookup"><span data-stu-id="f032b-257">False</span></span>                                                      |
| <span data-ttu-id="f032b-258">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f032b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="f032b-259">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f032b-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="f032b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f032b-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f032b-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="f032b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-262">Search-Flags</span></span>           | <span data-ttu-id="f032b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f032b-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="f032b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f032b-264">System-Flags</span></span>           | <span data-ttu-id="f032b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f032b-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="f032b-266">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f032b-266">Classes used in</span></span>        | [<span data-ttu-id="f032b-267">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="f032b-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 






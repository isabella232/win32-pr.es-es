---
title: Invocation-Id atributo)
description: Se utiliza para identificar de forma única cada directorio de Microsoft Exchange Server de la organización.
ms.assetid: c069a57c-b9d0-49e9-8096-39b43f378573
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Invocation-Id
- Esquema de AD de atributo de invocación
topic_type:
- apiref
api_name:
- Invocation-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611589c466013ad46c0920a2da1e2250cf596214
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151402"
---
# <a name="invocation-id-attribute"></a><span data-ttu-id="f14d2-105">Invocation-Id atributo)</span><span class="sxs-lookup"><span data-stu-id="f14d2-105">Invocation-Id attribute</span></span>

<span data-ttu-id="f14d2-106">Se utiliza para identificar de forma única cada directorio de Microsoft Exchange Server de la organización.</span><span class="sxs-lookup"><span data-stu-id="f14d2-106">Used to uniquely identify each Microsoft Exchange Server directory in the organization.</span></span>



| <span data-ttu-id="f14d2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14d2-107">Entry</span></span> | <span data-ttu-id="f14d2-108">Value</span><span class="sxs-lookup"><span data-stu-id="f14d2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f14d2-109">CN</span><span class="sxs-lookup"><span data-stu-id="f14d2-109">CN</span></span>                | <span data-ttu-id="f14d2-110">Invocation-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-110">Invocation-Id</span></span>                                         |
| <span data-ttu-id="f14d2-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f14d2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f14d2-112">Vocación</span><span class="sxs-lookup"><span data-stu-id="f14d2-112">invocationId</span></span>                                          |
| <span data-ttu-id="f14d2-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f14d2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f14d2-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f14d2-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="f14d2-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f14d2-115">Update Frequency</span></span>  | <span data-ttu-id="f14d2-116">Cuando se instala el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f14d2-116">When the Exchange Server is installed.</span></span>                |
| <span data-ttu-id="f14d2-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-117">Attribute-Id</span></span>      | <span data-ttu-id="f14d2-118">1.2.840.113556.1.2.115</span><span class="sxs-lookup"><span data-stu-id="f14d2-118">1.2.840.113556.1.2.115</span></span>                                |
| <span data-ttu-id="f14d2-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f14d2-119">System-Id-Guid</span></span>    | <span data-ttu-id="f14d2-120">bf96798e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f14d2-120">bf96798e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="f14d2-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f14d2-121">Syntax</span></span>            | [<span data-ttu-id="f14d2-122">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f14d2-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f14d2-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f14d2-123">Implementations</span></span>

-   [<span data-ttu-id="f14d2-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f14d2-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f14d2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f14d2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f14d2-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f14d2-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f14d2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f14d2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f14d2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f14d2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f14d2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f14d2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f14d2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f14d2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f14d2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f14d2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f14d2-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14d2-132">Entry</span></span> | <span data-ttu-id="f14d2-133">Value</span><span class="sxs-lookup"><span data-stu-id="f14d2-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f14d2-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f14d2-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f14d2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-135">MAPI-Id</span></span>                | <span data-ttu-id="f14d2-136">0x80BF</span><span class="sxs-lookup"><span data-stu-id="f14d2-136">0x80BF</span></span>                                   |
| <span data-ttu-id="f14d2-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f14d2-137">System-Only</span></span>            | <span data-ttu-id="f14d2-138">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-138">True</span></span>                                     |
| <span data-ttu-id="f14d2-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f14d2-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f14d2-140">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-140">True</span></span>                                     |
| <span data-ttu-id="f14d2-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f14d2-141">Is Indexed</span></span>             | <span data-ttu-id="f14d2-142">False</span><span class="sxs-lookup"><span data-stu-id="f14d2-142">False</span></span>                                    |
| <span data-ttu-id="f14d2-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f14d2-143">In Global Catalog</span></span>      | <span data-ttu-id="f14d2-144">False</span><span class="sxs-lookup"><span data-stu-id="f14d2-144">False</span></span>                                    |
| <span data-ttu-id="f14d2-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f14d2-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f14d2-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f14d2-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f14d2-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f14d2-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f14d2-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-149">Search-Flags</span></span>           | <span data-ttu-id="f14d2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f14d2-150">0x00000000</span></span>                               |
| <span data-ttu-id="f14d2-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-151">System-Flags</span></span>           | <span data-ttu-id="f14d2-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f14d2-152">0x00000010</span></span>                               |
| <span data-ttu-id="f14d2-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f14d2-153">Classes used in</span></span>        | [<span data-ttu-id="f14d2-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f14d2-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f14d2-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f14d2-155">Windows Server 2003</span></span>



| <span data-ttu-id="f14d2-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14d2-156">Entry</span></span> | <span data-ttu-id="f14d2-157">Value</span><span class="sxs-lookup"><span data-stu-id="f14d2-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f14d2-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f14d2-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f14d2-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-159">MAPI-Id</span></span>                | <span data-ttu-id="f14d2-160">0x80BF</span><span class="sxs-lookup"><span data-stu-id="f14d2-160">0x80BF</span></span>                                   |
| <span data-ttu-id="f14d2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f14d2-161">System-Only</span></span>            | <span data-ttu-id="f14d2-162">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-162">True</span></span>                                     |
| <span data-ttu-id="f14d2-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f14d2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f14d2-164">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-164">True</span></span>                                     |
| <span data-ttu-id="f14d2-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f14d2-165">Is Indexed</span></span>             | <span data-ttu-id="f14d2-166">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-166">True</span></span>                                     |
| <span data-ttu-id="f14d2-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f14d2-167">In Global Catalog</span></span>      | <span data-ttu-id="f14d2-168">False</span><span class="sxs-lookup"><span data-stu-id="f14d2-168">False</span></span>                                    |
| <span data-ttu-id="f14d2-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f14d2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f14d2-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f14d2-170">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f14d2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f14d2-171">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f14d2-172">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-173">Search-Flags</span></span>           | <span data-ttu-id="f14d2-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f14d2-174">0x00000001</span></span>                               |
| <span data-ttu-id="f14d2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-175">System-Flags</span></span>           | <span data-ttu-id="f14d2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f14d2-176">0x00000010</span></span>                               |
| <span data-ttu-id="f14d2-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f14d2-177">Classes used in</span></span>        | [<span data-ttu-id="f14d2-178">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f14d2-178">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f14d2-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="f14d2-179">ADAM</span></span>



| <span data-ttu-id="f14d2-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14d2-180">Entry</span></span> | <span data-ttu-id="f14d2-181">Value</span><span class="sxs-lookup"><span data-stu-id="f14d2-181">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f14d2-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f14d2-182">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f14d2-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-183">MAPI-Id</span></span>                | <span data-ttu-id="f14d2-184">0x80BF</span><span class="sxs-lookup"><span data-stu-id="f14d2-184">0x80BF</span></span>                                   |
| <span data-ttu-id="f14d2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f14d2-185">System-Only</span></span>            | <span data-ttu-id="f14d2-186">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-186">True</span></span>                                     |
| <span data-ttu-id="f14d2-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f14d2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f14d2-188">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-188">True</span></span>                                     |
| <span data-ttu-id="f14d2-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f14d2-189">Is Indexed</span></span>             | <span data-ttu-id="f14d2-190">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-190">True</span></span>                                     |
| <span data-ttu-id="f14d2-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f14d2-191">In Global Catalog</span></span>      | <span data-ttu-id="f14d2-192">False</span><span class="sxs-lookup"><span data-stu-id="f14d2-192">False</span></span>                                    |
| <span data-ttu-id="f14d2-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f14d2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f14d2-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f14d2-194">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f14d2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f14d2-195">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f14d2-196">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-197">Search-Flags</span></span>           | <span data-ttu-id="f14d2-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f14d2-198">0x00000001</span></span>                               |
| <span data-ttu-id="f14d2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-199">System-Flags</span></span>           | <span data-ttu-id="f14d2-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f14d2-200">0x00000010</span></span>                               |
| <span data-ttu-id="f14d2-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f14d2-201">Classes used in</span></span>        | [<span data-ttu-id="f14d2-202">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f14d2-202">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f14d2-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f14d2-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f14d2-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14d2-204">Entry</span></span> | <span data-ttu-id="f14d2-205">Value</span><span class="sxs-lookup"><span data-stu-id="f14d2-205">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f14d2-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f14d2-206">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f14d2-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-207">MAPI-Id</span></span>                | <span data-ttu-id="f14d2-208">0x80BF</span><span class="sxs-lookup"><span data-stu-id="f14d2-208">0x80BF</span></span>                                   |
| <span data-ttu-id="f14d2-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f14d2-209">System-Only</span></span>            | <span data-ttu-id="f14d2-210">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-210">True</span></span>                                     |
| <span data-ttu-id="f14d2-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f14d2-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f14d2-212">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-212">True</span></span>                                     |
| <span data-ttu-id="f14d2-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f14d2-213">Is Indexed</span></span>             | <span data-ttu-id="f14d2-214">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-214">True</span></span>                                     |
| <span data-ttu-id="f14d2-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f14d2-215">In Global Catalog</span></span>      | <span data-ttu-id="f14d2-216">False</span><span class="sxs-lookup"><span data-stu-id="f14d2-216">False</span></span>                                    |
| <span data-ttu-id="f14d2-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f14d2-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f14d2-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f14d2-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f14d2-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f14d2-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f14d2-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-221">Search-Flags</span></span>           | <span data-ttu-id="f14d2-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f14d2-222">0x00000001</span></span>                               |
| <span data-ttu-id="f14d2-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-223">System-Flags</span></span>           | <span data-ttu-id="f14d2-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f14d2-224">0x00000010</span></span>                               |
| <span data-ttu-id="f14d2-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f14d2-225">Classes used in</span></span>        | [<span data-ttu-id="f14d2-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f14d2-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f14d2-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f14d2-227">Windows Server 2008</span></span>



| <span data-ttu-id="f14d2-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14d2-228">Entry</span></span> | <span data-ttu-id="f14d2-229">Value</span><span class="sxs-lookup"><span data-stu-id="f14d2-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f14d2-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f14d2-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f14d2-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-231">MAPI-Id</span></span>                | <span data-ttu-id="f14d2-232">0x80BF</span><span class="sxs-lookup"><span data-stu-id="f14d2-232">0x80BF</span></span>                                   |
| <span data-ttu-id="f14d2-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="f14d2-233">System-Only</span></span>            | <span data-ttu-id="f14d2-234">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-234">True</span></span>                                     |
| <span data-ttu-id="f14d2-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f14d2-235">Is-Single-Valued</span></span>       | <span data-ttu-id="f14d2-236">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-236">True</span></span>                                     |
| <span data-ttu-id="f14d2-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f14d2-237">Is Indexed</span></span>             | <span data-ttu-id="f14d2-238">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-238">True</span></span>                                     |
| <span data-ttu-id="f14d2-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f14d2-239">In Global Catalog</span></span>      | <span data-ttu-id="f14d2-240">False</span><span class="sxs-lookup"><span data-stu-id="f14d2-240">False</span></span>                                    |
| <span data-ttu-id="f14d2-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f14d2-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="f14d2-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f14d2-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f14d2-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f14d2-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f14d2-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-245">Search-Flags</span></span>           | <span data-ttu-id="f14d2-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f14d2-246">0x00000001</span></span>                               |
| <span data-ttu-id="f14d2-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-247">System-Flags</span></span>           | <span data-ttu-id="f14d2-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f14d2-248">0x00000010</span></span>                               |
| <span data-ttu-id="f14d2-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f14d2-249">Classes used in</span></span>        | [<span data-ttu-id="f14d2-250">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f14d2-250">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f14d2-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f14d2-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f14d2-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14d2-252">Entry</span></span> | <span data-ttu-id="f14d2-253">Value</span><span class="sxs-lookup"><span data-stu-id="f14d2-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f14d2-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f14d2-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f14d2-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-255">MAPI-Id</span></span>                | <span data-ttu-id="f14d2-256">0x80BF</span><span class="sxs-lookup"><span data-stu-id="f14d2-256">0x80BF</span></span>                                   |
| <span data-ttu-id="f14d2-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="f14d2-257">System-Only</span></span>            | <span data-ttu-id="f14d2-258">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-258">True</span></span>                                     |
| <span data-ttu-id="f14d2-259">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f14d2-259">Is-Single-Valued</span></span>       | <span data-ttu-id="f14d2-260">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-260">True</span></span>                                     |
| <span data-ttu-id="f14d2-261">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f14d2-261">Is Indexed</span></span>             | <span data-ttu-id="f14d2-262">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-262">True</span></span>                                     |
| <span data-ttu-id="f14d2-263">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f14d2-263">In Global Catalog</span></span>      | <span data-ttu-id="f14d2-264">False</span><span class="sxs-lookup"><span data-stu-id="f14d2-264">False</span></span>                                    |
| <span data-ttu-id="f14d2-265">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f14d2-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="f14d2-266">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f14d2-266">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f14d2-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f14d2-267">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f14d2-268">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-269">Search-Flags</span></span>           | <span data-ttu-id="f14d2-270">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f14d2-270">0x00000001</span></span>                               |
| <span data-ttu-id="f14d2-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-271">System-Flags</span></span>           | <span data-ttu-id="f14d2-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f14d2-272">0x00000010</span></span>                               |
| <span data-ttu-id="f14d2-273">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f14d2-273">Classes used in</span></span>        | [<span data-ttu-id="f14d2-274">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f14d2-274">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f14d2-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f14d2-275">Windows Server 2012</span></span>



| <span data-ttu-id="f14d2-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="f14d2-276">Entry</span></span> | <span data-ttu-id="f14d2-277">Value</span><span class="sxs-lookup"><span data-stu-id="f14d2-277">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f14d2-278">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f14d2-278">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f14d2-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f14d2-279">MAPI-Id</span></span>                | <span data-ttu-id="f14d2-280">0x80BF</span><span class="sxs-lookup"><span data-stu-id="f14d2-280">0x80BF</span></span>                                   |
| <span data-ttu-id="f14d2-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="f14d2-281">System-Only</span></span>            | <span data-ttu-id="f14d2-282">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-282">True</span></span>                                     |
| <span data-ttu-id="f14d2-283">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f14d2-283">Is-Single-Valued</span></span>       | <span data-ttu-id="f14d2-284">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-284">True</span></span>                                     |
| <span data-ttu-id="f14d2-285">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f14d2-285">Is Indexed</span></span>             | <span data-ttu-id="f14d2-286">True</span><span class="sxs-lookup"><span data-stu-id="f14d2-286">True</span></span>                                     |
| <span data-ttu-id="f14d2-287">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f14d2-287">In Global Catalog</span></span>      | <span data-ttu-id="f14d2-288">False</span><span class="sxs-lookup"><span data-stu-id="f14d2-288">False</span></span>                                    |
| <span data-ttu-id="f14d2-289">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f14d2-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="f14d2-290">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f14d2-290">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f14d2-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f14d2-291">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f14d2-292">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f14d2-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-293">Search-Flags</span></span>           | <span data-ttu-id="f14d2-294">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f14d2-294">0x00000001</span></span>                               |
| <span data-ttu-id="f14d2-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f14d2-295">System-Flags</span></span>           | <span data-ttu-id="f14d2-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f14d2-296">0x00000010</span></span>                               |
| <span data-ttu-id="f14d2-297">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f14d2-297">Classes used in</span></span>        | [<span data-ttu-id="f14d2-298">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f14d2-298">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 






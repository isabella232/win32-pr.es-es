---
title: Atributo MSMQ-Secure-Source
description: Esto forma parte de un objeto MSMQ, se establece mediante una llamada a la API a MQCreateQueue o MQSetProperties. Controla si MSMQ acepta mensajes solo de un origen protegido (por ejemplo, https) para esta cola.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de origen de MSMQ-protegido
- Esquema de AD de atributo de MSMQ-SecuredSource
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535974"
---
# <a name="msmq-secured-source-attribute"></a><span data-ttu-id="353ce-106">Atributo MSMQ-Secure-Source</span><span class="sxs-lookup"><span data-stu-id="353ce-106">MSMQ-Secured-Source attribute</span></span>

<span data-ttu-id="353ce-107">Esto forma parte de un objeto MSMQ, se establece mediante una llamada a la API a MQCreateQueue o MQSetProperties.</span><span class="sxs-lookup"><span data-stu-id="353ce-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="353ce-108">Controla si MSMQ acepta mensajes solo de un origen protegido (por ejemplo, https) para esta cola.</span><span class="sxs-lookup"><span data-stu-id="353ce-108">It controls whether MSMQ accepts messages only from a secured source (for example, https) for this queue.</span></span>



| <span data-ttu-id="353ce-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="353ce-109">Entry</span></span> | <span data-ttu-id="353ce-110">Value</span><span class="sxs-lookup"><span data-stu-id="353ce-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="353ce-111">CN</span><span class="sxs-lookup"><span data-stu-id="353ce-111">CN</span></span>                | <span data-ttu-id="353ce-112">Código fuente de MSMQ protegido</span><span class="sxs-lookup"><span data-stu-id="353ce-112">MSMQ-Secured-Source</span></span>                  |
| <span data-ttu-id="353ce-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="353ce-113">Ldap-Display-Name</span></span> | <span data-ttu-id="353ce-114">MSMQ-SecuredSource</span><span class="sxs-lookup"><span data-stu-id="353ce-114">MSMQ-SecuredSource</span></span>                   |
| <span data-ttu-id="353ce-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="353ce-115">Size</span></span>              | <span data-ttu-id="353ce-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="353ce-116">4 bytes</span></span>                              |
| <span data-ttu-id="353ce-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="353ce-117">Update Privilege</span></span>  | <span data-ttu-id="353ce-118">Propietario de la cola.</span><span class="sxs-lookup"><span data-stu-id="353ce-118">The queue owner.</span></span>                     |
| <span data-ttu-id="353ce-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="353ce-119">Update Frequency</span></span>  | <span data-ttu-id="353ce-120">Cuando se crea una cola.</span><span class="sxs-lookup"><span data-stu-id="353ce-120">When a queue is created.</span></span>             |
| <span data-ttu-id="353ce-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="353ce-121">Attribute-Id</span></span>      | <span data-ttu-id="353ce-122">1.2.840.113556.1.4.1713</span><span class="sxs-lookup"><span data-stu-id="353ce-122">1.2.840.113556.1.4.1713</span></span>              |
| <span data-ttu-id="353ce-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="353ce-123">System-Id-Guid</span></span>    | <span data-ttu-id="353ce-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span><span class="sxs-lookup"><span data-stu-id="353ce-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span></span> |
| <span data-ttu-id="353ce-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="353ce-125">Syntax</span></span>            | [<span data-ttu-id="353ce-126">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="353ce-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="353ce-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="353ce-127">Implementations</span></span>

-   [<span data-ttu-id="353ce-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="353ce-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="353ce-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="353ce-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="353ce-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="353ce-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="353ce-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="353ce-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="353ce-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="353ce-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="353ce-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="353ce-133">Windows Server 2003</span></span>



| <span data-ttu-id="353ce-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="353ce-134">Entry</span></span> | <span data-ttu-id="353ce-135">Value</span><span class="sxs-lookup"><span data-stu-id="353ce-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="353ce-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="353ce-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="353ce-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="353ce-138">System-Only</span></span>            | <span data-ttu-id="353ce-139">False</span><span class="sxs-lookup"><span data-stu-id="353ce-139">False</span></span>                                        |
| <span data-ttu-id="353ce-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="353ce-140">Is-Single-Valued</span></span>       | <span data-ttu-id="353ce-141">True</span><span class="sxs-lookup"><span data-stu-id="353ce-141">True</span></span>                                         |
| <span data-ttu-id="353ce-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="353ce-142">Is Indexed</span></span>             | <span data-ttu-id="353ce-143">False</span><span class="sxs-lookup"><span data-stu-id="353ce-143">False</span></span>                                        |
| <span data-ttu-id="353ce-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="353ce-144">In Global Catalog</span></span>      | <span data-ttu-id="353ce-145">True</span><span class="sxs-lookup"><span data-stu-id="353ce-145">True</span></span>                                         |
| <span data-ttu-id="353ce-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="353ce-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="353ce-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="353ce-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="353ce-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="353ce-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="353ce-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="353ce-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="353ce-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-150">Search-Flags</span></span>           | <span data-ttu-id="353ce-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="353ce-151">0x00000000</span></span>                                   |
| <span data-ttu-id="353ce-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-152">System-Flags</span></span>           | <span data-ttu-id="353ce-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="353ce-153">0x00000010</span></span>                                   |
| <span data-ttu-id="353ce-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="353ce-154">Classes used in</span></span>        | [<span data-ttu-id="353ce-155">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="353ce-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="353ce-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="353ce-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="353ce-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="353ce-157">Entry</span></span> | <span data-ttu-id="353ce-158">Value</span><span class="sxs-lookup"><span data-stu-id="353ce-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="353ce-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="353ce-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="353ce-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="353ce-161">System-Only</span></span>            | <span data-ttu-id="353ce-162">False</span><span class="sxs-lookup"><span data-stu-id="353ce-162">False</span></span>                                        |
| <span data-ttu-id="353ce-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="353ce-163">Is-Single-Valued</span></span>       | <span data-ttu-id="353ce-164">True</span><span class="sxs-lookup"><span data-stu-id="353ce-164">True</span></span>                                         |
| <span data-ttu-id="353ce-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="353ce-165">Is Indexed</span></span>             | <span data-ttu-id="353ce-166">False</span><span class="sxs-lookup"><span data-stu-id="353ce-166">False</span></span>                                        |
| <span data-ttu-id="353ce-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="353ce-167">In Global Catalog</span></span>      | <span data-ttu-id="353ce-168">True</span><span class="sxs-lookup"><span data-stu-id="353ce-168">True</span></span>                                         |
| <span data-ttu-id="353ce-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="353ce-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="353ce-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="353ce-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="353ce-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="353ce-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="353ce-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="353ce-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="353ce-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-173">Search-Flags</span></span>           | <span data-ttu-id="353ce-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="353ce-174">0x00000000</span></span>                                   |
| <span data-ttu-id="353ce-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-175">System-Flags</span></span>           | <span data-ttu-id="353ce-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="353ce-176">0x00000010</span></span>                                   |
| <span data-ttu-id="353ce-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="353ce-177">Classes used in</span></span>        | [<span data-ttu-id="353ce-178">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="353ce-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="353ce-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="353ce-179">Windows Server 2008</span></span>



| <span data-ttu-id="353ce-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="353ce-180">Entry</span></span> | <span data-ttu-id="353ce-181">Value</span><span class="sxs-lookup"><span data-stu-id="353ce-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="353ce-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="353ce-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="353ce-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="353ce-184">System-Only</span></span>            | <span data-ttu-id="353ce-185">False</span><span class="sxs-lookup"><span data-stu-id="353ce-185">False</span></span>                                        |
| <span data-ttu-id="353ce-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="353ce-186">Is-Single-Valued</span></span>       | <span data-ttu-id="353ce-187">True</span><span class="sxs-lookup"><span data-stu-id="353ce-187">True</span></span>                                         |
| <span data-ttu-id="353ce-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="353ce-188">Is Indexed</span></span>             | <span data-ttu-id="353ce-189">False</span><span class="sxs-lookup"><span data-stu-id="353ce-189">False</span></span>                                        |
| <span data-ttu-id="353ce-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="353ce-190">In Global Catalog</span></span>      | <span data-ttu-id="353ce-191">True</span><span class="sxs-lookup"><span data-stu-id="353ce-191">True</span></span>                                         |
| <span data-ttu-id="353ce-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="353ce-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="353ce-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="353ce-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="353ce-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="353ce-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="353ce-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="353ce-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="353ce-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-196">Search-Flags</span></span>           | <span data-ttu-id="353ce-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="353ce-197">0x00000000</span></span>                                   |
| <span data-ttu-id="353ce-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-198">System-Flags</span></span>           | <span data-ttu-id="353ce-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="353ce-199">0x00000010</span></span>                                   |
| <span data-ttu-id="353ce-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="353ce-200">Classes used in</span></span>        | [<span data-ttu-id="353ce-201">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="353ce-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="353ce-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="353ce-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="353ce-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="353ce-203">Entry</span></span> | <span data-ttu-id="353ce-204">Value</span><span class="sxs-lookup"><span data-stu-id="353ce-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="353ce-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="353ce-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="353ce-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="353ce-207">System-Only</span></span>            | <span data-ttu-id="353ce-208">False</span><span class="sxs-lookup"><span data-stu-id="353ce-208">False</span></span>                                        |
| <span data-ttu-id="353ce-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="353ce-209">Is-Single-Valued</span></span>       | <span data-ttu-id="353ce-210">True</span><span class="sxs-lookup"><span data-stu-id="353ce-210">True</span></span>                                         |
| <span data-ttu-id="353ce-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="353ce-211">Is Indexed</span></span>             | <span data-ttu-id="353ce-212">False</span><span class="sxs-lookup"><span data-stu-id="353ce-212">False</span></span>                                        |
| <span data-ttu-id="353ce-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="353ce-213">In Global Catalog</span></span>      | <span data-ttu-id="353ce-214">True</span><span class="sxs-lookup"><span data-stu-id="353ce-214">True</span></span>                                         |
| <span data-ttu-id="353ce-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="353ce-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="353ce-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="353ce-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="353ce-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="353ce-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="353ce-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="353ce-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="353ce-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-219">Search-Flags</span></span>           | <span data-ttu-id="353ce-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="353ce-220">0x00000000</span></span>                                   |
| <span data-ttu-id="353ce-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-221">System-Flags</span></span>           | <span data-ttu-id="353ce-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="353ce-222">0x00000010</span></span>                                   |
| <span data-ttu-id="353ce-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="353ce-223">Classes used in</span></span>        | [<span data-ttu-id="353ce-224">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="353ce-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="353ce-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="353ce-225">Windows Server 2012</span></span>



| <span data-ttu-id="353ce-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="353ce-226">Entry</span></span> | <span data-ttu-id="353ce-227">Value</span><span class="sxs-lookup"><span data-stu-id="353ce-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="353ce-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="353ce-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="353ce-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="353ce-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="353ce-230">System-Only</span></span>            | <span data-ttu-id="353ce-231">False</span><span class="sxs-lookup"><span data-stu-id="353ce-231">False</span></span>                                        |
| <span data-ttu-id="353ce-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="353ce-232">Is-Single-Valued</span></span>       | <span data-ttu-id="353ce-233">True</span><span class="sxs-lookup"><span data-stu-id="353ce-233">True</span></span>                                         |
| <span data-ttu-id="353ce-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="353ce-234">Is Indexed</span></span>             | <span data-ttu-id="353ce-235">False</span><span class="sxs-lookup"><span data-stu-id="353ce-235">False</span></span>                                        |
| <span data-ttu-id="353ce-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="353ce-236">In Global Catalog</span></span>      | <span data-ttu-id="353ce-237">True</span><span class="sxs-lookup"><span data-stu-id="353ce-237">True</span></span>                                         |
| <span data-ttu-id="353ce-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="353ce-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="353ce-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="353ce-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="353ce-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="353ce-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="353ce-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="353ce-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="353ce-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-242">Search-Flags</span></span>           | <span data-ttu-id="353ce-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="353ce-243">0x00000000</span></span>                                   |
| <span data-ttu-id="353ce-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="353ce-244">System-Flags</span></span>           | <span data-ttu-id="353ce-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="353ce-245">0x00000010</span></span>                                   |
| <span data-ttu-id="353ce-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="353ce-246">Classes used in</span></span>        | [<span data-ttu-id="353ce-247">**MSMQ-cola**</span><span class="sxs-lookup"><span data-stu-id="353ce-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 






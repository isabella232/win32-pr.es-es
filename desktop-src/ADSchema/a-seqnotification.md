---
title: Seq-Notification atributo)
description: Este atributo contiene un contador que se incrementa a diario. Este valor de contador se proporciona al servicio de seguimiento de vínculos, que agrega el valor a sus volúmenes y vincula los archivos de origen cuando se actualizan. El controlador de dominio mantiene este valor.
ms.assetid: 63fbded5-a21f-4a0e-aadc-568e199e8b9e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Seq-Notification
- seqNotification esquema de AD de atributos
topic_type:
- apiref
api_name:
- Seq-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31fc3abc61a8102ced02c87897d5e7a4f706dbbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151571"
---
# <a name="seq-notification-attribute"></a><span data-ttu-id="87d35-107">Seq-Notification atributo)</span><span class="sxs-lookup"><span data-stu-id="87d35-107">Seq-Notification attribute</span></span>

<span data-ttu-id="87d35-108">Este atributo contiene un contador que se incrementa a diario.</span><span class="sxs-lookup"><span data-stu-id="87d35-108">This attribute contains a counter that is incremented daily.</span></span> <span data-ttu-id="87d35-109">Este valor de contador se proporciona al servicio de seguimiento de vínculos, que agrega el valor a sus volúmenes y vincula los archivos de origen cuando se actualizan.</span><span class="sxs-lookup"><span data-stu-id="87d35-109">This counter value is given to the link tracking service which adds the value to its volumes and link source files when they are refreshed.</span></span> <span data-ttu-id="87d35-110">El controlador de dominio mantiene este valor.</span><span class="sxs-lookup"><span data-stu-id="87d35-110">The domain controller maintains this value.</span></span>



| <span data-ttu-id="87d35-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="87d35-111">Entry</span></span> | <span data-ttu-id="87d35-112">Value</span><span class="sxs-lookup"><span data-stu-id="87d35-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="87d35-113">CN</span><span class="sxs-lookup"><span data-stu-id="87d35-113">CN</span></span>                | <span data-ttu-id="87d35-114">Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="87d35-114">Seq-Notification</span></span>                     |
| <span data-ttu-id="87d35-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="87d35-115">Ldap-Display-Name</span></span> | <span data-ttu-id="87d35-116">seqNotification</span><span class="sxs-lookup"><span data-stu-id="87d35-116">seqNotification</span></span>                      |
| <span data-ttu-id="87d35-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="87d35-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="87d35-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="87d35-118">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="87d35-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="87d35-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="87d35-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="87d35-120">Attribute-Id</span></span>      | <span data-ttu-id="87d35-121">1.2.840.113556.1.4.504</span><span class="sxs-lookup"><span data-stu-id="87d35-121">1.2.840.113556.1.4.504</span></span>               |
| <span data-ttu-id="87d35-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="87d35-122">System-Id-Guid</span></span>    | <span data-ttu-id="87d35-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="87d35-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="87d35-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87d35-124">Syntax</span></span>            | [<span data-ttu-id="87d35-125">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="87d35-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="87d35-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="87d35-126">Implementations</span></span>

-   [<span data-ttu-id="87d35-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="87d35-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="87d35-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="87d35-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="87d35-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="87d35-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="87d35-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="87d35-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="87d35-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="87d35-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="87d35-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="87d35-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="87d35-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="87d35-133">Windows 2000 Server</span></span>



| <span data-ttu-id="87d35-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="87d35-134">Entry</span></span> | <span data-ttu-id="87d35-135">Value</span><span class="sxs-lookup"><span data-stu-id="87d35-135">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="87d35-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="87d35-136">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87d35-137">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="87d35-138">System-Only</span></span>            | <span data-ttu-id="87d35-139">False</span><span class="sxs-lookup"><span data-stu-id="87d35-139">False</span></span>                                                          |
| <span data-ttu-id="87d35-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="87d35-140">Is-Single-Valued</span></span>       | <span data-ttu-id="87d35-141">True</span><span class="sxs-lookup"><span data-stu-id="87d35-141">True</span></span>                                                           |
| <span data-ttu-id="87d35-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="87d35-142">Is Indexed</span></span>             | <span data-ttu-id="87d35-143">False</span><span class="sxs-lookup"><span data-stu-id="87d35-143">False</span></span>                                                          |
| <span data-ttu-id="87d35-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="87d35-144">In Global Catalog</span></span>      | <span data-ttu-id="87d35-145">False</span><span class="sxs-lookup"><span data-stu-id="87d35-145">False</span></span>                                                          |
| <span data-ttu-id="87d35-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="87d35-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="87d35-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87d35-147">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="87d35-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87d35-148">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87d35-149">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-150">Search-Flags</span></span>           | <span data-ttu-id="87d35-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87d35-151">0x00000000</span></span>                                                     |
| <span data-ttu-id="87d35-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-152">System-Flags</span></span>           | <span data-ttu-id="87d35-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87d35-153">0x00000010</span></span>                                                     |
| <span data-ttu-id="87d35-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="87d35-154">Classes used in</span></span>        | [<span data-ttu-id="87d35-155">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="87d35-155">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="87d35-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="87d35-156">Windows Server 2003</span></span>



| <span data-ttu-id="87d35-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="87d35-157">Entry</span></span> | <span data-ttu-id="87d35-158">Value</span><span class="sxs-lookup"><span data-stu-id="87d35-158">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="87d35-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="87d35-159">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87d35-160">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="87d35-161">System-Only</span></span>            | <span data-ttu-id="87d35-162">False</span><span class="sxs-lookup"><span data-stu-id="87d35-162">False</span></span>                                                          |
| <span data-ttu-id="87d35-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="87d35-163">Is-Single-Valued</span></span>       | <span data-ttu-id="87d35-164">True</span><span class="sxs-lookup"><span data-stu-id="87d35-164">True</span></span>                                                           |
| <span data-ttu-id="87d35-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="87d35-165">Is Indexed</span></span>             | <span data-ttu-id="87d35-166">False</span><span class="sxs-lookup"><span data-stu-id="87d35-166">False</span></span>                                                          |
| <span data-ttu-id="87d35-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="87d35-167">In Global Catalog</span></span>      | <span data-ttu-id="87d35-168">False</span><span class="sxs-lookup"><span data-stu-id="87d35-168">False</span></span>                                                          |
| <span data-ttu-id="87d35-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="87d35-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="87d35-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87d35-170">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="87d35-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87d35-171">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87d35-172">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-173">Search-Flags</span></span>           | <span data-ttu-id="87d35-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87d35-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="87d35-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-175">System-Flags</span></span>           | <span data-ttu-id="87d35-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87d35-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="87d35-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="87d35-177">Classes used in</span></span>        | [<span data-ttu-id="87d35-178">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="87d35-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="87d35-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="87d35-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="87d35-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="87d35-180">Entry</span></span> | <span data-ttu-id="87d35-181">Value</span><span class="sxs-lookup"><span data-stu-id="87d35-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="87d35-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="87d35-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87d35-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="87d35-184">System-Only</span></span>            | <span data-ttu-id="87d35-185">False</span><span class="sxs-lookup"><span data-stu-id="87d35-185">False</span></span>                                                          |
| <span data-ttu-id="87d35-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="87d35-186">Is-Single-Valued</span></span>       | <span data-ttu-id="87d35-187">True</span><span class="sxs-lookup"><span data-stu-id="87d35-187">True</span></span>                                                           |
| <span data-ttu-id="87d35-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="87d35-188">Is Indexed</span></span>             | <span data-ttu-id="87d35-189">False</span><span class="sxs-lookup"><span data-stu-id="87d35-189">False</span></span>                                                          |
| <span data-ttu-id="87d35-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="87d35-190">In Global Catalog</span></span>      | <span data-ttu-id="87d35-191">False</span><span class="sxs-lookup"><span data-stu-id="87d35-191">False</span></span>                                                          |
| <span data-ttu-id="87d35-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="87d35-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="87d35-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87d35-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="87d35-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87d35-194">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87d35-195">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-196">Search-Flags</span></span>           | <span data-ttu-id="87d35-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87d35-197">0x00000000</span></span>                                                     |
| <span data-ttu-id="87d35-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-198">System-Flags</span></span>           | <span data-ttu-id="87d35-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87d35-199">0x00000010</span></span>                                                     |
| <span data-ttu-id="87d35-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="87d35-200">Classes used in</span></span>        | [<span data-ttu-id="87d35-201">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="87d35-201">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="87d35-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87d35-202">Windows Server 2008</span></span>



| <span data-ttu-id="87d35-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="87d35-203">Entry</span></span> | <span data-ttu-id="87d35-204">Value</span><span class="sxs-lookup"><span data-stu-id="87d35-204">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="87d35-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="87d35-205">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87d35-206">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="87d35-207">System-Only</span></span>            | <span data-ttu-id="87d35-208">False</span><span class="sxs-lookup"><span data-stu-id="87d35-208">False</span></span>                                                          |
| <span data-ttu-id="87d35-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="87d35-209">Is-Single-Valued</span></span>       | <span data-ttu-id="87d35-210">True</span><span class="sxs-lookup"><span data-stu-id="87d35-210">True</span></span>                                                           |
| <span data-ttu-id="87d35-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="87d35-211">Is Indexed</span></span>             | <span data-ttu-id="87d35-212">False</span><span class="sxs-lookup"><span data-stu-id="87d35-212">False</span></span>                                                          |
| <span data-ttu-id="87d35-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="87d35-213">In Global Catalog</span></span>      | <span data-ttu-id="87d35-214">False</span><span class="sxs-lookup"><span data-stu-id="87d35-214">False</span></span>                                                          |
| <span data-ttu-id="87d35-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="87d35-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="87d35-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87d35-216">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="87d35-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87d35-217">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87d35-218">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-219">Search-Flags</span></span>           | <span data-ttu-id="87d35-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87d35-220">0x00000000</span></span>                                                     |
| <span data-ttu-id="87d35-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-221">System-Flags</span></span>           | <span data-ttu-id="87d35-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87d35-222">0x00000010</span></span>                                                     |
| <span data-ttu-id="87d35-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="87d35-223">Classes used in</span></span>        | [<span data-ttu-id="87d35-224">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="87d35-224">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="87d35-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="87d35-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="87d35-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="87d35-226">Entry</span></span> | <span data-ttu-id="87d35-227">Value</span><span class="sxs-lookup"><span data-stu-id="87d35-227">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="87d35-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="87d35-228">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87d35-229">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="87d35-230">System-Only</span></span>            | <span data-ttu-id="87d35-231">False</span><span class="sxs-lookup"><span data-stu-id="87d35-231">False</span></span>                                                          |
| <span data-ttu-id="87d35-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="87d35-232">Is-Single-Valued</span></span>       | <span data-ttu-id="87d35-233">True</span><span class="sxs-lookup"><span data-stu-id="87d35-233">True</span></span>                                                           |
| <span data-ttu-id="87d35-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="87d35-234">Is Indexed</span></span>             | <span data-ttu-id="87d35-235">False</span><span class="sxs-lookup"><span data-stu-id="87d35-235">False</span></span>                                                          |
| <span data-ttu-id="87d35-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="87d35-236">In Global Catalog</span></span>      | <span data-ttu-id="87d35-237">False</span><span class="sxs-lookup"><span data-stu-id="87d35-237">False</span></span>                                                          |
| <span data-ttu-id="87d35-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="87d35-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="87d35-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87d35-239">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="87d35-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87d35-240">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87d35-241">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-242">Search-Flags</span></span>           | <span data-ttu-id="87d35-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87d35-243">0x00000000</span></span>                                                     |
| <span data-ttu-id="87d35-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-244">System-Flags</span></span>           | <span data-ttu-id="87d35-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87d35-245">0x00000010</span></span>                                                     |
| <span data-ttu-id="87d35-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="87d35-246">Classes used in</span></span>        | [<span data-ttu-id="87d35-247">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="87d35-247">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="87d35-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87d35-248">Windows Server 2012</span></span>



| <span data-ttu-id="87d35-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="87d35-249">Entry</span></span> | <span data-ttu-id="87d35-250">Value</span><span class="sxs-lookup"><span data-stu-id="87d35-250">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="87d35-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="87d35-251">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87d35-252">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="87d35-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="87d35-253">System-Only</span></span>            | <span data-ttu-id="87d35-254">False</span><span class="sxs-lookup"><span data-stu-id="87d35-254">False</span></span>                                                          |
| <span data-ttu-id="87d35-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="87d35-255">Is-Single-Valued</span></span>       | <span data-ttu-id="87d35-256">True</span><span class="sxs-lookup"><span data-stu-id="87d35-256">True</span></span>                                                           |
| <span data-ttu-id="87d35-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="87d35-257">Is Indexed</span></span>             | <span data-ttu-id="87d35-258">False</span><span class="sxs-lookup"><span data-stu-id="87d35-258">False</span></span>                                                          |
| <span data-ttu-id="87d35-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="87d35-259">In Global Catalog</span></span>      | <span data-ttu-id="87d35-260">False</span><span class="sxs-lookup"><span data-stu-id="87d35-260">False</span></span>                                                          |
| <span data-ttu-id="87d35-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="87d35-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="87d35-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87d35-262">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="87d35-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87d35-263">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87d35-264">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="87d35-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-265">Search-Flags</span></span>           | <span data-ttu-id="87d35-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87d35-266">0x00000000</span></span>                                                     |
| <span data-ttu-id="87d35-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87d35-267">System-Flags</span></span>           | <span data-ttu-id="87d35-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87d35-268">0x00000010</span></span>                                                     |
| <span data-ttu-id="87d35-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="87d35-269">Classes used in</span></span>        | [<span data-ttu-id="87d35-270">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="87d35-270">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 






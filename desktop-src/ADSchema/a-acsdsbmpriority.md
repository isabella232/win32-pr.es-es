---
title: ACS-DSBM-atributo de prioridad
description: Este atributo contiene la prioridad de este administrador de ancho de banda de subred (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-esquema de AD de atributo de prioridad
- aCSDSBMPriority esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151907"
---
# <a name="acs-dsbm-priority-attribute"></a><span data-ttu-id="769ae-105">ACS-DSBM-atributo de prioridad</span><span class="sxs-lookup"><span data-stu-id="769ae-105">ACS-DSBM-Priority attribute</span></span>

<span data-ttu-id="769ae-106">Este atributo contiene la prioridad de este administrador de ancho de banda de subred (SBM).</span><span class="sxs-lookup"><span data-stu-id="769ae-106">This attributes contains the priority for this Subnet Bandwidth Manager (SBM).</span></span> <span data-ttu-id="769ae-107">Cuando es necesario elegir un nuevo administrador de ancho de banda de subred (DSBM), este valor se envía a otros SBMs del dominio como parte de un mensaje de uso de DSBM \_ .</span><span class="sxs-lookup"><span data-stu-id="769ae-107">When a new Designated Subnet Bandwidth Manager (DSBM) needs to be elected, this value is sent to other SBMs in the domain as part of a DSBM\_willing message.</span></span> <span data-ttu-id="769ae-108">El SBM con la prioridad más alta se elige como el nuevo DSBM.</span><span class="sxs-lookup"><span data-stu-id="769ae-108">The SBM with the highest priority is elected as the new DSBM.</span></span>



| <span data-ttu-id="769ae-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="769ae-109">Entry</span></span> | <span data-ttu-id="769ae-110">Value</span><span class="sxs-lookup"><span data-stu-id="769ae-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="769ae-111">CN</span><span class="sxs-lookup"><span data-stu-id="769ae-111">CN</span></span>                | <span data-ttu-id="769ae-112">ACS-DSBM-prioridad</span><span class="sxs-lookup"><span data-stu-id="769ae-112">ACS-DSBM-Priority</span></span>                    |
| <span data-ttu-id="769ae-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="769ae-113">Ldap-Display-Name</span></span> | <span data-ttu-id="769ae-114">aCSDSBMPriority</span><span class="sxs-lookup"><span data-stu-id="769ae-114">aCSDSBMPriority</span></span>                      |
| <span data-ttu-id="769ae-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="769ae-115">Size</span></span>              | <span data-ttu-id="769ae-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="769ae-116">4 bytes</span></span>                              |
| <span data-ttu-id="769ae-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="769ae-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="769ae-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="769ae-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="769ae-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="769ae-119">Attribute-Id</span></span>      | <span data-ttu-id="769ae-120">1.2.840.113556.1.4.776</span><span class="sxs-lookup"><span data-stu-id="769ae-120">1.2.840.113556.1.4.776</span></span>               |
| <span data-ttu-id="769ae-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="769ae-121">System-Id-Guid</span></span>    | <span data-ttu-id="769ae-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="769ae-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="769ae-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="769ae-123">Syntax</span></span>            | [<span data-ttu-id="769ae-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="769ae-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="769ae-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="769ae-125">Implementations</span></span>

-   [<span data-ttu-id="769ae-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="769ae-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="769ae-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="769ae-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="769ae-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="769ae-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="769ae-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="769ae-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="769ae-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="769ae-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="769ae-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="769ae-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="769ae-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="769ae-132">Windows 2000 Server</span></span>



| <span data-ttu-id="769ae-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="769ae-133">Entry</span></span> | <span data-ttu-id="769ae-134">Value</span><span class="sxs-lookup"><span data-stu-id="769ae-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="769ae-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="769ae-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="769ae-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="769ae-137">System-Only</span></span>            | <span data-ttu-id="769ae-138">False</span><span class="sxs-lookup"><span data-stu-id="769ae-138">False</span></span>                                        |
| <span data-ttu-id="769ae-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="769ae-139">Is-Single-Valued</span></span>       | <span data-ttu-id="769ae-140">True</span><span class="sxs-lookup"><span data-stu-id="769ae-140">True</span></span>                                         |
| <span data-ttu-id="769ae-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="769ae-141">Is Indexed</span></span>             | <span data-ttu-id="769ae-142">False</span><span class="sxs-lookup"><span data-stu-id="769ae-142">False</span></span>                                        |
| <span data-ttu-id="769ae-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="769ae-143">In Global Catalog</span></span>      | <span data-ttu-id="769ae-144">False</span><span class="sxs-lookup"><span data-stu-id="769ae-144">False</span></span>                                        |
| <span data-ttu-id="769ae-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="769ae-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="769ae-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="769ae-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="769ae-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="769ae-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="769ae-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="769ae-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="769ae-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-149">Search-Flags</span></span>           | <span data-ttu-id="769ae-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="769ae-150">0x00000000</span></span>                                   |
| <span data-ttu-id="769ae-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-151">System-Flags</span></span>           | <span data-ttu-id="769ae-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="769ae-152">0x00000010</span></span>                                   |
| <span data-ttu-id="769ae-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="769ae-153">Classes used in</span></span>        | [<span data-ttu-id="769ae-154">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="769ae-154">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="769ae-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="769ae-155">Windows Server 2003</span></span>



| <span data-ttu-id="769ae-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="769ae-156">Entry</span></span> | <span data-ttu-id="769ae-157">Value</span><span class="sxs-lookup"><span data-stu-id="769ae-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="769ae-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="769ae-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="769ae-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="769ae-160">System-Only</span></span>            | <span data-ttu-id="769ae-161">False</span><span class="sxs-lookup"><span data-stu-id="769ae-161">False</span></span>                                        |
| <span data-ttu-id="769ae-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="769ae-162">Is-Single-Valued</span></span>       | <span data-ttu-id="769ae-163">True</span><span class="sxs-lookup"><span data-stu-id="769ae-163">True</span></span>                                         |
| <span data-ttu-id="769ae-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="769ae-164">Is Indexed</span></span>             | <span data-ttu-id="769ae-165">False</span><span class="sxs-lookup"><span data-stu-id="769ae-165">False</span></span>                                        |
| <span data-ttu-id="769ae-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="769ae-166">In Global Catalog</span></span>      | <span data-ttu-id="769ae-167">False</span><span class="sxs-lookup"><span data-stu-id="769ae-167">False</span></span>                                        |
| <span data-ttu-id="769ae-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="769ae-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="769ae-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="769ae-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="769ae-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="769ae-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="769ae-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="769ae-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="769ae-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-172">Search-Flags</span></span>           | <span data-ttu-id="769ae-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="769ae-173">0x00000000</span></span>                                   |
| <span data-ttu-id="769ae-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-174">System-Flags</span></span>           | <span data-ttu-id="769ae-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="769ae-175">0x00000010</span></span>                                   |
| <span data-ttu-id="769ae-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="769ae-176">Classes used in</span></span>        | [<span data-ttu-id="769ae-177">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="769ae-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="769ae-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="769ae-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="769ae-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="769ae-179">Entry</span></span> | <span data-ttu-id="769ae-180">Value</span><span class="sxs-lookup"><span data-stu-id="769ae-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="769ae-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="769ae-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="769ae-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="769ae-183">System-Only</span></span>            | <span data-ttu-id="769ae-184">False</span><span class="sxs-lookup"><span data-stu-id="769ae-184">False</span></span>                                        |
| <span data-ttu-id="769ae-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="769ae-185">Is-Single-Valued</span></span>       | <span data-ttu-id="769ae-186">True</span><span class="sxs-lookup"><span data-stu-id="769ae-186">True</span></span>                                         |
| <span data-ttu-id="769ae-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="769ae-187">Is Indexed</span></span>             | <span data-ttu-id="769ae-188">False</span><span class="sxs-lookup"><span data-stu-id="769ae-188">False</span></span>                                        |
| <span data-ttu-id="769ae-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="769ae-189">In Global Catalog</span></span>      | <span data-ttu-id="769ae-190">False</span><span class="sxs-lookup"><span data-stu-id="769ae-190">False</span></span>                                        |
| <span data-ttu-id="769ae-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="769ae-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="769ae-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="769ae-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="769ae-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="769ae-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="769ae-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="769ae-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="769ae-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-195">Search-Flags</span></span>           | <span data-ttu-id="769ae-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="769ae-196">0x00000000</span></span>                                   |
| <span data-ttu-id="769ae-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-197">System-Flags</span></span>           | <span data-ttu-id="769ae-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="769ae-198">0x00000010</span></span>                                   |
| <span data-ttu-id="769ae-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="769ae-199">Classes used in</span></span>        | [<span data-ttu-id="769ae-200">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="769ae-200">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="769ae-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="769ae-201">Windows Server 2008</span></span>



| <span data-ttu-id="769ae-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="769ae-202">Entry</span></span> | <span data-ttu-id="769ae-203">Value</span><span class="sxs-lookup"><span data-stu-id="769ae-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="769ae-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="769ae-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="769ae-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="769ae-206">System-Only</span></span>            | <span data-ttu-id="769ae-207">False</span><span class="sxs-lookup"><span data-stu-id="769ae-207">False</span></span>                                        |
| <span data-ttu-id="769ae-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="769ae-208">Is-Single-Valued</span></span>       | <span data-ttu-id="769ae-209">True</span><span class="sxs-lookup"><span data-stu-id="769ae-209">True</span></span>                                         |
| <span data-ttu-id="769ae-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="769ae-210">Is Indexed</span></span>             | <span data-ttu-id="769ae-211">False</span><span class="sxs-lookup"><span data-stu-id="769ae-211">False</span></span>                                        |
| <span data-ttu-id="769ae-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="769ae-212">In Global Catalog</span></span>      | <span data-ttu-id="769ae-213">False</span><span class="sxs-lookup"><span data-stu-id="769ae-213">False</span></span>                                        |
| <span data-ttu-id="769ae-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="769ae-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="769ae-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="769ae-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="769ae-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="769ae-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="769ae-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="769ae-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="769ae-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-218">Search-Flags</span></span>           | <span data-ttu-id="769ae-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="769ae-219">0x00000000</span></span>                                   |
| <span data-ttu-id="769ae-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-220">System-Flags</span></span>           | <span data-ttu-id="769ae-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="769ae-221">0x00000010</span></span>                                   |
| <span data-ttu-id="769ae-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="769ae-222">Classes used in</span></span>        | [<span data-ttu-id="769ae-223">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="769ae-223">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="769ae-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="769ae-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="769ae-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="769ae-225">Entry</span></span> | <span data-ttu-id="769ae-226">Value</span><span class="sxs-lookup"><span data-stu-id="769ae-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="769ae-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="769ae-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="769ae-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="769ae-229">System-Only</span></span>            | <span data-ttu-id="769ae-230">False</span><span class="sxs-lookup"><span data-stu-id="769ae-230">False</span></span>                                        |
| <span data-ttu-id="769ae-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="769ae-231">Is-Single-Valued</span></span>       | <span data-ttu-id="769ae-232">True</span><span class="sxs-lookup"><span data-stu-id="769ae-232">True</span></span>                                         |
| <span data-ttu-id="769ae-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="769ae-233">Is Indexed</span></span>             | <span data-ttu-id="769ae-234">False</span><span class="sxs-lookup"><span data-stu-id="769ae-234">False</span></span>                                        |
| <span data-ttu-id="769ae-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="769ae-235">In Global Catalog</span></span>      | <span data-ttu-id="769ae-236">False</span><span class="sxs-lookup"><span data-stu-id="769ae-236">False</span></span>                                        |
| <span data-ttu-id="769ae-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="769ae-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="769ae-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="769ae-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="769ae-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="769ae-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="769ae-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="769ae-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="769ae-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-241">Search-Flags</span></span>           | <span data-ttu-id="769ae-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="769ae-242">0x00000000</span></span>                                   |
| <span data-ttu-id="769ae-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-243">System-Flags</span></span>           | <span data-ttu-id="769ae-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="769ae-244">0x00000010</span></span>                                   |
| <span data-ttu-id="769ae-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="769ae-245">Classes used in</span></span>        | [<span data-ttu-id="769ae-246">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="769ae-246">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="769ae-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="769ae-247">Windows Server 2012</span></span>



| <span data-ttu-id="769ae-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="769ae-248">Entry</span></span> | <span data-ttu-id="769ae-249">Value</span><span class="sxs-lookup"><span data-stu-id="769ae-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="769ae-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="769ae-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="769ae-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="769ae-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="769ae-252">System-Only</span></span>            | <span data-ttu-id="769ae-253">False</span><span class="sxs-lookup"><span data-stu-id="769ae-253">False</span></span>                                        |
| <span data-ttu-id="769ae-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="769ae-254">Is-Single-Valued</span></span>       | <span data-ttu-id="769ae-255">True</span><span class="sxs-lookup"><span data-stu-id="769ae-255">True</span></span>                                         |
| <span data-ttu-id="769ae-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="769ae-256">Is Indexed</span></span>             | <span data-ttu-id="769ae-257">False</span><span class="sxs-lookup"><span data-stu-id="769ae-257">False</span></span>                                        |
| <span data-ttu-id="769ae-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="769ae-258">In Global Catalog</span></span>      | <span data-ttu-id="769ae-259">False</span><span class="sxs-lookup"><span data-stu-id="769ae-259">False</span></span>                                        |
| <span data-ttu-id="769ae-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="769ae-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="769ae-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="769ae-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="769ae-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="769ae-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="769ae-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="769ae-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="769ae-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-264">Search-Flags</span></span>           | <span data-ttu-id="769ae-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="769ae-265">0x00000000</span></span>                                   |
| <span data-ttu-id="769ae-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="769ae-266">System-Flags</span></span>           | <span data-ttu-id="769ae-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="769ae-267">0x00000010</span></span>                                   |
| <span data-ttu-id="769ae-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="769ae-268">Classes used in</span></span>        | [<span data-ttu-id="769ae-269">**ACS-subred**</span><span class="sxs-lookup"><span data-stu-id="769ae-269">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 






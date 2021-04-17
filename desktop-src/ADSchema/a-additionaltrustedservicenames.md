---
title: Atributo de nombre de servicio de confianza adicional
description: Una lista de los servicios del dominio en los que se puede confiar. No se usa en AD.
ms.assetid: 0c574a99-4036-408b-807c-b4b3394624c7
ms.tgt_platform: multiple
keywords:
- Atributo de nombre de servicio de nombres de servicio de confianza adicional
- additionalTrustedServiceNames esquema de AD de atributos
topic_type:
- apiref
api_name:
- Additional-Trusted-Service-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8066190082cfe0f1bbb8825768ad135090a7a4f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659234"
---
# <a name="additional-trusted-service-names-attribute"></a><span data-ttu-id="2907a-106">Atributo de nombre de servicio de confianza adicional</span><span class="sxs-lookup"><span data-stu-id="2907a-106">Additional-Trusted-Service-Names attribute</span></span>

<span data-ttu-id="2907a-107">Una lista de los servicios del dominio en los que se puede confiar.</span><span class="sxs-lookup"><span data-stu-id="2907a-107">A list of services in the domain that can be trusted.</span></span> <span data-ttu-id="2907a-108">No se usa en AD.</span><span class="sxs-lookup"><span data-stu-id="2907a-108">Not used by AD.</span></span>



| <span data-ttu-id="2907a-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="2907a-109">Entry</span></span> | <span data-ttu-id="2907a-110">Value</span><span class="sxs-lookup"><span data-stu-id="2907a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2907a-111">CN</span><span class="sxs-lookup"><span data-stu-id="2907a-111">CN</span></span>                | <span data-ttu-id="2907a-112">Nombres de servicio de confianza adicionales</span><span class="sxs-lookup"><span data-stu-id="2907a-112">Additional-Trusted-Service-Names</span></span>            |
| <span data-ttu-id="2907a-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="2907a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2907a-114">additionalTrustedServiceNames</span><span class="sxs-lookup"><span data-stu-id="2907a-114">additionalTrustedServiceNames</span></span>               |
| <span data-ttu-id="2907a-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="2907a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="2907a-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="2907a-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="2907a-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="2907a-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="2907a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2907a-118">Attribute-Id</span></span>      | <span data-ttu-id="2907a-119">1.2.840.113556.1.4.889</span><span class="sxs-lookup"><span data-stu-id="2907a-119">1.2.840.113556.1.4.889</span></span>                      |
| <span data-ttu-id="2907a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2907a-120">System-Id-Guid</span></span>    | <span data-ttu-id="2907a-121">032160be-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2907a-121">032160be-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="2907a-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2907a-122">Syntax</span></span>            | [<span data-ttu-id="2907a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="2907a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2907a-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="2907a-124">Implementations</span></span>

-   [<span data-ttu-id="2907a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2907a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2907a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2907a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2907a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2907a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2907a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2907a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2907a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2907a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2907a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2907a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2907a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2907a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2907a-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="2907a-132">Entry</span></span> | <span data-ttu-id="2907a-133">Value</span><span class="sxs-lookup"><span data-stu-id="2907a-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2907a-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2907a-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2907a-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="2907a-136">System-Only</span></span>            | <span data-ttu-id="2907a-137">False</span><span class="sxs-lookup"><span data-stu-id="2907a-137">False</span></span>                                                |
| <span data-ttu-id="2907a-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2907a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="2907a-139">False</span><span class="sxs-lookup"><span data-stu-id="2907a-139">False</span></span>                                                |
| <span data-ttu-id="2907a-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2907a-140">Is Indexed</span></span>             | <span data-ttu-id="2907a-141">False</span><span class="sxs-lookup"><span data-stu-id="2907a-141">False</span></span>                                                |
| <span data-ttu-id="2907a-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2907a-142">In Global Catalog</span></span>      | <span data-ttu-id="2907a-143">False</span><span class="sxs-lookup"><span data-stu-id="2907a-143">False</span></span>                                                |
| <span data-ttu-id="2907a-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2907a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="2907a-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2907a-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2907a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2907a-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2907a-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-148">Search-Flags</span></span>           | <span data-ttu-id="2907a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2907a-149">0x00000000</span></span>                                           |
| <span data-ttu-id="2907a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-150">System-Flags</span></span>           | <span data-ttu-id="2907a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2907a-151">0x00000010</span></span>                                           |
| <span data-ttu-id="2907a-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2907a-152">Classes used in</span></span>        | [<span data-ttu-id="2907a-153">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2907a-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2907a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2907a-154">Windows Server 2003</span></span>



| <span data-ttu-id="2907a-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="2907a-155">Entry</span></span> | <span data-ttu-id="2907a-156">Value</span><span class="sxs-lookup"><span data-stu-id="2907a-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2907a-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2907a-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2907a-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="2907a-159">System-Only</span></span>            | <span data-ttu-id="2907a-160">False</span><span class="sxs-lookup"><span data-stu-id="2907a-160">False</span></span>                                                |
| <span data-ttu-id="2907a-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2907a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="2907a-162">False</span><span class="sxs-lookup"><span data-stu-id="2907a-162">False</span></span>                                                |
| <span data-ttu-id="2907a-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2907a-163">Is Indexed</span></span>             | <span data-ttu-id="2907a-164">False</span><span class="sxs-lookup"><span data-stu-id="2907a-164">False</span></span>                                                |
| <span data-ttu-id="2907a-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2907a-165">In Global Catalog</span></span>      | <span data-ttu-id="2907a-166">False</span><span class="sxs-lookup"><span data-stu-id="2907a-166">False</span></span>                                                |
| <span data-ttu-id="2907a-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2907a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="2907a-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2907a-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2907a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2907a-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2907a-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-171">Search-Flags</span></span>           | <span data-ttu-id="2907a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2907a-172">0x00000000</span></span>                                           |
| <span data-ttu-id="2907a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-173">System-Flags</span></span>           | <span data-ttu-id="2907a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2907a-174">0x00000010</span></span>                                           |
| <span data-ttu-id="2907a-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2907a-175">Classes used in</span></span>        | [<span data-ttu-id="2907a-176">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2907a-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2907a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2907a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2907a-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="2907a-178">Entry</span></span> | <span data-ttu-id="2907a-179">Value</span><span class="sxs-lookup"><span data-stu-id="2907a-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2907a-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2907a-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2907a-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="2907a-182">System-Only</span></span>            | <span data-ttu-id="2907a-183">False</span><span class="sxs-lookup"><span data-stu-id="2907a-183">False</span></span>                                                |
| <span data-ttu-id="2907a-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2907a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="2907a-185">False</span><span class="sxs-lookup"><span data-stu-id="2907a-185">False</span></span>                                                |
| <span data-ttu-id="2907a-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2907a-186">Is Indexed</span></span>             | <span data-ttu-id="2907a-187">False</span><span class="sxs-lookup"><span data-stu-id="2907a-187">False</span></span>                                                |
| <span data-ttu-id="2907a-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2907a-188">In Global Catalog</span></span>      | <span data-ttu-id="2907a-189">False</span><span class="sxs-lookup"><span data-stu-id="2907a-189">False</span></span>                                                |
| <span data-ttu-id="2907a-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2907a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="2907a-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2907a-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2907a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2907a-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2907a-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-194">Search-Flags</span></span>           | <span data-ttu-id="2907a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2907a-195">0x00000000</span></span>                                           |
| <span data-ttu-id="2907a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-196">System-Flags</span></span>           | <span data-ttu-id="2907a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2907a-197">0x00000010</span></span>                                           |
| <span data-ttu-id="2907a-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2907a-198">Classes used in</span></span>        | [<span data-ttu-id="2907a-199">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2907a-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2907a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2907a-200">Windows Server 2008</span></span>



| <span data-ttu-id="2907a-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="2907a-201">Entry</span></span> | <span data-ttu-id="2907a-202">Value</span><span class="sxs-lookup"><span data-stu-id="2907a-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2907a-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2907a-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2907a-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="2907a-205">System-Only</span></span>            | <span data-ttu-id="2907a-206">False</span><span class="sxs-lookup"><span data-stu-id="2907a-206">False</span></span>                                                |
| <span data-ttu-id="2907a-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2907a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="2907a-208">False</span><span class="sxs-lookup"><span data-stu-id="2907a-208">False</span></span>                                                |
| <span data-ttu-id="2907a-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2907a-209">Is Indexed</span></span>             | <span data-ttu-id="2907a-210">False</span><span class="sxs-lookup"><span data-stu-id="2907a-210">False</span></span>                                                |
| <span data-ttu-id="2907a-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2907a-211">In Global Catalog</span></span>      | <span data-ttu-id="2907a-212">False</span><span class="sxs-lookup"><span data-stu-id="2907a-212">False</span></span>                                                |
| <span data-ttu-id="2907a-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2907a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="2907a-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2907a-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2907a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2907a-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2907a-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-217">Search-Flags</span></span>           | <span data-ttu-id="2907a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2907a-218">0x00000000</span></span>                                           |
| <span data-ttu-id="2907a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-219">System-Flags</span></span>           | <span data-ttu-id="2907a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2907a-220">0x00000010</span></span>                                           |
| <span data-ttu-id="2907a-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2907a-221">Classes used in</span></span>        | [<span data-ttu-id="2907a-222">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2907a-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2907a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2907a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2907a-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="2907a-224">Entry</span></span> | <span data-ttu-id="2907a-225">Value</span><span class="sxs-lookup"><span data-stu-id="2907a-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2907a-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2907a-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2907a-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="2907a-228">System-Only</span></span>            | <span data-ttu-id="2907a-229">False</span><span class="sxs-lookup"><span data-stu-id="2907a-229">False</span></span>                                                |
| <span data-ttu-id="2907a-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2907a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="2907a-231">False</span><span class="sxs-lookup"><span data-stu-id="2907a-231">False</span></span>                                                |
| <span data-ttu-id="2907a-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2907a-232">Is Indexed</span></span>             | <span data-ttu-id="2907a-233">False</span><span class="sxs-lookup"><span data-stu-id="2907a-233">False</span></span>                                                |
| <span data-ttu-id="2907a-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2907a-234">In Global Catalog</span></span>      | <span data-ttu-id="2907a-235">False</span><span class="sxs-lookup"><span data-stu-id="2907a-235">False</span></span>                                                |
| <span data-ttu-id="2907a-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2907a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="2907a-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2907a-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2907a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2907a-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2907a-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-240">Search-Flags</span></span>           | <span data-ttu-id="2907a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2907a-241">0x00000000</span></span>                                           |
| <span data-ttu-id="2907a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-242">System-Flags</span></span>           | <span data-ttu-id="2907a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2907a-243">0x00000010</span></span>                                           |
| <span data-ttu-id="2907a-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2907a-244">Classes used in</span></span>        | [<span data-ttu-id="2907a-245">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2907a-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2907a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2907a-246">Windows Server 2012</span></span>



| <span data-ttu-id="2907a-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="2907a-247">Entry</span></span> | <span data-ttu-id="2907a-248">Value</span><span class="sxs-lookup"><span data-stu-id="2907a-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2907a-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="2907a-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2907a-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2907a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="2907a-251">System-Only</span></span>            | <span data-ttu-id="2907a-252">False</span><span class="sxs-lookup"><span data-stu-id="2907a-252">False</span></span>                                                |
| <span data-ttu-id="2907a-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="2907a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="2907a-254">False</span><span class="sxs-lookup"><span data-stu-id="2907a-254">False</span></span>                                                |
| <span data-ttu-id="2907a-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="2907a-255">Is Indexed</span></span>             | <span data-ttu-id="2907a-256">False</span><span class="sxs-lookup"><span data-stu-id="2907a-256">False</span></span>                                                |
| <span data-ttu-id="2907a-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="2907a-257">In Global Catalog</span></span>      | <span data-ttu-id="2907a-258">False</span><span class="sxs-lookup"><span data-stu-id="2907a-258">False</span></span>                                                |
| <span data-ttu-id="2907a-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="2907a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="2907a-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2907a-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2907a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2907a-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2907a-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2907a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-263">Search-Flags</span></span>           | <span data-ttu-id="2907a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2907a-264">0x00000000</span></span>                                           |
| <span data-ttu-id="2907a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2907a-265">System-Flags</span></span>           | <span data-ttu-id="2907a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2907a-266">0x00000010</span></span>                                           |
| <span data-ttu-id="2907a-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="2907a-267">Classes used in</span></span>        | [<span data-ttu-id="2907a-268">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="2907a-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






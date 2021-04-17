---
title: Dominio-atributo de referencia cruzada
description: Se trata de una referencia de un objeto de dominio de confianza al objeto de referencia cruzada del dominio de confianza.
ms.assetid: aa6fe6f9-a45c-448c-9fc5-17bc2994c764
ms.tgt_platform: multiple
keywords:
- Dominio-esquema de AD de atributo de referencia cruzada
- domainCrossRef esquema de AD de atributos
topic_type:
- apiref
api_name:
- Domain-Cross-Ref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b85e1293ce8141a3614c9401dbb34c1031de5935
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658551"
---
# <a name="domain-cross-ref-attribute"></a><span data-ttu-id="c336b-105">Dominio-atributo de referencia cruzada</span><span class="sxs-lookup"><span data-stu-id="c336b-105">Domain-Cross-Ref attribute</span></span>

<span data-ttu-id="c336b-106">Se trata de una referencia de un objeto de dominio de confianza al objeto de referencia cruzada del dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="c336b-106">This is a reference from a trusted domain object to the cross reference object of the trusted domain.</span></span>



| <span data-ttu-id="c336b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c336b-107">Entry</span></span> | <span data-ttu-id="c336b-108">Value</span><span class="sxs-lookup"><span data-stu-id="c336b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c336b-109">CN</span><span class="sxs-lookup"><span data-stu-id="c336b-109">CN</span></span>                | <span data-ttu-id="c336b-110">Dominio-referencia cruzada</span><span class="sxs-lookup"><span data-stu-id="c336b-110">Domain-Cross-Ref</span></span>                        |
| <span data-ttu-id="c336b-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c336b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c336b-112">domainCrossRef</span><span class="sxs-lookup"><span data-stu-id="c336b-112">domainCrossRef</span></span>                          |
| <span data-ttu-id="c336b-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c336b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c336b-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c336b-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c336b-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c336b-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c336b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c336b-116">Attribute-Id</span></span>      | <span data-ttu-id="c336b-117">1.2.840.113556.1.4.472</span><span class="sxs-lookup"><span data-stu-id="c336b-117">1.2.840.113556.1.4.472</span></span>                  |
| <span data-ttu-id="c336b-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c336b-118">System-Id-Guid</span></span>    | <span data-ttu-id="c336b-119">b000ea7b-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c336b-119">b000ea7b-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="c336b-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c336b-120">Syntax</span></span>            | [<span data-ttu-id="c336b-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c336b-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c336b-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c336b-122">Implementations</span></span>

-   [<span data-ttu-id="c336b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c336b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c336b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c336b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c336b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c336b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c336b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c336b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c336b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c336b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c336b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c336b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c336b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c336b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c336b-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="c336b-130">Entry</span></span> | <span data-ttu-id="c336b-131">Value</span><span class="sxs-lookup"><span data-stu-id="c336b-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c336b-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c336b-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c336b-133">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c336b-134">System-Only</span></span>            | <span data-ttu-id="c336b-135">False</span><span class="sxs-lookup"><span data-stu-id="c336b-135">False</span></span>                                                |
| <span data-ttu-id="c336b-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c336b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c336b-137">True</span><span class="sxs-lookup"><span data-stu-id="c336b-137">True</span></span>                                                 |
| <span data-ttu-id="c336b-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c336b-138">Is Indexed</span></span>             | <span data-ttu-id="c336b-139">False</span><span class="sxs-lookup"><span data-stu-id="c336b-139">False</span></span>                                                |
| <span data-ttu-id="c336b-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c336b-140">In Global Catalog</span></span>      | <span data-ttu-id="c336b-141">False</span><span class="sxs-lookup"><span data-stu-id="c336b-141">False</span></span>                                                |
| <span data-ttu-id="c336b-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c336b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c336b-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c336b-143">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c336b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c336b-144">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c336b-145">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-146">Search-Flags</span></span>           | <span data-ttu-id="c336b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c336b-147">0x00000000</span></span>                                           |
| <span data-ttu-id="c336b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-148">System-Flags</span></span>           | <span data-ttu-id="c336b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c336b-149">0x00000010</span></span>                                           |
| <span data-ttu-id="c336b-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c336b-150">Classes used in</span></span>        | [<span data-ttu-id="c336b-151">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="c336b-151">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c336b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c336b-152">Windows Server 2003</span></span>



| <span data-ttu-id="c336b-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="c336b-153">Entry</span></span> | <span data-ttu-id="c336b-154">Value</span><span class="sxs-lookup"><span data-stu-id="c336b-154">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c336b-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c336b-155">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c336b-156">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c336b-157">System-Only</span></span>            | <span data-ttu-id="c336b-158">False</span><span class="sxs-lookup"><span data-stu-id="c336b-158">False</span></span>                                                |
| <span data-ttu-id="c336b-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c336b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c336b-160">True</span><span class="sxs-lookup"><span data-stu-id="c336b-160">True</span></span>                                                 |
| <span data-ttu-id="c336b-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c336b-161">Is Indexed</span></span>             | <span data-ttu-id="c336b-162">False</span><span class="sxs-lookup"><span data-stu-id="c336b-162">False</span></span>                                                |
| <span data-ttu-id="c336b-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c336b-163">In Global Catalog</span></span>      | <span data-ttu-id="c336b-164">False</span><span class="sxs-lookup"><span data-stu-id="c336b-164">False</span></span>                                                |
| <span data-ttu-id="c336b-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c336b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c336b-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c336b-166">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c336b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c336b-167">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c336b-168">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-169">Search-Flags</span></span>           | <span data-ttu-id="c336b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c336b-170">0x00000000</span></span>                                           |
| <span data-ttu-id="c336b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-171">System-Flags</span></span>           | <span data-ttu-id="c336b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c336b-172">0x00000010</span></span>                                           |
| <span data-ttu-id="c336b-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c336b-173">Classes used in</span></span>        | [<span data-ttu-id="c336b-174">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="c336b-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c336b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c336b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c336b-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="c336b-176">Entry</span></span> | <span data-ttu-id="c336b-177">Value</span><span class="sxs-lookup"><span data-stu-id="c336b-177">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c336b-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c336b-178">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c336b-179">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c336b-180">System-Only</span></span>            | <span data-ttu-id="c336b-181">False</span><span class="sxs-lookup"><span data-stu-id="c336b-181">False</span></span>                                                |
| <span data-ttu-id="c336b-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c336b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c336b-183">True</span><span class="sxs-lookup"><span data-stu-id="c336b-183">True</span></span>                                                 |
| <span data-ttu-id="c336b-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c336b-184">Is Indexed</span></span>             | <span data-ttu-id="c336b-185">False</span><span class="sxs-lookup"><span data-stu-id="c336b-185">False</span></span>                                                |
| <span data-ttu-id="c336b-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c336b-186">In Global Catalog</span></span>      | <span data-ttu-id="c336b-187">False</span><span class="sxs-lookup"><span data-stu-id="c336b-187">False</span></span>                                                |
| <span data-ttu-id="c336b-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c336b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c336b-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c336b-189">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c336b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c336b-190">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c336b-191">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-192">Search-Flags</span></span>           | <span data-ttu-id="c336b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c336b-193">0x00000000</span></span>                                           |
| <span data-ttu-id="c336b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-194">System-Flags</span></span>           | <span data-ttu-id="c336b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c336b-195">0x00000010</span></span>                                           |
| <span data-ttu-id="c336b-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c336b-196">Classes used in</span></span>        | [<span data-ttu-id="c336b-197">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="c336b-197">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c336b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c336b-198">Windows Server 2008</span></span>



| <span data-ttu-id="c336b-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="c336b-199">Entry</span></span> | <span data-ttu-id="c336b-200">Value</span><span class="sxs-lookup"><span data-stu-id="c336b-200">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c336b-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c336b-201">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c336b-202">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c336b-203">System-Only</span></span>            | <span data-ttu-id="c336b-204">False</span><span class="sxs-lookup"><span data-stu-id="c336b-204">False</span></span>                                                |
| <span data-ttu-id="c336b-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c336b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c336b-206">True</span><span class="sxs-lookup"><span data-stu-id="c336b-206">True</span></span>                                                 |
| <span data-ttu-id="c336b-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c336b-207">Is Indexed</span></span>             | <span data-ttu-id="c336b-208">False</span><span class="sxs-lookup"><span data-stu-id="c336b-208">False</span></span>                                                |
| <span data-ttu-id="c336b-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c336b-209">In Global Catalog</span></span>      | <span data-ttu-id="c336b-210">False</span><span class="sxs-lookup"><span data-stu-id="c336b-210">False</span></span>                                                |
| <span data-ttu-id="c336b-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c336b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c336b-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c336b-212">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c336b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c336b-213">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c336b-214">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-215">Search-Flags</span></span>           | <span data-ttu-id="c336b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c336b-216">0x00000000</span></span>                                           |
| <span data-ttu-id="c336b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-217">System-Flags</span></span>           | <span data-ttu-id="c336b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c336b-218">0x00000010</span></span>                                           |
| <span data-ttu-id="c336b-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c336b-219">Classes used in</span></span>        | [<span data-ttu-id="c336b-220">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="c336b-220">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c336b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c336b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c336b-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="c336b-222">Entry</span></span> | <span data-ttu-id="c336b-223">Value</span><span class="sxs-lookup"><span data-stu-id="c336b-223">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c336b-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c336b-224">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c336b-225">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c336b-226">System-Only</span></span>            | <span data-ttu-id="c336b-227">False</span><span class="sxs-lookup"><span data-stu-id="c336b-227">False</span></span>                                                |
| <span data-ttu-id="c336b-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c336b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c336b-229">True</span><span class="sxs-lookup"><span data-stu-id="c336b-229">True</span></span>                                                 |
| <span data-ttu-id="c336b-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c336b-230">Is Indexed</span></span>             | <span data-ttu-id="c336b-231">False</span><span class="sxs-lookup"><span data-stu-id="c336b-231">False</span></span>                                                |
| <span data-ttu-id="c336b-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c336b-232">In Global Catalog</span></span>      | <span data-ttu-id="c336b-233">False</span><span class="sxs-lookup"><span data-stu-id="c336b-233">False</span></span>                                                |
| <span data-ttu-id="c336b-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c336b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c336b-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c336b-235">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c336b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c336b-236">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c336b-237">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-238">Search-Flags</span></span>           | <span data-ttu-id="c336b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c336b-239">0x00000000</span></span>                                           |
| <span data-ttu-id="c336b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-240">System-Flags</span></span>           | <span data-ttu-id="c336b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c336b-241">0x00000010</span></span>                                           |
| <span data-ttu-id="c336b-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c336b-242">Classes used in</span></span>        | [<span data-ttu-id="c336b-243">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="c336b-243">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c336b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c336b-244">Windows Server 2012</span></span>



| <span data-ttu-id="c336b-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="c336b-245">Entry</span></span> | <span data-ttu-id="c336b-246">Value</span><span class="sxs-lookup"><span data-stu-id="c336b-246">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c336b-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c336b-247">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c336b-248">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c336b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c336b-249">System-Only</span></span>            | <span data-ttu-id="c336b-250">False</span><span class="sxs-lookup"><span data-stu-id="c336b-250">False</span></span>                                                |
| <span data-ttu-id="c336b-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c336b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c336b-252">True</span><span class="sxs-lookup"><span data-stu-id="c336b-252">True</span></span>                                                 |
| <span data-ttu-id="c336b-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c336b-253">Is Indexed</span></span>             | <span data-ttu-id="c336b-254">False</span><span class="sxs-lookup"><span data-stu-id="c336b-254">False</span></span>                                                |
| <span data-ttu-id="c336b-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c336b-255">In Global Catalog</span></span>      | <span data-ttu-id="c336b-256">False</span><span class="sxs-lookup"><span data-stu-id="c336b-256">False</span></span>                                                |
| <span data-ttu-id="c336b-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c336b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c336b-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c336b-258">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c336b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c336b-259">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c336b-260">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c336b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-261">Search-Flags</span></span>           | <span data-ttu-id="c336b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c336b-262">0x00000000</span></span>                                           |
| <span data-ttu-id="c336b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c336b-263">System-Flags</span></span>           | <span data-ttu-id="c336b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c336b-264">0x00000010</span></span>                                           |
| <span data-ttu-id="c336b-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c336b-265">Classes used in</span></span>        | [<span data-ttu-id="c336b-266">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="c336b-266">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






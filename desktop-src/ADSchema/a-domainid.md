---
title: Atributo domain-ID
description: Referencia a un dominio que está asociado a una entidad de certificación.
ms.assetid: dd2f0822-cf94-485b-8d21-8954dddb81ad
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de ID. de dominio
- domainID esquema de AD de atributos
topic_type:
- apiref
api_name:
- Domain-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6c321fdea062ccbca907e22a2d72b06c26110ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422663"
---
# <a name="domain-id-attribute"></a><span data-ttu-id="dc22b-105">Atributo domain-ID</span><span class="sxs-lookup"><span data-stu-id="dc22b-105">Domain-ID attribute</span></span>

<span data-ttu-id="dc22b-106">Referencia a un dominio que está asociado a una entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="dc22b-106">Reference to a domain that is associated with a certification authority.</span></span>



| <span data-ttu-id="dc22b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc22b-107">Entry</span></span> | <span data-ttu-id="dc22b-108">Value</span><span class="sxs-lookup"><span data-stu-id="dc22b-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="dc22b-109">CN</span><span class="sxs-lookup"><span data-stu-id="dc22b-109">CN</span></span>                | <span data-ttu-id="dc22b-110">IDENTIFICADOR de dominio</span><span class="sxs-lookup"><span data-stu-id="dc22b-110">Domain-ID</span></span>                               |
| <span data-ttu-id="dc22b-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="dc22b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dc22b-112">domainID</span><span class="sxs-lookup"><span data-stu-id="dc22b-112">domainID</span></span>                                |
| <span data-ttu-id="dc22b-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="dc22b-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="dc22b-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="dc22b-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="dc22b-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="dc22b-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="dc22b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dc22b-116">Attribute-Id</span></span>      | <span data-ttu-id="dc22b-117">1.2.840.113556.1.4.686</span><span class="sxs-lookup"><span data-stu-id="dc22b-117">1.2.840.113556.1.4.686</span></span>                  |
| <span data-ttu-id="dc22b-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dc22b-118">System-Id-Guid</span></span>    | <span data-ttu-id="dc22b-119">963d2734-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="dc22b-119">963d2734-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="dc22b-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc22b-120">Syntax</span></span>            | [<span data-ttu-id="dc22b-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="dc22b-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="dc22b-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="dc22b-122">Implementations</span></span>

-   [<span data-ttu-id="dc22b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dc22b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dc22b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dc22b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dc22b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dc22b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dc22b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dc22b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dc22b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dc22b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dc22b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dc22b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dc22b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc22b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="dc22b-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc22b-130">Entry</span></span> | <span data-ttu-id="dc22b-131">Value</span><span class="sxs-lookup"><span data-stu-id="dc22b-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dc22b-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc22b-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc22b-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc22b-134">System-Only</span></span>            | <span data-ttu-id="dc22b-135">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-135">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc22b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="dc22b-137">True</span><span class="sxs-lookup"><span data-stu-id="dc22b-137">True</span></span>                                                                   |
| <span data-ttu-id="dc22b-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc22b-138">Is Indexed</span></span>             | <span data-ttu-id="dc22b-139">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-139">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc22b-140">In Global Catalog</span></span>      | <span data-ttu-id="dc22b-141">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-141">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc22b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc22b-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc22b-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dc22b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc22b-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc22b-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-146">Search-Flags</span></span>           | <span data-ttu-id="dc22b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc22b-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="dc22b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-148">System-Flags</span></span>           | <span data-ttu-id="dc22b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc22b-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="dc22b-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc22b-150">Classes used in</span></span>        | [<span data-ttu-id="dc22b-151">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dc22b-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dc22b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc22b-152">Windows Server 2003</span></span>



| <span data-ttu-id="dc22b-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc22b-153">Entry</span></span> | <span data-ttu-id="dc22b-154">Value</span><span class="sxs-lookup"><span data-stu-id="dc22b-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dc22b-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc22b-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc22b-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc22b-157">System-Only</span></span>            | <span data-ttu-id="dc22b-158">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-158">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc22b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="dc22b-160">True</span><span class="sxs-lookup"><span data-stu-id="dc22b-160">True</span></span>                                                                   |
| <span data-ttu-id="dc22b-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc22b-161">Is Indexed</span></span>             | <span data-ttu-id="dc22b-162">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-162">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc22b-163">In Global Catalog</span></span>      | <span data-ttu-id="dc22b-164">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-164">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc22b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc22b-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc22b-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dc22b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc22b-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc22b-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-169">Search-Flags</span></span>           | <span data-ttu-id="dc22b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc22b-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="dc22b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-171">System-Flags</span></span>           | <span data-ttu-id="dc22b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc22b-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="dc22b-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc22b-173">Classes used in</span></span>        | [<span data-ttu-id="dc22b-174">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dc22b-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dc22b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dc22b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dc22b-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc22b-176">Entry</span></span> | <span data-ttu-id="dc22b-177">Value</span><span class="sxs-lookup"><span data-stu-id="dc22b-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dc22b-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc22b-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc22b-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc22b-180">System-Only</span></span>            | <span data-ttu-id="dc22b-181">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-181">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc22b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="dc22b-183">True</span><span class="sxs-lookup"><span data-stu-id="dc22b-183">True</span></span>                                                                   |
| <span data-ttu-id="dc22b-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc22b-184">Is Indexed</span></span>             | <span data-ttu-id="dc22b-185">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-185">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc22b-186">In Global Catalog</span></span>      | <span data-ttu-id="dc22b-187">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-187">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc22b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc22b-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc22b-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dc22b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc22b-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc22b-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-192">Search-Flags</span></span>           | <span data-ttu-id="dc22b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc22b-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="dc22b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-194">System-Flags</span></span>           | <span data-ttu-id="dc22b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc22b-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="dc22b-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc22b-196">Classes used in</span></span>        | [<span data-ttu-id="dc22b-197">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dc22b-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dc22b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc22b-198">Windows Server 2008</span></span>



| <span data-ttu-id="dc22b-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc22b-199">Entry</span></span> | <span data-ttu-id="dc22b-200">Value</span><span class="sxs-lookup"><span data-stu-id="dc22b-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dc22b-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc22b-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc22b-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc22b-203">System-Only</span></span>            | <span data-ttu-id="dc22b-204">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-204">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc22b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="dc22b-206">True</span><span class="sxs-lookup"><span data-stu-id="dc22b-206">True</span></span>                                                                   |
| <span data-ttu-id="dc22b-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc22b-207">Is Indexed</span></span>             | <span data-ttu-id="dc22b-208">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-208">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc22b-209">In Global Catalog</span></span>      | <span data-ttu-id="dc22b-210">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-210">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc22b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc22b-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc22b-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dc22b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc22b-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc22b-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-215">Search-Flags</span></span>           | <span data-ttu-id="dc22b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc22b-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="dc22b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-217">System-Flags</span></span>           | <span data-ttu-id="dc22b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc22b-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="dc22b-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc22b-219">Classes used in</span></span>        | [<span data-ttu-id="dc22b-220">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dc22b-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dc22b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc22b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dc22b-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc22b-222">Entry</span></span> | <span data-ttu-id="dc22b-223">Value</span><span class="sxs-lookup"><span data-stu-id="dc22b-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dc22b-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc22b-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc22b-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc22b-226">System-Only</span></span>            | <span data-ttu-id="dc22b-227">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-227">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc22b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="dc22b-229">True</span><span class="sxs-lookup"><span data-stu-id="dc22b-229">True</span></span>                                                                   |
| <span data-ttu-id="dc22b-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc22b-230">Is Indexed</span></span>             | <span data-ttu-id="dc22b-231">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-231">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc22b-232">In Global Catalog</span></span>      | <span data-ttu-id="dc22b-233">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-233">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc22b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc22b-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc22b-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dc22b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc22b-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc22b-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-238">Search-Flags</span></span>           | <span data-ttu-id="dc22b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc22b-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="dc22b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-240">System-Flags</span></span>           | <span data-ttu-id="dc22b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc22b-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="dc22b-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc22b-242">Classes used in</span></span>        | [<span data-ttu-id="dc22b-243">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dc22b-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dc22b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc22b-244">Windows Server 2012</span></span>



| <span data-ttu-id="dc22b-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="dc22b-245">Entry</span></span> | <span data-ttu-id="dc22b-246">Value</span><span class="sxs-lookup"><span data-stu-id="dc22b-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dc22b-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dc22b-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc22b-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="dc22b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc22b-249">System-Only</span></span>            | <span data-ttu-id="dc22b-250">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-250">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dc22b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="dc22b-252">True</span><span class="sxs-lookup"><span data-stu-id="dc22b-252">True</span></span>                                                                   |
| <span data-ttu-id="dc22b-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dc22b-253">Is Indexed</span></span>             | <span data-ttu-id="dc22b-254">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-254">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dc22b-255">In Global Catalog</span></span>      | <span data-ttu-id="dc22b-256">False</span><span class="sxs-lookup"><span data-stu-id="dc22b-256">False</span></span>                                                                  |
| <span data-ttu-id="dc22b-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dc22b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc22b-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dc22b-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="dc22b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc22b-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc22b-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="dc22b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-261">Search-Flags</span></span>           | <span data-ttu-id="dc22b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc22b-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="dc22b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc22b-263">System-Flags</span></span>           | <span data-ttu-id="dc22b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc22b-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="dc22b-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dc22b-265">Classes used in</span></span>        | [<span data-ttu-id="dc22b-266">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dc22b-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 






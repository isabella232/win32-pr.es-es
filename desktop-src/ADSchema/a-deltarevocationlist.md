---
title: Atributo de lista de revocación Delta
description: Lista de certificados que se han revocado desde la última actualización diferencial.
ms.assetid: fc755c22-6d4f-4509-abb8-47c4f2f37545
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de lista de revocación Delta
- deltaRevocationList esquema de AD de atributos
topic_type:
- apiref
api_name:
- Delta-Revocation-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e866090dfb754c11fb4a25bbe904d5922a8fafd6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151438"
---
# <a name="delta-revocation-list-attribute"></a><span data-ttu-id="dce46-105">Atributo de lista de revocación Delta</span><span class="sxs-lookup"><span data-stu-id="dce46-105">Delta-Revocation-List attribute</span></span>

<span data-ttu-id="dce46-106">Lista de certificados que se han revocado desde la última actualización diferencial.</span><span class="sxs-lookup"><span data-stu-id="dce46-106">List of certificates that have been revoked since the last delta update.</span></span>



| <span data-ttu-id="dce46-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="dce46-107">Entry</span></span> | <span data-ttu-id="dce46-108">Value</span><span class="sxs-lookup"><span data-stu-id="dce46-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="dce46-109">CN</span><span class="sxs-lookup"><span data-stu-id="dce46-109">CN</span></span>                | <span data-ttu-id="dce46-110">Delta-revocación-lista</span><span class="sxs-lookup"><span data-stu-id="dce46-110">Delta-Revocation-List</span></span>                                 |
| <span data-ttu-id="dce46-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="dce46-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dce46-112">deltaRevocationList</span><span class="sxs-lookup"><span data-stu-id="dce46-112">deltaRevocationList</span></span>                                   |
| <span data-ttu-id="dce46-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="dce46-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="dce46-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="dce46-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="dce46-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="dce46-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="dce46-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dce46-116">Attribute-Id</span></span>      | <span data-ttu-id="dce46-117">2.5.4.53</span><span class="sxs-lookup"><span data-stu-id="dce46-117">2.5.4.53</span></span>                                              |
| <span data-ttu-id="dce46-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dce46-118">System-Id-Guid</span></span>    | <span data-ttu-id="dce46-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="dce46-119">167757b5-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="dce46-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dce46-120">Syntax</span></span>            | [<span data-ttu-id="dce46-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="dce46-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="dce46-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="dce46-122">Implementations</span></span>

-   [<span data-ttu-id="dce46-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dce46-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dce46-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dce46-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dce46-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dce46-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dce46-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dce46-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dce46-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dce46-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dce46-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dce46-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dce46-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dce46-129">Windows 2000 Server</span></span>



| <span data-ttu-id="dce46-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="dce46-130">Entry</span></span> | <span data-ttu-id="dce46-131">Value</span><span class="sxs-lookup"><span data-stu-id="dce46-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce46-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dce46-132">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="dce46-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce46-133">MAPI-Id</span></span>                | <span data-ttu-id="dce46-134">0x8C46</span><span class="sxs-lookup"><span data-stu-id="dce46-134">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="dce46-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce46-135">System-Only</span></span>            | <span data-ttu-id="dce46-136">False</span><span class="sxs-lookup"><span data-stu-id="dce46-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dce46-137">Is-Single-Valued</span></span>       | <span data-ttu-id="dce46-138">False</span><span class="sxs-lookup"><span data-stu-id="dce46-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dce46-139">Is Indexed</span></span>             | <span data-ttu-id="dce46-140">False</span><span class="sxs-lookup"><span data-stu-id="dce46-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dce46-141">In Global Catalog</span></span>      | <span data-ttu-id="dce46-142">False</span><span class="sxs-lookup"><span data-stu-id="dce46-142">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dce46-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce46-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dce46-144">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="dce46-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce46-145">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce46-146">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-147">Search-Flags</span></span>           | <span data-ttu-id="dce46-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-149">System-Flags</span></span>           | <span data-ttu-id="dce46-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-150">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dce46-151">Classes used in</span></span>        | [<span data-ttu-id="dce46-152">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dce46-152">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="dce46-153">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="dce46-153">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dce46-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dce46-154">Windows Server 2003</span></span>



| <span data-ttu-id="dce46-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="dce46-155">Entry</span></span> | <span data-ttu-id="dce46-156">Value</span><span class="sxs-lookup"><span data-stu-id="dce46-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce46-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dce46-157">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="dce46-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce46-158">MAPI-Id</span></span>                | <span data-ttu-id="dce46-159">0x8C46</span><span class="sxs-lookup"><span data-stu-id="dce46-159">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="dce46-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce46-160">System-Only</span></span>            | <span data-ttu-id="dce46-161">False</span><span class="sxs-lookup"><span data-stu-id="dce46-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dce46-162">Is-Single-Valued</span></span>       | <span data-ttu-id="dce46-163">False</span><span class="sxs-lookup"><span data-stu-id="dce46-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dce46-164">Is Indexed</span></span>             | <span data-ttu-id="dce46-165">False</span><span class="sxs-lookup"><span data-stu-id="dce46-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dce46-166">In Global Catalog</span></span>      | <span data-ttu-id="dce46-167">False</span><span class="sxs-lookup"><span data-stu-id="dce46-167">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dce46-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce46-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dce46-169">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="dce46-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce46-170">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce46-171">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-172">Search-Flags</span></span>           | <span data-ttu-id="dce46-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-174">System-Flags</span></span>           | <span data-ttu-id="dce46-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-175">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dce46-176">Classes used in</span></span>        | [<span data-ttu-id="dce46-177">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dce46-177">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="dce46-178">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="dce46-178">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dce46-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dce46-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dce46-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="dce46-180">Entry</span></span> | <span data-ttu-id="dce46-181">Value</span><span class="sxs-lookup"><span data-stu-id="dce46-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce46-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dce46-182">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="dce46-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce46-183">MAPI-Id</span></span>                | <span data-ttu-id="dce46-184">0x8C46</span><span class="sxs-lookup"><span data-stu-id="dce46-184">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="dce46-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce46-185">System-Only</span></span>            | <span data-ttu-id="dce46-186">False</span><span class="sxs-lookup"><span data-stu-id="dce46-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dce46-187">Is-Single-Valued</span></span>       | <span data-ttu-id="dce46-188">False</span><span class="sxs-lookup"><span data-stu-id="dce46-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dce46-189">Is Indexed</span></span>             | <span data-ttu-id="dce46-190">False</span><span class="sxs-lookup"><span data-stu-id="dce46-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dce46-191">In Global Catalog</span></span>      | <span data-ttu-id="dce46-192">False</span><span class="sxs-lookup"><span data-stu-id="dce46-192">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dce46-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce46-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dce46-194">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="dce46-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce46-195">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce46-196">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-197">Search-Flags</span></span>           | <span data-ttu-id="dce46-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-199">System-Flags</span></span>           | <span data-ttu-id="dce46-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-200">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dce46-201">Classes used in</span></span>        | [<span data-ttu-id="dce46-202">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dce46-202">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="dce46-203">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="dce46-203">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dce46-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dce46-204">Windows Server 2008</span></span>



| <span data-ttu-id="dce46-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="dce46-205">Entry</span></span> | <span data-ttu-id="dce46-206">Value</span><span class="sxs-lookup"><span data-stu-id="dce46-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce46-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dce46-207">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="dce46-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce46-208">MAPI-Id</span></span>                | <span data-ttu-id="dce46-209">0x8C46</span><span class="sxs-lookup"><span data-stu-id="dce46-209">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="dce46-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce46-210">System-Only</span></span>            | <span data-ttu-id="dce46-211">False</span><span class="sxs-lookup"><span data-stu-id="dce46-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dce46-212">Is-Single-Valued</span></span>       | <span data-ttu-id="dce46-213">False</span><span class="sxs-lookup"><span data-stu-id="dce46-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dce46-214">Is Indexed</span></span>             | <span data-ttu-id="dce46-215">False</span><span class="sxs-lookup"><span data-stu-id="dce46-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dce46-216">In Global Catalog</span></span>      | <span data-ttu-id="dce46-217">False</span><span class="sxs-lookup"><span data-stu-id="dce46-217">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dce46-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce46-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dce46-219">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="dce46-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce46-220">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce46-221">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-222">Search-Flags</span></span>           | <span data-ttu-id="dce46-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-224">System-Flags</span></span>           | <span data-ttu-id="dce46-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-225">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dce46-226">Classes used in</span></span>        | [<span data-ttu-id="dce46-227">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dce46-227">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="dce46-228">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="dce46-228">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dce46-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dce46-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dce46-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="dce46-230">Entry</span></span> | <span data-ttu-id="dce46-231">Value</span><span class="sxs-lookup"><span data-stu-id="dce46-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce46-232">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dce46-232">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="dce46-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce46-233">MAPI-Id</span></span>                | <span data-ttu-id="dce46-234">0x8C46</span><span class="sxs-lookup"><span data-stu-id="dce46-234">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="dce46-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce46-235">System-Only</span></span>            | <span data-ttu-id="dce46-236">False</span><span class="sxs-lookup"><span data-stu-id="dce46-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dce46-237">Is-Single-Valued</span></span>       | <span data-ttu-id="dce46-238">False</span><span class="sxs-lookup"><span data-stu-id="dce46-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dce46-239">Is Indexed</span></span>             | <span data-ttu-id="dce46-240">False</span><span class="sxs-lookup"><span data-stu-id="dce46-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dce46-241">In Global Catalog</span></span>      | <span data-ttu-id="dce46-242">False</span><span class="sxs-lookup"><span data-stu-id="dce46-242">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dce46-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce46-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dce46-244">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="dce46-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce46-245">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce46-246">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-247">Search-Flags</span></span>           | <span data-ttu-id="dce46-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-249">System-Flags</span></span>           | <span data-ttu-id="dce46-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-250">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-251">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dce46-251">Classes used in</span></span>        | [<span data-ttu-id="dce46-252">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dce46-252">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="dce46-253">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="dce46-253">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dce46-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dce46-254">Windows Server 2012</span></span>



| <span data-ttu-id="dce46-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="dce46-255">Entry</span></span> | <span data-ttu-id="dce46-256">Value</span><span class="sxs-lookup"><span data-stu-id="dce46-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce46-257">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="dce46-257">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="dce46-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dce46-258">MAPI-Id</span></span>                | <span data-ttu-id="dce46-259">0x8C46</span><span class="sxs-lookup"><span data-stu-id="dce46-259">0x8C46</span></span>                                                                                                                                     |
| <span data-ttu-id="dce46-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="dce46-260">System-Only</span></span>            | <span data-ttu-id="dce46-261">False</span><span class="sxs-lookup"><span data-stu-id="dce46-261">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-262">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="dce46-262">Is-Single-Valued</span></span>       | <span data-ttu-id="dce46-263">False</span><span class="sxs-lookup"><span data-stu-id="dce46-263">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-264">Está indexado</span><span class="sxs-lookup"><span data-stu-id="dce46-264">Is Indexed</span></span>             | <span data-ttu-id="dce46-265">False</span><span class="sxs-lookup"><span data-stu-id="dce46-265">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-266">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="dce46-266">In Global Catalog</span></span>      | <span data-ttu-id="dce46-267">False</span><span class="sxs-lookup"><span data-stu-id="dce46-267">False</span></span>                                                                                                                                      |
| <span data-ttu-id="dce46-268">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="dce46-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="dce46-269">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dce46-269">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="dce46-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dce46-270">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dce46-271">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="dce46-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-272">Search-Flags</span></span>           | <span data-ttu-id="dce46-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-273">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dce46-274">System-Flags</span></span>           | <span data-ttu-id="dce46-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dce46-275">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="dce46-276">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="dce46-276">Classes used in</span></span>        | [<span data-ttu-id="dce46-277">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="dce46-277">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> [<span data-ttu-id="dce46-278">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="dce46-278">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 






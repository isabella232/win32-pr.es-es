---
title: Certificate-Authority-Object (atributo)
description: Referencia a la entidad de certificación asociada a un punto de distribución de lista de revocación de certificados.
ms.assetid: 8dfd4441-6b45-4dc4-aed8-e33aa7fd099f
ms.tgt_platform: multiple
keywords:
- Certificado-autoridad-atributo de objeto esquema de AD
- certificateAuthorityObject esquema de AD de atributos
topic_type:
- apiref
api_name:
- Certificate-Authority-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65ffceb810cd6a4ef3033834dbf0f3c489f1506e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906265"
---
# <a name="certificate-authority-object-attribute"></a><span data-ttu-id="62430-105">Certificate-Authority-Object (atributo)</span><span class="sxs-lookup"><span data-stu-id="62430-105">Certificate-Authority-Object attribute</span></span>

<span data-ttu-id="62430-106">Referencia a la entidad de certificación asociada a un punto de distribución de lista de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="62430-106">Reference to the certification authority associated with a Certificate Revocation List distribution point.</span></span>



| <span data-ttu-id="62430-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="62430-107">Entry</span></span> | <span data-ttu-id="62430-108">Value</span><span class="sxs-lookup"><span data-stu-id="62430-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="62430-109">CN</span><span class="sxs-lookup"><span data-stu-id="62430-109">CN</span></span>                | <span data-ttu-id="62430-110">Certificate-Authority-Object</span><span class="sxs-lookup"><span data-stu-id="62430-110">Certificate-Authority-Object</span></span>            |
| <span data-ttu-id="62430-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="62430-111">Ldap-Display-Name</span></span> | <span data-ttu-id="62430-112">certificateAuthorityObject</span><span class="sxs-lookup"><span data-stu-id="62430-112">certificateAuthorityObject</span></span>              |
| <span data-ttu-id="62430-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="62430-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="62430-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="62430-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="62430-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="62430-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="62430-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="62430-116">Attribute-Id</span></span>      | <span data-ttu-id="62430-117">1.2.840.113556.1.4.684</span><span class="sxs-lookup"><span data-stu-id="62430-117">1.2.840.113556.1.4.684</span></span>                  |
| <span data-ttu-id="62430-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="62430-118">System-Id-Guid</span></span>    | <span data-ttu-id="62430-119">963d2732-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="62430-119">963d2732-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="62430-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62430-120">Syntax</span></span>            | [<span data-ttu-id="62430-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="62430-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="62430-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="62430-122">Implementations</span></span>

-   [<span data-ttu-id="62430-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="62430-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="62430-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="62430-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="62430-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="62430-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="62430-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="62430-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="62430-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="62430-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="62430-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="62430-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="62430-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="62430-129">Windows 2000 Server</span></span>



| <span data-ttu-id="62430-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="62430-130">Entry</span></span> | <span data-ttu-id="62430-131">Value</span><span class="sxs-lookup"><span data-stu-id="62430-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="62430-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62430-132">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62430-133">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="62430-134">System-Only</span></span>            | <span data-ttu-id="62430-135">False</span><span class="sxs-lookup"><span data-stu-id="62430-135">False</span></span>                                                               |
| <span data-ttu-id="62430-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62430-136">Is-Single-Valued</span></span>       | <span data-ttu-id="62430-137">True</span><span class="sxs-lookup"><span data-stu-id="62430-137">True</span></span>                                                                |
| <span data-ttu-id="62430-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62430-138">Is Indexed</span></span>             | <span data-ttu-id="62430-139">False</span><span class="sxs-lookup"><span data-stu-id="62430-139">False</span></span>                                                               |
| <span data-ttu-id="62430-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62430-140">In Global Catalog</span></span>      | <span data-ttu-id="62430-141">False</span><span class="sxs-lookup"><span data-stu-id="62430-141">False</span></span>                                                               |
| <span data-ttu-id="62430-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62430-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="62430-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62430-143">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="62430-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62430-144">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62430-145">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-146">Search-Flags</span></span>           | <span data-ttu-id="62430-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62430-147">0x00000000</span></span>                                                          |
| <span data-ttu-id="62430-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-148">System-Flags</span></span>           | <span data-ttu-id="62430-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62430-149">0x00000010</span></span>                                                          |
| <span data-ttu-id="62430-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62430-150">Classes used in</span></span>        | [<span data-ttu-id="62430-151">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="62430-151">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="62430-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="62430-152">Windows Server 2003</span></span>



| <span data-ttu-id="62430-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="62430-153">Entry</span></span> | <span data-ttu-id="62430-154">Value</span><span class="sxs-lookup"><span data-stu-id="62430-154">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="62430-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62430-155">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62430-156">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="62430-157">System-Only</span></span>            | <span data-ttu-id="62430-158">False</span><span class="sxs-lookup"><span data-stu-id="62430-158">False</span></span>                                                               |
| <span data-ttu-id="62430-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62430-159">Is-Single-Valued</span></span>       | <span data-ttu-id="62430-160">True</span><span class="sxs-lookup"><span data-stu-id="62430-160">True</span></span>                                                                |
| <span data-ttu-id="62430-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62430-161">Is Indexed</span></span>             | <span data-ttu-id="62430-162">False</span><span class="sxs-lookup"><span data-stu-id="62430-162">False</span></span>                                                               |
| <span data-ttu-id="62430-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62430-163">In Global Catalog</span></span>      | <span data-ttu-id="62430-164">False</span><span class="sxs-lookup"><span data-stu-id="62430-164">False</span></span>                                                               |
| <span data-ttu-id="62430-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62430-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="62430-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62430-166">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="62430-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62430-167">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62430-168">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-169">Search-Flags</span></span>           | <span data-ttu-id="62430-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62430-170">0x00000000</span></span>                                                          |
| <span data-ttu-id="62430-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-171">System-Flags</span></span>           | <span data-ttu-id="62430-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62430-172">0x00000010</span></span>                                                          |
| <span data-ttu-id="62430-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62430-173">Classes used in</span></span>        | [<span data-ttu-id="62430-174">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="62430-174">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="62430-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="62430-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="62430-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="62430-176">Entry</span></span> | <span data-ttu-id="62430-177">Value</span><span class="sxs-lookup"><span data-stu-id="62430-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="62430-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62430-178">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62430-179">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="62430-180">System-Only</span></span>            | <span data-ttu-id="62430-181">False</span><span class="sxs-lookup"><span data-stu-id="62430-181">False</span></span>                                                               |
| <span data-ttu-id="62430-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62430-182">Is-Single-Valued</span></span>       | <span data-ttu-id="62430-183">True</span><span class="sxs-lookup"><span data-stu-id="62430-183">True</span></span>                                                                |
| <span data-ttu-id="62430-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62430-184">Is Indexed</span></span>             | <span data-ttu-id="62430-185">False</span><span class="sxs-lookup"><span data-stu-id="62430-185">False</span></span>                                                               |
| <span data-ttu-id="62430-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62430-186">In Global Catalog</span></span>      | <span data-ttu-id="62430-187">False</span><span class="sxs-lookup"><span data-stu-id="62430-187">False</span></span>                                                               |
| <span data-ttu-id="62430-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62430-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="62430-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62430-189">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="62430-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62430-190">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62430-191">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-192">Search-Flags</span></span>           | <span data-ttu-id="62430-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62430-193">0x00000000</span></span>                                                          |
| <span data-ttu-id="62430-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-194">System-Flags</span></span>           | <span data-ttu-id="62430-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62430-195">0x00000010</span></span>                                                          |
| <span data-ttu-id="62430-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62430-196">Classes used in</span></span>        | [<span data-ttu-id="62430-197">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="62430-197">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="62430-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62430-198">Windows Server 2008</span></span>



| <span data-ttu-id="62430-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="62430-199">Entry</span></span> | <span data-ttu-id="62430-200">Value</span><span class="sxs-lookup"><span data-stu-id="62430-200">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="62430-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62430-201">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62430-202">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="62430-203">System-Only</span></span>            | <span data-ttu-id="62430-204">False</span><span class="sxs-lookup"><span data-stu-id="62430-204">False</span></span>                                                               |
| <span data-ttu-id="62430-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62430-205">Is-Single-Valued</span></span>       | <span data-ttu-id="62430-206">True</span><span class="sxs-lookup"><span data-stu-id="62430-206">True</span></span>                                                                |
| <span data-ttu-id="62430-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62430-207">Is Indexed</span></span>             | <span data-ttu-id="62430-208">False</span><span class="sxs-lookup"><span data-stu-id="62430-208">False</span></span>                                                               |
| <span data-ttu-id="62430-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62430-209">In Global Catalog</span></span>      | <span data-ttu-id="62430-210">False</span><span class="sxs-lookup"><span data-stu-id="62430-210">False</span></span>                                                               |
| <span data-ttu-id="62430-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62430-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="62430-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62430-212">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="62430-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62430-213">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62430-214">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-215">Search-Flags</span></span>           | <span data-ttu-id="62430-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62430-216">0x00000000</span></span>                                                          |
| <span data-ttu-id="62430-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-217">System-Flags</span></span>           | <span data-ttu-id="62430-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62430-218">0x00000010</span></span>                                                          |
| <span data-ttu-id="62430-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62430-219">Classes used in</span></span>        | [<span data-ttu-id="62430-220">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="62430-220">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="62430-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62430-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="62430-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="62430-222">Entry</span></span> | <span data-ttu-id="62430-223">Value</span><span class="sxs-lookup"><span data-stu-id="62430-223">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="62430-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62430-224">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62430-225">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="62430-226">System-Only</span></span>            | <span data-ttu-id="62430-227">False</span><span class="sxs-lookup"><span data-stu-id="62430-227">False</span></span>                                                               |
| <span data-ttu-id="62430-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62430-228">Is-Single-Valued</span></span>       | <span data-ttu-id="62430-229">True</span><span class="sxs-lookup"><span data-stu-id="62430-229">True</span></span>                                                                |
| <span data-ttu-id="62430-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62430-230">Is Indexed</span></span>             | <span data-ttu-id="62430-231">False</span><span class="sxs-lookup"><span data-stu-id="62430-231">False</span></span>                                                               |
| <span data-ttu-id="62430-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62430-232">In Global Catalog</span></span>      | <span data-ttu-id="62430-233">False</span><span class="sxs-lookup"><span data-stu-id="62430-233">False</span></span>                                                               |
| <span data-ttu-id="62430-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62430-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="62430-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62430-235">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="62430-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62430-236">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62430-237">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-238">Search-Flags</span></span>           | <span data-ttu-id="62430-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62430-239">0x00000000</span></span>                                                          |
| <span data-ttu-id="62430-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-240">System-Flags</span></span>           | <span data-ttu-id="62430-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62430-241">0x00000010</span></span>                                                          |
| <span data-ttu-id="62430-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62430-242">Classes used in</span></span>        | [<span data-ttu-id="62430-243">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="62430-243">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="62430-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62430-244">Windows Server 2012</span></span>



| <span data-ttu-id="62430-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="62430-245">Entry</span></span> | <span data-ttu-id="62430-246">Value</span><span class="sxs-lookup"><span data-stu-id="62430-246">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="62430-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="62430-247">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="62430-248">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="62430-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="62430-249">System-Only</span></span>            | <span data-ttu-id="62430-250">False</span><span class="sxs-lookup"><span data-stu-id="62430-250">False</span></span>                                                               |
| <span data-ttu-id="62430-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="62430-251">Is-Single-Valued</span></span>       | <span data-ttu-id="62430-252">True</span><span class="sxs-lookup"><span data-stu-id="62430-252">True</span></span>                                                                |
| <span data-ttu-id="62430-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="62430-253">Is Indexed</span></span>             | <span data-ttu-id="62430-254">False</span><span class="sxs-lookup"><span data-stu-id="62430-254">False</span></span>                                                               |
| <span data-ttu-id="62430-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="62430-255">In Global Catalog</span></span>      | <span data-ttu-id="62430-256">False</span><span class="sxs-lookup"><span data-stu-id="62430-256">False</span></span>                                                               |
| <span data-ttu-id="62430-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="62430-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="62430-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="62430-258">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="62430-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="62430-259">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="62430-260">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="62430-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-261">Search-Flags</span></span>           | <span data-ttu-id="62430-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="62430-262">0x00000000</span></span>                                                          |
| <span data-ttu-id="62430-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="62430-263">System-Flags</span></span>           | <span data-ttu-id="62430-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="62430-264">0x00000010</span></span>                                                          |
| <span data-ttu-id="62430-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="62430-265">Classes used in</span></span>        | [<span data-ttu-id="62430-266">**CRL-punto de distribución**</span><span class="sxs-lookup"><span data-stu-id="62430-266">**CRL-Distribution-Point**</span></span>](c-crldistributionpoint.md)<br/> |



 

 






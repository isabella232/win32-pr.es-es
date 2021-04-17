---
title: Atributo Parent-CA-Certificate-Chain
description: Certificado X. 509v3 codificado en DER para la entidad de certificación principal.
ms.assetid: 37e04c7b-5350-4e48-b3fd-22f97959d26a
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo primario-CA-Certificate-Chain
- parentCACertificateChain esquema de AD de atributos
topic_type:
- apiref
api_name:
- Parent-CA-Certificate-Chain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f27bacb77fb7ab3f1ae712920dace7cb525efc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493732"
---
# <a name="parent-ca-certificate-chain-attribute"></a><span data-ttu-id="044da-105">Atributo Parent-CA-Certificate-Chain</span><span class="sxs-lookup"><span data-stu-id="044da-105">Parent-CA-Certificate-Chain attribute</span></span>

<span data-ttu-id="044da-106">Certificado X. 509v3 codificado en DER para la entidad de certificación principal.</span><span class="sxs-lookup"><span data-stu-id="044da-106">DER-encoded X.509v3 certificate for the parent certification authority.</span></span>



| <span data-ttu-id="044da-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="044da-107">Entry</span></span> | <span data-ttu-id="044da-108">Value</span><span class="sxs-lookup"><span data-stu-id="044da-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="044da-109">CN</span><span class="sxs-lookup"><span data-stu-id="044da-109">CN</span></span>                | <span data-ttu-id="044da-110">Cadena de certificados de entidad de certificación primaria</span><span class="sxs-lookup"><span data-stu-id="044da-110">Parent-CA-Certificate-Chain</span></span>                           |
| <span data-ttu-id="044da-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="044da-111">Ldap-Display-Name</span></span> | <span data-ttu-id="044da-112">parentCACertificateChain</span><span class="sxs-lookup"><span data-stu-id="044da-112">parentCACertificateChain</span></span>                              |
| <span data-ttu-id="044da-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="044da-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="044da-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="044da-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="044da-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="044da-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="044da-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="044da-116">Attribute-Id</span></span>      | <span data-ttu-id="044da-117">1.2.840.113556.1.4.685</span><span class="sxs-lookup"><span data-stu-id="044da-117">1.2.840.113556.1.4.685</span></span>                                |
| <span data-ttu-id="044da-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="044da-118">System-Id-Guid</span></span>    | <span data-ttu-id="044da-119">963d2733-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="044da-119">963d2733-48be-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="044da-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="044da-120">Syntax</span></span>            | [<span data-ttu-id="044da-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="044da-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="044da-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="044da-122">Implementations</span></span>

-   [<span data-ttu-id="044da-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="044da-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="044da-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="044da-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="044da-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="044da-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="044da-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="044da-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="044da-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="044da-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="044da-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="044da-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="044da-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="044da-129">Windows 2000 Server</span></span>



| <span data-ttu-id="044da-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="044da-130">Entry</span></span> | <span data-ttu-id="044da-131">Value</span><span class="sxs-lookup"><span data-stu-id="044da-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="044da-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="044da-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="044da-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="044da-134">System-Only</span></span>            | <span data-ttu-id="044da-135">False</span><span class="sxs-lookup"><span data-stu-id="044da-135">False</span></span>                                                                  |
| <span data-ttu-id="044da-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="044da-136">Is-Single-Valued</span></span>       | <span data-ttu-id="044da-137">True</span><span class="sxs-lookup"><span data-stu-id="044da-137">True</span></span>                                                                   |
| <span data-ttu-id="044da-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="044da-138">Is Indexed</span></span>             | <span data-ttu-id="044da-139">False</span><span class="sxs-lookup"><span data-stu-id="044da-139">False</span></span>                                                                  |
| <span data-ttu-id="044da-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="044da-140">In Global Catalog</span></span>      | <span data-ttu-id="044da-141">False</span><span class="sxs-lookup"><span data-stu-id="044da-141">False</span></span>                                                                  |
| <span data-ttu-id="044da-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="044da-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="044da-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="044da-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="044da-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="044da-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="044da-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-146">Search-Flags</span></span>           | <span data-ttu-id="044da-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="044da-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="044da-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-148">System-Flags</span></span>           | <span data-ttu-id="044da-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="044da-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="044da-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="044da-150">Classes used in</span></span>        | [<span data-ttu-id="044da-151">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="044da-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="044da-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="044da-152">Windows Server 2003</span></span>



| <span data-ttu-id="044da-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="044da-153">Entry</span></span> | <span data-ttu-id="044da-154">Value</span><span class="sxs-lookup"><span data-stu-id="044da-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="044da-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="044da-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="044da-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="044da-157">System-Only</span></span>            | <span data-ttu-id="044da-158">False</span><span class="sxs-lookup"><span data-stu-id="044da-158">False</span></span>                                                                  |
| <span data-ttu-id="044da-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="044da-159">Is-Single-Valued</span></span>       | <span data-ttu-id="044da-160">True</span><span class="sxs-lookup"><span data-stu-id="044da-160">True</span></span>                                                                   |
| <span data-ttu-id="044da-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="044da-161">Is Indexed</span></span>             | <span data-ttu-id="044da-162">False</span><span class="sxs-lookup"><span data-stu-id="044da-162">False</span></span>                                                                  |
| <span data-ttu-id="044da-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="044da-163">In Global Catalog</span></span>      | <span data-ttu-id="044da-164">False</span><span class="sxs-lookup"><span data-stu-id="044da-164">False</span></span>                                                                  |
| <span data-ttu-id="044da-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="044da-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="044da-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="044da-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="044da-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="044da-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="044da-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-169">Search-Flags</span></span>           | <span data-ttu-id="044da-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="044da-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="044da-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-171">System-Flags</span></span>           | <span data-ttu-id="044da-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="044da-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="044da-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="044da-173">Classes used in</span></span>        | [<span data-ttu-id="044da-174">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="044da-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="044da-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="044da-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="044da-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="044da-176">Entry</span></span> | <span data-ttu-id="044da-177">Value</span><span class="sxs-lookup"><span data-stu-id="044da-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="044da-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="044da-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="044da-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="044da-180">System-Only</span></span>            | <span data-ttu-id="044da-181">False</span><span class="sxs-lookup"><span data-stu-id="044da-181">False</span></span>                                                                  |
| <span data-ttu-id="044da-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="044da-182">Is-Single-Valued</span></span>       | <span data-ttu-id="044da-183">True</span><span class="sxs-lookup"><span data-stu-id="044da-183">True</span></span>                                                                   |
| <span data-ttu-id="044da-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="044da-184">Is Indexed</span></span>             | <span data-ttu-id="044da-185">False</span><span class="sxs-lookup"><span data-stu-id="044da-185">False</span></span>                                                                  |
| <span data-ttu-id="044da-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="044da-186">In Global Catalog</span></span>      | <span data-ttu-id="044da-187">False</span><span class="sxs-lookup"><span data-stu-id="044da-187">False</span></span>                                                                  |
| <span data-ttu-id="044da-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="044da-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="044da-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="044da-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="044da-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="044da-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="044da-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-192">Search-Flags</span></span>           | <span data-ttu-id="044da-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="044da-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="044da-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-194">System-Flags</span></span>           | <span data-ttu-id="044da-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="044da-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="044da-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="044da-196">Classes used in</span></span>        | [<span data-ttu-id="044da-197">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="044da-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="044da-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="044da-198">Windows Server 2008</span></span>



| <span data-ttu-id="044da-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="044da-199">Entry</span></span> | <span data-ttu-id="044da-200">Value</span><span class="sxs-lookup"><span data-stu-id="044da-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="044da-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="044da-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="044da-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="044da-203">System-Only</span></span>            | <span data-ttu-id="044da-204">False</span><span class="sxs-lookup"><span data-stu-id="044da-204">False</span></span>                                                                  |
| <span data-ttu-id="044da-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="044da-205">Is-Single-Valued</span></span>       | <span data-ttu-id="044da-206">True</span><span class="sxs-lookup"><span data-stu-id="044da-206">True</span></span>                                                                   |
| <span data-ttu-id="044da-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="044da-207">Is Indexed</span></span>             | <span data-ttu-id="044da-208">False</span><span class="sxs-lookup"><span data-stu-id="044da-208">False</span></span>                                                                  |
| <span data-ttu-id="044da-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="044da-209">In Global Catalog</span></span>      | <span data-ttu-id="044da-210">False</span><span class="sxs-lookup"><span data-stu-id="044da-210">False</span></span>                                                                  |
| <span data-ttu-id="044da-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="044da-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="044da-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="044da-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="044da-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="044da-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="044da-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-215">Search-Flags</span></span>           | <span data-ttu-id="044da-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="044da-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="044da-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-217">System-Flags</span></span>           | <span data-ttu-id="044da-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="044da-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="044da-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="044da-219">Classes used in</span></span>        | [<span data-ttu-id="044da-220">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="044da-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="044da-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="044da-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="044da-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="044da-222">Entry</span></span> | <span data-ttu-id="044da-223">Value</span><span class="sxs-lookup"><span data-stu-id="044da-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="044da-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="044da-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="044da-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="044da-226">System-Only</span></span>            | <span data-ttu-id="044da-227">False</span><span class="sxs-lookup"><span data-stu-id="044da-227">False</span></span>                                                                  |
| <span data-ttu-id="044da-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="044da-228">Is-Single-Valued</span></span>       | <span data-ttu-id="044da-229">True</span><span class="sxs-lookup"><span data-stu-id="044da-229">True</span></span>                                                                   |
| <span data-ttu-id="044da-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="044da-230">Is Indexed</span></span>             | <span data-ttu-id="044da-231">False</span><span class="sxs-lookup"><span data-stu-id="044da-231">False</span></span>                                                                  |
| <span data-ttu-id="044da-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="044da-232">In Global Catalog</span></span>      | <span data-ttu-id="044da-233">False</span><span class="sxs-lookup"><span data-stu-id="044da-233">False</span></span>                                                                  |
| <span data-ttu-id="044da-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="044da-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="044da-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="044da-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="044da-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="044da-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="044da-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-238">Search-Flags</span></span>           | <span data-ttu-id="044da-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="044da-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="044da-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-240">System-Flags</span></span>           | <span data-ttu-id="044da-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="044da-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="044da-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="044da-242">Classes used in</span></span>        | [<span data-ttu-id="044da-243">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="044da-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="044da-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="044da-244">Windows Server 2012</span></span>



| <span data-ttu-id="044da-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="044da-245">Entry</span></span> | <span data-ttu-id="044da-246">Value</span><span class="sxs-lookup"><span data-stu-id="044da-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="044da-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="044da-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="044da-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="044da-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="044da-249">System-Only</span></span>            | <span data-ttu-id="044da-250">False</span><span class="sxs-lookup"><span data-stu-id="044da-250">False</span></span>                                                                  |
| <span data-ttu-id="044da-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="044da-251">Is-Single-Valued</span></span>       | <span data-ttu-id="044da-252">True</span><span class="sxs-lookup"><span data-stu-id="044da-252">True</span></span>                                                                   |
| <span data-ttu-id="044da-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="044da-253">Is Indexed</span></span>             | <span data-ttu-id="044da-254">False</span><span class="sxs-lookup"><span data-stu-id="044da-254">False</span></span>                                                                  |
| <span data-ttu-id="044da-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="044da-255">In Global Catalog</span></span>      | <span data-ttu-id="044da-256">False</span><span class="sxs-lookup"><span data-stu-id="044da-256">False</span></span>                                                                  |
| <span data-ttu-id="044da-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="044da-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="044da-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="044da-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="044da-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="044da-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="044da-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="044da-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-261">Search-Flags</span></span>           | <span data-ttu-id="044da-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="044da-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="044da-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="044da-263">System-Flags</span></span>           | <span data-ttu-id="044da-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="044da-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="044da-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="044da-265">Classes used in</span></span>        | [<span data-ttu-id="044da-266">**Entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="044da-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 






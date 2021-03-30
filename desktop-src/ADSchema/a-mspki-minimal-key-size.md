---
title: atributo MS-PKI-minimal-Key-size
description: Indica el tamaño mínimo de la clave privada.
ms.assetid: e38fbab5-14db-40d1-80c4-c14477c6f0da
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de tamaño mínimo de clave-PKI de MS-PKI
- Atributo mspki-minimal-Key-size Attribute AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-Minimal-Key-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb1a3f168393bb203f7c590ba52924670d3dab2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151633"
---
# <a name="ms-pki-minimal-key-size-attribute"></a><span data-ttu-id="95e25-105">atributo MS-PKI-minimal-Key-size</span><span class="sxs-lookup"><span data-stu-id="95e25-105">ms-PKI-Minimal-Key-Size attribute</span></span>

<span data-ttu-id="95e25-106">Indica el tamaño mínimo de la clave privada.</span><span class="sxs-lookup"><span data-stu-id="95e25-106">Indicates the minimum private key size.</span></span>



| <span data-ttu-id="95e25-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="95e25-107">Entry</span></span> | <span data-ttu-id="95e25-108">Value</span><span class="sxs-lookup"><span data-stu-id="95e25-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e25-109">CN</span><span class="sxs-lookup"><span data-stu-id="95e25-109">CN</span></span>                | <span data-ttu-id="95e25-110">MS-PKI-mínimo-clave-tamaño</span><span class="sxs-lookup"><span data-stu-id="95e25-110">ms-PKI-Minimal-Key-Size</span></span>                                                                           |
| <span data-ttu-id="95e25-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="95e25-111">Ldap-Display-Name</span></span> | <span data-ttu-id="95e25-112">Atributo mspki-minimal-tamaño de clave</span><span class="sxs-lookup"><span data-stu-id="95e25-112">msPKI-Minimal-Key-Size</span></span>                                                                            |
| <span data-ttu-id="95e25-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="95e25-113">Size</span></span>              | <span data-ttu-id="95e25-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="95e25-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="95e25-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="95e25-115">Update Privilege</span></span>  | <span data-ttu-id="95e25-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="95e25-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="95e25-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="95e25-117">Update Frequency</span></span>  | <span data-ttu-id="95e25-118">Cuando se edita, crea o clona el objeto plantilla de certificado (MS-PKI-Certificate-template).</span><span class="sxs-lookup"><span data-stu-id="95e25-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="95e25-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="95e25-119">Attribute-Id</span></span>      | <span data-ttu-id="95e25-120">1.2.840.113556.1.4.1433</span><span class="sxs-lookup"><span data-stu-id="95e25-120">1.2.840.113556.1.4.1433</span></span>                                                                           |
| <span data-ttu-id="95e25-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="95e25-121">System-Id-Guid</span></span>    | <span data-ttu-id="95e25-122">e96a63f5-417f-46d3-be52-db7703c503df</span><span class="sxs-lookup"><span data-stu-id="95e25-122">e96a63f5-417f-46d3-be52-db7703c503df</span></span>                                                              |
| <span data-ttu-id="95e25-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95e25-123">Syntax</span></span>            | [<span data-ttu-id="95e25-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="95e25-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="95e25-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="95e25-125">Implementations</span></span>

-   [<span data-ttu-id="95e25-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="95e25-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="95e25-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="95e25-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="95e25-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="95e25-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="95e25-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="95e25-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="95e25-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="95e25-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="95e25-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="95e25-131">Windows Server 2003</span></span>



| <span data-ttu-id="95e25-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="95e25-132">Entry</span></span> | <span data-ttu-id="95e25-133">Value</span><span class="sxs-lookup"><span data-stu-id="95e25-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="95e25-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="95e25-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95e25-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="95e25-136">System-Only</span></span>            | <span data-ttu-id="95e25-137">False</span><span class="sxs-lookup"><span data-stu-id="95e25-137">False</span></span>                                                                   |
| <span data-ttu-id="95e25-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="95e25-138">Is-Single-Valued</span></span>       | <span data-ttu-id="95e25-139">True</span><span class="sxs-lookup"><span data-stu-id="95e25-139">True</span></span>                                                                    |
| <span data-ttu-id="95e25-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="95e25-140">Is Indexed</span></span>             | <span data-ttu-id="95e25-141">False</span><span class="sxs-lookup"><span data-stu-id="95e25-141">False</span></span>                                                                   |
| <span data-ttu-id="95e25-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="95e25-142">In Global Catalog</span></span>      | <span data-ttu-id="95e25-143">False</span><span class="sxs-lookup"><span data-stu-id="95e25-143">False</span></span>                                                                   |
| <span data-ttu-id="95e25-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="95e25-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="95e25-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="95e25-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="95e25-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95e25-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95e25-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-148">Search-Flags</span></span>           | <span data-ttu-id="95e25-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95e25-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="95e25-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-150">System-Flags</span></span>           | <span data-ttu-id="95e25-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95e25-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="95e25-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="95e25-152">Classes used in</span></span>        | [<span data-ttu-id="95e25-153">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="95e25-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="95e25-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="95e25-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="95e25-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="95e25-155">Entry</span></span> | <span data-ttu-id="95e25-156">Value</span><span class="sxs-lookup"><span data-stu-id="95e25-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="95e25-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="95e25-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95e25-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="95e25-159">System-Only</span></span>            | <span data-ttu-id="95e25-160">False</span><span class="sxs-lookup"><span data-stu-id="95e25-160">False</span></span>                                                                   |
| <span data-ttu-id="95e25-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="95e25-161">Is-Single-Valued</span></span>       | <span data-ttu-id="95e25-162">True</span><span class="sxs-lookup"><span data-stu-id="95e25-162">True</span></span>                                                                    |
| <span data-ttu-id="95e25-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="95e25-163">Is Indexed</span></span>             | <span data-ttu-id="95e25-164">False</span><span class="sxs-lookup"><span data-stu-id="95e25-164">False</span></span>                                                                   |
| <span data-ttu-id="95e25-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="95e25-165">In Global Catalog</span></span>      | <span data-ttu-id="95e25-166">False</span><span class="sxs-lookup"><span data-stu-id="95e25-166">False</span></span>                                                                   |
| <span data-ttu-id="95e25-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="95e25-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="95e25-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="95e25-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="95e25-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95e25-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95e25-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-171">Search-Flags</span></span>           | <span data-ttu-id="95e25-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95e25-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="95e25-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-173">System-Flags</span></span>           | <span data-ttu-id="95e25-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95e25-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="95e25-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="95e25-175">Classes used in</span></span>        | [<span data-ttu-id="95e25-176">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="95e25-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="95e25-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95e25-177">Windows Server 2008</span></span>



| <span data-ttu-id="95e25-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="95e25-178">Entry</span></span> | <span data-ttu-id="95e25-179">Value</span><span class="sxs-lookup"><span data-stu-id="95e25-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="95e25-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="95e25-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95e25-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="95e25-182">System-Only</span></span>            | <span data-ttu-id="95e25-183">False</span><span class="sxs-lookup"><span data-stu-id="95e25-183">False</span></span>                                                                   |
| <span data-ttu-id="95e25-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="95e25-184">Is-Single-Valued</span></span>       | <span data-ttu-id="95e25-185">True</span><span class="sxs-lookup"><span data-stu-id="95e25-185">True</span></span>                                                                    |
| <span data-ttu-id="95e25-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="95e25-186">Is Indexed</span></span>             | <span data-ttu-id="95e25-187">False</span><span class="sxs-lookup"><span data-stu-id="95e25-187">False</span></span>                                                                   |
| <span data-ttu-id="95e25-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="95e25-188">In Global Catalog</span></span>      | <span data-ttu-id="95e25-189">False</span><span class="sxs-lookup"><span data-stu-id="95e25-189">False</span></span>                                                                   |
| <span data-ttu-id="95e25-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="95e25-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="95e25-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="95e25-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="95e25-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95e25-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95e25-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-194">Search-Flags</span></span>           | <span data-ttu-id="95e25-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95e25-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="95e25-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-196">System-Flags</span></span>           | <span data-ttu-id="95e25-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95e25-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="95e25-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="95e25-198">Classes used in</span></span>        | [<span data-ttu-id="95e25-199">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="95e25-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="95e25-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="95e25-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="95e25-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="95e25-201">Entry</span></span> | <span data-ttu-id="95e25-202">Value</span><span class="sxs-lookup"><span data-stu-id="95e25-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="95e25-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="95e25-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95e25-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="95e25-205">System-Only</span></span>            | <span data-ttu-id="95e25-206">False</span><span class="sxs-lookup"><span data-stu-id="95e25-206">False</span></span>                                                                   |
| <span data-ttu-id="95e25-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="95e25-207">Is-Single-Valued</span></span>       | <span data-ttu-id="95e25-208">True</span><span class="sxs-lookup"><span data-stu-id="95e25-208">True</span></span>                                                                    |
| <span data-ttu-id="95e25-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="95e25-209">Is Indexed</span></span>             | <span data-ttu-id="95e25-210">False</span><span class="sxs-lookup"><span data-stu-id="95e25-210">False</span></span>                                                                   |
| <span data-ttu-id="95e25-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="95e25-211">In Global Catalog</span></span>      | <span data-ttu-id="95e25-212">False</span><span class="sxs-lookup"><span data-stu-id="95e25-212">False</span></span>                                                                   |
| <span data-ttu-id="95e25-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="95e25-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="95e25-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="95e25-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="95e25-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95e25-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95e25-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-217">Search-Flags</span></span>           | <span data-ttu-id="95e25-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95e25-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="95e25-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-219">System-Flags</span></span>           | <span data-ttu-id="95e25-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95e25-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="95e25-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="95e25-221">Classes used in</span></span>        | [<span data-ttu-id="95e25-222">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="95e25-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="95e25-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95e25-223">Windows Server 2012</span></span>



| <span data-ttu-id="95e25-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="95e25-224">Entry</span></span> | <span data-ttu-id="95e25-225">Value</span><span class="sxs-lookup"><span data-stu-id="95e25-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="95e25-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="95e25-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95e25-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="95e25-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="95e25-228">System-Only</span></span>            | <span data-ttu-id="95e25-229">False</span><span class="sxs-lookup"><span data-stu-id="95e25-229">False</span></span>                                                                   |
| <span data-ttu-id="95e25-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="95e25-230">Is-Single-Valued</span></span>       | <span data-ttu-id="95e25-231">True</span><span class="sxs-lookup"><span data-stu-id="95e25-231">True</span></span>                                                                    |
| <span data-ttu-id="95e25-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="95e25-232">Is Indexed</span></span>             | <span data-ttu-id="95e25-233">False</span><span class="sxs-lookup"><span data-stu-id="95e25-233">False</span></span>                                                                   |
| <span data-ttu-id="95e25-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="95e25-234">In Global Catalog</span></span>      | <span data-ttu-id="95e25-235">False</span><span class="sxs-lookup"><span data-stu-id="95e25-235">False</span></span>                                                                   |
| <span data-ttu-id="95e25-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="95e25-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="95e25-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="95e25-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="95e25-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95e25-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95e25-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="95e25-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-240">Search-Flags</span></span>           | <span data-ttu-id="95e25-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95e25-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="95e25-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95e25-242">System-Flags</span></span>           | <span data-ttu-id="95e25-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95e25-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="95e25-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="95e25-244">Classes used in</span></span>        | [<span data-ttu-id="95e25-245">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="95e25-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






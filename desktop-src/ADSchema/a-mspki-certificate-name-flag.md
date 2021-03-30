---
title: atributo MS-PKI-Certificate-Name-Flag
description: Contiene las marcas relacionadas con la construcción del nombre del firmante en un certificado emitido.
ms.assetid: 7aeeff69-86b5-4251-bd64-bd99b7c9ef4a
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-PKI-Certificate-Name-Flag
- Atributo mspki-Certificate-Name-Flag atributo AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Name-Flag
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a9a5f8d6db36c3e3b86945fa529572df38ff6df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422703"
---
# <a name="ms-pki-certificate-name-flag-attribute"></a><span data-ttu-id="c0b57-105">atributo MS-PKI-Certificate-Name-Flag</span><span class="sxs-lookup"><span data-stu-id="c0b57-105">ms-PKI-Certificate-Name-Flag attribute</span></span>

<span data-ttu-id="c0b57-106">Contiene las marcas relacionadas con la construcción del nombre del firmante en un certificado emitido.</span><span class="sxs-lookup"><span data-stu-id="c0b57-106">Contains the flags related to constructing the subject name in an issued certificate.</span></span>



| <span data-ttu-id="c0b57-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0b57-107">Entry</span></span> | <span data-ttu-id="c0b57-108">Value</span><span class="sxs-lookup"><span data-stu-id="c0b57-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b57-109">CN</span><span class="sxs-lookup"><span data-stu-id="c0b57-109">CN</span></span>                | <span data-ttu-id="c0b57-110">Marca MS-PKI-Certificate-Name-</span><span class="sxs-lookup"><span data-stu-id="c0b57-110">ms-PKI-Certificate-Name-Flag</span></span>                                                                      |
| <span data-ttu-id="c0b57-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c0b57-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c0b57-112">Atributo mspki-Certificate-Name-Flag</span><span class="sxs-lookup"><span data-stu-id="c0b57-112">msPKI-Certificate-Name-Flag</span></span>                                                                       |
| <span data-ttu-id="c0b57-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c0b57-113">Size</span></span>              | <span data-ttu-id="c0b57-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="c0b57-114">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="c0b57-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c0b57-115">Update Privilege</span></span>  | <span data-ttu-id="c0b57-116">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="c0b57-116">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="c0b57-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c0b57-117">Update Frequency</span></span>  | <span data-ttu-id="c0b57-118">Cuando se edita, crea o clona el objeto plantilla de certificado (MS-PKI-Certificate-template).</span><span class="sxs-lookup"><span data-stu-id="c0b57-118">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="c0b57-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c0b57-119">Attribute-Id</span></span>      | <span data-ttu-id="c0b57-120">1.2.840.113556.1.4.1432</span><span class="sxs-lookup"><span data-stu-id="c0b57-120">1.2.840.113556.1.4.1432</span></span>                                                                           |
| <span data-ttu-id="c0b57-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c0b57-121">System-Id-Guid</span></span>    | <span data-ttu-id="c0b57-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span><span class="sxs-lookup"><span data-stu-id="c0b57-122">ea1dddc4-60ff-416e-8cc0-17cee534bce7</span></span>                                                              |
| <span data-ttu-id="c0b57-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0b57-123">Syntax</span></span>            | [<span data-ttu-id="c0b57-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="c0b57-124">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="c0b57-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c0b57-125">Implementations</span></span>

-   [<span data-ttu-id="c0b57-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c0b57-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c0b57-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c0b57-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c0b57-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c0b57-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c0b57-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c0b57-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c0b57-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c0b57-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c0b57-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0b57-131">Windows Server 2003</span></span>



| <span data-ttu-id="c0b57-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0b57-132">Entry</span></span> | <span data-ttu-id="c0b57-133">Value</span><span class="sxs-lookup"><span data-stu-id="c0b57-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c0b57-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c0b57-134">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b57-135">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b57-136">System-Only</span></span>            | <span data-ttu-id="c0b57-137">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-137">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c0b57-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b57-139">True</span><span class="sxs-lookup"><span data-stu-id="c0b57-139">True</span></span>                                                                    |
| <span data-ttu-id="c0b57-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c0b57-140">Is Indexed</span></span>             | <span data-ttu-id="c0b57-141">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-141">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0b57-142">In Global Catalog</span></span>      | <span data-ttu-id="c0b57-143">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-143">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c0b57-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b57-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b57-145">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c0b57-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b57-146">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b57-147">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-148">Search-Flags</span></span>           | <span data-ttu-id="c0b57-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0b57-149">0x00000000</span></span>                                                              |
| <span data-ttu-id="c0b57-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-150">System-Flags</span></span>           | <span data-ttu-id="c0b57-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b57-151">0x00000010</span></span>                                                              |
| <span data-ttu-id="c0b57-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c0b57-152">Classes used in</span></span>        | [<span data-ttu-id="c0b57-153">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="c0b57-153">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c0b57-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c0b57-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c0b57-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0b57-155">Entry</span></span> | <span data-ttu-id="c0b57-156">Value</span><span class="sxs-lookup"><span data-stu-id="c0b57-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c0b57-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c0b57-157">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b57-158">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b57-159">System-Only</span></span>            | <span data-ttu-id="c0b57-160">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-160">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c0b57-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b57-162">True</span><span class="sxs-lookup"><span data-stu-id="c0b57-162">True</span></span>                                                                    |
| <span data-ttu-id="c0b57-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c0b57-163">Is Indexed</span></span>             | <span data-ttu-id="c0b57-164">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-164">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0b57-165">In Global Catalog</span></span>      | <span data-ttu-id="c0b57-166">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-166">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c0b57-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b57-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b57-168">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c0b57-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b57-169">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b57-170">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-171">Search-Flags</span></span>           | <span data-ttu-id="c0b57-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0b57-172">0x00000000</span></span>                                                              |
| <span data-ttu-id="c0b57-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-173">System-Flags</span></span>           | <span data-ttu-id="c0b57-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b57-174">0x00000010</span></span>                                                              |
| <span data-ttu-id="c0b57-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c0b57-175">Classes used in</span></span>        | [<span data-ttu-id="c0b57-176">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="c0b57-176">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c0b57-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0b57-177">Windows Server 2008</span></span>



| <span data-ttu-id="c0b57-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0b57-178">Entry</span></span> | <span data-ttu-id="c0b57-179">Value</span><span class="sxs-lookup"><span data-stu-id="c0b57-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c0b57-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c0b57-180">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b57-181">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b57-182">System-Only</span></span>            | <span data-ttu-id="c0b57-183">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-183">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c0b57-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b57-185">True</span><span class="sxs-lookup"><span data-stu-id="c0b57-185">True</span></span>                                                                    |
| <span data-ttu-id="c0b57-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c0b57-186">Is Indexed</span></span>             | <span data-ttu-id="c0b57-187">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-187">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0b57-188">In Global Catalog</span></span>      | <span data-ttu-id="c0b57-189">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-189">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c0b57-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b57-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b57-191">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c0b57-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b57-192">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b57-193">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-194">Search-Flags</span></span>           | <span data-ttu-id="c0b57-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0b57-195">0x00000000</span></span>                                                              |
| <span data-ttu-id="c0b57-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-196">System-Flags</span></span>           | <span data-ttu-id="c0b57-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b57-197">0x00000010</span></span>                                                              |
| <span data-ttu-id="c0b57-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c0b57-198">Classes used in</span></span>        | [<span data-ttu-id="c0b57-199">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="c0b57-199">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c0b57-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c0b57-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c0b57-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0b57-201">Entry</span></span> | <span data-ttu-id="c0b57-202">Value</span><span class="sxs-lookup"><span data-stu-id="c0b57-202">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c0b57-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c0b57-203">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b57-204">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b57-205">System-Only</span></span>            | <span data-ttu-id="c0b57-206">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-206">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c0b57-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b57-208">True</span><span class="sxs-lookup"><span data-stu-id="c0b57-208">True</span></span>                                                                    |
| <span data-ttu-id="c0b57-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c0b57-209">Is Indexed</span></span>             | <span data-ttu-id="c0b57-210">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-210">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0b57-211">In Global Catalog</span></span>      | <span data-ttu-id="c0b57-212">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-212">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c0b57-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b57-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b57-214">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c0b57-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b57-215">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b57-216">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-217">Search-Flags</span></span>           | <span data-ttu-id="c0b57-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0b57-218">0x00000000</span></span>                                                              |
| <span data-ttu-id="c0b57-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-219">System-Flags</span></span>           | <span data-ttu-id="c0b57-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b57-220">0x00000010</span></span>                                                              |
| <span data-ttu-id="c0b57-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c0b57-221">Classes used in</span></span>        | [<span data-ttu-id="c0b57-222">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="c0b57-222">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c0b57-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0b57-223">Windows Server 2012</span></span>



| <span data-ttu-id="c0b57-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0b57-224">Entry</span></span> | <span data-ttu-id="c0b57-225">Value</span><span class="sxs-lookup"><span data-stu-id="c0b57-225">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c0b57-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c0b57-226">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0b57-227">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c0b57-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0b57-228">System-Only</span></span>            | <span data-ttu-id="c0b57-229">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-229">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c0b57-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c0b57-231">True</span><span class="sxs-lookup"><span data-stu-id="c0b57-231">True</span></span>                                                                    |
| <span data-ttu-id="c0b57-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c0b57-232">Is Indexed</span></span>             | <span data-ttu-id="c0b57-233">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-233">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0b57-234">In Global Catalog</span></span>      | <span data-ttu-id="c0b57-235">False</span><span class="sxs-lookup"><span data-stu-id="c0b57-235">False</span></span>                                                                   |
| <span data-ttu-id="c0b57-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c0b57-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0b57-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0b57-237">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c0b57-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0b57-238">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0b57-239">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c0b57-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-240">Search-Flags</span></span>           | <span data-ttu-id="c0b57-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0b57-241">0x00000000</span></span>                                                              |
| <span data-ttu-id="c0b57-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0b57-242">System-Flags</span></span>           | <span data-ttu-id="c0b57-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0b57-243">0x00000010</span></span>                                                              |
| <span data-ttu-id="c0b57-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c0b57-244">Classes used in</span></span>        | [<span data-ttu-id="c0b57-245">**PKI-Certificate-template**</span><span class="sxs-lookup"><span data-stu-id="c0b57-245">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 






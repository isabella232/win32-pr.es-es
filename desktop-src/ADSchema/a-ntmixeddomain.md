---
title: 'NT: atributo de dominio mixto'
description: Indica que el dominio está en modo nativo o mixto. Este atributo se encuentra en el objeto domainDNS (Head) del dominio.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- NT-Mixed-esquema de AD de atributos de dominio
- nTMixedDomain esquema de AD de atributos
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658789"
---
# <a name="nt-mixed-domain-attribute"></a><span data-ttu-id="08c4d-106">NT: atributo de dominio mixto</span><span class="sxs-lookup"><span data-stu-id="08c4d-106">NT-Mixed-Domain attribute</span></span>

<span data-ttu-id="08c4d-107">Indica que el dominio está en modo nativo o mixto.</span><span class="sxs-lookup"><span data-stu-id="08c4d-107">Indicates that the domain is in native mode or mixed mode.</span></span> <span data-ttu-id="08c4d-108">Este atributo se encuentra en el objeto domainDNS (Head) del dominio.</span><span class="sxs-lookup"><span data-stu-id="08c4d-108">This attribute is found in the domainDNS (head) object for the domain.</span></span>



| <span data-ttu-id="08c4d-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="08c4d-109">Entry</span></span> | <span data-ttu-id="08c4d-110">Value</span><span class="sxs-lookup"><span data-stu-id="08c4d-110">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="08c4d-111">CN</span><span class="sxs-lookup"><span data-stu-id="08c4d-111">CN</span></span>                | <span data-ttu-id="08c4d-112">NT-Mixed-Domain</span><span class="sxs-lookup"><span data-stu-id="08c4d-112">NT-Mixed-Domain</span></span>                       |
| <span data-ttu-id="08c4d-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="08c4d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="08c4d-114">nTMixedDomain</span><span class="sxs-lookup"><span data-stu-id="08c4d-114">nTMixedDomain</span></span>                         |
| <span data-ttu-id="08c4d-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="08c4d-115">Size</span></span>              | <span data-ttu-id="08c4d-116">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="08c4d-116">4 bytes.</span></span> <span data-ttu-id="08c4d-117">Modo mixto 1, modo nativo 0.</span><span class="sxs-lookup"><span data-stu-id="08c4d-117">Mixed mode 1, native mode 0.</span></span> |
| <span data-ttu-id="08c4d-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="08c4d-118">Update Privilege</span></span>  | \-                                    |
| <span data-ttu-id="08c4d-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="08c4d-119">Update Frequency</span></span>  | \-                                    |
| <span data-ttu-id="08c4d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="08c4d-120">Attribute-Id</span></span>      | <span data-ttu-id="08c4d-121">1.2.840.113556.1.4.357</span><span class="sxs-lookup"><span data-stu-id="08c4d-121">1.2.840.113556.1.4.357</span></span>                |
| <span data-ttu-id="08c4d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="08c4d-122">System-Id-Guid</span></span>    | <span data-ttu-id="08c4d-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="08c4d-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span></span>  |
| <span data-ttu-id="08c4d-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08c4d-124">Syntax</span></span>            | [<span data-ttu-id="08c4d-125">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="08c4d-125">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="08c4d-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="08c4d-126">Implementations</span></span>

-   [<span data-ttu-id="08c4d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="08c4d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="08c4d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="08c4d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="08c4d-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="08c4d-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="08c4d-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="08c4d-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="08c4d-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="08c4d-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="08c4d-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="08c4d-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="08c4d-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08c4d-133">Windows 2000 Server</span></span>



| <span data-ttu-id="08c4d-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="08c4d-134">Entry</span></span> | <span data-ttu-id="08c4d-135">Value</span><span class="sxs-lookup"><span data-stu-id="08c4d-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="08c4d-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08c4d-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="08c4d-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08c4d-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="08c4d-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="08c4d-138">System-Only</span></span>            | <span data-ttu-id="08c4d-139">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-139">False</span></span>                                        |
| <span data-ttu-id="08c4d-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08c4d-140">Is-Single-Valued</span></span>       | <span data-ttu-id="08c4d-141">True</span><span class="sxs-lookup"><span data-stu-id="08c4d-141">True</span></span>                                         |
| <span data-ttu-id="08c4d-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08c4d-142">Is Indexed</span></span>             | <span data-ttu-id="08c4d-143">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-143">False</span></span>                                        |
| <span data-ttu-id="08c4d-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08c4d-144">In Global Catalog</span></span>      | <span data-ttu-id="08c4d-145">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-145">False</span></span>                                        |
| <span data-ttu-id="08c4d-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08c4d-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="08c4d-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08c4d-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="08c4d-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08c4d-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="08c4d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08c4d-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="08c4d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-150">Search-Flags</span></span>           | <span data-ttu-id="08c4d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08c4d-151">0x00000000</span></span>                                   |
| <span data-ttu-id="08c4d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-152">System-Flags</span></span>           | <span data-ttu-id="08c4d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08c4d-153">0x00000010</span></span>                                   |
| <span data-ttu-id="08c4d-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08c4d-154">Classes used in</span></span>        | [<span data-ttu-id="08c4d-155">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="08c4d-155">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="08c4d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08c4d-156">Windows Server 2003</span></span>



| <span data-ttu-id="08c4d-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="08c4d-157">Entry</span></span> | <span data-ttu-id="08c4d-158">Value</span><span class="sxs-lookup"><span data-stu-id="08c4d-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08c4d-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08c4d-159">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08c4d-160">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="08c4d-161">System-Only</span></span>            | <span data-ttu-id="08c4d-162">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-162">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08c4d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="08c4d-164">True</span><span class="sxs-lookup"><span data-stu-id="08c4d-164">True</span></span>                                                                                    |
| <span data-ttu-id="08c4d-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08c4d-165">Is Indexed</span></span>             | <span data-ttu-id="08c4d-166">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-166">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08c4d-167">In Global Catalog</span></span>      | <span data-ttu-id="08c4d-168">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-168">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08c4d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="08c4d-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08c4d-170">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="08c4d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08c4d-171">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08c4d-172">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-173">Search-Flags</span></span>           | <span data-ttu-id="08c4d-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08c4d-174">0x00000000</span></span>                                                                              |
| <span data-ttu-id="08c4d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-175">System-Flags</span></span>           | <span data-ttu-id="08c4d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08c4d-176">0x00000010</span></span>                                                                              |
| <span data-ttu-id="08c4d-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08c4d-177">Classes used in</span></span>        | [<span data-ttu-id="08c4d-178">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08c4d-178">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="08c4d-179">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="08c4d-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="08c4d-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="08c4d-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="08c4d-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="08c4d-181">Entry</span></span> | <span data-ttu-id="08c4d-182">Value</span><span class="sxs-lookup"><span data-stu-id="08c4d-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08c4d-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08c4d-183">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08c4d-184">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="08c4d-185">System-Only</span></span>            | <span data-ttu-id="08c4d-186">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-186">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08c4d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="08c4d-188">True</span><span class="sxs-lookup"><span data-stu-id="08c4d-188">True</span></span>                                                                                    |
| <span data-ttu-id="08c4d-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08c4d-189">Is Indexed</span></span>             | <span data-ttu-id="08c4d-190">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-190">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08c4d-191">In Global Catalog</span></span>      | <span data-ttu-id="08c4d-192">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-192">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08c4d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="08c4d-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08c4d-194">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="08c4d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08c4d-195">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08c4d-196">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-197">Search-Flags</span></span>           | <span data-ttu-id="08c4d-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08c4d-198">0x00000000</span></span>                                                                              |
| <span data-ttu-id="08c4d-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-199">System-Flags</span></span>           | <span data-ttu-id="08c4d-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08c4d-200">0x00000010</span></span>                                                                              |
| <span data-ttu-id="08c4d-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08c4d-201">Classes used in</span></span>        | [<span data-ttu-id="08c4d-202">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08c4d-202">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="08c4d-203">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="08c4d-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="08c4d-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08c4d-204">Windows Server 2008</span></span>



| <span data-ttu-id="08c4d-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="08c4d-205">Entry</span></span> | <span data-ttu-id="08c4d-206">Value</span><span class="sxs-lookup"><span data-stu-id="08c4d-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08c4d-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08c4d-207">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08c4d-208">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="08c4d-209">System-Only</span></span>            | <span data-ttu-id="08c4d-210">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-210">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08c4d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="08c4d-212">True</span><span class="sxs-lookup"><span data-stu-id="08c4d-212">True</span></span>                                                                                    |
| <span data-ttu-id="08c4d-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08c4d-213">Is Indexed</span></span>             | <span data-ttu-id="08c4d-214">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-214">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08c4d-215">In Global Catalog</span></span>      | <span data-ttu-id="08c4d-216">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-216">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08c4d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="08c4d-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08c4d-218">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="08c4d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08c4d-219">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08c4d-220">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-221">Search-Flags</span></span>           | <span data-ttu-id="08c4d-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08c4d-222">0x00000000</span></span>                                                                              |
| <span data-ttu-id="08c4d-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-223">System-Flags</span></span>           | <span data-ttu-id="08c4d-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08c4d-224">0x00000010</span></span>                                                                              |
| <span data-ttu-id="08c4d-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08c4d-225">Classes used in</span></span>        | [<span data-ttu-id="08c4d-226">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08c4d-226">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="08c4d-227">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="08c4d-227">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="08c4d-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08c4d-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="08c4d-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="08c4d-229">Entry</span></span> | <span data-ttu-id="08c4d-230">Value</span><span class="sxs-lookup"><span data-stu-id="08c4d-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08c4d-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08c4d-231">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08c4d-232">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="08c4d-233">System-Only</span></span>            | <span data-ttu-id="08c4d-234">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-234">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08c4d-235">Is-Single-Valued</span></span>       | <span data-ttu-id="08c4d-236">True</span><span class="sxs-lookup"><span data-stu-id="08c4d-236">True</span></span>                                                                                    |
| <span data-ttu-id="08c4d-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08c4d-237">Is Indexed</span></span>             | <span data-ttu-id="08c4d-238">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-238">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08c4d-239">In Global Catalog</span></span>      | <span data-ttu-id="08c4d-240">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-240">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08c4d-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="08c4d-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08c4d-242">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="08c4d-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08c4d-243">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08c4d-244">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-245">Search-Flags</span></span>           | <span data-ttu-id="08c4d-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08c4d-246">0x00000000</span></span>                                                                              |
| <span data-ttu-id="08c4d-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-247">System-Flags</span></span>           | <span data-ttu-id="08c4d-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08c4d-248">0x00000010</span></span>                                                                              |
| <span data-ttu-id="08c4d-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08c4d-249">Classes used in</span></span>        | [<span data-ttu-id="08c4d-250">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08c4d-250">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="08c4d-251">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="08c4d-251">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="08c4d-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08c4d-252">Windows Server 2012</span></span>



| <span data-ttu-id="08c4d-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="08c4d-253">Entry</span></span> | <span data-ttu-id="08c4d-254">Value</span><span class="sxs-lookup"><span data-stu-id="08c4d-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08c4d-255">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="08c4d-255">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="08c4d-256">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="08c4d-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="08c4d-257">System-Only</span></span>            | <span data-ttu-id="08c4d-258">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-258">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-259">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="08c4d-259">Is-Single-Valued</span></span>       | <span data-ttu-id="08c4d-260">True</span><span class="sxs-lookup"><span data-stu-id="08c4d-260">True</span></span>                                                                                    |
| <span data-ttu-id="08c4d-261">Está indexado</span><span class="sxs-lookup"><span data-stu-id="08c4d-261">Is Indexed</span></span>             | <span data-ttu-id="08c4d-262">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-262">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-263">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="08c4d-263">In Global Catalog</span></span>      | <span data-ttu-id="08c4d-264">False</span><span class="sxs-lookup"><span data-stu-id="08c4d-264">False</span></span>                                                                                   |
| <span data-ttu-id="08c4d-265">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="08c4d-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="08c4d-266">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="08c4d-266">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="08c4d-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="08c4d-267">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="08c4d-268">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="08c4d-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-269">Search-Flags</span></span>           | <span data-ttu-id="08c4d-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="08c4d-270">0x00000000</span></span>                                                                              |
| <span data-ttu-id="08c4d-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="08c4d-271">System-Flags</span></span>           | <span data-ttu-id="08c4d-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08c4d-272">0x00000010</span></span>                                                                              |
| <span data-ttu-id="08c4d-273">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="08c4d-273">Classes used in</span></span>        | [<span data-ttu-id="08c4d-274">**Referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="08c4d-274">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="08c4d-275">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="08c4d-275">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






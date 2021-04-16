---
title: Atributo Max-Renew-Age
description: Este atributo determina el período de tiempo, en días, durante el que se puede renovar el vale de concesión de vales (TGT) de un usuario para la autenticación Kerberos. La configuración predeterminada es de 7 días en el dominio predeterminado directiva de grupo objeto (GPO).
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Max-Renew-Age
- maxRenewAge esquema de AD de atributos
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0068beff1f7d7af1ab66f01f7236dcc4b0116c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658613"
---
# <a name="max-renew-age-attribute"></a><span data-ttu-id="019e8-106">Atributo Max-Renew-Age</span><span class="sxs-lookup"><span data-stu-id="019e8-106">Max-Renew-Age attribute</span></span>

<span data-ttu-id="019e8-107">Este atributo determina el período de tiempo, en días, durante el que se puede renovar el vale de concesión de vales (TGT) de un usuario para la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="019e8-107">This attribute determines the time period, in days, during which a user's ticket-granting ticket (TGT) can be renewed for purposes of Kerberos authentication.</span></span> <span data-ttu-id="019e8-108">La configuración predeterminada es de 7 días en el dominio predeterminado directiva de grupo objeto (GPO).</span><span class="sxs-lookup"><span data-stu-id="019e8-108">The default setting is 7 days in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="019e8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="019e8-109">Entry</span></span> | <span data-ttu-id="019e8-110">Value</span><span class="sxs-lookup"><span data-stu-id="019e8-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="019e8-111">CN</span><span class="sxs-lookup"><span data-stu-id="019e8-111">CN</span></span>                | <span data-ttu-id="019e8-112">Max-Renew-Age</span><span class="sxs-lookup"><span data-stu-id="019e8-112">Max-Renew-Age</span></span>                        |
| <span data-ttu-id="019e8-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="019e8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="019e8-114">maxRenewAge</span><span class="sxs-lookup"><span data-stu-id="019e8-114">maxRenewAge</span></span>                          |
| <span data-ttu-id="019e8-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="019e8-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="019e8-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="019e8-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="019e8-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="019e8-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="019e8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="019e8-118">Attribute-Id</span></span>      | <span data-ttu-id="019e8-119">1.2.840.113556.1.4.75</span><span class="sxs-lookup"><span data-stu-id="019e8-119">1.2.840.113556.1.4.75</span></span>                |
| <span data-ttu-id="019e8-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="019e8-120">System-Id-Guid</span></span>    | <span data-ttu-id="019e8-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="019e8-121">bf9679bc-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="019e8-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="019e8-122">Syntax</span></span>            | [<span data-ttu-id="019e8-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="019e8-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="019e8-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="019e8-124">Implementations</span></span>

-   [<span data-ttu-id="019e8-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="019e8-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="019e8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="019e8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="019e8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="019e8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="019e8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="019e8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="019e8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="019e8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="019e8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="019e8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="019e8-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="019e8-131">Windows 2000 Server</span></span>



| <span data-ttu-id="019e8-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="019e8-132">Entry</span></span> | <span data-ttu-id="019e8-133">Value</span><span class="sxs-lookup"><span data-stu-id="019e8-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="019e8-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="019e8-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019e8-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="019e8-136">System-Only</span></span>            | <span data-ttu-id="019e8-137">False</span><span class="sxs-lookup"><span data-stu-id="019e8-137">False</span></span>                                              |
| <span data-ttu-id="019e8-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="019e8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="019e8-139">True</span><span class="sxs-lookup"><span data-stu-id="019e8-139">True</span></span>                                               |
| <span data-ttu-id="019e8-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="019e8-140">Is Indexed</span></span>             | <span data-ttu-id="019e8-141">False</span><span class="sxs-lookup"><span data-stu-id="019e8-141">False</span></span>                                              |
| <span data-ttu-id="019e8-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="019e8-142">In Global Catalog</span></span>      | <span data-ttu-id="019e8-143">False</span><span class="sxs-lookup"><span data-stu-id="019e8-143">False</span></span>                                              |
| <span data-ttu-id="019e8-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="019e8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="019e8-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="019e8-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="019e8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019e8-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019e8-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-148">Search-Flags</span></span>           | <span data-ttu-id="019e8-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="019e8-149">0x00000000</span></span>                                         |
| <span data-ttu-id="019e8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-150">System-Flags</span></span>           | <span data-ttu-id="019e8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019e8-151">0x00000010</span></span>                                         |
| <span data-ttu-id="019e8-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="019e8-152">Classes used in</span></span>        | [<span data-ttu-id="019e8-153">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="019e8-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="019e8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="019e8-154">Windows Server 2003</span></span>



| <span data-ttu-id="019e8-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="019e8-155">Entry</span></span> | <span data-ttu-id="019e8-156">Value</span><span class="sxs-lookup"><span data-stu-id="019e8-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="019e8-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="019e8-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019e8-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="019e8-159">System-Only</span></span>            | <span data-ttu-id="019e8-160">False</span><span class="sxs-lookup"><span data-stu-id="019e8-160">False</span></span>                                              |
| <span data-ttu-id="019e8-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="019e8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="019e8-162">True</span><span class="sxs-lookup"><span data-stu-id="019e8-162">True</span></span>                                               |
| <span data-ttu-id="019e8-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="019e8-163">Is Indexed</span></span>             | <span data-ttu-id="019e8-164">False</span><span class="sxs-lookup"><span data-stu-id="019e8-164">False</span></span>                                              |
| <span data-ttu-id="019e8-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="019e8-165">In Global Catalog</span></span>      | <span data-ttu-id="019e8-166">False</span><span class="sxs-lookup"><span data-stu-id="019e8-166">False</span></span>                                              |
| <span data-ttu-id="019e8-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="019e8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="019e8-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="019e8-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="019e8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019e8-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019e8-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-171">Search-Flags</span></span>           | <span data-ttu-id="019e8-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="019e8-172">0x00000000</span></span>                                         |
| <span data-ttu-id="019e8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-173">System-Flags</span></span>           | <span data-ttu-id="019e8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019e8-174">0x00000010</span></span>                                         |
| <span data-ttu-id="019e8-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="019e8-175">Classes used in</span></span>        | [<span data-ttu-id="019e8-176">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="019e8-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="019e8-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="019e8-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="019e8-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="019e8-178">Entry</span></span> | <span data-ttu-id="019e8-179">Value</span><span class="sxs-lookup"><span data-stu-id="019e8-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="019e8-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="019e8-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019e8-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="019e8-182">System-Only</span></span>            | <span data-ttu-id="019e8-183">False</span><span class="sxs-lookup"><span data-stu-id="019e8-183">False</span></span>                                              |
| <span data-ttu-id="019e8-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="019e8-184">Is-Single-Valued</span></span>       | <span data-ttu-id="019e8-185">True</span><span class="sxs-lookup"><span data-stu-id="019e8-185">True</span></span>                                               |
| <span data-ttu-id="019e8-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="019e8-186">Is Indexed</span></span>             | <span data-ttu-id="019e8-187">False</span><span class="sxs-lookup"><span data-stu-id="019e8-187">False</span></span>                                              |
| <span data-ttu-id="019e8-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="019e8-188">In Global Catalog</span></span>      | <span data-ttu-id="019e8-189">False</span><span class="sxs-lookup"><span data-stu-id="019e8-189">False</span></span>                                              |
| <span data-ttu-id="019e8-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="019e8-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="019e8-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="019e8-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="019e8-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019e8-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019e8-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-194">Search-Flags</span></span>           | <span data-ttu-id="019e8-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="019e8-195">0x00000000</span></span>                                         |
| <span data-ttu-id="019e8-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-196">System-Flags</span></span>           | <span data-ttu-id="019e8-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019e8-197">0x00000010</span></span>                                         |
| <span data-ttu-id="019e8-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="019e8-198">Classes used in</span></span>        | [<span data-ttu-id="019e8-199">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="019e8-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="019e8-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="019e8-200">Windows Server 2008</span></span>



| <span data-ttu-id="019e8-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="019e8-201">Entry</span></span> | <span data-ttu-id="019e8-202">Value</span><span class="sxs-lookup"><span data-stu-id="019e8-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="019e8-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="019e8-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019e8-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="019e8-205">System-Only</span></span>            | <span data-ttu-id="019e8-206">False</span><span class="sxs-lookup"><span data-stu-id="019e8-206">False</span></span>                                              |
| <span data-ttu-id="019e8-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="019e8-207">Is-Single-Valued</span></span>       | <span data-ttu-id="019e8-208">True</span><span class="sxs-lookup"><span data-stu-id="019e8-208">True</span></span>                                               |
| <span data-ttu-id="019e8-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="019e8-209">Is Indexed</span></span>             | <span data-ttu-id="019e8-210">False</span><span class="sxs-lookup"><span data-stu-id="019e8-210">False</span></span>                                              |
| <span data-ttu-id="019e8-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="019e8-211">In Global Catalog</span></span>      | <span data-ttu-id="019e8-212">False</span><span class="sxs-lookup"><span data-stu-id="019e8-212">False</span></span>                                              |
| <span data-ttu-id="019e8-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="019e8-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="019e8-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="019e8-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="019e8-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019e8-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019e8-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-217">Search-Flags</span></span>           | <span data-ttu-id="019e8-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="019e8-218">0x00000000</span></span>                                         |
| <span data-ttu-id="019e8-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-219">System-Flags</span></span>           | <span data-ttu-id="019e8-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019e8-220">0x00000010</span></span>                                         |
| <span data-ttu-id="019e8-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="019e8-221">Classes used in</span></span>        | [<span data-ttu-id="019e8-222">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="019e8-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="019e8-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="019e8-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="019e8-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="019e8-224">Entry</span></span> | <span data-ttu-id="019e8-225">Value</span><span class="sxs-lookup"><span data-stu-id="019e8-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="019e8-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="019e8-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019e8-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="019e8-228">System-Only</span></span>            | <span data-ttu-id="019e8-229">False</span><span class="sxs-lookup"><span data-stu-id="019e8-229">False</span></span>                                              |
| <span data-ttu-id="019e8-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="019e8-230">Is-Single-Valued</span></span>       | <span data-ttu-id="019e8-231">True</span><span class="sxs-lookup"><span data-stu-id="019e8-231">True</span></span>                                               |
| <span data-ttu-id="019e8-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="019e8-232">Is Indexed</span></span>             | <span data-ttu-id="019e8-233">False</span><span class="sxs-lookup"><span data-stu-id="019e8-233">False</span></span>                                              |
| <span data-ttu-id="019e8-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="019e8-234">In Global Catalog</span></span>      | <span data-ttu-id="019e8-235">False</span><span class="sxs-lookup"><span data-stu-id="019e8-235">False</span></span>                                              |
| <span data-ttu-id="019e8-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="019e8-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="019e8-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="019e8-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="019e8-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019e8-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019e8-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-240">Search-Flags</span></span>           | <span data-ttu-id="019e8-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="019e8-241">0x00000000</span></span>                                         |
| <span data-ttu-id="019e8-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-242">System-Flags</span></span>           | <span data-ttu-id="019e8-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019e8-243">0x00000010</span></span>                                         |
| <span data-ttu-id="019e8-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="019e8-244">Classes used in</span></span>        | [<span data-ttu-id="019e8-245">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="019e8-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="019e8-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="019e8-246">Windows Server 2012</span></span>



| <span data-ttu-id="019e8-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="019e8-247">Entry</span></span> | <span data-ttu-id="019e8-248">Value</span><span class="sxs-lookup"><span data-stu-id="019e8-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="019e8-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="019e8-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="019e8-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="019e8-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="019e8-251">System-Only</span></span>            | <span data-ttu-id="019e8-252">False</span><span class="sxs-lookup"><span data-stu-id="019e8-252">False</span></span>                                              |
| <span data-ttu-id="019e8-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="019e8-253">Is-Single-Valued</span></span>       | <span data-ttu-id="019e8-254">True</span><span class="sxs-lookup"><span data-stu-id="019e8-254">True</span></span>                                               |
| <span data-ttu-id="019e8-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="019e8-255">Is Indexed</span></span>             | <span data-ttu-id="019e8-256">False</span><span class="sxs-lookup"><span data-stu-id="019e8-256">False</span></span>                                              |
| <span data-ttu-id="019e8-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="019e8-257">In Global Catalog</span></span>      | <span data-ttu-id="019e8-258">False</span><span class="sxs-lookup"><span data-stu-id="019e8-258">False</span></span>                                              |
| <span data-ttu-id="019e8-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="019e8-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="019e8-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="019e8-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="019e8-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="019e8-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="019e8-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="019e8-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-263">Search-Flags</span></span>           | <span data-ttu-id="019e8-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="019e8-264">0x00000000</span></span>                                         |
| <span data-ttu-id="019e8-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="019e8-265">System-Flags</span></span>           | <span data-ttu-id="019e8-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="019e8-266">0x00000010</span></span>                                         |
| <span data-ttu-id="019e8-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="019e8-267">Classes used in</span></span>        | [<span data-ttu-id="019e8-268">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="019e8-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 






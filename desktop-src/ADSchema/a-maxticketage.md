---
title: Atributo Max-ticket-Age
description: Este atributo determina el tiempo máximo, en horas, que se puede usar el vale de concesión de vales (TGT) de un usuario para la autenticación Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Max-ticket-Age
- maxTicketAge esquema de AD de atributos
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804411"
---
# <a name="max-ticket-age-attribute"></a><span data-ttu-id="b2078-105">Atributo Max-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="b2078-105">Max-Ticket-Age attribute</span></span>

<span data-ttu-id="b2078-106">Este atributo determina el tiempo máximo, en horas, que se puede usar el vale de concesión de vales (TGT) de un usuario para la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b2078-106">This attribute determines the maximum amount of time, in hours, that a user's ticket-granting ticket (TGT) can be used for the purpose of Kerberos authentication.</span></span> <span data-ttu-id="b2078-107">Cuando expire el TGT de un usuario, se debe solicitar uno nuevo o se debe renovar el existente.</span><span class="sxs-lookup"><span data-stu-id="b2078-107">When a user's TGT expires, a new one must be requested, or the existing one must be renewed.</span></span> <span data-ttu-id="b2078-108">De forma predeterminada, este valor se establece en 10 horas en el dominio predeterminado directiva de grupo objeto (GPO).</span><span class="sxs-lookup"><span data-stu-id="b2078-108">By default, this setting is set to 10 hours in the Default Domain Group Policy object (GPO).</span></span>



| <span data-ttu-id="b2078-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2078-109">Entry</span></span> | <span data-ttu-id="b2078-110">Value</span><span class="sxs-lookup"><span data-stu-id="b2078-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b2078-111">CN</span><span class="sxs-lookup"><span data-stu-id="b2078-111">CN</span></span>                | <span data-ttu-id="b2078-112">Max-ticket-Age</span><span class="sxs-lookup"><span data-stu-id="b2078-112">Max-Ticket-Age</span></span>                       |
| <span data-ttu-id="b2078-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b2078-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b2078-114">maxTicketAge</span><span class="sxs-lookup"><span data-stu-id="b2078-114">maxTicketAge</span></span>                         |
| <span data-ttu-id="b2078-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b2078-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="b2078-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b2078-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b2078-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b2078-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b2078-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b2078-118">Attribute-Id</span></span>      | <span data-ttu-id="b2078-119">1.2.840.113556.1.4.77</span><span class="sxs-lookup"><span data-stu-id="b2078-119">1.2.840.113556.1.4.77</span></span>                |
| <span data-ttu-id="b2078-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b2078-120">System-Id-Guid</span></span>    | <span data-ttu-id="b2078-121">bf9679be-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b2078-121">bf9679be-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b2078-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2078-122">Syntax</span></span>            | [<span data-ttu-id="b2078-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="b2078-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="b2078-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b2078-124">Implementations</span></span>

-   [<span data-ttu-id="b2078-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b2078-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b2078-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b2078-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b2078-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b2078-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b2078-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b2078-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b2078-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b2078-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b2078-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b2078-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b2078-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2078-131">Windows 2000 Server</span></span>



| <span data-ttu-id="b2078-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2078-132">Entry</span></span> | <span data-ttu-id="b2078-133">Value</span><span class="sxs-lookup"><span data-stu-id="b2078-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b2078-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b2078-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2078-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2078-136">System-Only</span></span>            | <span data-ttu-id="b2078-137">False</span><span class="sxs-lookup"><span data-stu-id="b2078-137">False</span></span>                                              |
| <span data-ttu-id="b2078-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b2078-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b2078-139">True</span><span class="sxs-lookup"><span data-stu-id="b2078-139">True</span></span>                                               |
| <span data-ttu-id="b2078-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b2078-140">Is Indexed</span></span>             | <span data-ttu-id="b2078-141">False</span><span class="sxs-lookup"><span data-stu-id="b2078-141">False</span></span>                                              |
| <span data-ttu-id="b2078-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b2078-142">In Global Catalog</span></span>      | <span data-ttu-id="b2078-143">False</span><span class="sxs-lookup"><span data-stu-id="b2078-143">False</span></span>                                              |
| <span data-ttu-id="b2078-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b2078-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2078-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2078-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b2078-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2078-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2078-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-148">Search-Flags</span></span>           | <span data-ttu-id="b2078-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2078-149">0x00000000</span></span>                                         |
| <span data-ttu-id="b2078-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-150">System-Flags</span></span>           | <span data-ttu-id="b2078-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2078-151">0x00000010</span></span>                                         |
| <span data-ttu-id="b2078-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b2078-152">Classes used in</span></span>        | [<span data-ttu-id="b2078-153">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="b2078-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b2078-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2078-154">Windows Server 2003</span></span>



| <span data-ttu-id="b2078-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2078-155">Entry</span></span> | <span data-ttu-id="b2078-156">Value</span><span class="sxs-lookup"><span data-stu-id="b2078-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b2078-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b2078-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2078-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2078-159">System-Only</span></span>            | <span data-ttu-id="b2078-160">False</span><span class="sxs-lookup"><span data-stu-id="b2078-160">False</span></span>                                              |
| <span data-ttu-id="b2078-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b2078-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b2078-162">True</span><span class="sxs-lookup"><span data-stu-id="b2078-162">True</span></span>                                               |
| <span data-ttu-id="b2078-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b2078-163">Is Indexed</span></span>             | <span data-ttu-id="b2078-164">False</span><span class="sxs-lookup"><span data-stu-id="b2078-164">False</span></span>                                              |
| <span data-ttu-id="b2078-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b2078-165">In Global Catalog</span></span>      | <span data-ttu-id="b2078-166">False</span><span class="sxs-lookup"><span data-stu-id="b2078-166">False</span></span>                                              |
| <span data-ttu-id="b2078-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b2078-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2078-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2078-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b2078-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2078-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2078-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-171">Search-Flags</span></span>           | <span data-ttu-id="b2078-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2078-172">0x00000000</span></span>                                         |
| <span data-ttu-id="b2078-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-173">System-Flags</span></span>           | <span data-ttu-id="b2078-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2078-174">0x00000010</span></span>                                         |
| <span data-ttu-id="b2078-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b2078-175">Classes used in</span></span>        | [<span data-ttu-id="b2078-176">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="b2078-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b2078-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b2078-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b2078-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2078-178">Entry</span></span> | <span data-ttu-id="b2078-179">Value</span><span class="sxs-lookup"><span data-stu-id="b2078-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b2078-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b2078-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2078-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2078-182">System-Only</span></span>            | <span data-ttu-id="b2078-183">False</span><span class="sxs-lookup"><span data-stu-id="b2078-183">False</span></span>                                              |
| <span data-ttu-id="b2078-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b2078-184">Is-Single-Valued</span></span>       | <span data-ttu-id="b2078-185">True</span><span class="sxs-lookup"><span data-stu-id="b2078-185">True</span></span>                                               |
| <span data-ttu-id="b2078-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b2078-186">Is Indexed</span></span>             | <span data-ttu-id="b2078-187">False</span><span class="sxs-lookup"><span data-stu-id="b2078-187">False</span></span>                                              |
| <span data-ttu-id="b2078-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b2078-188">In Global Catalog</span></span>      | <span data-ttu-id="b2078-189">False</span><span class="sxs-lookup"><span data-stu-id="b2078-189">False</span></span>                                              |
| <span data-ttu-id="b2078-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b2078-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2078-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2078-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b2078-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2078-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2078-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-194">Search-Flags</span></span>           | <span data-ttu-id="b2078-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2078-195">0x00000000</span></span>                                         |
| <span data-ttu-id="b2078-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-196">System-Flags</span></span>           | <span data-ttu-id="b2078-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2078-197">0x00000010</span></span>                                         |
| <span data-ttu-id="b2078-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b2078-198">Classes used in</span></span>        | [<span data-ttu-id="b2078-199">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="b2078-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b2078-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2078-200">Windows Server 2008</span></span>



| <span data-ttu-id="b2078-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2078-201">Entry</span></span> | <span data-ttu-id="b2078-202">Value</span><span class="sxs-lookup"><span data-stu-id="b2078-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b2078-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b2078-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2078-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2078-205">System-Only</span></span>            | <span data-ttu-id="b2078-206">False</span><span class="sxs-lookup"><span data-stu-id="b2078-206">False</span></span>                                              |
| <span data-ttu-id="b2078-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b2078-207">Is-Single-Valued</span></span>       | <span data-ttu-id="b2078-208">True</span><span class="sxs-lookup"><span data-stu-id="b2078-208">True</span></span>                                               |
| <span data-ttu-id="b2078-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b2078-209">Is Indexed</span></span>             | <span data-ttu-id="b2078-210">False</span><span class="sxs-lookup"><span data-stu-id="b2078-210">False</span></span>                                              |
| <span data-ttu-id="b2078-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b2078-211">In Global Catalog</span></span>      | <span data-ttu-id="b2078-212">False</span><span class="sxs-lookup"><span data-stu-id="b2078-212">False</span></span>                                              |
| <span data-ttu-id="b2078-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b2078-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2078-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2078-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b2078-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2078-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2078-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-217">Search-Flags</span></span>           | <span data-ttu-id="b2078-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2078-218">0x00000000</span></span>                                         |
| <span data-ttu-id="b2078-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-219">System-Flags</span></span>           | <span data-ttu-id="b2078-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2078-220">0x00000010</span></span>                                         |
| <span data-ttu-id="b2078-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b2078-221">Classes used in</span></span>        | [<span data-ttu-id="b2078-222">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="b2078-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b2078-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2078-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b2078-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2078-224">Entry</span></span> | <span data-ttu-id="b2078-225">Value</span><span class="sxs-lookup"><span data-stu-id="b2078-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b2078-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b2078-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2078-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2078-228">System-Only</span></span>            | <span data-ttu-id="b2078-229">False</span><span class="sxs-lookup"><span data-stu-id="b2078-229">False</span></span>                                              |
| <span data-ttu-id="b2078-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b2078-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b2078-231">True</span><span class="sxs-lookup"><span data-stu-id="b2078-231">True</span></span>                                               |
| <span data-ttu-id="b2078-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b2078-232">Is Indexed</span></span>             | <span data-ttu-id="b2078-233">False</span><span class="sxs-lookup"><span data-stu-id="b2078-233">False</span></span>                                              |
| <span data-ttu-id="b2078-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b2078-234">In Global Catalog</span></span>      | <span data-ttu-id="b2078-235">False</span><span class="sxs-lookup"><span data-stu-id="b2078-235">False</span></span>                                              |
| <span data-ttu-id="b2078-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b2078-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2078-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2078-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b2078-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2078-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2078-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-240">Search-Flags</span></span>           | <span data-ttu-id="b2078-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2078-241">0x00000000</span></span>                                         |
| <span data-ttu-id="b2078-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-242">System-Flags</span></span>           | <span data-ttu-id="b2078-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2078-243">0x00000010</span></span>                                         |
| <span data-ttu-id="b2078-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b2078-244">Classes used in</span></span>        | [<span data-ttu-id="b2078-245">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="b2078-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b2078-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2078-246">Windows Server 2012</span></span>



| <span data-ttu-id="b2078-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="b2078-247">Entry</span></span> | <span data-ttu-id="b2078-248">Value</span><span class="sxs-lookup"><span data-stu-id="b2078-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="b2078-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b2078-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2078-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="b2078-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2078-251">System-Only</span></span>            | <span data-ttu-id="b2078-252">False</span><span class="sxs-lookup"><span data-stu-id="b2078-252">False</span></span>                                              |
| <span data-ttu-id="b2078-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b2078-253">Is-Single-Valued</span></span>       | <span data-ttu-id="b2078-254">True</span><span class="sxs-lookup"><span data-stu-id="b2078-254">True</span></span>                                               |
| <span data-ttu-id="b2078-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b2078-255">Is Indexed</span></span>             | <span data-ttu-id="b2078-256">False</span><span class="sxs-lookup"><span data-stu-id="b2078-256">False</span></span>                                              |
| <span data-ttu-id="b2078-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b2078-257">In Global Catalog</span></span>      | <span data-ttu-id="b2078-258">False</span><span class="sxs-lookup"><span data-stu-id="b2078-258">False</span></span>                                              |
| <span data-ttu-id="b2078-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b2078-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2078-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2078-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="b2078-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2078-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2078-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="b2078-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-263">Search-Flags</span></span>           | <span data-ttu-id="b2078-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2078-264">0x00000000</span></span>                                         |
| <span data-ttu-id="b2078-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2078-265">System-Flags</span></span>           | <span data-ttu-id="b2078-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2078-266">0x00000010</span></span>                                         |
| <span data-ttu-id="b2078-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b2078-267">Classes used in</span></span>        | [<span data-ttu-id="b2078-268">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="b2078-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 






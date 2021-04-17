---
title: Account-Expires atributo)
description: Fecha de expiración de la cuenta.
ms.assetid: 8c3c565e-77fe-4e8b-970a-8396fc6b45aa
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Account-Expires
- accountExpires esquema de AD de atributos
topic_type:
- apiref
api_name:
- Account-Expires
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb5041c544f96f79ad4c3172d776ebe909b1983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659203"
---
# <a name="account-expires-attribute"></a><span data-ttu-id="ff2a2-105">Account-Expires atributo)</span><span class="sxs-lookup"><span data-stu-id="ff2a2-105">Account-Expires attribute</span></span>

<span data-ttu-id="ff2a2-106">Fecha de expiración de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="ff2a2-106">The date when the account expires.</span></span> <span data-ttu-id="ff2a2-107">Este valor representa el número de intervalos de 100 segundos desde el 1 de enero de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="ff2a2-107">This value represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="ff2a2-108">Un valor de 0 o 0x7FFFFFFFFFFFFFFF (9223372036854775807) indica que la cuenta nunca expira.</span><span class="sxs-lookup"><span data-stu-id="ff2a2-108">A value of 0 or 0x7FFFFFFFFFFFFFFF (9223372036854775807) indicates that the account never expires.</span></span>



| <span data-ttu-id="ff2a2-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2a2-109">Entry</span></span> | <span data-ttu-id="ff2a2-110">Value</span><span class="sxs-lookup"><span data-stu-id="ff2a2-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ff2a2-111">CN</span><span class="sxs-lookup"><span data-stu-id="ff2a2-111">CN</span></span>                | <span data-ttu-id="ff2a2-112">Account-Expires</span><span class="sxs-lookup"><span data-stu-id="ff2a2-112">Account-Expires</span></span>                                                        |
| <span data-ttu-id="ff2a2-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ff2a2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ff2a2-114">accountExpires</span><span class="sxs-lookup"><span data-stu-id="ff2a2-114">accountExpires</span></span>                                                         |
| <span data-ttu-id="ff2a2-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ff2a2-115">Size</span></span>              | <span data-ttu-id="ff2a2-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="ff2a2-116">8 bytes</span></span>                                                                |
| <span data-ttu-id="ff2a2-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ff2a2-117">Update Privilege</span></span>  | <span data-ttu-id="ff2a2-118">El administrador de dominio establece este atributo.</span><span class="sxs-lookup"><span data-stu-id="ff2a2-118">The domain administrator sets this attribute.</span></span>                          |
| <span data-ttu-id="ff2a2-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ff2a2-119">Update Frequency</span></span>  | <span data-ttu-id="ff2a2-120">Cada vez que la fecha de expiración anterior expira y debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="ff2a2-120">Whenever the previous expiration date expires and needs to be updated.</span></span> |
| <span data-ttu-id="ff2a2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ff2a2-121">Attribute-Id</span></span>      | <span data-ttu-id="ff2a2-122">1.2.840.113556.1.4.159</span><span class="sxs-lookup"><span data-stu-id="ff2a2-122">1.2.840.113556.1.4.159</span></span>                                                 |
| <span data-ttu-id="ff2a2-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ff2a2-123">System-Id-Guid</span></span>    | <span data-ttu-id="ff2a2-124">bf967915-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ff2a2-124">bf967915-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="ff2a2-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff2a2-125">Syntax</span></span>            | [<span data-ttu-id="ff2a2-126">**Interval**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-126">**Interval**</span></span>](s-interval.md)                                         |



## <a name="implementations"></a><span data-ttu-id="ff2a2-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ff2a2-127">Implementations</span></span>

-   [<span data-ttu-id="ff2a2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ff2a2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff2a2-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ff2a2-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff2a2-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff2a2-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff2a2-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ff2a2-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff2a2-135">Windows 2000 Server</span></span>



| <span data-ttu-id="ff2a2-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2a2-136">Entry</span></span> | <span data-ttu-id="ff2a2-137">Value</span><span class="sxs-lookup"><span data-stu-id="ff2a2-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ff2a2-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff2a2-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff2a2-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff2a2-140">System-Only</span></span>            | <span data-ttu-id="ff2a2-141">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-141">False</span></span>                             |
| <span data-ttu-id="ff2a2-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff2a2-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ff2a2-143">True</span><span class="sxs-lookup"><span data-stu-id="ff2a2-143">True</span></span>                              |
| <span data-ttu-id="ff2a2-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff2a2-144">Is Indexed</span></span>             | <span data-ttu-id="ff2a2-145">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-145">False</span></span>                             |
| <span data-ttu-id="ff2a2-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff2a2-146">In Global Catalog</span></span>      | <span data-ttu-id="ff2a2-147">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-147">False</span></span>                             |
| <span data-ttu-id="ff2a2-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff2a2-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff2a2-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff2a2-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ff2a2-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff2a2-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff2a2-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-152">Search-Flags</span></span>           | <span data-ttu-id="ff2a2-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-153">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-154">System-Flags</span></span>           | <span data-ttu-id="ff2a2-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-155">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-156">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff2a2-156">Classes used in</span></span>        | [<span data-ttu-id="ff2a2-157">**User**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ff2a2-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff2a2-158">Windows Server 2003</span></span>



| <span data-ttu-id="ff2a2-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2a2-159">Entry</span></span> | <span data-ttu-id="ff2a2-160">Value</span><span class="sxs-lookup"><span data-stu-id="ff2a2-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ff2a2-161">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff2a2-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff2a2-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff2a2-163">System-Only</span></span>            | <span data-ttu-id="ff2a2-164">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-164">False</span></span>                             |
| <span data-ttu-id="ff2a2-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff2a2-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ff2a2-166">True</span><span class="sxs-lookup"><span data-stu-id="ff2a2-166">True</span></span>                              |
| <span data-ttu-id="ff2a2-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff2a2-167">Is Indexed</span></span>             | <span data-ttu-id="ff2a2-168">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-168">False</span></span>                             |
| <span data-ttu-id="ff2a2-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff2a2-169">In Global Catalog</span></span>      | <span data-ttu-id="ff2a2-170">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-170">False</span></span>                             |
| <span data-ttu-id="ff2a2-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff2a2-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff2a2-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff2a2-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ff2a2-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff2a2-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff2a2-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-175">Search-Flags</span></span>           | <span data-ttu-id="ff2a2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-176">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-177">System-Flags</span></span>           | <span data-ttu-id="ff2a2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-178">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff2a2-179">Classes used in</span></span>        | [<span data-ttu-id="ff2a2-180">**User**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ff2a2-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="ff2a2-181">ADAM</span></span>



| <span data-ttu-id="ff2a2-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2a2-182">Entry</span></span> | <span data-ttu-id="ff2a2-183">Value</span><span class="sxs-lookup"><span data-stu-id="ff2a2-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ff2a2-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff2a2-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ff2a2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff2a2-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ff2a2-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff2a2-186">System-Only</span></span>            | <span data-ttu-id="ff2a2-187">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-187">False</span></span>                                                             |
| <span data-ttu-id="ff2a2-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff2a2-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ff2a2-189">True</span><span class="sxs-lookup"><span data-stu-id="ff2a2-189">True</span></span>                                                              |
| <span data-ttu-id="ff2a2-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff2a2-190">Is Indexed</span></span>             | <span data-ttu-id="ff2a2-191">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-191">False</span></span>                                                             |
| <span data-ttu-id="ff2a2-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff2a2-192">In Global Catalog</span></span>      | <span data-ttu-id="ff2a2-193">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-193">False</span></span>                                                             |
| <span data-ttu-id="ff2a2-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff2a2-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff2a2-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff2a2-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ff2a2-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff2a2-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ff2a2-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff2a2-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ff2a2-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-198">Search-Flags</span></span>           | <span data-ttu-id="ff2a2-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-199">0x00000010</span></span>                                                        |
| <span data-ttu-id="ff2a2-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-200">System-Flags</span></span>           | <span data-ttu-id="ff2a2-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="ff2a2-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff2a2-202">Classes used in</span></span>        | [<span data-ttu-id="ff2a2-203">**Objeto MS-DS-Bindable**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff2a2-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff2a2-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff2a2-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2a2-205">Entry</span></span> | <span data-ttu-id="ff2a2-206">Value</span><span class="sxs-lookup"><span data-stu-id="ff2a2-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ff2a2-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff2a2-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff2a2-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff2a2-209">System-Only</span></span>            | <span data-ttu-id="ff2a2-210">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-210">False</span></span>                             |
| <span data-ttu-id="ff2a2-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff2a2-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ff2a2-212">True</span><span class="sxs-lookup"><span data-stu-id="ff2a2-212">True</span></span>                              |
| <span data-ttu-id="ff2a2-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff2a2-213">Is Indexed</span></span>             | <span data-ttu-id="ff2a2-214">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-214">False</span></span>                             |
| <span data-ttu-id="ff2a2-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff2a2-215">In Global Catalog</span></span>      | <span data-ttu-id="ff2a2-216">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-216">False</span></span>                             |
| <span data-ttu-id="ff2a2-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff2a2-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff2a2-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff2a2-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ff2a2-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff2a2-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff2a2-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-221">Search-Flags</span></span>           | <span data-ttu-id="ff2a2-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-222">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-223">System-Flags</span></span>           | <span data-ttu-id="ff2a2-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-224">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff2a2-225">Classes used in</span></span>        | [<span data-ttu-id="ff2a2-226">**User**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ff2a2-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff2a2-227">Windows Server 2008</span></span>



| <span data-ttu-id="ff2a2-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2a2-228">Entry</span></span> | <span data-ttu-id="ff2a2-229">Value</span><span class="sxs-lookup"><span data-stu-id="ff2a2-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ff2a2-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff2a2-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff2a2-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff2a2-232">System-Only</span></span>            | <span data-ttu-id="ff2a2-233">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-233">False</span></span>                             |
| <span data-ttu-id="ff2a2-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff2a2-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ff2a2-235">True</span><span class="sxs-lookup"><span data-stu-id="ff2a2-235">True</span></span>                              |
| <span data-ttu-id="ff2a2-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff2a2-236">Is Indexed</span></span>             | <span data-ttu-id="ff2a2-237">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-237">False</span></span>                             |
| <span data-ttu-id="ff2a2-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff2a2-238">In Global Catalog</span></span>      | <span data-ttu-id="ff2a2-239">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-239">False</span></span>                             |
| <span data-ttu-id="ff2a2-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff2a2-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff2a2-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff2a2-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ff2a2-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff2a2-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff2a2-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-244">Search-Flags</span></span>           | <span data-ttu-id="ff2a2-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-245">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-246">System-Flags</span></span>           | <span data-ttu-id="ff2a2-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-247">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff2a2-248">Classes used in</span></span>        | [<span data-ttu-id="ff2a2-249">**User**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff2a2-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff2a2-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff2a2-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2a2-251">Entry</span></span> | <span data-ttu-id="ff2a2-252">Value</span><span class="sxs-lookup"><span data-stu-id="ff2a2-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ff2a2-253">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff2a2-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff2a2-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff2a2-255">System-Only</span></span>            | <span data-ttu-id="ff2a2-256">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-256">False</span></span>                             |
| <span data-ttu-id="ff2a2-257">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff2a2-257">Is-Single-Valued</span></span>       | <span data-ttu-id="ff2a2-258">True</span><span class="sxs-lookup"><span data-stu-id="ff2a2-258">True</span></span>                              |
| <span data-ttu-id="ff2a2-259">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff2a2-259">Is Indexed</span></span>             | <span data-ttu-id="ff2a2-260">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-260">False</span></span>                             |
| <span data-ttu-id="ff2a2-261">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff2a2-261">In Global Catalog</span></span>      | <span data-ttu-id="ff2a2-262">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-262">False</span></span>                             |
| <span data-ttu-id="ff2a2-263">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff2a2-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff2a2-264">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff2a2-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ff2a2-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff2a2-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff2a2-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-267">Search-Flags</span></span>           | <span data-ttu-id="ff2a2-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-268">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-269">System-Flags</span></span>           | <span data-ttu-id="ff2a2-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-270">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-271">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff2a2-271">Classes used in</span></span>        | [<span data-ttu-id="ff2a2-272">**User**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ff2a2-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff2a2-273">Windows Server 2012</span></span>



| <span data-ttu-id="ff2a2-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff2a2-274">Entry</span></span> | <span data-ttu-id="ff2a2-275">Value</span><span class="sxs-lookup"><span data-stu-id="ff2a2-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ff2a2-276">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ff2a2-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff2a2-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ff2a2-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff2a2-278">System-Only</span></span>            | <span data-ttu-id="ff2a2-279">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-279">False</span></span>                             |
| <span data-ttu-id="ff2a2-280">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ff2a2-280">Is-Single-Valued</span></span>       | <span data-ttu-id="ff2a2-281">True</span><span class="sxs-lookup"><span data-stu-id="ff2a2-281">True</span></span>                              |
| <span data-ttu-id="ff2a2-282">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ff2a2-282">Is Indexed</span></span>             | <span data-ttu-id="ff2a2-283">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-283">False</span></span>                             |
| <span data-ttu-id="ff2a2-284">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff2a2-284">In Global Catalog</span></span>      | <span data-ttu-id="ff2a2-285">False</span><span class="sxs-lookup"><span data-stu-id="ff2a2-285">False</span></span>                             |
| <span data-ttu-id="ff2a2-286">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ff2a2-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff2a2-287">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff2a2-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ff2a2-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff2a2-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff2a2-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ff2a2-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-290">Search-Flags</span></span>           | <span data-ttu-id="ff2a2-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-291">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff2a2-292">System-Flags</span></span>           | <span data-ttu-id="ff2a2-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff2a2-293">0x00000010</span></span>                        |
| <span data-ttu-id="ff2a2-294">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ff2a2-294">Classes used in</span></span>        | [<span data-ttu-id="ff2a2-295">**User**</span><span class="sxs-lookup"><span data-stu-id="ff2a2-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ff2a2-296">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff2a2-296">Remarks</span></span>

<span data-ttu-id="ff2a2-297">La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="ff2a2-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

 


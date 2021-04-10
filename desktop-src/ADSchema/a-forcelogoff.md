---
title: Force-Logoff atributo)
description: Se usa para calcular el tiempo de inicio en SamIGetAccountRestrictions. La hora de cierre de sesión menos forzar el cierre del registro es igual a la hora de inicio.
ms.assetid: 2ce1d5db-52aa-49c5-aef2-ec67122100ed
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Force-Logoff
- forceLogoff esquema de AD de atributos
topic_type:
- apiref
api_name:
- Force-Logoff
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e31cb241cde4deb40d5978594b4354fbcc564b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151421"
---
# <a name="force-logoff-attribute"></a><span data-ttu-id="4caa4-106">Force-Logoff atributo)</span><span class="sxs-lookup"><span data-stu-id="4caa4-106">Force-Logoff attribute</span></span>

<span data-ttu-id="4caa4-107">Se usa para calcular el tiempo de inicio en SamIGetAccountRestrictions.</span><span class="sxs-lookup"><span data-stu-id="4caa4-107">Used in computing the kick off time in SamIGetAccountRestrictions.</span></span> <span data-ttu-id="4caa4-108">La hora de cierre de sesión menos forzar el cierre del registro es igual a la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="4caa4-108">Logoff time minus Force Log off equals kick off time.</span></span>



| <span data-ttu-id="4caa4-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="4caa4-109">Entry</span></span> | <span data-ttu-id="4caa4-110">Value</span><span class="sxs-lookup"><span data-stu-id="4caa4-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4caa4-111">CN</span><span class="sxs-lookup"><span data-stu-id="4caa4-111">CN</span></span>                | <span data-ttu-id="4caa4-112">Force-Logoff</span><span class="sxs-lookup"><span data-stu-id="4caa4-112">Force-Logoff</span></span>                         |
| <span data-ttu-id="4caa4-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="4caa4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4caa4-114">forceLogoff</span><span class="sxs-lookup"><span data-stu-id="4caa4-114">forceLogoff</span></span>                          |
| <span data-ttu-id="4caa4-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="4caa4-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="4caa4-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="4caa4-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4caa4-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="4caa4-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4caa4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4caa4-118">Attribute-Id</span></span>      | <span data-ttu-id="4caa4-119">1.2.840.113556.1.4.39</span><span class="sxs-lookup"><span data-stu-id="4caa4-119">1.2.840.113556.1.4.39</span></span>                |
| <span data-ttu-id="4caa4-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4caa4-120">System-Id-Guid</span></span>    | <span data-ttu-id="4caa4-121">bf967977-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4caa4-121">bf967977-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="4caa4-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4caa4-122">Syntax</span></span>            | [<span data-ttu-id="4caa4-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="4caa4-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4caa4-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="4caa4-124">Implementations</span></span>

-   [<span data-ttu-id="4caa4-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4caa4-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4caa4-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4caa4-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4caa4-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4caa4-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4caa4-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4caa4-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4caa4-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4caa4-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4caa4-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4caa4-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4caa4-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4caa4-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4caa4-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="4caa4-132">Entry</span></span> | <span data-ttu-id="4caa4-133">Value</span><span class="sxs-lookup"><span data-stu-id="4caa4-133">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caa4-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4caa4-134">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4caa4-135">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4caa4-136">System-Only</span></span>            | <span data-ttu-id="4caa4-137">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-137">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4caa4-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4caa4-139">True</span><span class="sxs-lookup"><span data-stu-id="4caa4-139">True</span></span>                                                                                                     |
| <span data-ttu-id="4caa4-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4caa4-140">Is Indexed</span></span>             | <span data-ttu-id="4caa4-141">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-141">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4caa4-142">In Global Catalog</span></span>      | <span data-ttu-id="4caa4-143">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-143">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4caa4-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4caa4-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4caa4-145">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="4caa4-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4caa4-146">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4caa4-147">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-148">Search-Flags</span></span>           | <span data-ttu-id="4caa4-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4caa4-149">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="4caa4-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-150">System-Flags</span></span>           | <span data-ttu-id="4caa4-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4caa4-151">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="4caa4-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4caa4-152">Classes used in</span></span>        | [<span data-ttu-id="4caa4-153">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="4caa4-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="4caa4-154">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="4caa4-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4caa4-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4caa4-155">Windows Server 2003</span></span>



| <span data-ttu-id="4caa4-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="4caa4-156">Entry</span></span> | <span data-ttu-id="4caa4-157">Value</span><span class="sxs-lookup"><span data-stu-id="4caa4-157">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caa4-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4caa4-158">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4caa4-159">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="4caa4-160">System-Only</span></span>            | <span data-ttu-id="4caa4-161">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-161">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4caa4-162">Is-Single-Valued</span></span>       | <span data-ttu-id="4caa4-163">True</span><span class="sxs-lookup"><span data-stu-id="4caa4-163">True</span></span>                                                                                                     |
| <span data-ttu-id="4caa4-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4caa4-164">Is Indexed</span></span>             | <span data-ttu-id="4caa4-165">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-165">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4caa4-166">In Global Catalog</span></span>      | <span data-ttu-id="4caa4-167">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-167">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4caa4-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="4caa4-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4caa4-169">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="4caa4-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4caa4-170">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4caa4-171">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-172">Search-Flags</span></span>           | <span data-ttu-id="4caa4-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4caa4-173">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="4caa4-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-174">System-Flags</span></span>           | <span data-ttu-id="4caa4-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4caa4-175">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="4caa4-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4caa4-176">Classes used in</span></span>        | [<span data-ttu-id="4caa4-177">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="4caa4-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="4caa4-178">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="4caa4-178">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4caa4-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4caa4-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4caa4-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="4caa4-180">Entry</span></span> | <span data-ttu-id="4caa4-181">Value</span><span class="sxs-lookup"><span data-stu-id="4caa4-181">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caa4-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4caa4-182">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4caa4-183">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="4caa4-184">System-Only</span></span>            | <span data-ttu-id="4caa4-185">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-185">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4caa4-186">Is-Single-Valued</span></span>       | <span data-ttu-id="4caa4-187">True</span><span class="sxs-lookup"><span data-stu-id="4caa4-187">True</span></span>                                                                                                     |
| <span data-ttu-id="4caa4-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4caa4-188">Is Indexed</span></span>             | <span data-ttu-id="4caa4-189">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-189">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4caa4-190">In Global Catalog</span></span>      | <span data-ttu-id="4caa4-191">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-191">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4caa4-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="4caa4-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4caa4-193">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="4caa4-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4caa4-194">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4caa4-195">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-196">Search-Flags</span></span>           | <span data-ttu-id="4caa4-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4caa4-197">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="4caa4-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-198">System-Flags</span></span>           | <span data-ttu-id="4caa4-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4caa4-199">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="4caa4-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4caa4-200">Classes used in</span></span>        | [<span data-ttu-id="4caa4-201">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="4caa4-201">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="4caa4-202">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="4caa4-202">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4caa4-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4caa4-203">Windows Server 2008</span></span>



| <span data-ttu-id="4caa4-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="4caa4-204">Entry</span></span> | <span data-ttu-id="4caa4-205">Value</span><span class="sxs-lookup"><span data-stu-id="4caa4-205">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caa4-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4caa4-206">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4caa4-207">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="4caa4-208">System-Only</span></span>            | <span data-ttu-id="4caa4-209">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-209">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4caa4-210">Is-Single-Valued</span></span>       | <span data-ttu-id="4caa4-211">True</span><span class="sxs-lookup"><span data-stu-id="4caa4-211">True</span></span>                                                                                                     |
| <span data-ttu-id="4caa4-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4caa4-212">Is Indexed</span></span>             | <span data-ttu-id="4caa4-213">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-213">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4caa4-214">In Global Catalog</span></span>      | <span data-ttu-id="4caa4-215">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-215">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4caa4-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="4caa4-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4caa4-217">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="4caa4-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4caa4-218">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4caa4-219">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-220">Search-Flags</span></span>           | <span data-ttu-id="4caa4-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4caa4-221">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="4caa4-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-222">System-Flags</span></span>           | <span data-ttu-id="4caa4-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4caa4-223">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="4caa4-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4caa4-224">Classes used in</span></span>        | [<span data-ttu-id="4caa4-225">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="4caa4-225">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="4caa4-226">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="4caa4-226">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4caa4-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4caa4-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4caa4-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="4caa4-228">Entry</span></span> | <span data-ttu-id="4caa4-229">Value</span><span class="sxs-lookup"><span data-stu-id="4caa4-229">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caa4-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4caa4-230">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4caa4-231">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="4caa4-232">System-Only</span></span>            | <span data-ttu-id="4caa4-233">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-233">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4caa4-234">Is-Single-Valued</span></span>       | <span data-ttu-id="4caa4-235">True</span><span class="sxs-lookup"><span data-stu-id="4caa4-235">True</span></span>                                                                                                     |
| <span data-ttu-id="4caa4-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4caa4-236">Is Indexed</span></span>             | <span data-ttu-id="4caa4-237">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-237">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4caa4-238">In Global Catalog</span></span>      | <span data-ttu-id="4caa4-239">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-239">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4caa4-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="4caa4-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4caa4-241">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="4caa4-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4caa4-242">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4caa4-243">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-244">Search-Flags</span></span>           | <span data-ttu-id="4caa4-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4caa4-245">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="4caa4-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-246">System-Flags</span></span>           | <span data-ttu-id="4caa4-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4caa4-247">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="4caa4-248">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4caa4-248">Classes used in</span></span>        | [<span data-ttu-id="4caa4-249">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="4caa4-249">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="4caa4-250">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="4caa4-250">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4caa4-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4caa4-251">Windows Server 2012</span></span>



| <span data-ttu-id="4caa4-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="4caa4-252">Entry</span></span> | <span data-ttu-id="4caa4-253">Value</span><span class="sxs-lookup"><span data-stu-id="4caa4-253">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caa4-254">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4caa4-254">Link-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4caa4-255">MAPI-Id</span></span>                | \-                                                                                                       |
| <span data-ttu-id="4caa4-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="4caa4-256">System-Only</span></span>            | <span data-ttu-id="4caa4-257">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-257">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-258">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4caa4-258">Is-Single-Valued</span></span>       | <span data-ttu-id="4caa4-259">True</span><span class="sxs-lookup"><span data-stu-id="4caa4-259">True</span></span>                                                                                                     |
| <span data-ttu-id="4caa4-260">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4caa4-260">Is Indexed</span></span>             | <span data-ttu-id="4caa4-261">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-261">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-262">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4caa4-262">In Global Catalog</span></span>      | <span data-ttu-id="4caa4-263">False</span><span class="sxs-lookup"><span data-stu-id="4caa4-263">False</span></span>                                                                                                    |
| <span data-ttu-id="4caa4-264">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4caa4-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="4caa4-265">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4caa4-265">O:BAG:BAD:S:</span></span>                                                                                             |
| <span data-ttu-id="4caa4-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4caa4-266">Range-Lower</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4caa4-267">Range-Upper</span></span>            | \-                                                                                                       |
| <span data-ttu-id="4caa4-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-268">Search-Flags</span></span>           | <span data-ttu-id="4caa4-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4caa4-269">0x00000000</span></span>                                                                                               |
| <span data-ttu-id="4caa4-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4caa4-270">System-Flags</span></span>           | <span data-ttu-id="4caa4-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4caa4-271">0x00000010</span></span>                                                                                               |
| <span data-ttu-id="4caa4-272">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4caa4-272">Classes used in</span></span>        | [<span data-ttu-id="4caa4-273">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="4caa4-273">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="4caa4-274">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="4caa4-274">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 






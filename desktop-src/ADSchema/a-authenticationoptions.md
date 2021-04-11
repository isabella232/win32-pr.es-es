---
title: Authentication-Options atributo)
description: Opciones de autenticación usadas en ADSI para enlazar a los objetos de servicios de directorio.
ms.assetid: a6dc4591-d825-456a-8f77-78cb3c91af9f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Authentication-Options
- authenticationOptions esquema de AD de atributos
topic_type:
- apiref
api_name:
- Authentication-Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa9c422dfe196ab002c02c361759461f43965d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151490"
---
# <a name="authentication-options-attribute"></a><span data-ttu-id="a5168-105">Authentication-Options atributo)</span><span class="sxs-lookup"><span data-stu-id="a5168-105">Authentication-Options attribute</span></span>

<span data-ttu-id="a5168-106">Opciones de autenticación usadas en ADSI para enlazar a los objetos de servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="a5168-106">The authentication options used in ADSI to bind to directory services objects.</span></span>



| <span data-ttu-id="a5168-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5168-107">Entry</span></span> | <span data-ttu-id="a5168-108">Value</span><span class="sxs-lookup"><span data-stu-id="a5168-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5168-109">CN</span><span class="sxs-lookup"><span data-stu-id="a5168-109">CN</span></span>                | <span data-ttu-id="a5168-110">Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="a5168-110">Authentication-Options</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a5168-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a5168-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a5168-112">authenticationOptions</span><span class="sxs-lookup"><span data-stu-id="a5168-112">authenticationOptions</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a5168-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a5168-113">Size</span></span>              | <span data-ttu-id="a5168-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="a5168-114">4 bytes.</span></span> <span data-ttu-id="a5168-115">Valores definidos en IADS. h: \_ autenticación segura de ADS \_ 0X1, ADS \_ usar \_ cifrado 0X2, ADS \_ usar \_ SSL 0X2, ADS \_ ReadOnly \_ Server 0x4, ADS \_ prompt \_ CREDENTIALS 0x8, ADS \_ sin \_ autenticación 0x10, ADS \_ Fast \_ BIND 0x20, ADS \_ usar \_ firma 0x40, ADS \_ usar el \_ sellado 0x80</span><span class="sxs-lookup"><span data-stu-id="a5168-115">Values defined in IADS.h: ADS\_SECURE\_AUTHENTICATION 0x1, ADS\_USE\_ENCRYPTION 0x2, ADS\_USE\_SSL 0x2, ADS\_READONLY\_SERVER 0x4, ADS\_PROMPT\_CREDENTIALS 0x8, ADS\_NO\_AUTHENTICATION 0x10, ADS\_FAST\_BIND 0x20, ADS\_USE\_SIGNING 0x40, ADS\_USE\_SEALING 0x80</span></span> |
| <span data-ttu-id="a5168-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a5168-116">Update Privilege</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a5168-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a5168-117">Update Frequency</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a5168-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a5168-118">Attribute-Id</span></span>      | <span data-ttu-id="a5168-119">1.2.840.113556.1.4.11</span><span class="sxs-lookup"><span data-stu-id="a5168-119">1.2.840.113556.1.4.11</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a5168-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a5168-120">System-Id-Guid</span></span>    | <span data-ttu-id="a5168-121">bf967928-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a5168-121">bf967928-0de6-11d0-a285-00aa003049e2</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="a5168-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5168-122">Syntax</span></span>            | [<span data-ttu-id="a5168-123">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="a5168-123">**Enumeration**</span></span>](s-enumeration.md)                                                                                                                                                                                                                                         |



## <a name="implementations"></a><span data-ttu-id="a5168-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a5168-124">Implementations</span></span>

-   [<span data-ttu-id="a5168-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a5168-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a5168-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a5168-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a5168-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a5168-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a5168-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a5168-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a5168-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a5168-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a5168-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a5168-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a5168-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5168-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a5168-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5168-132">Entry</span></span> | <span data-ttu-id="a5168-133">Value</span><span class="sxs-lookup"><span data-stu-id="a5168-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5168-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a5168-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5168-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5168-136">System-Only</span></span>            | <span data-ttu-id="a5168-137">False</span><span class="sxs-lookup"><span data-stu-id="a5168-137">False</span></span>                                              |
| <span data-ttu-id="a5168-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a5168-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a5168-139">True</span><span class="sxs-lookup"><span data-stu-id="a5168-139">True</span></span>                                               |
| <span data-ttu-id="a5168-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a5168-140">Is Indexed</span></span>             | <span data-ttu-id="a5168-141">False</span><span class="sxs-lookup"><span data-stu-id="a5168-141">False</span></span>                                              |
| <span data-ttu-id="a5168-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5168-142">In Global Catalog</span></span>      | <span data-ttu-id="a5168-143">False</span><span class="sxs-lookup"><span data-stu-id="a5168-143">False</span></span>                                              |
| <span data-ttu-id="a5168-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a5168-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5168-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5168-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5168-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5168-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5168-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-148">Search-Flags</span></span>           | <span data-ttu-id="a5168-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5168-149">0x00000000</span></span>                                         |
| <span data-ttu-id="a5168-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-150">System-Flags</span></span>           | <span data-ttu-id="a5168-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5168-151">0x00000010</span></span>                                         |
| <span data-ttu-id="a5168-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a5168-152">Classes used in</span></span>        | [<span data-ttu-id="a5168-153">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="a5168-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a5168-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a5168-154">Windows Server 2003</span></span>



| <span data-ttu-id="a5168-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5168-155">Entry</span></span> | <span data-ttu-id="a5168-156">Value</span><span class="sxs-lookup"><span data-stu-id="a5168-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5168-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a5168-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5168-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5168-159">System-Only</span></span>            | <span data-ttu-id="a5168-160">False</span><span class="sxs-lookup"><span data-stu-id="a5168-160">False</span></span>                                              |
| <span data-ttu-id="a5168-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a5168-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a5168-162">True</span><span class="sxs-lookup"><span data-stu-id="a5168-162">True</span></span>                                               |
| <span data-ttu-id="a5168-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a5168-163">Is Indexed</span></span>             | <span data-ttu-id="a5168-164">False</span><span class="sxs-lookup"><span data-stu-id="a5168-164">False</span></span>                                              |
| <span data-ttu-id="a5168-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5168-165">In Global Catalog</span></span>      | <span data-ttu-id="a5168-166">False</span><span class="sxs-lookup"><span data-stu-id="a5168-166">False</span></span>                                              |
| <span data-ttu-id="a5168-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a5168-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5168-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5168-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5168-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5168-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5168-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-171">Search-Flags</span></span>           | <span data-ttu-id="a5168-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5168-172">0x00000000</span></span>                                         |
| <span data-ttu-id="a5168-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-173">System-Flags</span></span>           | <span data-ttu-id="a5168-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5168-174">0x00000010</span></span>                                         |
| <span data-ttu-id="a5168-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a5168-175">Classes used in</span></span>        | [<span data-ttu-id="a5168-176">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="a5168-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a5168-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a5168-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a5168-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5168-178">Entry</span></span> | <span data-ttu-id="a5168-179">Value</span><span class="sxs-lookup"><span data-stu-id="a5168-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5168-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a5168-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5168-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5168-182">System-Only</span></span>            | <span data-ttu-id="a5168-183">False</span><span class="sxs-lookup"><span data-stu-id="a5168-183">False</span></span>                                              |
| <span data-ttu-id="a5168-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a5168-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a5168-185">True</span><span class="sxs-lookup"><span data-stu-id="a5168-185">True</span></span>                                               |
| <span data-ttu-id="a5168-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a5168-186">Is Indexed</span></span>             | <span data-ttu-id="a5168-187">False</span><span class="sxs-lookup"><span data-stu-id="a5168-187">False</span></span>                                              |
| <span data-ttu-id="a5168-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5168-188">In Global Catalog</span></span>      | <span data-ttu-id="a5168-189">False</span><span class="sxs-lookup"><span data-stu-id="a5168-189">False</span></span>                                              |
| <span data-ttu-id="a5168-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a5168-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5168-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5168-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5168-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5168-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5168-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-194">Search-Flags</span></span>           | <span data-ttu-id="a5168-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5168-195">0x00000000</span></span>                                         |
| <span data-ttu-id="a5168-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-196">System-Flags</span></span>           | <span data-ttu-id="a5168-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5168-197">0x00000010</span></span>                                         |
| <span data-ttu-id="a5168-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a5168-198">Classes used in</span></span>        | [<span data-ttu-id="a5168-199">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="a5168-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a5168-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5168-200">Windows Server 2008</span></span>



| <span data-ttu-id="a5168-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5168-201">Entry</span></span> | <span data-ttu-id="a5168-202">Value</span><span class="sxs-lookup"><span data-stu-id="a5168-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5168-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a5168-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5168-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5168-205">System-Only</span></span>            | <span data-ttu-id="a5168-206">False</span><span class="sxs-lookup"><span data-stu-id="a5168-206">False</span></span>                                              |
| <span data-ttu-id="a5168-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a5168-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a5168-208">True</span><span class="sxs-lookup"><span data-stu-id="a5168-208">True</span></span>                                               |
| <span data-ttu-id="a5168-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a5168-209">Is Indexed</span></span>             | <span data-ttu-id="a5168-210">False</span><span class="sxs-lookup"><span data-stu-id="a5168-210">False</span></span>                                              |
| <span data-ttu-id="a5168-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5168-211">In Global Catalog</span></span>      | <span data-ttu-id="a5168-212">False</span><span class="sxs-lookup"><span data-stu-id="a5168-212">False</span></span>                                              |
| <span data-ttu-id="a5168-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a5168-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5168-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5168-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5168-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5168-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5168-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-217">Search-Flags</span></span>           | <span data-ttu-id="a5168-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5168-218">0x00000000</span></span>                                         |
| <span data-ttu-id="a5168-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-219">System-Flags</span></span>           | <span data-ttu-id="a5168-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5168-220">0x00000010</span></span>                                         |
| <span data-ttu-id="a5168-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a5168-221">Classes used in</span></span>        | [<span data-ttu-id="a5168-222">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="a5168-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a5168-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5168-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a5168-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5168-224">Entry</span></span> | <span data-ttu-id="a5168-225">Value</span><span class="sxs-lookup"><span data-stu-id="a5168-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5168-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a5168-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5168-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5168-228">System-Only</span></span>            | <span data-ttu-id="a5168-229">False</span><span class="sxs-lookup"><span data-stu-id="a5168-229">False</span></span>                                              |
| <span data-ttu-id="a5168-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a5168-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a5168-231">True</span><span class="sxs-lookup"><span data-stu-id="a5168-231">True</span></span>                                               |
| <span data-ttu-id="a5168-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a5168-232">Is Indexed</span></span>             | <span data-ttu-id="a5168-233">False</span><span class="sxs-lookup"><span data-stu-id="a5168-233">False</span></span>                                              |
| <span data-ttu-id="a5168-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5168-234">In Global Catalog</span></span>      | <span data-ttu-id="a5168-235">False</span><span class="sxs-lookup"><span data-stu-id="a5168-235">False</span></span>                                              |
| <span data-ttu-id="a5168-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a5168-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5168-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5168-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5168-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5168-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5168-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-240">Search-Flags</span></span>           | <span data-ttu-id="a5168-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5168-241">0x00000000</span></span>                                         |
| <span data-ttu-id="a5168-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-242">System-Flags</span></span>           | <span data-ttu-id="a5168-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5168-243">0x00000010</span></span>                                         |
| <span data-ttu-id="a5168-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a5168-244">Classes used in</span></span>        | [<span data-ttu-id="a5168-245">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="a5168-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a5168-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a5168-246">Windows Server 2012</span></span>



| <span data-ttu-id="a5168-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5168-247">Entry</span></span> | <span data-ttu-id="a5168-248">Value</span><span class="sxs-lookup"><span data-stu-id="a5168-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="a5168-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a5168-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5168-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="a5168-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5168-251">System-Only</span></span>            | <span data-ttu-id="a5168-252">False</span><span class="sxs-lookup"><span data-stu-id="a5168-252">False</span></span>                                              |
| <span data-ttu-id="a5168-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a5168-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a5168-254">True</span><span class="sxs-lookup"><span data-stu-id="a5168-254">True</span></span>                                               |
| <span data-ttu-id="a5168-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a5168-255">Is Indexed</span></span>             | <span data-ttu-id="a5168-256">False</span><span class="sxs-lookup"><span data-stu-id="a5168-256">False</span></span>                                              |
| <span data-ttu-id="a5168-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5168-257">In Global Catalog</span></span>      | <span data-ttu-id="a5168-258">False</span><span class="sxs-lookup"><span data-stu-id="a5168-258">False</span></span>                                              |
| <span data-ttu-id="a5168-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a5168-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5168-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5168-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="a5168-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5168-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5168-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="a5168-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-263">Search-Flags</span></span>           | <span data-ttu-id="a5168-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5168-264">0x00000000</span></span>                                         |
| <span data-ttu-id="a5168-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5168-265">System-Flags</span></span>           | <span data-ttu-id="a5168-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5168-266">0x00000010</span></span>                                         |
| <span data-ttu-id="a5168-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a5168-267">Classes used in</span></span>        | [<span data-ttu-id="a5168-268">**Directiva de dominio**</span><span class="sxs-lookup"><span data-stu-id="a5168-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 






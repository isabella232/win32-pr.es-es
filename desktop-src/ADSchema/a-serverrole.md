---
title: Server-Role atributo)
description: Por compatibilidad con servidores anteriores a Windows 2000 Server. Un equipo que ejecuta Windows NT Server puede ser un servidor independiente, un controlador de dominio principal (PDC) o un controlador de dominio de copia de seguridad (BDC).
ms.assetid: 0c2e5b18-14ad-4f77-a62c-eeb95aabbb99
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Server-Role
- Esquema de AD de atributo de la función de función
topic_type:
- apiref
api_name:
- Server-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a127a94cd1ecc2bfce3701c11ee2a5e0c2376c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658975"
---
# <a name="server-role-attribute"></a><span data-ttu-id="b8a2e-106">Server-Role atributo)</span><span class="sxs-lookup"><span data-stu-id="b8a2e-106">Server-Role attribute</span></span>

<span data-ttu-id="b8a2e-107">Por compatibilidad con servidores anteriores a Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-107">For compatibility with pre-Windows 2000 Server servers.</span></span> <span data-ttu-id="b8a2e-108">Un equipo que ejecuta Windows NT Server puede ser un servidor independiente, un controlador de dominio principal (PDC) o un controlador de dominio de copia de seguridad (BDC).</span><span class="sxs-lookup"><span data-stu-id="b8a2e-108">A computer running Windows NT Server can be a standalone server, a primary domain controller (PDC), or a backup domain controller (BDC).</span></span>



| <span data-ttu-id="b8a2e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8a2e-109">Entry</span></span> | <span data-ttu-id="b8a2e-110">Value</span><span class="sxs-lookup"><span data-stu-id="b8a2e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b8a2e-111">CN</span><span class="sxs-lookup"><span data-stu-id="b8a2e-111">CN</span></span>                | <span data-ttu-id="b8a2e-112">Server-Role</span><span class="sxs-lookup"><span data-stu-id="b8a2e-112">Server-Role</span></span>                          |
| <span data-ttu-id="b8a2e-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b8a2e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b8a2e-114">serverRole</span><span class="sxs-lookup"><span data-stu-id="b8a2e-114">serverRole</span></span>                           |
| <span data-ttu-id="b8a2e-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b8a2e-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="b8a2e-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b8a2e-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b8a2e-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b8a2e-117">Update Frequency</span></span>  | <span data-ttu-id="b8a2e-118">4 bytes</span><span class="sxs-lookup"><span data-stu-id="b8a2e-118">4 bytes</span></span>                              |
| <span data-ttu-id="b8a2e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8a2e-119">Attribute-Id</span></span>      | <span data-ttu-id="b8a2e-120">1.2.840.113556.1.4.157</span><span class="sxs-lookup"><span data-stu-id="b8a2e-120">1.2.840.113556.1.4.157</span></span>               |
| <span data-ttu-id="b8a2e-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b8a2e-121">System-Id-Guid</span></span>    | <span data-ttu-id="b8a2e-122">bf967a33-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b8a2e-122">bf967a33-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="b8a2e-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8a2e-123">Syntax</span></span>            | [<span data-ttu-id="b8a2e-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b8a2e-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b8a2e-125">Implementations</span></span>

-   [<span data-ttu-id="b8a2e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8a2e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8a2e-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8a2e-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8a2e-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8a2e-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8a2e-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8a2e-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b8a2e-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8a2e-133">Entry</span></span> | <span data-ttu-id="b8a2e-134">Value</span><span class="sxs-lookup"><span data-stu-id="b8a2e-134">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b8a2e-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b8a2e-135">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8a2e-136">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8a2e-137">System-Only</span></span>            | <span data-ttu-id="b8a2e-138">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-138">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b8a2e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b8a2e-140">True</span><span class="sxs-lookup"><span data-stu-id="b8a2e-140">True</span></span>                                                  |
| <span data-ttu-id="b8a2e-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b8a2e-141">Is Indexed</span></span>             | <span data-ttu-id="b8a2e-142">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-142">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8a2e-143">In Global Catalog</span></span>      | <span data-ttu-id="b8a2e-144">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-144">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b8a2e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8a2e-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8a2e-146">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b8a2e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8a2e-147">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8a2e-148">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-149">Search-Flags</span></span>           | <span data-ttu-id="b8a2e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8a2e-150">0x00000000</span></span>                                            |
| <span data-ttu-id="b8a2e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-151">System-Flags</span></span>           | <span data-ttu-id="b8a2e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8a2e-152">0x00000010</span></span>                                            |
| <span data-ttu-id="b8a2e-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b8a2e-153">Classes used in</span></span>        | [<span data-ttu-id="b8a2e-154">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-154">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8a2e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8a2e-155">Windows Server 2003</span></span>



| <span data-ttu-id="b8a2e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8a2e-156">Entry</span></span> | <span data-ttu-id="b8a2e-157">Value</span><span class="sxs-lookup"><span data-stu-id="b8a2e-157">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b8a2e-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b8a2e-158">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8a2e-159">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8a2e-160">System-Only</span></span>            | <span data-ttu-id="b8a2e-161">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-161">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b8a2e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b8a2e-163">True</span><span class="sxs-lookup"><span data-stu-id="b8a2e-163">True</span></span>                                                  |
| <span data-ttu-id="b8a2e-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b8a2e-164">Is Indexed</span></span>             | <span data-ttu-id="b8a2e-165">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-165">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8a2e-166">In Global Catalog</span></span>      | <span data-ttu-id="b8a2e-167">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-167">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b8a2e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8a2e-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8a2e-169">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b8a2e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8a2e-170">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8a2e-171">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-172">Search-Flags</span></span>           | <span data-ttu-id="b8a2e-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8a2e-173">0x00000000</span></span>                                            |
| <span data-ttu-id="b8a2e-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-174">System-Flags</span></span>           | <span data-ttu-id="b8a2e-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8a2e-175">0x00000010</span></span>                                            |
| <span data-ttu-id="b8a2e-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b8a2e-176">Classes used in</span></span>        | [<span data-ttu-id="b8a2e-177">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-177">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8a2e-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8a2e-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8a2e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8a2e-179">Entry</span></span> | <span data-ttu-id="b8a2e-180">Value</span><span class="sxs-lookup"><span data-stu-id="b8a2e-180">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b8a2e-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b8a2e-181">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8a2e-182">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8a2e-183">System-Only</span></span>            | <span data-ttu-id="b8a2e-184">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-184">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b8a2e-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b8a2e-186">True</span><span class="sxs-lookup"><span data-stu-id="b8a2e-186">True</span></span>                                                  |
| <span data-ttu-id="b8a2e-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b8a2e-187">Is Indexed</span></span>             | <span data-ttu-id="b8a2e-188">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-188">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8a2e-189">In Global Catalog</span></span>      | <span data-ttu-id="b8a2e-190">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-190">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b8a2e-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8a2e-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8a2e-192">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b8a2e-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8a2e-193">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8a2e-194">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-195">Search-Flags</span></span>           | <span data-ttu-id="b8a2e-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8a2e-196">0x00000000</span></span>                                            |
| <span data-ttu-id="b8a2e-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-197">System-Flags</span></span>           | <span data-ttu-id="b8a2e-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8a2e-198">0x00000010</span></span>                                            |
| <span data-ttu-id="b8a2e-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b8a2e-199">Classes used in</span></span>        | [<span data-ttu-id="b8a2e-200">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-200">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8a2e-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8a2e-201">Windows Server 2008</span></span>



| <span data-ttu-id="b8a2e-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8a2e-202">Entry</span></span> | <span data-ttu-id="b8a2e-203">Value</span><span class="sxs-lookup"><span data-stu-id="b8a2e-203">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b8a2e-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b8a2e-204">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8a2e-205">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8a2e-206">System-Only</span></span>            | <span data-ttu-id="b8a2e-207">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-207">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b8a2e-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b8a2e-209">True</span><span class="sxs-lookup"><span data-stu-id="b8a2e-209">True</span></span>                                                  |
| <span data-ttu-id="b8a2e-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b8a2e-210">Is Indexed</span></span>             | <span data-ttu-id="b8a2e-211">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-211">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8a2e-212">In Global Catalog</span></span>      | <span data-ttu-id="b8a2e-213">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-213">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b8a2e-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8a2e-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8a2e-215">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b8a2e-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8a2e-216">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8a2e-217">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-218">Search-Flags</span></span>           | <span data-ttu-id="b8a2e-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8a2e-219">0x00000000</span></span>                                            |
| <span data-ttu-id="b8a2e-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-220">System-Flags</span></span>           | <span data-ttu-id="b8a2e-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8a2e-221">0x00000010</span></span>                                            |
| <span data-ttu-id="b8a2e-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b8a2e-222">Classes used in</span></span>        | [<span data-ttu-id="b8a2e-223">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-223">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8a2e-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8a2e-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8a2e-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8a2e-225">Entry</span></span> | <span data-ttu-id="b8a2e-226">Value</span><span class="sxs-lookup"><span data-stu-id="b8a2e-226">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b8a2e-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b8a2e-227">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8a2e-228">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8a2e-229">System-Only</span></span>            | <span data-ttu-id="b8a2e-230">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-230">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b8a2e-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b8a2e-232">True</span><span class="sxs-lookup"><span data-stu-id="b8a2e-232">True</span></span>                                                  |
| <span data-ttu-id="b8a2e-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b8a2e-233">Is Indexed</span></span>             | <span data-ttu-id="b8a2e-234">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-234">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8a2e-235">In Global Catalog</span></span>      | <span data-ttu-id="b8a2e-236">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-236">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b8a2e-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8a2e-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8a2e-238">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b8a2e-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8a2e-239">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8a2e-240">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-241">Search-Flags</span></span>           | <span data-ttu-id="b8a2e-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8a2e-242">0x00000000</span></span>                                            |
| <span data-ttu-id="b8a2e-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-243">System-Flags</span></span>           | <span data-ttu-id="b8a2e-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8a2e-244">0x00000010</span></span>                                            |
| <span data-ttu-id="b8a2e-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b8a2e-245">Classes used in</span></span>        | [<span data-ttu-id="b8a2e-246">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-246">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8a2e-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8a2e-247">Windows Server 2012</span></span>



| <span data-ttu-id="b8a2e-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8a2e-248">Entry</span></span> | <span data-ttu-id="b8a2e-249">Value</span><span class="sxs-lookup"><span data-stu-id="b8a2e-249">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b8a2e-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b8a2e-250">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8a2e-251">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="b8a2e-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8a2e-252">System-Only</span></span>            | <span data-ttu-id="b8a2e-253">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-253">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b8a2e-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b8a2e-255">True</span><span class="sxs-lookup"><span data-stu-id="b8a2e-255">True</span></span>                                                  |
| <span data-ttu-id="b8a2e-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b8a2e-256">Is Indexed</span></span>             | <span data-ttu-id="b8a2e-257">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-257">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b8a2e-258">In Global Catalog</span></span>      | <span data-ttu-id="b8a2e-259">False</span><span class="sxs-lookup"><span data-stu-id="b8a2e-259">False</span></span>                                                 |
| <span data-ttu-id="b8a2e-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b8a2e-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8a2e-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8a2e-261">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="b8a2e-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8a2e-262">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8a2e-263">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="b8a2e-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-264">Search-Flags</span></span>           | <span data-ttu-id="b8a2e-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8a2e-265">0x00000000</span></span>                                            |
| <span data-ttu-id="b8a2e-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8a2e-266">System-Flags</span></span>           | <span data-ttu-id="b8a2e-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b8a2e-267">0x00000010</span></span>                                            |
| <span data-ttu-id="b8a2e-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b8a2e-268">Classes used in</span></span>        | [<span data-ttu-id="b8a2e-269">**Sam-dominio-base**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-269">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 






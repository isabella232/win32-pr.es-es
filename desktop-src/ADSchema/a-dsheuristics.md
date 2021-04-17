---
title: DS-Heuristics atributo)
description: Contiene la configuración global para todo el bosque.
ms.assetid: d5fd990b-7bbf-4ede-a3af-7f3f7ac959b3
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de DS-Heuristics
- atributo Fdisableautoindexingonschemaupdate de AD Schema
topic_type:
- apiref
api_name:
- DS-Heuristics
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65922b580975ec05877ae33d213ff3a3675ec72f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658548"
---
# <a name="ds-heuristics-attribute"></a><span data-ttu-id="ce36c-105">DS-Heuristics atributo)</span><span class="sxs-lookup"><span data-stu-id="ce36c-105">DS-Heuristics attribute</span></span>

<span data-ttu-id="ce36c-106">Contiene la configuración global para todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="ce36c-106">Contains global settings for the entire forest.</span></span>

<span data-ttu-id="ce36c-107">Hay información sobre los bits de exclusión de adminSDholder disponible en el sitio web de ayuda y soporte técnico de Microsoft en un número de artículo [817433, los permisos delegados no están disponibles y la herencia se deshabilita automáticamente](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span><span class="sxs-lookup"><span data-stu-id="ce36c-107">There is information about adminSDholder exclusion bits available on the Microsoft Help and Support website in an article number [817433, Delegated permissions are not available and inheritance is automatically disabled](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span></span>



| <span data-ttu-id="ce36c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce36c-108">Entry</span></span> | <span data-ttu-id="ce36c-109">Value</span><span class="sxs-lookup"><span data-stu-id="ce36c-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ce36c-110">CN</span><span class="sxs-lookup"><span data-stu-id="ce36c-110">CN</span></span>                | <span data-ttu-id="ce36c-111">DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="ce36c-111">DS-Heuristics</span></span>                               |
| <span data-ttu-id="ce36c-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="ce36c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ce36c-113">dSHeuristics</span><span class="sxs-lookup"><span data-stu-id="ce36c-113">dSHeuristics</span></span>                                |
| <span data-ttu-id="ce36c-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ce36c-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="ce36c-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="ce36c-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ce36c-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="ce36c-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ce36c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ce36c-117">Attribute-Id</span></span>      | <span data-ttu-id="ce36c-118">1.2.840.113556.1.2.212</span><span class="sxs-lookup"><span data-stu-id="ce36c-118">1.2.840.113556.1.2.212</span></span>                      |
| <span data-ttu-id="ce36c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ce36c-119">System-Id-Guid</span></span>    | <span data-ttu-id="ce36c-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="ce36c-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="ce36c-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce36c-121">Syntax</span></span>            | [<span data-ttu-id="ce36c-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ce36c-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ce36c-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ce36c-123">Implementations</span></span>

-   [<span data-ttu-id="ce36c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ce36c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ce36c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ce36c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ce36c-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="ce36c-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="ce36c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ce36c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ce36c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ce36c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ce36c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ce36c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ce36c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ce36c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ce36c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce36c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ce36c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce36c-132">Entry</span></span> | <span data-ttu-id="ce36c-133">Value</span><span class="sxs-lookup"><span data-stu-id="ce36c-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ce36c-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ce36c-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce36c-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce36c-136">System-Only</span></span>            | <span data-ttu-id="ce36c-137">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-137">False</span></span>                                            |
| <span data-ttu-id="ce36c-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ce36c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ce36c-139">True</span><span class="sxs-lookup"><span data-stu-id="ce36c-139">True</span></span>                                             |
| <span data-ttu-id="ce36c-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ce36c-140">Is Indexed</span></span>             | <span data-ttu-id="ce36c-141">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-141">False</span></span>                                            |
| <span data-ttu-id="ce36c-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ce36c-142">In Global Catalog</span></span>      | <span data-ttu-id="ce36c-143">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-143">False</span></span>                                            |
| <span data-ttu-id="ce36c-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ce36c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce36c-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce36c-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ce36c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce36c-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce36c-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-148">Search-Flags</span></span>           | <span data-ttu-id="ce36c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce36c-149">0x00000000</span></span>                                       |
| <span data-ttu-id="ce36c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-150">System-Flags</span></span>           | <span data-ttu-id="ce36c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce36c-151">0x00000010</span></span>                                       |
| <span data-ttu-id="ce36c-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ce36c-152">Classes used in</span></span>        | [<span data-ttu-id="ce36c-153">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="ce36c-153">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ce36c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce36c-154">Windows Server 2003</span></span>



| <span data-ttu-id="ce36c-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce36c-155">Entry</span></span> | <span data-ttu-id="ce36c-156">Value</span><span class="sxs-lookup"><span data-stu-id="ce36c-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ce36c-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ce36c-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce36c-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce36c-159">System-Only</span></span>            | <span data-ttu-id="ce36c-160">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-160">False</span></span>                                            |
| <span data-ttu-id="ce36c-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ce36c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ce36c-162">True</span><span class="sxs-lookup"><span data-stu-id="ce36c-162">True</span></span>                                             |
| <span data-ttu-id="ce36c-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ce36c-163">Is Indexed</span></span>             | <span data-ttu-id="ce36c-164">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-164">False</span></span>                                            |
| <span data-ttu-id="ce36c-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ce36c-165">In Global Catalog</span></span>      | <span data-ttu-id="ce36c-166">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-166">False</span></span>                                            |
| <span data-ttu-id="ce36c-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ce36c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce36c-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce36c-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ce36c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce36c-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce36c-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-171">Search-Flags</span></span>           | <span data-ttu-id="ce36c-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce36c-172">0x00000000</span></span>                                       |
| <span data-ttu-id="ce36c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-173">System-Flags</span></span>           | <span data-ttu-id="ce36c-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce36c-174">0x00000010</span></span>                                       |
| <span data-ttu-id="ce36c-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ce36c-175">Classes used in</span></span>        | [<span data-ttu-id="ce36c-176">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="ce36c-176">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="ce36c-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="ce36c-177">ADAM</span></span>



| <span data-ttu-id="ce36c-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce36c-178">Entry</span></span> | <span data-ttu-id="ce36c-179">Value</span><span class="sxs-lookup"><span data-stu-id="ce36c-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ce36c-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ce36c-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce36c-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce36c-182">System-Only</span></span>            | <span data-ttu-id="ce36c-183">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-183">False</span></span>                                            |
| <span data-ttu-id="ce36c-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ce36c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ce36c-185">True</span><span class="sxs-lookup"><span data-stu-id="ce36c-185">True</span></span>                                             |
| <span data-ttu-id="ce36c-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ce36c-186">Is Indexed</span></span>             | <span data-ttu-id="ce36c-187">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-187">False</span></span>                                            |
| <span data-ttu-id="ce36c-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ce36c-188">In Global Catalog</span></span>      | <span data-ttu-id="ce36c-189">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-189">False</span></span>                                            |
| <span data-ttu-id="ce36c-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ce36c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce36c-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce36c-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ce36c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce36c-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce36c-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-194">Search-Flags</span></span>           | <span data-ttu-id="ce36c-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce36c-195">0x00000000</span></span>                                       |
| <span data-ttu-id="ce36c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-196">System-Flags</span></span>           | <span data-ttu-id="ce36c-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce36c-197">0x00000010</span></span>                                       |
| <span data-ttu-id="ce36c-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ce36c-198">Classes used in</span></span>        | [<span data-ttu-id="ce36c-199">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="ce36c-199">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ce36c-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ce36c-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ce36c-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce36c-201">Entry</span></span> | <span data-ttu-id="ce36c-202">Value</span><span class="sxs-lookup"><span data-stu-id="ce36c-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ce36c-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ce36c-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce36c-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce36c-205">System-Only</span></span>            | <span data-ttu-id="ce36c-206">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-206">False</span></span>                                            |
| <span data-ttu-id="ce36c-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ce36c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ce36c-208">True</span><span class="sxs-lookup"><span data-stu-id="ce36c-208">True</span></span>                                             |
| <span data-ttu-id="ce36c-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ce36c-209">Is Indexed</span></span>             | <span data-ttu-id="ce36c-210">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-210">False</span></span>                                            |
| <span data-ttu-id="ce36c-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ce36c-211">In Global Catalog</span></span>      | <span data-ttu-id="ce36c-212">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-212">False</span></span>                                            |
| <span data-ttu-id="ce36c-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ce36c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce36c-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce36c-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ce36c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce36c-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce36c-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-217">Search-Flags</span></span>           | <span data-ttu-id="ce36c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce36c-218">0x00000000</span></span>                                       |
| <span data-ttu-id="ce36c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-219">System-Flags</span></span>           | <span data-ttu-id="ce36c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce36c-220">0x00000010</span></span>                                       |
| <span data-ttu-id="ce36c-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ce36c-221">Classes used in</span></span>        | [<span data-ttu-id="ce36c-222">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="ce36c-222">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ce36c-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce36c-223">Windows Server 2008</span></span>



| <span data-ttu-id="ce36c-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce36c-224">Entry</span></span> | <span data-ttu-id="ce36c-225">Value</span><span class="sxs-lookup"><span data-stu-id="ce36c-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ce36c-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ce36c-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce36c-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce36c-228">System-Only</span></span>            | <span data-ttu-id="ce36c-229">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-229">False</span></span>                                            |
| <span data-ttu-id="ce36c-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ce36c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ce36c-231">True</span><span class="sxs-lookup"><span data-stu-id="ce36c-231">True</span></span>                                             |
| <span data-ttu-id="ce36c-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ce36c-232">Is Indexed</span></span>             | <span data-ttu-id="ce36c-233">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-233">False</span></span>                                            |
| <span data-ttu-id="ce36c-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ce36c-234">In Global Catalog</span></span>      | <span data-ttu-id="ce36c-235">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-235">False</span></span>                                            |
| <span data-ttu-id="ce36c-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ce36c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce36c-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce36c-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ce36c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce36c-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce36c-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-240">Search-Flags</span></span>           | <span data-ttu-id="ce36c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce36c-241">0x00000000</span></span>                                       |
| <span data-ttu-id="ce36c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-242">System-Flags</span></span>           | <span data-ttu-id="ce36c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce36c-243">0x00000010</span></span>                                       |
| <span data-ttu-id="ce36c-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ce36c-244">Classes used in</span></span>        | [<span data-ttu-id="ce36c-245">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="ce36c-245">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ce36c-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce36c-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ce36c-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce36c-247">Entry</span></span> | <span data-ttu-id="ce36c-248">Value</span><span class="sxs-lookup"><span data-stu-id="ce36c-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ce36c-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ce36c-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce36c-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce36c-251">System-Only</span></span>            | <span data-ttu-id="ce36c-252">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-252">False</span></span>                                            |
| <span data-ttu-id="ce36c-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ce36c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ce36c-254">True</span><span class="sxs-lookup"><span data-stu-id="ce36c-254">True</span></span>                                             |
| <span data-ttu-id="ce36c-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ce36c-255">Is Indexed</span></span>             | <span data-ttu-id="ce36c-256">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-256">False</span></span>                                            |
| <span data-ttu-id="ce36c-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ce36c-257">In Global Catalog</span></span>      | <span data-ttu-id="ce36c-258">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-258">False</span></span>                                            |
| <span data-ttu-id="ce36c-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ce36c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce36c-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce36c-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ce36c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce36c-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce36c-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-263">Search-Flags</span></span>           | <span data-ttu-id="ce36c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce36c-264">0x00000000</span></span>                                       |
| <span data-ttu-id="ce36c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-265">System-Flags</span></span>           | <span data-ttu-id="ce36c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce36c-266">0x00000010</span></span>                                       |
| <span data-ttu-id="ce36c-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ce36c-267">Classes used in</span></span>        | [<span data-ttu-id="ce36c-268">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="ce36c-268">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ce36c-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce36c-269">Windows Server 2012</span></span>



| <span data-ttu-id="ce36c-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="ce36c-270">Entry</span></span> | <span data-ttu-id="ce36c-271">Value</span><span class="sxs-lookup"><span data-stu-id="ce36c-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="ce36c-272">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="ce36c-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce36c-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="ce36c-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce36c-274">System-Only</span></span>            | <span data-ttu-id="ce36c-275">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-275">False</span></span>                                            |
| <span data-ttu-id="ce36c-276">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="ce36c-276">Is-Single-Valued</span></span>       | <span data-ttu-id="ce36c-277">True</span><span class="sxs-lookup"><span data-stu-id="ce36c-277">True</span></span>                                             |
| <span data-ttu-id="ce36c-278">Está indexado</span><span class="sxs-lookup"><span data-stu-id="ce36c-278">Is Indexed</span></span>             | <span data-ttu-id="ce36c-279">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-279">False</span></span>                                            |
| <span data-ttu-id="ce36c-280">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="ce36c-280">In Global Catalog</span></span>      | <span data-ttu-id="ce36c-281">False</span><span class="sxs-lookup"><span data-stu-id="ce36c-281">False</span></span>                                            |
| <span data-ttu-id="ce36c-282">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="ce36c-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce36c-283">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ce36c-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="ce36c-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce36c-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce36c-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="ce36c-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-286">Search-Flags</span></span>           | <span data-ttu-id="ce36c-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce36c-287">0x00000000</span></span>                                       |
| <span data-ttu-id="ce36c-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce36c-288">System-Flags</span></span>           | <span data-ttu-id="ce36c-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce36c-289">0x00000010</span></span>                                       |
| <span data-ttu-id="ce36c-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="ce36c-290">Classes used in</span></span>        | [<span data-ttu-id="ce36c-291">**NTDS-servicio**</span><span class="sxs-lookup"><span data-stu-id="ce36c-291">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ce36c-292">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce36c-292">Remarks</span></span>

<span data-ttu-id="ce36c-293">Cada bosque Active Directory contiene un DS-Heuristics atributo que contiene la configuración de todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="ce36c-293">Each Active Directory forest contains a DS-Heuristics attribute that contains settings for the entire forest.</span></span> <span data-ttu-id="ce36c-294">El atributo DS-Heuristics es un atributo del objeto "CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration <Domain> ".</span><span class="sxs-lookup"><span data-stu-id="ce36c-294">The DS-Heuristics attribute is an attribute of the "CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,<Domain>" object.</span></span>

<span data-ttu-id="ce36c-295">DS-Heuristics es una cadena Unicode en la que cada carácter contiene un valor para una única configuración de todo el dominio.</span><span class="sxs-lookup"><span data-stu-id="ce36c-295">DS-Heuristics is a Unicode string in which each character contains a value for a single domain-wide setting.</span></span> <span data-ttu-id="ce36c-296">La cadena de DS-Heuristics toma el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="ce36c-296">The DS-Heuristics string takes the following format.</span></span>

``` syntax
|<1>|<2>|<3>|<4>|<5>|<6>|<7>|<8>|<9>|<10>|<11>|<12>|<13>|<14>|<15>|<16>|<17>|<18>|<19>|<20>|<21>|<22>|<23>|<24>|<25>|
```

<span data-ttu-id="ce36c-297">Para proporcionar la validación de datos, cada décimo carácter se establece en el número de carácter dividido entre diez.</span><span class="sxs-lookup"><span data-stu-id="ce36c-297">To provide data validation, each tenth character is set to the character number divided by ten.</span></span> <span data-ttu-id="ce36c-298">Por ejemplo, el décimo carácter es ' 1 '; el vigésimo carácter es ' 2 ', y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="ce36c-298">For example, the tenth character is '1'; the twentieth character is '2', and so on.</span></span>

<span data-ttu-id="ce36c-299">Se supone que cualquier carácter que no está establecido es un "0".</span><span class="sxs-lookup"><span data-stu-id="ce36c-299">Any character that is not set is assumed to be a '0'.</span></span> <span data-ttu-id="ce36c-300">Si no se establece el atributo DS-Heuristics, se supone que todos los valores son "0".</span><span class="sxs-lookup"><span data-stu-id="ce36c-300">If the DS-Heuristics attribute is not set, all values are assumed to be '0'.</span></span> <span data-ttu-id="ce36c-301">Actualmente se usan 25 caracteres y no es necesario rellenar la cadena para rellenar los 25 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ce36c-301">There are currently 25 characters being used and it is not necessary to pad the string to fill all 25 characters.</span></span> <span data-ttu-id="ce36c-302">Por ejemplo, si el carácter más alto que se usa es 7, la cadena "0000002" es aceptable.</span><span class="sxs-lookup"><span data-stu-id="ce36c-302">For example, if the highest character being used is 7, then the string "0000002" is acceptable.</span></span>

<span data-ttu-id="ce36c-303">Para obtener más información acerca de cada carácter, consulte [dSHeuristics en \[ MS-ADTS \] Active Directory especificación técnica](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span><span class="sxs-lookup"><span data-stu-id="ce36c-303">For details about each character, see [dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span></span>

### <a name="anr-search-filters"></a><span data-ttu-id="ce36c-304">Filtros de búsqueda de ANR</span><span class="sxs-lookup"><span data-stu-id="ce36c-304">ANR Search Filters</span></span>

<span data-ttu-id="ce36c-305">Los caracteres 1, 2 y 4 se usan para modificar el comportamiento de los filtros de búsqueda de ANR.</span><span class="sxs-lookup"><span data-stu-id="ce36c-305">Characters 1, 2, and 4 are used to modify the behavior of ANR search filters.</span></span> <span data-ttu-id="ce36c-306">Si el carácter 1 se establece en "1", la expansión del filtro ANR para incluir el valor de **GivenName**  -   (cuando se encuentra espacio) está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="ce36c-306">If character 1 is set to '1', then the expansion of the ANR filter to include **GivenName** - **Surname** (when space is found) is disabled.</span></span> <span data-ttu-id="ce36c-307">Si el carácter 2 se establece en "1", se deshabilita la expansión del filtro ANR para incluir el **Apellido**  -  **GivenName** .</span><span class="sxs-lookup"><span data-stu-id="ce36c-307">If character 2 is set to '1', the expansion of the ANR filter to include **Surname** - **GivenName** is disabled.</span></span> <span data-ttu-id="ce36c-308">Si hay un espacio incrustado en la cadena de búsqueda, la cadena de búsqueda se dividirá normalmente en dos cadenas que se comparan con los atributos **GivenName** y **apellidos** .</span><span class="sxs-lookup"><span data-stu-id="ce36c-308">If an embedded space is present in the search string, the search string will normally be divided into two strings, which are compared pair-wise against the **GivenName** and **Surname** attributes.</span></span> <span data-ttu-id="ce36c-309">Establecer los caracteres 1 y 2 en ' 1 ' impedirá que se intenten esas coincidencias.</span><span class="sxs-lookup"><span data-stu-id="ce36c-309">Setting characters 1 and 2 to '1' will prevent those matches from being attempted.</span></span> <span data-ttu-id="ce36c-310">Esta coincidencia podría deshabilitarse si el administrador está seguro de que las búsquedas de "Jeff Smith" siempre se proporcionarán como "Jeff Smith" y no "Smith, Jeff".</span><span class="sxs-lookup"><span data-stu-id="ce36c-310">This matching might be disabled if the administrator is confident that searches for "Jeff Smith" would always be provided as "jeff smith" and not "smith, jeff".</span></span> <span data-ttu-id="ce36c-311">Normalmente solo se suprimirían una o la otra coincidencia, de acuerdo con la Convención local.</span><span class="sxs-lookup"><span data-stu-id="ce36c-311">Normally only one or the other match would be suppressed, according to local convention.</span></span>

<span data-ttu-id="ce36c-312">Si el carácter 4 se establece en ' 1 ', Active Directory llevará a cabo la "resolución de alias preferente".</span><span class="sxs-lookup"><span data-stu-id="ce36c-312">If the character 4 is set to '1' then Active Directory will perform "pre-emptive nickname resolution".</span></span> <span data-ttu-id="ce36c-313">Es decir, si la cadena de búsqueda coincide exactamente con el alias de exactamente un objeto en el ámbito de búsqueda, se devuelve un objeto como resultado de la búsqueda y se omite el resto de ANR.</span><span class="sxs-lookup"><span data-stu-id="ce36c-313">That is, if the search string exactly matches the nickname of exactly one object in the search scope, that one object is returned as the result of the search, and the rest of ANR is skipped.</span></span> <span data-ttu-id="ce36c-314">Tenga en cuenta que, mientras que el resto de la búsqueda de ANR está disponible a través de LDAP, la resolución de alias preferente (también conocida como "alias") solo está disponible a través de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce36c-314">Note that while the rest of ANR searching is available through LDAP, pre-emptive nickname resolution (also known as "nickname snap") is available only through MAPI.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce36c-315">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce36c-315">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce36c-316">[dSHeuristics en \[ MS-ADTS \] Active Directory especificación técnica](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span><span class="sxs-lookup"><span data-stu-id="ce36c-316">[dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span></span>
</dt> </dl>

 


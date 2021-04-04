---
title: Display-Name-atributo imprimible
description: Nombre para mostrar imprimible de un objeto.
ms.assetid: e8e5ff25-66dd-4c74-9571-9ec765d6d1af
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de visualización de nombre para mostrar
- displayNamePrintable esquema de AD de atributos
topic_type:
- apiref
api_name:
- Display-Name-Printable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eff05c2279f026e3a94b707b522509b4801ff27
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906243"
---
# <a name="display-name-printable-attribute"></a><span data-ttu-id="d9387-105">Display-Name-atributo imprimible</span><span class="sxs-lookup"><span data-stu-id="d9387-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="d9387-106">Nombre para mostrar imprimible de un objeto.</span><span class="sxs-lookup"><span data-stu-id="d9387-106">The printable display name for an object.</span></span> <span data-ttu-id="d9387-107">El nombre para mostrar que se imprime suele ser la combinación del nombre del usuario, el inicial y el apellido.</span><span class="sxs-lookup"><span data-stu-id="d9387-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="d9387-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9387-108">Entry</span></span> | <span data-ttu-id="d9387-109">Value</span><span class="sxs-lookup"><span data-stu-id="d9387-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="d9387-110">CN</span><span class="sxs-lookup"><span data-stu-id="d9387-110">CN</span></span>                | <span data-ttu-id="d9387-111">Display-Name-printable</span><span class="sxs-lookup"><span data-stu-id="d9387-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="d9387-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d9387-112">Ldap-Display-Name</span></span> | <span data-ttu-id="d9387-113">displayNamePrintable</span><span class="sxs-lookup"><span data-stu-id="d9387-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="d9387-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d9387-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="d9387-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d9387-115">Update Privilege</span></span>  | <span data-ttu-id="d9387-116">Administrador de dominio o propietario de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="d9387-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="d9387-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d9387-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="d9387-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d9387-118">Attribute-Id</span></span>      | <span data-ttu-id="d9387-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="d9387-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="d9387-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d9387-120">System-Id-Guid</span></span>    | <span data-ttu-id="d9387-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d9387-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="d9387-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9387-122">Syntax</span></span>            | [<span data-ttu-id="d9387-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="d9387-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="d9387-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d9387-124">Implementations</span></span>

-   [<span data-ttu-id="d9387-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d9387-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d9387-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d9387-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d9387-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d9387-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d9387-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d9387-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d9387-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d9387-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d9387-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d9387-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d9387-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d9387-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d9387-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9387-132">Entry</span></span> | <span data-ttu-id="d9387-133">Value</span><span class="sxs-lookup"><span data-stu-id="d9387-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9387-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9387-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9387-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9387-135">MAPI-Id</span></span>                | <span data-ttu-id="d9387-136">0x39FF</span><span class="sxs-lookup"><span data-stu-id="d9387-136">0x39FF</span></span>                          |
| <span data-ttu-id="d9387-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9387-137">System-Only</span></span>            | <span data-ttu-id="d9387-138">False</span><span class="sxs-lookup"><span data-stu-id="d9387-138">False</span></span>                           |
| <span data-ttu-id="d9387-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9387-139">Is-Single-Valued</span></span>       | <span data-ttu-id="d9387-140">True</span><span class="sxs-lookup"><span data-stu-id="d9387-140">True</span></span>                            |
| <span data-ttu-id="d9387-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9387-141">Is Indexed</span></span>             | <span data-ttu-id="d9387-142">False</span><span class="sxs-lookup"><span data-stu-id="d9387-142">False</span></span>                           |
| <span data-ttu-id="d9387-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9387-143">In Global Catalog</span></span>      | <span data-ttu-id="d9387-144">False</span><span class="sxs-lookup"><span data-stu-id="d9387-144">False</span></span>                           |
| <span data-ttu-id="d9387-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9387-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9387-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9387-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9387-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9387-147">Range-Lower</span></span>            | <span data-ttu-id="d9387-148">1</span><span class="sxs-lookup"><span data-stu-id="d9387-148">1</span></span>                               |
| <span data-ttu-id="d9387-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9387-149">Range-Upper</span></span>            | <span data-ttu-id="d9387-150">256</span><span class="sxs-lookup"><span data-stu-id="d9387-150">256</span></span>                             |
| <span data-ttu-id="d9387-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-151">Search-Flags</span></span>           | <span data-ttu-id="d9387-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9387-152">0x00000000</span></span>                      |
| <span data-ttu-id="d9387-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-153">System-Flags</span></span>           | <span data-ttu-id="d9387-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9387-154">0x00000010</span></span>                      |
| <span data-ttu-id="d9387-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9387-155">Classes used in</span></span>        | [<span data-ttu-id="d9387-156">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9387-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d9387-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d9387-157">Windows Server 2003</span></span>



| <span data-ttu-id="d9387-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9387-158">Entry</span></span> | <span data-ttu-id="d9387-159">Value</span><span class="sxs-lookup"><span data-stu-id="d9387-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9387-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9387-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9387-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9387-161">MAPI-Id</span></span>                | <span data-ttu-id="d9387-162">0x39FF</span><span class="sxs-lookup"><span data-stu-id="d9387-162">0x39FF</span></span>                          |
| <span data-ttu-id="d9387-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9387-163">System-Only</span></span>            | <span data-ttu-id="d9387-164">False</span><span class="sxs-lookup"><span data-stu-id="d9387-164">False</span></span>                           |
| <span data-ttu-id="d9387-165">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9387-165">Is-Single-Valued</span></span>       | <span data-ttu-id="d9387-166">True</span><span class="sxs-lookup"><span data-stu-id="d9387-166">True</span></span>                            |
| <span data-ttu-id="d9387-167">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9387-167">Is Indexed</span></span>             | <span data-ttu-id="d9387-168">False</span><span class="sxs-lookup"><span data-stu-id="d9387-168">False</span></span>                           |
| <span data-ttu-id="d9387-169">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9387-169">In Global Catalog</span></span>      | <span data-ttu-id="d9387-170">False</span><span class="sxs-lookup"><span data-stu-id="d9387-170">False</span></span>                           |
| <span data-ttu-id="d9387-171">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9387-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9387-172">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9387-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9387-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9387-173">Range-Lower</span></span>            | <span data-ttu-id="d9387-174">1</span><span class="sxs-lookup"><span data-stu-id="d9387-174">1</span></span>                               |
| <span data-ttu-id="d9387-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9387-175">Range-Upper</span></span>            | <span data-ttu-id="d9387-176">256</span><span class="sxs-lookup"><span data-stu-id="d9387-176">256</span></span>                             |
| <span data-ttu-id="d9387-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-177">Search-Flags</span></span>           | <span data-ttu-id="d9387-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9387-178">0x00000000</span></span>                      |
| <span data-ttu-id="d9387-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-179">System-Flags</span></span>           | <span data-ttu-id="d9387-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9387-180">0x00000010</span></span>                      |
| <span data-ttu-id="d9387-181">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9387-181">Classes used in</span></span>        | [<span data-ttu-id="d9387-182">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9387-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d9387-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d9387-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d9387-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9387-184">Entry</span></span> | <span data-ttu-id="d9387-185">Value</span><span class="sxs-lookup"><span data-stu-id="d9387-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9387-186">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9387-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9387-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9387-187">MAPI-Id</span></span>                | <span data-ttu-id="d9387-188">0x39FF</span><span class="sxs-lookup"><span data-stu-id="d9387-188">0x39FF</span></span>                          |
| <span data-ttu-id="d9387-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9387-189">System-Only</span></span>            | <span data-ttu-id="d9387-190">False</span><span class="sxs-lookup"><span data-stu-id="d9387-190">False</span></span>                           |
| <span data-ttu-id="d9387-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9387-191">Is-Single-Valued</span></span>       | <span data-ttu-id="d9387-192">True</span><span class="sxs-lookup"><span data-stu-id="d9387-192">True</span></span>                            |
| <span data-ttu-id="d9387-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9387-193">Is Indexed</span></span>             | <span data-ttu-id="d9387-194">False</span><span class="sxs-lookup"><span data-stu-id="d9387-194">False</span></span>                           |
| <span data-ttu-id="d9387-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9387-195">In Global Catalog</span></span>      | <span data-ttu-id="d9387-196">False</span><span class="sxs-lookup"><span data-stu-id="d9387-196">False</span></span>                           |
| <span data-ttu-id="d9387-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9387-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9387-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9387-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9387-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9387-199">Range-Lower</span></span>            | <span data-ttu-id="d9387-200">1</span><span class="sxs-lookup"><span data-stu-id="d9387-200">1</span></span>                               |
| <span data-ttu-id="d9387-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9387-201">Range-Upper</span></span>            | <span data-ttu-id="d9387-202">256</span><span class="sxs-lookup"><span data-stu-id="d9387-202">256</span></span>                             |
| <span data-ttu-id="d9387-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-203">Search-Flags</span></span>           | <span data-ttu-id="d9387-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9387-204">0x00000000</span></span>                      |
| <span data-ttu-id="d9387-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-205">System-Flags</span></span>           | <span data-ttu-id="d9387-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9387-206">0x00000010</span></span>                      |
| <span data-ttu-id="d9387-207">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9387-207">Classes used in</span></span>        | [<span data-ttu-id="d9387-208">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9387-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d9387-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9387-209">Windows Server 2008</span></span>



| <span data-ttu-id="d9387-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9387-210">Entry</span></span> | <span data-ttu-id="d9387-211">Value</span><span class="sxs-lookup"><span data-stu-id="d9387-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9387-212">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9387-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9387-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9387-213">MAPI-Id</span></span>                | <span data-ttu-id="d9387-214">0x39FF</span><span class="sxs-lookup"><span data-stu-id="d9387-214">0x39FF</span></span>                          |
| <span data-ttu-id="d9387-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9387-215">System-Only</span></span>            | <span data-ttu-id="d9387-216">False</span><span class="sxs-lookup"><span data-stu-id="d9387-216">False</span></span>                           |
| <span data-ttu-id="d9387-217">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9387-217">Is-Single-Valued</span></span>       | <span data-ttu-id="d9387-218">True</span><span class="sxs-lookup"><span data-stu-id="d9387-218">True</span></span>                            |
| <span data-ttu-id="d9387-219">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9387-219">Is Indexed</span></span>             | <span data-ttu-id="d9387-220">False</span><span class="sxs-lookup"><span data-stu-id="d9387-220">False</span></span>                           |
| <span data-ttu-id="d9387-221">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9387-221">In Global Catalog</span></span>      | <span data-ttu-id="d9387-222">False</span><span class="sxs-lookup"><span data-stu-id="d9387-222">False</span></span>                           |
| <span data-ttu-id="d9387-223">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9387-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9387-224">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9387-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9387-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9387-225">Range-Lower</span></span>            | <span data-ttu-id="d9387-226">1</span><span class="sxs-lookup"><span data-stu-id="d9387-226">1</span></span>                               |
| <span data-ttu-id="d9387-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9387-227">Range-Upper</span></span>            | <span data-ttu-id="d9387-228">256</span><span class="sxs-lookup"><span data-stu-id="d9387-228">256</span></span>                             |
| <span data-ttu-id="d9387-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-229">Search-Flags</span></span>           | <span data-ttu-id="d9387-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9387-230">0x00000000</span></span>                      |
| <span data-ttu-id="d9387-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-231">System-Flags</span></span>           | <span data-ttu-id="d9387-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9387-232">0x00000010</span></span>                      |
| <span data-ttu-id="d9387-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9387-233">Classes used in</span></span>        | [<span data-ttu-id="d9387-234">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9387-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d9387-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9387-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d9387-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9387-236">Entry</span></span> | <span data-ttu-id="d9387-237">Value</span><span class="sxs-lookup"><span data-stu-id="d9387-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9387-238">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9387-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9387-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9387-239">MAPI-Id</span></span>                | <span data-ttu-id="d9387-240">0x39FF</span><span class="sxs-lookup"><span data-stu-id="d9387-240">0x39FF</span></span>                          |
| <span data-ttu-id="d9387-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9387-241">System-Only</span></span>            | <span data-ttu-id="d9387-242">False</span><span class="sxs-lookup"><span data-stu-id="d9387-242">False</span></span>                           |
| <span data-ttu-id="d9387-243">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9387-243">Is-Single-Valued</span></span>       | <span data-ttu-id="d9387-244">True</span><span class="sxs-lookup"><span data-stu-id="d9387-244">True</span></span>                            |
| <span data-ttu-id="d9387-245">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9387-245">Is Indexed</span></span>             | <span data-ttu-id="d9387-246">False</span><span class="sxs-lookup"><span data-stu-id="d9387-246">False</span></span>                           |
| <span data-ttu-id="d9387-247">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9387-247">In Global Catalog</span></span>      | <span data-ttu-id="d9387-248">False</span><span class="sxs-lookup"><span data-stu-id="d9387-248">False</span></span>                           |
| <span data-ttu-id="d9387-249">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9387-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9387-250">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9387-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9387-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9387-251">Range-Lower</span></span>            | <span data-ttu-id="d9387-252">1</span><span class="sxs-lookup"><span data-stu-id="d9387-252">1</span></span>                               |
| <span data-ttu-id="d9387-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9387-253">Range-Upper</span></span>            | <span data-ttu-id="d9387-254">256</span><span class="sxs-lookup"><span data-stu-id="d9387-254">256</span></span>                             |
| <span data-ttu-id="d9387-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-255">Search-Flags</span></span>           | <span data-ttu-id="d9387-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9387-256">0x00000000</span></span>                      |
| <span data-ttu-id="d9387-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-257">System-Flags</span></span>           | <span data-ttu-id="d9387-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9387-258">0x00000010</span></span>                      |
| <span data-ttu-id="d9387-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9387-259">Classes used in</span></span>        | [<span data-ttu-id="d9387-260">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9387-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d9387-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9387-261">Windows Server 2012</span></span>



| <span data-ttu-id="d9387-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9387-262">Entry</span></span> | <span data-ttu-id="d9387-263">Value</span><span class="sxs-lookup"><span data-stu-id="d9387-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d9387-264">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d9387-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d9387-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9387-265">MAPI-Id</span></span>                | <span data-ttu-id="d9387-266">0x39FF</span><span class="sxs-lookup"><span data-stu-id="d9387-266">0x39FF</span></span>                          |
| <span data-ttu-id="d9387-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9387-267">System-Only</span></span>            | <span data-ttu-id="d9387-268">False</span><span class="sxs-lookup"><span data-stu-id="d9387-268">False</span></span>                           |
| <span data-ttu-id="d9387-269">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d9387-269">Is-Single-Valued</span></span>       | <span data-ttu-id="d9387-270">True</span><span class="sxs-lookup"><span data-stu-id="d9387-270">True</span></span>                            |
| <span data-ttu-id="d9387-271">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d9387-271">Is Indexed</span></span>             | <span data-ttu-id="d9387-272">False</span><span class="sxs-lookup"><span data-stu-id="d9387-272">False</span></span>                           |
| <span data-ttu-id="d9387-273">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9387-273">In Global Catalog</span></span>      | <span data-ttu-id="d9387-274">False</span><span class="sxs-lookup"><span data-stu-id="d9387-274">False</span></span>                           |
| <span data-ttu-id="d9387-275">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d9387-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9387-276">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d9387-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d9387-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9387-277">Range-Lower</span></span>            | <span data-ttu-id="d9387-278">1</span><span class="sxs-lookup"><span data-stu-id="d9387-278">1</span></span>                               |
| <span data-ttu-id="d9387-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9387-279">Range-Upper</span></span>            | <span data-ttu-id="d9387-280">256</span><span class="sxs-lookup"><span data-stu-id="d9387-280">256</span></span>                             |
| <span data-ttu-id="d9387-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-281">Search-Flags</span></span>           | <span data-ttu-id="d9387-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9387-282">0x00000000</span></span>                      |
| <span data-ttu-id="d9387-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9387-283">System-Flags</span></span>           | <span data-ttu-id="d9387-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9387-284">0x00000010</span></span>                      |
| <span data-ttu-id="d9387-285">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d9387-285">Classes used in</span></span>        | [<span data-ttu-id="d9387-286">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="d9387-286">**Top**</span></span>](c-top.md)<br/> |



 

 






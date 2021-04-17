---
title: Atributo Pek-Key-Change-Interval
description: Intervalo de cambio de clave de cifrado de contraseña.
ms.assetid: 2031feda-3f5d-4c76-bb45-42157fd5cb84
ms.tgt_platform: multiple
keywords:
- Pek-Key-Change-Interval atributo AD Schema
- pekKeyChangeInterval esquema de AD de atributos
topic_type:
- apiref
api_name:
- Pek-Key-Change-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2259bdd4dfee24bbccfeafa6d5bb06490c24c25c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658777"
---
# <a name="pek-key-change-interval-attribute"></a><span data-ttu-id="c8acf-105">Atributo Pek-Key-Change-Interval</span><span class="sxs-lookup"><span data-stu-id="c8acf-105">Pek-Key-Change-Interval attribute</span></span>

<span data-ttu-id="c8acf-106">Intervalo de cambio de clave de cifrado de contraseña.</span><span class="sxs-lookup"><span data-stu-id="c8acf-106">Password encryption key change interval.</span></span>



| <span data-ttu-id="c8acf-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8acf-107">Entry</span></span> | <span data-ttu-id="c8acf-108">Value</span><span class="sxs-lookup"><span data-stu-id="c8acf-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c8acf-109">CN</span><span class="sxs-lookup"><span data-stu-id="c8acf-109">CN</span></span>                | <span data-ttu-id="c8acf-110">Pek-Key-Change-Interval</span><span class="sxs-lookup"><span data-stu-id="c8acf-110">Pek-Key-Change-Interval</span></span>              |
| <span data-ttu-id="c8acf-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c8acf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c8acf-112">pekKeyChangeInterval</span><span class="sxs-lookup"><span data-stu-id="c8acf-112">pekKeyChangeInterval</span></span>                 |
| <span data-ttu-id="c8acf-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c8acf-113">Size</span></span>              | <span data-ttu-id="c8acf-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="c8acf-114">8 bytes</span></span>                              |
| <span data-ttu-id="c8acf-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c8acf-115">Update Privilege</span></span>  | <span data-ttu-id="c8acf-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="c8acf-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="c8acf-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c8acf-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c8acf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c8acf-118">Attribute-Id</span></span>      | <span data-ttu-id="c8acf-119">1.2.840.113556.1.4.866</span><span class="sxs-lookup"><span data-stu-id="c8acf-119">1.2.840.113556.1.4.866</span></span>               |
| <span data-ttu-id="c8acf-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c8acf-120">System-Id-Guid</span></span>    | <span data-ttu-id="c8acf-121">07383084-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c8acf-121">07383084-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="c8acf-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8acf-122">Syntax</span></span>            | [<span data-ttu-id="c8acf-123">**Interval**</span><span class="sxs-lookup"><span data-stu-id="c8acf-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="c8acf-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c8acf-124">Implementations</span></span>

-   [<span data-ttu-id="c8acf-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c8acf-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c8acf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c8acf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c8acf-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c8acf-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c8acf-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c8acf-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c8acf-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c8acf-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c8acf-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c8acf-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c8acf-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8acf-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c8acf-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8acf-132">Entry</span></span> | <span data-ttu-id="c8acf-133">Value</span><span class="sxs-lookup"><span data-stu-id="c8acf-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8acf-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8acf-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8acf-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8acf-136">System-Only</span></span>            | <span data-ttu-id="c8acf-137">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-137">False</span></span>                                        |
| <span data-ttu-id="c8acf-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8acf-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c8acf-139">True</span><span class="sxs-lookup"><span data-stu-id="c8acf-139">True</span></span>                                         |
| <span data-ttu-id="c8acf-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8acf-140">Is Indexed</span></span>             | <span data-ttu-id="c8acf-141">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-141">False</span></span>                                        |
| <span data-ttu-id="c8acf-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8acf-142">In Global Catalog</span></span>      | <span data-ttu-id="c8acf-143">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-143">False</span></span>                                        |
| <span data-ttu-id="c8acf-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8acf-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8acf-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8acf-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8acf-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8acf-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8acf-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-148">Search-Flags</span></span>           | <span data-ttu-id="c8acf-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8acf-149">0x00000000</span></span>                                   |
| <span data-ttu-id="c8acf-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-150">System-Flags</span></span>           | <span data-ttu-id="c8acf-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8acf-151">0x00000010</span></span>                                   |
| <span data-ttu-id="c8acf-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8acf-152">Classes used in</span></span>        | [<span data-ttu-id="c8acf-153">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="c8acf-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c8acf-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c8acf-154">Windows Server 2003</span></span>



| <span data-ttu-id="c8acf-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8acf-155">Entry</span></span> | <span data-ttu-id="c8acf-156">Value</span><span class="sxs-lookup"><span data-stu-id="c8acf-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8acf-157">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8acf-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8acf-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8acf-159">System-Only</span></span>            | <span data-ttu-id="c8acf-160">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-160">False</span></span>                                        |
| <span data-ttu-id="c8acf-161">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8acf-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c8acf-162">True</span><span class="sxs-lookup"><span data-stu-id="c8acf-162">True</span></span>                                         |
| <span data-ttu-id="c8acf-163">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8acf-163">Is Indexed</span></span>             | <span data-ttu-id="c8acf-164">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-164">False</span></span>                                        |
| <span data-ttu-id="c8acf-165">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8acf-165">In Global Catalog</span></span>      | <span data-ttu-id="c8acf-166">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-166">False</span></span>                                        |
| <span data-ttu-id="c8acf-167">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8acf-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8acf-168">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8acf-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8acf-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8acf-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8acf-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-171">Search-Flags</span></span>           | <span data-ttu-id="c8acf-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8acf-172">0x00000000</span></span>                                   |
| <span data-ttu-id="c8acf-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-173">System-Flags</span></span>           | <span data-ttu-id="c8acf-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8acf-174">0x00000010</span></span>                                   |
| <span data-ttu-id="c8acf-175">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8acf-175">Classes used in</span></span>        | [<span data-ttu-id="c8acf-176">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="c8acf-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c8acf-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c8acf-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c8acf-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8acf-178">Entry</span></span> | <span data-ttu-id="c8acf-179">Value</span><span class="sxs-lookup"><span data-stu-id="c8acf-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8acf-180">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8acf-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8acf-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8acf-182">System-Only</span></span>            | <span data-ttu-id="c8acf-183">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-183">False</span></span>                                        |
| <span data-ttu-id="c8acf-184">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8acf-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c8acf-185">True</span><span class="sxs-lookup"><span data-stu-id="c8acf-185">True</span></span>                                         |
| <span data-ttu-id="c8acf-186">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8acf-186">Is Indexed</span></span>             | <span data-ttu-id="c8acf-187">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-187">False</span></span>                                        |
| <span data-ttu-id="c8acf-188">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8acf-188">In Global Catalog</span></span>      | <span data-ttu-id="c8acf-189">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-189">False</span></span>                                        |
| <span data-ttu-id="c8acf-190">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8acf-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8acf-191">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8acf-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8acf-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8acf-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8acf-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-194">Search-Flags</span></span>           | <span data-ttu-id="c8acf-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8acf-195">0x00000000</span></span>                                   |
| <span data-ttu-id="c8acf-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-196">System-Flags</span></span>           | <span data-ttu-id="c8acf-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8acf-197">0x00000010</span></span>                                   |
| <span data-ttu-id="c8acf-198">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8acf-198">Classes used in</span></span>        | [<span data-ttu-id="c8acf-199">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="c8acf-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c8acf-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8acf-200">Windows Server 2008</span></span>



| <span data-ttu-id="c8acf-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8acf-201">Entry</span></span> | <span data-ttu-id="c8acf-202">Value</span><span class="sxs-lookup"><span data-stu-id="c8acf-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8acf-203">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8acf-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8acf-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8acf-205">System-Only</span></span>            | <span data-ttu-id="c8acf-206">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-206">False</span></span>                                        |
| <span data-ttu-id="c8acf-207">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8acf-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c8acf-208">True</span><span class="sxs-lookup"><span data-stu-id="c8acf-208">True</span></span>                                         |
| <span data-ttu-id="c8acf-209">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8acf-209">Is Indexed</span></span>             | <span data-ttu-id="c8acf-210">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-210">False</span></span>                                        |
| <span data-ttu-id="c8acf-211">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8acf-211">In Global Catalog</span></span>      | <span data-ttu-id="c8acf-212">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-212">False</span></span>                                        |
| <span data-ttu-id="c8acf-213">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8acf-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8acf-214">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8acf-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8acf-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8acf-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8acf-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-217">Search-Flags</span></span>           | <span data-ttu-id="c8acf-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8acf-218">0x00000000</span></span>                                   |
| <span data-ttu-id="c8acf-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-219">System-Flags</span></span>           | <span data-ttu-id="c8acf-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8acf-220">0x00000010</span></span>                                   |
| <span data-ttu-id="c8acf-221">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8acf-221">Classes used in</span></span>        | [<span data-ttu-id="c8acf-222">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="c8acf-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c8acf-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8acf-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c8acf-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8acf-224">Entry</span></span> | <span data-ttu-id="c8acf-225">Value</span><span class="sxs-lookup"><span data-stu-id="c8acf-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8acf-226">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8acf-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8acf-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8acf-228">System-Only</span></span>            | <span data-ttu-id="c8acf-229">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-229">False</span></span>                                        |
| <span data-ttu-id="c8acf-230">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8acf-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c8acf-231">True</span><span class="sxs-lookup"><span data-stu-id="c8acf-231">True</span></span>                                         |
| <span data-ttu-id="c8acf-232">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8acf-232">Is Indexed</span></span>             | <span data-ttu-id="c8acf-233">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-233">False</span></span>                                        |
| <span data-ttu-id="c8acf-234">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8acf-234">In Global Catalog</span></span>      | <span data-ttu-id="c8acf-235">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-235">False</span></span>                                        |
| <span data-ttu-id="c8acf-236">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8acf-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8acf-237">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8acf-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8acf-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8acf-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8acf-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-240">Search-Flags</span></span>           | <span data-ttu-id="c8acf-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8acf-241">0x00000000</span></span>                                   |
| <span data-ttu-id="c8acf-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-242">System-Flags</span></span>           | <span data-ttu-id="c8acf-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8acf-243">0x00000010</span></span>                                   |
| <span data-ttu-id="c8acf-244">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8acf-244">Classes used in</span></span>        | [<span data-ttu-id="c8acf-245">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="c8acf-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c8acf-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8acf-246">Windows Server 2012</span></span>



| <span data-ttu-id="c8acf-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="c8acf-247">Entry</span></span> | <span data-ttu-id="c8acf-248">Value</span><span class="sxs-lookup"><span data-stu-id="c8acf-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c8acf-249">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c8acf-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c8acf-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c8acf-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c8acf-251">System-Only</span></span>            | <span data-ttu-id="c8acf-252">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-252">False</span></span>                                        |
| <span data-ttu-id="c8acf-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c8acf-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c8acf-254">True</span><span class="sxs-lookup"><span data-stu-id="c8acf-254">True</span></span>                                         |
| <span data-ttu-id="c8acf-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c8acf-255">Is Indexed</span></span>             | <span data-ttu-id="c8acf-256">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-256">False</span></span>                                        |
| <span data-ttu-id="c8acf-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c8acf-257">In Global Catalog</span></span>      | <span data-ttu-id="c8acf-258">False</span><span class="sxs-lookup"><span data-stu-id="c8acf-258">False</span></span>                                        |
| <span data-ttu-id="c8acf-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c8acf-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c8acf-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c8acf-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c8acf-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c8acf-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c8acf-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c8acf-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-263">Search-Flags</span></span>           | <span data-ttu-id="c8acf-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c8acf-264">0x00000000</span></span>                                   |
| <span data-ttu-id="c8acf-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c8acf-265">System-Flags</span></span>           | <span data-ttu-id="c8acf-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c8acf-266">0x00000010</span></span>                                   |
| <span data-ttu-id="c8acf-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c8acf-267">Classes used in</span></span>        | [<span data-ttu-id="c8acf-268">**Sam-dominio**</span><span class="sxs-lookup"><span data-stu-id="c8acf-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 






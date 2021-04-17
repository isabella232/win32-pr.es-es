---
title: System-auxiliar-Class (atributo)
description: Una lista de las clases auxiliares que el usuario no puede modificar.
ms.assetid: 6d629925-7321-4f3a-bf4c-4adf0d33c946
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de clase auxiliar del sistema
- systemAuxiliaryClass esquema de AD de atributos
topic_type:
- apiref
api_name:
- System-Auxiliary-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe70899ba2bda8fe98b38228cb661e7a773ec1d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658732"
---
# <a name="system-auxiliary-class-attribute"></a><span data-ttu-id="6e06b-105">System-auxiliar-Class (atributo)</span><span class="sxs-lookup"><span data-stu-id="6e06b-105">System-Auxiliary-Class attribute</span></span>

<span data-ttu-id="6e06b-106">Una lista de las clases auxiliares que el usuario no puede modificar.</span><span class="sxs-lookup"><span data-stu-id="6e06b-106">A list of auxiliary classes that cannot be modified by the user.</span></span>



| <span data-ttu-id="6e06b-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e06b-107">Entry</span></span> | <span data-ttu-id="6e06b-108">Value</span><span class="sxs-lookup"><span data-stu-id="6e06b-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6e06b-109">CN</span><span class="sxs-lookup"><span data-stu-id="6e06b-109">CN</span></span>                | <span data-ttu-id="6e06b-110">System-auxiliar-clase</span><span class="sxs-lookup"><span data-stu-id="6e06b-110">System-Auxiliary-Class</span></span>                                             |
| <span data-ttu-id="6e06b-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6e06b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6e06b-112">systemAuxiliaryClass</span><span class="sxs-lookup"><span data-stu-id="6e06b-112">systemAuxiliaryClass</span></span>                                               |
| <span data-ttu-id="6e06b-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6e06b-113">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="6e06b-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6e06b-114">Update Privilege</span></span>  | <span data-ttu-id="6e06b-115">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="6e06b-115">Schema administrator</span></span>                                               |
| <span data-ttu-id="6e06b-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6e06b-116">Update Frequency</span></span>  | <span data-ttu-id="6e06b-117">Cuando se crea la clase o se le agrega una nueva clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="6e06b-117">When the class is created or a new auxiliary class is added to it.</span></span> |
| <span data-ttu-id="6e06b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6e06b-118">Attribute-Id</span></span>      | <span data-ttu-id="6e06b-119">1.2.840.113556.1.4.198</span><span class="sxs-lookup"><span data-stu-id="6e06b-119">1.2.840.113556.1.4.198</span></span>                                             |
| <span data-ttu-id="6e06b-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6e06b-120">System-Id-Guid</span></span>    | <span data-ttu-id="6e06b-121">bf967a43-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6e06b-121">bf967a43-0de6-11d0-a285-00aa003049e2</span></span>                               |
| <span data-ttu-id="6e06b-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e06b-122">Syntax</span></span>            | [<span data-ttu-id="6e06b-123">**String(Object-Identifier)**</span><span class="sxs-lookup"><span data-stu-id="6e06b-123">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md)    |



## <a name="implementations"></a><span data-ttu-id="6e06b-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6e06b-124">Implementations</span></span>

-   [<span data-ttu-id="6e06b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6e06b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6e06b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6e06b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6e06b-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6e06b-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6e06b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6e06b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6e06b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6e06b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6e06b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6e06b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6e06b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6e06b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6e06b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e06b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6e06b-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e06b-133">Entry</span></span> | <span data-ttu-id="6e06b-134">Value</span><span class="sxs-lookup"><span data-stu-id="6e06b-134">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e06b-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6e06b-135">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e06b-136">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e06b-137">System-Only</span></span>            | <span data-ttu-id="6e06b-138">True</span><span class="sxs-lookup"><span data-stu-id="6e06b-138">True</span></span>                                             |
| <span data-ttu-id="6e06b-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6e06b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6e06b-140">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-140">False</span></span>                                            |
| <span data-ttu-id="6e06b-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6e06b-141">Is Indexed</span></span>             | <span data-ttu-id="6e06b-142">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-142">False</span></span>                                            |
| <span data-ttu-id="6e06b-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6e06b-143">In Global Catalog</span></span>      | <span data-ttu-id="6e06b-144">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-144">False</span></span>                                            |
| <span data-ttu-id="6e06b-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6e06b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e06b-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6e06b-146">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e06b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e06b-147">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e06b-148">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-149">Search-Flags</span></span>           | <span data-ttu-id="6e06b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e06b-150">0x00000000</span></span>                                       |
| <span data-ttu-id="6e06b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-151">System-Flags</span></span>           | <span data-ttu-id="6e06b-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e06b-152">0x00000010</span></span>                                       |
| <span data-ttu-id="6e06b-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6e06b-153">Classes used in</span></span>        | [<span data-ttu-id="6e06b-154">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="6e06b-154">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6e06b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e06b-155">Windows Server 2003</span></span>



| <span data-ttu-id="6e06b-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e06b-156">Entry</span></span> | <span data-ttu-id="6e06b-157">Value</span><span class="sxs-lookup"><span data-stu-id="6e06b-157">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e06b-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6e06b-158">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e06b-159">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e06b-160">System-Only</span></span>            | <span data-ttu-id="6e06b-161">True</span><span class="sxs-lookup"><span data-stu-id="6e06b-161">True</span></span>                                             |
| <span data-ttu-id="6e06b-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6e06b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="6e06b-163">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-163">False</span></span>                                            |
| <span data-ttu-id="6e06b-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6e06b-164">Is Indexed</span></span>             | <span data-ttu-id="6e06b-165">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-165">False</span></span>                                            |
| <span data-ttu-id="6e06b-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6e06b-166">In Global Catalog</span></span>      | <span data-ttu-id="6e06b-167">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-167">False</span></span>                                            |
| <span data-ttu-id="6e06b-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6e06b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e06b-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6e06b-169">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e06b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e06b-170">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e06b-171">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-172">Search-Flags</span></span>           | <span data-ttu-id="6e06b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e06b-173">0x00000000</span></span>                                       |
| <span data-ttu-id="6e06b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-174">System-Flags</span></span>           | <span data-ttu-id="6e06b-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e06b-175">0x00000010</span></span>                                       |
| <span data-ttu-id="6e06b-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6e06b-176">Classes used in</span></span>        | [<span data-ttu-id="6e06b-177">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="6e06b-177">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6e06b-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="6e06b-178">ADAM</span></span>



| <span data-ttu-id="6e06b-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e06b-179">Entry</span></span> | <span data-ttu-id="6e06b-180">Value</span><span class="sxs-lookup"><span data-stu-id="6e06b-180">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e06b-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6e06b-181">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e06b-182">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e06b-183">System-Only</span></span>            | <span data-ttu-id="6e06b-184">True</span><span class="sxs-lookup"><span data-stu-id="6e06b-184">True</span></span>                                             |
| <span data-ttu-id="6e06b-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6e06b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="6e06b-186">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-186">False</span></span>                                            |
| <span data-ttu-id="6e06b-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6e06b-187">Is Indexed</span></span>             | <span data-ttu-id="6e06b-188">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-188">False</span></span>                                            |
| <span data-ttu-id="6e06b-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6e06b-189">In Global Catalog</span></span>      | <span data-ttu-id="6e06b-190">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-190">False</span></span>                                            |
| <span data-ttu-id="6e06b-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6e06b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e06b-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6e06b-192">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e06b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e06b-193">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e06b-194">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-195">Search-Flags</span></span>           | <span data-ttu-id="6e06b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e06b-196">0x00000000</span></span>                                       |
| <span data-ttu-id="6e06b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-197">System-Flags</span></span>           | <span data-ttu-id="6e06b-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e06b-198">0x00000010</span></span>                                       |
| <span data-ttu-id="6e06b-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6e06b-199">Classes used in</span></span>        | [<span data-ttu-id="6e06b-200">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="6e06b-200">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6e06b-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6e06b-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6e06b-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e06b-202">Entry</span></span> | <span data-ttu-id="6e06b-203">Value</span><span class="sxs-lookup"><span data-stu-id="6e06b-203">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e06b-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6e06b-204">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e06b-205">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e06b-206">System-Only</span></span>            | <span data-ttu-id="6e06b-207">True</span><span class="sxs-lookup"><span data-stu-id="6e06b-207">True</span></span>                                             |
| <span data-ttu-id="6e06b-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6e06b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="6e06b-209">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-209">False</span></span>                                            |
| <span data-ttu-id="6e06b-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6e06b-210">Is Indexed</span></span>             | <span data-ttu-id="6e06b-211">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-211">False</span></span>                                            |
| <span data-ttu-id="6e06b-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6e06b-212">In Global Catalog</span></span>      | <span data-ttu-id="6e06b-213">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-213">False</span></span>                                            |
| <span data-ttu-id="6e06b-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6e06b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e06b-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6e06b-215">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e06b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e06b-216">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e06b-217">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-218">Search-Flags</span></span>           | <span data-ttu-id="6e06b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e06b-219">0x00000000</span></span>                                       |
| <span data-ttu-id="6e06b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-220">System-Flags</span></span>           | <span data-ttu-id="6e06b-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e06b-221">0x00000010</span></span>                                       |
| <span data-ttu-id="6e06b-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6e06b-222">Classes used in</span></span>        | [<span data-ttu-id="6e06b-223">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="6e06b-223">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6e06b-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e06b-224">Windows Server 2008</span></span>



| <span data-ttu-id="6e06b-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e06b-225">Entry</span></span> | <span data-ttu-id="6e06b-226">Value</span><span class="sxs-lookup"><span data-stu-id="6e06b-226">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e06b-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6e06b-227">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e06b-228">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e06b-229">System-Only</span></span>            | <span data-ttu-id="6e06b-230">True</span><span class="sxs-lookup"><span data-stu-id="6e06b-230">True</span></span>                                             |
| <span data-ttu-id="6e06b-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6e06b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="6e06b-232">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-232">False</span></span>                                            |
| <span data-ttu-id="6e06b-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6e06b-233">Is Indexed</span></span>             | <span data-ttu-id="6e06b-234">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-234">False</span></span>                                            |
| <span data-ttu-id="6e06b-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6e06b-235">In Global Catalog</span></span>      | <span data-ttu-id="6e06b-236">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-236">False</span></span>                                            |
| <span data-ttu-id="6e06b-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6e06b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e06b-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6e06b-238">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e06b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e06b-239">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e06b-240">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-241">Search-Flags</span></span>           | <span data-ttu-id="6e06b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e06b-242">0x00000000</span></span>                                       |
| <span data-ttu-id="6e06b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-243">System-Flags</span></span>           | <span data-ttu-id="6e06b-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e06b-244">0x00000010</span></span>                                       |
| <span data-ttu-id="6e06b-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6e06b-245">Classes used in</span></span>        | [<span data-ttu-id="6e06b-246">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="6e06b-246">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6e06b-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6e06b-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6e06b-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e06b-248">Entry</span></span> | <span data-ttu-id="6e06b-249">Value</span><span class="sxs-lookup"><span data-stu-id="6e06b-249">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e06b-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6e06b-250">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e06b-251">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e06b-252">System-Only</span></span>            | <span data-ttu-id="6e06b-253">True</span><span class="sxs-lookup"><span data-stu-id="6e06b-253">True</span></span>                                             |
| <span data-ttu-id="6e06b-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6e06b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="6e06b-255">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-255">False</span></span>                                            |
| <span data-ttu-id="6e06b-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6e06b-256">Is Indexed</span></span>             | <span data-ttu-id="6e06b-257">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-257">False</span></span>                                            |
| <span data-ttu-id="6e06b-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6e06b-258">In Global Catalog</span></span>      | <span data-ttu-id="6e06b-259">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-259">False</span></span>                                            |
| <span data-ttu-id="6e06b-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6e06b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e06b-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6e06b-261">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e06b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e06b-262">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e06b-263">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-264">Search-Flags</span></span>           | <span data-ttu-id="6e06b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e06b-265">0x00000000</span></span>                                       |
| <span data-ttu-id="6e06b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-266">System-Flags</span></span>           | <span data-ttu-id="6e06b-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e06b-267">0x00000010</span></span>                                       |
| <span data-ttu-id="6e06b-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6e06b-268">Classes used in</span></span>        | [<span data-ttu-id="6e06b-269">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="6e06b-269">**Class-Schema**</span></span>](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6e06b-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e06b-270">Windows Server 2012</span></span>



| <span data-ttu-id="6e06b-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e06b-271">Entry</span></span> | <span data-ttu-id="6e06b-272">Value</span><span class="sxs-lookup"><span data-stu-id="6e06b-272">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6e06b-273">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6e06b-273">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6e06b-274">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="6e06b-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="6e06b-275">System-Only</span></span>            | <span data-ttu-id="6e06b-276">True</span><span class="sxs-lookup"><span data-stu-id="6e06b-276">True</span></span>                                             |
| <span data-ttu-id="6e06b-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6e06b-277">Is-Single-Valued</span></span>       | <span data-ttu-id="6e06b-278">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-278">False</span></span>                                            |
| <span data-ttu-id="6e06b-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6e06b-279">Is Indexed</span></span>             | <span data-ttu-id="6e06b-280">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-280">False</span></span>                                            |
| <span data-ttu-id="6e06b-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6e06b-281">In Global Catalog</span></span>      | <span data-ttu-id="6e06b-282">False</span><span class="sxs-lookup"><span data-stu-id="6e06b-282">False</span></span>                                            |
| <span data-ttu-id="6e06b-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6e06b-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="6e06b-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6e06b-284">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6e06b-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6e06b-285">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6e06b-286">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6e06b-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-287">Search-Flags</span></span>           | <span data-ttu-id="6e06b-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6e06b-288">0x00000000</span></span>                                       |
| <span data-ttu-id="6e06b-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6e06b-289">System-Flags</span></span>           | <span data-ttu-id="6e06b-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6e06b-290">0x00000010</span></span>                                       |
| <span data-ttu-id="6e06b-291">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6e06b-291">Classes used in</span></span>        | [<span data-ttu-id="6e06b-292">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="6e06b-292">**Class-Schema**</span></span>](c-classschema.md)<br/> |



 

 






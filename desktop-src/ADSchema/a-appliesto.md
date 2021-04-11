---
title: Applies-To atributo)
description: Contiene la lista de clases de objetos a la que se aplica el derecho extendido. En la lista, una clase de objeto se representa mediante la propiedad schemaIDGUID para su objeto schemaClass.
ms.assetid: 8333e508-627c-42ce-865b-db061a5603db
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Applies-To
- atributo appliesTo esquema de AD
topic_type:
- apiref
api_name:
- Applies-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b96a2690f420259b038b54b6d2b070b41f56d4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151895"
---
# <a name="applies-to-attribute"></a><span data-ttu-id="6f51a-106">Applies-To atributo)</span><span class="sxs-lookup"><span data-stu-id="6f51a-106">Applies-To attribute</span></span>

<span data-ttu-id="6f51a-107">Contiene la lista de clases de objetos a la que se aplica el derecho extendido.</span><span class="sxs-lookup"><span data-stu-id="6f51a-107">Contains the list of object classes that the extended right applies to.</span></span> <span data-ttu-id="6f51a-108">En la lista, una clase de objeto se representa mediante la propiedad schemaIDGUID para su objeto schemaClass.</span><span class="sxs-lookup"><span data-stu-id="6f51a-108">In the list, an object class is represented by the schemaIDGUID property for its schemaClass object.</span></span>



| <span data-ttu-id="6f51a-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f51a-109">Entry</span></span> | <span data-ttu-id="6f51a-110">Value</span><span class="sxs-lookup"><span data-stu-id="6f51a-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6f51a-111">CN</span><span class="sxs-lookup"><span data-stu-id="6f51a-111">CN</span></span>                | <span data-ttu-id="6f51a-112">Applies-To</span><span class="sxs-lookup"><span data-stu-id="6f51a-112">Applies-To</span></span>                                  |
| <span data-ttu-id="6f51a-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6f51a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6f51a-114">appliesTo</span><span class="sxs-lookup"><span data-stu-id="6f51a-114">appliesTo</span></span>                                   |
| <span data-ttu-id="6f51a-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6f51a-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="6f51a-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6f51a-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6f51a-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6f51a-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6f51a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6f51a-118">Attribute-Id</span></span>      | <span data-ttu-id="6f51a-119">1.2.840.113556.1.4.341</span><span class="sxs-lookup"><span data-stu-id="6f51a-119">1.2.840.113556.1.4.341</span></span>                      |
| <span data-ttu-id="6f51a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6f51a-120">System-Id-Guid</span></span>    | <span data-ttu-id="6f51a-121">8297931d-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="6f51a-121">8297931d-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="6f51a-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f51a-122">Syntax</span></span>            | [<span data-ttu-id="6f51a-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6f51a-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6f51a-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6f51a-124">Implementations</span></span>

-   [<span data-ttu-id="6f51a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6f51a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6f51a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6f51a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6f51a-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6f51a-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6f51a-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6f51a-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6f51a-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6f51a-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6f51a-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6f51a-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6f51a-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6f51a-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6f51a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f51a-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6f51a-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f51a-133">Entry</span></span> | <span data-ttu-id="6f51a-134">Value</span><span class="sxs-lookup"><span data-stu-id="6f51a-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6f51a-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6f51a-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f51a-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f51a-137">System-Only</span></span>            | <span data-ttu-id="6f51a-138">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-138">False</span></span>                                                           |
| <span data-ttu-id="6f51a-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6f51a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6f51a-140">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-140">False</span></span>                                                           |
| <span data-ttu-id="6f51a-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6f51a-141">Is Indexed</span></span>             | <span data-ttu-id="6f51a-142">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-142">False</span></span>                                                           |
| <span data-ttu-id="6f51a-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6f51a-143">In Global Catalog</span></span>      | <span data-ttu-id="6f51a-144">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-144">False</span></span>                                                           |
| <span data-ttu-id="6f51a-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6f51a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f51a-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f51a-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6f51a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f51a-147">Range-Lower</span></span>            | <span data-ttu-id="6f51a-148">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-148">36</span></span>                                                              |
| <span data-ttu-id="6f51a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f51a-149">Range-Upper</span></span>            | <span data-ttu-id="6f51a-150">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-150">36</span></span>                                                              |
| <span data-ttu-id="6f51a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-151">Search-Flags</span></span>           | <span data-ttu-id="6f51a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f51a-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="6f51a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-153">System-Flags</span></span>           | <span data-ttu-id="6f51a-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f51a-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="6f51a-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6f51a-155">Classes used in</span></span>        | [<span data-ttu-id="6f51a-156">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="6f51a-156">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6f51a-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f51a-157">Windows Server 2003</span></span>



| <span data-ttu-id="6f51a-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f51a-158">Entry</span></span> | <span data-ttu-id="6f51a-159">Value</span><span class="sxs-lookup"><span data-stu-id="6f51a-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6f51a-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6f51a-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f51a-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f51a-162">System-Only</span></span>            | <span data-ttu-id="6f51a-163">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-163">False</span></span>                                                           |
| <span data-ttu-id="6f51a-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6f51a-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6f51a-165">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-165">False</span></span>                                                           |
| <span data-ttu-id="6f51a-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6f51a-166">Is Indexed</span></span>             | <span data-ttu-id="6f51a-167">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-167">False</span></span>                                                           |
| <span data-ttu-id="6f51a-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6f51a-168">In Global Catalog</span></span>      | <span data-ttu-id="6f51a-169">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-169">False</span></span>                                                           |
| <span data-ttu-id="6f51a-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6f51a-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f51a-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f51a-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6f51a-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f51a-172">Range-Lower</span></span>            | <span data-ttu-id="6f51a-173">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-173">36</span></span>                                                              |
| <span data-ttu-id="6f51a-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f51a-174">Range-Upper</span></span>            | <span data-ttu-id="6f51a-175">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-175">36</span></span>                                                              |
| <span data-ttu-id="6f51a-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-176">Search-Flags</span></span>           | <span data-ttu-id="6f51a-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f51a-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="6f51a-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-178">System-Flags</span></span>           | <span data-ttu-id="6f51a-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f51a-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="6f51a-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6f51a-180">Classes used in</span></span>        | [<span data-ttu-id="6f51a-181">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="6f51a-181">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6f51a-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="6f51a-182">ADAM</span></span>



| <span data-ttu-id="6f51a-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f51a-183">Entry</span></span> | <span data-ttu-id="6f51a-184">Value</span><span class="sxs-lookup"><span data-stu-id="6f51a-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6f51a-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6f51a-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f51a-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f51a-187">System-Only</span></span>            | <span data-ttu-id="6f51a-188">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-188">False</span></span>                                                           |
| <span data-ttu-id="6f51a-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6f51a-189">Is-Single-Valued</span></span>       | <span data-ttu-id="6f51a-190">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-190">False</span></span>                                                           |
| <span data-ttu-id="6f51a-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6f51a-191">Is Indexed</span></span>             | <span data-ttu-id="6f51a-192">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-192">False</span></span>                                                           |
| <span data-ttu-id="6f51a-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6f51a-193">In Global Catalog</span></span>      | <span data-ttu-id="6f51a-194">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-194">False</span></span>                                                           |
| <span data-ttu-id="6f51a-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6f51a-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f51a-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f51a-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6f51a-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f51a-197">Range-Lower</span></span>            | <span data-ttu-id="6f51a-198">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-198">36</span></span>                                                              |
| <span data-ttu-id="6f51a-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f51a-199">Range-Upper</span></span>            | <span data-ttu-id="6f51a-200">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-200">36</span></span>                                                              |
| <span data-ttu-id="6f51a-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-201">Search-Flags</span></span>           | <span data-ttu-id="6f51a-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f51a-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="6f51a-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-203">System-Flags</span></span>           | <span data-ttu-id="6f51a-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f51a-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="6f51a-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6f51a-205">Classes used in</span></span>        | [<span data-ttu-id="6f51a-206">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="6f51a-206">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6f51a-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f51a-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6f51a-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f51a-208">Entry</span></span> | <span data-ttu-id="6f51a-209">Value</span><span class="sxs-lookup"><span data-stu-id="6f51a-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6f51a-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6f51a-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f51a-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f51a-212">System-Only</span></span>            | <span data-ttu-id="6f51a-213">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-213">False</span></span>                                                           |
| <span data-ttu-id="6f51a-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6f51a-214">Is-Single-Valued</span></span>       | <span data-ttu-id="6f51a-215">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-215">False</span></span>                                                           |
| <span data-ttu-id="6f51a-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6f51a-216">Is Indexed</span></span>             | <span data-ttu-id="6f51a-217">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-217">False</span></span>                                                           |
| <span data-ttu-id="6f51a-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6f51a-218">In Global Catalog</span></span>      | <span data-ttu-id="6f51a-219">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-219">False</span></span>                                                           |
| <span data-ttu-id="6f51a-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6f51a-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f51a-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f51a-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6f51a-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f51a-222">Range-Lower</span></span>            | <span data-ttu-id="6f51a-223">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-223">36</span></span>                                                              |
| <span data-ttu-id="6f51a-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f51a-224">Range-Upper</span></span>            | <span data-ttu-id="6f51a-225">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-225">36</span></span>                                                              |
| <span data-ttu-id="6f51a-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-226">Search-Flags</span></span>           | <span data-ttu-id="6f51a-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f51a-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="6f51a-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-228">System-Flags</span></span>           | <span data-ttu-id="6f51a-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f51a-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="6f51a-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6f51a-230">Classes used in</span></span>        | [<span data-ttu-id="6f51a-231">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="6f51a-231">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6f51a-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f51a-232">Windows Server 2008</span></span>



| <span data-ttu-id="6f51a-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f51a-233">Entry</span></span> | <span data-ttu-id="6f51a-234">Value</span><span class="sxs-lookup"><span data-stu-id="6f51a-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6f51a-235">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6f51a-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f51a-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f51a-237">System-Only</span></span>            | <span data-ttu-id="6f51a-238">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-238">False</span></span>                                                           |
| <span data-ttu-id="6f51a-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6f51a-239">Is-Single-Valued</span></span>       | <span data-ttu-id="6f51a-240">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-240">False</span></span>                                                           |
| <span data-ttu-id="6f51a-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6f51a-241">Is Indexed</span></span>             | <span data-ttu-id="6f51a-242">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-242">False</span></span>                                                           |
| <span data-ttu-id="6f51a-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6f51a-243">In Global Catalog</span></span>      | <span data-ttu-id="6f51a-244">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-244">False</span></span>                                                           |
| <span data-ttu-id="6f51a-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6f51a-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f51a-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f51a-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6f51a-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f51a-247">Range-Lower</span></span>            | <span data-ttu-id="6f51a-248">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-248">36</span></span>                                                              |
| <span data-ttu-id="6f51a-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f51a-249">Range-Upper</span></span>            | <span data-ttu-id="6f51a-250">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-250">36</span></span>                                                              |
| <span data-ttu-id="6f51a-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-251">Search-Flags</span></span>           | <span data-ttu-id="6f51a-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f51a-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="6f51a-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-253">System-Flags</span></span>           | <span data-ttu-id="6f51a-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f51a-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="6f51a-255">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6f51a-255">Classes used in</span></span>        | [<span data-ttu-id="6f51a-256">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="6f51a-256">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6f51a-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f51a-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6f51a-258">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f51a-258">Entry</span></span> | <span data-ttu-id="6f51a-259">Value</span><span class="sxs-lookup"><span data-stu-id="6f51a-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6f51a-260">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6f51a-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f51a-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f51a-262">System-Only</span></span>            | <span data-ttu-id="6f51a-263">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-263">False</span></span>                                                           |
| <span data-ttu-id="6f51a-264">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6f51a-264">Is-Single-Valued</span></span>       | <span data-ttu-id="6f51a-265">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-265">False</span></span>                                                           |
| <span data-ttu-id="6f51a-266">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6f51a-266">Is Indexed</span></span>             | <span data-ttu-id="6f51a-267">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-267">False</span></span>                                                           |
| <span data-ttu-id="6f51a-268">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6f51a-268">In Global Catalog</span></span>      | <span data-ttu-id="6f51a-269">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-269">False</span></span>                                                           |
| <span data-ttu-id="6f51a-270">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6f51a-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f51a-271">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f51a-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6f51a-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f51a-272">Range-Lower</span></span>            | <span data-ttu-id="6f51a-273">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-273">36</span></span>                                                              |
| <span data-ttu-id="6f51a-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f51a-274">Range-Upper</span></span>            | <span data-ttu-id="6f51a-275">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-275">36</span></span>                                                              |
| <span data-ttu-id="6f51a-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-276">Search-Flags</span></span>           | <span data-ttu-id="6f51a-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f51a-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="6f51a-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-278">System-Flags</span></span>           | <span data-ttu-id="6f51a-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f51a-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="6f51a-280">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6f51a-280">Classes used in</span></span>        | [<span data-ttu-id="6f51a-281">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="6f51a-281">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6f51a-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f51a-282">Windows Server 2012</span></span>



| <span data-ttu-id="6f51a-283">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f51a-283">Entry</span></span> | <span data-ttu-id="6f51a-284">Value</span><span class="sxs-lookup"><span data-stu-id="6f51a-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6f51a-285">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6f51a-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6f51a-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6f51a-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="6f51a-287">System-Only</span></span>            | <span data-ttu-id="6f51a-288">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-288">False</span></span>                                                           |
| <span data-ttu-id="6f51a-289">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6f51a-289">Is-Single-Valued</span></span>       | <span data-ttu-id="6f51a-290">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-290">False</span></span>                                                           |
| <span data-ttu-id="6f51a-291">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6f51a-291">Is Indexed</span></span>             | <span data-ttu-id="6f51a-292">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-292">False</span></span>                                                           |
| <span data-ttu-id="6f51a-293">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6f51a-293">In Global Catalog</span></span>      | <span data-ttu-id="6f51a-294">False</span><span class="sxs-lookup"><span data-stu-id="6f51a-294">False</span></span>                                                           |
| <span data-ttu-id="6f51a-295">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6f51a-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="6f51a-296">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6f51a-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6f51a-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6f51a-297">Range-Lower</span></span>            | <span data-ttu-id="6f51a-298">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-298">36</span></span>                                                              |
| <span data-ttu-id="6f51a-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6f51a-299">Range-Upper</span></span>            | <span data-ttu-id="6f51a-300">36</span><span class="sxs-lookup"><span data-stu-id="6f51a-300">36</span></span>                                                              |
| <span data-ttu-id="6f51a-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-301">Search-Flags</span></span>           | <span data-ttu-id="6f51a-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6f51a-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="6f51a-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6f51a-303">System-Flags</span></span>           | <span data-ttu-id="6f51a-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f51a-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="6f51a-305">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6f51a-305">Classes used in</span></span>        | [<span data-ttu-id="6f51a-306">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="6f51a-306">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 






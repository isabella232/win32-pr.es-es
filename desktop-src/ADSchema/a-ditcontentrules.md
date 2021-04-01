---
title: Atributo DIT-Content-rules
description: Esto especifica el contenido permitido de las entradas de una clase de objeto estructural determinada mediante la identificación de un conjunto opcional de clases de objeto auxiliares y atributos obligatorios, opcionales y excluidos.
ms.assetid: 75550f5c-efbf-4cd9-8619-a69d2b462f13
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo DIT-Content-rules
- dITContentRules esquema de AD de atributos
topic_type:
- apiref
api_name:
- DIT-Content-Rules
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399529237cb7a9f2c4bf1803255f546184ad47f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151857"
---
# <a name="dit-content-rules-attribute"></a><span data-ttu-id="a615c-105">Atributo DIT-Content-rules</span><span class="sxs-lookup"><span data-stu-id="a615c-105">DIT-Content-Rules attribute</span></span>

<span data-ttu-id="a615c-106">Esto especifica el contenido permitido de las entradas de una clase de objeto estructural determinada mediante la identificación de un conjunto opcional de clases de objeto auxiliares y atributos obligatorios, opcionales y excluidos.</span><span class="sxs-lookup"><span data-stu-id="a615c-106">This specifies the permissible content of entries of a particular structural object class by using the identification of an optional set of auxiliary object classes, and mandatory, optional, and precluded attributes.</span></span> <span data-ttu-id="a615c-107">Los atributos colectivos se incluyen en DIT-Content-rules, tal y como se define en RFC 2251.</span><span class="sxs-lookup"><span data-stu-id="a615c-107">Collective attributes are included in DIT-Content-Rules as defined in RFC 2251.</span></span>



| <span data-ttu-id="a615c-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="a615c-108">Entry</span></span> | <span data-ttu-id="a615c-109">Value</span><span class="sxs-lookup"><span data-stu-id="a615c-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a615c-110">CN</span><span class="sxs-lookup"><span data-stu-id="a615c-110">CN</span></span>                | <span data-ttu-id="a615c-111">DIT-Content-rules</span><span class="sxs-lookup"><span data-stu-id="a615c-111">DIT-Content-Rules</span></span>                           |
| <span data-ttu-id="a615c-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="a615c-112">Ldap-Display-Name</span></span> | <span data-ttu-id="a615c-113">dITContentRules</span><span class="sxs-lookup"><span data-stu-id="a615c-113">dITContentRules</span></span>                             |
| <span data-ttu-id="a615c-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a615c-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="a615c-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="a615c-115">Update Privilege</span></span>  | <span data-ttu-id="a615c-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a615c-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="a615c-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="a615c-117">Update Frequency</span></span>  | <span data-ttu-id="a615c-118">Siempre que se crea una nueva clase.</span><span class="sxs-lookup"><span data-stu-id="a615c-118">Whenever a new class is created.</span></span>            |
| <span data-ttu-id="a615c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a615c-119">Attribute-Id</span></span>      | <span data-ttu-id="a615c-120">2.5.21.2</span><span class="sxs-lookup"><span data-stu-id="a615c-120">2.5.21.2</span></span>                                    |
| <span data-ttu-id="a615c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a615c-121">System-Id-Guid</span></span>    | <span data-ttu-id="a615c-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="a615c-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="a615c-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a615c-123">Syntax</span></span>            | [<span data-ttu-id="a615c-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a615c-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a615c-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="a615c-125">Implementations</span></span>

-   [<span data-ttu-id="a615c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a615c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a615c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a615c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a615c-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a615c-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a615c-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a615c-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a615c-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a615c-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a615c-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a615c-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a615c-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a615c-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a615c-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a615c-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a615c-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="a615c-134">Entry</span></span> | <span data-ttu-id="a615c-135">Value</span><span class="sxs-lookup"><span data-stu-id="a615c-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="a615c-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a615c-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a615c-137">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a615c-138">System-Only</span></span>            | <span data-ttu-id="a615c-139">True</span><span class="sxs-lookup"><span data-stu-id="a615c-139">True</span></span>                                        |
| <span data-ttu-id="a615c-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a615c-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a615c-141">False</span><span class="sxs-lookup"><span data-stu-id="a615c-141">False</span></span>                                       |
| <span data-ttu-id="a615c-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a615c-142">Is Indexed</span></span>             | <span data-ttu-id="a615c-143">False</span><span class="sxs-lookup"><span data-stu-id="a615c-143">False</span></span>                                       |
| <span data-ttu-id="a615c-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a615c-144">In Global Catalog</span></span>      | <span data-ttu-id="a615c-145">False</span><span class="sxs-lookup"><span data-stu-id="a615c-145">False</span></span>                                       |
| <span data-ttu-id="a615c-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a615c-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a615c-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a615c-147">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="a615c-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a615c-148">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="a615c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a615c-149">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="a615c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-150">Search-Flags</span></span>           | <span data-ttu-id="a615c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a615c-151">0x00000000</span></span>                                  |
| <span data-ttu-id="a615c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-152">System-Flags</span></span>           | <span data-ttu-id="a615c-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a615c-153">0x08000014</span></span>                                  |
| <span data-ttu-id="a615c-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a615c-154">Classes used in</span></span>        | [<span data-ttu-id="a615c-155">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a615c-155">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a615c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a615c-156">Windows Server 2003</span></span>



| <span data-ttu-id="a615c-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="a615c-157">Entry</span></span> | <span data-ttu-id="a615c-158">Value</span><span class="sxs-lookup"><span data-stu-id="a615c-158">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="a615c-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a615c-159">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a615c-160">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a615c-161">System-Only</span></span>            | <span data-ttu-id="a615c-162">True</span><span class="sxs-lookup"><span data-stu-id="a615c-162">True</span></span>                                        |
| <span data-ttu-id="a615c-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a615c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a615c-164">False</span><span class="sxs-lookup"><span data-stu-id="a615c-164">False</span></span>                                       |
| <span data-ttu-id="a615c-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a615c-165">Is Indexed</span></span>             | <span data-ttu-id="a615c-166">False</span><span class="sxs-lookup"><span data-stu-id="a615c-166">False</span></span>                                       |
| <span data-ttu-id="a615c-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a615c-167">In Global Catalog</span></span>      | <span data-ttu-id="a615c-168">False</span><span class="sxs-lookup"><span data-stu-id="a615c-168">False</span></span>                                       |
| <span data-ttu-id="a615c-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a615c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a615c-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a615c-170">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="a615c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a615c-171">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="a615c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a615c-172">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="a615c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-173">Search-Flags</span></span>           | <span data-ttu-id="a615c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a615c-174">0x00000000</span></span>                                  |
| <span data-ttu-id="a615c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-175">System-Flags</span></span>           | <span data-ttu-id="a615c-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a615c-176">0x08000014</span></span>                                  |
| <span data-ttu-id="a615c-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a615c-177">Classes used in</span></span>        | [<span data-ttu-id="a615c-178">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a615c-178">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a615c-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="a615c-179">ADAM</span></span>



| <span data-ttu-id="a615c-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="a615c-180">Entry</span></span> | <span data-ttu-id="a615c-181">Value</span><span class="sxs-lookup"><span data-stu-id="a615c-181">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="a615c-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a615c-182">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a615c-183">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a615c-184">System-Only</span></span>            | <span data-ttu-id="a615c-185">True</span><span class="sxs-lookup"><span data-stu-id="a615c-185">True</span></span>                                        |
| <span data-ttu-id="a615c-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a615c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a615c-187">False</span><span class="sxs-lookup"><span data-stu-id="a615c-187">False</span></span>                                       |
| <span data-ttu-id="a615c-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a615c-188">Is Indexed</span></span>             | <span data-ttu-id="a615c-189">False</span><span class="sxs-lookup"><span data-stu-id="a615c-189">False</span></span>                                       |
| <span data-ttu-id="a615c-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a615c-190">In Global Catalog</span></span>      | <span data-ttu-id="a615c-191">False</span><span class="sxs-lookup"><span data-stu-id="a615c-191">False</span></span>                                       |
| <span data-ttu-id="a615c-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a615c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a615c-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a615c-193">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="a615c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a615c-194">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="a615c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a615c-195">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="a615c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-196">Search-Flags</span></span>           | <span data-ttu-id="a615c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a615c-197">0x00000000</span></span>                                  |
| <span data-ttu-id="a615c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-198">System-Flags</span></span>           | <span data-ttu-id="a615c-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a615c-199">0x08000014</span></span>                                  |
| <span data-ttu-id="a615c-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a615c-200">Classes used in</span></span>        | [<span data-ttu-id="a615c-201">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a615c-201">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a615c-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a615c-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a615c-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="a615c-203">Entry</span></span> | <span data-ttu-id="a615c-204">Value</span><span class="sxs-lookup"><span data-stu-id="a615c-204">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="a615c-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a615c-205">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a615c-206">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a615c-207">System-Only</span></span>            | <span data-ttu-id="a615c-208">True</span><span class="sxs-lookup"><span data-stu-id="a615c-208">True</span></span>                                        |
| <span data-ttu-id="a615c-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a615c-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a615c-210">False</span><span class="sxs-lookup"><span data-stu-id="a615c-210">False</span></span>                                       |
| <span data-ttu-id="a615c-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a615c-211">Is Indexed</span></span>             | <span data-ttu-id="a615c-212">False</span><span class="sxs-lookup"><span data-stu-id="a615c-212">False</span></span>                                       |
| <span data-ttu-id="a615c-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a615c-213">In Global Catalog</span></span>      | <span data-ttu-id="a615c-214">False</span><span class="sxs-lookup"><span data-stu-id="a615c-214">False</span></span>                                       |
| <span data-ttu-id="a615c-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a615c-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a615c-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a615c-216">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="a615c-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a615c-217">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="a615c-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a615c-218">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="a615c-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-219">Search-Flags</span></span>           | <span data-ttu-id="a615c-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a615c-220">0x00000000</span></span>                                  |
| <span data-ttu-id="a615c-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-221">System-Flags</span></span>           | <span data-ttu-id="a615c-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a615c-222">0x08000014</span></span>                                  |
| <span data-ttu-id="a615c-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a615c-223">Classes used in</span></span>        | [<span data-ttu-id="a615c-224">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a615c-224">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a615c-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a615c-225">Windows Server 2008</span></span>



| <span data-ttu-id="a615c-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="a615c-226">Entry</span></span> | <span data-ttu-id="a615c-227">Value</span><span class="sxs-lookup"><span data-stu-id="a615c-227">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="a615c-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a615c-228">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a615c-229">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a615c-230">System-Only</span></span>            | <span data-ttu-id="a615c-231">True</span><span class="sxs-lookup"><span data-stu-id="a615c-231">True</span></span>                                        |
| <span data-ttu-id="a615c-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a615c-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a615c-233">False</span><span class="sxs-lookup"><span data-stu-id="a615c-233">False</span></span>                                       |
| <span data-ttu-id="a615c-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a615c-234">Is Indexed</span></span>             | <span data-ttu-id="a615c-235">False</span><span class="sxs-lookup"><span data-stu-id="a615c-235">False</span></span>                                       |
| <span data-ttu-id="a615c-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a615c-236">In Global Catalog</span></span>      | <span data-ttu-id="a615c-237">False</span><span class="sxs-lookup"><span data-stu-id="a615c-237">False</span></span>                                       |
| <span data-ttu-id="a615c-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a615c-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a615c-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a615c-239">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="a615c-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a615c-240">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="a615c-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a615c-241">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="a615c-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-242">Search-Flags</span></span>           | <span data-ttu-id="a615c-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a615c-243">0x00000000</span></span>                                  |
| <span data-ttu-id="a615c-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-244">System-Flags</span></span>           | <span data-ttu-id="a615c-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a615c-245">0x08000014</span></span>                                  |
| <span data-ttu-id="a615c-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a615c-246">Classes used in</span></span>        | [<span data-ttu-id="a615c-247">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a615c-247">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a615c-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a615c-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a615c-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="a615c-249">Entry</span></span> | <span data-ttu-id="a615c-250">Value</span><span class="sxs-lookup"><span data-stu-id="a615c-250">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="a615c-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a615c-251">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a615c-252">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="a615c-253">System-Only</span></span>            | <span data-ttu-id="a615c-254">True</span><span class="sxs-lookup"><span data-stu-id="a615c-254">True</span></span>                                        |
| <span data-ttu-id="a615c-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a615c-255">Is-Single-Valued</span></span>       | <span data-ttu-id="a615c-256">False</span><span class="sxs-lookup"><span data-stu-id="a615c-256">False</span></span>                                       |
| <span data-ttu-id="a615c-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a615c-257">Is Indexed</span></span>             | <span data-ttu-id="a615c-258">False</span><span class="sxs-lookup"><span data-stu-id="a615c-258">False</span></span>                                       |
| <span data-ttu-id="a615c-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a615c-259">In Global Catalog</span></span>      | <span data-ttu-id="a615c-260">False</span><span class="sxs-lookup"><span data-stu-id="a615c-260">False</span></span>                                       |
| <span data-ttu-id="a615c-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a615c-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="a615c-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a615c-262">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="a615c-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a615c-263">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="a615c-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a615c-264">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="a615c-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-265">Search-Flags</span></span>           | <span data-ttu-id="a615c-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a615c-266">0x00000000</span></span>                                  |
| <span data-ttu-id="a615c-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-267">System-Flags</span></span>           | <span data-ttu-id="a615c-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a615c-268">0x08000014</span></span>                                  |
| <span data-ttu-id="a615c-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a615c-269">Classes used in</span></span>        | [<span data-ttu-id="a615c-270">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a615c-270">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a615c-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a615c-271">Windows Server 2012</span></span>



| <span data-ttu-id="a615c-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="a615c-272">Entry</span></span> | <span data-ttu-id="a615c-273">Value</span><span class="sxs-lookup"><span data-stu-id="a615c-273">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="a615c-274">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="a615c-274">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a615c-275">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="a615c-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="a615c-276">System-Only</span></span>            | <span data-ttu-id="a615c-277">True</span><span class="sxs-lookup"><span data-stu-id="a615c-277">True</span></span>                                        |
| <span data-ttu-id="a615c-278">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="a615c-278">Is-Single-Valued</span></span>       | <span data-ttu-id="a615c-279">False</span><span class="sxs-lookup"><span data-stu-id="a615c-279">False</span></span>                                       |
| <span data-ttu-id="a615c-280">Está indexado</span><span class="sxs-lookup"><span data-stu-id="a615c-280">Is Indexed</span></span>             | <span data-ttu-id="a615c-281">False</span><span class="sxs-lookup"><span data-stu-id="a615c-281">False</span></span>                                       |
| <span data-ttu-id="a615c-282">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="a615c-282">In Global Catalog</span></span>      | <span data-ttu-id="a615c-283">False</span><span class="sxs-lookup"><span data-stu-id="a615c-283">False</span></span>                                       |
| <span data-ttu-id="a615c-284">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="a615c-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="a615c-285">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a615c-285">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="a615c-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a615c-286">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="a615c-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a615c-287">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="a615c-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-288">Search-Flags</span></span>           | <span data-ttu-id="a615c-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a615c-289">0x00000000</span></span>                                  |
| <span data-ttu-id="a615c-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a615c-290">System-Flags</span></span>           | <span data-ttu-id="a615c-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a615c-291">0x08000014</span></span>                                  |
| <span data-ttu-id="a615c-292">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="a615c-292">Classes used in</span></span>        | [<span data-ttu-id="a615c-293">**Subesquema**</span><span class="sxs-lookup"><span data-stu-id="a615c-293">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 






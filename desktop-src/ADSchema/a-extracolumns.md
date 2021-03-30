---
title: Extra-Columns atributo)
description: Se trata de un atributo multivalor cuyos valores se componen de una tupla de 5 (nombre de atributo), (título de columna), (visibilidad predeterminada (0, 1)), (el ancho de columna (\ 8211; 1 para el ancho automático), 0 (reservado para uso futuro debe ser cero).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Extra-Columns
- atributo de extracolumns esquema de AD
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804435"
---
# <a name="extra-columns-attribute"></a><span data-ttu-id="871ed-105">Extra-Columns atributo)</span><span class="sxs-lookup"><span data-stu-id="871ed-105">Extra-Columns attribute</span></span>

<span data-ttu-id="871ed-106">Se trata de un atributo multivalor cuyos valores se componen de una tupla 5: (nombre de atributo), (título de columna), (visibilidad predeterminada (0, 1)), (ancho de columna (1 para ancho automático), 0 (reservado para uso futuro debe ser cero).</span><span class="sxs-lookup"><span data-stu-id="871ed-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="871ed-107">La consola usuarios y equipos de AD usa este valor.</span><span class="sxs-lookup"><span data-stu-id="871ed-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="871ed-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="871ed-108">Entry</span></span> | <span data-ttu-id="871ed-109">Value</span><span class="sxs-lookup"><span data-stu-id="871ed-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="871ed-110">CN</span><span class="sxs-lookup"><span data-stu-id="871ed-110">CN</span></span>                | <span data-ttu-id="871ed-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="871ed-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="871ed-112">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="871ed-112">Ldap-Display-Name</span></span> | <span data-ttu-id="871ed-113">extracolumns</span><span class="sxs-lookup"><span data-stu-id="871ed-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="871ed-114">Tamaño</span><span class="sxs-lookup"><span data-stu-id="871ed-114">Size</span></span>              | <span data-ttu-id="871ed-115">Cada valor sería el tamaño de la cadena de la tupla 5 anterior.</span><span class="sxs-lookup"><span data-stu-id="871ed-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="871ed-116">De forma predeterminada, habrá 22 valores en el objeto de visualización predeterminado en el contenedor DisplaySpecifier.</span><span class="sxs-lookup"><span data-stu-id="871ed-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="871ed-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="871ed-117">Update Privilege</span></span>  | <span data-ttu-id="871ed-118">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="871ed-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="871ed-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="871ed-119">Update Frequency</span></span>  | <span data-ttu-id="871ed-120">Solo se actualizará si se ha instalado un servicio como Exchange.</span><span class="sxs-lookup"><span data-stu-id="871ed-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="871ed-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="871ed-121">Attribute-Id</span></span>      | <span data-ttu-id="871ed-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="871ed-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="871ed-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="871ed-123">System-Id-Guid</span></span>    | <span data-ttu-id="871ed-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="871ed-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="871ed-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="871ed-125">Syntax</span></span>            | [<span data-ttu-id="871ed-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="871ed-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="871ed-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="871ed-127">Implementations</span></span>

-   [<span data-ttu-id="871ed-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="871ed-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="871ed-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="871ed-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="871ed-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="871ed-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="871ed-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="871ed-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="871ed-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="871ed-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="871ed-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="871ed-133">Windows Server 2003</span></span>



| <span data-ttu-id="871ed-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="871ed-134">Entry</span></span> | <span data-ttu-id="871ed-135">Value</span><span class="sxs-lookup"><span data-stu-id="871ed-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="871ed-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="871ed-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="871ed-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="871ed-138">System-Only</span></span>            | <span data-ttu-id="871ed-139">False</span><span class="sxs-lookup"><span data-stu-id="871ed-139">False</span></span>                                                      |
| <span data-ttu-id="871ed-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="871ed-140">Is-Single-Valued</span></span>       | <span data-ttu-id="871ed-141">False</span><span class="sxs-lookup"><span data-stu-id="871ed-141">False</span></span>                                                      |
| <span data-ttu-id="871ed-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="871ed-142">Is Indexed</span></span>             | <span data-ttu-id="871ed-143">False</span><span class="sxs-lookup"><span data-stu-id="871ed-143">False</span></span>                                                      |
| <span data-ttu-id="871ed-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="871ed-144">In Global Catalog</span></span>      | <span data-ttu-id="871ed-145">False</span><span class="sxs-lookup"><span data-stu-id="871ed-145">False</span></span>                                                      |
| <span data-ttu-id="871ed-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="871ed-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="871ed-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="871ed-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="871ed-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="871ed-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="871ed-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-150">Search-Flags</span></span>           | <span data-ttu-id="871ed-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="871ed-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="871ed-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-152">System-Flags</span></span>           | <span data-ttu-id="871ed-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="871ed-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="871ed-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="871ed-154">Classes used in</span></span>        | [<span data-ttu-id="871ed-155">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="871ed-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="871ed-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="871ed-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="871ed-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="871ed-157">Entry</span></span> | <span data-ttu-id="871ed-158">Value</span><span class="sxs-lookup"><span data-stu-id="871ed-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="871ed-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="871ed-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="871ed-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="871ed-161">System-Only</span></span>            | <span data-ttu-id="871ed-162">False</span><span class="sxs-lookup"><span data-stu-id="871ed-162">False</span></span>                                                      |
| <span data-ttu-id="871ed-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="871ed-163">Is-Single-Valued</span></span>       | <span data-ttu-id="871ed-164">False</span><span class="sxs-lookup"><span data-stu-id="871ed-164">False</span></span>                                                      |
| <span data-ttu-id="871ed-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="871ed-165">Is Indexed</span></span>             | <span data-ttu-id="871ed-166">False</span><span class="sxs-lookup"><span data-stu-id="871ed-166">False</span></span>                                                      |
| <span data-ttu-id="871ed-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="871ed-167">In Global Catalog</span></span>      | <span data-ttu-id="871ed-168">False</span><span class="sxs-lookup"><span data-stu-id="871ed-168">False</span></span>                                                      |
| <span data-ttu-id="871ed-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="871ed-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="871ed-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="871ed-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="871ed-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="871ed-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="871ed-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-173">Search-Flags</span></span>           | <span data-ttu-id="871ed-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="871ed-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="871ed-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-175">System-Flags</span></span>           | <span data-ttu-id="871ed-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="871ed-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="871ed-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="871ed-177">Classes used in</span></span>        | [<span data-ttu-id="871ed-178">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="871ed-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="871ed-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="871ed-179">Windows Server 2008</span></span>



| <span data-ttu-id="871ed-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="871ed-180">Entry</span></span> | <span data-ttu-id="871ed-181">Value</span><span class="sxs-lookup"><span data-stu-id="871ed-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="871ed-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="871ed-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="871ed-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="871ed-184">System-Only</span></span>            | <span data-ttu-id="871ed-185">False</span><span class="sxs-lookup"><span data-stu-id="871ed-185">False</span></span>                                                      |
| <span data-ttu-id="871ed-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="871ed-186">Is-Single-Valued</span></span>       | <span data-ttu-id="871ed-187">False</span><span class="sxs-lookup"><span data-stu-id="871ed-187">False</span></span>                                                      |
| <span data-ttu-id="871ed-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="871ed-188">Is Indexed</span></span>             | <span data-ttu-id="871ed-189">False</span><span class="sxs-lookup"><span data-stu-id="871ed-189">False</span></span>                                                      |
| <span data-ttu-id="871ed-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="871ed-190">In Global Catalog</span></span>      | <span data-ttu-id="871ed-191">False</span><span class="sxs-lookup"><span data-stu-id="871ed-191">False</span></span>                                                      |
| <span data-ttu-id="871ed-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="871ed-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="871ed-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="871ed-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="871ed-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="871ed-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="871ed-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-196">Search-Flags</span></span>           | <span data-ttu-id="871ed-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="871ed-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="871ed-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-198">System-Flags</span></span>           | <span data-ttu-id="871ed-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="871ed-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="871ed-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="871ed-200">Classes used in</span></span>        | [<span data-ttu-id="871ed-201">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="871ed-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="871ed-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="871ed-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="871ed-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="871ed-203">Entry</span></span> | <span data-ttu-id="871ed-204">Value</span><span class="sxs-lookup"><span data-stu-id="871ed-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="871ed-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="871ed-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="871ed-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="871ed-207">System-Only</span></span>            | <span data-ttu-id="871ed-208">False</span><span class="sxs-lookup"><span data-stu-id="871ed-208">False</span></span>                                                      |
| <span data-ttu-id="871ed-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="871ed-209">Is-Single-Valued</span></span>       | <span data-ttu-id="871ed-210">False</span><span class="sxs-lookup"><span data-stu-id="871ed-210">False</span></span>                                                      |
| <span data-ttu-id="871ed-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="871ed-211">Is Indexed</span></span>             | <span data-ttu-id="871ed-212">False</span><span class="sxs-lookup"><span data-stu-id="871ed-212">False</span></span>                                                      |
| <span data-ttu-id="871ed-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="871ed-213">In Global Catalog</span></span>      | <span data-ttu-id="871ed-214">False</span><span class="sxs-lookup"><span data-stu-id="871ed-214">False</span></span>                                                      |
| <span data-ttu-id="871ed-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="871ed-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="871ed-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="871ed-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="871ed-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="871ed-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="871ed-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-219">Search-Flags</span></span>           | <span data-ttu-id="871ed-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="871ed-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="871ed-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-221">System-Flags</span></span>           | <span data-ttu-id="871ed-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="871ed-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="871ed-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="871ed-223">Classes used in</span></span>        | [<span data-ttu-id="871ed-224">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="871ed-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="871ed-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="871ed-225">Windows Server 2012</span></span>



| <span data-ttu-id="871ed-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="871ed-226">Entry</span></span> | <span data-ttu-id="871ed-227">Value</span><span class="sxs-lookup"><span data-stu-id="871ed-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="871ed-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="871ed-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="871ed-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="871ed-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="871ed-230">System-Only</span></span>            | <span data-ttu-id="871ed-231">False</span><span class="sxs-lookup"><span data-stu-id="871ed-231">False</span></span>                                                      |
| <span data-ttu-id="871ed-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="871ed-232">Is-Single-Valued</span></span>       | <span data-ttu-id="871ed-233">False</span><span class="sxs-lookup"><span data-stu-id="871ed-233">False</span></span>                                                      |
| <span data-ttu-id="871ed-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="871ed-234">Is Indexed</span></span>             | <span data-ttu-id="871ed-235">False</span><span class="sxs-lookup"><span data-stu-id="871ed-235">False</span></span>                                                      |
| <span data-ttu-id="871ed-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="871ed-236">In Global Catalog</span></span>      | <span data-ttu-id="871ed-237">False</span><span class="sxs-lookup"><span data-stu-id="871ed-237">False</span></span>                                                      |
| <span data-ttu-id="871ed-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="871ed-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="871ed-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="871ed-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="871ed-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="871ed-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="871ed-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="871ed-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-242">Search-Flags</span></span>           | <span data-ttu-id="871ed-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="871ed-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="871ed-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="871ed-244">System-Flags</span></span>           | <span data-ttu-id="871ed-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="871ed-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="871ed-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="871ed-246">Classes used in</span></span>        | [<span data-ttu-id="871ed-247">**Display-Specifier**</span><span class="sxs-lookup"><span data-stu-id="871ed-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 






---
title: 'Entry: atributo TTL'
description: Este atributo operativo es mantenido por el servidor y parece estar presente en cada entrada dinámica.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Entry-TTL atributo AD Schema
- entryTTL esquema de AD de atributos
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493534"
---
# <a name="entry-ttl-attribute"></a><span data-ttu-id="4ec61-105">Entry: atributo TTL</span><span class="sxs-lookup"><span data-stu-id="4ec61-105">Entry-TTL attribute</span></span>

<span data-ttu-id="4ec61-106">Este atributo operativo es mantenido por el servidor y parece estar presente en cada entrada dinámica.</span><span class="sxs-lookup"><span data-stu-id="4ec61-106">This operational attribute is maintained by the server and appears to be present in every dynamic entry.</span></span> <span data-ttu-id="4ec61-107">El atributo no está presente cuando la entrada no contiene la clase de objeto dynamicObject.</span><span class="sxs-lookup"><span data-stu-id="4ec61-107">The attribute is not present when the entry does not contain the dynamicObject object class.</span></span> <span data-ttu-id="4ec61-108">El valor de este atributo es el tiempo, en segundos, que la entrada seguirá existiendo antes de que se desaparezca del directorio.</span><span class="sxs-lookup"><span data-stu-id="4ec61-108">The value of this attribute is the time, in seconds, that the entry will continue to exist before disappearing from the directory.</span></span> <span data-ttu-id="4ec61-109">En ausencia de operaciones de "actualización" intermedias, se garantiza que los valores devueltos al leer el atributo en dos búsquedas sucesivas no están en aumento.</span><span class="sxs-lookup"><span data-stu-id="4ec61-109">In the absence of intervening "refresh" operations, the values returned by reading the attribute in two successive searches are guaranteed to be nonincreasing.</span></span> <span data-ttu-id="4ec61-110">El valor mínimo permitido es 0, lo que indica que la entrada puede desaparecer sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="4ec61-110">The smallest permissible value is 0, indicating that the entry may disappear without warning.</span></span> <span data-ttu-id="4ec61-111">El atributo está marcado como NO MODIFICAble por el usuario porque solo se puede cambiar mediante la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="4ec61-111">The attribute is marked NO-USER-MODIFICATION because it may only be changed by using the refresh operation.</span></span>



| <span data-ttu-id="4ec61-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ec61-112">Entry</span></span> | <span data-ttu-id="4ec61-113">Value</span><span class="sxs-lookup"><span data-stu-id="4ec61-113">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4ec61-114">CN</span><span class="sxs-lookup"><span data-stu-id="4ec61-114">CN</span></span>                | <span data-ttu-id="4ec61-115">Entrada: TTL</span><span class="sxs-lookup"><span data-stu-id="4ec61-115">Entry-TTL</span></span>                                   |
| <span data-ttu-id="4ec61-116">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="4ec61-116">Ldap-Display-Name</span></span> | <span data-ttu-id="4ec61-117">entryTTL</span><span class="sxs-lookup"><span data-stu-id="4ec61-117">entryTTL</span></span>                                    |
| <span data-ttu-id="4ec61-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="4ec61-118">Size</span></span>              | <span data-ttu-id="4ec61-119">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="4ec61-119">4 bytes.</span></span> <span data-ttu-id="4ec61-120">Máximo = 1 año, valor predeterminado = 1 día.</span><span class="sxs-lookup"><span data-stu-id="4ec61-120">Maximum = 1 year, default = 1 day.</span></span> |
| <span data-ttu-id="4ec61-121">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="4ec61-121">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4ec61-122">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="4ec61-122">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4ec61-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4ec61-123">Attribute-Id</span></span>      | <span data-ttu-id="4ec61-124">1.3.6.1.4.1.1466.101.119.3</span><span class="sxs-lookup"><span data-stu-id="4ec61-124">1.3.6.1.4.1.1466.101.119.3</span></span>                  |
| <span data-ttu-id="4ec61-125">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4ec61-125">System-Id-Guid</span></span>    | <span data-ttu-id="4ec61-126">d213decc-d81a-4384-AAC2-dcfcfd631cf8</span><span class="sxs-lookup"><span data-stu-id="4ec61-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span></span>        |
| <span data-ttu-id="4ec61-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ec61-127">Syntax</span></span>            | [<span data-ttu-id="4ec61-128">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="4ec61-128">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="4ec61-129">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="4ec61-129">Implementations</span></span>

-   [<span data-ttu-id="4ec61-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4ec61-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4ec61-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4ec61-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4ec61-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4ec61-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4ec61-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4ec61-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4ec61-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4ec61-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4ec61-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4ec61-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4ec61-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ec61-136">Windows Server 2003</span></span>



| <span data-ttu-id="4ec61-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ec61-137">Entry</span></span> | <span data-ttu-id="4ec61-138">Value</span><span class="sxs-lookup"><span data-stu-id="4ec61-138">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4ec61-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4ec61-139">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ec61-140">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ec61-141">System-Only</span></span>            | <span data-ttu-id="4ec61-142">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-142">False</span></span>                                                |
| <span data-ttu-id="4ec61-143">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4ec61-143">Is-Single-Valued</span></span>       | <span data-ttu-id="4ec61-144">True</span><span class="sxs-lookup"><span data-stu-id="4ec61-144">True</span></span>                                                 |
| <span data-ttu-id="4ec61-145">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4ec61-145">Is Indexed</span></span>             | <span data-ttu-id="4ec61-146">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-146">False</span></span>                                                |
| <span data-ttu-id="4ec61-147">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ec61-147">In Global Catalog</span></span>      | <span data-ttu-id="4ec61-148">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-148">False</span></span>                                                |
| <span data-ttu-id="4ec61-149">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4ec61-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ec61-150">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4ec61-150">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4ec61-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ec61-151">Range-Lower</span></span>            | <span data-ttu-id="4ec61-152">0</span><span class="sxs-lookup"><span data-stu-id="4ec61-152">0</span></span>                                                    |
| <span data-ttu-id="4ec61-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ec61-153">Range-Upper</span></span>            | <span data-ttu-id="4ec61-154">31557600</span><span class="sxs-lookup"><span data-stu-id="4ec61-154">31557600</span></span>                                             |
| <span data-ttu-id="4ec61-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-155">Search-Flags</span></span>           | <span data-ttu-id="4ec61-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ec61-156">0x00000000</span></span>                                           |
| <span data-ttu-id="4ec61-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-157">System-Flags</span></span>           | <span data-ttu-id="4ec61-158">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4ec61-158">0x00000014</span></span>                                           |
| <span data-ttu-id="4ec61-159">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4ec61-159">Classes used in</span></span>        | [<span data-ttu-id="4ec61-160">**Objeto dinámico**</span><span class="sxs-lookup"><span data-stu-id="4ec61-160">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4ec61-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="4ec61-161">ADAM</span></span>



| <span data-ttu-id="4ec61-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ec61-162">Entry</span></span> | <span data-ttu-id="4ec61-163">Value</span><span class="sxs-lookup"><span data-stu-id="4ec61-163">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4ec61-164">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4ec61-164">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ec61-165">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ec61-166">System-Only</span></span>            | <span data-ttu-id="4ec61-167">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-167">False</span></span>                                                |
| <span data-ttu-id="4ec61-168">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4ec61-168">Is-Single-Valued</span></span>       | <span data-ttu-id="4ec61-169">True</span><span class="sxs-lookup"><span data-stu-id="4ec61-169">True</span></span>                                                 |
| <span data-ttu-id="4ec61-170">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4ec61-170">Is Indexed</span></span>             | <span data-ttu-id="4ec61-171">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-171">False</span></span>                                                |
| <span data-ttu-id="4ec61-172">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ec61-172">In Global Catalog</span></span>      | <span data-ttu-id="4ec61-173">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-173">False</span></span>                                                |
| <span data-ttu-id="4ec61-174">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4ec61-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ec61-175">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4ec61-175">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4ec61-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ec61-176">Range-Lower</span></span>            | <span data-ttu-id="4ec61-177">0</span><span class="sxs-lookup"><span data-stu-id="4ec61-177">0</span></span>                                                    |
| <span data-ttu-id="4ec61-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ec61-178">Range-Upper</span></span>            | <span data-ttu-id="4ec61-179">31557600</span><span class="sxs-lookup"><span data-stu-id="4ec61-179">31557600</span></span>                                             |
| <span data-ttu-id="4ec61-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-180">Search-Flags</span></span>           | <span data-ttu-id="4ec61-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ec61-181">0x00000000</span></span>                                           |
| <span data-ttu-id="4ec61-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-182">System-Flags</span></span>           | <span data-ttu-id="4ec61-183">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4ec61-183">0x00000014</span></span>                                           |
| <span data-ttu-id="4ec61-184">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4ec61-184">Classes used in</span></span>        | [<span data-ttu-id="4ec61-185">**Objeto dinámico**</span><span class="sxs-lookup"><span data-stu-id="4ec61-185">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4ec61-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4ec61-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4ec61-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ec61-187">Entry</span></span> | <span data-ttu-id="4ec61-188">Value</span><span class="sxs-lookup"><span data-stu-id="4ec61-188">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4ec61-189">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4ec61-189">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ec61-190">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ec61-191">System-Only</span></span>            | <span data-ttu-id="4ec61-192">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-192">False</span></span>                                                |
| <span data-ttu-id="4ec61-193">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4ec61-193">Is-Single-Valued</span></span>       | <span data-ttu-id="4ec61-194">True</span><span class="sxs-lookup"><span data-stu-id="4ec61-194">True</span></span>                                                 |
| <span data-ttu-id="4ec61-195">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4ec61-195">Is Indexed</span></span>             | <span data-ttu-id="4ec61-196">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-196">False</span></span>                                                |
| <span data-ttu-id="4ec61-197">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ec61-197">In Global Catalog</span></span>      | <span data-ttu-id="4ec61-198">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-198">False</span></span>                                                |
| <span data-ttu-id="4ec61-199">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4ec61-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ec61-200">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4ec61-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4ec61-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ec61-201">Range-Lower</span></span>            | <span data-ttu-id="4ec61-202">0</span><span class="sxs-lookup"><span data-stu-id="4ec61-202">0</span></span>                                                    |
| <span data-ttu-id="4ec61-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ec61-203">Range-Upper</span></span>            | <span data-ttu-id="4ec61-204">31557600</span><span class="sxs-lookup"><span data-stu-id="4ec61-204">31557600</span></span>                                             |
| <span data-ttu-id="4ec61-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-205">Search-Flags</span></span>           | <span data-ttu-id="4ec61-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ec61-206">0x00000000</span></span>                                           |
| <span data-ttu-id="4ec61-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-207">System-Flags</span></span>           | <span data-ttu-id="4ec61-208">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4ec61-208">0x00000014</span></span>                                           |
| <span data-ttu-id="4ec61-209">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4ec61-209">Classes used in</span></span>        | [<span data-ttu-id="4ec61-210">**Objeto dinámico**</span><span class="sxs-lookup"><span data-stu-id="4ec61-210">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4ec61-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ec61-211">Windows Server 2008</span></span>



| <span data-ttu-id="4ec61-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ec61-212">Entry</span></span> | <span data-ttu-id="4ec61-213">Value</span><span class="sxs-lookup"><span data-stu-id="4ec61-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4ec61-214">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4ec61-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ec61-215">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ec61-216">System-Only</span></span>            | <span data-ttu-id="4ec61-217">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-217">False</span></span>                                                |
| <span data-ttu-id="4ec61-218">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4ec61-218">Is-Single-Valued</span></span>       | <span data-ttu-id="4ec61-219">True</span><span class="sxs-lookup"><span data-stu-id="4ec61-219">True</span></span>                                                 |
| <span data-ttu-id="4ec61-220">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4ec61-220">Is Indexed</span></span>             | <span data-ttu-id="4ec61-221">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-221">False</span></span>                                                |
| <span data-ttu-id="4ec61-222">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ec61-222">In Global Catalog</span></span>      | <span data-ttu-id="4ec61-223">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-223">False</span></span>                                                |
| <span data-ttu-id="4ec61-224">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4ec61-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ec61-225">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4ec61-225">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4ec61-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ec61-226">Range-Lower</span></span>            | <span data-ttu-id="4ec61-227">0</span><span class="sxs-lookup"><span data-stu-id="4ec61-227">0</span></span>                                                    |
| <span data-ttu-id="4ec61-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ec61-228">Range-Upper</span></span>            | <span data-ttu-id="4ec61-229">31557600</span><span class="sxs-lookup"><span data-stu-id="4ec61-229">31557600</span></span>                                             |
| <span data-ttu-id="4ec61-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-230">Search-Flags</span></span>           | <span data-ttu-id="4ec61-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ec61-231">0x00000000</span></span>                                           |
| <span data-ttu-id="4ec61-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-232">System-Flags</span></span>           | <span data-ttu-id="4ec61-233">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4ec61-233">0x00000014</span></span>                                           |
| <span data-ttu-id="4ec61-234">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4ec61-234">Classes used in</span></span>        | [<span data-ttu-id="4ec61-235">**Objeto dinámico**</span><span class="sxs-lookup"><span data-stu-id="4ec61-235">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4ec61-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ec61-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4ec61-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ec61-237">Entry</span></span> | <span data-ttu-id="4ec61-238">Value</span><span class="sxs-lookup"><span data-stu-id="4ec61-238">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4ec61-239">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4ec61-239">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ec61-240">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ec61-241">System-Only</span></span>            | <span data-ttu-id="4ec61-242">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-242">False</span></span>                                                |
| <span data-ttu-id="4ec61-243">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4ec61-243">Is-Single-Valued</span></span>       | <span data-ttu-id="4ec61-244">True</span><span class="sxs-lookup"><span data-stu-id="4ec61-244">True</span></span>                                                 |
| <span data-ttu-id="4ec61-245">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4ec61-245">Is Indexed</span></span>             | <span data-ttu-id="4ec61-246">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-246">False</span></span>                                                |
| <span data-ttu-id="4ec61-247">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ec61-247">In Global Catalog</span></span>      | <span data-ttu-id="4ec61-248">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-248">False</span></span>                                                |
| <span data-ttu-id="4ec61-249">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4ec61-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ec61-250">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4ec61-250">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4ec61-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ec61-251">Range-Lower</span></span>            | <span data-ttu-id="4ec61-252">0</span><span class="sxs-lookup"><span data-stu-id="4ec61-252">0</span></span>                                                    |
| <span data-ttu-id="4ec61-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ec61-253">Range-Upper</span></span>            | <span data-ttu-id="4ec61-254">31557600</span><span class="sxs-lookup"><span data-stu-id="4ec61-254">31557600</span></span>                                             |
| <span data-ttu-id="4ec61-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-255">Search-Flags</span></span>           | <span data-ttu-id="4ec61-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ec61-256">0x00000000</span></span>                                           |
| <span data-ttu-id="4ec61-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-257">System-Flags</span></span>           | <span data-ttu-id="4ec61-258">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4ec61-258">0x00000014</span></span>                                           |
| <span data-ttu-id="4ec61-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4ec61-259">Classes used in</span></span>        | [<span data-ttu-id="4ec61-260">**Objeto dinámico**</span><span class="sxs-lookup"><span data-stu-id="4ec61-260">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4ec61-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ec61-261">Windows Server 2012</span></span>



| <span data-ttu-id="4ec61-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="4ec61-262">Entry</span></span> | <span data-ttu-id="4ec61-263">Value</span><span class="sxs-lookup"><span data-stu-id="4ec61-263">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4ec61-264">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="4ec61-264">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4ec61-265">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4ec61-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="4ec61-266">System-Only</span></span>            | <span data-ttu-id="4ec61-267">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-267">False</span></span>                                                |
| <span data-ttu-id="4ec61-268">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="4ec61-268">Is-Single-Valued</span></span>       | <span data-ttu-id="4ec61-269">True</span><span class="sxs-lookup"><span data-stu-id="4ec61-269">True</span></span>                                                 |
| <span data-ttu-id="4ec61-270">Está indexado</span><span class="sxs-lookup"><span data-stu-id="4ec61-270">Is Indexed</span></span>             | <span data-ttu-id="4ec61-271">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-271">False</span></span>                                                |
| <span data-ttu-id="4ec61-272">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="4ec61-272">In Global Catalog</span></span>      | <span data-ttu-id="4ec61-273">False</span><span class="sxs-lookup"><span data-stu-id="4ec61-273">False</span></span>                                                |
| <span data-ttu-id="4ec61-274">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="4ec61-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="4ec61-275">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4ec61-275">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4ec61-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4ec61-276">Range-Lower</span></span>            | <span data-ttu-id="4ec61-277">0</span><span class="sxs-lookup"><span data-stu-id="4ec61-277">0</span></span>                                                    |
| <span data-ttu-id="4ec61-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4ec61-278">Range-Upper</span></span>            | <span data-ttu-id="4ec61-279">31557600</span><span class="sxs-lookup"><span data-stu-id="4ec61-279">31557600</span></span>                                             |
| <span data-ttu-id="4ec61-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-280">Search-Flags</span></span>           | <span data-ttu-id="4ec61-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ec61-281">0x00000000</span></span>                                           |
| <span data-ttu-id="4ec61-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4ec61-282">System-Flags</span></span>           | <span data-ttu-id="4ec61-283">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4ec61-283">0x00000014</span></span>                                           |
| <span data-ttu-id="4ec61-284">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="4ec61-284">Classes used in</span></span>        | [<span data-ttu-id="4ec61-285">**Objeto dinámico**</span><span class="sxs-lookup"><span data-stu-id="4ec61-285">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 






---
title: atributo MS-DS-UpdateScript
description: Se usa para contener el script con las instrucciones de reestructuración del dominio.
ms.assetid: a9dd205d-f6c3-4eeb-95dc-491bfe30ab8b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-UpdateScript
- Esquema de AD de atributo msDS-UpdateScript
topic_type:
- apiref
api_name:
- ms-DS-UpdateScript
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7809bf6fdbaabb38976068d1998cacfb12bdaf3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659101"
---
# <a name="ms-ds-updatescript-attribute"></a><span data-ttu-id="b6468-105">atributo MS-DS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="b6468-105">ms-DS-UpdateScript attribute</span></span>

<span data-ttu-id="b6468-106">Se usa para contener el script con las instrucciones de reestructuración del dominio.</span><span class="sxs-lookup"><span data-stu-id="b6468-106">This is used to hold the script with the domain restructure instructions.</span></span>



| <span data-ttu-id="b6468-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b6468-107">Entry</span></span> | <span data-ttu-id="b6468-108">Value</span><span class="sxs-lookup"><span data-stu-id="b6468-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b6468-109">CN</span><span class="sxs-lookup"><span data-stu-id="b6468-109">CN</span></span>                | <span data-ttu-id="b6468-110">MS-DS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="b6468-110">ms-DS-UpdateScript</span></span>                          |
| <span data-ttu-id="b6468-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="b6468-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b6468-112">msDS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="b6468-112">msDS-UpdateScript</span></span>                           |
| <span data-ttu-id="b6468-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b6468-113">Size</span></span>              | <span data-ttu-id="b6468-114">Tamaño máximo de 10 000 bytes.</span><span class="sxs-lookup"><span data-stu-id="b6468-114">Maximum size 10K bytes.</span></span>                     |
| <span data-ttu-id="b6468-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="b6468-115">Update Privilege</span></span>  | <span data-ttu-id="b6468-116">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="b6468-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="b6468-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="b6468-117">Update Frequency</span></span>  | <span data-ttu-id="b6468-118">Solo durante la reestructuración de dominios.</span><span class="sxs-lookup"><span data-stu-id="b6468-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="b6468-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b6468-119">Attribute-Id</span></span>      | <span data-ttu-id="b6468-120">1.2.840.113556.1.4.1721</span><span class="sxs-lookup"><span data-stu-id="b6468-120">1.2.840.113556.1.4.1721</span></span>                     |
| <span data-ttu-id="b6468-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b6468-121">System-Id-Guid</span></span>    | <span data-ttu-id="b6468-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span><span class="sxs-lookup"><span data-stu-id="b6468-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span></span>        |
| <span data-ttu-id="b6468-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6468-123">Syntax</span></span>            | [<span data-ttu-id="b6468-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b6468-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b6468-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b6468-125">Implementations</span></span>

-   [<span data-ttu-id="b6468-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b6468-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b6468-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b6468-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b6468-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b6468-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b6468-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b6468-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b6468-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b6468-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b6468-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b6468-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b6468-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6468-132">Windows Server 2003</span></span>



| <span data-ttu-id="b6468-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="b6468-133">Entry</span></span> | <span data-ttu-id="b6468-134">Value</span><span class="sxs-lookup"><span data-stu-id="b6468-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b6468-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b6468-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6468-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6468-137">System-Only</span></span>            | <span data-ttu-id="b6468-138">False</span><span class="sxs-lookup"><span data-stu-id="b6468-138">False</span></span>                                                         |
| <span data-ttu-id="b6468-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b6468-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b6468-140">True</span><span class="sxs-lookup"><span data-stu-id="b6468-140">True</span></span>                                                          |
| <span data-ttu-id="b6468-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b6468-141">Is Indexed</span></span>             | <span data-ttu-id="b6468-142">False</span><span class="sxs-lookup"><span data-stu-id="b6468-142">False</span></span>                                                         |
| <span data-ttu-id="b6468-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b6468-143">In Global Catalog</span></span>      | <span data-ttu-id="b6468-144">False</span><span class="sxs-lookup"><span data-stu-id="b6468-144">False</span></span>                                                         |
| <span data-ttu-id="b6468-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b6468-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6468-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6468-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b6468-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6468-147">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6468-148">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-149">Search-Flags</span></span>           | <span data-ttu-id="b6468-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6468-150">0x00000000</span></span>                                                    |
| <span data-ttu-id="b6468-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-151">System-Flags</span></span>           | <span data-ttu-id="b6468-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6468-152">0x00000010</span></span>                                                    |
| <span data-ttu-id="b6468-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b6468-153">Classes used in</span></span>        | [<span data-ttu-id="b6468-154">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="b6468-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b6468-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="b6468-155">ADAM</span></span>



| <span data-ttu-id="b6468-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="b6468-156">Entry</span></span> | <span data-ttu-id="b6468-157">Value</span><span class="sxs-lookup"><span data-stu-id="b6468-157">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b6468-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b6468-158">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6468-159">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6468-160">System-Only</span></span>            | <span data-ttu-id="b6468-161">False</span><span class="sxs-lookup"><span data-stu-id="b6468-161">False</span></span>                                                         |
| <span data-ttu-id="b6468-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b6468-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b6468-163">True</span><span class="sxs-lookup"><span data-stu-id="b6468-163">True</span></span>                                                          |
| <span data-ttu-id="b6468-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b6468-164">Is Indexed</span></span>             | <span data-ttu-id="b6468-165">False</span><span class="sxs-lookup"><span data-stu-id="b6468-165">False</span></span>                                                         |
| <span data-ttu-id="b6468-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b6468-166">In Global Catalog</span></span>      | <span data-ttu-id="b6468-167">False</span><span class="sxs-lookup"><span data-stu-id="b6468-167">False</span></span>                                                         |
| <span data-ttu-id="b6468-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b6468-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6468-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6468-169">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b6468-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6468-170">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6468-171">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-172">Search-Flags</span></span>           | <span data-ttu-id="b6468-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6468-173">0x00000000</span></span>                                                    |
| <span data-ttu-id="b6468-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-174">System-Flags</span></span>           | <span data-ttu-id="b6468-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6468-175">0x00000010</span></span>                                                    |
| <span data-ttu-id="b6468-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b6468-176">Classes used in</span></span>        | [<span data-ttu-id="b6468-177">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="b6468-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b6468-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b6468-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b6468-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="b6468-179">Entry</span></span> | <span data-ttu-id="b6468-180">Value</span><span class="sxs-lookup"><span data-stu-id="b6468-180">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b6468-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b6468-181">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6468-182">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6468-183">System-Only</span></span>            | <span data-ttu-id="b6468-184">False</span><span class="sxs-lookup"><span data-stu-id="b6468-184">False</span></span>                                                         |
| <span data-ttu-id="b6468-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b6468-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b6468-186">True</span><span class="sxs-lookup"><span data-stu-id="b6468-186">True</span></span>                                                          |
| <span data-ttu-id="b6468-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b6468-187">Is Indexed</span></span>             | <span data-ttu-id="b6468-188">False</span><span class="sxs-lookup"><span data-stu-id="b6468-188">False</span></span>                                                         |
| <span data-ttu-id="b6468-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b6468-189">In Global Catalog</span></span>      | <span data-ttu-id="b6468-190">False</span><span class="sxs-lookup"><span data-stu-id="b6468-190">False</span></span>                                                         |
| <span data-ttu-id="b6468-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b6468-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6468-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6468-192">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b6468-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6468-193">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6468-194">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-195">Search-Flags</span></span>           | <span data-ttu-id="b6468-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6468-196">0x00000000</span></span>                                                    |
| <span data-ttu-id="b6468-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-197">System-Flags</span></span>           | <span data-ttu-id="b6468-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6468-198">0x00000010</span></span>                                                    |
| <span data-ttu-id="b6468-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b6468-199">Classes used in</span></span>        | [<span data-ttu-id="b6468-200">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="b6468-200">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b6468-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6468-201">Windows Server 2008</span></span>



| <span data-ttu-id="b6468-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="b6468-202">Entry</span></span> | <span data-ttu-id="b6468-203">Value</span><span class="sxs-lookup"><span data-stu-id="b6468-203">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b6468-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b6468-204">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6468-205">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6468-206">System-Only</span></span>            | <span data-ttu-id="b6468-207">False</span><span class="sxs-lookup"><span data-stu-id="b6468-207">False</span></span>                                                         |
| <span data-ttu-id="b6468-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b6468-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b6468-209">True</span><span class="sxs-lookup"><span data-stu-id="b6468-209">True</span></span>                                                          |
| <span data-ttu-id="b6468-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b6468-210">Is Indexed</span></span>             | <span data-ttu-id="b6468-211">False</span><span class="sxs-lookup"><span data-stu-id="b6468-211">False</span></span>                                                         |
| <span data-ttu-id="b6468-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b6468-212">In Global Catalog</span></span>      | <span data-ttu-id="b6468-213">False</span><span class="sxs-lookup"><span data-stu-id="b6468-213">False</span></span>                                                         |
| <span data-ttu-id="b6468-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b6468-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6468-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6468-215">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b6468-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6468-216">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6468-217">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-218">Search-Flags</span></span>           | <span data-ttu-id="b6468-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6468-219">0x00000000</span></span>                                                    |
| <span data-ttu-id="b6468-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-220">System-Flags</span></span>           | <span data-ttu-id="b6468-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6468-221">0x00000010</span></span>                                                    |
| <span data-ttu-id="b6468-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b6468-222">Classes used in</span></span>        | [<span data-ttu-id="b6468-223">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="b6468-223">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b6468-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b6468-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b6468-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="b6468-225">Entry</span></span> | <span data-ttu-id="b6468-226">Value</span><span class="sxs-lookup"><span data-stu-id="b6468-226">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b6468-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b6468-227">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6468-228">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6468-229">System-Only</span></span>            | <span data-ttu-id="b6468-230">False</span><span class="sxs-lookup"><span data-stu-id="b6468-230">False</span></span>                                                         |
| <span data-ttu-id="b6468-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b6468-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b6468-232">True</span><span class="sxs-lookup"><span data-stu-id="b6468-232">True</span></span>                                                          |
| <span data-ttu-id="b6468-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b6468-233">Is Indexed</span></span>             | <span data-ttu-id="b6468-234">False</span><span class="sxs-lookup"><span data-stu-id="b6468-234">False</span></span>                                                         |
| <span data-ttu-id="b6468-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b6468-235">In Global Catalog</span></span>      | <span data-ttu-id="b6468-236">False</span><span class="sxs-lookup"><span data-stu-id="b6468-236">False</span></span>                                                         |
| <span data-ttu-id="b6468-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b6468-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6468-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6468-238">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b6468-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6468-239">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6468-240">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-241">Search-Flags</span></span>           | <span data-ttu-id="b6468-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6468-242">0x00000000</span></span>                                                    |
| <span data-ttu-id="b6468-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-243">System-Flags</span></span>           | <span data-ttu-id="b6468-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6468-244">0x00000010</span></span>                                                    |
| <span data-ttu-id="b6468-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b6468-245">Classes used in</span></span>        | [<span data-ttu-id="b6468-246">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="b6468-246">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b6468-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6468-247">Windows Server 2012</span></span>



| <span data-ttu-id="b6468-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="b6468-248">Entry</span></span> | <span data-ttu-id="b6468-249">Value</span><span class="sxs-lookup"><span data-stu-id="b6468-249">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b6468-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="b6468-250">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6468-251">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="b6468-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6468-252">System-Only</span></span>            | <span data-ttu-id="b6468-253">False</span><span class="sxs-lookup"><span data-stu-id="b6468-253">False</span></span>                                                         |
| <span data-ttu-id="b6468-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="b6468-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b6468-255">True</span><span class="sxs-lookup"><span data-stu-id="b6468-255">True</span></span>                                                          |
| <span data-ttu-id="b6468-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="b6468-256">Is Indexed</span></span>             | <span data-ttu-id="b6468-257">False</span><span class="sxs-lookup"><span data-stu-id="b6468-257">False</span></span>                                                         |
| <span data-ttu-id="b6468-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="b6468-258">In Global Catalog</span></span>      | <span data-ttu-id="b6468-259">False</span><span class="sxs-lookup"><span data-stu-id="b6468-259">False</span></span>                                                         |
| <span data-ttu-id="b6468-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="b6468-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6468-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6468-261">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="b6468-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6468-262">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6468-263">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="b6468-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-264">Search-Flags</span></span>           | <span data-ttu-id="b6468-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6468-265">0x00000000</span></span>                                                    |
| <span data-ttu-id="b6468-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6468-266">System-Flags</span></span>           | <span data-ttu-id="b6468-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6468-267">0x00000010</span></span>                                                    |
| <span data-ttu-id="b6468-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="b6468-268">Classes used in</span></span>        | [<span data-ttu-id="b6468-269">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="b6468-269">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 






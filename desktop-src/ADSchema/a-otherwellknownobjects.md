---
title: Otro atributo de objetos conocidos
description: Contiene una lista de contenedores por GUID y nombre distintivo. Esto permite recuperar un objeto una vez que se ha desusado usando solo el GUID y el nombre de dominio. Cada vez que se mueve el objeto, el sistema actualiza automáticamente el nombre distintivo.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- 'Otro: esquema de AD de atributos de objetos conocidos'
- otherWellKnownObjects esquema de AD de atributos
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493954"
---
# <a name="other-well-known-objects-attribute"></a><span data-ttu-id="26b64-107">Otro atributo de objetos conocidos</span><span class="sxs-lookup"><span data-stu-id="26b64-107">Other-Well-Known-Objects attribute</span></span>

<span data-ttu-id="26b64-108">Contiene una lista de contenedores por GUID y nombre distintivo.</span><span class="sxs-lookup"><span data-stu-id="26b64-108">Contains a list of containers by GUID and Distinguished Name.</span></span> <span data-ttu-id="26b64-109">Esto permite recuperar un objeto una vez que se ha desusado usando solo el GUID y el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="26b64-109">This permits retrieving an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="26b64-110">Cada vez que se mueve el objeto, el sistema actualiza automáticamente el nombre distintivo.</span><span class="sxs-lookup"><span data-stu-id="26b64-110">Whenever the object is moved, the system automatically updates the Distinguished Name.</span></span>



| <span data-ttu-id="26b64-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b64-111">Entry</span></span> | <span data-ttu-id="26b64-112">Value</span><span class="sxs-lookup"><span data-stu-id="26b64-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26b64-113">CN</span><span class="sxs-lookup"><span data-stu-id="26b64-113">CN</span></span>                | <span data-ttu-id="26b64-114">Otros objetos conocidos</span><span class="sxs-lookup"><span data-stu-id="26b64-114">Other-Well-Known-Objects</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="26b64-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="26b64-115">Ldap-Display-Name</span></span> | <span data-ttu-id="26b64-116">otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="26b64-116">otherWellKnownObjects</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="26b64-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="26b64-117">Size</span></span>              | <span data-ttu-id="26b64-118">Ejemplo para recuperar el contenedor de usuarios en el dominio de Microsoft: LDAP://(WKGUID = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com).</span><span class="sxs-lookup"><span data-stu-id="26b64-118">Sample for retrieving the Users container in the microsoft domain: LDAP://(WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=microsoft,dc=com).</span></span> <span data-ttu-id="26b64-119">Nota: los corchetes angulares se sustituyen por paréntesis para evitar conflictos XML.</span><span class="sxs-lookup"><span data-stu-id="26b64-119">NOTE: Angle brackets replaced by parentheses to avoid XML conflicts.</span></span> |
| <span data-ttu-id="26b64-120">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="26b64-120">Update Privilege</span></span>  | <span data-ttu-id="26b64-121">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="26b64-121">Schema administrator</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="26b64-122">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="26b64-122">Update Frequency</span></span>  | <span data-ttu-id="26b64-123">Cada vez que se mueve el objeto.</span><span class="sxs-lookup"><span data-stu-id="26b64-123">Whenever the object is moved.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="26b64-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="26b64-124">Attribute-Id</span></span>      | <span data-ttu-id="26b64-125">1.2.840.113556.1.4.1359</span><span class="sxs-lookup"><span data-stu-id="26b64-125">1.2.840.113556.1.4.1359</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="26b64-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="26b64-126">System-Id-Guid</span></span>    | <span data-ttu-id="26b64-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="26b64-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span></span>                                                                                                                                                                          |
| <span data-ttu-id="26b64-128">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26b64-128">Syntax</span></span>            | [<span data-ttu-id="26b64-129">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="26b64-129">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                               |



## <a name="implementations"></a><span data-ttu-id="26b64-130">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="26b64-130">Implementations</span></span>

-   [<span data-ttu-id="26b64-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="26b64-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="26b64-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="26b64-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="26b64-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="26b64-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="26b64-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="26b64-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="26b64-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="26b64-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="26b64-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="26b64-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="26b64-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="26b64-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="26b64-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26b64-138">Windows 2000 Server</span></span>



| <span data-ttu-id="26b64-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b64-139">Entry</span></span> | <span data-ttu-id="26b64-140">Value</span><span class="sxs-lookup"><span data-stu-id="26b64-140">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26b64-141">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="26b64-141">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26b64-142">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="26b64-143">System-Only</span></span>            | <span data-ttu-id="26b64-144">False</span><span class="sxs-lookup"><span data-stu-id="26b64-144">False</span></span>                           |
| <span data-ttu-id="26b64-145">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="26b64-145">Is-Single-Valued</span></span>       | <span data-ttu-id="26b64-146">False</span><span class="sxs-lookup"><span data-stu-id="26b64-146">False</span></span>                           |
| <span data-ttu-id="26b64-147">Está indexado</span><span class="sxs-lookup"><span data-stu-id="26b64-147">Is Indexed</span></span>             | <span data-ttu-id="26b64-148">False</span><span class="sxs-lookup"><span data-stu-id="26b64-148">False</span></span>                           |
| <span data-ttu-id="26b64-149">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="26b64-149">In Global Catalog</span></span>      | <span data-ttu-id="26b64-150">False</span><span class="sxs-lookup"><span data-stu-id="26b64-150">False</span></span>                           |
| <span data-ttu-id="26b64-151">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="26b64-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="26b64-152">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26b64-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26b64-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26b64-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="26b64-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26b64-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="26b64-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-155">Search-Flags</span></span>           | <span data-ttu-id="26b64-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26b64-156">0x00000000</span></span>                      |
| <span data-ttu-id="26b64-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-157">System-Flags</span></span>           | <span data-ttu-id="26b64-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26b64-158">0x00000010</span></span>                      |
| <span data-ttu-id="26b64-159">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="26b64-159">Classes used in</span></span>        | [<span data-ttu-id="26b64-160">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="26b64-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="26b64-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26b64-161">Windows Server 2003</span></span>



| <span data-ttu-id="26b64-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b64-162">Entry</span></span> | <span data-ttu-id="26b64-163">Value</span><span class="sxs-lookup"><span data-stu-id="26b64-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26b64-164">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="26b64-164">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26b64-165">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="26b64-166">System-Only</span></span>            | <span data-ttu-id="26b64-167">False</span><span class="sxs-lookup"><span data-stu-id="26b64-167">False</span></span>                           |
| <span data-ttu-id="26b64-168">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="26b64-168">Is-Single-Valued</span></span>       | <span data-ttu-id="26b64-169">False</span><span class="sxs-lookup"><span data-stu-id="26b64-169">False</span></span>                           |
| <span data-ttu-id="26b64-170">Está indexado</span><span class="sxs-lookup"><span data-stu-id="26b64-170">Is Indexed</span></span>             | <span data-ttu-id="26b64-171">False</span><span class="sxs-lookup"><span data-stu-id="26b64-171">False</span></span>                           |
| <span data-ttu-id="26b64-172">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="26b64-172">In Global Catalog</span></span>      | <span data-ttu-id="26b64-173">False</span><span class="sxs-lookup"><span data-stu-id="26b64-173">False</span></span>                           |
| <span data-ttu-id="26b64-174">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="26b64-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="26b64-175">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26b64-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26b64-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26b64-176">Range-Lower</span></span>            | <span data-ttu-id="26b64-177">16</span><span class="sxs-lookup"><span data-stu-id="26b64-177">16</span></span>                              |
| <span data-ttu-id="26b64-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26b64-178">Range-Upper</span></span>            | <span data-ttu-id="26b64-179">16</span><span class="sxs-lookup"><span data-stu-id="26b64-179">16</span></span>                              |
| <span data-ttu-id="26b64-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-180">Search-Flags</span></span>           | <span data-ttu-id="26b64-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26b64-181">0x00000000</span></span>                      |
| <span data-ttu-id="26b64-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-182">System-Flags</span></span>           | <span data-ttu-id="26b64-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26b64-183">0x00000010</span></span>                      |
| <span data-ttu-id="26b64-184">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="26b64-184">Classes used in</span></span>        | [<span data-ttu-id="26b64-185">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="26b64-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="26b64-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="26b64-186">ADAM</span></span>



| <span data-ttu-id="26b64-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b64-187">Entry</span></span> | <span data-ttu-id="26b64-188">Value</span><span class="sxs-lookup"><span data-stu-id="26b64-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26b64-189">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="26b64-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26b64-190">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="26b64-191">System-Only</span></span>            | <span data-ttu-id="26b64-192">False</span><span class="sxs-lookup"><span data-stu-id="26b64-192">False</span></span>                           |
| <span data-ttu-id="26b64-193">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="26b64-193">Is-Single-Valued</span></span>       | <span data-ttu-id="26b64-194">False</span><span class="sxs-lookup"><span data-stu-id="26b64-194">False</span></span>                           |
| <span data-ttu-id="26b64-195">Está indexado</span><span class="sxs-lookup"><span data-stu-id="26b64-195">Is Indexed</span></span>             | <span data-ttu-id="26b64-196">False</span><span class="sxs-lookup"><span data-stu-id="26b64-196">False</span></span>                           |
| <span data-ttu-id="26b64-197">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="26b64-197">In Global Catalog</span></span>      | <span data-ttu-id="26b64-198">False</span><span class="sxs-lookup"><span data-stu-id="26b64-198">False</span></span>                           |
| <span data-ttu-id="26b64-199">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="26b64-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="26b64-200">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26b64-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26b64-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26b64-201">Range-Lower</span></span>            | <span data-ttu-id="26b64-202">16</span><span class="sxs-lookup"><span data-stu-id="26b64-202">16</span></span>                              |
| <span data-ttu-id="26b64-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26b64-203">Range-Upper</span></span>            | <span data-ttu-id="26b64-204">16</span><span class="sxs-lookup"><span data-stu-id="26b64-204">16</span></span>                              |
| <span data-ttu-id="26b64-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-205">Search-Flags</span></span>           | <span data-ttu-id="26b64-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26b64-206">0x00000000</span></span>                      |
| <span data-ttu-id="26b64-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-207">System-Flags</span></span>           | <span data-ttu-id="26b64-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26b64-208">0x00000010</span></span>                      |
| <span data-ttu-id="26b64-209">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="26b64-209">Classes used in</span></span>        | [<span data-ttu-id="26b64-210">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="26b64-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="26b64-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="26b64-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="26b64-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b64-212">Entry</span></span> | <span data-ttu-id="26b64-213">Value</span><span class="sxs-lookup"><span data-stu-id="26b64-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26b64-214">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="26b64-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26b64-215">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="26b64-216">System-Only</span></span>            | <span data-ttu-id="26b64-217">False</span><span class="sxs-lookup"><span data-stu-id="26b64-217">False</span></span>                           |
| <span data-ttu-id="26b64-218">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="26b64-218">Is-Single-Valued</span></span>       | <span data-ttu-id="26b64-219">False</span><span class="sxs-lookup"><span data-stu-id="26b64-219">False</span></span>                           |
| <span data-ttu-id="26b64-220">Está indexado</span><span class="sxs-lookup"><span data-stu-id="26b64-220">Is Indexed</span></span>             | <span data-ttu-id="26b64-221">False</span><span class="sxs-lookup"><span data-stu-id="26b64-221">False</span></span>                           |
| <span data-ttu-id="26b64-222">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="26b64-222">In Global Catalog</span></span>      | <span data-ttu-id="26b64-223">False</span><span class="sxs-lookup"><span data-stu-id="26b64-223">False</span></span>                           |
| <span data-ttu-id="26b64-224">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="26b64-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="26b64-225">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26b64-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26b64-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26b64-226">Range-Lower</span></span>            | <span data-ttu-id="26b64-227">16</span><span class="sxs-lookup"><span data-stu-id="26b64-227">16</span></span>                              |
| <span data-ttu-id="26b64-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26b64-228">Range-Upper</span></span>            | <span data-ttu-id="26b64-229">16</span><span class="sxs-lookup"><span data-stu-id="26b64-229">16</span></span>                              |
| <span data-ttu-id="26b64-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-230">Search-Flags</span></span>           | <span data-ttu-id="26b64-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26b64-231">0x00000000</span></span>                      |
| <span data-ttu-id="26b64-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-232">System-Flags</span></span>           | <span data-ttu-id="26b64-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26b64-233">0x00000010</span></span>                      |
| <span data-ttu-id="26b64-234">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="26b64-234">Classes used in</span></span>        | [<span data-ttu-id="26b64-235">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="26b64-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="26b64-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26b64-236">Windows Server 2008</span></span>



| <span data-ttu-id="26b64-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b64-237">Entry</span></span> | <span data-ttu-id="26b64-238">Value</span><span class="sxs-lookup"><span data-stu-id="26b64-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26b64-239">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="26b64-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26b64-240">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="26b64-241">System-Only</span></span>            | <span data-ttu-id="26b64-242">False</span><span class="sxs-lookup"><span data-stu-id="26b64-242">False</span></span>                           |
| <span data-ttu-id="26b64-243">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="26b64-243">Is-Single-Valued</span></span>       | <span data-ttu-id="26b64-244">False</span><span class="sxs-lookup"><span data-stu-id="26b64-244">False</span></span>                           |
| <span data-ttu-id="26b64-245">Está indexado</span><span class="sxs-lookup"><span data-stu-id="26b64-245">Is Indexed</span></span>             | <span data-ttu-id="26b64-246">False</span><span class="sxs-lookup"><span data-stu-id="26b64-246">False</span></span>                           |
| <span data-ttu-id="26b64-247">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="26b64-247">In Global Catalog</span></span>      | <span data-ttu-id="26b64-248">False</span><span class="sxs-lookup"><span data-stu-id="26b64-248">False</span></span>                           |
| <span data-ttu-id="26b64-249">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="26b64-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="26b64-250">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26b64-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26b64-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26b64-251">Range-Lower</span></span>            | <span data-ttu-id="26b64-252">16</span><span class="sxs-lookup"><span data-stu-id="26b64-252">16</span></span>                              |
| <span data-ttu-id="26b64-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26b64-253">Range-Upper</span></span>            | <span data-ttu-id="26b64-254">16</span><span class="sxs-lookup"><span data-stu-id="26b64-254">16</span></span>                              |
| <span data-ttu-id="26b64-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-255">Search-Flags</span></span>           | <span data-ttu-id="26b64-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26b64-256">0x00000000</span></span>                      |
| <span data-ttu-id="26b64-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-257">System-Flags</span></span>           | <span data-ttu-id="26b64-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26b64-258">0x00000010</span></span>                      |
| <span data-ttu-id="26b64-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="26b64-259">Classes used in</span></span>        | [<span data-ttu-id="26b64-260">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="26b64-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="26b64-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26b64-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="26b64-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b64-262">Entry</span></span> | <span data-ttu-id="26b64-263">Value</span><span class="sxs-lookup"><span data-stu-id="26b64-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26b64-264">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="26b64-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26b64-265">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="26b64-266">System-Only</span></span>            | <span data-ttu-id="26b64-267">False</span><span class="sxs-lookup"><span data-stu-id="26b64-267">False</span></span>                           |
| <span data-ttu-id="26b64-268">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="26b64-268">Is-Single-Valued</span></span>       | <span data-ttu-id="26b64-269">False</span><span class="sxs-lookup"><span data-stu-id="26b64-269">False</span></span>                           |
| <span data-ttu-id="26b64-270">Está indexado</span><span class="sxs-lookup"><span data-stu-id="26b64-270">Is Indexed</span></span>             | <span data-ttu-id="26b64-271">False</span><span class="sxs-lookup"><span data-stu-id="26b64-271">False</span></span>                           |
| <span data-ttu-id="26b64-272">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="26b64-272">In Global Catalog</span></span>      | <span data-ttu-id="26b64-273">False</span><span class="sxs-lookup"><span data-stu-id="26b64-273">False</span></span>                           |
| <span data-ttu-id="26b64-274">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="26b64-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="26b64-275">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26b64-275">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26b64-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26b64-276">Range-Lower</span></span>            | <span data-ttu-id="26b64-277">16</span><span class="sxs-lookup"><span data-stu-id="26b64-277">16</span></span>                              |
| <span data-ttu-id="26b64-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26b64-278">Range-Upper</span></span>            | <span data-ttu-id="26b64-279">16</span><span class="sxs-lookup"><span data-stu-id="26b64-279">16</span></span>                              |
| <span data-ttu-id="26b64-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-280">Search-Flags</span></span>           | <span data-ttu-id="26b64-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26b64-281">0x00000000</span></span>                      |
| <span data-ttu-id="26b64-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-282">System-Flags</span></span>           | <span data-ttu-id="26b64-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26b64-283">0x00000010</span></span>                      |
| <span data-ttu-id="26b64-284">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="26b64-284">Classes used in</span></span>        | [<span data-ttu-id="26b64-285">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="26b64-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="26b64-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26b64-286">Windows Server 2012</span></span>



| <span data-ttu-id="26b64-287">Entrada</span><span class="sxs-lookup"><span data-stu-id="26b64-287">Entry</span></span> | <span data-ttu-id="26b64-288">Value</span><span class="sxs-lookup"><span data-stu-id="26b64-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="26b64-289">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="26b64-289">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-290">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26b64-290">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="26b64-291">System-Only</span><span class="sxs-lookup"><span data-stu-id="26b64-291">System-Only</span></span>            | <span data-ttu-id="26b64-292">False</span><span class="sxs-lookup"><span data-stu-id="26b64-292">False</span></span>                           |
| <span data-ttu-id="26b64-293">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="26b64-293">Is-Single-Valued</span></span>       | <span data-ttu-id="26b64-294">False</span><span class="sxs-lookup"><span data-stu-id="26b64-294">False</span></span>                           |
| <span data-ttu-id="26b64-295">Está indexado</span><span class="sxs-lookup"><span data-stu-id="26b64-295">Is Indexed</span></span>             | <span data-ttu-id="26b64-296">False</span><span class="sxs-lookup"><span data-stu-id="26b64-296">False</span></span>                           |
| <span data-ttu-id="26b64-297">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="26b64-297">In Global Catalog</span></span>      | <span data-ttu-id="26b64-298">False</span><span class="sxs-lookup"><span data-stu-id="26b64-298">False</span></span>                           |
| <span data-ttu-id="26b64-299">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="26b64-299">NT-Security-Descriptor</span></span> | <span data-ttu-id="26b64-300">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="26b64-300">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="26b64-301">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26b64-301">Range-Lower</span></span>            | <span data-ttu-id="26b64-302">16</span><span class="sxs-lookup"><span data-stu-id="26b64-302">16</span></span>                              |
| <span data-ttu-id="26b64-303">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26b64-303">Range-Upper</span></span>            | <span data-ttu-id="26b64-304">16</span><span class="sxs-lookup"><span data-stu-id="26b64-304">16</span></span>                              |
| <span data-ttu-id="26b64-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-305">Search-Flags</span></span>           | <span data-ttu-id="26b64-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26b64-306">0x00000000</span></span>                      |
| <span data-ttu-id="26b64-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26b64-307">System-Flags</span></span>           | <span data-ttu-id="26b64-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26b64-308">0x00000010</span></span>                      |
| <span data-ttu-id="26b64-309">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="26b64-309">Classes used in</span></span>        | [<span data-ttu-id="26b64-310">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="26b64-310">**Top**</span></span>](c-top.md)<br/> |



 

 






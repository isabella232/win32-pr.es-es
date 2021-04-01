---
title: atributo MS-DS-Settings
description: Se utiliza para almacenar la configuración de un objeto. Su uso está determinado únicamente por el propietario del objeto. Se recomienda usarlo para almacenar pares de nombre/valor. Por ejemplo, color azul.
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Settings
- atributo msDS-Settings esquema de AD
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f466bd5aa5a904482ff9c84c1f818c12205f69c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906018"
---
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="1f198-108">atributo MS-DS-Settings</span><span class="sxs-lookup"><span data-stu-id="1f198-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="1f198-109">Se utiliza para almacenar la configuración de un objeto.</span><span class="sxs-lookup"><span data-stu-id="1f198-109">Used to store settings for an object.</span></span> <span data-ttu-id="1f198-110">Su uso está determinado únicamente por el propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="1f198-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="1f198-111">Se recomienda usarlo para almacenar pares de nombre/valor.</span><span class="sxs-lookup"><span data-stu-id="1f198-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="1f198-112">Por ejemplo, color = Blue.</span><span class="sxs-lookup"><span data-stu-id="1f198-112">For example, color=blue.</span></span>



| <span data-ttu-id="1f198-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f198-113">Entry</span></span> | <span data-ttu-id="1f198-114">Value</span><span class="sxs-lookup"><span data-stu-id="1f198-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1f198-115">CN</span><span class="sxs-lookup"><span data-stu-id="1f198-115">CN</span></span>                | <span data-ttu-id="1f198-116">Configuración de MS-DS</span><span class="sxs-lookup"><span data-stu-id="1f198-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="1f198-117">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1f198-117">Ldap-Display-Name</span></span> | <span data-ttu-id="1f198-118">msDS-Settings</span><span class="sxs-lookup"><span data-stu-id="1f198-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="1f198-119">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1f198-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="1f198-120">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1f198-120">Update Privilege</span></span>  | <span data-ttu-id="1f198-121">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="1f198-121">Domain administrator</span></span>                        |
| <span data-ttu-id="1f198-122">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1f198-122">Update Frequency</span></span>  | <span data-ttu-id="1f198-123">Cada vez que cambian los valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="1f198-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="1f198-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1f198-124">Attribute-Id</span></span>      | <span data-ttu-id="1f198-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="1f198-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="1f198-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1f198-126">System-Id-Guid</span></span>    | <span data-ttu-id="1f198-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="1f198-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="1f198-128">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f198-128">Syntax</span></span>            | [<span data-ttu-id="1f198-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1f198-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1f198-130">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1f198-130">Implementations</span></span>

-   [<span data-ttu-id="1f198-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1f198-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1f198-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1f198-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1f198-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1f198-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1f198-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1f198-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1f198-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1f198-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1f198-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1f198-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1f198-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f198-137">Windows Server 2003</span></span>



| <span data-ttu-id="1f198-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f198-138">Entry</span></span> | <span data-ttu-id="1f198-139">Value</span><span class="sxs-lookup"><span data-stu-id="1f198-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f198-140">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1f198-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f198-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f198-142">System-Only</span></span>            | <span data-ttu-id="1f198-143">False</span><span class="sxs-lookup"><span data-stu-id="1f198-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-144">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1f198-144">Is-Single-Valued</span></span>       | <span data-ttu-id="1f198-145">False</span><span class="sxs-lookup"><span data-stu-id="1f198-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-146">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1f198-146">Is Indexed</span></span>             | <span data-ttu-id="1f198-147">False</span><span class="sxs-lookup"><span data-stu-id="1f198-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-148">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1f198-148">In Global Catalog</span></span>      | <span data-ttu-id="1f198-149">False</span><span class="sxs-lookup"><span data-stu-id="1f198-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-150">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1f198-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f198-151">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f198-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="1f198-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f198-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f198-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-154">Search-Flags</span></span>           | <span data-ttu-id="1f198-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-156">System-Flags</span></span>           | <span data-ttu-id="1f198-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-158">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1f198-158">Classes used in</span></span>        | [<span data-ttu-id="1f198-159">**Configuración de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="1f198-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="1f198-160">**Punto de conexión**</span><span class="sxs-lookup"><span data-stu-id="1f198-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1f198-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="1f198-161">ADAM</span></span>



| <span data-ttu-id="1f198-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f198-162">Entry</span></span> | <span data-ttu-id="1f198-163">Value</span><span class="sxs-lookup"><span data-stu-id="1f198-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f198-164">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1f198-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f198-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f198-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f198-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f198-166">System-Only</span></span>            | <span data-ttu-id="1f198-167">False</span><span class="sxs-lookup"><span data-stu-id="1f198-167">False</span></span>                                                            |
| <span data-ttu-id="1f198-168">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1f198-168">Is-Single-Valued</span></span>       | <span data-ttu-id="1f198-169">False</span><span class="sxs-lookup"><span data-stu-id="1f198-169">False</span></span>                                                            |
| <span data-ttu-id="1f198-170">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1f198-170">Is Indexed</span></span>             | <span data-ttu-id="1f198-171">False</span><span class="sxs-lookup"><span data-stu-id="1f198-171">False</span></span>                                                            |
| <span data-ttu-id="1f198-172">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1f198-172">In Global Catalog</span></span>      | <span data-ttu-id="1f198-173">False</span><span class="sxs-lookup"><span data-stu-id="1f198-173">False</span></span>                                                            |
| <span data-ttu-id="1f198-174">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1f198-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f198-175">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f198-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f198-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f198-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="1f198-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f198-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="1f198-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-178">Search-Flags</span></span>           | <span data-ttu-id="1f198-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f198-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-180">System-Flags</span></span>           | <span data-ttu-id="1f198-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f198-182">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1f198-182">Classes used in</span></span>        | [<span data-ttu-id="1f198-183">**Configuración de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="1f198-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1f198-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1f198-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1f198-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f198-185">Entry</span></span> | <span data-ttu-id="1f198-186">Value</span><span class="sxs-lookup"><span data-stu-id="1f198-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f198-187">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1f198-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f198-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f198-189">System-Only</span></span>            | <span data-ttu-id="1f198-190">False</span><span class="sxs-lookup"><span data-stu-id="1f198-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-191">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1f198-191">Is-Single-Valued</span></span>       | <span data-ttu-id="1f198-192">False</span><span class="sxs-lookup"><span data-stu-id="1f198-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-193">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1f198-193">Is Indexed</span></span>             | <span data-ttu-id="1f198-194">False</span><span class="sxs-lookup"><span data-stu-id="1f198-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-195">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1f198-195">In Global Catalog</span></span>      | <span data-ttu-id="1f198-196">False</span><span class="sxs-lookup"><span data-stu-id="1f198-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-197">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1f198-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f198-198">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f198-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="1f198-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f198-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f198-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-201">Search-Flags</span></span>           | <span data-ttu-id="1f198-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-203">System-Flags</span></span>           | <span data-ttu-id="1f198-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1f198-205">Classes used in</span></span>        | [<span data-ttu-id="1f198-206">**Configuración de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="1f198-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="1f198-207">**Punto de conexión**</span><span class="sxs-lookup"><span data-stu-id="1f198-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1f198-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f198-208">Windows Server 2008</span></span>



| <span data-ttu-id="1f198-209">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f198-209">Entry</span></span> | <span data-ttu-id="1f198-210">Value</span><span class="sxs-lookup"><span data-stu-id="1f198-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f198-211">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1f198-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f198-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f198-213">System-Only</span></span>            | <span data-ttu-id="1f198-214">False</span><span class="sxs-lookup"><span data-stu-id="1f198-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-215">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1f198-215">Is-Single-Valued</span></span>       | <span data-ttu-id="1f198-216">False</span><span class="sxs-lookup"><span data-stu-id="1f198-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-217">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1f198-217">Is Indexed</span></span>             | <span data-ttu-id="1f198-218">False</span><span class="sxs-lookup"><span data-stu-id="1f198-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-219">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1f198-219">In Global Catalog</span></span>      | <span data-ttu-id="1f198-220">False</span><span class="sxs-lookup"><span data-stu-id="1f198-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-221">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1f198-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f198-222">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f198-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="1f198-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f198-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f198-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-225">Search-Flags</span></span>           | <span data-ttu-id="1f198-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-227">System-Flags</span></span>           | <span data-ttu-id="1f198-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1f198-229">Classes used in</span></span>        | [<span data-ttu-id="1f198-230">**Configuración de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="1f198-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="1f198-231">**Punto de conexión**</span><span class="sxs-lookup"><span data-stu-id="1f198-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1f198-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1f198-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1f198-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f198-233">Entry</span></span> | <span data-ttu-id="1f198-234">Value</span><span class="sxs-lookup"><span data-stu-id="1f198-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f198-235">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1f198-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f198-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f198-237">System-Only</span></span>            | <span data-ttu-id="1f198-238">False</span><span class="sxs-lookup"><span data-stu-id="1f198-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-239">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1f198-239">Is-Single-Valued</span></span>       | <span data-ttu-id="1f198-240">False</span><span class="sxs-lookup"><span data-stu-id="1f198-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-241">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1f198-241">Is Indexed</span></span>             | <span data-ttu-id="1f198-242">False</span><span class="sxs-lookup"><span data-stu-id="1f198-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-243">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1f198-243">In Global Catalog</span></span>      | <span data-ttu-id="1f198-244">False</span><span class="sxs-lookup"><span data-stu-id="1f198-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-245">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1f198-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f198-246">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f198-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="1f198-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f198-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f198-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-249">Search-Flags</span></span>           | <span data-ttu-id="1f198-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-251">System-Flags</span></span>           | <span data-ttu-id="1f198-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-253">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1f198-253">Classes used in</span></span>        | [<span data-ttu-id="1f198-254">**Configuración de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="1f198-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="1f198-255">**Punto de conexión**</span><span class="sxs-lookup"><span data-stu-id="1f198-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1f198-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f198-256">Windows Server 2012</span></span>



| <span data-ttu-id="1f198-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="1f198-257">Entry</span></span> | <span data-ttu-id="1f198-258">Value</span><span class="sxs-lookup"><span data-stu-id="1f198-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f198-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1f198-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f198-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="1f198-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f198-261">System-Only</span></span>            | <span data-ttu-id="1f198-262">False</span><span class="sxs-lookup"><span data-stu-id="1f198-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1f198-263">Is-Single-Valued</span></span>       | <span data-ttu-id="1f198-264">False</span><span class="sxs-lookup"><span data-stu-id="1f198-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1f198-265">Is Indexed</span></span>             | <span data-ttu-id="1f198-266">False</span><span class="sxs-lookup"><span data-stu-id="1f198-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1f198-267">In Global Catalog</span></span>      | <span data-ttu-id="1f198-268">False</span><span class="sxs-lookup"><span data-stu-id="1f198-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="1f198-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1f198-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f198-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f198-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="1f198-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f198-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f198-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="1f198-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-273">Search-Flags</span></span>           | <span data-ttu-id="1f198-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f198-275">System-Flags</span></span>           | <span data-ttu-id="1f198-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f198-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="1f198-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1f198-277">Classes used in</span></span>        | [<span data-ttu-id="1f198-278">**Configuración de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="1f198-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="1f198-279">**Punto de conexión**</span><span class="sxs-lookup"><span data-stu-id="1f198-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 






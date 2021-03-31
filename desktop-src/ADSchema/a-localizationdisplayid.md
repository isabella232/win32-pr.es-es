---
title: 'Localization: display-ID (atributo)'
description: Se usa para indexar en el archivo Extrts.mc para obtener el displayName adaptado para los objetos con fines de interfaz de usuario.
ms.assetid: ed99d499-0064-4832-81ad-75fb3c8c548d
ms.tgt_platform: multiple
keywords:
- 'Localization: Schema de identificador de pantalla esquema de AD'
- localizationDisplayId esquema de AD de atributos
topic_type:
- apiref
api_name:
- Localization-Display-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4d9453b04bd5c944784b68ff5e4442f00bf65f5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804753"
---
# <a name="localization-display-id-attribute"></a><span data-ttu-id="1764c-105">Localization: display-ID (atributo)</span><span class="sxs-lookup"><span data-stu-id="1764c-105">Localization-Display-Id attribute</span></span>

<span data-ttu-id="1764c-106">Se usa para indexar en el archivo Extrts.mc para obtener el displayName adaptado para los objetos con fines de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1764c-106">Used to index into the file Extrts.mc to get the localized displayName for the objects for UI purposes.</span></span>



| <span data-ttu-id="1764c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1764c-107">Entry</span></span> | <span data-ttu-id="1764c-108">Value</span><span class="sxs-lookup"><span data-stu-id="1764c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1764c-109">CN</span><span class="sxs-lookup"><span data-stu-id="1764c-109">CN</span></span>                | <span data-ttu-id="1764c-110">Localización: ID. de presentación</span><span class="sxs-lookup"><span data-stu-id="1764c-110">Localization-Display-Id</span></span>              |
| <span data-ttu-id="1764c-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1764c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1764c-112">localizationDisplayId</span><span class="sxs-lookup"><span data-stu-id="1764c-112">localizationDisplayId</span></span>                |
| <span data-ttu-id="1764c-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1764c-113">Size</span></span>              | <span data-ttu-id="1764c-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="1764c-114">4 bytes</span></span>                              |
| <span data-ttu-id="1764c-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1764c-115">Update Privilege</span></span>  | <span data-ttu-id="1764c-116">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="1764c-116">Schema administrator</span></span>                 |
| <span data-ttu-id="1764c-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1764c-117">Update Frequency</span></span>  | <span data-ttu-id="1764c-118">Un identificador nunca debe cambiarse.</span><span class="sxs-lookup"><span data-stu-id="1764c-118">An ID should never be changed.</span></span>       |
| <span data-ttu-id="1764c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1764c-119">Attribute-Id</span></span>      | <span data-ttu-id="1764c-120">1.2.840.113556.1.4.1353</span><span class="sxs-lookup"><span data-stu-id="1764c-120">1.2.840.113556.1.4.1353</span></span>              |
| <span data-ttu-id="1764c-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1764c-121">System-Id-Guid</span></span>    | <span data-ttu-id="1764c-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="1764c-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span></span> |
| <span data-ttu-id="1764c-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1764c-123">Syntax</span></span>            | [<span data-ttu-id="1764c-124">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="1764c-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1764c-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1764c-125">Implementations</span></span>

-   [<span data-ttu-id="1764c-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1764c-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1764c-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1764c-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1764c-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1764c-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1764c-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1764c-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1764c-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1764c-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1764c-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1764c-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1764c-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1764c-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1764c-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1764c-133">Windows 2000 Server</span></span>



| <span data-ttu-id="1764c-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="1764c-134">Entry</span></span> | <span data-ttu-id="1764c-135">Value</span><span class="sxs-lookup"><span data-stu-id="1764c-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1764c-136">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1764c-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1764c-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="1764c-138">System-Only</span></span>            | <span data-ttu-id="1764c-139">False</span><span class="sxs-lookup"><span data-stu-id="1764c-139">False</span></span>                                                           |
| <span data-ttu-id="1764c-140">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1764c-140">Is-Single-Valued</span></span>       | <span data-ttu-id="1764c-141">True</span><span class="sxs-lookup"><span data-stu-id="1764c-141">True</span></span>                                                            |
| <span data-ttu-id="1764c-142">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1764c-142">Is Indexed</span></span>             | <span data-ttu-id="1764c-143">False</span><span class="sxs-lookup"><span data-stu-id="1764c-143">False</span></span>                                                           |
| <span data-ttu-id="1764c-144">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1764c-144">In Global Catalog</span></span>      | <span data-ttu-id="1764c-145">False</span><span class="sxs-lookup"><span data-stu-id="1764c-145">False</span></span>                                                           |
| <span data-ttu-id="1764c-146">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1764c-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="1764c-147">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1764c-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1764c-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1764c-148">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1764c-149">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-150">Search-Flags</span></span>           | <span data-ttu-id="1764c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1764c-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="1764c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-152">System-Flags</span></span>           | <span data-ttu-id="1764c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1764c-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="1764c-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1764c-154">Classes used in</span></span>        | [<span data-ttu-id="1764c-155">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="1764c-155">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1764c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1764c-156">Windows Server 2003</span></span>



| <span data-ttu-id="1764c-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="1764c-157">Entry</span></span> | <span data-ttu-id="1764c-158">Value</span><span class="sxs-lookup"><span data-stu-id="1764c-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1764c-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1764c-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1764c-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="1764c-161">System-Only</span></span>            | <span data-ttu-id="1764c-162">False</span><span class="sxs-lookup"><span data-stu-id="1764c-162">False</span></span>                                                           |
| <span data-ttu-id="1764c-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1764c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="1764c-164">True</span><span class="sxs-lookup"><span data-stu-id="1764c-164">True</span></span>                                                            |
| <span data-ttu-id="1764c-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1764c-165">Is Indexed</span></span>             | <span data-ttu-id="1764c-166">False</span><span class="sxs-lookup"><span data-stu-id="1764c-166">False</span></span>                                                           |
| <span data-ttu-id="1764c-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1764c-167">In Global Catalog</span></span>      | <span data-ttu-id="1764c-168">False</span><span class="sxs-lookup"><span data-stu-id="1764c-168">False</span></span>                                                           |
| <span data-ttu-id="1764c-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1764c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="1764c-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1764c-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1764c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1764c-171">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1764c-172">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-173">Search-Flags</span></span>           | <span data-ttu-id="1764c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1764c-174">0x00000000</span></span>                                                      |
| <span data-ttu-id="1764c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-175">System-Flags</span></span>           | <span data-ttu-id="1764c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1764c-176">0x00000010</span></span>                                                      |
| <span data-ttu-id="1764c-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1764c-177">Classes used in</span></span>        | [<span data-ttu-id="1764c-178">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="1764c-178">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1764c-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="1764c-179">ADAM</span></span>



| <span data-ttu-id="1764c-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="1764c-180">Entry</span></span> | <span data-ttu-id="1764c-181">Value</span><span class="sxs-lookup"><span data-stu-id="1764c-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1764c-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1764c-182">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1764c-183">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="1764c-184">System-Only</span></span>            | <span data-ttu-id="1764c-185">False</span><span class="sxs-lookup"><span data-stu-id="1764c-185">False</span></span>                                                           |
| <span data-ttu-id="1764c-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1764c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="1764c-187">True</span><span class="sxs-lookup"><span data-stu-id="1764c-187">True</span></span>                                                            |
| <span data-ttu-id="1764c-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1764c-188">Is Indexed</span></span>             | <span data-ttu-id="1764c-189">False</span><span class="sxs-lookup"><span data-stu-id="1764c-189">False</span></span>                                                           |
| <span data-ttu-id="1764c-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1764c-190">In Global Catalog</span></span>      | <span data-ttu-id="1764c-191">False</span><span class="sxs-lookup"><span data-stu-id="1764c-191">False</span></span>                                                           |
| <span data-ttu-id="1764c-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1764c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="1764c-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1764c-193">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1764c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1764c-194">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1764c-195">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-196">Search-Flags</span></span>           | <span data-ttu-id="1764c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1764c-197">0x00000000</span></span>                                                      |
| <span data-ttu-id="1764c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-198">System-Flags</span></span>           | <span data-ttu-id="1764c-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1764c-199">0x00000010</span></span>                                                      |
| <span data-ttu-id="1764c-200">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1764c-200">Classes used in</span></span>        | [<span data-ttu-id="1764c-201">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="1764c-201">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1764c-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1764c-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1764c-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="1764c-203">Entry</span></span> | <span data-ttu-id="1764c-204">Value</span><span class="sxs-lookup"><span data-stu-id="1764c-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1764c-205">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1764c-205">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1764c-206">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="1764c-207">System-Only</span></span>            | <span data-ttu-id="1764c-208">False</span><span class="sxs-lookup"><span data-stu-id="1764c-208">False</span></span>                                                           |
| <span data-ttu-id="1764c-209">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1764c-209">Is-Single-Valued</span></span>       | <span data-ttu-id="1764c-210">True</span><span class="sxs-lookup"><span data-stu-id="1764c-210">True</span></span>                                                            |
| <span data-ttu-id="1764c-211">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1764c-211">Is Indexed</span></span>             | <span data-ttu-id="1764c-212">False</span><span class="sxs-lookup"><span data-stu-id="1764c-212">False</span></span>                                                           |
| <span data-ttu-id="1764c-213">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1764c-213">In Global Catalog</span></span>      | <span data-ttu-id="1764c-214">False</span><span class="sxs-lookup"><span data-stu-id="1764c-214">False</span></span>                                                           |
| <span data-ttu-id="1764c-215">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1764c-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="1764c-216">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1764c-216">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1764c-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1764c-217">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1764c-218">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-219">Search-Flags</span></span>           | <span data-ttu-id="1764c-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1764c-220">0x00000000</span></span>                                                      |
| <span data-ttu-id="1764c-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-221">System-Flags</span></span>           | <span data-ttu-id="1764c-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1764c-222">0x00000010</span></span>                                                      |
| <span data-ttu-id="1764c-223">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1764c-223">Classes used in</span></span>        | [<span data-ttu-id="1764c-224">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="1764c-224">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1764c-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1764c-225">Windows Server 2008</span></span>



| <span data-ttu-id="1764c-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="1764c-226">Entry</span></span> | <span data-ttu-id="1764c-227">Value</span><span class="sxs-lookup"><span data-stu-id="1764c-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1764c-228">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1764c-228">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1764c-229">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="1764c-230">System-Only</span></span>            | <span data-ttu-id="1764c-231">False</span><span class="sxs-lookup"><span data-stu-id="1764c-231">False</span></span>                                                           |
| <span data-ttu-id="1764c-232">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1764c-232">Is-Single-Valued</span></span>       | <span data-ttu-id="1764c-233">True</span><span class="sxs-lookup"><span data-stu-id="1764c-233">True</span></span>                                                            |
| <span data-ttu-id="1764c-234">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1764c-234">Is Indexed</span></span>             | <span data-ttu-id="1764c-235">False</span><span class="sxs-lookup"><span data-stu-id="1764c-235">False</span></span>                                                           |
| <span data-ttu-id="1764c-236">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1764c-236">In Global Catalog</span></span>      | <span data-ttu-id="1764c-237">False</span><span class="sxs-lookup"><span data-stu-id="1764c-237">False</span></span>                                                           |
| <span data-ttu-id="1764c-238">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1764c-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="1764c-239">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1764c-239">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1764c-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1764c-240">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1764c-241">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-242">Search-Flags</span></span>           | <span data-ttu-id="1764c-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1764c-243">0x00000000</span></span>                                                      |
| <span data-ttu-id="1764c-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-244">System-Flags</span></span>           | <span data-ttu-id="1764c-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1764c-245">0x00000010</span></span>                                                      |
| <span data-ttu-id="1764c-246">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1764c-246">Classes used in</span></span>        | [<span data-ttu-id="1764c-247">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="1764c-247">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1764c-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1764c-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1764c-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="1764c-249">Entry</span></span> | <span data-ttu-id="1764c-250">Value</span><span class="sxs-lookup"><span data-stu-id="1764c-250">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1764c-251">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1764c-251">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1764c-252">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="1764c-253">System-Only</span></span>            | <span data-ttu-id="1764c-254">False</span><span class="sxs-lookup"><span data-stu-id="1764c-254">False</span></span>                                                           |
| <span data-ttu-id="1764c-255">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1764c-255">Is-Single-Valued</span></span>       | <span data-ttu-id="1764c-256">True</span><span class="sxs-lookup"><span data-stu-id="1764c-256">True</span></span>                                                            |
| <span data-ttu-id="1764c-257">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1764c-257">Is Indexed</span></span>             | <span data-ttu-id="1764c-258">False</span><span class="sxs-lookup"><span data-stu-id="1764c-258">False</span></span>                                                           |
| <span data-ttu-id="1764c-259">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1764c-259">In Global Catalog</span></span>      | <span data-ttu-id="1764c-260">False</span><span class="sxs-lookup"><span data-stu-id="1764c-260">False</span></span>                                                           |
| <span data-ttu-id="1764c-261">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1764c-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="1764c-262">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1764c-262">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1764c-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1764c-263">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1764c-264">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-265">Search-Flags</span></span>           | <span data-ttu-id="1764c-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1764c-266">0x00000000</span></span>                                                      |
| <span data-ttu-id="1764c-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-267">System-Flags</span></span>           | <span data-ttu-id="1764c-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1764c-268">0x00000010</span></span>                                                      |
| <span data-ttu-id="1764c-269">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1764c-269">Classes used in</span></span>        | [<span data-ttu-id="1764c-270">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="1764c-270">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1764c-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1764c-271">Windows Server 2012</span></span>



| <span data-ttu-id="1764c-272">Entrada</span><span class="sxs-lookup"><span data-stu-id="1764c-272">Entry</span></span> | <span data-ttu-id="1764c-273">Value</span><span class="sxs-lookup"><span data-stu-id="1764c-273">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1764c-274">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1764c-274">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1764c-275">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1764c-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="1764c-276">System-Only</span></span>            | <span data-ttu-id="1764c-277">False</span><span class="sxs-lookup"><span data-stu-id="1764c-277">False</span></span>                                                           |
| <span data-ttu-id="1764c-278">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1764c-278">Is-Single-Valued</span></span>       | <span data-ttu-id="1764c-279">True</span><span class="sxs-lookup"><span data-stu-id="1764c-279">True</span></span>                                                            |
| <span data-ttu-id="1764c-280">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1764c-280">Is Indexed</span></span>             | <span data-ttu-id="1764c-281">False</span><span class="sxs-lookup"><span data-stu-id="1764c-281">False</span></span>                                                           |
| <span data-ttu-id="1764c-282">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1764c-282">In Global Catalog</span></span>      | <span data-ttu-id="1764c-283">False</span><span class="sxs-lookup"><span data-stu-id="1764c-283">False</span></span>                                                           |
| <span data-ttu-id="1764c-284">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1764c-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="1764c-285">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1764c-285">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1764c-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1764c-286">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1764c-287">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="1764c-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-288">Search-Flags</span></span>           | <span data-ttu-id="1764c-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1764c-289">0x00000000</span></span>                                                      |
| <span data-ttu-id="1764c-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1764c-290">System-Flags</span></span>           | <span data-ttu-id="1764c-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1764c-291">0x00000010</span></span>                                                      |
| <span data-ttu-id="1764c-292">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1764c-292">Classes used in</span></span>        | [<span data-ttu-id="1764c-293">**Control-acceso-derecha**</span><span class="sxs-lookup"><span data-stu-id="1764c-293">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 






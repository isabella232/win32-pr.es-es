---
title: Atributo de nombre de entidad de seguridad de servicio
description: Lista de nombres de entidad de seguridad utilizados para la autenticación mutua con una instancia de un servicio en este equipo.
ms.assetid: 0ad1694f-0d6f-4350-a088-fdf3ef798c46
ms.tgt_platform: multiple
keywords:
- 'Nombre de la entidad de seguridad de servicio: esquema de AD'
- Esquema de AD del atributo servicePrincipalName
topic_type:
- apiref
api_name:
- Service-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 861f160d2c9b71d2c9914c7ff9c2ea0ee43c8528
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658737"
---
# <a name="service-principal-name-attribute"></a><span data-ttu-id="9122d-105">Atributo de nombre de entidad de seguridad de servicio</span><span class="sxs-lookup"><span data-stu-id="9122d-105">Service-Principal-Name attribute</span></span>

<span data-ttu-id="9122d-106">Lista de nombres de entidad de seguridad utilizados para la autenticación mutua con una instancia de un servicio en este equipo.</span><span class="sxs-lookup"><span data-stu-id="9122d-106">List of principal names used for mutual authentication with an instance of a service on this computer.</span></span>



| <span data-ttu-id="9122d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9122d-107">Entry</span></span> | <span data-ttu-id="9122d-108">Value</span><span class="sxs-lookup"><span data-stu-id="9122d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9122d-109">CN</span><span class="sxs-lookup"><span data-stu-id="9122d-109">CN</span></span>                | <span data-ttu-id="9122d-110">Nombre de entidad de seguridad de servicio</span><span class="sxs-lookup"><span data-stu-id="9122d-110">Service-Principal-Name</span></span>                      |
| <span data-ttu-id="9122d-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="9122d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9122d-112">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9122d-112">servicePrincipalName</span></span>                        |
| <span data-ttu-id="9122d-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9122d-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9122d-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="9122d-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9122d-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="9122d-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9122d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9122d-116">Attribute-Id</span></span>      | <span data-ttu-id="9122d-117">1.2.840.113556.1.4.771</span><span class="sxs-lookup"><span data-stu-id="9122d-117">1.2.840.113556.1.4.771</span></span>                      |
| <span data-ttu-id="9122d-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9122d-118">System-Id-Guid</span></span>    | <span data-ttu-id="9122d-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9122d-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span></span>        |
| <span data-ttu-id="9122d-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9122d-120">Syntax</span></span>            | [<span data-ttu-id="9122d-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="9122d-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9122d-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="9122d-122">Implementations</span></span>

-   [<span data-ttu-id="9122d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9122d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9122d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9122d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9122d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9122d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9122d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9122d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9122d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9122d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9122d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9122d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9122d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9122d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9122d-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="9122d-130">Entry</span></span> | <span data-ttu-id="9122d-131">Value</span><span class="sxs-lookup"><span data-stu-id="9122d-131">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9122d-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9122d-132">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9122d-133">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9122d-134">System-Only</span></span>            | <span data-ttu-id="9122d-135">False</span><span class="sxs-lookup"><span data-stu-id="9122d-135">False</span></span>                             |
| <span data-ttu-id="9122d-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9122d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9122d-137">False</span><span class="sxs-lookup"><span data-stu-id="9122d-137">False</span></span>                             |
| <span data-ttu-id="9122d-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9122d-138">Is Indexed</span></span>             | <span data-ttu-id="9122d-139">True</span><span class="sxs-lookup"><span data-stu-id="9122d-139">True</span></span>                              |
| <span data-ttu-id="9122d-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9122d-140">In Global Catalog</span></span>      | <span data-ttu-id="9122d-141">True</span><span class="sxs-lookup"><span data-stu-id="9122d-141">True</span></span>                              |
| <span data-ttu-id="9122d-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9122d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9122d-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9122d-143">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9122d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9122d-144">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9122d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9122d-145">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9122d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-146">Search-Flags</span></span>           | <span data-ttu-id="9122d-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9122d-147">0x00000001</span></span>                        |
| <span data-ttu-id="9122d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-148">System-Flags</span></span>           | <span data-ttu-id="9122d-149">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9122d-149">0x00000012</span></span>                        |
| <span data-ttu-id="9122d-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9122d-150">Classes used in</span></span>        | [<span data-ttu-id="9122d-151">**User**</span><span class="sxs-lookup"><span data-stu-id="9122d-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9122d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9122d-152">Windows Server 2003</span></span>



| <span data-ttu-id="9122d-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="9122d-153">Entry</span></span> | <span data-ttu-id="9122d-154">Value</span><span class="sxs-lookup"><span data-stu-id="9122d-154">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9122d-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9122d-155">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9122d-156">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9122d-157">System-Only</span></span>            | <span data-ttu-id="9122d-158">False</span><span class="sxs-lookup"><span data-stu-id="9122d-158">False</span></span>                             |
| <span data-ttu-id="9122d-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9122d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9122d-160">False</span><span class="sxs-lookup"><span data-stu-id="9122d-160">False</span></span>                             |
| <span data-ttu-id="9122d-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9122d-161">Is Indexed</span></span>             | <span data-ttu-id="9122d-162">True</span><span class="sxs-lookup"><span data-stu-id="9122d-162">True</span></span>                              |
| <span data-ttu-id="9122d-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9122d-163">In Global Catalog</span></span>      | <span data-ttu-id="9122d-164">True</span><span class="sxs-lookup"><span data-stu-id="9122d-164">True</span></span>                              |
| <span data-ttu-id="9122d-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9122d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9122d-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9122d-166">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9122d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9122d-167">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9122d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9122d-168">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9122d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-169">Search-Flags</span></span>           | <span data-ttu-id="9122d-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9122d-170">0x00000001</span></span>                        |
| <span data-ttu-id="9122d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-171">System-Flags</span></span>           | <span data-ttu-id="9122d-172">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9122d-172">0x00000012</span></span>                        |
| <span data-ttu-id="9122d-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9122d-173">Classes used in</span></span>        | [<span data-ttu-id="9122d-174">**User**</span><span class="sxs-lookup"><span data-stu-id="9122d-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9122d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9122d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9122d-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="9122d-176">Entry</span></span> | <span data-ttu-id="9122d-177">Value</span><span class="sxs-lookup"><span data-stu-id="9122d-177">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9122d-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9122d-178">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9122d-179">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9122d-180">System-Only</span></span>            | <span data-ttu-id="9122d-181">False</span><span class="sxs-lookup"><span data-stu-id="9122d-181">False</span></span>                             |
| <span data-ttu-id="9122d-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9122d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9122d-183">False</span><span class="sxs-lookup"><span data-stu-id="9122d-183">False</span></span>                             |
| <span data-ttu-id="9122d-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9122d-184">Is Indexed</span></span>             | <span data-ttu-id="9122d-185">True</span><span class="sxs-lookup"><span data-stu-id="9122d-185">True</span></span>                              |
| <span data-ttu-id="9122d-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9122d-186">In Global Catalog</span></span>      | <span data-ttu-id="9122d-187">True</span><span class="sxs-lookup"><span data-stu-id="9122d-187">True</span></span>                              |
| <span data-ttu-id="9122d-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9122d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9122d-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9122d-189">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9122d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9122d-190">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9122d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9122d-191">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9122d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-192">Search-Flags</span></span>           | <span data-ttu-id="9122d-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9122d-193">0x00000001</span></span>                        |
| <span data-ttu-id="9122d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-194">System-Flags</span></span>           | <span data-ttu-id="9122d-195">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9122d-195">0x00000012</span></span>                        |
| <span data-ttu-id="9122d-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9122d-196">Classes used in</span></span>        | [<span data-ttu-id="9122d-197">**User**</span><span class="sxs-lookup"><span data-stu-id="9122d-197">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9122d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9122d-198">Windows Server 2008</span></span>



| <span data-ttu-id="9122d-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="9122d-199">Entry</span></span> | <span data-ttu-id="9122d-200">Value</span><span class="sxs-lookup"><span data-stu-id="9122d-200">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9122d-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9122d-201">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9122d-202">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9122d-203">System-Only</span></span>            | <span data-ttu-id="9122d-204">False</span><span class="sxs-lookup"><span data-stu-id="9122d-204">False</span></span>                             |
| <span data-ttu-id="9122d-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9122d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9122d-206">False</span><span class="sxs-lookup"><span data-stu-id="9122d-206">False</span></span>                             |
| <span data-ttu-id="9122d-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9122d-207">Is Indexed</span></span>             | <span data-ttu-id="9122d-208">True</span><span class="sxs-lookup"><span data-stu-id="9122d-208">True</span></span>                              |
| <span data-ttu-id="9122d-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9122d-209">In Global Catalog</span></span>      | <span data-ttu-id="9122d-210">True</span><span class="sxs-lookup"><span data-stu-id="9122d-210">True</span></span>                              |
| <span data-ttu-id="9122d-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9122d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9122d-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9122d-212">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9122d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9122d-213">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9122d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9122d-214">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9122d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-215">Search-Flags</span></span>           | <span data-ttu-id="9122d-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9122d-216">0x00000001</span></span>                        |
| <span data-ttu-id="9122d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-217">System-Flags</span></span>           | <span data-ttu-id="9122d-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9122d-218">0x00000012</span></span>                        |
| <span data-ttu-id="9122d-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9122d-219">Classes used in</span></span>        | [<span data-ttu-id="9122d-220">**User**</span><span class="sxs-lookup"><span data-stu-id="9122d-220">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9122d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9122d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9122d-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="9122d-222">Entry</span></span> | <span data-ttu-id="9122d-223">Value</span><span class="sxs-lookup"><span data-stu-id="9122d-223">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9122d-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9122d-224">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9122d-225">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9122d-226">System-Only</span></span>            | <span data-ttu-id="9122d-227">False</span><span class="sxs-lookup"><span data-stu-id="9122d-227">False</span></span>                             |
| <span data-ttu-id="9122d-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9122d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9122d-229">False</span><span class="sxs-lookup"><span data-stu-id="9122d-229">False</span></span>                             |
| <span data-ttu-id="9122d-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9122d-230">Is Indexed</span></span>             | <span data-ttu-id="9122d-231">True</span><span class="sxs-lookup"><span data-stu-id="9122d-231">True</span></span>                              |
| <span data-ttu-id="9122d-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9122d-232">In Global Catalog</span></span>      | <span data-ttu-id="9122d-233">True</span><span class="sxs-lookup"><span data-stu-id="9122d-233">True</span></span>                              |
| <span data-ttu-id="9122d-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9122d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9122d-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9122d-235">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9122d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9122d-236">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9122d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9122d-237">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9122d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-238">Search-Flags</span></span>           | <span data-ttu-id="9122d-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9122d-239">0x00000001</span></span>                        |
| <span data-ttu-id="9122d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-240">System-Flags</span></span>           | <span data-ttu-id="9122d-241">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9122d-241">0x00000012</span></span>                        |
| <span data-ttu-id="9122d-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9122d-242">Classes used in</span></span>        | [<span data-ttu-id="9122d-243">**User**</span><span class="sxs-lookup"><span data-stu-id="9122d-243">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9122d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9122d-244">Windows Server 2012</span></span>



| <span data-ttu-id="9122d-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="9122d-245">Entry</span></span> | <span data-ttu-id="9122d-246">Value</span><span class="sxs-lookup"><span data-stu-id="9122d-246">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9122d-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="9122d-247">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9122d-248">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9122d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="9122d-249">System-Only</span></span>            | <span data-ttu-id="9122d-250">False</span><span class="sxs-lookup"><span data-stu-id="9122d-250">False</span></span>                             |
| <span data-ttu-id="9122d-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="9122d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="9122d-252">False</span><span class="sxs-lookup"><span data-stu-id="9122d-252">False</span></span>                             |
| <span data-ttu-id="9122d-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="9122d-253">Is Indexed</span></span>             | <span data-ttu-id="9122d-254">True</span><span class="sxs-lookup"><span data-stu-id="9122d-254">True</span></span>                              |
| <span data-ttu-id="9122d-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="9122d-255">In Global Catalog</span></span>      | <span data-ttu-id="9122d-256">True</span><span class="sxs-lookup"><span data-stu-id="9122d-256">True</span></span>                              |
| <span data-ttu-id="9122d-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="9122d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="9122d-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9122d-258">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9122d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9122d-259">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9122d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9122d-260">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9122d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-261">Search-Flags</span></span>           | <span data-ttu-id="9122d-262">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9122d-262">0x00000001</span></span>                        |
| <span data-ttu-id="9122d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9122d-263">System-Flags</span></span>           | <span data-ttu-id="9122d-264">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9122d-264">0x00000012</span></span>                        |
| <span data-ttu-id="9122d-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="9122d-265">Classes used in</span></span>        | [<span data-ttu-id="9122d-266">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="9122d-266">**User**</span></span>](c-user.md)<br/> |



 

 






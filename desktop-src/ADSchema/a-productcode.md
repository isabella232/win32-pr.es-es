---
title: Product-Code atributo)
description: Este atributo contiene un identificador único para una aplicación para un lanzamiento de producto determinado, representado como un GUID de cadena, por ejemplo \ 0034; 12345678-1234-1234-1234-123456789012 \ 0034;.
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Product-Code
- atributo productCode AD Schema
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dc874552fc819de4f9c58b23809b9f5662ee6e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997244"
---
# <a name="product-code-attribute"></a><span data-ttu-id="54cf0-105">Product-Code atributo)</span><span class="sxs-lookup"><span data-stu-id="54cf0-105">Product-Code attribute</span></span>

<span data-ttu-id="54cf0-106">Este atributo contiene un identificador único para una aplicación para un lanzamiento de producto determinado, representado como un GUID de cadena, por ejemplo, " {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="54cf0-106">This attribute contains a unique identifier for an application for a particular product release, represented as a string GUID, for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="54cf0-107">Las letras usadas en este GUID deben estar en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="54cf0-107">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="54cf0-108">Este identificador debe variar en diferentes versiones e idiomas.</span><span class="sxs-lookup"><span data-stu-id="54cf0-108">This ID must vary for different versions and languages.</span></span>



| <span data-ttu-id="54cf0-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="54cf0-109">Entry</span></span> | <span data-ttu-id="54cf0-110">Value</span><span class="sxs-lookup"><span data-stu-id="54cf0-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="54cf0-111">CN</span><span class="sxs-lookup"><span data-stu-id="54cf0-111">CN</span></span>                | <span data-ttu-id="54cf0-112">Product-Code</span><span class="sxs-lookup"><span data-stu-id="54cf0-112">Product-Code</span></span>                                          |
| <span data-ttu-id="54cf0-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="54cf0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="54cf0-114">productCode</span><span class="sxs-lookup"><span data-stu-id="54cf0-114">productCode</span></span>                                           |
| <span data-ttu-id="54cf0-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="54cf0-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="54cf0-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="54cf0-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="54cf0-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="54cf0-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="54cf0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="54cf0-118">Attribute-Id</span></span>      | <span data-ttu-id="54cf0-119">1.2.840.113556.1.4.818</span><span class="sxs-lookup"><span data-stu-id="54cf0-119">1.2.840.113556.1.4.818</span></span>                                |
| <span data-ttu-id="54cf0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="54cf0-120">System-Id-Guid</span></span>    | <span data-ttu-id="54cf0-121">d9e18317-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="54cf0-121">d9e18317-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="54cf0-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54cf0-122">Syntax</span></span>            | [<span data-ttu-id="54cf0-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="54cf0-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="54cf0-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="54cf0-124">Implementations</span></span>

-   [<span data-ttu-id="54cf0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="54cf0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="54cf0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="54cf0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="54cf0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="54cf0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="54cf0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="54cf0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="54cf0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="54cf0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="54cf0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="54cf0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="54cf0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="54cf0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="54cf0-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="54cf0-132">Entry</span></span> | <span data-ttu-id="54cf0-133">Value</span><span class="sxs-lookup"><span data-stu-id="54cf0-133">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="54cf0-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="54cf0-134">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54cf0-135">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="54cf0-136">System-Only</span></span>            | <span data-ttu-id="54cf0-137">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-137">False</span></span>                                                            |
| <span data-ttu-id="54cf0-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="54cf0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="54cf0-139">True</span><span class="sxs-lookup"><span data-stu-id="54cf0-139">True</span></span>                                                             |
| <span data-ttu-id="54cf0-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="54cf0-140">Is Indexed</span></span>             | <span data-ttu-id="54cf0-141">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-141">False</span></span>                                                            |
| <span data-ttu-id="54cf0-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="54cf0-142">In Global Catalog</span></span>      | <span data-ttu-id="54cf0-143">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-143">False</span></span>                                                            |
| <span data-ttu-id="54cf0-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="54cf0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="54cf0-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="54cf0-145">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="54cf0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54cf0-146">Range-Lower</span></span>            | <span data-ttu-id="54cf0-147">0</span><span class="sxs-lookup"><span data-stu-id="54cf0-147">0</span></span>                                                                |
| <span data-ttu-id="54cf0-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54cf0-148">Range-Upper</span></span>            | <span data-ttu-id="54cf0-149">16</span><span class="sxs-lookup"><span data-stu-id="54cf0-149">16</span></span>                                                               |
| <span data-ttu-id="54cf0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-150">Search-Flags</span></span>           | <span data-ttu-id="54cf0-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54cf0-151">0x00000000</span></span>                                                       |
| <span data-ttu-id="54cf0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-152">System-Flags</span></span>           | <span data-ttu-id="54cf0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54cf0-153">0x00000010</span></span>                                                       |
| <span data-ttu-id="54cf0-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="54cf0-154">Classes used in</span></span>        | [<span data-ttu-id="54cf0-155">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="54cf0-155">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="54cf0-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="54cf0-156">Windows Server 2003</span></span>



| <span data-ttu-id="54cf0-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="54cf0-157">Entry</span></span> | <span data-ttu-id="54cf0-158">Value</span><span class="sxs-lookup"><span data-stu-id="54cf0-158">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="54cf0-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="54cf0-159">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54cf0-160">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="54cf0-161">System-Only</span></span>            | <span data-ttu-id="54cf0-162">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-162">False</span></span>                                                            |
| <span data-ttu-id="54cf0-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="54cf0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="54cf0-164">True</span><span class="sxs-lookup"><span data-stu-id="54cf0-164">True</span></span>                                                             |
| <span data-ttu-id="54cf0-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="54cf0-165">Is Indexed</span></span>             | <span data-ttu-id="54cf0-166">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-166">False</span></span>                                                            |
| <span data-ttu-id="54cf0-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="54cf0-167">In Global Catalog</span></span>      | <span data-ttu-id="54cf0-168">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-168">False</span></span>                                                            |
| <span data-ttu-id="54cf0-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="54cf0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="54cf0-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="54cf0-170">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="54cf0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54cf0-171">Range-Lower</span></span>            | <span data-ttu-id="54cf0-172">0</span><span class="sxs-lookup"><span data-stu-id="54cf0-172">0</span></span>                                                                |
| <span data-ttu-id="54cf0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54cf0-173">Range-Upper</span></span>            | <span data-ttu-id="54cf0-174">16</span><span class="sxs-lookup"><span data-stu-id="54cf0-174">16</span></span>                                                               |
| <span data-ttu-id="54cf0-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-175">Search-Flags</span></span>           | <span data-ttu-id="54cf0-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54cf0-176">0x00000000</span></span>                                                       |
| <span data-ttu-id="54cf0-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-177">System-Flags</span></span>           | <span data-ttu-id="54cf0-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54cf0-178">0x00000010</span></span>                                                       |
| <span data-ttu-id="54cf0-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="54cf0-179">Classes used in</span></span>        | [<span data-ttu-id="54cf0-180">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="54cf0-180">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="54cf0-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="54cf0-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="54cf0-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="54cf0-182">Entry</span></span> | <span data-ttu-id="54cf0-183">Value</span><span class="sxs-lookup"><span data-stu-id="54cf0-183">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="54cf0-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="54cf0-184">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54cf0-185">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="54cf0-186">System-Only</span></span>            | <span data-ttu-id="54cf0-187">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-187">False</span></span>                                                            |
| <span data-ttu-id="54cf0-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="54cf0-188">Is-Single-Valued</span></span>       | <span data-ttu-id="54cf0-189">True</span><span class="sxs-lookup"><span data-stu-id="54cf0-189">True</span></span>                                                             |
| <span data-ttu-id="54cf0-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="54cf0-190">Is Indexed</span></span>             | <span data-ttu-id="54cf0-191">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-191">False</span></span>                                                            |
| <span data-ttu-id="54cf0-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="54cf0-192">In Global Catalog</span></span>      | <span data-ttu-id="54cf0-193">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-193">False</span></span>                                                            |
| <span data-ttu-id="54cf0-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="54cf0-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="54cf0-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="54cf0-195">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="54cf0-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54cf0-196">Range-Lower</span></span>            | <span data-ttu-id="54cf0-197">0</span><span class="sxs-lookup"><span data-stu-id="54cf0-197">0</span></span>                                                                |
| <span data-ttu-id="54cf0-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54cf0-198">Range-Upper</span></span>            | <span data-ttu-id="54cf0-199">16</span><span class="sxs-lookup"><span data-stu-id="54cf0-199">16</span></span>                                                               |
| <span data-ttu-id="54cf0-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-200">Search-Flags</span></span>           | <span data-ttu-id="54cf0-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54cf0-201">0x00000000</span></span>                                                       |
| <span data-ttu-id="54cf0-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-202">System-Flags</span></span>           | <span data-ttu-id="54cf0-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54cf0-203">0x00000010</span></span>                                                       |
| <span data-ttu-id="54cf0-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="54cf0-204">Classes used in</span></span>        | [<span data-ttu-id="54cf0-205">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="54cf0-205">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="54cf0-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54cf0-206">Windows Server 2008</span></span>



| <span data-ttu-id="54cf0-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="54cf0-207">Entry</span></span> | <span data-ttu-id="54cf0-208">Value</span><span class="sxs-lookup"><span data-stu-id="54cf0-208">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="54cf0-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="54cf0-209">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54cf0-210">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="54cf0-211">System-Only</span></span>            | <span data-ttu-id="54cf0-212">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-212">False</span></span>                                                            |
| <span data-ttu-id="54cf0-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="54cf0-213">Is-Single-Valued</span></span>       | <span data-ttu-id="54cf0-214">True</span><span class="sxs-lookup"><span data-stu-id="54cf0-214">True</span></span>                                                             |
| <span data-ttu-id="54cf0-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="54cf0-215">Is Indexed</span></span>             | <span data-ttu-id="54cf0-216">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-216">False</span></span>                                                            |
| <span data-ttu-id="54cf0-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="54cf0-217">In Global Catalog</span></span>      | <span data-ttu-id="54cf0-218">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-218">False</span></span>                                                            |
| <span data-ttu-id="54cf0-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="54cf0-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="54cf0-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="54cf0-220">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="54cf0-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54cf0-221">Range-Lower</span></span>            | <span data-ttu-id="54cf0-222">0</span><span class="sxs-lookup"><span data-stu-id="54cf0-222">0</span></span>                                                                |
| <span data-ttu-id="54cf0-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54cf0-223">Range-Upper</span></span>            | <span data-ttu-id="54cf0-224">16</span><span class="sxs-lookup"><span data-stu-id="54cf0-224">16</span></span>                                                               |
| <span data-ttu-id="54cf0-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-225">Search-Flags</span></span>           | <span data-ttu-id="54cf0-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54cf0-226">0x00000000</span></span>                                                       |
| <span data-ttu-id="54cf0-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-227">System-Flags</span></span>           | <span data-ttu-id="54cf0-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54cf0-228">0x00000010</span></span>                                                       |
| <span data-ttu-id="54cf0-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="54cf0-229">Classes used in</span></span>        | [<span data-ttu-id="54cf0-230">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="54cf0-230">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="54cf0-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54cf0-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="54cf0-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="54cf0-232">Entry</span></span> | <span data-ttu-id="54cf0-233">Value</span><span class="sxs-lookup"><span data-stu-id="54cf0-233">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="54cf0-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="54cf0-234">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54cf0-235">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="54cf0-236">System-Only</span></span>            | <span data-ttu-id="54cf0-237">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-237">False</span></span>                                                            |
| <span data-ttu-id="54cf0-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="54cf0-238">Is-Single-Valued</span></span>       | <span data-ttu-id="54cf0-239">True</span><span class="sxs-lookup"><span data-stu-id="54cf0-239">True</span></span>                                                             |
| <span data-ttu-id="54cf0-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="54cf0-240">Is Indexed</span></span>             | <span data-ttu-id="54cf0-241">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-241">False</span></span>                                                            |
| <span data-ttu-id="54cf0-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="54cf0-242">In Global Catalog</span></span>      | <span data-ttu-id="54cf0-243">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-243">False</span></span>                                                            |
| <span data-ttu-id="54cf0-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="54cf0-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="54cf0-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="54cf0-245">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="54cf0-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54cf0-246">Range-Lower</span></span>            | <span data-ttu-id="54cf0-247">0</span><span class="sxs-lookup"><span data-stu-id="54cf0-247">0</span></span>                                                                |
| <span data-ttu-id="54cf0-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54cf0-248">Range-Upper</span></span>            | <span data-ttu-id="54cf0-249">16</span><span class="sxs-lookup"><span data-stu-id="54cf0-249">16</span></span>                                                               |
| <span data-ttu-id="54cf0-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-250">Search-Flags</span></span>           | <span data-ttu-id="54cf0-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54cf0-251">0x00000000</span></span>                                                       |
| <span data-ttu-id="54cf0-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-252">System-Flags</span></span>           | <span data-ttu-id="54cf0-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54cf0-253">0x00000010</span></span>                                                       |
| <span data-ttu-id="54cf0-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="54cf0-254">Classes used in</span></span>        | [<span data-ttu-id="54cf0-255">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="54cf0-255">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="54cf0-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54cf0-256">Windows Server 2012</span></span>



| <span data-ttu-id="54cf0-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="54cf0-257">Entry</span></span> | <span data-ttu-id="54cf0-258">Value</span><span class="sxs-lookup"><span data-stu-id="54cf0-258">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="54cf0-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="54cf0-259">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="54cf0-260">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="54cf0-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="54cf0-261">System-Only</span></span>            | <span data-ttu-id="54cf0-262">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-262">False</span></span>                                                            |
| <span data-ttu-id="54cf0-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="54cf0-263">Is-Single-Valued</span></span>       | <span data-ttu-id="54cf0-264">True</span><span class="sxs-lookup"><span data-stu-id="54cf0-264">True</span></span>                                                             |
| <span data-ttu-id="54cf0-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="54cf0-265">Is Indexed</span></span>             | <span data-ttu-id="54cf0-266">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-266">False</span></span>                                                            |
| <span data-ttu-id="54cf0-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="54cf0-267">In Global Catalog</span></span>      | <span data-ttu-id="54cf0-268">False</span><span class="sxs-lookup"><span data-stu-id="54cf0-268">False</span></span>                                                            |
| <span data-ttu-id="54cf0-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="54cf0-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="54cf0-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="54cf0-270">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="54cf0-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="54cf0-271">Range-Lower</span></span>            | <span data-ttu-id="54cf0-272">0</span><span class="sxs-lookup"><span data-stu-id="54cf0-272">0</span></span>                                                                |
| <span data-ttu-id="54cf0-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="54cf0-273">Range-Upper</span></span>            | <span data-ttu-id="54cf0-274">16</span><span class="sxs-lookup"><span data-stu-id="54cf0-274">16</span></span>                                                               |
| <span data-ttu-id="54cf0-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-275">Search-Flags</span></span>           | <span data-ttu-id="54cf0-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54cf0-276">0x00000000</span></span>                                                       |
| <span data-ttu-id="54cf0-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="54cf0-277">System-Flags</span></span>           | <span data-ttu-id="54cf0-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="54cf0-278">0x00000010</span></span>                                                       |
| <span data-ttu-id="54cf0-279">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="54cf0-279">Classes used in</span></span>        | [<span data-ttu-id="54cf0-280">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="54cf0-280">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 






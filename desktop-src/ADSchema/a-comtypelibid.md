---
title: Atributo COM-typelib-ID
description: Este atributo almacena la lista de identificadores de biblioteca de tipos que contiene este paquete de aplicación.
ms.assetid: 3dcd2d1f-8b6d-46f6-9707-4af006f0e610
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de ID. de biblioteca COM-typelib
- cOMTypelibId esquema de AD de atributos
topic_type:
- apiref
api_name:
- COM-Typelib-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0be116963137dcdba4d97aa3de751bdf7308c335
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659216"
---
# <a name="com-typelib-id-attribute"></a><span data-ttu-id="d5c5e-105">Atributo COM-typelib-ID</span><span class="sxs-lookup"><span data-stu-id="d5c5e-105">COM-Typelib-Id attribute</span></span>

<span data-ttu-id="d5c5e-106">Este atributo almacena la lista de identificadores de biblioteca de tipos que contiene este paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5c5e-106">This attribute stores the list of type library IDs contained in this application package.</span></span>



| <span data-ttu-id="d5c5e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5c5e-107">Entry</span></span> | <span data-ttu-id="d5c5e-108">Value</span><span class="sxs-lookup"><span data-stu-id="d5c5e-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d5c5e-109">CN</span><span class="sxs-lookup"><span data-stu-id="d5c5e-109">CN</span></span>                | <span data-ttu-id="d5c5e-110">Identificador de typelib de COM</span><span class="sxs-lookup"><span data-stu-id="d5c5e-110">COM-Typelib-Id</span></span>                                                                   |
| <span data-ttu-id="d5c5e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d5c5e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d5c5e-112">cOMTypelibId</span><span class="sxs-lookup"><span data-stu-id="d5c5e-112">cOMTypelibId</span></span>                                                                     |
| <span data-ttu-id="d5c5e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d5c5e-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="d5c5e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d5c5e-114">Update Privilege</span></span>  | <span data-ttu-id="d5c5e-115">Cualquier usuario puede actualizar este objeto en función de la seguridad del objeto que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="d5c5e-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="d5c5e-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d5c5e-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="d5c5e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d5c5e-117">Attribute-Id</span></span>      | <span data-ttu-id="d5c5e-118">1.2.840.113556.1.4.254</span><span class="sxs-lookup"><span data-stu-id="d5c5e-118">1.2.840.113556.1.4.254</span></span>                                                           |
| <span data-ttu-id="d5c5e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d5c5e-119">System-Id-Guid</span></span>    | <span data-ttu-id="d5c5e-120">281416de-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="d5c5e-120">281416de-1968-11d0-a28f-00aa003049e2</span></span>                                             |
| <span data-ttu-id="d5c5e-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5c5e-121">Syntax</span></span>            | [<span data-ttu-id="d5c5e-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="d5c5e-123">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d5c5e-123">Implementations</span></span>

-   [<span data-ttu-id="d5c5e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d5c5e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d5c5e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d5c5e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d5c5e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d5c5e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d5c5e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5c5e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d5c5e-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5c5e-131">Entry</span></span> | <span data-ttu-id="d5c5e-132">Value</span><span class="sxs-lookup"><span data-stu-id="d5c5e-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d5c5e-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5c5e-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c5e-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c5e-135">System-Only</span></span>            | <span data-ttu-id="d5c5e-136">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-136">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5c5e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c5e-138">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-138">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5c5e-139">Is Indexed</span></span>             | <span data-ttu-id="d5c5e-140">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-140">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5c5e-141">In Global Catalog</span></span>      | <span data-ttu-id="d5c5e-142">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-142">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5c5e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c5e-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c5e-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d5c5e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c5e-145">Range-Lower</span></span>            | <span data-ttu-id="d5c5e-146">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-146">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c5e-147">Range-Upper</span></span>            | <span data-ttu-id="d5c5e-148">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-148">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-149">Search-Flags</span></span>           | <span data-ttu-id="d5c5e-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c5e-150">0x00000000</span></span>                                                       |
| <span data-ttu-id="d5c5e-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-151">System-Flags</span></span>           | <span data-ttu-id="d5c5e-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c5e-152">0x00000010</span></span>                                                       |
| <span data-ttu-id="d5c5e-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5c5e-153">Classes used in</span></span>        | [<span data-ttu-id="d5c5e-154">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-154">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d5c5e-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5c5e-155">Windows Server 2003</span></span>



| <span data-ttu-id="d5c5e-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5c5e-156">Entry</span></span> | <span data-ttu-id="d5c5e-157">Value</span><span class="sxs-lookup"><span data-stu-id="d5c5e-157">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d5c5e-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5c5e-158">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c5e-159">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c5e-160">System-Only</span></span>            | <span data-ttu-id="d5c5e-161">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-161">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5c5e-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c5e-163">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-163">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5c5e-164">Is Indexed</span></span>             | <span data-ttu-id="d5c5e-165">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-165">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5c5e-166">In Global Catalog</span></span>      | <span data-ttu-id="d5c5e-167">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-167">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5c5e-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c5e-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c5e-169">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d5c5e-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c5e-170">Range-Lower</span></span>            | <span data-ttu-id="d5c5e-171">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-171">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c5e-172">Range-Upper</span></span>            | <span data-ttu-id="d5c5e-173">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-173">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-174">Search-Flags</span></span>           | <span data-ttu-id="d5c5e-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c5e-175">0x00000000</span></span>                                                       |
| <span data-ttu-id="d5c5e-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-176">System-Flags</span></span>           | <span data-ttu-id="d5c5e-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c5e-177">0x00000010</span></span>                                                       |
| <span data-ttu-id="d5c5e-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5c5e-178">Classes used in</span></span>        | [<span data-ttu-id="d5c5e-179">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-179">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d5c5e-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d5c5e-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d5c5e-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5c5e-181">Entry</span></span> | <span data-ttu-id="d5c5e-182">Value</span><span class="sxs-lookup"><span data-stu-id="d5c5e-182">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d5c5e-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5c5e-183">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c5e-184">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c5e-185">System-Only</span></span>            | <span data-ttu-id="d5c5e-186">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-186">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5c5e-187">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c5e-188">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-188">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5c5e-189">Is Indexed</span></span>             | <span data-ttu-id="d5c5e-190">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-190">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5c5e-191">In Global Catalog</span></span>      | <span data-ttu-id="d5c5e-192">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-192">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5c5e-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c5e-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c5e-194">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d5c5e-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c5e-195">Range-Lower</span></span>            | <span data-ttu-id="d5c5e-196">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-196">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c5e-197">Range-Upper</span></span>            | <span data-ttu-id="d5c5e-198">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-198">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-199">Search-Flags</span></span>           | <span data-ttu-id="d5c5e-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c5e-200">0x00000000</span></span>                                                       |
| <span data-ttu-id="d5c5e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-201">System-Flags</span></span>           | <span data-ttu-id="d5c5e-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c5e-202">0x00000010</span></span>                                                       |
| <span data-ttu-id="d5c5e-203">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5c5e-203">Classes used in</span></span>        | [<span data-ttu-id="d5c5e-204">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-204">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d5c5e-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5c5e-205">Windows Server 2008</span></span>



| <span data-ttu-id="d5c5e-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5c5e-206">Entry</span></span> | <span data-ttu-id="d5c5e-207">Value</span><span class="sxs-lookup"><span data-stu-id="d5c5e-207">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d5c5e-208">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5c5e-208">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c5e-209">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c5e-210">System-Only</span></span>            | <span data-ttu-id="d5c5e-211">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-211">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-212">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5c5e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c5e-213">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-213">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-214">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5c5e-214">Is Indexed</span></span>             | <span data-ttu-id="d5c5e-215">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-215">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-216">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5c5e-216">In Global Catalog</span></span>      | <span data-ttu-id="d5c5e-217">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-217">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-218">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5c5e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c5e-219">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c5e-219">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d5c5e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c5e-220">Range-Lower</span></span>            | <span data-ttu-id="d5c5e-221">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-221">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c5e-222">Range-Upper</span></span>            | <span data-ttu-id="d5c5e-223">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-223">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-224">Search-Flags</span></span>           | <span data-ttu-id="d5c5e-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c5e-225">0x00000000</span></span>                                                       |
| <span data-ttu-id="d5c5e-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-226">System-Flags</span></span>           | <span data-ttu-id="d5c5e-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c5e-227">0x00000010</span></span>                                                       |
| <span data-ttu-id="d5c5e-228">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5c5e-228">Classes used in</span></span>        | [<span data-ttu-id="d5c5e-229">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-229">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d5c5e-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d5c5e-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d5c5e-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5c5e-231">Entry</span></span> | <span data-ttu-id="d5c5e-232">Value</span><span class="sxs-lookup"><span data-stu-id="d5c5e-232">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d5c5e-233">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5c5e-233">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c5e-234">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c5e-235">System-Only</span></span>            | <span data-ttu-id="d5c5e-236">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-236">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-237">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5c5e-237">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c5e-238">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-238">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-239">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5c5e-239">Is Indexed</span></span>             | <span data-ttu-id="d5c5e-240">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-240">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-241">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5c5e-241">In Global Catalog</span></span>      | <span data-ttu-id="d5c5e-242">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-242">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-243">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5c5e-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c5e-244">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c5e-244">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d5c5e-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c5e-245">Range-Lower</span></span>            | <span data-ttu-id="d5c5e-246">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-246">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c5e-247">Range-Upper</span></span>            | <span data-ttu-id="d5c5e-248">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-248">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-249">Search-Flags</span></span>           | <span data-ttu-id="d5c5e-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c5e-250">0x00000000</span></span>                                                       |
| <span data-ttu-id="d5c5e-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-251">System-Flags</span></span>           | <span data-ttu-id="d5c5e-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c5e-252">0x00000010</span></span>                                                       |
| <span data-ttu-id="d5c5e-253">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5c5e-253">Classes used in</span></span>        | [<span data-ttu-id="d5c5e-254">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-254">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d5c5e-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5c5e-255">Windows Server 2012</span></span>



| <span data-ttu-id="d5c5e-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="d5c5e-256">Entry</span></span> | <span data-ttu-id="d5c5e-257">Value</span><span class="sxs-lookup"><span data-stu-id="d5c5e-257">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d5c5e-258">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d5c5e-258">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c5e-259">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="d5c5e-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c5e-260">System-Only</span></span>            | <span data-ttu-id="d5c5e-261">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-261">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-262">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d5c5e-262">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c5e-263">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-263">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-264">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d5c5e-264">Is Indexed</span></span>             | <span data-ttu-id="d5c5e-265">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-265">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-266">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d5c5e-266">In Global Catalog</span></span>      | <span data-ttu-id="d5c5e-267">False</span><span class="sxs-lookup"><span data-stu-id="d5c5e-267">False</span></span>                                                            |
| <span data-ttu-id="d5c5e-268">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d5c5e-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c5e-269">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c5e-269">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="d5c5e-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c5e-270">Range-Lower</span></span>            | <span data-ttu-id="d5c5e-271">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-271">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c5e-272">Range-Upper</span></span>            | <span data-ttu-id="d5c5e-273">36</span><span class="sxs-lookup"><span data-stu-id="d5c5e-273">36</span></span>                                                               |
| <span data-ttu-id="d5c5e-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-274">Search-Flags</span></span>           | <span data-ttu-id="d5c5e-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c5e-275">0x00000000</span></span>                                                       |
| <span data-ttu-id="d5c5e-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c5e-276">System-Flags</span></span>           | <span data-ttu-id="d5c5e-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c5e-277">0x00000010</span></span>                                                       |
| <span data-ttu-id="d5c5e-278">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d5c5e-278">Classes used in</span></span>        | [<span data-ttu-id="d5c5e-279">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="d5c5e-279">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 






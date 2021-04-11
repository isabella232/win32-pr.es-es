---
title: Atributo MSI-File-List
description: Este atributo contiene una lista de archivos de Microsoft Installer, como archivos MSI base (. msi) y archivos de transformación MST (. MST).
ms.assetid: 259a13a2-bb34-49aa-862e-4159e887310c
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MSI-File-List
- msiFileList esquema de AD de atributos
topic_type:
- apiref
api_name:
- Msi-File-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05608cdf443ab053549fde7db509ca79be08b3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151801"
---
# <a name="msi-file-list-attribute"></a><span data-ttu-id="5971e-105">Atributo MSI-File-List</span><span class="sxs-lookup"><span data-stu-id="5971e-105">Msi-File-List attribute</span></span>

<span data-ttu-id="5971e-106">Este atributo contiene una lista de archivos de Microsoft Installer, como archivos MSI base (. msi) y archivos de transformación MST (. MST).</span><span class="sxs-lookup"><span data-stu-id="5971e-106">This attribute contains a list of Microsoft installer files, such as the base MSI file (.msi) and MST transform files (.mst).</span></span>



| <span data-ttu-id="5971e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5971e-107">Entry</span></span> | <span data-ttu-id="5971e-108">Value</span><span class="sxs-lookup"><span data-stu-id="5971e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5971e-109">CN</span><span class="sxs-lookup"><span data-stu-id="5971e-109">CN</span></span>                | <span data-ttu-id="5971e-110">Msi-archivo-lista</span><span class="sxs-lookup"><span data-stu-id="5971e-110">Msi-File-List</span></span>                               |
| <span data-ttu-id="5971e-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5971e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5971e-112">msiFileList</span><span class="sxs-lookup"><span data-stu-id="5971e-112">msiFileList</span></span>                                 |
| <span data-ttu-id="5971e-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5971e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="5971e-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5971e-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5971e-115">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5971e-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5971e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5971e-116">Attribute-Id</span></span>      | <span data-ttu-id="5971e-117">1.2.840.113556.1.4.671</span><span class="sxs-lookup"><span data-stu-id="5971e-117">1.2.840.113556.1.4.671</span></span>                      |
| <span data-ttu-id="5971e-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5971e-118">System-Id-Guid</span></span>    | <span data-ttu-id="5971e-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5971e-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="5971e-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5971e-120">Syntax</span></span>            | [<span data-ttu-id="5971e-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5971e-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5971e-122">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5971e-122">Implementations</span></span>

-   [<span data-ttu-id="5971e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5971e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5971e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5971e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5971e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5971e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5971e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5971e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5971e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5971e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5971e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5971e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5971e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5971e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5971e-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="5971e-130">Entry</span></span> | <span data-ttu-id="5971e-131">Value</span><span class="sxs-lookup"><span data-stu-id="5971e-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5971e-132">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5971e-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5971e-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5971e-134">System-Only</span></span>            | <span data-ttu-id="5971e-135">False</span><span class="sxs-lookup"><span data-stu-id="5971e-135">False</span></span>                                                            |
| <span data-ttu-id="5971e-136">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5971e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5971e-137">False</span><span class="sxs-lookup"><span data-stu-id="5971e-137">False</span></span>                                                            |
| <span data-ttu-id="5971e-138">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5971e-138">Is Indexed</span></span>             | <span data-ttu-id="5971e-139">False</span><span class="sxs-lookup"><span data-stu-id="5971e-139">False</span></span>                                                            |
| <span data-ttu-id="5971e-140">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5971e-140">In Global Catalog</span></span>      | <span data-ttu-id="5971e-141">False</span><span class="sxs-lookup"><span data-stu-id="5971e-141">False</span></span>                                                            |
| <span data-ttu-id="5971e-142">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5971e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5971e-143">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5971e-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5971e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5971e-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5971e-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-146">Search-Flags</span></span>           | <span data-ttu-id="5971e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5971e-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="5971e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-148">System-Flags</span></span>           | <span data-ttu-id="5971e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5971e-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="5971e-150">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5971e-150">Classes used in</span></span>        | [<span data-ttu-id="5971e-151">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="5971e-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5971e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5971e-152">Windows Server 2003</span></span>



| <span data-ttu-id="5971e-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="5971e-153">Entry</span></span> | <span data-ttu-id="5971e-154">Value</span><span class="sxs-lookup"><span data-stu-id="5971e-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5971e-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5971e-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5971e-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="5971e-157">System-Only</span></span>            | <span data-ttu-id="5971e-158">False</span><span class="sxs-lookup"><span data-stu-id="5971e-158">False</span></span>                                                            |
| <span data-ttu-id="5971e-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5971e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="5971e-160">False</span><span class="sxs-lookup"><span data-stu-id="5971e-160">False</span></span>                                                            |
| <span data-ttu-id="5971e-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5971e-161">Is Indexed</span></span>             | <span data-ttu-id="5971e-162">False</span><span class="sxs-lookup"><span data-stu-id="5971e-162">False</span></span>                                                            |
| <span data-ttu-id="5971e-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5971e-163">In Global Catalog</span></span>      | <span data-ttu-id="5971e-164">False</span><span class="sxs-lookup"><span data-stu-id="5971e-164">False</span></span>                                                            |
| <span data-ttu-id="5971e-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5971e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="5971e-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5971e-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5971e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5971e-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5971e-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-169">Search-Flags</span></span>           | <span data-ttu-id="5971e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5971e-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="5971e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-171">System-Flags</span></span>           | <span data-ttu-id="5971e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5971e-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="5971e-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5971e-173">Classes used in</span></span>        | [<span data-ttu-id="5971e-174">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="5971e-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5971e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5971e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5971e-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="5971e-176">Entry</span></span> | <span data-ttu-id="5971e-177">Value</span><span class="sxs-lookup"><span data-stu-id="5971e-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5971e-178">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5971e-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5971e-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="5971e-180">System-Only</span></span>            | <span data-ttu-id="5971e-181">False</span><span class="sxs-lookup"><span data-stu-id="5971e-181">False</span></span>                                                            |
| <span data-ttu-id="5971e-182">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5971e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="5971e-183">False</span><span class="sxs-lookup"><span data-stu-id="5971e-183">False</span></span>                                                            |
| <span data-ttu-id="5971e-184">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5971e-184">Is Indexed</span></span>             | <span data-ttu-id="5971e-185">False</span><span class="sxs-lookup"><span data-stu-id="5971e-185">False</span></span>                                                            |
| <span data-ttu-id="5971e-186">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5971e-186">In Global Catalog</span></span>      | <span data-ttu-id="5971e-187">False</span><span class="sxs-lookup"><span data-stu-id="5971e-187">False</span></span>                                                            |
| <span data-ttu-id="5971e-188">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5971e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="5971e-189">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5971e-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5971e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5971e-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5971e-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-192">Search-Flags</span></span>           | <span data-ttu-id="5971e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5971e-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="5971e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-194">System-Flags</span></span>           | <span data-ttu-id="5971e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5971e-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="5971e-196">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5971e-196">Classes used in</span></span>        | [<span data-ttu-id="5971e-197">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="5971e-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5971e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5971e-198">Windows Server 2008</span></span>



| <span data-ttu-id="5971e-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="5971e-199">Entry</span></span> | <span data-ttu-id="5971e-200">Value</span><span class="sxs-lookup"><span data-stu-id="5971e-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5971e-201">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5971e-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5971e-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="5971e-203">System-Only</span></span>            | <span data-ttu-id="5971e-204">False</span><span class="sxs-lookup"><span data-stu-id="5971e-204">False</span></span>                                                            |
| <span data-ttu-id="5971e-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5971e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="5971e-206">False</span><span class="sxs-lookup"><span data-stu-id="5971e-206">False</span></span>                                                            |
| <span data-ttu-id="5971e-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5971e-207">Is Indexed</span></span>             | <span data-ttu-id="5971e-208">False</span><span class="sxs-lookup"><span data-stu-id="5971e-208">False</span></span>                                                            |
| <span data-ttu-id="5971e-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5971e-209">In Global Catalog</span></span>      | <span data-ttu-id="5971e-210">False</span><span class="sxs-lookup"><span data-stu-id="5971e-210">False</span></span>                                                            |
| <span data-ttu-id="5971e-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5971e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="5971e-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5971e-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5971e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5971e-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5971e-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-215">Search-Flags</span></span>           | <span data-ttu-id="5971e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5971e-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="5971e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-217">System-Flags</span></span>           | <span data-ttu-id="5971e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5971e-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="5971e-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5971e-219">Classes used in</span></span>        | [<span data-ttu-id="5971e-220">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="5971e-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5971e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5971e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5971e-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="5971e-222">Entry</span></span> | <span data-ttu-id="5971e-223">Value</span><span class="sxs-lookup"><span data-stu-id="5971e-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5971e-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5971e-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5971e-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="5971e-226">System-Only</span></span>            | <span data-ttu-id="5971e-227">False</span><span class="sxs-lookup"><span data-stu-id="5971e-227">False</span></span>                                                            |
| <span data-ttu-id="5971e-228">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5971e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="5971e-229">False</span><span class="sxs-lookup"><span data-stu-id="5971e-229">False</span></span>                                                            |
| <span data-ttu-id="5971e-230">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5971e-230">Is Indexed</span></span>             | <span data-ttu-id="5971e-231">False</span><span class="sxs-lookup"><span data-stu-id="5971e-231">False</span></span>                                                            |
| <span data-ttu-id="5971e-232">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5971e-232">In Global Catalog</span></span>      | <span data-ttu-id="5971e-233">False</span><span class="sxs-lookup"><span data-stu-id="5971e-233">False</span></span>                                                            |
| <span data-ttu-id="5971e-234">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5971e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="5971e-235">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5971e-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5971e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5971e-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5971e-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-238">Search-Flags</span></span>           | <span data-ttu-id="5971e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5971e-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="5971e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-240">System-Flags</span></span>           | <span data-ttu-id="5971e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5971e-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="5971e-242">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5971e-242">Classes used in</span></span>        | [<span data-ttu-id="5971e-243">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="5971e-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5971e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5971e-244">Windows Server 2012</span></span>



| <span data-ttu-id="5971e-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="5971e-245">Entry</span></span> | <span data-ttu-id="5971e-246">Value</span><span class="sxs-lookup"><span data-stu-id="5971e-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5971e-247">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5971e-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5971e-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5971e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="5971e-249">System-Only</span></span>            | <span data-ttu-id="5971e-250">False</span><span class="sxs-lookup"><span data-stu-id="5971e-250">False</span></span>                                                            |
| <span data-ttu-id="5971e-251">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5971e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="5971e-252">False</span><span class="sxs-lookup"><span data-stu-id="5971e-252">False</span></span>                                                            |
| <span data-ttu-id="5971e-253">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5971e-253">Is Indexed</span></span>             | <span data-ttu-id="5971e-254">False</span><span class="sxs-lookup"><span data-stu-id="5971e-254">False</span></span>                                                            |
| <span data-ttu-id="5971e-255">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5971e-255">In Global Catalog</span></span>      | <span data-ttu-id="5971e-256">False</span><span class="sxs-lookup"><span data-stu-id="5971e-256">False</span></span>                                                            |
| <span data-ttu-id="5971e-257">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5971e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="5971e-258">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5971e-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5971e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5971e-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5971e-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="5971e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-261">Search-Flags</span></span>           | <span data-ttu-id="5971e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5971e-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="5971e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5971e-263">System-Flags</span></span>           | <span data-ttu-id="5971e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5971e-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="5971e-265">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5971e-265">Classes used in</span></span>        | [<span data-ttu-id="5971e-266">**Paquete-registro**</span><span class="sxs-lookup"><span data-stu-id="5971e-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 






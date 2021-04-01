---
title: atributo MS-DS-AZ-Class-ID
description: IDENTIFICADOR de clase requerido por la interfaz de usuario de AzRoles en el objeto AzApplication.
ms.assetid: cbbdc898-82b2-410e-8c9d-ae4f9641ac1a
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AZ-Class-ID
- Esquema de AD de atributo msDS-AzClassId
topic_type:
- apiref
api_name:
- ms-DS-Az-Class-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77d7ae6376deceaf23a9b7fa3c85ee8cb2b9748
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151822"
---
# <a name="ms-ds-az-class-id-attribute"></a><span data-ttu-id="878b9-105">atributo MS-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="878b9-105">ms-DS-Az-Class-ID attribute</span></span>

<span data-ttu-id="878b9-106">IDENTIFICADOR de clase requerido por la interfaz de usuario de AzRoles en el objeto AzApplication.</span><span class="sxs-lookup"><span data-stu-id="878b9-106">A class ID required by the AzRoles UI on the AzApplication object.</span></span>



| <span data-ttu-id="878b9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="878b9-107">Entry</span></span> | <span data-ttu-id="878b9-108">Value</span><span class="sxs-lookup"><span data-stu-id="878b9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="878b9-109">CN</span><span class="sxs-lookup"><span data-stu-id="878b9-109">CN</span></span>                | <span data-ttu-id="878b9-110">MS-DS-AZ-Class-ID</span><span class="sxs-lookup"><span data-stu-id="878b9-110">ms-DS-Az-Class-ID</span></span>                           |
| <span data-ttu-id="878b9-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="878b9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="878b9-112">msDS-AzClassId</span><span class="sxs-lookup"><span data-stu-id="878b9-112">msDS-AzClassId</span></span>                              |
| <span data-ttu-id="878b9-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="878b9-113">Size</span></span>              | <span data-ttu-id="878b9-114">36 caracteres</span><span class="sxs-lookup"><span data-stu-id="878b9-114">36 characters</span></span>                               |
| <span data-ttu-id="878b9-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="878b9-115">Update Privilege</span></span>  | <span data-ttu-id="878b9-116">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="878b9-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="878b9-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="878b9-117">Update Frequency</span></span>  | <span data-ttu-id="878b9-118">Durante la inicialización o el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="878b9-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="878b9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="878b9-119">Attribute-Id</span></span>      | <span data-ttu-id="878b9-120">1.2.840.113556.1.4.1816</span><span class="sxs-lookup"><span data-stu-id="878b9-120">1.2.840.113556.1.4.1816</span></span>                     |
| <span data-ttu-id="878b9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="878b9-121">System-Id-Guid</span></span>    | <span data-ttu-id="878b9-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span><span class="sxs-lookup"><span data-stu-id="878b9-122">013a7277-5c2d-49ef-a7de-b765b36a3f6f</span></span>        |
| <span data-ttu-id="878b9-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="878b9-123">Syntax</span></span>            | [<span data-ttu-id="878b9-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="878b9-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="878b9-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="878b9-125">Implementations</span></span>

-   [<span data-ttu-id="878b9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="878b9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="878b9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="878b9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="878b9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="878b9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="878b9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="878b9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="878b9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="878b9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="878b9-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="878b9-131">Windows Server 2003</span></span>



| <span data-ttu-id="878b9-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="878b9-132">Entry</span></span> | <span data-ttu-id="878b9-133">Value</span><span class="sxs-lookup"><span data-stu-id="878b9-133">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="878b9-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="878b9-134">Link-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="878b9-135">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="878b9-136">System-Only</span></span>            | <span data-ttu-id="878b9-137">False</span><span class="sxs-lookup"><span data-stu-id="878b9-137">False</span></span>        |
| <span data-ttu-id="878b9-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="878b9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="878b9-139">True</span><span class="sxs-lookup"><span data-stu-id="878b9-139">True</span></span>         |
| <span data-ttu-id="878b9-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="878b9-140">Is Indexed</span></span>             | <span data-ttu-id="878b9-141">False</span><span class="sxs-lookup"><span data-stu-id="878b9-141">False</span></span>        |
| <span data-ttu-id="878b9-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="878b9-142">In Global Catalog</span></span>      | <span data-ttu-id="878b9-143">False</span><span class="sxs-lookup"><span data-stu-id="878b9-143">False</span></span>        |
| <span data-ttu-id="878b9-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="878b9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="878b9-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="878b9-145">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="878b9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="878b9-146">Range-Lower</span></span>            | <span data-ttu-id="878b9-147">0</span><span class="sxs-lookup"><span data-stu-id="878b9-147">0</span></span>            |
| <span data-ttu-id="878b9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="878b9-148">Range-Upper</span></span>            | <span data-ttu-id="878b9-149">40</span><span class="sxs-lookup"><span data-stu-id="878b9-149">40</span></span>           |
| <span data-ttu-id="878b9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-150">Search-Flags</span></span>           | <span data-ttu-id="878b9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="878b9-151">0x00000000</span></span>   |
| <span data-ttu-id="878b9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-152">System-Flags</span></span>           | <span data-ttu-id="878b9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="878b9-153">0x00000010</span></span>   |
| <span data-ttu-id="878b9-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="878b9-154">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="878b9-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="878b9-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="878b9-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="878b9-156">Entry</span></span> | <span data-ttu-id="878b9-157">Value</span><span class="sxs-lookup"><span data-stu-id="878b9-157">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="878b9-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="878b9-158">Link-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="878b9-159">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="878b9-160">System-Only</span></span>            | <span data-ttu-id="878b9-161">False</span><span class="sxs-lookup"><span data-stu-id="878b9-161">False</span></span>        |
| <span data-ttu-id="878b9-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="878b9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="878b9-163">True</span><span class="sxs-lookup"><span data-stu-id="878b9-163">True</span></span>         |
| <span data-ttu-id="878b9-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="878b9-164">Is Indexed</span></span>             | <span data-ttu-id="878b9-165">False</span><span class="sxs-lookup"><span data-stu-id="878b9-165">False</span></span>        |
| <span data-ttu-id="878b9-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="878b9-166">In Global Catalog</span></span>      | <span data-ttu-id="878b9-167">False</span><span class="sxs-lookup"><span data-stu-id="878b9-167">False</span></span>        |
| <span data-ttu-id="878b9-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="878b9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="878b9-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="878b9-169">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="878b9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="878b9-170">Range-Lower</span></span>            | <span data-ttu-id="878b9-171">0</span><span class="sxs-lookup"><span data-stu-id="878b9-171">0</span></span>            |
| <span data-ttu-id="878b9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="878b9-172">Range-Upper</span></span>            | <span data-ttu-id="878b9-173">40</span><span class="sxs-lookup"><span data-stu-id="878b9-173">40</span></span>           |
| <span data-ttu-id="878b9-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-174">Search-Flags</span></span>           | <span data-ttu-id="878b9-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="878b9-175">0x00000000</span></span>   |
| <span data-ttu-id="878b9-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-176">System-Flags</span></span>           | <span data-ttu-id="878b9-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="878b9-177">0x00000010</span></span>   |
| <span data-ttu-id="878b9-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="878b9-178">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="878b9-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="878b9-179">Windows Server 2008</span></span>



| <span data-ttu-id="878b9-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="878b9-180">Entry</span></span> | <span data-ttu-id="878b9-181">Value</span><span class="sxs-lookup"><span data-stu-id="878b9-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="878b9-182">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="878b9-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="878b9-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="878b9-184">System-Only</span></span>            | <span data-ttu-id="878b9-185">False</span><span class="sxs-lookup"><span data-stu-id="878b9-185">False</span></span>        |
| <span data-ttu-id="878b9-186">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="878b9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="878b9-187">True</span><span class="sxs-lookup"><span data-stu-id="878b9-187">True</span></span>         |
| <span data-ttu-id="878b9-188">Está indexado</span><span class="sxs-lookup"><span data-stu-id="878b9-188">Is Indexed</span></span>             | <span data-ttu-id="878b9-189">False</span><span class="sxs-lookup"><span data-stu-id="878b9-189">False</span></span>        |
| <span data-ttu-id="878b9-190">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="878b9-190">In Global Catalog</span></span>      | <span data-ttu-id="878b9-191">False</span><span class="sxs-lookup"><span data-stu-id="878b9-191">False</span></span>        |
| <span data-ttu-id="878b9-192">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="878b9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="878b9-193">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="878b9-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="878b9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="878b9-194">Range-Lower</span></span>            | <span data-ttu-id="878b9-195">0</span><span class="sxs-lookup"><span data-stu-id="878b9-195">0</span></span>            |
| <span data-ttu-id="878b9-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="878b9-196">Range-Upper</span></span>            | <span data-ttu-id="878b9-197">40</span><span class="sxs-lookup"><span data-stu-id="878b9-197">40</span></span>           |
| <span data-ttu-id="878b9-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-198">Search-Flags</span></span>           | <span data-ttu-id="878b9-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="878b9-199">0x00000000</span></span>   |
| <span data-ttu-id="878b9-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-200">System-Flags</span></span>           | <span data-ttu-id="878b9-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="878b9-201">0x00000010</span></span>   |
| <span data-ttu-id="878b9-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="878b9-202">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="878b9-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="878b9-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="878b9-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="878b9-204">Entry</span></span> | <span data-ttu-id="878b9-205">Value</span><span class="sxs-lookup"><span data-stu-id="878b9-205">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="878b9-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="878b9-206">Link-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="878b9-207">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="878b9-208">System-Only</span></span>            | <span data-ttu-id="878b9-209">False</span><span class="sxs-lookup"><span data-stu-id="878b9-209">False</span></span>        |
| <span data-ttu-id="878b9-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="878b9-210">Is-Single-Valued</span></span>       | <span data-ttu-id="878b9-211">True</span><span class="sxs-lookup"><span data-stu-id="878b9-211">True</span></span>         |
| <span data-ttu-id="878b9-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="878b9-212">Is Indexed</span></span>             | <span data-ttu-id="878b9-213">False</span><span class="sxs-lookup"><span data-stu-id="878b9-213">False</span></span>        |
| <span data-ttu-id="878b9-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="878b9-214">In Global Catalog</span></span>      | <span data-ttu-id="878b9-215">False</span><span class="sxs-lookup"><span data-stu-id="878b9-215">False</span></span>        |
| <span data-ttu-id="878b9-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="878b9-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="878b9-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="878b9-217">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="878b9-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="878b9-218">Range-Lower</span></span>            | <span data-ttu-id="878b9-219">0</span><span class="sxs-lookup"><span data-stu-id="878b9-219">0</span></span>            |
| <span data-ttu-id="878b9-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="878b9-220">Range-Upper</span></span>            | <span data-ttu-id="878b9-221">40</span><span class="sxs-lookup"><span data-stu-id="878b9-221">40</span></span>           |
| <span data-ttu-id="878b9-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-222">Search-Flags</span></span>           | <span data-ttu-id="878b9-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="878b9-223">0x00000000</span></span>   |
| <span data-ttu-id="878b9-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-224">System-Flags</span></span>           | <span data-ttu-id="878b9-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="878b9-225">0x00000010</span></span>   |
| <span data-ttu-id="878b9-226">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="878b9-226">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="878b9-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="878b9-227">Windows Server 2012</span></span>



| <span data-ttu-id="878b9-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="878b9-228">Entry</span></span> | <span data-ttu-id="878b9-229">Value</span><span class="sxs-lookup"><span data-stu-id="878b9-229">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="878b9-230">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="878b9-230">Link-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="878b9-231">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="878b9-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="878b9-232">System-Only</span></span>            | <span data-ttu-id="878b9-233">False</span><span class="sxs-lookup"><span data-stu-id="878b9-233">False</span></span>        |
| <span data-ttu-id="878b9-234">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="878b9-234">Is-Single-Valued</span></span>       | <span data-ttu-id="878b9-235">True</span><span class="sxs-lookup"><span data-stu-id="878b9-235">True</span></span>         |
| <span data-ttu-id="878b9-236">Está indexado</span><span class="sxs-lookup"><span data-stu-id="878b9-236">Is Indexed</span></span>             | <span data-ttu-id="878b9-237">False</span><span class="sxs-lookup"><span data-stu-id="878b9-237">False</span></span>        |
| <span data-ttu-id="878b9-238">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="878b9-238">In Global Catalog</span></span>      | <span data-ttu-id="878b9-239">False</span><span class="sxs-lookup"><span data-stu-id="878b9-239">False</span></span>        |
| <span data-ttu-id="878b9-240">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="878b9-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="878b9-241">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="878b9-241">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="878b9-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="878b9-242">Range-Lower</span></span>            | <span data-ttu-id="878b9-243">0</span><span class="sxs-lookup"><span data-stu-id="878b9-243">0</span></span>            |
| <span data-ttu-id="878b9-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="878b9-244">Range-Upper</span></span>            | <span data-ttu-id="878b9-245">40</span><span class="sxs-lookup"><span data-stu-id="878b9-245">40</span></span>           |
| <span data-ttu-id="878b9-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-246">Search-Flags</span></span>           | <span data-ttu-id="878b9-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="878b9-247">0x00000000</span></span>   |
| <span data-ttu-id="878b9-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="878b9-248">System-Flags</span></span>           | <span data-ttu-id="878b9-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="878b9-249">0x00000010</span></span>   |
| <span data-ttu-id="878b9-250">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="878b9-250">Classes used in</span></span>        | \-           |



 

 





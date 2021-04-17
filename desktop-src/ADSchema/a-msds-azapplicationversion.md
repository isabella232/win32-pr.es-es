---
title: atributo MS-DS-AZ-Application-version
description: Un número de versión para indicar que el AzApplication está actualizado.
ms.assetid: e7a2771a-cada-48a3-979e-59af6a398a79
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AZ-Application-version
- Esquema de AD de atributo msDS-AzApplicationVersion
topic_type:
- apiref
api_name:
- ms-DS-Az-Application-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce0855f8462fb560bd337289a042f19be3380cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658899"
---
# <a name="ms-ds-az-application-version-attribute"></a><span data-ttu-id="6a5d7-105">atributo MS-DS-AZ-Application-version</span><span class="sxs-lookup"><span data-stu-id="6a5d7-105">ms-DS-Az-Application-Version attribute</span></span>

<span data-ttu-id="6a5d7-106">Un número de versión para indicar que el AzApplication está actualizado.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-106">A version number to indicate that the AzApplication is updated.</span></span>



| <span data-ttu-id="6a5d7-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a5d7-107">Entry</span></span> | <span data-ttu-id="6a5d7-108">Value</span><span class="sxs-lookup"><span data-stu-id="6a5d7-108">Value</span></span> |
|-------------------|------------------------------------------------------|
| <span data-ttu-id="6a5d7-109">CN</span><span class="sxs-lookup"><span data-stu-id="6a5d7-109">CN</span></span>                | <span data-ttu-id="6a5d7-110">MS-DS-AZ-Application-version</span><span class="sxs-lookup"><span data-stu-id="6a5d7-110">ms-DS-Az-Application-Version</span></span>                         |
| <span data-ttu-id="6a5d7-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="6a5d7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6a5d7-112">msDS-AzApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="6a5d7-112">msDS-AzApplicationVersion</span></span>                            |
| <span data-ttu-id="6a5d7-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6a5d7-113">Size</span></span>              | \-                                                   |
| <span data-ttu-id="6a5d7-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="6a5d7-114">Update Privilege</span></span>  | <span data-ttu-id="6a5d7-115">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="6a5d7-115">AzRoles admin</span></span>                                        |
| <span data-ttu-id="6a5d7-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="6a5d7-116">Update Frequency</span></span>  | <span data-ttu-id="6a5d7-117">Cuando cambia el número de versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-117">When the version number for the application changes.</span></span> |
| <span data-ttu-id="6a5d7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a5d7-118">Attribute-Id</span></span>      | <span data-ttu-id="6a5d7-119">1.2.840.113556.1.4.1817</span><span class="sxs-lookup"><span data-stu-id="6a5d7-119">1.2.840.113556.1.4.1817</span></span>                              |
| <span data-ttu-id="6a5d7-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6a5d7-120">System-Id-Guid</span></span>    | <span data-ttu-id="6a5d7-121">7184a120-3ac4-47ae-848f-fe0ab20784d4</span><span class="sxs-lookup"><span data-stu-id="6a5d7-121">7184a120-3ac4-47ae-848f-fe0ab20784d4</span></span>                 |
| <span data-ttu-id="6a5d7-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a5d7-122">Syntax</span></span>            | [<span data-ttu-id="6a5d7-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-123">**String(Unicode)**</span></span>](s-string-unicode.md)          |



## <a name="implementations"></a><span data-ttu-id="6a5d7-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6a5d7-124">Implementations</span></span>

-   [<span data-ttu-id="6a5d7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a5d7-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a5d7-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a5d7-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a5d7-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6a5d7-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a5d7-130">Windows Server 2003</span></span>



| <span data-ttu-id="6a5d7-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a5d7-131">Entry</span></span> | <span data-ttu-id="6a5d7-132">Value</span><span class="sxs-lookup"><span data-stu-id="6a5d7-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6a5d7-133">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a5d7-133">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a5d7-134">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a5d7-135">System-Only</span></span>            | <span data-ttu-id="6a5d7-136">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-136">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-137">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a5d7-137">Is-Single-Valued</span></span>       | <span data-ttu-id="6a5d7-138">True</span><span class="sxs-lookup"><span data-stu-id="6a5d7-138">True</span></span>                                                            |
| <span data-ttu-id="6a5d7-139">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a5d7-139">Is Indexed</span></span>             | <span data-ttu-id="6a5d7-140">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-140">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-141">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a5d7-141">In Global Catalog</span></span>      | <span data-ttu-id="6a5d7-142">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-142">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-143">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a5d7-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a5d7-144">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a5d7-144">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6a5d7-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a5d7-145">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a5d7-146">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-147">Search-Flags</span></span>           | <span data-ttu-id="6a5d7-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a5d7-148">0x00000000</span></span>                                                      |
| <span data-ttu-id="6a5d7-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-149">System-Flags</span></span>           | <span data-ttu-id="6a5d7-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a5d7-150">0x00000010</span></span>                                                      |
| <span data-ttu-id="6a5d7-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a5d7-151">Classes used in</span></span>        | [<span data-ttu-id="6a5d7-152">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-152">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a5d7-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a5d7-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a5d7-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a5d7-154">Entry</span></span> | <span data-ttu-id="6a5d7-155">Value</span><span class="sxs-lookup"><span data-stu-id="6a5d7-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6a5d7-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a5d7-156">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a5d7-157">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a5d7-158">System-Only</span></span>            | <span data-ttu-id="6a5d7-159">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-159">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a5d7-160">Is-Single-Valued</span></span>       | <span data-ttu-id="6a5d7-161">True</span><span class="sxs-lookup"><span data-stu-id="6a5d7-161">True</span></span>                                                            |
| <span data-ttu-id="6a5d7-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a5d7-162">Is Indexed</span></span>             | <span data-ttu-id="6a5d7-163">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-163">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a5d7-164">In Global Catalog</span></span>      | <span data-ttu-id="6a5d7-165">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-165">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a5d7-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a5d7-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a5d7-167">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6a5d7-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a5d7-168">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a5d7-169">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-170">Search-Flags</span></span>           | <span data-ttu-id="6a5d7-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a5d7-171">0x00000000</span></span>                                                      |
| <span data-ttu-id="6a5d7-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-172">System-Flags</span></span>           | <span data-ttu-id="6a5d7-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a5d7-173">0x00000010</span></span>                                                      |
| <span data-ttu-id="6a5d7-174">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a5d7-174">Classes used in</span></span>        | [<span data-ttu-id="6a5d7-175">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-175">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6a5d7-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a5d7-176">Windows Server 2008</span></span>



| <span data-ttu-id="6a5d7-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a5d7-177">Entry</span></span> | <span data-ttu-id="6a5d7-178">Value</span><span class="sxs-lookup"><span data-stu-id="6a5d7-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6a5d7-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a5d7-179">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a5d7-180">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a5d7-181">System-Only</span></span>            | <span data-ttu-id="6a5d7-182">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-182">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a5d7-183">Is-Single-Valued</span></span>       | <span data-ttu-id="6a5d7-184">True</span><span class="sxs-lookup"><span data-stu-id="6a5d7-184">True</span></span>                                                            |
| <span data-ttu-id="6a5d7-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a5d7-185">Is Indexed</span></span>             | <span data-ttu-id="6a5d7-186">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-186">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a5d7-187">In Global Catalog</span></span>      | <span data-ttu-id="6a5d7-188">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-188">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a5d7-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a5d7-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a5d7-190">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6a5d7-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a5d7-191">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a5d7-192">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-193">Search-Flags</span></span>           | <span data-ttu-id="6a5d7-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a5d7-194">0x00000000</span></span>                                                      |
| <span data-ttu-id="6a5d7-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-195">System-Flags</span></span>           | <span data-ttu-id="6a5d7-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a5d7-196">0x00000010</span></span>                                                      |
| <span data-ttu-id="6a5d7-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a5d7-197">Classes used in</span></span>        | [<span data-ttu-id="6a5d7-198">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-198">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a5d7-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a5d7-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a5d7-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a5d7-200">Entry</span></span> | <span data-ttu-id="6a5d7-201">Value</span><span class="sxs-lookup"><span data-stu-id="6a5d7-201">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6a5d7-202">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a5d7-202">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a5d7-203">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a5d7-204">System-Only</span></span>            | <span data-ttu-id="6a5d7-205">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-205">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-206">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a5d7-206">Is-Single-Valued</span></span>       | <span data-ttu-id="6a5d7-207">True</span><span class="sxs-lookup"><span data-stu-id="6a5d7-207">True</span></span>                                                            |
| <span data-ttu-id="6a5d7-208">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a5d7-208">Is Indexed</span></span>             | <span data-ttu-id="6a5d7-209">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-209">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-210">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a5d7-210">In Global Catalog</span></span>      | <span data-ttu-id="6a5d7-211">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-211">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-212">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a5d7-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a5d7-213">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a5d7-213">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6a5d7-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a5d7-214">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a5d7-215">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-216">Search-Flags</span></span>           | <span data-ttu-id="6a5d7-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a5d7-217">0x00000000</span></span>                                                      |
| <span data-ttu-id="6a5d7-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-218">System-Flags</span></span>           | <span data-ttu-id="6a5d7-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a5d7-219">0x00000010</span></span>                                                      |
| <span data-ttu-id="6a5d7-220">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a5d7-220">Classes used in</span></span>        | [<span data-ttu-id="6a5d7-221">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-221">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6a5d7-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a5d7-222">Windows Server 2012</span></span>



| <span data-ttu-id="6a5d7-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a5d7-223">Entry</span></span> | <span data-ttu-id="6a5d7-224">Value</span><span class="sxs-lookup"><span data-stu-id="6a5d7-224">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6a5d7-225">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="6a5d7-225">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a5d7-226">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="6a5d7-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a5d7-227">System-Only</span></span>            | <span data-ttu-id="6a5d7-228">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-228">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="6a5d7-229">Is-Single-Valued</span></span>       | <span data-ttu-id="6a5d7-230">True</span><span class="sxs-lookup"><span data-stu-id="6a5d7-230">True</span></span>                                                            |
| <span data-ttu-id="6a5d7-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="6a5d7-231">Is Indexed</span></span>             | <span data-ttu-id="6a5d7-232">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-232">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="6a5d7-233">In Global Catalog</span></span>      | <span data-ttu-id="6a5d7-234">False</span><span class="sxs-lookup"><span data-stu-id="6a5d7-234">False</span></span>                                                           |
| <span data-ttu-id="6a5d7-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="6a5d7-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a5d7-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6a5d7-236">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="6a5d7-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a5d7-237">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a5d7-238">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="6a5d7-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-239">Search-Flags</span></span>           | <span data-ttu-id="6a5d7-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a5d7-240">0x00000000</span></span>                                                      |
| <span data-ttu-id="6a5d7-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a5d7-241">System-Flags</span></span>           | <span data-ttu-id="6a5d7-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a5d7-242">0x00000010</span></span>                                                      |
| <span data-ttu-id="6a5d7-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="6a5d7-243">Classes used in</span></span>        | [<span data-ttu-id="6a5d7-244">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-244">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 






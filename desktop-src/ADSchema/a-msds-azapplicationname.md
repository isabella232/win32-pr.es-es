---
title: atributo MS-DS-AZ-Application-Name
description: Cadena que identifica de forma única un objeto de aplicación.
ms.assetid: 693a47f4-d3ae-4fae-8e5e-cbce41d00d45
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-AZ-Application-Name
- Esquema de AD de atributo msDS-AzApplicationName
topic_type:
- apiref
api_name:
- ms-DS-Az-Application-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24166af15a250ec284eeb600b81bb8bb7d264369
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659146"
---
# <a name="ms-ds-az-application-name-attribute"></a><span data-ttu-id="afc54-105">atributo MS-DS-AZ-Application-Name</span><span class="sxs-lookup"><span data-stu-id="afc54-105">ms-DS-Az-Application-Name attribute</span></span>

<span data-ttu-id="afc54-106">Cadena que identifica de forma única un objeto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="afc54-106">A string that uniquely identifies an application object.</span></span>



| <span data-ttu-id="afc54-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc54-107">Entry</span></span> | <span data-ttu-id="afc54-108">Value</span><span class="sxs-lookup"><span data-stu-id="afc54-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="afc54-109">CN</span><span class="sxs-lookup"><span data-stu-id="afc54-109">CN</span></span>                | <span data-ttu-id="afc54-110">MS-DS-AZ-Application-Name</span><span class="sxs-lookup"><span data-stu-id="afc54-110">ms-DS-Az-Application-Name</span></span>                   |
| <span data-ttu-id="afc54-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="afc54-111">Ldap-Display-Name</span></span> | <span data-ttu-id="afc54-112">msDS-AzApplicationName</span><span class="sxs-lookup"><span data-stu-id="afc54-112">msDS-AzApplicationName</span></span>                      |
| <span data-ttu-id="afc54-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="afc54-113">Size</span></span>              | <span data-ttu-id="afc54-114">128 caracteres</span><span class="sxs-lookup"><span data-stu-id="afc54-114">128 characters</span></span>                              |
| <span data-ttu-id="afc54-115">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="afc54-115">Update Privilege</span></span>  | <span data-ttu-id="afc54-116">Administrador de AzRoles</span><span class="sxs-lookup"><span data-stu-id="afc54-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="afc54-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="afc54-117">Update Frequency</span></span>  | <span data-ttu-id="afc54-118">Durante la inicialización o el cambio de directiva.</span><span class="sxs-lookup"><span data-stu-id="afc54-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="afc54-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="afc54-119">Attribute-Id</span></span>      | <span data-ttu-id="afc54-120">1.2.840.113556.1.4.1798</span><span class="sxs-lookup"><span data-stu-id="afc54-120">1.2.840.113556.1.4.1798</span></span>                     |
| <span data-ttu-id="afc54-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="afc54-121">System-Id-Guid</span></span>    | <span data-ttu-id="afc54-122">db5b0728-6208-4876-83b7-95d3e5695275</span><span class="sxs-lookup"><span data-stu-id="afc54-122">db5b0728-6208-4876-83b7-95d3e5695275</span></span>        |
| <span data-ttu-id="afc54-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afc54-123">Syntax</span></span>            | [<span data-ttu-id="afc54-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="afc54-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="afc54-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="afc54-125">Implementations</span></span>

-   [<span data-ttu-id="afc54-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="afc54-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="afc54-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="afc54-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="afc54-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="afc54-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="afc54-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="afc54-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="afc54-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="afc54-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="afc54-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afc54-131">Windows Server 2003</span></span>



| <span data-ttu-id="afc54-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc54-132">Entry</span></span> | <span data-ttu-id="afc54-133">Value</span><span class="sxs-lookup"><span data-stu-id="afc54-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="afc54-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afc54-134">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc54-135">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc54-136">System-Only</span></span>            | <span data-ttu-id="afc54-137">False</span><span class="sxs-lookup"><span data-stu-id="afc54-137">False</span></span>                                                           |
| <span data-ttu-id="afc54-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afc54-138">Is-Single-Valued</span></span>       | <span data-ttu-id="afc54-139">True</span><span class="sxs-lookup"><span data-stu-id="afc54-139">True</span></span>                                                            |
| <span data-ttu-id="afc54-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afc54-140">Is Indexed</span></span>             | <span data-ttu-id="afc54-141">False</span><span class="sxs-lookup"><span data-stu-id="afc54-141">False</span></span>                                                           |
| <span data-ttu-id="afc54-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc54-142">In Global Catalog</span></span>      | <span data-ttu-id="afc54-143">False</span><span class="sxs-lookup"><span data-stu-id="afc54-143">False</span></span>                                                           |
| <span data-ttu-id="afc54-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afc54-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc54-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afc54-145">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="afc54-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc54-146">Range-Lower</span></span>            | <span data-ttu-id="afc54-147">0</span><span class="sxs-lookup"><span data-stu-id="afc54-147">0</span></span>                                                               |
| <span data-ttu-id="afc54-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc54-148">Range-Upper</span></span>            | <span data-ttu-id="afc54-149">512</span><span class="sxs-lookup"><span data-stu-id="afc54-149">512</span></span>                                                             |
| <span data-ttu-id="afc54-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-150">Search-Flags</span></span>           | <span data-ttu-id="afc54-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc54-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="afc54-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-152">System-Flags</span></span>           | <span data-ttu-id="afc54-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc54-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="afc54-154">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afc54-154">Classes used in</span></span>        | [<span data-ttu-id="afc54-155">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="afc54-155">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="afc54-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="afc54-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="afc54-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc54-157">Entry</span></span> | <span data-ttu-id="afc54-158">Value</span><span class="sxs-lookup"><span data-stu-id="afc54-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="afc54-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afc54-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc54-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc54-161">System-Only</span></span>            | <span data-ttu-id="afc54-162">False</span><span class="sxs-lookup"><span data-stu-id="afc54-162">False</span></span>                                                           |
| <span data-ttu-id="afc54-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afc54-163">Is-Single-Valued</span></span>       | <span data-ttu-id="afc54-164">True</span><span class="sxs-lookup"><span data-stu-id="afc54-164">True</span></span>                                                            |
| <span data-ttu-id="afc54-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afc54-165">Is Indexed</span></span>             | <span data-ttu-id="afc54-166">False</span><span class="sxs-lookup"><span data-stu-id="afc54-166">False</span></span>                                                           |
| <span data-ttu-id="afc54-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc54-167">In Global Catalog</span></span>      | <span data-ttu-id="afc54-168">False</span><span class="sxs-lookup"><span data-stu-id="afc54-168">False</span></span>                                                           |
| <span data-ttu-id="afc54-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afc54-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc54-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afc54-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="afc54-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc54-171">Range-Lower</span></span>            | <span data-ttu-id="afc54-172">0</span><span class="sxs-lookup"><span data-stu-id="afc54-172">0</span></span>                                                               |
| <span data-ttu-id="afc54-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc54-173">Range-Upper</span></span>            | <span data-ttu-id="afc54-174">512</span><span class="sxs-lookup"><span data-stu-id="afc54-174">512</span></span>                                                             |
| <span data-ttu-id="afc54-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-175">Search-Flags</span></span>           | <span data-ttu-id="afc54-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc54-176">0x00000000</span></span>                                                      |
| <span data-ttu-id="afc54-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-177">System-Flags</span></span>           | <span data-ttu-id="afc54-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc54-178">0x00000010</span></span>                                                      |
| <span data-ttu-id="afc54-179">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afc54-179">Classes used in</span></span>        | [<span data-ttu-id="afc54-180">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="afc54-180">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="afc54-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afc54-181">Windows Server 2008</span></span>



| <span data-ttu-id="afc54-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc54-182">Entry</span></span> | <span data-ttu-id="afc54-183">Value</span><span class="sxs-lookup"><span data-stu-id="afc54-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="afc54-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afc54-184">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc54-185">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc54-186">System-Only</span></span>            | <span data-ttu-id="afc54-187">False</span><span class="sxs-lookup"><span data-stu-id="afc54-187">False</span></span>                                                           |
| <span data-ttu-id="afc54-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afc54-188">Is-Single-Valued</span></span>       | <span data-ttu-id="afc54-189">True</span><span class="sxs-lookup"><span data-stu-id="afc54-189">True</span></span>                                                            |
| <span data-ttu-id="afc54-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afc54-190">Is Indexed</span></span>             | <span data-ttu-id="afc54-191">False</span><span class="sxs-lookup"><span data-stu-id="afc54-191">False</span></span>                                                           |
| <span data-ttu-id="afc54-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc54-192">In Global Catalog</span></span>      | <span data-ttu-id="afc54-193">False</span><span class="sxs-lookup"><span data-stu-id="afc54-193">False</span></span>                                                           |
| <span data-ttu-id="afc54-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afc54-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc54-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afc54-195">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="afc54-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc54-196">Range-Lower</span></span>            | <span data-ttu-id="afc54-197">0</span><span class="sxs-lookup"><span data-stu-id="afc54-197">0</span></span>                                                               |
| <span data-ttu-id="afc54-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc54-198">Range-Upper</span></span>            | <span data-ttu-id="afc54-199">512</span><span class="sxs-lookup"><span data-stu-id="afc54-199">512</span></span>                                                             |
| <span data-ttu-id="afc54-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-200">Search-Flags</span></span>           | <span data-ttu-id="afc54-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc54-201">0x00000000</span></span>                                                      |
| <span data-ttu-id="afc54-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-202">System-Flags</span></span>           | <span data-ttu-id="afc54-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc54-203">0x00000010</span></span>                                                      |
| <span data-ttu-id="afc54-204">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afc54-204">Classes used in</span></span>        | [<span data-ttu-id="afc54-205">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="afc54-205">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="afc54-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afc54-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="afc54-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc54-207">Entry</span></span> | <span data-ttu-id="afc54-208">Value</span><span class="sxs-lookup"><span data-stu-id="afc54-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="afc54-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afc54-209">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc54-210">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc54-211">System-Only</span></span>            | <span data-ttu-id="afc54-212">False</span><span class="sxs-lookup"><span data-stu-id="afc54-212">False</span></span>                                                           |
| <span data-ttu-id="afc54-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afc54-213">Is-Single-Valued</span></span>       | <span data-ttu-id="afc54-214">True</span><span class="sxs-lookup"><span data-stu-id="afc54-214">True</span></span>                                                            |
| <span data-ttu-id="afc54-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afc54-215">Is Indexed</span></span>             | <span data-ttu-id="afc54-216">False</span><span class="sxs-lookup"><span data-stu-id="afc54-216">False</span></span>                                                           |
| <span data-ttu-id="afc54-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc54-217">In Global Catalog</span></span>      | <span data-ttu-id="afc54-218">False</span><span class="sxs-lookup"><span data-stu-id="afc54-218">False</span></span>                                                           |
| <span data-ttu-id="afc54-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afc54-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc54-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afc54-220">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="afc54-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc54-221">Range-Lower</span></span>            | <span data-ttu-id="afc54-222">0</span><span class="sxs-lookup"><span data-stu-id="afc54-222">0</span></span>                                                               |
| <span data-ttu-id="afc54-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc54-223">Range-Upper</span></span>            | <span data-ttu-id="afc54-224">512</span><span class="sxs-lookup"><span data-stu-id="afc54-224">512</span></span>                                                             |
| <span data-ttu-id="afc54-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-225">Search-Flags</span></span>           | <span data-ttu-id="afc54-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc54-226">0x00000000</span></span>                                                      |
| <span data-ttu-id="afc54-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-227">System-Flags</span></span>           | <span data-ttu-id="afc54-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc54-228">0x00000010</span></span>                                                      |
| <span data-ttu-id="afc54-229">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afc54-229">Classes used in</span></span>        | [<span data-ttu-id="afc54-230">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="afc54-230">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="afc54-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afc54-231">Windows Server 2012</span></span>



| <span data-ttu-id="afc54-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="afc54-232">Entry</span></span> | <span data-ttu-id="afc54-233">Value</span><span class="sxs-lookup"><span data-stu-id="afc54-233">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="afc54-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="afc54-234">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afc54-235">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="afc54-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="afc54-236">System-Only</span></span>            | <span data-ttu-id="afc54-237">False</span><span class="sxs-lookup"><span data-stu-id="afc54-237">False</span></span>                                                           |
| <span data-ttu-id="afc54-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="afc54-238">Is-Single-Valued</span></span>       | <span data-ttu-id="afc54-239">True</span><span class="sxs-lookup"><span data-stu-id="afc54-239">True</span></span>                                                            |
| <span data-ttu-id="afc54-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="afc54-240">Is Indexed</span></span>             | <span data-ttu-id="afc54-241">False</span><span class="sxs-lookup"><span data-stu-id="afc54-241">False</span></span>                                                           |
| <span data-ttu-id="afc54-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="afc54-242">In Global Catalog</span></span>      | <span data-ttu-id="afc54-243">False</span><span class="sxs-lookup"><span data-stu-id="afc54-243">False</span></span>                                                           |
| <span data-ttu-id="afc54-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="afc54-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="afc54-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afc54-245">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="afc54-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afc54-246">Range-Lower</span></span>            | <span data-ttu-id="afc54-247">0</span><span class="sxs-lookup"><span data-stu-id="afc54-247">0</span></span>                                                               |
| <span data-ttu-id="afc54-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afc54-248">Range-Upper</span></span>            | <span data-ttu-id="afc54-249">512</span><span class="sxs-lookup"><span data-stu-id="afc54-249">512</span></span>                                                             |
| <span data-ttu-id="afc54-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-250">Search-Flags</span></span>           | <span data-ttu-id="afc54-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="afc54-251">0x00000000</span></span>                                                      |
| <span data-ttu-id="afc54-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afc54-252">System-Flags</span></span>           | <span data-ttu-id="afc54-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="afc54-253">0x00000010</span></span>                                                      |
| <span data-ttu-id="afc54-254">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="afc54-254">Classes used in</span></span>        | [<span data-ttu-id="afc54-255">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="afc54-255">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 






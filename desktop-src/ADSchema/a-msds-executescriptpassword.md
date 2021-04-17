---
title: atributo MS-DS-ExecuteScriptPassword
description: Se usa durante el cambio de nombre del dominio. Este valor no se puede escribir ni leer desde mediante LDAP.
ms.assetid: 381c3676-0a11-4e53-8093-f04dbf156250
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-ExecuteScriptPassword
- Esquema de AD de atributo msDS-ExecuteScriptPassword
topic_type:
- apiref
api_name:
- ms-DS-ExecuteScriptPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01ebb231404188235236442df1d4916814f0636
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658880"
---
# <a name="ms-ds-executescriptpassword-attribute"></a><span data-ttu-id="f3b68-106">atributo MS-DS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="f3b68-106">ms-DS-ExecuteScriptPassword attribute</span></span>

<span data-ttu-id="f3b68-107">Se usa durante el cambio de nombre del dominio.</span><span class="sxs-lookup"><span data-stu-id="f3b68-107">Used during domain rename.</span></span> <span data-ttu-id="f3b68-108">Este valor no se puede escribir ni leer desde mediante LDAP.</span><span class="sxs-lookup"><span data-stu-id="f3b68-108">This value cannot be written to or read from by using LDAP.</span></span>



| <span data-ttu-id="f3b68-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b68-109">Entry</span></span> | <span data-ttu-id="f3b68-110">Value</span><span class="sxs-lookup"><span data-stu-id="f3b68-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f3b68-111">CN</span><span class="sxs-lookup"><span data-stu-id="f3b68-111">CN</span></span>                | <span data-ttu-id="f3b68-112">MS-DS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="f3b68-112">ms-DS-ExecuteScriptPassword</span></span>                           |
| <span data-ttu-id="f3b68-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="f3b68-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f3b68-114">msDS-ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="f3b68-114">msDS-ExecuteScriptPassword</span></span>                            |
| <span data-ttu-id="f3b68-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f3b68-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f3b68-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="f3b68-116">Update Privilege</span></span>  | <span data-ttu-id="f3b68-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="f3b68-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="f3b68-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="f3b68-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f3b68-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3b68-119">Attribute-Id</span></span>      | <span data-ttu-id="f3b68-120">1.2.840.113556.1.4.1783</span><span class="sxs-lookup"><span data-stu-id="f3b68-120">1.2.840.113556.1.4.1783</span></span>                               |
| <span data-ttu-id="f3b68-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f3b68-121">System-Id-Guid</span></span>    | <span data-ttu-id="f3b68-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span><span class="sxs-lookup"><span data-stu-id="f3b68-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span></span>                  |
| <span data-ttu-id="f3b68-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3b68-123">Syntax</span></span>            | [<span data-ttu-id="f3b68-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f3b68-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f3b68-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="f3b68-125">Implementations</span></span>

-   [<span data-ttu-id="f3b68-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3b68-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3b68-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f3b68-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f3b68-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3b68-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3b68-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3b68-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3b68-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3b68-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3b68-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3b68-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f3b68-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3b68-132">Windows Server 2003</span></span>



| <span data-ttu-id="f3b68-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b68-133">Entry</span></span> | <span data-ttu-id="f3b68-134">Value</span><span class="sxs-lookup"><span data-stu-id="f3b68-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f3b68-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3b68-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f3b68-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b68-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f3b68-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b68-137">System-Only</span></span>            | <span data-ttu-id="f3b68-138">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-138">True</span></span>                                                          |
| <span data-ttu-id="f3b68-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3b68-139">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b68-140">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-140">True</span></span>                                                          |
| <span data-ttu-id="f3b68-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3b68-141">Is Indexed</span></span>             | <span data-ttu-id="f3b68-142">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-142">False</span></span>                                                         |
| <span data-ttu-id="f3b68-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b68-143">In Global Catalog</span></span>      | <span data-ttu-id="f3b68-144">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-144">False</span></span>                                                         |
| <span data-ttu-id="f3b68-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3b68-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b68-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3b68-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f3b68-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b68-147">Range-Lower</span></span>            | <span data-ttu-id="f3b68-148">0</span><span class="sxs-lookup"><span data-stu-id="f3b68-148">0</span></span>                                                             |
| <span data-ttu-id="f3b68-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b68-149">Range-Upper</span></span>            | <span data-ttu-id="f3b68-150">64</span><span class="sxs-lookup"><span data-stu-id="f3b68-150">64</span></span>                                                            |
| <span data-ttu-id="f3b68-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-151">Search-Flags</span></span>           | <span data-ttu-id="f3b68-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b68-152">0x00000000</span></span>                                                    |
| <span data-ttu-id="f3b68-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-153">System-Flags</span></span>           | <span data-ttu-id="f3b68-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f3b68-154">0x00000011</span></span>                                                    |
| <span data-ttu-id="f3b68-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3b68-155">Classes used in</span></span>        | [<span data-ttu-id="f3b68-156">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="f3b68-156">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f3b68-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="f3b68-157">ADAM</span></span>



| <span data-ttu-id="f3b68-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b68-158">Entry</span></span> | <span data-ttu-id="f3b68-159">Value</span><span class="sxs-lookup"><span data-stu-id="f3b68-159">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f3b68-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3b68-160">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f3b68-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b68-161">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f3b68-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b68-162">System-Only</span></span>            | <span data-ttu-id="f3b68-163">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-163">True</span></span>                                                          |
| <span data-ttu-id="f3b68-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3b68-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b68-165">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-165">True</span></span>                                                          |
| <span data-ttu-id="f3b68-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3b68-166">Is Indexed</span></span>             | <span data-ttu-id="f3b68-167">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-167">False</span></span>                                                         |
| <span data-ttu-id="f3b68-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b68-168">In Global Catalog</span></span>      | <span data-ttu-id="f3b68-169">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-169">False</span></span>                                                         |
| <span data-ttu-id="f3b68-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3b68-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b68-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3b68-171">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f3b68-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b68-172">Range-Lower</span></span>            | <span data-ttu-id="f3b68-173">0</span><span class="sxs-lookup"><span data-stu-id="f3b68-173">0</span></span>                                                             |
| <span data-ttu-id="f3b68-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b68-174">Range-Upper</span></span>            | <span data-ttu-id="f3b68-175">64</span><span class="sxs-lookup"><span data-stu-id="f3b68-175">64</span></span>                                                            |
| <span data-ttu-id="f3b68-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-176">Search-Flags</span></span>           | <span data-ttu-id="f3b68-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b68-177">0x00000000</span></span>                                                    |
| <span data-ttu-id="f3b68-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-178">System-Flags</span></span>           | <span data-ttu-id="f3b68-179">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f3b68-179">0x00000011</span></span>                                                    |
| <span data-ttu-id="f3b68-180">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3b68-180">Classes used in</span></span>        | [<span data-ttu-id="f3b68-181">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="f3b68-181">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3b68-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3b68-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3b68-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b68-183">Entry</span></span> | <span data-ttu-id="f3b68-184">Value</span><span class="sxs-lookup"><span data-stu-id="f3b68-184">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f3b68-185">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3b68-185">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f3b68-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b68-186">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f3b68-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b68-187">System-Only</span></span>            | <span data-ttu-id="f3b68-188">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-188">True</span></span>                                                          |
| <span data-ttu-id="f3b68-189">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3b68-189">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b68-190">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-190">True</span></span>                                                          |
| <span data-ttu-id="f3b68-191">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3b68-191">Is Indexed</span></span>             | <span data-ttu-id="f3b68-192">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-192">False</span></span>                                                         |
| <span data-ttu-id="f3b68-193">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b68-193">In Global Catalog</span></span>      | <span data-ttu-id="f3b68-194">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-194">False</span></span>                                                         |
| <span data-ttu-id="f3b68-195">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3b68-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b68-196">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3b68-196">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f3b68-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b68-197">Range-Lower</span></span>            | <span data-ttu-id="f3b68-198">0</span><span class="sxs-lookup"><span data-stu-id="f3b68-198">0</span></span>                                                             |
| <span data-ttu-id="f3b68-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b68-199">Range-Upper</span></span>            | <span data-ttu-id="f3b68-200">64</span><span class="sxs-lookup"><span data-stu-id="f3b68-200">64</span></span>                                                            |
| <span data-ttu-id="f3b68-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-201">Search-Flags</span></span>           | <span data-ttu-id="f3b68-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b68-202">0x00000000</span></span>                                                    |
| <span data-ttu-id="f3b68-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-203">System-Flags</span></span>           | <span data-ttu-id="f3b68-204">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f3b68-204">0x00000011</span></span>                                                    |
| <span data-ttu-id="f3b68-205">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3b68-205">Classes used in</span></span>        | [<span data-ttu-id="f3b68-206">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="f3b68-206">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3b68-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3b68-207">Windows Server 2008</span></span>



| <span data-ttu-id="f3b68-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b68-208">Entry</span></span> | <span data-ttu-id="f3b68-209">Value</span><span class="sxs-lookup"><span data-stu-id="f3b68-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b68-210">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3b68-210">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f3b68-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b68-211">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f3b68-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b68-212">System-Only</span></span>            | <span data-ttu-id="f3b68-213">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-213">True</span></span>                                                                                                    |
| <span data-ttu-id="f3b68-214">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3b68-214">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b68-215">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-215">True</span></span>                                                                                                    |
| <span data-ttu-id="f3b68-216">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3b68-216">Is Indexed</span></span>             | <span data-ttu-id="f3b68-217">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-217">False</span></span>                                                                                                   |
| <span data-ttu-id="f3b68-218">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b68-218">In Global Catalog</span></span>      | <span data-ttu-id="f3b68-219">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-219">False</span></span>                                                                                                   |
| <span data-ttu-id="f3b68-220">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3b68-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b68-221">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3b68-221">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="f3b68-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b68-222">Range-Lower</span></span>            | <span data-ttu-id="f3b68-223">0</span><span class="sxs-lookup"><span data-stu-id="f3b68-223">0</span></span>                                                                                                       |
| <span data-ttu-id="f3b68-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b68-224">Range-Upper</span></span>            | <span data-ttu-id="f3b68-225">64</span><span class="sxs-lookup"><span data-stu-id="f3b68-225">64</span></span>                                                                                                      |
| <span data-ttu-id="f3b68-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-226">Search-Flags</span></span>           | <span data-ttu-id="f3b68-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b68-227">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="f3b68-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-228">System-Flags</span></span>           | <span data-ttu-id="f3b68-229">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f3b68-229">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="f3b68-230">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3b68-230">Classes used in</span></span>        | [<span data-ttu-id="f3b68-231">**Computer**</span><span class="sxs-lookup"><span data-stu-id="f3b68-231">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="f3b68-232">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="f3b68-232">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3b68-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3b68-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3b68-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b68-234">Entry</span></span> | <span data-ttu-id="f3b68-235">Value</span><span class="sxs-lookup"><span data-stu-id="f3b68-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b68-236">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3b68-236">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f3b68-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b68-237">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f3b68-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b68-238">System-Only</span></span>            | <span data-ttu-id="f3b68-239">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-239">True</span></span>                                                                                                    |
| <span data-ttu-id="f3b68-240">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3b68-240">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b68-241">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-241">True</span></span>                                                                                                    |
| <span data-ttu-id="f3b68-242">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3b68-242">Is Indexed</span></span>             | <span data-ttu-id="f3b68-243">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-243">False</span></span>                                                                                                   |
| <span data-ttu-id="f3b68-244">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b68-244">In Global Catalog</span></span>      | <span data-ttu-id="f3b68-245">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-245">False</span></span>                                                                                                   |
| <span data-ttu-id="f3b68-246">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3b68-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b68-247">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3b68-247">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="f3b68-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b68-248">Range-Lower</span></span>            | <span data-ttu-id="f3b68-249">0</span><span class="sxs-lookup"><span data-stu-id="f3b68-249">0</span></span>                                                                                                       |
| <span data-ttu-id="f3b68-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b68-250">Range-Upper</span></span>            | <span data-ttu-id="f3b68-251">64</span><span class="sxs-lookup"><span data-stu-id="f3b68-251">64</span></span>                                                                                                      |
| <span data-ttu-id="f3b68-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-252">Search-Flags</span></span>           | <span data-ttu-id="f3b68-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b68-253">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="f3b68-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-254">System-Flags</span></span>           | <span data-ttu-id="f3b68-255">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f3b68-255">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="f3b68-256">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3b68-256">Classes used in</span></span>        | [<span data-ttu-id="f3b68-257">**Computer**</span><span class="sxs-lookup"><span data-stu-id="f3b68-257">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="f3b68-258">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="f3b68-258">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3b68-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3b68-259">Windows Server 2012</span></span>



| <span data-ttu-id="f3b68-260">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b68-260">Entry</span></span> | <span data-ttu-id="f3b68-261">Value</span><span class="sxs-lookup"><span data-stu-id="f3b68-261">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b68-262">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="f3b68-262">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f3b68-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b68-263">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="f3b68-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b68-264">System-Only</span></span>            | <span data-ttu-id="f3b68-265">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-265">True</span></span>                                                                                                    |
| <span data-ttu-id="f3b68-266">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="f3b68-266">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b68-267">True</span><span class="sxs-lookup"><span data-stu-id="f3b68-267">True</span></span>                                                                                                    |
| <span data-ttu-id="f3b68-268">Está indexado</span><span class="sxs-lookup"><span data-stu-id="f3b68-268">Is Indexed</span></span>             | <span data-ttu-id="f3b68-269">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-269">False</span></span>                                                                                                   |
| <span data-ttu-id="f3b68-270">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b68-270">In Global Catalog</span></span>      | <span data-ttu-id="f3b68-271">False</span><span class="sxs-lookup"><span data-stu-id="f3b68-271">False</span></span>                                                                                                   |
| <span data-ttu-id="f3b68-272">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="f3b68-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b68-273">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f3b68-273">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="f3b68-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b68-274">Range-Lower</span></span>            | <span data-ttu-id="f3b68-275">0</span><span class="sxs-lookup"><span data-stu-id="f3b68-275">0</span></span>                                                                                                       |
| <span data-ttu-id="f3b68-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b68-276">Range-Upper</span></span>            | <span data-ttu-id="f3b68-277">64</span><span class="sxs-lookup"><span data-stu-id="f3b68-277">64</span></span>                                                                                                      |
| <span data-ttu-id="f3b68-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-278">Search-Flags</span></span>           | <span data-ttu-id="f3b68-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b68-279">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="f3b68-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b68-280">System-Flags</span></span>           | <span data-ttu-id="f3b68-281">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f3b68-281">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="f3b68-282">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="f3b68-282">Classes used in</span></span>        | [<span data-ttu-id="f3b68-283">**Computer**</span><span class="sxs-lookup"><span data-stu-id="f3b68-283">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="f3b68-284">**Contenedor de referencias cruzadas**</span><span class="sxs-lookup"><span data-stu-id="f3b68-284">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 






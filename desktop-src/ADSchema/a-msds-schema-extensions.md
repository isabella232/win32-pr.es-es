---
title: atributo MS-DS-Schema-Extensions
description: BLOB binario que se usa para almacenar información acerca de las extensiones de los objetos de esquema.
ms.assetid: a2ffc4c6-ec33-4265-9a1e-c07597d2af50
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Schema-Extensions
- Esquema de AD del atributo msDs-Schema-Extensions
topic_type:
- apiref
api_name:
- ms-ds-Schema-Extensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f524e28f2d45d03f7851fc46d32e986968f81bfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494014"
---
# <a name="ms-ds-schema-extensions-attribute"></a><span data-ttu-id="88a00-105">atributo MS-DS-Schema-Extensions</span><span class="sxs-lookup"><span data-stu-id="88a00-105">ms-ds-Schema-Extensions attribute</span></span>

<span data-ttu-id="88a00-106">BLOB binario que se usa para almacenar información acerca de las extensiones de los objetos de esquema.</span><span class="sxs-lookup"><span data-stu-id="88a00-106">A binary BLOB used to store information about extensions to schema objects.</span></span>



| <span data-ttu-id="88a00-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="88a00-107">Entry</span></span> | <span data-ttu-id="88a00-108">Value</span><span class="sxs-lookup"><span data-stu-id="88a00-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="88a00-109">CN</span><span class="sxs-lookup"><span data-stu-id="88a00-109">CN</span></span>                | <span data-ttu-id="88a00-110">Extensiones MS-DS-Schema-Extensions</span><span class="sxs-lookup"><span data-stu-id="88a00-110">ms-ds-Schema-Extensions</span></span>                               |
| <span data-ttu-id="88a00-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="88a00-111">Ldap-Display-Name</span></span> | <span data-ttu-id="88a00-112">msDs-Schema-Extensions</span><span class="sxs-lookup"><span data-stu-id="88a00-112">msDs-Schema-Extensions</span></span>                                |
| <span data-ttu-id="88a00-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="88a00-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="88a00-114">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="88a00-114">Update Privilege</span></span>  | <span data-ttu-id="88a00-115">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="88a00-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="88a00-116">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="88a00-116">Update Frequency</span></span>  | <span data-ttu-id="88a00-117">Cuando se extiende el esquema.</span><span class="sxs-lookup"><span data-stu-id="88a00-117">When the schema is extended.</span></span>                          |
| <span data-ttu-id="88a00-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88a00-118">Attribute-Id</span></span>      | <span data-ttu-id="88a00-119">1.2.840.113556.1.4.1440</span><span class="sxs-lookup"><span data-stu-id="88a00-119">1.2.840.113556.1.4.1440</span></span>                               |
| <span data-ttu-id="88a00-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="88a00-120">System-Id-Guid</span></span>    | <span data-ttu-id="88a00-121">b39a61be-ed07-4cab-9a4a-4963ed0141e1</span><span class="sxs-lookup"><span data-stu-id="88a00-121">b39a61be-ed07-4cab-9a4a-4963ed0141e1</span></span>                  |
| <span data-ttu-id="88a00-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88a00-122">Syntax</span></span>            | [<span data-ttu-id="88a00-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="88a00-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="88a00-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="88a00-124">Implementations</span></span>

-   [<span data-ttu-id="88a00-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88a00-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88a00-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="88a00-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="88a00-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88a00-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88a00-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88a00-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88a00-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88a00-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88a00-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88a00-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="88a00-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88a00-131">Windows Server 2003</span></span>



| <span data-ttu-id="88a00-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="88a00-132">Entry</span></span> | <span data-ttu-id="88a00-133">Value</span><span class="sxs-lookup"><span data-stu-id="88a00-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a00-134">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88a00-134">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a00-135">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a00-136">System-Only</span></span>            | <span data-ttu-id="88a00-137">True</span><span class="sxs-lookup"><span data-stu-id="88a00-137">True</span></span>                                                                                                                                      |
| <span data-ttu-id="88a00-138">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88a00-138">Is-Single-Valued</span></span>       | <span data-ttu-id="88a00-139">False</span><span class="sxs-lookup"><span data-stu-id="88a00-139">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-140">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88a00-140">Is Indexed</span></span>             | <span data-ttu-id="88a00-141">False</span><span class="sxs-lookup"><span data-stu-id="88a00-141">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-142">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88a00-142">In Global Catalog</span></span>      | <span data-ttu-id="88a00-143">False</span><span class="sxs-lookup"><span data-stu-id="88a00-143">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-144">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88a00-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a00-145">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88a00-145">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="88a00-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a00-146">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a00-147">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-148">Search-Flags</span></span>           | <span data-ttu-id="88a00-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a00-149">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-150">System-Flags</span></span>           | <span data-ttu-id="88a00-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a00-151">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-152">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88a00-152">Classes used in</span></span>        | [<span data-ttu-id="88a00-153">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="88a00-153">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="88a00-154">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="88a00-154">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="88a00-155">**DMD**</span><span class="sxs-lookup"><span data-stu-id="88a00-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="88a00-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="88a00-156">ADAM</span></span>



| <span data-ttu-id="88a00-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="88a00-157">Entry</span></span> | <span data-ttu-id="88a00-158">Value</span><span class="sxs-lookup"><span data-stu-id="88a00-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a00-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88a00-159">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a00-160">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a00-161">System-Only</span></span>            | <span data-ttu-id="88a00-162">True</span><span class="sxs-lookup"><span data-stu-id="88a00-162">True</span></span>                                                                                                                                      |
| <span data-ttu-id="88a00-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88a00-163">Is-Single-Valued</span></span>       | <span data-ttu-id="88a00-164">False</span><span class="sxs-lookup"><span data-stu-id="88a00-164">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88a00-165">Is Indexed</span></span>             | <span data-ttu-id="88a00-166">False</span><span class="sxs-lookup"><span data-stu-id="88a00-166">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88a00-167">In Global Catalog</span></span>      | <span data-ttu-id="88a00-168">False</span><span class="sxs-lookup"><span data-stu-id="88a00-168">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88a00-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a00-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88a00-170">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="88a00-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a00-171">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a00-172">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-173">Search-Flags</span></span>           | <span data-ttu-id="88a00-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a00-174">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-175">System-Flags</span></span>           | <span data-ttu-id="88a00-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a00-176">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88a00-177">Classes used in</span></span>        | [<span data-ttu-id="88a00-178">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="88a00-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="88a00-179">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="88a00-179">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="88a00-180">**DMD**</span><span class="sxs-lookup"><span data-stu-id="88a00-180">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88a00-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88a00-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88a00-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="88a00-182">Entry</span></span> | <span data-ttu-id="88a00-183">Value</span><span class="sxs-lookup"><span data-stu-id="88a00-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a00-184">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88a00-184">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a00-185">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a00-186">System-Only</span></span>            | <span data-ttu-id="88a00-187">True</span><span class="sxs-lookup"><span data-stu-id="88a00-187">True</span></span>                                                                                                                                      |
| <span data-ttu-id="88a00-188">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88a00-188">Is-Single-Valued</span></span>       | <span data-ttu-id="88a00-189">False</span><span class="sxs-lookup"><span data-stu-id="88a00-189">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-190">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88a00-190">Is Indexed</span></span>             | <span data-ttu-id="88a00-191">False</span><span class="sxs-lookup"><span data-stu-id="88a00-191">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-192">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88a00-192">In Global Catalog</span></span>      | <span data-ttu-id="88a00-193">False</span><span class="sxs-lookup"><span data-stu-id="88a00-193">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-194">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88a00-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a00-195">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88a00-195">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="88a00-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a00-196">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a00-197">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-198">Search-Flags</span></span>           | <span data-ttu-id="88a00-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a00-199">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-200">System-Flags</span></span>           | <span data-ttu-id="88a00-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a00-201">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-202">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88a00-202">Classes used in</span></span>        | [<span data-ttu-id="88a00-203">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="88a00-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="88a00-204">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="88a00-204">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="88a00-205">**DMD**</span><span class="sxs-lookup"><span data-stu-id="88a00-205">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88a00-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88a00-206">Windows Server 2008</span></span>



| <span data-ttu-id="88a00-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="88a00-207">Entry</span></span> | <span data-ttu-id="88a00-208">Value</span><span class="sxs-lookup"><span data-stu-id="88a00-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a00-209">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88a00-209">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a00-210">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a00-211">System-Only</span></span>            | <span data-ttu-id="88a00-212">True</span><span class="sxs-lookup"><span data-stu-id="88a00-212">True</span></span>                                                                                                                                      |
| <span data-ttu-id="88a00-213">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88a00-213">Is-Single-Valued</span></span>       | <span data-ttu-id="88a00-214">False</span><span class="sxs-lookup"><span data-stu-id="88a00-214">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-215">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88a00-215">Is Indexed</span></span>             | <span data-ttu-id="88a00-216">False</span><span class="sxs-lookup"><span data-stu-id="88a00-216">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-217">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88a00-217">In Global Catalog</span></span>      | <span data-ttu-id="88a00-218">False</span><span class="sxs-lookup"><span data-stu-id="88a00-218">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-219">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88a00-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a00-220">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88a00-220">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="88a00-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a00-221">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a00-222">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-223">Search-Flags</span></span>           | <span data-ttu-id="88a00-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a00-224">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-225">System-Flags</span></span>           | <span data-ttu-id="88a00-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a00-226">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-227">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88a00-227">Classes used in</span></span>        | [<span data-ttu-id="88a00-228">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="88a00-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="88a00-229">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="88a00-229">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="88a00-230">**DMD**</span><span class="sxs-lookup"><span data-stu-id="88a00-230">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88a00-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88a00-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88a00-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="88a00-232">Entry</span></span> | <span data-ttu-id="88a00-233">Value</span><span class="sxs-lookup"><span data-stu-id="88a00-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a00-234">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88a00-234">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a00-235">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a00-236">System-Only</span></span>            | <span data-ttu-id="88a00-237">True</span><span class="sxs-lookup"><span data-stu-id="88a00-237">True</span></span>                                                                                                                                      |
| <span data-ttu-id="88a00-238">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88a00-238">Is-Single-Valued</span></span>       | <span data-ttu-id="88a00-239">False</span><span class="sxs-lookup"><span data-stu-id="88a00-239">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-240">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88a00-240">Is Indexed</span></span>             | <span data-ttu-id="88a00-241">False</span><span class="sxs-lookup"><span data-stu-id="88a00-241">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-242">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88a00-242">In Global Catalog</span></span>      | <span data-ttu-id="88a00-243">False</span><span class="sxs-lookup"><span data-stu-id="88a00-243">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-244">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88a00-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a00-245">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88a00-245">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="88a00-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a00-246">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a00-247">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-248">Search-Flags</span></span>           | <span data-ttu-id="88a00-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a00-249">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-250">System-Flags</span></span>           | <span data-ttu-id="88a00-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a00-251">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-252">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88a00-252">Classes used in</span></span>        | [<span data-ttu-id="88a00-253">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="88a00-253">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="88a00-254">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="88a00-254">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="88a00-255">**DMD**</span><span class="sxs-lookup"><span data-stu-id="88a00-255">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88a00-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88a00-256">Windows Server 2012</span></span>



| <span data-ttu-id="88a00-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="88a00-257">Entry</span></span> | <span data-ttu-id="88a00-258">Value</span><span class="sxs-lookup"><span data-stu-id="88a00-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a00-259">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="88a00-259">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88a00-260">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="88a00-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="88a00-261">System-Only</span></span>            | <span data-ttu-id="88a00-262">True</span><span class="sxs-lookup"><span data-stu-id="88a00-262">True</span></span>                                                                                                                                      |
| <span data-ttu-id="88a00-263">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="88a00-263">Is-Single-Valued</span></span>       | <span data-ttu-id="88a00-264">False</span><span class="sxs-lookup"><span data-stu-id="88a00-264">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-265">Está indexado</span><span class="sxs-lookup"><span data-stu-id="88a00-265">Is Indexed</span></span>             | <span data-ttu-id="88a00-266">False</span><span class="sxs-lookup"><span data-stu-id="88a00-266">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-267">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="88a00-267">In Global Catalog</span></span>      | <span data-ttu-id="88a00-268">False</span><span class="sxs-lookup"><span data-stu-id="88a00-268">False</span></span>                                                                                                                                     |
| <span data-ttu-id="88a00-269">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="88a00-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="88a00-270">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="88a00-270">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="88a00-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88a00-271">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88a00-272">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="88a00-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-273">Search-Flags</span></span>           | <span data-ttu-id="88a00-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88a00-274">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88a00-275">System-Flags</span></span>           | <span data-ttu-id="88a00-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88a00-276">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="88a00-277">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="88a00-277">Classes used in</span></span>        | [<span data-ttu-id="88a00-278">**Attribute-Schema**</span><span class="sxs-lookup"><span data-stu-id="88a00-278">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="88a00-279">**Esquema de clase**</span><span class="sxs-lookup"><span data-stu-id="88a00-279">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="88a00-280">**DMD**</span><span class="sxs-lookup"><span data-stu-id="88a00-280">**DMD**</span></span>](c-dmd.md)<br/> |



 

 






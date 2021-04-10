---
title: Help-File-Name (atributo)
description: Este atributo se usó para Exchange 4,0. Contenía el nombre que se debe usar para el archivo cuando el proveedor descargó los datos de ayuda en un equipo cliente. No se utiliza para ninguna otra versión de Exchange.
ms.assetid: 3383b953-8a5c-4dfd-9d06-c35d29d6ea2d
ms.tgt_platform: multiple
keywords:
- Help-File-Name atributo AD Schema
- helpFileName esquema de AD de atributos
topic_type:
- apiref
api_name:
- Help-File-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e049e34fe43cb17314f8483a2a77bd680a4e7fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906079"
---
# <a name="help-file-name-attribute"></a><span data-ttu-id="5d426-107">Help-File-Name (atributo)</span><span class="sxs-lookup"><span data-stu-id="5d426-107">Help-File-Name attribute</span></span>

<span data-ttu-id="5d426-108">Este atributo se usó para Exchange 4,0.</span><span class="sxs-lookup"><span data-stu-id="5d426-108">This attribute was used for Exchange 4.0.</span></span> <span data-ttu-id="5d426-109">Contenía el nombre que se debe usar para el archivo cuando el proveedor descargó los datos de ayuda en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="5d426-109">It contained the name that should be used for the file when the provider downloaded help data to a client computer.</span></span> <span data-ttu-id="5d426-110">No se utiliza para ninguna otra versión de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d426-110">It is not used for any other versions of Exchange.</span></span>



| <span data-ttu-id="5d426-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="5d426-111">Entry</span></span> | <span data-ttu-id="5d426-112">Value</span><span class="sxs-lookup"><span data-stu-id="5d426-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5d426-113">CN</span><span class="sxs-lookup"><span data-stu-id="5d426-113">CN</span></span>                | <span data-ttu-id="5d426-114">Nombre de archivo de ayuda</span><span class="sxs-lookup"><span data-stu-id="5d426-114">Help-File-Name</span></span>                              |
| <span data-ttu-id="5d426-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5d426-115">Ldap-Display-Name</span></span> | <span data-ttu-id="5d426-116">helpFileName</span><span class="sxs-lookup"><span data-stu-id="5d426-116">helpFileName</span></span>                                |
| <span data-ttu-id="5d426-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5d426-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="5d426-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5d426-118">Update Privilege</span></span>  | <span data-ttu-id="5d426-119">Lo utiliza el sistema.</span><span class="sxs-lookup"><span data-stu-id="5d426-119">This is used by the system.</span></span>                 |
| <span data-ttu-id="5d426-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5d426-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5d426-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5d426-121">Attribute-Id</span></span>      | <span data-ttu-id="5d426-122">1.2.840.113556.1.2.327</span><span class="sxs-lookup"><span data-stu-id="5d426-122">1.2.840.113556.1.2.327</span></span>                      |
| <span data-ttu-id="5d426-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5d426-123">System-Id-Guid</span></span>    | <span data-ttu-id="5d426-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="5d426-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="5d426-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d426-125">Syntax</span></span>            | [<span data-ttu-id="5d426-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5d426-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5d426-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5d426-127">Implementations</span></span>

-   [<span data-ttu-id="5d426-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5d426-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5d426-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5d426-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5d426-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5d426-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5d426-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5d426-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5d426-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5d426-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5d426-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5d426-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5d426-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d426-134">Windows 2000 Server</span></span>



| <span data-ttu-id="5d426-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="5d426-135">Entry</span></span> | <span data-ttu-id="5d426-136">Value</span><span class="sxs-lookup"><span data-stu-id="5d426-136">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="5d426-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5d426-137">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="5d426-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d426-138">MAPI-Id</span></span>                | <span data-ttu-id="5d426-139">0x803B</span><span class="sxs-lookup"><span data-stu-id="5d426-139">0x803B</span></span>                                                   |
| <span data-ttu-id="5d426-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d426-140">System-Only</span></span>            | <span data-ttu-id="5d426-141">False</span><span class="sxs-lookup"><span data-stu-id="5d426-141">False</span></span>                                                    |
| <span data-ttu-id="5d426-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5d426-142">Is-Single-Valued</span></span>       | <span data-ttu-id="5d426-143">True</span><span class="sxs-lookup"><span data-stu-id="5d426-143">True</span></span>                                                     |
| <span data-ttu-id="5d426-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5d426-144">Is Indexed</span></span>             | <span data-ttu-id="5d426-145">False</span><span class="sxs-lookup"><span data-stu-id="5d426-145">False</span></span>                                                    |
| <span data-ttu-id="5d426-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5d426-146">In Global Catalog</span></span>      | <span data-ttu-id="5d426-147">False</span><span class="sxs-lookup"><span data-stu-id="5d426-147">False</span></span>                                                    |
| <span data-ttu-id="5d426-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5d426-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d426-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d426-149">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="5d426-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d426-150">Range-Lower</span></span>            | <span data-ttu-id="5d426-151">1</span><span class="sxs-lookup"><span data-stu-id="5d426-151">1</span></span>                                                        |
| <span data-ttu-id="5d426-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d426-152">Range-Upper</span></span>            | <span data-ttu-id="5d426-153">13</span><span class="sxs-lookup"><span data-stu-id="5d426-153">13</span></span>                                                       |
| <span data-ttu-id="5d426-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-154">Search-Flags</span></span>           | <span data-ttu-id="5d426-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d426-155">0x00000000</span></span>                                               |
| <span data-ttu-id="5d426-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-156">System-Flags</span></span>           | <span data-ttu-id="5d426-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d426-157">0x00000010</span></span>                                               |
| <span data-ttu-id="5d426-158">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5d426-158">Classes used in</span></span>        | [<span data-ttu-id="5d426-159">**Mostrar plantilla**</span><span class="sxs-lookup"><span data-stu-id="5d426-159">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5d426-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d426-160">Windows Server 2003</span></span>



| <span data-ttu-id="5d426-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="5d426-161">Entry</span></span> | <span data-ttu-id="5d426-162">Value</span><span class="sxs-lookup"><span data-stu-id="5d426-162">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="5d426-163">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5d426-163">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="5d426-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d426-164">MAPI-Id</span></span>                | <span data-ttu-id="5d426-165">0x803B</span><span class="sxs-lookup"><span data-stu-id="5d426-165">0x803B</span></span>                                                   |
| <span data-ttu-id="5d426-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d426-166">System-Only</span></span>            | <span data-ttu-id="5d426-167">False</span><span class="sxs-lookup"><span data-stu-id="5d426-167">False</span></span>                                                    |
| <span data-ttu-id="5d426-168">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5d426-168">Is-Single-Valued</span></span>       | <span data-ttu-id="5d426-169">True</span><span class="sxs-lookup"><span data-stu-id="5d426-169">True</span></span>                                                     |
| <span data-ttu-id="5d426-170">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5d426-170">Is Indexed</span></span>             | <span data-ttu-id="5d426-171">False</span><span class="sxs-lookup"><span data-stu-id="5d426-171">False</span></span>                                                    |
| <span data-ttu-id="5d426-172">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5d426-172">In Global Catalog</span></span>      | <span data-ttu-id="5d426-173">False</span><span class="sxs-lookup"><span data-stu-id="5d426-173">False</span></span>                                                    |
| <span data-ttu-id="5d426-174">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5d426-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d426-175">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d426-175">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="5d426-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d426-176">Range-Lower</span></span>            | <span data-ttu-id="5d426-177">1</span><span class="sxs-lookup"><span data-stu-id="5d426-177">1</span></span>                                                        |
| <span data-ttu-id="5d426-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d426-178">Range-Upper</span></span>            | <span data-ttu-id="5d426-179">13</span><span class="sxs-lookup"><span data-stu-id="5d426-179">13</span></span>                                                       |
| <span data-ttu-id="5d426-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-180">Search-Flags</span></span>           | <span data-ttu-id="5d426-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d426-181">0x00000000</span></span>                                               |
| <span data-ttu-id="5d426-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-182">System-Flags</span></span>           | <span data-ttu-id="5d426-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d426-183">0x00000010</span></span>                                               |
| <span data-ttu-id="5d426-184">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5d426-184">Classes used in</span></span>        | [<span data-ttu-id="5d426-185">**Mostrar plantilla**</span><span class="sxs-lookup"><span data-stu-id="5d426-185">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5d426-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5d426-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5d426-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="5d426-187">Entry</span></span> | <span data-ttu-id="5d426-188">Value</span><span class="sxs-lookup"><span data-stu-id="5d426-188">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="5d426-189">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5d426-189">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="5d426-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d426-190">MAPI-Id</span></span>                | <span data-ttu-id="5d426-191">0x803B</span><span class="sxs-lookup"><span data-stu-id="5d426-191">0x803B</span></span>                                                   |
| <span data-ttu-id="5d426-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d426-192">System-Only</span></span>            | <span data-ttu-id="5d426-193">False</span><span class="sxs-lookup"><span data-stu-id="5d426-193">False</span></span>                                                    |
| <span data-ttu-id="5d426-194">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5d426-194">Is-Single-Valued</span></span>       | <span data-ttu-id="5d426-195">True</span><span class="sxs-lookup"><span data-stu-id="5d426-195">True</span></span>                                                     |
| <span data-ttu-id="5d426-196">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5d426-196">Is Indexed</span></span>             | <span data-ttu-id="5d426-197">False</span><span class="sxs-lookup"><span data-stu-id="5d426-197">False</span></span>                                                    |
| <span data-ttu-id="5d426-198">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5d426-198">In Global Catalog</span></span>      | <span data-ttu-id="5d426-199">False</span><span class="sxs-lookup"><span data-stu-id="5d426-199">False</span></span>                                                    |
| <span data-ttu-id="5d426-200">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5d426-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d426-201">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d426-201">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="5d426-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d426-202">Range-Lower</span></span>            | <span data-ttu-id="5d426-203">1</span><span class="sxs-lookup"><span data-stu-id="5d426-203">1</span></span>                                                        |
| <span data-ttu-id="5d426-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d426-204">Range-Upper</span></span>            | <span data-ttu-id="5d426-205">13</span><span class="sxs-lookup"><span data-stu-id="5d426-205">13</span></span>                                                       |
| <span data-ttu-id="5d426-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-206">Search-Flags</span></span>           | <span data-ttu-id="5d426-207">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d426-207">0x00000000</span></span>                                               |
| <span data-ttu-id="5d426-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-208">System-Flags</span></span>           | <span data-ttu-id="5d426-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d426-209">0x00000010</span></span>                                               |
| <span data-ttu-id="5d426-210">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5d426-210">Classes used in</span></span>        | [<span data-ttu-id="5d426-211">**Mostrar plantilla**</span><span class="sxs-lookup"><span data-stu-id="5d426-211">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5d426-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d426-212">Windows Server 2008</span></span>



| <span data-ttu-id="5d426-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="5d426-213">Entry</span></span> | <span data-ttu-id="5d426-214">Value</span><span class="sxs-lookup"><span data-stu-id="5d426-214">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="5d426-215">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5d426-215">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="5d426-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d426-216">MAPI-Id</span></span>                | <span data-ttu-id="5d426-217">0x803B</span><span class="sxs-lookup"><span data-stu-id="5d426-217">0x803B</span></span>                                                   |
| <span data-ttu-id="5d426-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d426-218">System-Only</span></span>            | <span data-ttu-id="5d426-219">False</span><span class="sxs-lookup"><span data-stu-id="5d426-219">False</span></span>                                                    |
| <span data-ttu-id="5d426-220">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5d426-220">Is-Single-Valued</span></span>       | <span data-ttu-id="5d426-221">True</span><span class="sxs-lookup"><span data-stu-id="5d426-221">True</span></span>                                                     |
| <span data-ttu-id="5d426-222">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5d426-222">Is Indexed</span></span>             | <span data-ttu-id="5d426-223">False</span><span class="sxs-lookup"><span data-stu-id="5d426-223">False</span></span>                                                    |
| <span data-ttu-id="5d426-224">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5d426-224">In Global Catalog</span></span>      | <span data-ttu-id="5d426-225">False</span><span class="sxs-lookup"><span data-stu-id="5d426-225">False</span></span>                                                    |
| <span data-ttu-id="5d426-226">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5d426-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d426-227">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d426-227">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="5d426-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d426-228">Range-Lower</span></span>            | <span data-ttu-id="5d426-229">1</span><span class="sxs-lookup"><span data-stu-id="5d426-229">1</span></span>                                                        |
| <span data-ttu-id="5d426-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d426-230">Range-Upper</span></span>            | <span data-ttu-id="5d426-231">13</span><span class="sxs-lookup"><span data-stu-id="5d426-231">13</span></span>                                                       |
| <span data-ttu-id="5d426-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-232">Search-Flags</span></span>           | <span data-ttu-id="5d426-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d426-233">0x00000000</span></span>                                               |
| <span data-ttu-id="5d426-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-234">System-Flags</span></span>           | <span data-ttu-id="5d426-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d426-235">0x00000010</span></span>                                               |
| <span data-ttu-id="5d426-236">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5d426-236">Classes used in</span></span>        | [<span data-ttu-id="5d426-237">**Mostrar plantilla**</span><span class="sxs-lookup"><span data-stu-id="5d426-237">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5d426-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d426-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5d426-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="5d426-239">Entry</span></span> | <span data-ttu-id="5d426-240">Value</span><span class="sxs-lookup"><span data-stu-id="5d426-240">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="5d426-241">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5d426-241">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="5d426-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d426-242">MAPI-Id</span></span>                | <span data-ttu-id="5d426-243">0x803B</span><span class="sxs-lookup"><span data-stu-id="5d426-243">0x803B</span></span>                                                   |
| <span data-ttu-id="5d426-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d426-244">System-Only</span></span>            | <span data-ttu-id="5d426-245">False</span><span class="sxs-lookup"><span data-stu-id="5d426-245">False</span></span>                                                    |
| <span data-ttu-id="5d426-246">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5d426-246">Is-Single-Valued</span></span>       | <span data-ttu-id="5d426-247">True</span><span class="sxs-lookup"><span data-stu-id="5d426-247">True</span></span>                                                     |
| <span data-ttu-id="5d426-248">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5d426-248">Is Indexed</span></span>             | <span data-ttu-id="5d426-249">False</span><span class="sxs-lookup"><span data-stu-id="5d426-249">False</span></span>                                                    |
| <span data-ttu-id="5d426-250">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5d426-250">In Global Catalog</span></span>      | <span data-ttu-id="5d426-251">False</span><span class="sxs-lookup"><span data-stu-id="5d426-251">False</span></span>                                                    |
| <span data-ttu-id="5d426-252">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5d426-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d426-253">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d426-253">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="5d426-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d426-254">Range-Lower</span></span>            | <span data-ttu-id="5d426-255">1</span><span class="sxs-lookup"><span data-stu-id="5d426-255">1</span></span>                                                        |
| <span data-ttu-id="5d426-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d426-256">Range-Upper</span></span>            | <span data-ttu-id="5d426-257">13</span><span class="sxs-lookup"><span data-stu-id="5d426-257">13</span></span>                                                       |
| <span data-ttu-id="5d426-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-258">Search-Flags</span></span>           | <span data-ttu-id="5d426-259">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d426-259">0x00000000</span></span>                                               |
| <span data-ttu-id="5d426-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-260">System-Flags</span></span>           | <span data-ttu-id="5d426-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d426-261">0x00000010</span></span>                                               |
| <span data-ttu-id="5d426-262">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5d426-262">Classes used in</span></span>        | [<span data-ttu-id="5d426-263">**Mostrar plantilla**</span><span class="sxs-lookup"><span data-stu-id="5d426-263">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5d426-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d426-264">Windows Server 2012</span></span>



| <span data-ttu-id="5d426-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="5d426-265">Entry</span></span> | <span data-ttu-id="5d426-266">Value</span><span class="sxs-lookup"><span data-stu-id="5d426-266">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="5d426-267">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5d426-267">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="5d426-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5d426-268">MAPI-Id</span></span>                | <span data-ttu-id="5d426-269">0x803B</span><span class="sxs-lookup"><span data-stu-id="5d426-269">0x803B</span></span>                                                   |
| <span data-ttu-id="5d426-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="5d426-270">System-Only</span></span>            | <span data-ttu-id="5d426-271">False</span><span class="sxs-lookup"><span data-stu-id="5d426-271">False</span></span>                                                    |
| <span data-ttu-id="5d426-272">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5d426-272">Is-Single-Valued</span></span>       | <span data-ttu-id="5d426-273">True</span><span class="sxs-lookup"><span data-stu-id="5d426-273">True</span></span>                                                     |
| <span data-ttu-id="5d426-274">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5d426-274">Is Indexed</span></span>             | <span data-ttu-id="5d426-275">False</span><span class="sxs-lookup"><span data-stu-id="5d426-275">False</span></span>                                                    |
| <span data-ttu-id="5d426-276">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5d426-276">In Global Catalog</span></span>      | <span data-ttu-id="5d426-277">False</span><span class="sxs-lookup"><span data-stu-id="5d426-277">False</span></span>                                                    |
| <span data-ttu-id="5d426-278">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5d426-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="5d426-279">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5d426-279">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="5d426-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5d426-280">Range-Lower</span></span>            | <span data-ttu-id="5d426-281">1</span><span class="sxs-lookup"><span data-stu-id="5d426-281">1</span></span>                                                        |
| <span data-ttu-id="5d426-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5d426-282">Range-Upper</span></span>            | <span data-ttu-id="5d426-283">13</span><span class="sxs-lookup"><span data-stu-id="5d426-283">13</span></span>                                                       |
| <span data-ttu-id="5d426-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-284">Search-Flags</span></span>           | <span data-ttu-id="5d426-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d426-285">0x00000000</span></span>                                               |
| <span data-ttu-id="5d426-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5d426-286">System-Flags</span></span>           | <span data-ttu-id="5d426-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5d426-287">0x00000010</span></span>                                               |
| <span data-ttu-id="5d426-288">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5d426-288">Classes used in</span></span>        | [<span data-ttu-id="5d426-289">**Mostrar plantilla**</span><span class="sxs-lookup"><span data-stu-id="5d426-289">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



 

 






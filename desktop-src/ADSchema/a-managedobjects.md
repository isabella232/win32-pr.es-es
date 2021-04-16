---
title: Managed-Objects atributo)
description: Contiene la lista de objetos administrados por el usuario. Los objetos que se muestran son aquellos que tienen la propiedad managedBy de propiedad establecida en este usuario. Cada elemento de la lista es una referencia vinculada al objeto administrado.
ms.assetid: 59b76431-03a5-4839-8800-ef03d26b66cc
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Managed-Objects
- managedObjects esquema de AD de atributos
topic_type:
- apiref
api_name:
- Managed-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c7bc489d11c99f8790426a531e09a20f133476
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658617"
---
# <a name="managed-objects-attribute"></a><span data-ttu-id="1e09a-107">Managed-Objects atributo)</span><span class="sxs-lookup"><span data-stu-id="1e09a-107">Managed-Objects attribute</span></span>

<span data-ttu-id="1e09a-108">Contiene la lista de objetos administrados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1e09a-108">Contains the list of objects that are managed by the user.</span></span> <span data-ttu-id="1e09a-109">Los objetos que se muestran son aquellos que tienen la propiedad managedBy de propiedad establecida en este usuario.</span><span class="sxs-lookup"><span data-stu-id="1e09a-109">The objects listed are those that have the property managedBy property set to this user.</span></span> <span data-ttu-id="1e09a-110">Cada elemento de la lista es una referencia vinculada al objeto administrado.</span><span class="sxs-lookup"><span data-stu-id="1e09a-110">Each item in the list is a linked reference to the managed object.</span></span>



| <span data-ttu-id="1e09a-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e09a-111">Entry</span></span> | <span data-ttu-id="1e09a-112">Value</span><span class="sxs-lookup"><span data-stu-id="1e09a-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e09a-113">CN</span><span class="sxs-lookup"><span data-stu-id="1e09a-113">CN</span></span>                | <span data-ttu-id="1e09a-114">Managed-Objects</span><span class="sxs-lookup"><span data-stu-id="1e09a-114">Managed-Objects</span></span>                                                                    |
| <span data-ttu-id="1e09a-115">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="1e09a-115">Ldap-Display-Name</span></span> | <span data-ttu-id="1e09a-116">managedObjects</span><span class="sxs-lookup"><span data-stu-id="1e09a-116">managedObjects</span></span>                                                                     |
| <span data-ttu-id="1e09a-117">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1e09a-117">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="1e09a-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="1e09a-118">Update Privilege</span></span>  | <span data-ttu-id="1e09a-119">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="1e09a-119">This value is set by the system.</span></span>                                                   |
| <span data-ttu-id="1e09a-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="1e09a-120">Update Frequency</span></span>  | <span data-ttu-id="1e09a-121">Cuando se crea el registro de usuarios y cada vez que es necesario cambiar los objetos administrados.</span><span class="sxs-lookup"><span data-stu-id="1e09a-121">When the users record is created and whenever the managed objects needs to change.</span></span> |
| <span data-ttu-id="1e09a-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1e09a-122">Attribute-Id</span></span>      | <span data-ttu-id="1e09a-123">1.2.840.113556.1.4.654</span><span class="sxs-lookup"><span data-stu-id="1e09a-123">1.2.840.113556.1.4.654</span></span>                                                             |
| <span data-ttu-id="1e09a-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1e09a-124">System-Id-Guid</span></span>    | <span data-ttu-id="1e09a-125">0296c124-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1e09a-125">0296c124-40da-11d1-a9c0-0000f80367c1</span></span>                                               |
| <span data-ttu-id="1e09a-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e09a-126">Syntax</span></span>            | [<span data-ttu-id="1e09a-127">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1e09a-127">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                            |



## <a name="implementations"></a><span data-ttu-id="1e09a-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="1e09a-128">Implementations</span></span>

-   [<span data-ttu-id="1e09a-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1e09a-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1e09a-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1e09a-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1e09a-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1e09a-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1e09a-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1e09a-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1e09a-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1e09a-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1e09a-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1e09a-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1e09a-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1e09a-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1e09a-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e09a-136">Windows 2000 Server</span></span>



| <span data-ttu-id="1e09a-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e09a-137">Entry</span></span> | <span data-ttu-id="1e09a-138">Value</span><span class="sxs-lookup"><span data-stu-id="1e09a-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e09a-139">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e09a-139">Link-Id</span></span>                | <span data-ttu-id="1e09a-140">73</span><span class="sxs-lookup"><span data-stu-id="1e09a-140">73</span></span>                              |
| <span data-ttu-id="1e09a-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e09a-141">MAPI-Id</span></span>                | <span data-ttu-id="1e09a-142">0x8024</span><span class="sxs-lookup"><span data-stu-id="1e09a-142">0x8024</span></span>                          |
| <span data-ttu-id="1e09a-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e09a-143">System-Only</span></span>            | <span data-ttu-id="1e09a-144">True</span><span class="sxs-lookup"><span data-stu-id="1e09a-144">True</span></span>                            |
| <span data-ttu-id="1e09a-145">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e09a-145">Is-Single-Valued</span></span>       | <span data-ttu-id="1e09a-146">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-146">False</span></span>                           |
| <span data-ttu-id="1e09a-147">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e09a-147">Is Indexed</span></span>             | <span data-ttu-id="1e09a-148">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-148">False</span></span>                           |
| <span data-ttu-id="1e09a-149">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e09a-149">In Global Catalog</span></span>      | <span data-ttu-id="1e09a-150">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-150">False</span></span>                           |
| <span data-ttu-id="1e09a-151">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e09a-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e09a-152">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e09a-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e09a-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e09a-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e09a-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e09a-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e09a-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-155">Search-Flags</span></span>           | <span data-ttu-id="1e09a-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e09a-156">0x00000000</span></span>                      |
| <span data-ttu-id="1e09a-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-157">System-Flags</span></span>           | <span data-ttu-id="1e09a-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e09a-158">0x00000010</span></span>                      |
| <span data-ttu-id="1e09a-159">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e09a-159">Classes used in</span></span>        | [<span data-ttu-id="1e09a-160">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e09a-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1e09a-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e09a-161">Windows Server 2003</span></span>



| <span data-ttu-id="1e09a-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e09a-162">Entry</span></span> | <span data-ttu-id="1e09a-163">Value</span><span class="sxs-lookup"><span data-stu-id="1e09a-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e09a-164">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e09a-164">Link-Id</span></span>                | <span data-ttu-id="1e09a-165">73</span><span class="sxs-lookup"><span data-stu-id="1e09a-165">73</span></span>                              |
| <span data-ttu-id="1e09a-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e09a-166">MAPI-Id</span></span>                | <span data-ttu-id="1e09a-167">0x8024</span><span class="sxs-lookup"><span data-stu-id="1e09a-167">0x8024</span></span>                          |
| <span data-ttu-id="1e09a-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e09a-168">System-Only</span></span>            | <span data-ttu-id="1e09a-169">True</span><span class="sxs-lookup"><span data-stu-id="1e09a-169">True</span></span>                            |
| <span data-ttu-id="1e09a-170">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e09a-170">Is-Single-Valued</span></span>       | <span data-ttu-id="1e09a-171">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-171">False</span></span>                           |
| <span data-ttu-id="1e09a-172">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e09a-172">Is Indexed</span></span>             | <span data-ttu-id="1e09a-173">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-173">False</span></span>                           |
| <span data-ttu-id="1e09a-174">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e09a-174">In Global Catalog</span></span>      | <span data-ttu-id="1e09a-175">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-175">False</span></span>                           |
| <span data-ttu-id="1e09a-176">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e09a-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e09a-177">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e09a-177">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e09a-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e09a-178">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e09a-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e09a-179">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e09a-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-180">Search-Flags</span></span>           | <span data-ttu-id="1e09a-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e09a-181">0x00000000</span></span>                      |
| <span data-ttu-id="1e09a-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-182">System-Flags</span></span>           | <span data-ttu-id="1e09a-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e09a-183">0x00000010</span></span>                      |
| <span data-ttu-id="1e09a-184">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e09a-184">Classes used in</span></span>        | [<span data-ttu-id="1e09a-185">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e09a-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1e09a-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="1e09a-186">ADAM</span></span>



| <span data-ttu-id="1e09a-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e09a-187">Entry</span></span> | <span data-ttu-id="1e09a-188">Value</span><span class="sxs-lookup"><span data-stu-id="1e09a-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e09a-189">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e09a-189">Link-Id</span></span>                | <span data-ttu-id="1e09a-190">73</span><span class="sxs-lookup"><span data-stu-id="1e09a-190">73</span></span>                              |
| <span data-ttu-id="1e09a-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e09a-191">MAPI-Id</span></span>                | <span data-ttu-id="1e09a-192">0x8024</span><span class="sxs-lookup"><span data-stu-id="1e09a-192">0x8024</span></span>                          |
| <span data-ttu-id="1e09a-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e09a-193">System-Only</span></span>            | <span data-ttu-id="1e09a-194">True</span><span class="sxs-lookup"><span data-stu-id="1e09a-194">True</span></span>                            |
| <span data-ttu-id="1e09a-195">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e09a-195">Is-Single-Valued</span></span>       | <span data-ttu-id="1e09a-196">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-196">False</span></span>                           |
| <span data-ttu-id="1e09a-197">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e09a-197">Is Indexed</span></span>             | <span data-ttu-id="1e09a-198">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-198">False</span></span>                           |
| <span data-ttu-id="1e09a-199">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e09a-199">In Global Catalog</span></span>      | <span data-ttu-id="1e09a-200">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-200">False</span></span>                           |
| <span data-ttu-id="1e09a-201">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e09a-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e09a-202">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e09a-202">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e09a-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e09a-203">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e09a-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e09a-204">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e09a-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-205">Search-Flags</span></span>           | <span data-ttu-id="1e09a-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e09a-206">0x00000000</span></span>                      |
| <span data-ttu-id="1e09a-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-207">System-Flags</span></span>           | <span data-ttu-id="1e09a-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e09a-208">0x00000010</span></span>                      |
| <span data-ttu-id="1e09a-209">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e09a-209">Classes used in</span></span>        | [<span data-ttu-id="1e09a-210">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e09a-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1e09a-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1e09a-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1e09a-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e09a-212">Entry</span></span> | <span data-ttu-id="1e09a-213">Value</span><span class="sxs-lookup"><span data-stu-id="1e09a-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e09a-214">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e09a-214">Link-Id</span></span>                | <span data-ttu-id="1e09a-215">73</span><span class="sxs-lookup"><span data-stu-id="1e09a-215">73</span></span>                              |
| <span data-ttu-id="1e09a-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e09a-216">MAPI-Id</span></span>                | <span data-ttu-id="1e09a-217">0x8024</span><span class="sxs-lookup"><span data-stu-id="1e09a-217">0x8024</span></span>                          |
| <span data-ttu-id="1e09a-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e09a-218">System-Only</span></span>            | <span data-ttu-id="1e09a-219">True</span><span class="sxs-lookup"><span data-stu-id="1e09a-219">True</span></span>                            |
| <span data-ttu-id="1e09a-220">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e09a-220">Is-Single-Valued</span></span>       | <span data-ttu-id="1e09a-221">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-221">False</span></span>                           |
| <span data-ttu-id="1e09a-222">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e09a-222">Is Indexed</span></span>             | <span data-ttu-id="1e09a-223">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-223">False</span></span>                           |
| <span data-ttu-id="1e09a-224">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e09a-224">In Global Catalog</span></span>      | <span data-ttu-id="1e09a-225">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-225">False</span></span>                           |
| <span data-ttu-id="1e09a-226">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e09a-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e09a-227">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e09a-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e09a-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e09a-228">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e09a-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e09a-229">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e09a-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-230">Search-Flags</span></span>           | <span data-ttu-id="1e09a-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e09a-231">0x00000000</span></span>                      |
| <span data-ttu-id="1e09a-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-232">System-Flags</span></span>           | <span data-ttu-id="1e09a-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e09a-233">0x00000010</span></span>                      |
| <span data-ttu-id="1e09a-234">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e09a-234">Classes used in</span></span>        | [<span data-ttu-id="1e09a-235">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e09a-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1e09a-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e09a-236">Windows Server 2008</span></span>



| <span data-ttu-id="1e09a-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e09a-237">Entry</span></span> | <span data-ttu-id="1e09a-238">Value</span><span class="sxs-lookup"><span data-stu-id="1e09a-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e09a-239">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e09a-239">Link-Id</span></span>                | <span data-ttu-id="1e09a-240">73</span><span class="sxs-lookup"><span data-stu-id="1e09a-240">73</span></span>                              |
| <span data-ttu-id="1e09a-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e09a-241">MAPI-Id</span></span>                | <span data-ttu-id="1e09a-242">0x8024</span><span class="sxs-lookup"><span data-stu-id="1e09a-242">0x8024</span></span>                          |
| <span data-ttu-id="1e09a-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e09a-243">System-Only</span></span>            | <span data-ttu-id="1e09a-244">True</span><span class="sxs-lookup"><span data-stu-id="1e09a-244">True</span></span>                            |
| <span data-ttu-id="1e09a-245">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e09a-245">Is-Single-Valued</span></span>       | <span data-ttu-id="1e09a-246">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-246">False</span></span>                           |
| <span data-ttu-id="1e09a-247">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e09a-247">Is Indexed</span></span>             | <span data-ttu-id="1e09a-248">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-248">False</span></span>                           |
| <span data-ttu-id="1e09a-249">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e09a-249">In Global Catalog</span></span>      | <span data-ttu-id="1e09a-250">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-250">False</span></span>                           |
| <span data-ttu-id="1e09a-251">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e09a-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e09a-252">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e09a-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e09a-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e09a-253">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e09a-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e09a-254">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e09a-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-255">Search-Flags</span></span>           | <span data-ttu-id="1e09a-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e09a-256">0x00000000</span></span>                      |
| <span data-ttu-id="1e09a-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-257">System-Flags</span></span>           | <span data-ttu-id="1e09a-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e09a-258">0x00000010</span></span>                      |
| <span data-ttu-id="1e09a-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e09a-259">Classes used in</span></span>        | [<span data-ttu-id="1e09a-260">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e09a-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1e09a-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e09a-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1e09a-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e09a-262">Entry</span></span> | <span data-ttu-id="1e09a-263">Value</span><span class="sxs-lookup"><span data-stu-id="1e09a-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e09a-264">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e09a-264">Link-Id</span></span>                | <span data-ttu-id="1e09a-265">73</span><span class="sxs-lookup"><span data-stu-id="1e09a-265">73</span></span>                              |
| <span data-ttu-id="1e09a-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e09a-266">MAPI-Id</span></span>                | <span data-ttu-id="1e09a-267">0x8024</span><span class="sxs-lookup"><span data-stu-id="1e09a-267">0x8024</span></span>                          |
| <span data-ttu-id="1e09a-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e09a-268">System-Only</span></span>            | <span data-ttu-id="1e09a-269">True</span><span class="sxs-lookup"><span data-stu-id="1e09a-269">True</span></span>                            |
| <span data-ttu-id="1e09a-270">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e09a-270">Is-Single-Valued</span></span>       | <span data-ttu-id="1e09a-271">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-271">False</span></span>                           |
| <span data-ttu-id="1e09a-272">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e09a-272">Is Indexed</span></span>             | <span data-ttu-id="1e09a-273">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-273">False</span></span>                           |
| <span data-ttu-id="1e09a-274">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e09a-274">In Global Catalog</span></span>      | <span data-ttu-id="1e09a-275">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-275">False</span></span>                           |
| <span data-ttu-id="1e09a-276">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e09a-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e09a-277">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e09a-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e09a-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e09a-278">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e09a-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e09a-279">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e09a-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-280">Search-Flags</span></span>           | <span data-ttu-id="1e09a-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e09a-281">0x00000000</span></span>                      |
| <span data-ttu-id="1e09a-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-282">System-Flags</span></span>           | <span data-ttu-id="1e09a-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e09a-283">0x00000010</span></span>                      |
| <span data-ttu-id="1e09a-284">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e09a-284">Classes used in</span></span>        | [<span data-ttu-id="1e09a-285">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e09a-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1e09a-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e09a-286">Windows Server 2012</span></span>



| <span data-ttu-id="1e09a-287">Entrada</span><span class="sxs-lookup"><span data-stu-id="1e09a-287">Entry</span></span> | <span data-ttu-id="1e09a-288">Value</span><span class="sxs-lookup"><span data-stu-id="1e09a-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1e09a-289">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="1e09a-289">Link-Id</span></span>                | <span data-ttu-id="1e09a-290">73</span><span class="sxs-lookup"><span data-stu-id="1e09a-290">73</span></span>                              |
| <span data-ttu-id="1e09a-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e09a-291">MAPI-Id</span></span>                | <span data-ttu-id="1e09a-292">0x8024</span><span class="sxs-lookup"><span data-stu-id="1e09a-292">0x8024</span></span>                          |
| <span data-ttu-id="1e09a-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e09a-293">System-Only</span></span>            | <span data-ttu-id="1e09a-294">True</span><span class="sxs-lookup"><span data-stu-id="1e09a-294">True</span></span>                            |
| <span data-ttu-id="1e09a-295">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="1e09a-295">Is-Single-Valued</span></span>       | <span data-ttu-id="1e09a-296">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-296">False</span></span>                           |
| <span data-ttu-id="1e09a-297">Está indexado</span><span class="sxs-lookup"><span data-stu-id="1e09a-297">Is Indexed</span></span>             | <span data-ttu-id="1e09a-298">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-298">False</span></span>                           |
| <span data-ttu-id="1e09a-299">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="1e09a-299">In Global Catalog</span></span>      | <span data-ttu-id="1e09a-300">False</span><span class="sxs-lookup"><span data-stu-id="1e09a-300">False</span></span>                           |
| <span data-ttu-id="1e09a-301">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="1e09a-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e09a-302">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e09a-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1e09a-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e09a-303">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1e09a-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e09a-304">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1e09a-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-305">Search-Flags</span></span>           | <span data-ttu-id="1e09a-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e09a-306">0x00000000</span></span>                      |
| <span data-ttu-id="1e09a-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e09a-307">System-Flags</span></span>           | <span data-ttu-id="1e09a-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e09a-308">0x00000010</span></span>                      |
| <span data-ttu-id="1e09a-309">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="1e09a-309">Classes used in</span></span>        | [<span data-ttu-id="1e09a-310">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="1e09a-310">**Top**</span></span>](c-top.md)<br/> |



 

 






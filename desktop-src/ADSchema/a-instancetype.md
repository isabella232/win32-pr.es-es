---
title: Instance-Type atributo)
description: Un campo de bits que determina cómo se crea una instancia del objeto en un servidor determinado.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Instance-Type
- instanceType esquema de AD de atributos
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804777"
---
# <a name="instance-type-attribute"></a><span data-ttu-id="29663-105">Instance-Type atributo)</span><span class="sxs-lookup"><span data-stu-id="29663-105">Instance-Type attribute</span></span>

<span data-ttu-id="29663-106">Un campo de bits que determina cómo se crea una instancia del objeto en un servidor determinado.</span><span class="sxs-lookup"><span data-stu-id="29663-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="29663-107">El valor de este atributo puede diferir en las distintas réplicas, incluso si las réplicas están sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="29663-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="29663-108">Este atributo puede ser cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="29663-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="29663-109">Value</span><span class="sxs-lookup"><span data-stu-id="29663-109">Value</span></span>      | <span data-ttu-id="29663-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="29663-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29663-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="29663-111">0x00000001</span></span> | <span data-ttu-id="29663-112">Encabezado del contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="29663-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="29663-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="29663-113">0x00000002</span></span> | <span data-ttu-id="29663-114">No se crea una instancia de esta réplica.</span><span class="sxs-lookup"><span data-stu-id="29663-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="29663-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="29663-115">0x00000004</span></span> | <span data-ttu-id="29663-116">El objeto es grabable en este directorio.</span><span class="sxs-lookup"><span data-stu-id="29663-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="29663-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="29663-117">0x00000008</span></span> | <span data-ttu-id="29663-118">Se mantiene el contexto de nomenclatura por encima de este en este directorio.</span><span class="sxs-lookup"><span data-stu-id="29663-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="29663-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29663-119">0x00000010</span></span> | <span data-ttu-id="29663-120">El contexto de nomenclatura está en proceso de construirse por primera vez mediante la replicación.</span><span class="sxs-lookup"><span data-stu-id="29663-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="29663-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="29663-121">0x00000020</span></span> | <span data-ttu-id="29663-122">El contexto de nomenclatura está en proceso de quitarse del DSA local.</span><span class="sxs-lookup"><span data-stu-id="29663-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="29663-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="29663-123">Entry</span></span> | <span data-ttu-id="29663-124">Value</span><span class="sxs-lookup"><span data-stu-id="29663-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="29663-125">CN</span><span class="sxs-lookup"><span data-stu-id="29663-125">CN</span></span>                | <span data-ttu-id="29663-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="29663-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="29663-127">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="29663-127">Ldap-Display-Name</span></span> | <span data-ttu-id="29663-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="29663-128">instanceType</span></span>                                   |
| <span data-ttu-id="29663-129">Tamaño</span><span class="sxs-lookup"><span data-stu-id="29663-129">Size</span></span>              | <span data-ttu-id="29663-130">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="29663-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="29663-131">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="29663-131">Update Privilege</span></span>  | <span data-ttu-id="29663-132">El administrador del esquema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="29663-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="29663-133">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="29663-133">Update Frequency</span></span>  | <span data-ttu-id="29663-134">Cuando se crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="29663-134">When the object is created.</span></span>                    |
| <span data-ttu-id="29663-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29663-135">Attribute-Id</span></span>      | <span data-ttu-id="29663-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="29663-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="29663-137">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="29663-137">System-Id-Guid</span></span>    | <span data-ttu-id="29663-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="29663-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="29663-139">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29663-139">Syntax</span></span>            | [<span data-ttu-id="29663-140">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="29663-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="29663-141">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="29663-141">Implementations</span></span>

-   [<span data-ttu-id="29663-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="29663-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="29663-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29663-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29663-144">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="29663-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="29663-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29663-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29663-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29663-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29663-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29663-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29663-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29663-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="29663-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29663-149">Windows 2000 Server</span></span>



| <span data-ttu-id="29663-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="29663-150">Entry</span></span> | <span data-ttu-id="29663-151">Value</span><span class="sxs-lookup"><span data-stu-id="29663-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="29663-152">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29663-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="29663-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29663-153">MAPI-Id</span></span>                | <span data-ttu-id="29663-154">0x80BD</span><span class="sxs-lookup"><span data-stu-id="29663-154">0x80BD</span></span>                          |
| <span data-ttu-id="29663-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="29663-155">System-Only</span></span>            | <span data-ttu-id="29663-156">True</span><span class="sxs-lookup"><span data-stu-id="29663-156">True</span></span>                            |
| <span data-ttu-id="29663-157">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29663-157">Is-Single-Valued</span></span>       | <span data-ttu-id="29663-158">True</span><span class="sxs-lookup"><span data-stu-id="29663-158">True</span></span>                            |
| <span data-ttu-id="29663-159">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29663-159">Is Indexed</span></span>             | <span data-ttu-id="29663-160">False</span><span class="sxs-lookup"><span data-stu-id="29663-160">False</span></span>                           |
| <span data-ttu-id="29663-161">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29663-161">In Global Catalog</span></span>      | <span data-ttu-id="29663-162">True</span><span class="sxs-lookup"><span data-stu-id="29663-162">True</span></span>                            |
| <span data-ttu-id="29663-163">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29663-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="29663-164">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29663-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="29663-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29663-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="29663-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29663-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="29663-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-167">Search-Flags</span></span>           | <span data-ttu-id="29663-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="29663-168">0x00000008</span></span>                      |
| <span data-ttu-id="29663-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-169">System-Flags</span></span>           | <span data-ttu-id="29663-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29663-170">0x00000012</span></span>                      |
| <span data-ttu-id="29663-171">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29663-171">Classes used in</span></span>        | [<span data-ttu-id="29663-172">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="29663-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="29663-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29663-173">Windows Server 2003</span></span>



| <span data-ttu-id="29663-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="29663-174">Entry</span></span> | <span data-ttu-id="29663-175">Value</span><span class="sxs-lookup"><span data-stu-id="29663-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="29663-176">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29663-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="29663-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29663-177">MAPI-Id</span></span>                | <span data-ttu-id="29663-178">0x80BD</span><span class="sxs-lookup"><span data-stu-id="29663-178">0x80BD</span></span>                          |
| <span data-ttu-id="29663-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="29663-179">System-Only</span></span>            | <span data-ttu-id="29663-180">True</span><span class="sxs-lookup"><span data-stu-id="29663-180">True</span></span>                            |
| <span data-ttu-id="29663-181">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29663-181">Is-Single-Valued</span></span>       | <span data-ttu-id="29663-182">True</span><span class="sxs-lookup"><span data-stu-id="29663-182">True</span></span>                            |
| <span data-ttu-id="29663-183">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29663-183">Is Indexed</span></span>             | <span data-ttu-id="29663-184">False</span><span class="sxs-lookup"><span data-stu-id="29663-184">False</span></span>                           |
| <span data-ttu-id="29663-185">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29663-185">In Global Catalog</span></span>      | <span data-ttu-id="29663-186">True</span><span class="sxs-lookup"><span data-stu-id="29663-186">True</span></span>                            |
| <span data-ttu-id="29663-187">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29663-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="29663-188">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29663-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="29663-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29663-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="29663-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29663-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="29663-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-191">Search-Flags</span></span>           | <span data-ttu-id="29663-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="29663-192">0x00000008</span></span>                      |
| <span data-ttu-id="29663-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-193">System-Flags</span></span>           | <span data-ttu-id="29663-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29663-194">0x00000012</span></span>                      |
| <span data-ttu-id="29663-195">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29663-195">Classes used in</span></span>        | [<span data-ttu-id="29663-196">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="29663-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="29663-197">ADAM</span><span class="sxs-lookup"><span data-stu-id="29663-197">ADAM</span></span>



| <span data-ttu-id="29663-198">Entrada</span><span class="sxs-lookup"><span data-stu-id="29663-198">Entry</span></span> | <span data-ttu-id="29663-199">Value</span><span class="sxs-lookup"><span data-stu-id="29663-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="29663-200">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29663-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="29663-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29663-201">MAPI-Id</span></span>                | <span data-ttu-id="29663-202">0x80BD</span><span class="sxs-lookup"><span data-stu-id="29663-202">0x80BD</span></span>                          |
| <span data-ttu-id="29663-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="29663-203">System-Only</span></span>            | <span data-ttu-id="29663-204">True</span><span class="sxs-lookup"><span data-stu-id="29663-204">True</span></span>                            |
| <span data-ttu-id="29663-205">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29663-205">Is-Single-Valued</span></span>       | <span data-ttu-id="29663-206">True</span><span class="sxs-lookup"><span data-stu-id="29663-206">True</span></span>                            |
| <span data-ttu-id="29663-207">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29663-207">Is Indexed</span></span>             | <span data-ttu-id="29663-208">False</span><span class="sxs-lookup"><span data-stu-id="29663-208">False</span></span>                           |
| <span data-ttu-id="29663-209">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29663-209">In Global Catalog</span></span>      | <span data-ttu-id="29663-210">True</span><span class="sxs-lookup"><span data-stu-id="29663-210">True</span></span>                            |
| <span data-ttu-id="29663-211">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29663-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="29663-212">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29663-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="29663-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29663-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="29663-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29663-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="29663-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-215">Search-Flags</span></span>           | <span data-ttu-id="29663-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="29663-216">0x00000008</span></span>                      |
| <span data-ttu-id="29663-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-217">System-Flags</span></span>           | <span data-ttu-id="29663-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29663-218">0x00000012</span></span>                      |
| <span data-ttu-id="29663-219">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29663-219">Classes used in</span></span>        | [<span data-ttu-id="29663-220">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="29663-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29663-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29663-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29663-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="29663-222">Entry</span></span> | <span data-ttu-id="29663-223">Value</span><span class="sxs-lookup"><span data-stu-id="29663-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="29663-224">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29663-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="29663-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29663-225">MAPI-Id</span></span>                | <span data-ttu-id="29663-226">0x80BD</span><span class="sxs-lookup"><span data-stu-id="29663-226">0x80BD</span></span>                          |
| <span data-ttu-id="29663-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="29663-227">System-Only</span></span>            | <span data-ttu-id="29663-228">True</span><span class="sxs-lookup"><span data-stu-id="29663-228">True</span></span>                            |
| <span data-ttu-id="29663-229">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29663-229">Is-Single-Valued</span></span>       | <span data-ttu-id="29663-230">True</span><span class="sxs-lookup"><span data-stu-id="29663-230">True</span></span>                            |
| <span data-ttu-id="29663-231">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29663-231">Is Indexed</span></span>             | <span data-ttu-id="29663-232">False</span><span class="sxs-lookup"><span data-stu-id="29663-232">False</span></span>                           |
| <span data-ttu-id="29663-233">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29663-233">In Global Catalog</span></span>      | <span data-ttu-id="29663-234">True</span><span class="sxs-lookup"><span data-stu-id="29663-234">True</span></span>                            |
| <span data-ttu-id="29663-235">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29663-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="29663-236">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29663-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="29663-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29663-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="29663-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29663-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="29663-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-239">Search-Flags</span></span>           | <span data-ttu-id="29663-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="29663-240">0x00000008</span></span>                      |
| <span data-ttu-id="29663-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-241">System-Flags</span></span>           | <span data-ttu-id="29663-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29663-242">0x00000012</span></span>                      |
| <span data-ttu-id="29663-243">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29663-243">Classes used in</span></span>        | [<span data-ttu-id="29663-244">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="29663-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29663-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29663-245">Windows Server 2008</span></span>



| <span data-ttu-id="29663-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="29663-246">Entry</span></span> | <span data-ttu-id="29663-247">Value</span><span class="sxs-lookup"><span data-stu-id="29663-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="29663-248">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29663-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="29663-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29663-249">MAPI-Id</span></span>                | <span data-ttu-id="29663-250">0x80BD</span><span class="sxs-lookup"><span data-stu-id="29663-250">0x80BD</span></span>                          |
| <span data-ttu-id="29663-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="29663-251">System-Only</span></span>            | <span data-ttu-id="29663-252">True</span><span class="sxs-lookup"><span data-stu-id="29663-252">True</span></span>                            |
| <span data-ttu-id="29663-253">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29663-253">Is-Single-Valued</span></span>       | <span data-ttu-id="29663-254">True</span><span class="sxs-lookup"><span data-stu-id="29663-254">True</span></span>                            |
| <span data-ttu-id="29663-255">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29663-255">Is Indexed</span></span>             | <span data-ttu-id="29663-256">False</span><span class="sxs-lookup"><span data-stu-id="29663-256">False</span></span>                           |
| <span data-ttu-id="29663-257">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29663-257">In Global Catalog</span></span>      | <span data-ttu-id="29663-258">True</span><span class="sxs-lookup"><span data-stu-id="29663-258">True</span></span>                            |
| <span data-ttu-id="29663-259">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29663-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="29663-260">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29663-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="29663-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29663-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="29663-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29663-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="29663-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-263">Search-Flags</span></span>           | <span data-ttu-id="29663-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="29663-264">0x00000008</span></span>                      |
| <span data-ttu-id="29663-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-265">System-Flags</span></span>           | <span data-ttu-id="29663-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29663-266">0x00000012</span></span>                      |
| <span data-ttu-id="29663-267">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29663-267">Classes used in</span></span>        | [<span data-ttu-id="29663-268">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="29663-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29663-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29663-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29663-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="29663-270">Entry</span></span> | <span data-ttu-id="29663-271">Value</span><span class="sxs-lookup"><span data-stu-id="29663-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="29663-272">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29663-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="29663-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29663-273">MAPI-Id</span></span>                | <span data-ttu-id="29663-274">0x80BD</span><span class="sxs-lookup"><span data-stu-id="29663-274">0x80BD</span></span>                          |
| <span data-ttu-id="29663-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="29663-275">System-Only</span></span>            | <span data-ttu-id="29663-276">True</span><span class="sxs-lookup"><span data-stu-id="29663-276">True</span></span>                            |
| <span data-ttu-id="29663-277">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29663-277">Is-Single-Valued</span></span>       | <span data-ttu-id="29663-278">True</span><span class="sxs-lookup"><span data-stu-id="29663-278">True</span></span>                            |
| <span data-ttu-id="29663-279">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29663-279">Is Indexed</span></span>             | <span data-ttu-id="29663-280">False</span><span class="sxs-lookup"><span data-stu-id="29663-280">False</span></span>                           |
| <span data-ttu-id="29663-281">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29663-281">In Global Catalog</span></span>      | <span data-ttu-id="29663-282">True</span><span class="sxs-lookup"><span data-stu-id="29663-282">True</span></span>                            |
| <span data-ttu-id="29663-283">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29663-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="29663-284">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29663-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="29663-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29663-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="29663-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29663-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="29663-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-287">Search-Flags</span></span>           | <span data-ttu-id="29663-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="29663-288">0x00000008</span></span>                      |
| <span data-ttu-id="29663-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-289">System-Flags</span></span>           | <span data-ttu-id="29663-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29663-290">0x00000012</span></span>                      |
| <span data-ttu-id="29663-291">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29663-291">Classes used in</span></span>        | [<span data-ttu-id="29663-292">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="29663-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29663-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29663-293">Windows Server 2012</span></span>



| <span data-ttu-id="29663-294">Entrada</span><span class="sxs-lookup"><span data-stu-id="29663-294">Entry</span></span> | <span data-ttu-id="29663-295">Value</span><span class="sxs-lookup"><span data-stu-id="29663-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="29663-296">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="29663-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="29663-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29663-297">MAPI-Id</span></span>                | <span data-ttu-id="29663-298">0x80BD</span><span class="sxs-lookup"><span data-stu-id="29663-298">0x80BD</span></span>                          |
| <span data-ttu-id="29663-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="29663-299">System-Only</span></span>            | <span data-ttu-id="29663-300">True</span><span class="sxs-lookup"><span data-stu-id="29663-300">True</span></span>                            |
| <span data-ttu-id="29663-301">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="29663-301">Is-Single-Valued</span></span>       | <span data-ttu-id="29663-302">True</span><span class="sxs-lookup"><span data-stu-id="29663-302">True</span></span>                            |
| <span data-ttu-id="29663-303">Está indexado</span><span class="sxs-lookup"><span data-stu-id="29663-303">Is Indexed</span></span>             | <span data-ttu-id="29663-304">False</span><span class="sxs-lookup"><span data-stu-id="29663-304">False</span></span>                           |
| <span data-ttu-id="29663-305">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="29663-305">In Global Catalog</span></span>      | <span data-ttu-id="29663-306">True</span><span class="sxs-lookup"><span data-stu-id="29663-306">True</span></span>                            |
| <span data-ttu-id="29663-307">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="29663-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="29663-308">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29663-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="29663-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29663-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="29663-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29663-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="29663-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-311">Search-Flags</span></span>           | <span data-ttu-id="29663-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="29663-312">0x00000008</span></span>                      |
| <span data-ttu-id="29663-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29663-313">System-Flags</span></span>           | <span data-ttu-id="29663-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="29663-314">0x00000012</span></span>                      |
| <span data-ttu-id="29663-315">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="29663-315">Classes used in</span></span>        | [<span data-ttu-id="29663-316">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="29663-316">**Top**</span></span>](c-top.md)<br/> |



 

 






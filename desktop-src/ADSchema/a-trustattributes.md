---
title: Trust-Attributes atributo)
description: Este atributo almacena los atributos de confianza de un dominio de confianza.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Trust-Attributes
- trustAttributes esquema de AD de atributos
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804813"
---
# <a name="trust-attributes-attribute"></a><span data-ttu-id="7bae3-105">Trust-Attributes atributo)</span><span class="sxs-lookup"><span data-stu-id="7bae3-105">Trust-Attributes attribute</span></span>

<span data-ttu-id="7bae3-106">Este atributo almacena los atributos de confianza de un dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="7bae3-106">This attribute stores the trust attributes for a trusted domain.</span></span> <span data-ttu-id="7bae3-107">Los posibles valores de atributo son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7bae3-107">Possible attribute values are as follows:</span></span>

-   <span data-ttu-id="7bae3-108">\_Atributo de \_ confianza \_ deshabilitar transitividad.</span><span class="sxs-lookup"><span data-stu-id="7bae3-108">TRUST\_ATTRIBUTE\_NON\_TRANSITIVE Disable transitivity.</span></span>
-   <span data-ttu-id="7bae3-109">\_ \_ La confianza principal del árbol de atributos de confianza \_ está establecida en el árbol primario de la organización.</span><span class="sxs-lookup"><span data-stu-id="7bae3-109">TRUST\_ATTRIBUTE\_TREE\_PARENT Trust is set to the organization tree parent.</span></span>
-   <span data-ttu-id="7bae3-110">Confianza \_ \_ \_ raíz del árbol de atributos de confianza establecida en otra raíz de árbol del bosque.</span><span class="sxs-lookup"><span data-stu-id="7bae3-110">TRUST\_ATTRIBUTE\_TREE\_ROOT Trust set to another tree root in the forest.</span></span>
-   <span data-ttu-id="7bae3-111">\_Nivel de atributo de confianza \_ \_ : solo un vínculo de confianza válido solo para el cliente de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="7bae3-111">TRUST\_ATTRIBUTE\_UPLEVEL\_ONLY Trusted link valid only for uplevel client.</span></span>



| <span data-ttu-id="7bae3-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bae3-112">Entry</span></span> | <span data-ttu-id="7bae3-113">Value</span><span class="sxs-lookup"><span data-stu-id="7bae3-113">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7bae3-114">CN</span><span class="sxs-lookup"><span data-stu-id="7bae3-114">CN</span></span>                | <span data-ttu-id="7bae3-115">Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="7bae3-115">Trust-Attributes</span></span>                     |
| <span data-ttu-id="7bae3-116">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7bae3-116">Ldap-Display-Name</span></span> | <span data-ttu-id="7bae3-117">trustAttributes</span><span class="sxs-lookup"><span data-stu-id="7bae3-117">trustAttributes</span></span>                      |
| <span data-ttu-id="7bae3-118">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7bae3-118">Size</span></span>              | \-                                   |
| <span data-ttu-id="7bae3-119">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7bae3-119">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7bae3-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7bae3-120">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7bae3-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7bae3-121">Attribute-Id</span></span>      | <span data-ttu-id="7bae3-122">1.2.840.113556.1.4.470</span><span class="sxs-lookup"><span data-stu-id="7bae3-122">1.2.840.113556.1.4.470</span></span>               |
| <span data-ttu-id="7bae3-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7bae3-123">System-Id-Guid</span></span>    | <span data-ttu-id="7bae3-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="7bae3-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span></span> |
| <span data-ttu-id="7bae3-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bae3-125">Syntax</span></span>            | [<span data-ttu-id="7bae3-126">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="7bae3-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7bae3-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7bae3-127">Implementations</span></span>

-   [<span data-ttu-id="7bae3-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7bae3-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7bae3-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7bae3-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7bae3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7bae3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7bae3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7bae3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7bae3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7bae3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7bae3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7bae3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7bae3-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bae3-134">Windows 2000 Server</span></span>



| <span data-ttu-id="7bae3-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bae3-135">Entry</span></span> | <span data-ttu-id="7bae3-136">Value</span><span class="sxs-lookup"><span data-stu-id="7bae3-136">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="7bae3-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7bae3-137">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bae3-138">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bae3-139">System-Only</span></span>            | <span data-ttu-id="7bae3-140">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-140">False</span></span>                                                |
| <span data-ttu-id="7bae3-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7bae3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7bae3-142">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-142">True</span></span>                                                 |
| <span data-ttu-id="7bae3-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7bae3-143">Is Indexed</span></span>             | <span data-ttu-id="7bae3-144">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-144">False</span></span>                                                |
| <span data-ttu-id="7bae3-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bae3-145">In Global Catalog</span></span>      | <span data-ttu-id="7bae3-146">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-146">False</span></span>                                                |
| <span data-ttu-id="7bae3-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7bae3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bae3-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7bae3-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="7bae3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bae3-149">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bae3-150">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-151">Search-Flags</span></span>           | <span data-ttu-id="7bae3-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bae3-152">0x00000000</span></span>                                           |
| <span data-ttu-id="7bae3-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-153">System-Flags</span></span>           | <span data-ttu-id="7bae3-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bae3-154">0x00000010</span></span>                                           |
| <span data-ttu-id="7bae3-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7bae3-155">Classes used in</span></span>        | [<span data-ttu-id="7bae3-156">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="7bae3-156">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7bae3-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7bae3-157">Windows Server 2003</span></span>



| <span data-ttu-id="7bae3-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bae3-158">Entry</span></span> | <span data-ttu-id="7bae3-159">Value</span><span class="sxs-lookup"><span data-stu-id="7bae3-159">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="7bae3-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7bae3-160">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bae3-161">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bae3-162">System-Only</span></span>            | <span data-ttu-id="7bae3-163">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-163">False</span></span>                                                |
| <span data-ttu-id="7bae3-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7bae3-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7bae3-165">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-165">True</span></span>                                                 |
| <span data-ttu-id="7bae3-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7bae3-166">Is Indexed</span></span>             | <span data-ttu-id="7bae3-167">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-167">False</span></span>                                                |
| <span data-ttu-id="7bae3-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bae3-168">In Global Catalog</span></span>      | <span data-ttu-id="7bae3-169">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-169">True</span></span>                                                 |
| <span data-ttu-id="7bae3-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7bae3-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bae3-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7bae3-171">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="7bae3-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bae3-172">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bae3-173">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-174">Search-Flags</span></span>           | <span data-ttu-id="7bae3-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bae3-175">0x00000000</span></span>                                           |
| <span data-ttu-id="7bae3-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-176">System-Flags</span></span>           | <span data-ttu-id="7bae3-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bae3-177">0x00000010</span></span>                                           |
| <span data-ttu-id="7bae3-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7bae3-178">Classes used in</span></span>        | [<span data-ttu-id="7bae3-179">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="7bae3-179">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7bae3-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7bae3-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7bae3-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bae3-181">Entry</span></span> | <span data-ttu-id="7bae3-182">Value</span><span class="sxs-lookup"><span data-stu-id="7bae3-182">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="7bae3-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7bae3-183">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bae3-184">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bae3-185">System-Only</span></span>            | <span data-ttu-id="7bae3-186">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-186">False</span></span>                                                |
| <span data-ttu-id="7bae3-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7bae3-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7bae3-188">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-188">True</span></span>                                                 |
| <span data-ttu-id="7bae3-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7bae3-189">Is Indexed</span></span>             | <span data-ttu-id="7bae3-190">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-190">False</span></span>                                                |
| <span data-ttu-id="7bae3-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bae3-191">In Global Catalog</span></span>      | <span data-ttu-id="7bae3-192">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-192">True</span></span>                                                 |
| <span data-ttu-id="7bae3-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7bae3-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bae3-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7bae3-194">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="7bae3-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bae3-195">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bae3-196">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-197">Search-Flags</span></span>           | <span data-ttu-id="7bae3-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bae3-198">0x00000000</span></span>                                           |
| <span data-ttu-id="7bae3-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-199">System-Flags</span></span>           | <span data-ttu-id="7bae3-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bae3-200">0x00000010</span></span>                                           |
| <span data-ttu-id="7bae3-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7bae3-201">Classes used in</span></span>        | [<span data-ttu-id="7bae3-202">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="7bae3-202">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7bae3-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bae3-203">Windows Server 2008</span></span>



| <span data-ttu-id="7bae3-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bae3-204">Entry</span></span> | <span data-ttu-id="7bae3-205">Value</span><span class="sxs-lookup"><span data-stu-id="7bae3-205">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="7bae3-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7bae3-206">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bae3-207">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bae3-208">System-Only</span></span>            | <span data-ttu-id="7bae3-209">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-209">False</span></span>                                                |
| <span data-ttu-id="7bae3-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7bae3-210">Is-Single-Valued</span></span>       | <span data-ttu-id="7bae3-211">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-211">True</span></span>                                                 |
| <span data-ttu-id="7bae3-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7bae3-212">Is Indexed</span></span>             | <span data-ttu-id="7bae3-213">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-213">False</span></span>                                                |
| <span data-ttu-id="7bae3-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bae3-214">In Global Catalog</span></span>      | <span data-ttu-id="7bae3-215">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-215">True</span></span>                                                 |
| <span data-ttu-id="7bae3-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7bae3-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bae3-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7bae3-217">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="7bae3-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bae3-218">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bae3-219">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-220">Search-Flags</span></span>           | <span data-ttu-id="7bae3-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bae3-221">0x00000000</span></span>                                           |
| <span data-ttu-id="7bae3-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-222">System-Flags</span></span>           | <span data-ttu-id="7bae3-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bae3-223">0x00000010</span></span>                                           |
| <span data-ttu-id="7bae3-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7bae3-224">Classes used in</span></span>        | [<span data-ttu-id="7bae3-225">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="7bae3-225">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7bae3-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7bae3-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7bae3-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bae3-227">Entry</span></span> | <span data-ttu-id="7bae3-228">Value</span><span class="sxs-lookup"><span data-stu-id="7bae3-228">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="7bae3-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7bae3-229">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bae3-230">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bae3-231">System-Only</span></span>            | <span data-ttu-id="7bae3-232">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-232">False</span></span>                                                |
| <span data-ttu-id="7bae3-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7bae3-233">Is-Single-Valued</span></span>       | <span data-ttu-id="7bae3-234">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-234">True</span></span>                                                 |
| <span data-ttu-id="7bae3-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7bae3-235">Is Indexed</span></span>             | <span data-ttu-id="7bae3-236">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-236">False</span></span>                                                |
| <span data-ttu-id="7bae3-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bae3-237">In Global Catalog</span></span>      | <span data-ttu-id="7bae3-238">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-238">True</span></span>                                                 |
| <span data-ttu-id="7bae3-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7bae3-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bae3-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7bae3-240">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="7bae3-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bae3-241">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bae3-242">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-243">Search-Flags</span></span>           | <span data-ttu-id="7bae3-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bae3-244">0x00000000</span></span>                                           |
| <span data-ttu-id="7bae3-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-245">System-Flags</span></span>           | <span data-ttu-id="7bae3-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bae3-246">0x00000010</span></span>                                           |
| <span data-ttu-id="7bae3-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7bae3-247">Classes used in</span></span>        | [<span data-ttu-id="7bae3-248">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="7bae3-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7bae3-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7bae3-249">Windows Server 2012</span></span>



| <span data-ttu-id="7bae3-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bae3-250">Entry</span></span> | <span data-ttu-id="7bae3-251">Value</span><span class="sxs-lookup"><span data-stu-id="7bae3-251">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="7bae3-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7bae3-252">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bae3-253">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="7bae3-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bae3-254">System-Only</span></span>            | <span data-ttu-id="7bae3-255">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-255">False</span></span>                                                |
| <span data-ttu-id="7bae3-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7bae3-256">Is-Single-Valued</span></span>       | <span data-ttu-id="7bae3-257">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-257">True</span></span>                                                 |
| <span data-ttu-id="7bae3-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7bae3-258">Is Indexed</span></span>             | <span data-ttu-id="7bae3-259">False</span><span class="sxs-lookup"><span data-stu-id="7bae3-259">False</span></span>                                                |
| <span data-ttu-id="7bae3-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bae3-260">In Global Catalog</span></span>      | <span data-ttu-id="7bae3-261">True</span><span class="sxs-lookup"><span data-stu-id="7bae3-261">True</span></span>                                                 |
| <span data-ttu-id="7bae3-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7bae3-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bae3-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7bae3-263">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="7bae3-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bae3-264">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bae3-265">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="7bae3-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-266">Search-Flags</span></span>           | <span data-ttu-id="7bae3-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bae3-267">0x00000000</span></span>                                           |
| <span data-ttu-id="7bae3-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bae3-268">System-Flags</span></span>           | <span data-ttu-id="7bae3-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bae3-269">0x00000010</span></span>                                           |
| <span data-ttu-id="7bae3-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7bae3-270">Classes used in</span></span>        | [<span data-ttu-id="7bae3-271">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="7bae3-271">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 






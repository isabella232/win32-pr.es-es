---
title: Domain-Component atributo)
description: Atributo de asignación de nombres para los objetos de dominio y DNS. Normalmente, se muestra como DC DomainName.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Domain-Component
- Esquema de AD de atributo DC
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151442"
---
# <a name="domain-component-attribute"></a><span data-ttu-id="c4a52-106">Domain-Component atributo)</span><span class="sxs-lookup"><span data-stu-id="c4a52-106">Domain-Component attribute</span></span>

<span data-ttu-id="c4a52-107">Atributo de asignación de nombres para los objetos de dominio y DNS.</span><span class="sxs-lookup"><span data-stu-id="c4a52-107">The naming attribute for Domain and DNS objects.</span></span> <span data-ttu-id="c4a52-108">Normalmente se muestra como DC = DomainName.</span><span class="sxs-lookup"><span data-stu-id="c4a52-108">Usually displayed as dc=DomainName.</span></span>



| <span data-ttu-id="c4a52-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4a52-109">Entry</span></span> | <span data-ttu-id="c4a52-110">Value</span><span class="sxs-lookup"><span data-stu-id="c4a52-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c4a52-111">CN</span><span class="sxs-lookup"><span data-stu-id="c4a52-111">CN</span></span>                | <span data-ttu-id="c4a52-112">Domain-Component</span><span class="sxs-lookup"><span data-stu-id="c4a52-112">Domain-Component</span></span>                            |
| <span data-ttu-id="c4a52-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c4a52-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c4a52-114">dc</span><span class="sxs-lookup"><span data-stu-id="c4a52-114">dc</span></span>                                          |
| <span data-ttu-id="c4a52-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c4a52-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="c4a52-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c4a52-116">Update Privilege</span></span>  | <span data-ttu-id="c4a52-117">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="c4a52-117">Domain administrator</span></span>                        |
| <span data-ttu-id="c4a52-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c4a52-118">Update Frequency</span></span>  | <span data-ttu-id="c4a52-119">Cuando se crea el dominio.</span><span class="sxs-lookup"><span data-stu-id="c4a52-119">When the domain is created.</span></span>                 |
| <span data-ttu-id="c4a52-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4a52-120">Attribute-Id</span></span>      | <span data-ttu-id="c4a52-121">0.9.2342.19200300.100.1.25</span><span class="sxs-lookup"><span data-stu-id="c4a52-121">0.9.2342.19200300.100.1.25</span></span>                  |
| <span data-ttu-id="c4a52-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c4a52-122">System-Id-Guid</span></span>    | <span data-ttu-id="c4a52-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c4a52-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span></span>        |
| <span data-ttu-id="c4a52-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4a52-124">Syntax</span></span>            | [<span data-ttu-id="c4a52-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c4a52-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c4a52-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c4a52-126">Implementations</span></span>

-   [<span data-ttu-id="c4a52-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c4a52-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c4a52-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4a52-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4a52-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c4a52-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c4a52-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4a52-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4a52-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4a52-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4a52-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4a52-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4a52-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4a52-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c4a52-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4a52-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c4a52-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4a52-135">Entry</span></span> | <span data-ttu-id="c4a52-136">Value</span><span class="sxs-lookup"><span data-stu-id="c4a52-136">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a52-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4a52-137">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4a52-138">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4a52-139">System-Only</span></span>            | <span data-ttu-id="c4a52-140">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-140">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4a52-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c4a52-142">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-142">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4a52-143">Is Indexed</span></span>             | <span data-ttu-id="c4a52-144">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-144">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4a52-145">In Global Catalog</span></span>      | <span data-ttu-id="c4a52-146">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-146">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4a52-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4a52-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4a52-148">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="c4a52-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4a52-149">Range-Lower</span></span>            | <span data-ttu-id="c4a52-150">1</span><span class="sxs-lookup"><span data-stu-id="c4a52-150">1</span></span>                                                                                                                       |
| <span data-ttu-id="c4a52-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4a52-151">Range-Upper</span></span>            | <span data-ttu-id="c4a52-152">255</span><span class="sxs-lookup"><span data-stu-id="c4a52-152">255</span></span>                                                                                                                     |
| <span data-ttu-id="c4a52-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-153">Search-Flags</span></span>           | <span data-ttu-id="c4a52-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4a52-154">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-155">System-Flags</span></span>           | <span data-ttu-id="c4a52-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4a52-156">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-157">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4a52-157">Classes used in</span></span>        | [<span data-ttu-id="c4a52-158">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="c4a52-159">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-159">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="c4a52-160">**Domain**</span><span class="sxs-lookup"><span data-stu-id="c4a52-160">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c4a52-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4a52-161">Windows Server 2003</span></span>



| <span data-ttu-id="c4a52-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4a52-162">Entry</span></span> | <span data-ttu-id="c4a52-163">Value</span><span class="sxs-lookup"><span data-stu-id="c4a52-163">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a52-164">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4a52-164">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4a52-165">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4a52-166">System-Only</span></span>            | <span data-ttu-id="c4a52-167">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-167">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-168">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4a52-168">Is-Single-Valued</span></span>       | <span data-ttu-id="c4a52-169">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-169">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-170">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4a52-170">Is Indexed</span></span>             | <span data-ttu-id="c4a52-171">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-171">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-172">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4a52-172">In Global Catalog</span></span>      | <span data-ttu-id="c4a52-173">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-173">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-174">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4a52-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4a52-175">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4a52-175">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="c4a52-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4a52-176">Range-Lower</span></span>            | <span data-ttu-id="c4a52-177">1</span><span class="sxs-lookup"><span data-stu-id="c4a52-177">1</span></span>                                                                                                                       |
| <span data-ttu-id="c4a52-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4a52-178">Range-Upper</span></span>            | <span data-ttu-id="c4a52-179">255</span><span class="sxs-lookup"><span data-stu-id="c4a52-179">255</span></span>                                                                                                                     |
| <span data-ttu-id="c4a52-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-180">Search-Flags</span></span>           | <span data-ttu-id="c4a52-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4a52-181">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-182">System-Flags</span></span>           | <span data-ttu-id="c4a52-183">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4a52-183">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-184">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4a52-184">Classes used in</span></span>        | [<span data-ttu-id="c4a52-185">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-185">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="c4a52-186">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-186">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="c4a52-187">**Domain**</span><span class="sxs-lookup"><span data-stu-id="c4a52-187">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c4a52-188">ADAM</span><span class="sxs-lookup"><span data-stu-id="c4a52-188">ADAM</span></span>



| <span data-ttu-id="c4a52-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4a52-189">Entry</span></span> | <span data-ttu-id="c4a52-190">Value</span><span class="sxs-lookup"><span data-stu-id="c4a52-190">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="c4a52-191">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4a52-191">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="c4a52-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4a52-192">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="c4a52-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4a52-193">System-Only</span></span>            | <span data-ttu-id="c4a52-194">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-194">False</span></span>                                 |
| <span data-ttu-id="c4a52-195">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4a52-195">Is-Single-Valued</span></span>       | <span data-ttu-id="c4a52-196">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-196">True</span></span>                                  |
| <span data-ttu-id="c4a52-197">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4a52-197">Is Indexed</span></span>             | <span data-ttu-id="c4a52-198">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-198">False</span></span>                                 |
| <span data-ttu-id="c4a52-199">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4a52-199">In Global Catalog</span></span>      | <span data-ttu-id="c4a52-200">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-200">True</span></span>                                  |
| <span data-ttu-id="c4a52-201">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4a52-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4a52-202">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4a52-202">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="c4a52-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4a52-203">Range-Lower</span></span>            | <span data-ttu-id="c4a52-204">1</span><span class="sxs-lookup"><span data-stu-id="c4a52-204">1</span></span>                                     |
| <span data-ttu-id="c4a52-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4a52-205">Range-Upper</span></span>            | <span data-ttu-id="c4a52-206">255</span><span class="sxs-lookup"><span data-stu-id="c4a52-206">255</span></span>                                   |
| <span data-ttu-id="c4a52-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-207">Search-Flags</span></span>           | <span data-ttu-id="c4a52-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4a52-208">0x00000000</span></span>                            |
| <span data-ttu-id="c4a52-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-209">System-Flags</span></span>           | <span data-ttu-id="c4a52-210">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4a52-210">0x00000012</span></span>                            |
| <span data-ttu-id="c4a52-211">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4a52-211">Classes used in</span></span>        | [<span data-ttu-id="c4a52-212">**Domain**</span><span class="sxs-lookup"><span data-stu-id="c4a52-212">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4a52-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4a52-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4a52-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4a52-214">Entry</span></span> | <span data-ttu-id="c4a52-215">Value</span><span class="sxs-lookup"><span data-stu-id="c4a52-215">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a52-216">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4a52-216">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4a52-217">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4a52-218">System-Only</span></span>            | <span data-ttu-id="c4a52-219">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-219">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-220">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4a52-220">Is-Single-Valued</span></span>       | <span data-ttu-id="c4a52-221">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-221">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-222">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4a52-222">Is Indexed</span></span>             | <span data-ttu-id="c4a52-223">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-223">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-224">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4a52-224">In Global Catalog</span></span>      | <span data-ttu-id="c4a52-225">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-225">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-226">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4a52-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4a52-227">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4a52-227">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="c4a52-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4a52-228">Range-Lower</span></span>            | <span data-ttu-id="c4a52-229">1</span><span class="sxs-lookup"><span data-stu-id="c4a52-229">1</span></span>                                                                                                                       |
| <span data-ttu-id="c4a52-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4a52-230">Range-Upper</span></span>            | <span data-ttu-id="c4a52-231">255</span><span class="sxs-lookup"><span data-stu-id="c4a52-231">255</span></span>                                                                                                                     |
| <span data-ttu-id="c4a52-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-232">Search-Flags</span></span>           | <span data-ttu-id="c4a52-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4a52-233">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-234">System-Flags</span></span>           | <span data-ttu-id="c4a52-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4a52-235">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-236">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4a52-236">Classes used in</span></span>        | [<span data-ttu-id="c4a52-237">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-237">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="c4a52-238">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-238">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="c4a52-239">**Domain**</span><span class="sxs-lookup"><span data-stu-id="c4a52-239">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4a52-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4a52-240">Windows Server 2008</span></span>



| <span data-ttu-id="c4a52-241">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4a52-241">Entry</span></span> | <span data-ttu-id="c4a52-242">Value</span><span class="sxs-lookup"><span data-stu-id="c4a52-242">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a52-243">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4a52-243">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4a52-244">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4a52-245">System-Only</span></span>            | <span data-ttu-id="c4a52-246">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-246">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-247">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4a52-247">Is-Single-Valued</span></span>       | <span data-ttu-id="c4a52-248">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-248">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-249">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4a52-249">Is Indexed</span></span>             | <span data-ttu-id="c4a52-250">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-250">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-251">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4a52-251">In Global Catalog</span></span>      | <span data-ttu-id="c4a52-252">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-252">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-253">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4a52-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4a52-254">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4a52-254">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="c4a52-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4a52-255">Range-Lower</span></span>            | <span data-ttu-id="c4a52-256">1</span><span class="sxs-lookup"><span data-stu-id="c4a52-256">1</span></span>                                                                                                                       |
| <span data-ttu-id="c4a52-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4a52-257">Range-Upper</span></span>            | <span data-ttu-id="c4a52-258">255</span><span class="sxs-lookup"><span data-stu-id="c4a52-258">255</span></span>                                                                                                                     |
| <span data-ttu-id="c4a52-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-259">Search-Flags</span></span>           | <span data-ttu-id="c4a52-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4a52-260">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-261">System-Flags</span></span>           | <span data-ttu-id="c4a52-262">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4a52-262">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-263">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4a52-263">Classes used in</span></span>        | [<span data-ttu-id="c4a52-264">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-264">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="c4a52-265">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-265">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="c4a52-266">**Domain**</span><span class="sxs-lookup"><span data-stu-id="c4a52-266">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4a52-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4a52-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4a52-268">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4a52-268">Entry</span></span> | <span data-ttu-id="c4a52-269">Value</span><span class="sxs-lookup"><span data-stu-id="c4a52-269">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a52-270">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4a52-270">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4a52-271">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4a52-272">System-Only</span></span>            | <span data-ttu-id="c4a52-273">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-273">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-274">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4a52-274">Is-Single-Valued</span></span>       | <span data-ttu-id="c4a52-275">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-275">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-276">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4a52-276">Is Indexed</span></span>             | <span data-ttu-id="c4a52-277">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-277">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-278">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4a52-278">In Global Catalog</span></span>      | <span data-ttu-id="c4a52-279">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-279">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-280">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4a52-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4a52-281">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4a52-281">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="c4a52-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4a52-282">Range-Lower</span></span>            | <span data-ttu-id="c4a52-283">1</span><span class="sxs-lookup"><span data-stu-id="c4a52-283">1</span></span>                                                                                                                       |
| <span data-ttu-id="c4a52-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4a52-284">Range-Upper</span></span>            | <span data-ttu-id="c4a52-285">255</span><span class="sxs-lookup"><span data-stu-id="c4a52-285">255</span></span>                                                                                                                     |
| <span data-ttu-id="c4a52-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-286">Search-Flags</span></span>           | <span data-ttu-id="c4a52-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4a52-287">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-288">System-Flags</span></span>           | <span data-ttu-id="c4a52-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4a52-289">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-290">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4a52-290">Classes used in</span></span>        | [<span data-ttu-id="c4a52-291">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-291">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="c4a52-292">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-292">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="c4a52-293">**Domain**</span><span class="sxs-lookup"><span data-stu-id="c4a52-293">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4a52-294">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4a52-294">Windows Server 2012</span></span>



| <span data-ttu-id="c4a52-295">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4a52-295">Entry</span></span> | <span data-ttu-id="c4a52-296">Value</span><span class="sxs-lookup"><span data-stu-id="c4a52-296">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a52-297">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c4a52-297">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-298">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4a52-298">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="c4a52-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4a52-299">System-Only</span></span>            | <span data-ttu-id="c4a52-300">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-300">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-301">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c4a52-301">Is-Single-Valued</span></span>       | <span data-ttu-id="c4a52-302">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-302">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-303">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c4a52-303">Is Indexed</span></span>             | <span data-ttu-id="c4a52-304">False</span><span class="sxs-lookup"><span data-stu-id="c4a52-304">False</span></span>                                                                                                                   |
| <span data-ttu-id="c4a52-305">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c4a52-305">In Global Catalog</span></span>      | <span data-ttu-id="c4a52-306">True</span><span class="sxs-lookup"><span data-stu-id="c4a52-306">True</span></span>                                                                                                                    |
| <span data-ttu-id="c4a52-307">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c4a52-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4a52-308">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4a52-308">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="c4a52-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4a52-309">Range-Lower</span></span>            | <span data-ttu-id="c4a52-310">1</span><span class="sxs-lookup"><span data-stu-id="c4a52-310">1</span></span>                                                                                                                       |
| <span data-ttu-id="c4a52-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4a52-311">Range-Upper</span></span>            | <span data-ttu-id="c4a52-312">255</span><span class="sxs-lookup"><span data-stu-id="c4a52-312">255</span></span>                                                                                                                     |
| <span data-ttu-id="c4a52-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-313">Search-Flags</span></span>           | <span data-ttu-id="c4a52-314">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4a52-314">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4a52-315">System-Flags</span></span>           | <span data-ttu-id="c4a52-316">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c4a52-316">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="c4a52-317">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c4a52-317">Classes used in</span></span>        | [<span data-ttu-id="c4a52-318">**Nodo DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-318">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="c4a52-319">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="c4a52-319">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="c4a52-320">**Domain**</span><span class="sxs-lookup"><span data-stu-id="c4a52-320">**Domain**</span></span>](c-domain.md)<br/> |



 

 






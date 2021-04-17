---
title: Print-duplex-atributo compatible
description: Indica el tipo de compatibilidad dúplex que tiene una impresora.
ms.assetid: c7d3e3f1-d6a1-41b7-a54d-c932a00b2a68
ms.tgt_platform: multiple
keywords:
- 'Impresión-dúplex: esquema de AD de atributos admitidos'
- printDuplexSupported esquema de AD de atributos
topic_type:
- apiref
api_name:
- Print-Duplex-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027b5af8d2c2bc8ece810a00c17060608b7824c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658772"
---
# <a name="print-duplex-supported-attribute"></a><span data-ttu-id="63b80-105">Print-duplex-atributo compatible</span><span class="sxs-lookup"><span data-stu-id="63b80-105">Print-Duplex-Supported attribute</span></span>

<span data-ttu-id="63b80-106">Indica el tipo de compatibilidad dúplex que tiene una impresora.</span><span class="sxs-lookup"><span data-stu-id="63b80-106">Indicates the type of duplex support a printer has.</span></span>



| <span data-ttu-id="63b80-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="63b80-107">Entry</span></span> | <span data-ttu-id="63b80-108">Value</span><span class="sxs-lookup"><span data-stu-id="63b80-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="63b80-109">CN</span><span class="sxs-lookup"><span data-stu-id="63b80-109">CN</span></span>                | <span data-ttu-id="63b80-110">Impresión-dúplex: compatible</span><span class="sxs-lookup"><span data-stu-id="63b80-110">Print-Duplex-Supported</span></span>                                |
| <span data-ttu-id="63b80-111">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="63b80-111">Ldap-Display-Name</span></span> | <span data-ttu-id="63b80-112">printDuplexSupported</span><span class="sxs-lookup"><span data-stu-id="63b80-112">printDuplexSupported</span></span>                                  |
| <span data-ttu-id="63b80-113">Tamaño</span><span class="sxs-lookup"><span data-stu-id="63b80-113">Size</span></span>              | <span data-ttu-id="63b80-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="63b80-114">4 bytes.</span></span> <span data-ttu-id="63b80-115">Dúplex compatible = 2.</span><span class="sxs-lookup"><span data-stu-id="63b80-115">Duplex supported = 2.</span></span> <span data-ttu-id="63b80-116">Simplex solo = 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="63b80-116">Simplex only = 1 or 0.</span></span> |
| <span data-ttu-id="63b80-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="63b80-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="63b80-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="63b80-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="63b80-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="63b80-119">Attribute-Id</span></span>      | <span data-ttu-id="63b80-120">1.2.840.113556.1.4.1311</span><span class="sxs-lookup"><span data-stu-id="63b80-120">1.2.840.113556.1.4.1311</span></span>                               |
| <span data-ttu-id="63b80-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="63b80-121">System-Id-Guid</span></span>    | <span data-ttu-id="63b80-122">281416cc-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="63b80-122">281416cc-1968-11d0-a28f-00aa003049e2</span></span>                  |
| <span data-ttu-id="63b80-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63b80-123">Syntax</span></span>            | [<span data-ttu-id="63b80-124">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="63b80-124">**Boolean**</span></span>](s-boolean.md)                          |



## <a name="implementations"></a><span data-ttu-id="63b80-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="63b80-125">Implementations</span></span>

-   [<span data-ttu-id="63b80-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="63b80-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="63b80-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="63b80-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="63b80-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="63b80-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="63b80-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="63b80-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="63b80-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="63b80-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="63b80-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="63b80-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="63b80-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63b80-132">Windows 2000 Server</span></span>



| <span data-ttu-id="63b80-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="63b80-133">Entry</span></span> | <span data-ttu-id="63b80-134">Value</span><span class="sxs-lookup"><span data-stu-id="63b80-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="63b80-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="63b80-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63b80-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="63b80-137">System-Only</span></span>            | <span data-ttu-id="63b80-138">False</span><span class="sxs-lookup"><span data-stu-id="63b80-138">False</span></span>                                          |
| <span data-ttu-id="63b80-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="63b80-139">Is-Single-Valued</span></span>       | <span data-ttu-id="63b80-140">True</span><span class="sxs-lookup"><span data-stu-id="63b80-140">True</span></span>                                           |
| <span data-ttu-id="63b80-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="63b80-141">Is Indexed</span></span>             | <span data-ttu-id="63b80-142">False</span><span class="sxs-lookup"><span data-stu-id="63b80-142">False</span></span>                                          |
| <span data-ttu-id="63b80-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="63b80-143">In Global Catalog</span></span>      | <span data-ttu-id="63b80-144">True</span><span class="sxs-lookup"><span data-stu-id="63b80-144">True</span></span>                                           |
| <span data-ttu-id="63b80-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="63b80-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="63b80-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63b80-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="63b80-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63b80-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="63b80-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63b80-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="63b80-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-149">Search-Flags</span></span>           | <span data-ttu-id="63b80-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63b80-150">0x00000000</span></span>                                     |
| <span data-ttu-id="63b80-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-151">System-Flags</span></span>           | <span data-ttu-id="63b80-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63b80-152">0x00000010</span></span>                                     |
| <span data-ttu-id="63b80-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="63b80-153">Classes used in</span></span>        | [<span data-ttu-id="63b80-154">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="63b80-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="63b80-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63b80-155">Windows Server 2003</span></span>



| <span data-ttu-id="63b80-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="63b80-156">Entry</span></span> | <span data-ttu-id="63b80-157">Value</span><span class="sxs-lookup"><span data-stu-id="63b80-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="63b80-158">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="63b80-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63b80-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="63b80-160">System-Only</span></span>            | <span data-ttu-id="63b80-161">False</span><span class="sxs-lookup"><span data-stu-id="63b80-161">False</span></span>                                          |
| <span data-ttu-id="63b80-162">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="63b80-162">Is-Single-Valued</span></span>       | <span data-ttu-id="63b80-163">True</span><span class="sxs-lookup"><span data-stu-id="63b80-163">True</span></span>                                           |
| <span data-ttu-id="63b80-164">Está indexado</span><span class="sxs-lookup"><span data-stu-id="63b80-164">Is Indexed</span></span>             | <span data-ttu-id="63b80-165">False</span><span class="sxs-lookup"><span data-stu-id="63b80-165">False</span></span>                                          |
| <span data-ttu-id="63b80-166">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="63b80-166">In Global Catalog</span></span>      | <span data-ttu-id="63b80-167">True</span><span class="sxs-lookup"><span data-stu-id="63b80-167">True</span></span>                                           |
| <span data-ttu-id="63b80-168">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="63b80-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="63b80-169">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63b80-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="63b80-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63b80-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="63b80-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63b80-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="63b80-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-172">Search-Flags</span></span>           | <span data-ttu-id="63b80-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63b80-173">0x00000000</span></span>                                     |
| <span data-ttu-id="63b80-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-174">System-Flags</span></span>           | <span data-ttu-id="63b80-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63b80-175">0x00000010</span></span>                                     |
| <span data-ttu-id="63b80-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="63b80-176">Classes used in</span></span>        | [<span data-ttu-id="63b80-177">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="63b80-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="63b80-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="63b80-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="63b80-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="63b80-179">Entry</span></span> | <span data-ttu-id="63b80-180">Value</span><span class="sxs-lookup"><span data-stu-id="63b80-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="63b80-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="63b80-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63b80-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="63b80-183">System-Only</span></span>            | <span data-ttu-id="63b80-184">False</span><span class="sxs-lookup"><span data-stu-id="63b80-184">False</span></span>                                          |
| <span data-ttu-id="63b80-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="63b80-185">Is-Single-Valued</span></span>       | <span data-ttu-id="63b80-186">True</span><span class="sxs-lookup"><span data-stu-id="63b80-186">True</span></span>                                           |
| <span data-ttu-id="63b80-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="63b80-187">Is Indexed</span></span>             | <span data-ttu-id="63b80-188">False</span><span class="sxs-lookup"><span data-stu-id="63b80-188">False</span></span>                                          |
| <span data-ttu-id="63b80-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="63b80-189">In Global Catalog</span></span>      | <span data-ttu-id="63b80-190">True</span><span class="sxs-lookup"><span data-stu-id="63b80-190">True</span></span>                                           |
| <span data-ttu-id="63b80-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="63b80-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="63b80-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63b80-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="63b80-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63b80-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="63b80-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63b80-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="63b80-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-195">Search-Flags</span></span>           | <span data-ttu-id="63b80-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63b80-196">0x00000000</span></span>                                     |
| <span data-ttu-id="63b80-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-197">System-Flags</span></span>           | <span data-ttu-id="63b80-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63b80-198">0x00000010</span></span>                                     |
| <span data-ttu-id="63b80-199">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="63b80-199">Classes used in</span></span>        | [<span data-ttu-id="63b80-200">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="63b80-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="63b80-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63b80-201">Windows Server 2008</span></span>



| <span data-ttu-id="63b80-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="63b80-202">Entry</span></span> | <span data-ttu-id="63b80-203">Value</span><span class="sxs-lookup"><span data-stu-id="63b80-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="63b80-204">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="63b80-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63b80-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="63b80-206">System-Only</span></span>            | <span data-ttu-id="63b80-207">False</span><span class="sxs-lookup"><span data-stu-id="63b80-207">False</span></span>                                          |
| <span data-ttu-id="63b80-208">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="63b80-208">Is-Single-Valued</span></span>       | <span data-ttu-id="63b80-209">True</span><span class="sxs-lookup"><span data-stu-id="63b80-209">True</span></span>                                           |
| <span data-ttu-id="63b80-210">Está indexado</span><span class="sxs-lookup"><span data-stu-id="63b80-210">Is Indexed</span></span>             | <span data-ttu-id="63b80-211">False</span><span class="sxs-lookup"><span data-stu-id="63b80-211">False</span></span>                                          |
| <span data-ttu-id="63b80-212">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="63b80-212">In Global Catalog</span></span>      | <span data-ttu-id="63b80-213">True</span><span class="sxs-lookup"><span data-stu-id="63b80-213">True</span></span>                                           |
| <span data-ttu-id="63b80-214">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="63b80-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="63b80-215">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63b80-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="63b80-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63b80-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="63b80-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63b80-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="63b80-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-218">Search-Flags</span></span>           | <span data-ttu-id="63b80-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63b80-219">0x00000000</span></span>                                     |
| <span data-ttu-id="63b80-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-220">System-Flags</span></span>           | <span data-ttu-id="63b80-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63b80-221">0x00000010</span></span>                                     |
| <span data-ttu-id="63b80-222">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="63b80-222">Classes used in</span></span>        | [<span data-ttu-id="63b80-223">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="63b80-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="63b80-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63b80-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="63b80-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="63b80-225">Entry</span></span> | <span data-ttu-id="63b80-226">Value</span><span class="sxs-lookup"><span data-stu-id="63b80-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="63b80-227">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="63b80-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63b80-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="63b80-229">System-Only</span></span>            | <span data-ttu-id="63b80-230">False</span><span class="sxs-lookup"><span data-stu-id="63b80-230">False</span></span>                                          |
| <span data-ttu-id="63b80-231">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="63b80-231">Is-Single-Valued</span></span>       | <span data-ttu-id="63b80-232">True</span><span class="sxs-lookup"><span data-stu-id="63b80-232">True</span></span>                                           |
| <span data-ttu-id="63b80-233">Está indexado</span><span class="sxs-lookup"><span data-stu-id="63b80-233">Is Indexed</span></span>             | <span data-ttu-id="63b80-234">False</span><span class="sxs-lookup"><span data-stu-id="63b80-234">False</span></span>                                          |
| <span data-ttu-id="63b80-235">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="63b80-235">In Global Catalog</span></span>      | <span data-ttu-id="63b80-236">True</span><span class="sxs-lookup"><span data-stu-id="63b80-236">True</span></span>                                           |
| <span data-ttu-id="63b80-237">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="63b80-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="63b80-238">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63b80-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="63b80-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63b80-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="63b80-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63b80-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="63b80-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-241">Search-Flags</span></span>           | <span data-ttu-id="63b80-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63b80-242">0x00000000</span></span>                                     |
| <span data-ttu-id="63b80-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-243">System-Flags</span></span>           | <span data-ttu-id="63b80-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63b80-244">0x00000010</span></span>                                     |
| <span data-ttu-id="63b80-245">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="63b80-245">Classes used in</span></span>        | [<span data-ttu-id="63b80-246">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="63b80-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="63b80-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63b80-247">Windows Server 2012</span></span>



| <span data-ttu-id="63b80-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="63b80-248">Entry</span></span> | <span data-ttu-id="63b80-249">Value</span><span class="sxs-lookup"><span data-stu-id="63b80-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="63b80-250">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="63b80-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63b80-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="63b80-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="63b80-252">System-Only</span></span>            | <span data-ttu-id="63b80-253">False</span><span class="sxs-lookup"><span data-stu-id="63b80-253">False</span></span>                                          |
| <span data-ttu-id="63b80-254">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="63b80-254">Is-Single-Valued</span></span>       | <span data-ttu-id="63b80-255">True</span><span class="sxs-lookup"><span data-stu-id="63b80-255">True</span></span>                                           |
| <span data-ttu-id="63b80-256">Está indexado</span><span class="sxs-lookup"><span data-stu-id="63b80-256">Is Indexed</span></span>             | <span data-ttu-id="63b80-257">False</span><span class="sxs-lookup"><span data-stu-id="63b80-257">False</span></span>                                          |
| <span data-ttu-id="63b80-258">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="63b80-258">In Global Catalog</span></span>      | <span data-ttu-id="63b80-259">True</span><span class="sxs-lookup"><span data-stu-id="63b80-259">True</span></span>                                           |
| <span data-ttu-id="63b80-260">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="63b80-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="63b80-261">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63b80-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="63b80-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63b80-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="63b80-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63b80-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="63b80-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-264">Search-Flags</span></span>           | <span data-ttu-id="63b80-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63b80-265">0x00000000</span></span>                                     |
| <span data-ttu-id="63b80-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63b80-266">System-Flags</span></span>           | <span data-ttu-id="63b80-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63b80-267">0x00000010</span></span>                                     |
| <span data-ttu-id="63b80-268">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="63b80-268">Classes used in</span></span>        | [<span data-ttu-id="63b80-269">**Cola de impresión**</span><span class="sxs-lookup"><span data-stu-id="63b80-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 






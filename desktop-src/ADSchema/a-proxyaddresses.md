---
title: Proxy-Addresses atributo)
description: Una dirección proxy es la dirección por la que se reconoce un objeto de destinatario de Microsoft Exchange Server en un sistema de correo externo. Las direcciones de proxy son necesarias para todos los objetos de destinatario, como los destinatarios personalizados y las listas de distribución.
ms.assetid: 7bb299d8-e67a-4062-91a3-b579fd71d5c9
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Proxy-Addresses
- atributo proxyAddresses esquema de AD
topic_type:
- apiref
api_name:
- Proxy-Addresses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03542cef9bca48dbba1585e3837056b53673f34
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906121"
---
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="208ce-106">Proxy-Addresses atributo)</span><span class="sxs-lookup"><span data-stu-id="208ce-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="208ce-107">Una dirección proxy es la dirección por la que se reconoce un objeto de destinatario de Microsoft Exchange Server en un sistema de correo externo.</span><span class="sxs-lookup"><span data-stu-id="208ce-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="208ce-108">Las direcciones de proxy son necesarias para todos los objetos de destinatario, como los destinatarios personalizados y las listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="208ce-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="208ce-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="208ce-109">Entry</span></span> | <span data-ttu-id="208ce-110">Value</span><span class="sxs-lookup"><span data-stu-id="208ce-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208ce-111">CN</span><span class="sxs-lookup"><span data-stu-id="208ce-111">CN</span></span>                | <span data-ttu-id="208ce-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="208ce-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="208ce-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="208ce-113">Ldap-Display-Name</span></span> | <span data-ttu-id="208ce-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="208ce-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="208ce-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="208ce-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="208ce-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="208ce-116">Update Privilege</span></span>  | <span data-ttu-id="208ce-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="208ce-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="208ce-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="208ce-118">Update Frequency</span></span>  | <span data-ttu-id="208ce-119">Creado por un archivo DLL proporcionado con el objeto de directorio Address-Type cuando se instala el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="208ce-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="208ce-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="208ce-120">Attribute-Id</span></span>      | <span data-ttu-id="208ce-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="208ce-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="208ce-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="208ce-122">System-Id-Guid</span></span>    | <span data-ttu-id="208ce-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="208ce-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="208ce-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="208ce-124">Syntax</span></span>            | [<span data-ttu-id="208ce-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="208ce-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="208ce-126">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="208ce-126">Implementations</span></span>

-   [<span data-ttu-id="208ce-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="208ce-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="208ce-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="208ce-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="208ce-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="208ce-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="208ce-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="208ce-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="208ce-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="208ce-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="208ce-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="208ce-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="208ce-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="208ce-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="208ce-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="208ce-134">Windows 2000 Server</span></span>



| <span data-ttu-id="208ce-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="208ce-135">Entry</span></span> | <span data-ttu-id="208ce-136">Value</span><span class="sxs-lookup"><span data-stu-id="208ce-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="208ce-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="208ce-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="208ce-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="208ce-138">MAPI-Id</span></span>                | <span data-ttu-id="208ce-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="208ce-139">0x800F</span></span>                          |
| <span data-ttu-id="208ce-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="208ce-140">System-Only</span></span>            | <span data-ttu-id="208ce-141">False</span><span class="sxs-lookup"><span data-stu-id="208ce-141">False</span></span>                           |
| <span data-ttu-id="208ce-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="208ce-142">Is-Single-Valued</span></span>       | <span data-ttu-id="208ce-143">False</span><span class="sxs-lookup"><span data-stu-id="208ce-143">False</span></span>                           |
| <span data-ttu-id="208ce-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="208ce-144">Is Indexed</span></span>             | <span data-ttu-id="208ce-145">True</span><span class="sxs-lookup"><span data-stu-id="208ce-145">True</span></span>                            |
| <span data-ttu-id="208ce-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="208ce-146">In Global Catalog</span></span>      | <span data-ttu-id="208ce-147">False</span><span class="sxs-lookup"><span data-stu-id="208ce-147">False</span></span>                           |
| <span data-ttu-id="208ce-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="208ce-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="208ce-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="208ce-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="208ce-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="208ce-150">Range-Lower</span></span>            | <span data-ttu-id="208ce-151">1</span><span class="sxs-lookup"><span data-stu-id="208ce-151">1</span></span>                               |
| <span data-ttu-id="208ce-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="208ce-152">Range-Upper</span></span>            | <span data-ttu-id="208ce-153">1123</span><span class="sxs-lookup"><span data-stu-id="208ce-153">1123</span></span>                            |
| <span data-ttu-id="208ce-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-154">Search-Flags</span></span>           | <span data-ttu-id="208ce-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="208ce-155">0x00000005</span></span>                      |
| <span data-ttu-id="208ce-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-156">System-Flags</span></span>           | <span data-ttu-id="208ce-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="208ce-157">0x00000010</span></span>                      |
| <span data-ttu-id="208ce-158">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="208ce-158">Classes used in</span></span>        | [<span data-ttu-id="208ce-159">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="208ce-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="208ce-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="208ce-160">Windows Server 2003</span></span>



| <span data-ttu-id="208ce-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="208ce-161">Entry</span></span> | <span data-ttu-id="208ce-162">Value</span><span class="sxs-lookup"><span data-stu-id="208ce-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="208ce-163">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="208ce-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="208ce-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="208ce-164">MAPI-Id</span></span>                | <span data-ttu-id="208ce-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="208ce-165">0x800F</span></span>                          |
| <span data-ttu-id="208ce-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="208ce-166">System-Only</span></span>            | <span data-ttu-id="208ce-167">False</span><span class="sxs-lookup"><span data-stu-id="208ce-167">False</span></span>                           |
| <span data-ttu-id="208ce-168">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="208ce-168">Is-Single-Valued</span></span>       | <span data-ttu-id="208ce-169">False</span><span class="sxs-lookup"><span data-stu-id="208ce-169">False</span></span>                           |
| <span data-ttu-id="208ce-170">Está indexado</span><span class="sxs-lookup"><span data-stu-id="208ce-170">Is Indexed</span></span>             | <span data-ttu-id="208ce-171">True</span><span class="sxs-lookup"><span data-stu-id="208ce-171">True</span></span>                            |
| <span data-ttu-id="208ce-172">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="208ce-172">In Global Catalog</span></span>      | <span data-ttu-id="208ce-173">False</span><span class="sxs-lookup"><span data-stu-id="208ce-173">False</span></span>                           |
| <span data-ttu-id="208ce-174">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="208ce-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="208ce-175">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="208ce-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="208ce-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="208ce-176">Range-Lower</span></span>            | <span data-ttu-id="208ce-177">1</span><span class="sxs-lookup"><span data-stu-id="208ce-177">1</span></span>                               |
| <span data-ttu-id="208ce-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="208ce-178">Range-Upper</span></span>            | <span data-ttu-id="208ce-179">1123</span><span class="sxs-lookup"><span data-stu-id="208ce-179">1123</span></span>                            |
| <span data-ttu-id="208ce-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-180">Search-Flags</span></span>           | <span data-ttu-id="208ce-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="208ce-181">0x00000005</span></span>                      |
| <span data-ttu-id="208ce-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-182">System-Flags</span></span>           | <span data-ttu-id="208ce-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="208ce-183">0x00000010</span></span>                      |
| <span data-ttu-id="208ce-184">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="208ce-184">Classes used in</span></span>        | [<span data-ttu-id="208ce-185">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="208ce-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="208ce-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="208ce-186">ADAM</span></span>



| <span data-ttu-id="208ce-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="208ce-187">Entry</span></span> | <span data-ttu-id="208ce-188">Value</span><span class="sxs-lookup"><span data-stu-id="208ce-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="208ce-189">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="208ce-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="208ce-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="208ce-190">MAPI-Id</span></span>                | <span data-ttu-id="208ce-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="208ce-191">0x800F</span></span>                          |
| <span data-ttu-id="208ce-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="208ce-192">System-Only</span></span>            | <span data-ttu-id="208ce-193">False</span><span class="sxs-lookup"><span data-stu-id="208ce-193">False</span></span>                           |
| <span data-ttu-id="208ce-194">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="208ce-194">Is-Single-Valued</span></span>       | <span data-ttu-id="208ce-195">False</span><span class="sxs-lookup"><span data-stu-id="208ce-195">False</span></span>                           |
| <span data-ttu-id="208ce-196">Está indexado</span><span class="sxs-lookup"><span data-stu-id="208ce-196">Is Indexed</span></span>             | <span data-ttu-id="208ce-197">True</span><span class="sxs-lookup"><span data-stu-id="208ce-197">True</span></span>                            |
| <span data-ttu-id="208ce-198">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="208ce-198">In Global Catalog</span></span>      | <span data-ttu-id="208ce-199">False</span><span class="sxs-lookup"><span data-stu-id="208ce-199">False</span></span>                           |
| <span data-ttu-id="208ce-200">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="208ce-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="208ce-201">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="208ce-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="208ce-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="208ce-202">Range-Lower</span></span>            | <span data-ttu-id="208ce-203">1</span><span class="sxs-lookup"><span data-stu-id="208ce-203">1</span></span>                               |
| <span data-ttu-id="208ce-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="208ce-204">Range-Upper</span></span>            | <span data-ttu-id="208ce-205">1123</span><span class="sxs-lookup"><span data-stu-id="208ce-205">1123</span></span>                            |
| <span data-ttu-id="208ce-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-206">Search-Flags</span></span>           | <span data-ttu-id="208ce-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="208ce-207">0x00000005</span></span>                      |
| <span data-ttu-id="208ce-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-208">System-Flags</span></span>           | <span data-ttu-id="208ce-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="208ce-209">0x00000010</span></span>                      |
| <span data-ttu-id="208ce-210">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="208ce-210">Classes used in</span></span>        | [<span data-ttu-id="208ce-211">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="208ce-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="208ce-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="208ce-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="208ce-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="208ce-213">Entry</span></span> | <span data-ttu-id="208ce-214">Value</span><span class="sxs-lookup"><span data-stu-id="208ce-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="208ce-215">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="208ce-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="208ce-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="208ce-216">MAPI-Id</span></span>                | <span data-ttu-id="208ce-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="208ce-217">0x800F</span></span>                          |
| <span data-ttu-id="208ce-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="208ce-218">System-Only</span></span>            | <span data-ttu-id="208ce-219">False</span><span class="sxs-lookup"><span data-stu-id="208ce-219">False</span></span>                           |
| <span data-ttu-id="208ce-220">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="208ce-220">Is-Single-Valued</span></span>       | <span data-ttu-id="208ce-221">False</span><span class="sxs-lookup"><span data-stu-id="208ce-221">False</span></span>                           |
| <span data-ttu-id="208ce-222">Está indexado</span><span class="sxs-lookup"><span data-stu-id="208ce-222">Is Indexed</span></span>             | <span data-ttu-id="208ce-223">True</span><span class="sxs-lookup"><span data-stu-id="208ce-223">True</span></span>                            |
| <span data-ttu-id="208ce-224">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="208ce-224">In Global Catalog</span></span>      | <span data-ttu-id="208ce-225">False</span><span class="sxs-lookup"><span data-stu-id="208ce-225">False</span></span>                           |
| <span data-ttu-id="208ce-226">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="208ce-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="208ce-227">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="208ce-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="208ce-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="208ce-228">Range-Lower</span></span>            | <span data-ttu-id="208ce-229">1</span><span class="sxs-lookup"><span data-stu-id="208ce-229">1</span></span>                               |
| <span data-ttu-id="208ce-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="208ce-230">Range-Upper</span></span>            | <span data-ttu-id="208ce-231">1123</span><span class="sxs-lookup"><span data-stu-id="208ce-231">1123</span></span>                            |
| <span data-ttu-id="208ce-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-232">Search-Flags</span></span>           | <span data-ttu-id="208ce-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="208ce-233">0x00000005</span></span>                      |
| <span data-ttu-id="208ce-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-234">System-Flags</span></span>           | <span data-ttu-id="208ce-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="208ce-235">0x00000010</span></span>                      |
| <span data-ttu-id="208ce-236">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="208ce-236">Classes used in</span></span>        | [<span data-ttu-id="208ce-237">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="208ce-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="208ce-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="208ce-238">Windows Server 2008</span></span>



| <span data-ttu-id="208ce-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="208ce-239">Entry</span></span> | <span data-ttu-id="208ce-240">Value</span><span class="sxs-lookup"><span data-stu-id="208ce-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="208ce-241">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="208ce-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="208ce-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="208ce-242">MAPI-Id</span></span>                | <span data-ttu-id="208ce-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="208ce-243">0x800F</span></span>                          |
| <span data-ttu-id="208ce-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="208ce-244">System-Only</span></span>            | <span data-ttu-id="208ce-245">False</span><span class="sxs-lookup"><span data-stu-id="208ce-245">False</span></span>                           |
| <span data-ttu-id="208ce-246">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="208ce-246">Is-Single-Valued</span></span>       | <span data-ttu-id="208ce-247">False</span><span class="sxs-lookup"><span data-stu-id="208ce-247">False</span></span>                           |
| <span data-ttu-id="208ce-248">Está indexado</span><span class="sxs-lookup"><span data-stu-id="208ce-248">Is Indexed</span></span>             | <span data-ttu-id="208ce-249">True</span><span class="sxs-lookup"><span data-stu-id="208ce-249">True</span></span>                            |
| <span data-ttu-id="208ce-250">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="208ce-250">In Global Catalog</span></span>      | <span data-ttu-id="208ce-251">False</span><span class="sxs-lookup"><span data-stu-id="208ce-251">False</span></span>                           |
| <span data-ttu-id="208ce-252">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="208ce-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="208ce-253">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="208ce-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="208ce-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="208ce-254">Range-Lower</span></span>            | <span data-ttu-id="208ce-255">1</span><span class="sxs-lookup"><span data-stu-id="208ce-255">1</span></span>                               |
| <span data-ttu-id="208ce-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="208ce-256">Range-Upper</span></span>            | <span data-ttu-id="208ce-257">1123</span><span class="sxs-lookup"><span data-stu-id="208ce-257">1123</span></span>                            |
| <span data-ttu-id="208ce-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-258">Search-Flags</span></span>           | <span data-ttu-id="208ce-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="208ce-259">0x00000005</span></span>                      |
| <span data-ttu-id="208ce-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-260">System-Flags</span></span>           | <span data-ttu-id="208ce-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="208ce-261">0x00000010</span></span>                      |
| <span data-ttu-id="208ce-262">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="208ce-262">Classes used in</span></span>        | [<span data-ttu-id="208ce-263">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="208ce-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="208ce-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="208ce-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="208ce-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="208ce-265">Entry</span></span> | <span data-ttu-id="208ce-266">Value</span><span class="sxs-lookup"><span data-stu-id="208ce-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="208ce-267">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="208ce-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="208ce-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="208ce-268">MAPI-Id</span></span>                | <span data-ttu-id="208ce-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="208ce-269">0x800F</span></span>                          |
| <span data-ttu-id="208ce-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="208ce-270">System-Only</span></span>            | <span data-ttu-id="208ce-271">False</span><span class="sxs-lookup"><span data-stu-id="208ce-271">False</span></span>                           |
| <span data-ttu-id="208ce-272">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="208ce-272">Is-Single-Valued</span></span>       | <span data-ttu-id="208ce-273">False</span><span class="sxs-lookup"><span data-stu-id="208ce-273">False</span></span>                           |
| <span data-ttu-id="208ce-274">Está indexado</span><span class="sxs-lookup"><span data-stu-id="208ce-274">Is Indexed</span></span>             | <span data-ttu-id="208ce-275">True</span><span class="sxs-lookup"><span data-stu-id="208ce-275">True</span></span>                            |
| <span data-ttu-id="208ce-276">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="208ce-276">In Global Catalog</span></span>      | <span data-ttu-id="208ce-277">False</span><span class="sxs-lookup"><span data-stu-id="208ce-277">False</span></span>                           |
| <span data-ttu-id="208ce-278">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="208ce-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="208ce-279">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="208ce-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="208ce-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="208ce-280">Range-Lower</span></span>            | <span data-ttu-id="208ce-281">1</span><span class="sxs-lookup"><span data-stu-id="208ce-281">1</span></span>                               |
| <span data-ttu-id="208ce-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="208ce-282">Range-Upper</span></span>            | <span data-ttu-id="208ce-283">1123</span><span class="sxs-lookup"><span data-stu-id="208ce-283">1123</span></span>                            |
| <span data-ttu-id="208ce-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-284">Search-Flags</span></span>           | <span data-ttu-id="208ce-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="208ce-285">0x00000005</span></span>                      |
| <span data-ttu-id="208ce-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-286">System-Flags</span></span>           | <span data-ttu-id="208ce-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="208ce-287">0x00000010</span></span>                      |
| <span data-ttu-id="208ce-288">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="208ce-288">Classes used in</span></span>        | [<span data-ttu-id="208ce-289">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="208ce-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="208ce-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="208ce-290">Windows Server 2012</span></span>



| <span data-ttu-id="208ce-291">Entrada</span><span class="sxs-lookup"><span data-stu-id="208ce-291">Entry</span></span> | <span data-ttu-id="208ce-292">Value</span><span class="sxs-lookup"><span data-stu-id="208ce-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="208ce-293">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="208ce-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="208ce-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="208ce-294">MAPI-Id</span></span>                | <span data-ttu-id="208ce-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="208ce-295">0x800F</span></span>                          |
| <span data-ttu-id="208ce-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="208ce-296">System-Only</span></span>            | <span data-ttu-id="208ce-297">False</span><span class="sxs-lookup"><span data-stu-id="208ce-297">False</span></span>                           |
| <span data-ttu-id="208ce-298">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="208ce-298">Is-Single-Valued</span></span>       | <span data-ttu-id="208ce-299">False</span><span class="sxs-lookup"><span data-stu-id="208ce-299">False</span></span>                           |
| <span data-ttu-id="208ce-300">Está indexado</span><span class="sxs-lookup"><span data-stu-id="208ce-300">Is Indexed</span></span>             | <span data-ttu-id="208ce-301">True</span><span class="sxs-lookup"><span data-stu-id="208ce-301">True</span></span>                            |
| <span data-ttu-id="208ce-302">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="208ce-302">In Global Catalog</span></span>      | <span data-ttu-id="208ce-303">False</span><span class="sxs-lookup"><span data-stu-id="208ce-303">False</span></span>                           |
| <span data-ttu-id="208ce-304">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="208ce-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="208ce-305">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="208ce-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="208ce-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="208ce-306">Range-Lower</span></span>            | <span data-ttu-id="208ce-307">1</span><span class="sxs-lookup"><span data-stu-id="208ce-307">1</span></span>                               |
| <span data-ttu-id="208ce-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="208ce-308">Range-Upper</span></span>            | <span data-ttu-id="208ce-309">1123</span><span class="sxs-lookup"><span data-stu-id="208ce-309">1123</span></span>                            |
| <span data-ttu-id="208ce-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-310">Search-Flags</span></span>           | <span data-ttu-id="208ce-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="208ce-311">0x00000005</span></span>                      |
| <span data-ttu-id="208ce-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="208ce-312">System-Flags</span></span>           | <span data-ttu-id="208ce-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="208ce-313">0x00000010</span></span>                      |
| <span data-ttu-id="208ce-314">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="208ce-314">Classes used in</span></span>        | [<span data-ttu-id="208ce-315">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="208ce-315">**Top**</span></span>](c-top.md)<br/> |



 

 






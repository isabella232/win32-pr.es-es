---
title: Netboot-Machine-File-Path (atributo)
description: Este atributo especifica el servidor que responde al cliente. A partir del sistema operativo Windows Server 2003, puede indicar el Startrom.com que el cliente obtiene.
ms.assetid: 8706bf38-8027-4260-b382-4d4c2a6e0f6e
ms.tgt_platform: multiple
keywords:
- Netboot-Machine-File-path atributo AD Schema
- netbootMachineFilePath esquema de AD de atributos
topic_type:
- apiref
api_name:
- Netboot-Machine-File-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d03ead4f307b7c0b524192d9c865ee437fbd9d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658795"
---
# <a name="netboot-machine-file-path-attribute"></a><span data-ttu-id="8cad2-106">Netboot-Machine-File-Path (atributo)</span><span class="sxs-lookup"><span data-stu-id="8cad2-106">Netboot-Machine-File-Path attribute</span></span>

<span data-ttu-id="8cad2-107">Este atributo especifica el servidor que responde al cliente.</span><span class="sxs-lookup"><span data-stu-id="8cad2-107">This attribute specifies the server that answers the client.</span></span> <span data-ttu-id="8cad2-108">A partir del sistema operativo Windows Server 2003, puede indicar el Startrom.com que el cliente obtiene.</span><span class="sxs-lookup"><span data-stu-id="8cad2-108">Beginning with the Windows Server 2003 operating system, it can indicate the Startrom.com that the client gets.</span></span>



| <span data-ttu-id="8cad2-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cad2-109">Entry</span></span> | <span data-ttu-id="8cad2-110">Value</span><span class="sxs-lookup"><span data-stu-id="8cad2-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8cad2-111">CN</span><span class="sxs-lookup"><span data-stu-id="8cad2-111">CN</span></span>                | <span data-ttu-id="8cad2-112">Netboot-Machine-File-path</span><span class="sxs-lookup"><span data-stu-id="8cad2-112">Netboot-Machine-File-Path</span></span>                   |
| <span data-ttu-id="8cad2-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="8cad2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8cad2-114">netbootMachineFilePath</span><span class="sxs-lookup"><span data-stu-id="8cad2-114">netbootMachineFilePath</span></span>                      |
| <span data-ttu-id="8cad2-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8cad2-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="8cad2-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="8cad2-116">Update Privilege</span></span>  | <span data-ttu-id="8cad2-117">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="8cad2-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="8cad2-118">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="8cad2-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8cad2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8cad2-119">Attribute-Id</span></span>      | <span data-ttu-id="8cad2-120">1.2.840.113556.1.4.361</span><span class="sxs-lookup"><span data-stu-id="8cad2-120">1.2.840.113556.1.4.361</span></span>                      |
| <span data-ttu-id="8cad2-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8cad2-121">System-Id-Guid</span></span>    | <span data-ttu-id="8cad2-122">3e978923-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="8cad2-122">3e978923-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="8cad2-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cad2-123">Syntax</span></span>            | [<span data-ttu-id="8cad2-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8cad2-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8cad2-125">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="8cad2-125">Implementations</span></span>

-   [<span data-ttu-id="8cad2-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8cad2-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8cad2-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8cad2-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8cad2-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8cad2-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8cad2-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8cad2-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8cad2-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8cad2-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8cad2-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8cad2-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8cad2-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cad2-132">Windows 2000 Server</span></span>



| <span data-ttu-id="8cad2-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cad2-133">Entry</span></span> | <span data-ttu-id="8cad2-134">Value</span><span class="sxs-lookup"><span data-stu-id="8cad2-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cad2-135">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8cad2-135">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cad2-136">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cad2-137">System-Only</span></span>            | <span data-ttu-id="8cad2-138">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-138">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-139">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8cad2-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8cad2-140">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-140">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-141">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8cad2-141">Is Indexed</span></span>             | <span data-ttu-id="8cad2-142">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-142">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-143">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cad2-143">In Global Catalog</span></span>      | <span data-ttu-id="8cad2-144">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-144">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-145">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8cad2-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cad2-146">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cad2-146">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8cad2-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cad2-147">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cad2-148">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-149">Search-Flags</span></span>           | <span data-ttu-id="8cad2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cad2-150">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8cad2-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-151">System-Flags</span></span>           | <span data-ttu-id="8cad2-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cad2-152">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8cad2-153">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8cad2-153">Classes used in</span></span>        | [<span data-ttu-id="8cad2-154">**Computer**</span><span class="sxs-lookup"><span data-stu-id="8cad2-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8cad2-155">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8cad2-155">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8cad2-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cad2-156">Windows Server 2003</span></span>



| <span data-ttu-id="8cad2-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cad2-157">Entry</span></span> | <span data-ttu-id="8cad2-158">Value</span><span class="sxs-lookup"><span data-stu-id="8cad2-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cad2-159">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8cad2-159">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cad2-160">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cad2-161">System-Only</span></span>            | <span data-ttu-id="8cad2-162">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-162">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-163">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8cad2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8cad2-164">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-164">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-165">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8cad2-165">Is Indexed</span></span>             | <span data-ttu-id="8cad2-166">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-166">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-167">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cad2-167">In Global Catalog</span></span>      | <span data-ttu-id="8cad2-168">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-168">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-169">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8cad2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cad2-170">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cad2-170">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8cad2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cad2-171">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cad2-172">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-173">Search-Flags</span></span>           | <span data-ttu-id="8cad2-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cad2-174">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8cad2-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-175">System-Flags</span></span>           | <span data-ttu-id="8cad2-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cad2-176">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8cad2-177">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8cad2-177">Classes used in</span></span>        | [<span data-ttu-id="8cad2-178">**Computer**</span><span class="sxs-lookup"><span data-stu-id="8cad2-178">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8cad2-179">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8cad2-179">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8cad2-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8cad2-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8cad2-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cad2-181">Entry</span></span> | <span data-ttu-id="8cad2-182">Value</span><span class="sxs-lookup"><span data-stu-id="8cad2-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cad2-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8cad2-183">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cad2-184">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cad2-185">System-Only</span></span>            | <span data-ttu-id="8cad2-186">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-186">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8cad2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="8cad2-188">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-188">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8cad2-189">Is Indexed</span></span>             | <span data-ttu-id="8cad2-190">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-190">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cad2-191">In Global Catalog</span></span>      | <span data-ttu-id="8cad2-192">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-192">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8cad2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cad2-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cad2-194">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8cad2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cad2-195">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cad2-196">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-197">Search-Flags</span></span>           | <span data-ttu-id="8cad2-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cad2-198">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8cad2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-199">System-Flags</span></span>           | <span data-ttu-id="8cad2-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cad2-200">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8cad2-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8cad2-201">Classes used in</span></span>        | [<span data-ttu-id="8cad2-202">**Computer**</span><span class="sxs-lookup"><span data-stu-id="8cad2-202">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8cad2-203">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8cad2-203">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8cad2-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cad2-204">Windows Server 2008</span></span>



| <span data-ttu-id="8cad2-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cad2-205">Entry</span></span> | <span data-ttu-id="8cad2-206">Value</span><span class="sxs-lookup"><span data-stu-id="8cad2-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cad2-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8cad2-207">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cad2-208">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cad2-209">System-Only</span></span>            | <span data-ttu-id="8cad2-210">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-210">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8cad2-211">Is-Single-Valued</span></span>       | <span data-ttu-id="8cad2-212">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-212">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8cad2-213">Is Indexed</span></span>             | <span data-ttu-id="8cad2-214">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-214">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cad2-215">In Global Catalog</span></span>      | <span data-ttu-id="8cad2-216">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-216">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8cad2-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cad2-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cad2-218">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8cad2-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cad2-219">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cad2-220">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-221">Search-Flags</span></span>           | <span data-ttu-id="8cad2-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cad2-222">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8cad2-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-223">System-Flags</span></span>           | <span data-ttu-id="8cad2-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cad2-224">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8cad2-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8cad2-225">Classes used in</span></span>        | [<span data-ttu-id="8cad2-226">**Computer**</span><span class="sxs-lookup"><span data-stu-id="8cad2-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8cad2-227">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8cad2-227">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8cad2-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8cad2-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8cad2-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cad2-229">Entry</span></span> | <span data-ttu-id="8cad2-230">Value</span><span class="sxs-lookup"><span data-stu-id="8cad2-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cad2-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8cad2-231">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cad2-232">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cad2-233">System-Only</span></span>            | <span data-ttu-id="8cad2-234">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-234">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8cad2-235">Is-Single-Valued</span></span>       | <span data-ttu-id="8cad2-236">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-236">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8cad2-237">Is Indexed</span></span>             | <span data-ttu-id="8cad2-238">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-238">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cad2-239">In Global Catalog</span></span>      | <span data-ttu-id="8cad2-240">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-240">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8cad2-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cad2-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cad2-242">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8cad2-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cad2-243">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cad2-244">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-245">Search-Flags</span></span>           | <span data-ttu-id="8cad2-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cad2-246">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8cad2-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-247">System-Flags</span></span>           | <span data-ttu-id="8cad2-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cad2-248">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8cad2-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8cad2-249">Classes used in</span></span>        | [<span data-ttu-id="8cad2-250">**Computer**</span><span class="sxs-lookup"><span data-stu-id="8cad2-250">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8cad2-251">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8cad2-251">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8cad2-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8cad2-252">Windows Server 2012</span></span>



| <span data-ttu-id="8cad2-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cad2-253">Entry</span></span> | <span data-ttu-id="8cad2-254">Value</span><span class="sxs-lookup"><span data-stu-id="8cad2-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cad2-255">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="8cad2-255">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cad2-256">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="8cad2-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cad2-257">System-Only</span></span>            | <span data-ttu-id="8cad2-258">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-258">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-259">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="8cad2-259">Is-Single-Valued</span></span>       | <span data-ttu-id="8cad2-260">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-260">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-261">Está indexado</span><span class="sxs-lookup"><span data-stu-id="8cad2-261">Is Indexed</span></span>             | <span data-ttu-id="8cad2-262">False</span><span class="sxs-lookup"><span data-stu-id="8cad2-262">False</span></span>                                                                                                |
| <span data-ttu-id="8cad2-263">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cad2-263">In Global Catalog</span></span>      | <span data-ttu-id="8cad2-264">True</span><span class="sxs-lookup"><span data-stu-id="8cad2-264">True</span></span>                                                                                                 |
| <span data-ttu-id="8cad2-265">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="8cad2-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cad2-266">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cad2-266">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="8cad2-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cad2-267">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cad2-268">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="8cad2-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-269">Search-Flags</span></span>           | <span data-ttu-id="8cad2-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cad2-270">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="8cad2-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cad2-271">System-Flags</span></span>           | <span data-ttu-id="8cad2-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cad2-272">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="8cad2-273">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="8cad2-273">Classes used in</span></span>        | [<span data-ttu-id="8cad2-274">**Computer**</span><span class="sxs-lookup"><span data-stu-id="8cad2-274">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="8cad2-275">**IntelliMirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="8cad2-275">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 






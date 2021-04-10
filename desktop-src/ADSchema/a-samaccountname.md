---
title: Atributo SAM-Account-Name
description: Nombre de inicio de sesión que se usa para admitir clientes y servidores que ejecutan versiones anteriores del sistema operativo, como Windows NT 4,0, Windows 95, Windows 98 y LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre de cuenta SAM
- atributo sAMAccountName esquema de AD
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906114"
---
# <a name="sam-account-name-attribute"></a><span data-ttu-id="7892e-105">Atributo SAM-Account-Name</span><span class="sxs-lookup"><span data-stu-id="7892e-105">SAM-Account-Name attribute</span></span>

<span data-ttu-id="7892e-106">Nombre de inicio de sesión que se usa para admitir clientes y servidores que ejecutan versiones anteriores del sistema operativo, como Windows NT 4,0, Windows 95, Windows 98 y LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="7892e-106">The logon name used to support clients and servers running earlier versions of the operating system, such as Windows NT 4.0, Windows 95, Windows 98, and LAN Manager.</span></span>

<span data-ttu-id="7892e-107">Este atributo debe tener 20 caracteres o menos para admitir clientes anteriores y no puede contener ninguno de estos caracteres:</span><span class="sxs-lookup"><span data-stu-id="7892e-107">This attribute must be 20 characters or less to support earlier clients, and cannot contain any of these characters:</span></span>

-   <span data-ttu-id="7892e-108">"/ \\ \[ \] : ; \| = , + \* ?</span><span class="sxs-lookup"><span data-stu-id="7892e-108">"/ \\ \[ \] : ; \| = , + \* ?</span></span> <span data-ttu-id="7892e-109">< ></span><span class="sxs-lookup"><span data-stu-id="7892e-109">< ></span></span>



| <span data-ttu-id="7892e-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="7892e-110">Entry</span></span> | <span data-ttu-id="7892e-111">Value</span><span class="sxs-lookup"><span data-stu-id="7892e-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7892e-112">CN</span><span class="sxs-lookup"><span data-stu-id="7892e-112">CN</span></span>                | <span data-ttu-id="7892e-113">Nombre de cuenta SAM</span><span class="sxs-lookup"><span data-stu-id="7892e-113">SAM-Account-Name</span></span>                                                                         |
| <span data-ttu-id="7892e-114">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="7892e-114">Ldap-Display-Name</span></span> | <span data-ttu-id="7892e-115">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="7892e-115">sAMAccountName</span></span>                                                                           |
| <span data-ttu-id="7892e-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7892e-116">Size</span></span>              | <span data-ttu-id="7892e-117">20 caracteres o menos.</span><span class="sxs-lookup"><span data-stu-id="7892e-117">20 characters or less.</span></span>                                                                   |
| <span data-ttu-id="7892e-118">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="7892e-118">Update Privilege</span></span>  | <span data-ttu-id="7892e-119">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="7892e-119">Domain administrator</span></span>                                                                     |
| <span data-ttu-id="7892e-120">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="7892e-120">Update Frequency</span></span>  | <span data-ttu-id="7892e-121">Este valor debe asignarse cuando se crea el registro de cuenta y no debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="7892e-121">This value should be assigned when the account record is created, and should not change.</span></span> |
| <span data-ttu-id="7892e-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7892e-122">Attribute-Id</span></span>      | <span data-ttu-id="7892e-123">1.2.840.113556.1.4.221</span><span class="sxs-lookup"><span data-stu-id="7892e-123">1.2.840.113556.1.4.221</span></span>                                                                   |
| <span data-ttu-id="7892e-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7892e-124">System-Id-Guid</span></span>    | <span data-ttu-id="7892e-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="7892e-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span></span>                                                     |
| <span data-ttu-id="7892e-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7892e-126">Syntax</span></span>            | [<span data-ttu-id="7892e-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7892e-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                              |



## <a name="implementations"></a><span data-ttu-id="7892e-128">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="7892e-128">Implementations</span></span>

-   [<span data-ttu-id="7892e-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7892e-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7892e-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7892e-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7892e-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7892e-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7892e-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7892e-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7892e-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7892e-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7892e-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7892e-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7892e-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7892e-135">Windows 2000 Server</span></span>



| <span data-ttu-id="7892e-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="7892e-136">Entry</span></span> | <span data-ttu-id="7892e-137">Value</span><span class="sxs-lookup"><span data-stu-id="7892e-137">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7892e-138">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7892e-138">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7892e-139">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="7892e-140">System-Only</span></span>            | <span data-ttu-id="7892e-141">False</span><span class="sxs-lookup"><span data-stu-id="7892e-141">False</span></span>                                                        |
| <span data-ttu-id="7892e-142">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7892e-142">Is-Single-Valued</span></span>       | <span data-ttu-id="7892e-143">True</span><span class="sxs-lookup"><span data-stu-id="7892e-143">True</span></span>                                                         |
| <span data-ttu-id="7892e-144">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7892e-144">Is Indexed</span></span>             | <span data-ttu-id="7892e-145">True</span><span class="sxs-lookup"><span data-stu-id="7892e-145">True</span></span>                                                         |
| <span data-ttu-id="7892e-146">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7892e-146">In Global Catalog</span></span>      | <span data-ttu-id="7892e-147">True</span><span class="sxs-lookup"><span data-stu-id="7892e-147">True</span></span>                                                         |
| <span data-ttu-id="7892e-148">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7892e-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="7892e-149">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7892e-149">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7892e-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7892e-150">Range-Lower</span></span>            | <span data-ttu-id="7892e-151">0</span><span class="sxs-lookup"><span data-stu-id="7892e-151">0</span></span>                                                            |
| <span data-ttu-id="7892e-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7892e-152">Range-Upper</span></span>            | <span data-ttu-id="7892e-153">256</span><span class="sxs-lookup"><span data-stu-id="7892e-153">256</span></span>                                                          |
| <span data-ttu-id="7892e-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-154">Search-Flags</span></span>           | <span data-ttu-id="7892e-155">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="7892e-155">0x0000000D</span></span>                                                   |
| <span data-ttu-id="7892e-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-156">System-Flags</span></span>           | <span data-ttu-id="7892e-157">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7892e-157">0x00000012</span></span>                                                   |
| <span data-ttu-id="7892e-158">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7892e-158">Classes used in</span></span>        | [<span data-ttu-id="7892e-159">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7892e-159">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7892e-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7892e-160">Windows Server 2003</span></span>



| <span data-ttu-id="7892e-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="7892e-161">Entry</span></span> | <span data-ttu-id="7892e-162">Value</span><span class="sxs-lookup"><span data-stu-id="7892e-162">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7892e-163">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7892e-163">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7892e-164">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="7892e-165">System-Only</span></span>            | <span data-ttu-id="7892e-166">False</span><span class="sxs-lookup"><span data-stu-id="7892e-166">False</span></span>                                                        |
| <span data-ttu-id="7892e-167">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7892e-167">Is-Single-Valued</span></span>       | <span data-ttu-id="7892e-168">True</span><span class="sxs-lookup"><span data-stu-id="7892e-168">True</span></span>                                                         |
| <span data-ttu-id="7892e-169">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7892e-169">Is Indexed</span></span>             | <span data-ttu-id="7892e-170">True</span><span class="sxs-lookup"><span data-stu-id="7892e-170">True</span></span>                                                         |
| <span data-ttu-id="7892e-171">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7892e-171">In Global Catalog</span></span>      | <span data-ttu-id="7892e-172">True</span><span class="sxs-lookup"><span data-stu-id="7892e-172">True</span></span>                                                         |
| <span data-ttu-id="7892e-173">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7892e-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="7892e-174">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7892e-174">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7892e-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7892e-175">Range-Lower</span></span>            | <span data-ttu-id="7892e-176">0</span><span class="sxs-lookup"><span data-stu-id="7892e-176">0</span></span>                                                            |
| <span data-ttu-id="7892e-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7892e-177">Range-Upper</span></span>            | <span data-ttu-id="7892e-178">256</span><span class="sxs-lookup"><span data-stu-id="7892e-178">256</span></span>                                                          |
| <span data-ttu-id="7892e-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-179">Search-Flags</span></span>           | <span data-ttu-id="7892e-180">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="7892e-180">0x0000000D</span></span>                                                   |
| <span data-ttu-id="7892e-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-181">System-Flags</span></span>           | <span data-ttu-id="7892e-182">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7892e-182">0x00000012</span></span>                                                   |
| <span data-ttu-id="7892e-183">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7892e-183">Classes used in</span></span>        | [<span data-ttu-id="7892e-184">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7892e-184">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7892e-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7892e-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7892e-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="7892e-186">Entry</span></span> | <span data-ttu-id="7892e-187">Value</span><span class="sxs-lookup"><span data-stu-id="7892e-187">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7892e-188">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7892e-188">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7892e-189">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="7892e-190">System-Only</span></span>            | <span data-ttu-id="7892e-191">False</span><span class="sxs-lookup"><span data-stu-id="7892e-191">False</span></span>                                                        |
| <span data-ttu-id="7892e-192">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7892e-192">Is-Single-Valued</span></span>       | <span data-ttu-id="7892e-193">True</span><span class="sxs-lookup"><span data-stu-id="7892e-193">True</span></span>                                                         |
| <span data-ttu-id="7892e-194">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7892e-194">Is Indexed</span></span>             | <span data-ttu-id="7892e-195">True</span><span class="sxs-lookup"><span data-stu-id="7892e-195">True</span></span>                                                         |
| <span data-ttu-id="7892e-196">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7892e-196">In Global Catalog</span></span>      | <span data-ttu-id="7892e-197">True</span><span class="sxs-lookup"><span data-stu-id="7892e-197">True</span></span>                                                         |
| <span data-ttu-id="7892e-198">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7892e-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="7892e-199">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7892e-199">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7892e-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7892e-200">Range-Lower</span></span>            | <span data-ttu-id="7892e-201">0</span><span class="sxs-lookup"><span data-stu-id="7892e-201">0</span></span>                                                            |
| <span data-ttu-id="7892e-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7892e-202">Range-Upper</span></span>            | <span data-ttu-id="7892e-203">256</span><span class="sxs-lookup"><span data-stu-id="7892e-203">256</span></span>                                                          |
| <span data-ttu-id="7892e-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-204">Search-Flags</span></span>           | <span data-ttu-id="7892e-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="7892e-205">0x0000000D</span></span>                                                   |
| <span data-ttu-id="7892e-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-206">System-Flags</span></span>           | <span data-ttu-id="7892e-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7892e-207">0x00000012</span></span>                                                   |
| <span data-ttu-id="7892e-208">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7892e-208">Classes used in</span></span>        | [<span data-ttu-id="7892e-209">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7892e-209">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7892e-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7892e-210">Windows Server 2008</span></span>



| <span data-ttu-id="7892e-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="7892e-211">Entry</span></span> | <span data-ttu-id="7892e-212">Value</span><span class="sxs-lookup"><span data-stu-id="7892e-212">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7892e-213">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7892e-213">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7892e-214">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="7892e-215">System-Only</span></span>            | <span data-ttu-id="7892e-216">False</span><span class="sxs-lookup"><span data-stu-id="7892e-216">False</span></span>                                                        |
| <span data-ttu-id="7892e-217">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7892e-217">Is-Single-Valued</span></span>       | <span data-ttu-id="7892e-218">True</span><span class="sxs-lookup"><span data-stu-id="7892e-218">True</span></span>                                                         |
| <span data-ttu-id="7892e-219">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7892e-219">Is Indexed</span></span>             | <span data-ttu-id="7892e-220">True</span><span class="sxs-lookup"><span data-stu-id="7892e-220">True</span></span>                                                         |
| <span data-ttu-id="7892e-221">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7892e-221">In Global Catalog</span></span>      | <span data-ttu-id="7892e-222">True</span><span class="sxs-lookup"><span data-stu-id="7892e-222">True</span></span>                                                         |
| <span data-ttu-id="7892e-223">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7892e-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="7892e-224">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7892e-224">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7892e-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7892e-225">Range-Lower</span></span>            | <span data-ttu-id="7892e-226">0</span><span class="sxs-lookup"><span data-stu-id="7892e-226">0</span></span>                                                            |
| <span data-ttu-id="7892e-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7892e-227">Range-Upper</span></span>            | <span data-ttu-id="7892e-228">256</span><span class="sxs-lookup"><span data-stu-id="7892e-228">256</span></span>                                                          |
| <span data-ttu-id="7892e-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-229">Search-Flags</span></span>           | <span data-ttu-id="7892e-230">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="7892e-230">0x0000000D</span></span>                                                   |
| <span data-ttu-id="7892e-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-231">System-Flags</span></span>           | <span data-ttu-id="7892e-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7892e-232">0x00000012</span></span>                                                   |
| <span data-ttu-id="7892e-233">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7892e-233">Classes used in</span></span>        | [<span data-ttu-id="7892e-234">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7892e-234">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7892e-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7892e-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7892e-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="7892e-236">Entry</span></span> | <span data-ttu-id="7892e-237">Value</span><span class="sxs-lookup"><span data-stu-id="7892e-237">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7892e-238">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7892e-238">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7892e-239">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="7892e-240">System-Only</span></span>            | <span data-ttu-id="7892e-241">False</span><span class="sxs-lookup"><span data-stu-id="7892e-241">False</span></span>                                                        |
| <span data-ttu-id="7892e-242">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7892e-242">Is-Single-Valued</span></span>       | <span data-ttu-id="7892e-243">True</span><span class="sxs-lookup"><span data-stu-id="7892e-243">True</span></span>                                                         |
| <span data-ttu-id="7892e-244">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7892e-244">Is Indexed</span></span>             | <span data-ttu-id="7892e-245">True</span><span class="sxs-lookup"><span data-stu-id="7892e-245">True</span></span>                                                         |
| <span data-ttu-id="7892e-246">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7892e-246">In Global Catalog</span></span>      | <span data-ttu-id="7892e-247">True</span><span class="sxs-lookup"><span data-stu-id="7892e-247">True</span></span>                                                         |
| <span data-ttu-id="7892e-248">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7892e-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="7892e-249">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7892e-249">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7892e-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7892e-250">Range-Lower</span></span>            | <span data-ttu-id="7892e-251">0</span><span class="sxs-lookup"><span data-stu-id="7892e-251">0</span></span>                                                            |
| <span data-ttu-id="7892e-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7892e-252">Range-Upper</span></span>            | <span data-ttu-id="7892e-253">256</span><span class="sxs-lookup"><span data-stu-id="7892e-253">256</span></span>                                                          |
| <span data-ttu-id="7892e-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-254">Search-Flags</span></span>           | <span data-ttu-id="7892e-255">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="7892e-255">0x0000000D</span></span>                                                   |
| <span data-ttu-id="7892e-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-256">System-Flags</span></span>           | <span data-ttu-id="7892e-257">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7892e-257">0x00000012</span></span>                                                   |
| <span data-ttu-id="7892e-258">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7892e-258">Classes used in</span></span>        | [<span data-ttu-id="7892e-259">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7892e-259">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7892e-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7892e-260">Windows Server 2012</span></span>



| <span data-ttu-id="7892e-261">Entrada</span><span class="sxs-lookup"><span data-stu-id="7892e-261">Entry</span></span> | <span data-ttu-id="7892e-262">Value</span><span class="sxs-lookup"><span data-stu-id="7892e-262">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7892e-263">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="7892e-263">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7892e-264">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7892e-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="7892e-265">System-Only</span></span>            | <span data-ttu-id="7892e-266">False</span><span class="sxs-lookup"><span data-stu-id="7892e-266">False</span></span>                                                        |
| <span data-ttu-id="7892e-267">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="7892e-267">Is-Single-Valued</span></span>       | <span data-ttu-id="7892e-268">True</span><span class="sxs-lookup"><span data-stu-id="7892e-268">True</span></span>                                                         |
| <span data-ttu-id="7892e-269">Está indexado</span><span class="sxs-lookup"><span data-stu-id="7892e-269">Is Indexed</span></span>             | <span data-ttu-id="7892e-270">True</span><span class="sxs-lookup"><span data-stu-id="7892e-270">True</span></span>                                                         |
| <span data-ttu-id="7892e-271">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="7892e-271">In Global Catalog</span></span>      | <span data-ttu-id="7892e-272">True</span><span class="sxs-lookup"><span data-stu-id="7892e-272">True</span></span>                                                         |
| <span data-ttu-id="7892e-273">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="7892e-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="7892e-274">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7892e-274">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7892e-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7892e-275">Range-Lower</span></span>            | <span data-ttu-id="7892e-276">0</span><span class="sxs-lookup"><span data-stu-id="7892e-276">0</span></span>                                                            |
| <span data-ttu-id="7892e-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7892e-277">Range-Upper</span></span>            | <span data-ttu-id="7892e-278">256</span><span class="sxs-lookup"><span data-stu-id="7892e-278">256</span></span>                                                          |
| <span data-ttu-id="7892e-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-279">Search-Flags</span></span>           | <span data-ttu-id="7892e-280">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="7892e-280">0x0000000D</span></span>                                                   |
| <span data-ttu-id="7892e-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7892e-281">System-Flags</span></span>           | <span data-ttu-id="7892e-282">0x00000012</span><span class="sxs-lookup"><span data-stu-id="7892e-282">0x00000012</span></span>                                                   |
| <span data-ttu-id="7892e-283">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="7892e-283">Classes used in</span></span>        | [<span data-ttu-id="7892e-284">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="7892e-284">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 






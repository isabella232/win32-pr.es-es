---
title: Home-Drive atributo)
description: Especifica la letra de unidad a la que se va a asignar la ruta de acceso UNC especificada por homeDirectory.
ms.assetid: fa402e14-febf-4ed9-bcc6-a6bfd405068c
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Home-Drive
- atributo homeDrive AD Schema
topic_type:
- apiref
api_name:
- Home-Drive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce9bff87662cc3b9da962b0c5647e79e90a3068
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658507"
---
# <a name="home-drive-attribute"></a><span data-ttu-id="55e9c-105">Home-Drive atributo)</span><span class="sxs-lookup"><span data-stu-id="55e9c-105">Home-Drive attribute</span></span>

<span data-ttu-id="55e9c-106">Especifica la letra de unidad a la que se va a asignar la ruta de acceso UNC especificada por [**HomeDirectory**](a-homedirectory.md).</span><span class="sxs-lookup"><span data-stu-id="55e9c-106">Specifies the drive letter to which to map the UNC path specified by [**homeDirectory**](a-homedirectory.md).</span></span> <span data-ttu-id="55e9c-107">La letra de unidad debe especificarse con el formato \*letraDeUnidad \* \* \*:\*\*, donde *letraDeUnidad* es la letra de la unidad que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="55e9c-107">The drive letter must be specified in the form *DriveLetter\*\*\*:*\* where *DriveLetter* is the letter of the drive to map.</span></span> <span data-ttu-id="55e9c-108">*LetraDeUnidad* debe ser una sola letra mayúscula y dos puntos (:) es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55e9c-108">The *DriveLetter* must be a single, uppercase letter and the colon (:) is required.</span></span>



| <span data-ttu-id="55e9c-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="55e9c-109">Entry</span></span> | <span data-ttu-id="55e9c-110">Value</span><span class="sxs-lookup"><span data-stu-id="55e9c-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="55e9c-111">CN</span><span class="sxs-lookup"><span data-stu-id="55e9c-111">CN</span></span>                | <span data-ttu-id="55e9c-112">Home-Drive</span><span class="sxs-lookup"><span data-stu-id="55e9c-112">Home-Drive</span></span>                                                                        |
| <span data-ttu-id="55e9c-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="55e9c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="55e9c-114">homeDrive</span><span class="sxs-lookup"><span data-stu-id="55e9c-114">homeDrive</span></span>                                                                         |
| <span data-ttu-id="55e9c-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="55e9c-115">Size</span></span>              | <span data-ttu-id="55e9c-116">2 bytes</span><span class="sxs-lookup"><span data-stu-id="55e9c-116">2 bytes</span></span>                                                                           |
| <span data-ttu-id="55e9c-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="55e9c-117">Update Privilege</span></span>  | <span data-ttu-id="55e9c-118">El administrador de dominio establece este valor.</span><span class="sxs-lookup"><span data-stu-id="55e9c-118">The domain administrator sets this value.</span></span>                                         |
| <span data-ttu-id="55e9c-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="55e9c-119">Update Frequency</span></span>  | <span data-ttu-id="55e9c-120">Cuando se crea el registro de un usuario y cada vez que es necesario cambiar la unidad principal.</span><span class="sxs-lookup"><span data-stu-id="55e9c-120">When the record of a user is created and whenever the home drive needs to change.</span></span> |
| <span data-ttu-id="55e9c-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="55e9c-121">Attribute-Id</span></span>      | <span data-ttu-id="55e9c-122">1.2.840.113556.1.4.45</span><span class="sxs-lookup"><span data-stu-id="55e9c-122">1.2.840.113556.1.4.45</span></span>                                                             |
| <span data-ttu-id="55e9c-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="55e9c-123">System-Id-Guid</span></span>    | <span data-ttu-id="55e9c-124">bf967986-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="55e9c-124">bf967986-0de6-11d0-a285-00aa003049e2</span></span>                                              |
| <span data-ttu-id="55e9c-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55e9c-125">Syntax</span></span>            | [<span data-ttu-id="55e9c-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="55e9c-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="55e9c-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="55e9c-127">Implementations</span></span>

-   [<span data-ttu-id="55e9c-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="55e9c-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="55e9c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="55e9c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="55e9c-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="55e9c-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="55e9c-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="55e9c-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="55e9c-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="55e9c-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="55e9c-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="55e9c-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="55e9c-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55e9c-134">Windows 2000 Server</span></span>



| <span data-ttu-id="55e9c-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="55e9c-135">Entry</span></span> | <span data-ttu-id="55e9c-136">Value</span><span class="sxs-lookup"><span data-stu-id="55e9c-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="55e9c-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="55e9c-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e9c-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e9c-139">System-Only</span></span>            | <span data-ttu-id="55e9c-140">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-140">False</span></span>                             |
| <span data-ttu-id="55e9c-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="55e9c-141">Is-Single-Valued</span></span>       | <span data-ttu-id="55e9c-142">True</span><span class="sxs-lookup"><span data-stu-id="55e9c-142">True</span></span>                              |
| <span data-ttu-id="55e9c-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="55e9c-143">Is Indexed</span></span>             | <span data-ttu-id="55e9c-144">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-144">False</span></span>                             |
| <span data-ttu-id="55e9c-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="55e9c-145">In Global Catalog</span></span>      | <span data-ttu-id="55e9c-146">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-146">False</span></span>                             |
| <span data-ttu-id="55e9c-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="55e9c-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e9c-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="55e9c-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="55e9c-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e9c-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="55e9c-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e9c-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="55e9c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-151">Search-Flags</span></span>           | <span data-ttu-id="55e9c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-152">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-153">System-Flags</span></span>           | <span data-ttu-id="55e9c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-154">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="55e9c-155">Classes used in</span></span>        | [<span data-ttu-id="55e9c-156">**User**</span><span class="sxs-lookup"><span data-stu-id="55e9c-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="55e9c-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55e9c-157">Windows Server 2003</span></span>



| <span data-ttu-id="55e9c-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="55e9c-158">Entry</span></span> | <span data-ttu-id="55e9c-159">Value</span><span class="sxs-lookup"><span data-stu-id="55e9c-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="55e9c-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="55e9c-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e9c-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e9c-162">System-Only</span></span>            | <span data-ttu-id="55e9c-163">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-163">False</span></span>                             |
| <span data-ttu-id="55e9c-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="55e9c-164">Is-Single-Valued</span></span>       | <span data-ttu-id="55e9c-165">True</span><span class="sxs-lookup"><span data-stu-id="55e9c-165">True</span></span>                              |
| <span data-ttu-id="55e9c-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="55e9c-166">Is Indexed</span></span>             | <span data-ttu-id="55e9c-167">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-167">False</span></span>                             |
| <span data-ttu-id="55e9c-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="55e9c-168">In Global Catalog</span></span>      | <span data-ttu-id="55e9c-169">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-169">False</span></span>                             |
| <span data-ttu-id="55e9c-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="55e9c-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e9c-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="55e9c-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="55e9c-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e9c-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="55e9c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e9c-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="55e9c-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-174">Search-Flags</span></span>           | <span data-ttu-id="55e9c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-175">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-176">System-Flags</span></span>           | <span data-ttu-id="55e9c-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-177">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="55e9c-178">Classes used in</span></span>        | [<span data-ttu-id="55e9c-179">**User**</span><span class="sxs-lookup"><span data-stu-id="55e9c-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="55e9c-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="55e9c-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="55e9c-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="55e9c-181">Entry</span></span> | <span data-ttu-id="55e9c-182">Value</span><span class="sxs-lookup"><span data-stu-id="55e9c-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="55e9c-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="55e9c-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e9c-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e9c-185">System-Only</span></span>            | <span data-ttu-id="55e9c-186">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-186">False</span></span>                             |
| <span data-ttu-id="55e9c-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="55e9c-187">Is-Single-Valued</span></span>       | <span data-ttu-id="55e9c-188">True</span><span class="sxs-lookup"><span data-stu-id="55e9c-188">True</span></span>                              |
| <span data-ttu-id="55e9c-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="55e9c-189">Is Indexed</span></span>             | <span data-ttu-id="55e9c-190">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-190">False</span></span>                             |
| <span data-ttu-id="55e9c-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="55e9c-191">In Global Catalog</span></span>      | <span data-ttu-id="55e9c-192">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-192">False</span></span>                             |
| <span data-ttu-id="55e9c-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="55e9c-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e9c-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="55e9c-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="55e9c-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e9c-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="55e9c-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e9c-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="55e9c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-197">Search-Flags</span></span>           | <span data-ttu-id="55e9c-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-198">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-199">System-Flags</span></span>           | <span data-ttu-id="55e9c-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-200">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="55e9c-201">Classes used in</span></span>        | [<span data-ttu-id="55e9c-202">**User**</span><span class="sxs-lookup"><span data-stu-id="55e9c-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="55e9c-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55e9c-203">Windows Server 2008</span></span>



| <span data-ttu-id="55e9c-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="55e9c-204">Entry</span></span> | <span data-ttu-id="55e9c-205">Value</span><span class="sxs-lookup"><span data-stu-id="55e9c-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="55e9c-206">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="55e9c-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e9c-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e9c-208">System-Only</span></span>            | <span data-ttu-id="55e9c-209">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-209">False</span></span>                             |
| <span data-ttu-id="55e9c-210">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="55e9c-210">Is-Single-Valued</span></span>       | <span data-ttu-id="55e9c-211">True</span><span class="sxs-lookup"><span data-stu-id="55e9c-211">True</span></span>                              |
| <span data-ttu-id="55e9c-212">Está indexado</span><span class="sxs-lookup"><span data-stu-id="55e9c-212">Is Indexed</span></span>             | <span data-ttu-id="55e9c-213">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-213">False</span></span>                             |
| <span data-ttu-id="55e9c-214">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="55e9c-214">In Global Catalog</span></span>      | <span data-ttu-id="55e9c-215">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-215">False</span></span>                             |
| <span data-ttu-id="55e9c-216">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="55e9c-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e9c-217">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="55e9c-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="55e9c-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e9c-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="55e9c-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e9c-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="55e9c-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-220">Search-Flags</span></span>           | <span data-ttu-id="55e9c-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-221">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-222">System-Flags</span></span>           | <span data-ttu-id="55e9c-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-223">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-224">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="55e9c-224">Classes used in</span></span>        | [<span data-ttu-id="55e9c-225">**User**</span><span class="sxs-lookup"><span data-stu-id="55e9c-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="55e9c-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="55e9c-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="55e9c-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="55e9c-227">Entry</span></span> | <span data-ttu-id="55e9c-228">Value</span><span class="sxs-lookup"><span data-stu-id="55e9c-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="55e9c-229">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="55e9c-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e9c-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e9c-231">System-Only</span></span>            | <span data-ttu-id="55e9c-232">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-232">False</span></span>                             |
| <span data-ttu-id="55e9c-233">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="55e9c-233">Is-Single-Valued</span></span>       | <span data-ttu-id="55e9c-234">True</span><span class="sxs-lookup"><span data-stu-id="55e9c-234">True</span></span>                              |
| <span data-ttu-id="55e9c-235">Está indexado</span><span class="sxs-lookup"><span data-stu-id="55e9c-235">Is Indexed</span></span>             | <span data-ttu-id="55e9c-236">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-236">False</span></span>                             |
| <span data-ttu-id="55e9c-237">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="55e9c-237">In Global Catalog</span></span>      | <span data-ttu-id="55e9c-238">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-238">False</span></span>                             |
| <span data-ttu-id="55e9c-239">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="55e9c-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e9c-240">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="55e9c-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="55e9c-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e9c-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="55e9c-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e9c-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="55e9c-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-243">Search-Flags</span></span>           | <span data-ttu-id="55e9c-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-244">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-245">System-Flags</span></span>           | <span data-ttu-id="55e9c-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-246">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-247">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="55e9c-247">Classes used in</span></span>        | [<span data-ttu-id="55e9c-248">**User**</span><span class="sxs-lookup"><span data-stu-id="55e9c-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="55e9c-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55e9c-249">Windows Server 2012</span></span>



| <span data-ttu-id="55e9c-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="55e9c-250">Entry</span></span> | <span data-ttu-id="55e9c-251">Value</span><span class="sxs-lookup"><span data-stu-id="55e9c-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="55e9c-252">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="55e9c-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="55e9c-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="55e9c-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="55e9c-254">System-Only</span></span>            | <span data-ttu-id="55e9c-255">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-255">False</span></span>                             |
| <span data-ttu-id="55e9c-256">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="55e9c-256">Is-Single-Valued</span></span>       | <span data-ttu-id="55e9c-257">True</span><span class="sxs-lookup"><span data-stu-id="55e9c-257">True</span></span>                              |
| <span data-ttu-id="55e9c-258">Está indexado</span><span class="sxs-lookup"><span data-stu-id="55e9c-258">Is Indexed</span></span>             | <span data-ttu-id="55e9c-259">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-259">False</span></span>                             |
| <span data-ttu-id="55e9c-260">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="55e9c-260">In Global Catalog</span></span>      | <span data-ttu-id="55e9c-261">False</span><span class="sxs-lookup"><span data-stu-id="55e9c-261">False</span></span>                             |
| <span data-ttu-id="55e9c-262">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="55e9c-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="55e9c-263">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="55e9c-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="55e9c-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="55e9c-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="55e9c-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="55e9c-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="55e9c-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-266">Search-Flags</span></span>           | <span data-ttu-id="55e9c-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-267">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="55e9c-268">System-Flags</span></span>           | <span data-ttu-id="55e9c-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="55e9c-269">0x00000010</span></span>                        |
| <span data-ttu-id="55e9c-270">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="55e9c-270">Classes used in</span></span>        | [<span data-ttu-id="55e9c-271">**User**</span><span class="sxs-lookup"><span data-stu-id="55e9c-271">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="55e9c-272">Vea también</span><span class="sxs-lookup"><span data-stu-id="55e9c-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e9c-273">**homeDirectory**</span><span class="sxs-lookup"><span data-stu-id="55e9c-273">**homeDirectory**</span></span>](a-homedirectory.md)
</dt> </dl>

 

 






---
title: Home-Directory atributo)
description: Directorio particular de la cuenta.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Home-Directory
- homeDirectory esquema de AD de atributos
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804789"
---
# <a name="home-directory-attribute"></a><span data-ttu-id="aaef8-105">Home-Directory atributo)</span><span class="sxs-lookup"><span data-stu-id="aaef8-105">Home-Directory attribute</span></span>

<span data-ttu-id="aaef8-106">Directorio particular de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="aaef8-106">The home directory for the account.</span></span> <span data-ttu-id="aaef8-107">Si [**HOMEDRIVE**](a-homedrive.md) se establece y especifica una letra de unidad, **HomeDirectory** debe ser una ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="aaef8-107">If [**homeDrive**](a-homedrive.md) is set and specifies a drive letter, **homeDirectory** must be a UNC path.</span></span> <span data-ttu-id="aaef8-108">De lo contrario, **HomeDirectory** es una ruta de acceso local completa que incluye la letra de unidad (por ejemplo, \*letraDeUnidad ***: \\** carpeta del _directorio_* _\\_ \* ).</span><span class="sxs-lookup"><span data-stu-id="aaef8-108">Otherwise, **homeDirectory** is a fully qualified local path including the drive letter (for example, *DriveLetter\***:\\**_Directory_*_\\_\*_Folder_).</span></span> <span data-ttu-id="aaef8-109">Este valor puede ser una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="aaef8-109">This value can be a null string.</span></span>



| <span data-ttu-id="aaef8-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="aaef8-110">Entry</span></span> | <span data-ttu-id="aaef8-111">Value</span><span class="sxs-lookup"><span data-stu-id="aaef8-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aaef8-112">CN</span><span class="sxs-lookup"><span data-stu-id="aaef8-112">CN</span></span>                | <span data-ttu-id="aaef8-113">Home-Directory</span><span class="sxs-lookup"><span data-stu-id="aaef8-113">Home-Directory</span></span>                                                                     |
| <span data-ttu-id="aaef8-114">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="aaef8-114">Ldap-Display-Name</span></span> | <span data-ttu-id="aaef8-115">homeDirectory</span><span class="sxs-lookup"><span data-stu-id="aaef8-115">homeDirectory</span></span>                                                                      |
| <span data-ttu-id="aaef8-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="aaef8-116">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="aaef8-117">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="aaef8-117">Update Privilege</span></span>  | <span data-ttu-id="aaef8-118">Administrador de dominio</span><span class="sxs-lookup"><span data-stu-id="aaef8-118">Domain administrator</span></span>                                                               |
| <span data-ttu-id="aaef8-119">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="aaef8-119">Update Frequency</span></span>  | <span data-ttu-id="aaef8-120">Cuando se crea el registro del usuario y cada vez que es necesario cambiar el directorio particular.</span><span class="sxs-lookup"><span data-stu-id="aaef8-120">When the user's record is created and whenever the home directory needs to change.</span></span> |
| <span data-ttu-id="aaef8-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aaef8-121">Attribute-Id</span></span>      | <span data-ttu-id="aaef8-122">1.2.840.113556.1.4.44</span><span class="sxs-lookup"><span data-stu-id="aaef8-122">1.2.840.113556.1.4.44</span></span>                                                              |
| <span data-ttu-id="aaef8-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aaef8-123">System-Id-Guid</span></span>    | <span data-ttu-id="aaef8-124">bf967985-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="aaef8-124">bf967985-0de6-11d0-a285-00aa003049e2</span></span>                                               |
| <span data-ttu-id="aaef8-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aaef8-125">Syntax</span></span>            | [<span data-ttu-id="aaef8-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="aaef8-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                        |



## <a name="implementations"></a><span data-ttu-id="aaef8-127">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="aaef8-127">Implementations</span></span>

-   [<span data-ttu-id="aaef8-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aaef8-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aaef8-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aaef8-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aaef8-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aaef8-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aaef8-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aaef8-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aaef8-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aaef8-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aaef8-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aaef8-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aaef8-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aaef8-134">Windows 2000 Server</span></span>



| <span data-ttu-id="aaef8-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="aaef8-135">Entry</span></span> | <span data-ttu-id="aaef8-136">Value</span><span class="sxs-lookup"><span data-stu-id="aaef8-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="aaef8-137">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aaef8-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="aaef8-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaef8-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="aaef8-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaef8-139">System-Only</span></span>            | <span data-ttu-id="aaef8-140">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-140">False</span></span>                             |
| <span data-ttu-id="aaef8-141">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aaef8-141">Is-Single-Valued</span></span>       | <span data-ttu-id="aaef8-142">True</span><span class="sxs-lookup"><span data-stu-id="aaef8-142">True</span></span>                              |
| <span data-ttu-id="aaef8-143">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aaef8-143">Is Indexed</span></span>             | <span data-ttu-id="aaef8-144">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-144">False</span></span>                             |
| <span data-ttu-id="aaef8-145">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aaef8-145">In Global Catalog</span></span>      | <span data-ttu-id="aaef8-146">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-146">False</span></span>                             |
| <span data-ttu-id="aaef8-147">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aaef8-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaef8-148">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aaef8-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="aaef8-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaef8-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="aaef8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaef8-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="aaef8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-151">Search-Flags</span></span>           | <span data-ttu-id="aaef8-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-152">0x00000010</span></span>                        |
| <span data-ttu-id="aaef8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-153">System-Flags</span></span>           | <span data-ttu-id="aaef8-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-154">0x00000010</span></span>                        |
| <span data-ttu-id="aaef8-155">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aaef8-155">Classes used in</span></span>        | [<span data-ttu-id="aaef8-156">**User**</span><span class="sxs-lookup"><span data-stu-id="aaef8-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aaef8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aaef8-157">Windows Server 2003</span></span>



| <span data-ttu-id="aaef8-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="aaef8-158">Entry</span></span> | <span data-ttu-id="aaef8-159">Value</span><span class="sxs-lookup"><span data-stu-id="aaef8-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="aaef8-160">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aaef8-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="aaef8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaef8-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="aaef8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaef8-162">System-Only</span></span>            | <span data-ttu-id="aaef8-163">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-163">False</span></span>                             |
| <span data-ttu-id="aaef8-164">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aaef8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="aaef8-165">True</span><span class="sxs-lookup"><span data-stu-id="aaef8-165">True</span></span>                              |
| <span data-ttu-id="aaef8-166">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aaef8-166">Is Indexed</span></span>             | <span data-ttu-id="aaef8-167">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-167">False</span></span>                             |
| <span data-ttu-id="aaef8-168">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aaef8-168">In Global Catalog</span></span>      | <span data-ttu-id="aaef8-169">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-169">False</span></span>                             |
| <span data-ttu-id="aaef8-170">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aaef8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaef8-171">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aaef8-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="aaef8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaef8-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="aaef8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaef8-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="aaef8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-174">Search-Flags</span></span>           | <span data-ttu-id="aaef8-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-175">0x00000010</span></span>                        |
| <span data-ttu-id="aaef8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-176">System-Flags</span></span>           | <span data-ttu-id="aaef8-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-177">0x00000010</span></span>                        |
| <span data-ttu-id="aaef8-178">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aaef8-178">Classes used in</span></span>        | [<span data-ttu-id="aaef8-179">**User**</span><span class="sxs-lookup"><span data-stu-id="aaef8-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aaef8-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aaef8-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aaef8-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="aaef8-181">Entry</span></span> | <span data-ttu-id="aaef8-182">Value</span><span class="sxs-lookup"><span data-stu-id="aaef8-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aaef8-183">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aaef8-183">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="aaef8-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaef8-184">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="aaef8-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaef8-185">System-Only</span></span>            | <span data-ttu-id="aaef8-186">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-186">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-187">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aaef8-187">Is-Single-Valued</span></span>       | <span data-ttu-id="aaef8-188">True</span><span class="sxs-lookup"><span data-stu-id="aaef8-188">True</span></span>                                                                                |
| <span data-ttu-id="aaef8-189">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aaef8-189">Is Indexed</span></span>             | <span data-ttu-id="aaef8-190">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-190">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-191">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aaef8-191">In Global Catalog</span></span>      | <span data-ttu-id="aaef8-192">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-192">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-193">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aaef8-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaef8-194">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aaef8-194">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="aaef8-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaef8-195">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="aaef8-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaef8-196">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="aaef8-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-197">Search-Flags</span></span>           | <span data-ttu-id="aaef8-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-198">0x00000010</span></span>                                                                          |
| <span data-ttu-id="aaef8-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-199">System-Flags</span></span>           | <span data-ttu-id="aaef8-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-200">0x00000010</span></span>                                                                          |
| <span data-ttu-id="aaef8-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aaef8-201">Classes used in</span></span>        | [<span data-ttu-id="aaef8-202">**User**</span><span class="sxs-lookup"><span data-stu-id="aaef8-202">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="aaef8-203">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="aaef8-203">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aaef8-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaef8-204">Windows Server 2008</span></span>



| <span data-ttu-id="aaef8-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="aaef8-205">Entry</span></span> | <span data-ttu-id="aaef8-206">Value</span><span class="sxs-lookup"><span data-stu-id="aaef8-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aaef8-207">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aaef8-207">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="aaef8-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaef8-208">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="aaef8-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaef8-209">System-Only</span></span>            | <span data-ttu-id="aaef8-210">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-210">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-211">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aaef8-211">Is-Single-Valued</span></span>       | <span data-ttu-id="aaef8-212">True</span><span class="sxs-lookup"><span data-stu-id="aaef8-212">True</span></span>                                                                                |
| <span data-ttu-id="aaef8-213">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aaef8-213">Is Indexed</span></span>             | <span data-ttu-id="aaef8-214">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-214">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-215">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aaef8-215">In Global Catalog</span></span>      | <span data-ttu-id="aaef8-216">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-216">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-217">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aaef8-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaef8-218">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aaef8-218">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="aaef8-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaef8-219">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="aaef8-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaef8-220">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="aaef8-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-221">Search-Flags</span></span>           | <span data-ttu-id="aaef8-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-222">0x00000010</span></span>                                                                          |
| <span data-ttu-id="aaef8-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-223">System-Flags</span></span>           | <span data-ttu-id="aaef8-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-224">0x00000010</span></span>                                                                          |
| <span data-ttu-id="aaef8-225">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aaef8-225">Classes used in</span></span>        | [<span data-ttu-id="aaef8-226">**User**</span><span class="sxs-lookup"><span data-stu-id="aaef8-226">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="aaef8-227">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="aaef8-227">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aaef8-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aaef8-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aaef8-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="aaef8-229">Entry</span></span> | <span data-ttu-id="aaef8-230">Value</span><span class="sxs-lookup"><span data-stu-id="aaef8-230">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aaef8-231">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aaef8-231">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="aaef8-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaef8-232">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="aaef8-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaef8-233">System-Only</span></span>            | <span data-ttu-id="aaef8-234">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-234">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-235">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aaef8-235">Is-Single-Valued</span></span>       | <span data-ttu-id="aaef8-236">True</span><span class="sxs-lookup"><span data-stu-id="aaef8-236">True</span></span>                                                                                |
| <span data-ttu-id="aaef8-237">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aaef8-237">Is Indexed</span></span>             | <span data-ttu-id="aaef8-238">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-238">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-239">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aaef8-239">In Global Catalog</span></span>      | <span data-ttu-id="aaef8-240">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-240">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-241">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aaef8-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaef8-242">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aaef8-242">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="aaef8-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaef8-243">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="aaef8-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaef8-244">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="aaef8-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-245">Search-Flags</span></span>           | <span data-ttu-id="aaef8-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-246">0x00000010</span></span>                                                                          |
| <span data-ttu-id="aaef8-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-247">System-Flags</span></span>           | <span data-ttu-id="aaef8-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-248">0x00000010</span></span>                                                                          |
| <span data-ttu-id="aaef8-249">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aaef8-249">Classes used in</span></span>        | [<span data-ttu-id="aaef8-250">**User**</span><span class="sxs-lookup"><span data-stu-id="aaef8-250">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="aaef8-251">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="aaef8-251">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aaef8-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aaef8-252">Windows Server 2012</span></span>



| <span data-ttu-id="aaef8-253">Entrada</span><span class="sxs-lookup"><span data-stu-id="aaef8-253">Entry</span></span> | <span data-ttu-id="aaef8-254">Value</span><span class="sxs-lookup"><span data-stu-id="aaef8-254">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aaef8-255">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="aaef8-255">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="aaef8-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aaef8-256">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="aaef8-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="aaef8-257">System-Only</span></span>            | <span data-ttu-id="aaef8-258">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-258">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-259">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="aaef8-259">Is-Single-Valued</span></span>       | <span data-ttu-id="aaef8-260">True</span><span class="sxs-lookup"><span data-stu-id="aaef8-260">True</span></span>                                                                                |
| <span data-ttu-id="aaef8-261">Está indexado</span><span class="sxs-lookup"><span data-stu-id="aaef8-261">Is Indexed</span></span>             | <span data-ttu-id="aaef8-262">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-262">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-263">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="aaef8-263">In Global Catalog</span></span>      | <span data-ttu-id="aaef8-264">False</span><span class="sxs-lookup"><span data-stu-id="aaef8-264">False</span></span>                                                                               |
| <span data-ttu-id="aaef8-265">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="aaef8-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="aaef8-266">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="aaef8-266">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="aaef8-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aaef8-267">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="aaef8-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aaef8-268">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="aaef8-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-269">Search-Flags</span></span>           | <span data-ttu-id="aaef8-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-270">0x00000010</span></span>                                                                          |
| <span data-ttu-id="aaef8-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aaef8-271">System-Flags</span></span>           | <span data-ttu-id="aaef8-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aaef8-272">0x00000010</span></span>                                                                          |
| <span data-ttu-id="aaef8-273">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="aaef8-273">Classes used in</span></span>        | [<span data-ttu-id="aaef8-274">**User**</span><span class="sxs-lookup"><span data-stu-id="aaef8-274">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="aaef8-275">**posixAccount**</span><span class="sxs-lookup"><span data-stu-id="aaef8-275">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="aaef8-276">Vea también</span><span class="sxs-lookup"><span data-stu-id="aaef8-276">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaef8-277">**homeDrive**</span><span class="sxs-lookup"><span data-stu-id="aaef8-277">**homeDrive**</span></span>](a-homedrive.md)
</dt> </dl>

 

 






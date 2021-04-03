---
title: atributo MS-TS-Profile-path
description: Terminal Services ruta de acceso de perfil especifica una ruta de acceso de perfil móvil o obligatoria para usar cuando el usuario inicia sesión en el servidor de Terminal Server. La ruta de acceso del perfil está en el siguiente formato de ruta de acceso de red \\ \\ ServerName \\ ProfilesFolderName \\ username.
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-TS-Profile-path
- msTSProfilePath esquema de AD de atributos
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67243c2ef588bd1470a50417c0948b1ea4ea7fa9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997398"
---
# <a name="ms-ts-profile-path-attribute"></a><span data-ttu-id="30483-106">atributo MS-TS-Profile-path</span><span class="sxs-lookup"><span data-stu-id="30483-106">ms-TS-Profile-Path attribute</span></span>

<span data-ttu-id="30483-107">Terminal Services ruta de acceso de perfil especifica una ruta de acceso de perfil móvil o obligatoria para usar cuando el usuario inicia sesión en el servidor de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="30483-107">Terminal Services Profile Path specifies a roaming or mandatory profile path to use when the user logs on to the terminal server.</span></span> <span data-ttu-id="30483-108">La ruta de acceso del perfil está en el siguiente formato de ruta de acceso de red: **\\\\** _ServerName_ *_\\_* _ProfilesFolderName_ *_\\_* _username_.</span><span class="sxs-lookup"><span data-stu-id="30483-108">The profile path is in the following network path format: **\\\\**_ServerName_*_\\_*_ProfilesFolderName_*_\\_*_UserName_.</span></span>



| <span data-ttu-id="30483-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="30483-109">Entry</span></span> | <span data-ttu-id="30483-110">Value</span><span class="sxs-lookup"><span data-stu-id="30483-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="30483-111">CN</span><span class="sxs-lookup"><span data-stu-id="30483-111">CN</span></span>                | <span data-ttu-id="30483-112">Ruta de acceso de MS-TS-Profile</span><span class="sxs-lookup"><span data-stu-id="30483-112">ms-TS-Profile-Path</span></span>                          |
| <span data-ttu-id="30483-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="30483-113">Ldap-Display-Name</span></span> | <span data-ttu-id="30483-114">msTSProfilePath</span><span class="sxs-lookup"><span data-stu-id="30483-114">msTSProfilePath</span></span>                             |
| <span data-ttu-id="30483-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="30483-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="30483-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="30483-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="30483-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="30483-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="30483-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="30483-118">Attribute-Id</span></span>      | <span data-ttu-id="30483-119">1.2.840.113556.1.4.1976</span><span class="sxs-lookup"><span data-stu-id="30483-119">1.2.840.113556.1.4.1976</span></span>                     |
| <span data-ttu-id="30483-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="30483-120">System-Id-Guid</span></span>    | <span data-ttu-id="30483-121">e65c30db-316c-4060-a3a0-387b083f09cd</span><span class="sxs-lookup"><span data-stu-id="30483-121">e65c30db-316c-4060-a3a0-387b083f09cd</span></span>        |
| <span data-ttu-id="30483-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30483-122">Syntax</span></span>            | [<span data-ttu-id="30483-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="30483-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="30483-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="30483-124">Implementations</span></span>

-   [<span data-ttu-id="30483-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="30483-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="30483-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="30483-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="30483-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="30483-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="30483-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30483-128">Windows Server 2008</span></span>



| <span data-ttu-id="30483-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="30483-129">Entry</span></span> | <span data-ttu-id="30483-130">Value</span><span class="sxs-lookup"><span data-stu-id="30483-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30483-131">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30483-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30483-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30483-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30483-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="30483-133">System-Only</span></span>            | <span data-ttu-id="30483-134">False</span><span class="sxs-lookup"><span data-stu-id="30483-134">False</span></span>                             |
| <span data-ttu-id="30483-135">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30483-135">Is-Single-Valued</span></span>       | <span data-ttu-id="30483-136">True</span><span class="sxs-lookup"><span data-stu-id="30483-136">True</span></span>                              |
| <span data-ttu-id="30483-137">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30483-137">Is Indexed</span></span>             | <span data-ttu-id="30483-138">False</span><span class="sxs-lookup"><span data-stu-id="30483-138">False</span></span>                             |
| <span data-ttu-id="30483-139">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30483-139">In Global Catalog</span></span>      | <span data-ttu-id="30483-140">False</span><span class="sxs-lookup"><span data-stu-id="30483-140">False</span></span>                             |
| <span data-ttu-id="30483-141">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30483-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="30483-142">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30483-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30483-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30483-143">Range-Lower</span></span>            | <span data-ttu-id="30483-144">0</span><span class="sxs-lookup"><span data-stu-id="30483-144">0</span></span>                                 |
| <span data-ttu-id="30483-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30483-145">Range-Upper</span></span>            | <span data-ttu-id="30483-146">32767</span><span class="sxs-lookup"><span data-stu-id="30483-146">32767</span></span>                             |
| <span data-ttu-id="30483-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30483-147">Search-Flags</span></span>           | <span data-ttu-id="30483-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30483-148">0x00000000</span></span>                        |
| <span data-ttu-id="30483-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30483-149">System-Flags</span></span>           | <span data-ttu-id="30483-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30483-150">0x00000010</span></span>                        |
| <span data-ttu-id="30483-151">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30483-151">Classes used in</span></span>        | [<span data-ttu-id="30483-152">**User**</span><span class="sxs-lookup"><span data-stu-id="30483-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="30483-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30483-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="30483-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="30483-154">Entry</span></span> | <span data-ttu-id="30483-155">Value</span><span class="sxs-lookup"><span data-stu-id="30483-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30483-156">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30483-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30483-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30483-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30483-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="30483-158">System-Only</span></span>            | <span data-ttu-id="30483-159">False</span><span class="sxs-lookup"><span data-stu-id="30483-159">False</span></span>                             |
| <span data-ttu-id="30483-160">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30483-160">Is-Single-Valued</span></span>       | <span data-ttu-id="30483-161">True</span><span class="sxs-lookup"><span data-stu-id="30483-161">True</span></span>                              |
| <span data-ttu-id="30483-162">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30483-162">Is Indexed</span></span>             | <span data-ttu-id="30483-163">False</span><span class="sxs-lookup"><span data-stu-id="30483-163">False</span></span>                             |
| <span data-ttu-id="30483-164">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30483-164">In Global Catalog</span></span>      | <span data-ttu-id="30483-165">False</span><span class="sxs-lookup"><span data-stu-id="30483-165">False</span></span>                             |
| <span data-ttu-id="30483-166">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30483-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="30483-167">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30483-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30483-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30483-168">Range-Lower</span></span>            | <span data-ttu-id="30483-169">0</span><span class="sxs-lookup"><span data-stu-id="30483-169">0</span></span>                                 |
| <span data-ttu-id="30483-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30483-170">Range-Upper</span></span>            | <span data-ttu-id="30483-171">32767</span><span class="sxs-lookup"><span data-stu-id="30483-171">32767</span></span>                             |
| <span data-ttu-id="30483-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30483-172">Search-Flags</span></span>           | <span data-ttu-id="30483-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30483-173">0x00000000</span></span>                        |
| <span data-ttu-id="30483-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30483-174">System-Flags</span></span>           | <span data-ttu-id="30483-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30483-175">0x00000010</span></span>                        |
| <span data-ttu-id="30483-176">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30483-176">Classes used in</span></span>        | [<span data-ttu-id="30483-177">**User**</span><span class="sxs-lookup"><span data-stu-id="30483-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="30483-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30483-178">Windows Server 2012</span></span>



| <span data-ttu-id="30483-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="30483-179">Entry</span></span> | <span data-ttu-id="30483-180">Value</span><span class="sxs-lookup"><span data-stu-id="30483-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="30483-181">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="30483-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="30483-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="30483-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="30483-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="30483-183">System-Only</span></span>            | <span data-ttu-id="30483-184">False</span><span class="sxs-lookup"><span data-stu-id="30483-184">False</span></span>                             |
| <span data-ttu-id="30483-185">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="30483-185">Is-Single-Valued</span></span>       | <span data-ttu-id="30483-186">True</span><span class="sxs-lookup"><span data-stu-id="30483-186">True</span></span>                              |
| <span data-ttu-id="30483-187">Está indexado</span><span class="sxs-lookup"><span data-stu-id="30483-187">Is Indexed</span></span>             | <span data-ttu-id="30483-188">False</span><span class="sxs-lookup"><span data-stu-id="30483-188">False</span></span>                             |
| <span data-ttu-id="30483-189">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="30483-189">In Global Catalog</span></span>      | <span data-ttu-id="30483-190">False</span><span class="sxs-lookup"><span data-stu-id="30483-190">False</span></span>                             |
| <span data-ttu-id="30483-191">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="30483-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="30483-192">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="30483-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="30483-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="30483-193">Range-Lower</span></span>            | <span data-ttu-id="30483-194">0</span><span class="sxs-lookup"><span data-stu-id="30483-194">0</span></span>                                 |
| <span data-ttu-id="30483-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="30483-195">Range-Upper</span></span>            | <span data-ttu-id="30483-196">32767</span><span class="sxs-lookup"><span data-stu-id="30483-196">32767</span></span>                             |
| <span data-ttu-id="30483-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="30483-197">Search-Flags</span></span>           | <span data-ttu-id="30483-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30483-198">0x00000000</span></span>                        |
| <span data-ttu-id="30483-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="30483-199">System-Flags</span></span>           | <span data-ttu-id="30483-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="30483-200">0x00000010</span></span>                        |
| <span data-ttu-id="30483-201">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="30483-201">Classes used in</span></span>        | [<span data-ttu-id="30483-202">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="30483-202">**User**</span></span>](c-user.md)<br/> |



 

 






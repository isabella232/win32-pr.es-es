---
title: atributo MS-TS-allow-Logon
description: Especifica si el usuario puede iniciar sesión en el Terminal Server. El valor es 1 si se permite el inicio de sesión y 0 si no se permite el inicio de sesión.
ms.assetid: 9cd6edbc-f8e7-4933-9f62-1e34e3d31fb7
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-TS-allow-Logon
- msTSAllowLogon esquema de AD de atributos
topic_type:
- apiref
api_name:
- ms-TS-Allow-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd78662167e281ea720f2ad5d98f25c2f5c4ae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905977"
---
# <a name="ms-ts-allow-logon-attribute"></a><span data-ttu-id="d08b0-106">atributo MS-TS-allow-Logon</span><span class="sxs-lookup"><span data-stu-id="d08b0-106">ms-TS-Allow-Logon attribute</span></span>

<span data-ttu-id="d08b0-107">Especifica si el usuario puede iniciar sesión en el Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="d08b0-107">Specifies whether the user is allowed to log on to the Terminal Server.</span></span> <span data-ttu-id="d08b0-108">El valor es 1 si se permite el inicio de sesión y 0 si no se permite el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d08b0-108">The value is 1 if logon is allowed, and 0 if logon is not allowed.</span></span>



| <span data-ttu-id="d08b0-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08b0-109">Entry</span></span> | <span data-ttu-id="d08b0-110">Value</span><span class="sxs-lookup"><span data-stu-id="d08b0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d08b0-111">CN</span><span class="sxs-lookup"><span data-stu-id="d08b0-111">CN</span></span>                | <span data-ttu-id="d08b0-112">MS-TS-allow-Logon</span><span class="sxs-lookup"><span data-stu-id="d08b0-112">ms-TS-Allow-Logon</span></span>                    |
| <span data-ttu-id="d08b0-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="d08b0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d08b0-114">msTSAllowLogon</span><span class="sxs-lookup"><span data-stu-id="d08b0-114">msTSAllowLogon</span></span>                       |
| <span data-ttu-id="d08b0-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d08b0-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="d08b0-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="d08b0-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d08b0-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="d08b0-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d08b0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d08b0-118">Attribute-Id</span></span>      | <span data-ttu-id="d08b0-119">1.2.840.113556.1.4.1979</span><span class="sxs-lookup"><span data-stu-id="d08b0-119">1.2.840.113556.1.4.1979</span></span>              |
| <span data-ttu-id="d08b0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d08b0-120">System-Id-Guid</span></span>    | <span data-ttu-id="d08b0-121">3a0cd464-bc54-40e7-93ae-a646a6ecc4b4</span><span class="sxs-lookup"><span data-stu-id="d08b0-121">3a0cd464-bc54-40e7-93ae-a646a6ecc4b4</span></span> |
| <span data-ttu-id="d08b0-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d08b0-122">Syntax</span></span>            | [<span data-ttu-id="d08b0-123">**Booleano**</span><span class="sxs-lookup"><span data-stu-id="d08b0-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="d08b0-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="d08b0-124">Implementations</span></span>

-   [<span data-ttu-id="d08b0-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d08b0-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d08b0-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d08b0-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d08b0-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d08b0-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="d08b0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d08b0-128">Windows Server 2008</span></span>



| <span data-ttu-id="d08b0-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08b0-129">Entry</span></span> | <span data-ttu-id="d08b0-130">Value</span><span class="sxs-lookup"><span data-stu-id="d08b0-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d08b0-131">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d08b0-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d08b0-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08b0-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d08b0-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08b0-133">System-Only</span></span>            | <span data-ttu-id="d08b0-134">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-134">False</span></span>                             |
| <span data-ttu-id="d08b0-135">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d08b0-135">Is-Single-Valued</span></span>       | <span data-ttu-id="d08b0-136">True</span><span class="sxs-lookup"><span data-stu-id="d08b0-136">True</span></span>                              |
| <span data-ttu-id="d08b0-137">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d08b0-137">Is Indexed</span></span>             | <span data-ttu-id="d08b0-138">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-138">False</span></span>                             |
| <span data-ttu-id="d08b0-139">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08b0-139">In Global Catalog</span></span>      | <span data-ttu-id="d08b0-140">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-140">False</span></span>                             |
| <span data-ttu-id="d08b0-141">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d08b0-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08b0-142">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d08b0-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d08b0-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08b0-143">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d08b0-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08b0-144">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d08b0-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08b0-145">Search-Flags</span></span>           | <span data-ttu-id="d08b0-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d08b0-146">0x00000000</span></span>                        |
| <span data-ttu-id="d08b0-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08b0-147">System-Flags</span></span>           | <span data-ttu-id="d08b0-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d08b0-148">0x00000010</span></span>                        |
| <span data-ttu-id="d08b0-149">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d08b0-149">Classes used in</span></span>        | [<span data-ttu-id="d08b0-150">**User**</span><span class="sxs-lookup"><span data-stu-id="d08b0-150">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d08b0-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d08b0-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d08b0-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08b0-152">Entry</span></span> | <span data-ttu-id="d08b0-153">Value</span><span class="sxs-lookup"><span data-stu-id="d08b0-153">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d08b0-154">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d08b0-154">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d08b0-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08b0-155">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d08b0-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08b0-156">System-Only</span></span>            | <span data-ttu-id="d08b0-157">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-157">False</span></span>                             |
| <span data-ttu-id="d08b0-158">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d08b0-158">Is-Single-Valued</span></span>       | <span data-ttu-id="d08b0-159">True</span><span class="sxs-lookup"><span data-stu-id="d08b0-159">True</span></span>                              |
| <span data-ttu-id="d08b0-160">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d08b0-160">Is Indexed</span></span>             | <span data-ttu-id="d08b0-161">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-161">False</span></span>                             |
| <span data-ttu-id="d08b0-162">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08b0-162">In Global Catalog</span></span>      | <span data-ttu-id="d08b0-163">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-163">False</span></span>                             |
| <span data-ttu-id="d08b0-164">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d08b0-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08b0-165">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d08b0-165">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d08b0-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08b0-166">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d08b0-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08b0-167">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d08b0-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08b0-168">Search-Flags</span></span>           | <span data-ttu-id="d08b0-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d08b0-169">0x00000000</span></span>                        |
| <span data-ttu-id="d08b0-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08b0-170">System-Flags</span></span>           | <span data-ttu-id="d08b0-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d08b0-171">0x00000010</span></span>                        |
| <span data-ttu-id="d08b0-172">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d08b0-172">Classes used in</span></span>        | [<span data-ttu-id="d08b0-173">**User**</span><span class="sxs-lookup"><span data-stu-id="d08b0-173">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d08b0-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d08b0-174">Windows Server 2012</span></span>



| <span data-ttu-id="d08b0-175">Entrada</span><span class="sxs-lookup"><span data-stu-id="d08b0-175">Entry</span></span> | <span data-ttu-id="d08b0-176">Value</span><span class="sxs-lookup"><span data-stu-id="d08b0-176">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d08b0-177">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="d08b0-177">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="d08b0-178">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d08b0-178">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d08b0-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="d08b0-179">System-Only</span></span>            | <span data-ttu-id="d08b0-180">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-180">False</span></span>                             |
| <span data-ttu-id="d08b0-181">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="d08b0-181">Is-Single-Valued</span></span>       | <span data-ttu-id="d08b0-182">True</span><span class="sxs-lookup"><span data-stu-id="d08b0-182">True</span></span>                              |
| <span data-ttu-id="d08b0-183">Está indexado</span><span class="sxs-lookup"><span data-stu-id="d08b0-183">Is Indexed</span></span>             | <span data-ttu-id="d08b0-184">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-184">False</span></span>                             |
| <span data-ttu-id="d08b0-185">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="d08b0-185">In Global Catalog</span></span>      | <span data-ttu-id="d08b0-186">False</span><span class="sxs-lookup"><span data-stu-id="d08b0-186">False</span></span>                             |
| <span data-ttu-id="d08b0-187">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="d08b0-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="d08b0-188">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d08b0-188">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d08b0-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d08b0-189">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d08b0-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d08b0-190">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d08b0-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d08b0-191">Search-Flags</span></span>           | <span data-ttu-id="d08b0-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d08b0-192">0x00000000</span></span>                        |
| <span data-ttu-id="d08b0-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d08b0-193">System-Flags</span></span>           | <span data-ttu-id="d08b0-194">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d08b0-194">0x00000010</span></span>                        |
| <span data-ttu-id="d08b0-195">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="d08b0-195">Classes used in</span></span>        | [<span data-ttu-id="d08b0-196">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="d08b0-196">**User**</span></span>](c-user.md)<br/> |



 

 






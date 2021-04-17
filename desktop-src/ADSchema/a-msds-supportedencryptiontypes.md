---
title: atributo MS-DS-Supported-Encryption-Types
description: Los algoritmos de cifrado compatibles con cuentas de usuario, equipo o confianza. Tenga en cuenta que el KDC usa esta información durante la generación de un vale de servicio para esta cuenta.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- MS-DS-Supported-Encryption-Types atributo AD Schema
- Esquema de AD de atributo msDS-SupportedEncryptionTypes
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659104"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a><span data-ttu-id="95723-105">atributo MS-DS-Supported-Encryption-Types</span><span class="sxs-lookup"><span data-stu-id="95723-105">ms-DS-Supported-Encryption-Types attribute</span></span>

<span data-ttu-id="95723-106">Los algoritmos de cifrado compatibles con cuentas de usuario, equipo o confianza.</span><span class="sxs-lookup"><span data-stu-id="95723-106">The encryption algorithms supported by user, computer or trust accounts.</span></span>

> [!Note]  
> <span data-ttu-id="95723-107">El KDC usa esta información durante la generación de un vale de servicio para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="95723-107">The KDC uses this information while generating a service ticket for this account.</span></span> <span data-ttu-id="95723-108">Los servicios y equipos pueden actualizar automáticamente este atributo en sus cuentas respectivas en Active Directory y, por tanto, necesitan tener acceso de escritura a este atributo.</span><span class="sxs-lookup"><span data-stu-id="95723-108">Services and Computers can automatically update this attribute on their respective accounts in Active Directory, and therefore need write access to this attribute.</span></span>

 



| <span data-ttu-id="95723-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="95723-109">Entry</span></span> | <span data-ttu-id="95723-110">Value</span><span class="sxs-lookup"><span data-stu-id="95723-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="95723-111">CN</span><span class="sxs-lookup"><span data-stu-id="95723-111">CN</span></span>                | <span data-ttu-id="95723-112">MS-DS-compatible-tipos de cifrado</span><span class="sxs-lookup"><span data-stu-id="95723-112">ms-DS-Supported-Encryption-Types</span></span>     |
| <span data-ttu-id="95723-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="95723-113">Ldap-Display-Name</span></span> | <span data-ttu-id="95723-114">msDS-SupportedEncryptionTypes</span><span class="sxs-lookup"><span data-stu-id="95723-114">msDS-SupportedEncryptionTypes</span></span>        |
| <span data-ttu-id="95723-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="95723-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="95723-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="95723-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="95723-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="95723-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="95723-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="95723-118">Attribute-Id</span></span>      | <span data-ttu-id="95723-119">1.2.840.113556.1.4.1963</span><span class="sxs-lookup"><span data-stu-id="95723-119">1.2.840.113556.1.4.1963</span></span>              |
| <span data-ttu-id="95723-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="95723-120">System-Id-Guid</span></span>    | <span data-ttu-id="95723-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span><span class="sxs-lookup"><span data-stu-id="95723-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span></span> |
| <span data-ttu-id="95723-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95723-122">Syntax</span></span>            | [<span data-ttu-id="95723-123">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="95723-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="95723-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="95723-124">Implementations</span></span>

-   [<span data-ttu-id="95723-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="95723-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="95723-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="95723-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="95723-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="95723-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="95723-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95723-128">Windows Server 2008</span></span>



| <span data-ttu-id="95723-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="95723-129">Entry</span></span> | <span data-ttu-id="95723-130">Value</span><span class="sxs-lookup"><span data-stu-id="95723-130">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95723-131">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="95723-131">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="95723-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95723-132">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="95723-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="95723-133">System-Only</span></span>            | <span data-ttu-id="95723-134">False</span><span class="sxs-lookup"><span data-stu-id="95723-134">False</span></span>                                                                                  |
| <span data-ttu-id="95723-135">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="95723-135">Is-Single-Valued</span></span>       | <span data-ttu-id="95723-136">True</span><span class="sxs-lookup"><span data-stu-id="95723-136">True</span></span>                                                                                   |
| <span data-ttu-id="95723-137">Está indexado</span><span class="sxs-lookup"><span data-stu-id="95723-137">Is Indexed</span></span>             | <span data-ttu-id="95723-138">False</span><span class="sxs-lookup"><span data-stu-id="95723-138">False</span></span>                                                                                  |
| <span data-ttu-id="95723-139">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="95723-139">In Global Catalog</span></span>      | <span data-ttu-id="95723-140">False</span><span class="sxs-lookup"><span data-stu-id="95723-140">False</span></span>                                                                                  |
| <span data-ttu-id="95723-141">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="95723-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="95723-142">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="95723-142">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="95723-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95723-143">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="95723-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95723-144">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="95723-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95723-145">Search-Flags</span></span>           | <span data-ttu-id="95723-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95723-146">0x00000000</span></span>                                                                             |
| <span data-ttu-id="95723-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95723-147">System-Flags</span></span>           | <span data-ttu-id="95723-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95723-148">0x00000010</span></span>                                                                             |
| <span data-ttu-id="95723-149">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="95723-149">Classes used in</span></span>        | [<span data-ttu-id="95723-150">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="95723-150">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="95723-151">**User**</span><span class="sxs-lookup"><span data-stu-id="95723-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="95723-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="95723-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="95723-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="95723-153">Entry</span></span> | <span data-ttu-id="95723-154">Value</span><span class="sxs-lookup"><span data-stu-id="95723-154">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95723-155">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="95723-155">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="95723-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95723-156">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="95723-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="95723-157">System-Only</span></span>            | <span data-ttu-id="95723-158">False</span><span class="sxs-lookup"><span data-stu-id="95723-158">False</span></span>                                                                                  |
| <span data-ttu-id="95723-159">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="95723-159">Is-Single-Valued</span></span>       | <span data-ttu-id="95723-160">True</span><span class="sxs-lookup"><span data-stu-id="95723-160">True</span></span>                                                                                   |
| <span data-ttu-id="95723-161">Está indexado</span><span class="sxs-lookup"><span data-stu-id="95723-161">Is Indexed</span></span>             | <span data-ttu-id="95723-162">False</span><span class="sxs-lookup"><span data-stu-id="95723-162">False</span></span>                                                                                  |
| <span data-ttu-id="95723-163">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="95723-163">In Global Catalog</span></span>      | <span data-ttu-id="95723-164">False</span><span class="sxs-lookup"><span data-stu-id="95723-164">False</span></span>                                                                                  |
| <span data-ttu-id="95723-165">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="95723-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="95723-166">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="95723-166">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="95723-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95723-167">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="95723-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95723-168">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="95723-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95723-169">Search-Flags</span></span>           | <span data-ttu-id="95723-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95723-170">0x00000000</span></span>                                                                             |
| <span data-ttu-id="95723-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95723-171">System-Flags</span></span>           | <span data-ttu-id="95723-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95723-172">0x00000010</span></span>                                                                             |
| <span data-ttu-id="95723-173">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="95723-173">Classes used in</span></span>        | [<span data-ttu-id="95723-174">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="95723-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="95723-175">**User**</span><span class="sxs-lookup"><span data-stu-id="95723-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="95723-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95723-176">Windows Server 2012</span></span>



| <span data-ttu-id="95723-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="95723-177">Entry</span></span> | <span data-ttu-id="95723-178">Value</span><span class="sxs-lookup"><span data-stu-id="95723-178">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95723-179">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="95723-179">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="95723-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="95723-180">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="95723-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="95723-181">System-Only</span></span>            | <span data-ttu-id="95723-182">False</span><span class="sxs-lookup"><span data-stu-id="95723-182">False</span></span>                                                                                  |
| <span data-ttu-id="95723-183">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="95723-183">Is-Single-Valued</span></span>       | <span data-ttu-id="95723-184">True</span><span class="sxs-lookup"><span data-stu-id="95723-184">True</span></span>                                                                                   |
| <span data-ttu-id="95723-185">Está indexado</span><span class="sxs-lookup"><span data-stu-id="95723-185">Is Indexed</span></span>             | <span data-ttu-id="95723-186">False</span><span class="sxs-lookup"><span data-stu-id="95723-186">False</span></span>                                                                                  |
| <span data-ttu-id="95723-187">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="95723-187">In Global Catalog</span></span>      | <span data-ttu-id="95723-188">False</span><span class="sxs-lookup"><span data-stu-id="95723-188">False</span></span>                                                                                  |
| <span data-ttu-id="95723-189">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="95723-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="95723-190">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="95723-190">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="95723-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="95723-191">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="95723-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="95723-192">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="95723-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="95723-193">Search-Flags</span></span>           | <span data-ttu-id="95723-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="95723-194">0x00000000</span></span>                                                                             |
| <span data-ttu-id="95723-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="95723-195">System-Flags</span></span>           | <span data-ttu-id="95723-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95723-196">0x00000010</span></span>                                                                             |
| <span data-ttu-id="95723-197">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="95723-197">Classes used in</span></span>        | [<span data-ttu-id="95723-198">**Dominio de confianza**</span><span class="sxs-lookup"><span data-stu-id="95723-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="95723-199">**Usuario**</span><span class="sxs-lookup"><span data-stu-id="95723-199">**User**</span></span>](c-user.md)<br/> |



 

 






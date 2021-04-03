---
title: Atributo SAM-Account-Type
description: Este atributo contiene información sobre cada objeto de tipo de cuenta.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- SAM-Account-Type atributo AD Schema
- sAMAccountType esquema de AD de atributos
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997368"
---
# <a name="sam-account-type-attribute"></a><span data-ttu-id="5f21b-105">Atributo SAM-Account-Type</span><span class="sxs-lookup"><span data-stu-id="5f21b-105">SAM-Account-Type attribute</span></span>

<span data-ttu-id="5f21b-106">Este atributo contiene información sobre cada objeto de tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="5f21b-106">This attribute contains information about every account type object.</span></span> <span data-ttu-id="5f21b-107">Puede enumerar una lista de tipos de cuenta o puede usar la API Mostrar información para crear una lista.</span><span class="sxs-lookup"><span data-stu-id="5f21b-107">You can enumerate a list of account types or you can use the Display Information API to create a list.</span></span> <span data-ttu-id="5f21b-108">Dado que los equipos, las cuentas de usuario normales y las cuentas de confianza también se pueden enumerar como objetos de usuario, los valores de estas cuentas deben ser un intervalo contiguo.</span><span class="sxs-lookup"><span data-stu-id="5f21b-108">Because computers, normal user accounts, and trust accounts can also be enumerated as user objects, the values for these accounts must be a contiguous range.</span></span>

<span data-ttu-id="5f21b-109">Los valores posibles para este atributo son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5f21b-109">The possible values for this attribute are the following:</span></span>

-   <span data-ttu-id="5f21b-110">\_Objeto de dominio Sam \_ 0X0</span><span class="sxs-lookup"><span data-stu-id="5f21b-110">SAM\_DOMAIN\_OBJECT 0x0</span></span>
-   <span data-ttu-id="5f21b-111">\_Objeto de Grupo SAM \_ 0x10000000</span><span class="sxs-lookup"><span data-stu-id="5f21b-111">SAM\_GROUP\_OBJECT 0x10000000</span></span>
-   <span data-ttu-id="5f21b-112">\_Objeto de \_ grupo de no seguridad Sam \_ \_ 0x10000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-112">SAM\_NON\_SECURITY\_GROUP\_OBJECT 0x10000001</span></span>
-   <span data-ttu-id="5f21b-113">\_Objeto de alias Sam \_ 0x20000000</span><span class="sxs-lookup"><span data-stu-id="5f21b-113">SAM\_ALIAS\_OBJECT 0x20000000</span></span>
-   <span data-ttu-id="5f21b-114">\_Objeto de \_ alias de no seguridad Sam \_ \_ 0x20000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-114">SAM\_NON\_SECURITY\_ALIAS\_OBJECT 0x20000001</span></span>
-   <span data-ttu-id="5f21b-115">\_Objeto de usuario Sam \_ 0x30000000</span><span class="sxs-lookup"><span data-stu-id="5f21b-115">SAM\_USER\_OBJECT 0x30000000</span></span>
-   <span data-ttu-id="5f21b-116">SAM \_ \_ 0x30000000 de cuenta de usuario normal \_</span><span class="sxs-lookup"><span data-stu-id="5f21b-116">SAM\_NORMAL\_USER\_ACCOUNT 0x30000000</span></span>
-   <span data-ttu-id="5f21b-117">SAM \_ cuenta de equipo \_ 0x30000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-117">SAM\_MACHINE\_ACCOUNT 0x30000001</span></span>
-   <span data-ttu-id="5f21b-118">SAM de la \_ cuenta de confianza \_ 0x30000002</span><span class="sxs-lookup"><span data-stu-id="5f21b-118">SAM\_TRUST\_ACCOUNT 0x30000002</span></span>
-   <span data-ttu-id="5f21b-119">\_ \_ Grupo básico de la aplicación Sam \_</span><span class="sxs-lookup"><span data-stu-id="5f21b-119">SAM\_APP\_BASIC\_GROUP 0x40000000</span></span>
-   <span data-ttu-id="5f21b-120">\_Grupo de consulta de aplicaciones Sam \_ \_ 0x40000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-120">SAM\_APP\_QUERY\_GROUP 0x40000001</span></span>
-   <span data-ttu-id="5f21b-121">\_Tipo de cuenta SAM \_ \_ máx.</span><span class="sxs-lookup"><span data-stu-id="5f21b-121">SAM\_ACCOUNT\_TYPE\_MAX 0x7fffffff</span></span>



| <span data-ttu-id="5f21b-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f21b-122">Entry</span></span> | <span data-ttu-id="5f21b-123">Value</span><span class="sxs-lookup"><span data-stu-id="5f21b-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5f21b-124">CN</span><span class="sxs-lookup"><span data-stu-id="5f21b-124">CN</span></span>                | <span data-ttu-id="5f21b-125">Tipo de cuenta SAM</span><span class="sxs-lookup"><span data-stu-id="5f21b-125">SAM-Account-Type</span></span>                                                |
| <span data-ttu-id="5f21b-126">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="5f21b-126">Ldap-Display-Name</span></span> | <span data-ttu-id="5f21b-127">sAMAccountType</span><span class="sxs-lookup"><span data-stu-id="5f21b-127">sAMAccountType</span></span>                                                  |
| <span data-ttu-id="5f21b-128">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5f21b-128">Size</span></span>              | \-                                                              |
| <span data-ttu-id="5f21b-129">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="5f21b-129">Update Privilege</span></span>  | <span data-ttu-id="5f21b-130">El sistema establece este valor.</span><span class="sxs-lookup"><span data-stu-id="5f21b-130">This value is set by the system.</span></span>                                |
| <span data-ttu-id="5f21b-131">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="5f21b-131">Update Frequency</span></span>  | <span data-ttu-id="5f21b-132">Lo establece el sistema operativo cuando se crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="5f21b-132">This is set by the operating system when the object is created.</span></span> |
| <span data-ttu-id="5f21b-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5f21b-133">Attribute-Id</span></span>      | <span data-ttu-id="5f21b-134">1.2.840.113556.1.4.302</span><span class="sxs-lookup"><span data-stu-id="5f21b-134">1.2.840.113556.1.4.302</span></span>                                          |
| <span data-ttu-id="5f21b-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5f21b-135">System-Id-Guid</span></span>    | <span data-ttu-id="5f21b-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="5f21b-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span></span>                            |
| <span data-ttu-id="5f21b-137">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f21b-137">Syntax</span></span>            | [<span data-ttu-id="5f21b-138">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="5f21b-138">**Enumeration**</span></span>](s-enumeration.md)                            |



## <a name="implementations"></a><span data-ttu-id="5f21b-139">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="5f21b-139">Implementations</span></span>

-   [<span data-ttu-id="5f21b-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5f21b-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5f21b-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5f21b-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5f21b-142">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5f21b-142">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5f21b-143">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5f21b-143">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5f21b-144">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5f21b-144">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5f21b-145">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5f21b-145">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5f21b-146">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f21b-146">Windows 2000 Server</span></span>



| <span data-ttu-id="5f21b-147">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f21b-147">Entry</span></span> | <span data-ttu-id="5f21b-148">Value</span><span class="sxs-lookup"><span data-stu-id="5f21b-148">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5f21b-149">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f21b-149">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-150">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f21b-150">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-151">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f21b-151">System-Only</span></span>            | <span data-ttu-id="5f21b-152">False</span><span class="sxs-lookup"><span data-stu-id="5f21b-152">False</span></span>                                                        |
| <span data-ttu-id="5f21b-153">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f21b-153">Is-Single-Valued</span></span>       | <span data-ttu-id="5f21b-154">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-154">True</span></span>                                                         |
| <span data-ttu-id="5f21b-155">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f21b-155">Is Indexed</span></span>             | <span data-ttu-id="5f21b-156">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-156">True</span></span>                                                         |
| <span data-ttu-id="5f21b-157">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f21b-157">In Global Catalog</span></span>      | <span data-ttu-id="5f21b-158">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-158">True</span></span>                                                         |
| <span data-ttu-id="5f21b-159">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f21b-159">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f21b-160">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f21b-160">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5f21b-161">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f21b-161">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-162">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f21b-162">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-163">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-163">Search-Flags</span></span>           | <span data-ttu-id="5f21b-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-164">0x00000001</span></span>                                                   |
| <span data-ttu-id="5f21b-165">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-165">System-Flags</span></span>           | <span data-ttu-id="5f21b-166">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5f21b-166">0x00000012</span></span>                                                   |
| <span data-ttu-id="5f21b-167">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f21b-167">Classes used in</span></span>        | [<span data-ttu-id="5f21b-168">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="5f21b-168">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5f21b-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f21b-169">Windows Server 2003</span></span>



| <span data-ttu-id="5f21b-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f21b-170">Entry</span></span> | <span data-ttu-id="5f21b-171">Value</span><span class="sxs-lookup"><span data-stu-id="5f21b-171">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5f21b-172">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f21b-172">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-173">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f21b-173">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-174">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f21b-174">System-Only</span></span>            | <span data-ttu-id="5f21b-175">False</span><span class="sxs-lookup"><span data-stu-id="5f21b-175">False</span></span>                                                        |
| <span data-ttu-id="5f21b-176">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f21b-176">Is-Single-Valued</span></span>       | <span data-ttu-id="5f21b-177">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-177">True</span></span>                                                         |
| <span data-ttu-id="5f21b-178">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f21b-178">Is Indexed</span></span>             | <span data-ttu-id="5f21b-179">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-179">True</span></span>                                                         |
| <span data-ttu-id="5f21b-180">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f21b-180">In Global Catalog</span></span>      | <span data-ttu-id="5f21b-181">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-181">True</span></span>                                                         |
| <span data-ttu-id="5f21b-182">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f21b-182">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f21b-183">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f21b-183">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5f21b-184">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f21b-184">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-185">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f21b-185">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-186">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-186">Search-Flags</span></span>           | <span data-ttu-id="5f21b-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-187">0x00000001</span></span>                                                   |
| <span data-ttu-id="5f21b-188">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-188">System-Flags</span></span>           | <span data-ttu-id="5f21b-189">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5f21b-189">0x00000012</span></span>                                                   |
| <span data-ttu-id="5f21b-190">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f21b-190">Classes used in</span></span>        | [<span data-ttu-id="5f21b-191">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="5f21b-191">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5f21b-192">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5f21b-192">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5f21b-193">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f21b-193">Entry</span></span> | <span data-ttu-id="5f21b-194">Value</span><span class="sxs-lookup"><span data-stu-id="5f21b-194">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5f21b-195">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f21b-195">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-196">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f21b-196">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f21b-197">System-Only</span></span>            | <span data-ttu-id="5f21b-198">False</span><span class="sxs-lookup"><span data-stu-id="5f21b-198">False</span></span>                                                        |
| <span data-ttu-id="5f21b-199">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f21b-199">Is-Single-Valued</span></span>       | <span data-ttu-id="5f21b-200">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-200">True</span></span>                                                         |
| <span data-ttu-id="5f21b-201">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f21b-201">Is Indexed</span></span>             | <span data-ttu-id="5f21b-202">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-202">True</span></span>                                                         |
| <span data-ttu-id="5f21b-203">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f21b-203">In Global Catalog</span></span>      | <span data-ttu-id="5f21b-204">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-204">True</span></span>                                                         |
| <span data-ttu-id="5f21b-205">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f21b-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f21b-206">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f21b-206">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5f21b-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f21b-207">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-208">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f21b-208">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-209">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-209">Search-Flags</span></span>           | <span data-ttu-id="5f21b-210">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-210">0x00000001</span></span>                                                   |
| <span data-ttu-id="5f21b-211">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-211">System-Flags</span></span>           | <span data-ttu-id="5f21b-212">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5f21b-212">0x00000012</span></span>                                                   |
| <span data-ttu-id="5f21b-213">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f21b-213">Classes used in</span></span>        | [<span data-ttu-id="5f21b-214">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="5f21b-214">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5f21b-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f21b-215">Windows Server 2008</span></span>



| <span data-ttu-id="5f21b-216">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f21b-216">Entry</span></span> | <span data-ttu-id="5f21b-217">Value</span><span class="sxs-lookup"><span data-stu-id="5f21b-217">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5f21b-218">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f21b-218">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-219">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f21b-219">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f21b-220">System-Only</span></span>            | <span data-ttu-id="5f21b-221">False</span><span class="sxs-lookup"><span data-stu-id="5f21b-221">False</span></span>                                                        |
| <span data-ttu-id="5f21b-222">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f21b-222">Is-Single-Valued</span></span>       | <span data-ttu-id="5f21b-223">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-223">True</span></span>                                                         |
| <span data-ttu-id="5f21b-224">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f21b-224">Is Indexed</span></span>             | <span data-ttu-id="5f21b-225">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-225">True</span></span>                                                         |
| <span data-ttu-id="5f21b-226">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f21b-226">In Global Catalog</span></span>      | <span data-ttu-id="5f21b-227">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-227">True</span></span>                                                         |
| <span data-ttu-id="5f21b-228">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f21b-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f21b-229">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f21b-229">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5f21b-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f21b-230">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f21b-231">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-232">Search-Flags</span></span>           | <span data-ttu-id="5f21b-233">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-233">0x00000001</span></span>                                                   |
| <span data-ttu-id="5f21b-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-234">System-Flags</span></span>           | <span data-ttu-id="5f21b-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5f21b-235">0x00000012</span></span>                                                   |
| <span data-ttu-id="5f21b-236">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f21b-236">Classes used in</span></span>        | [<span data-ttu-id="5f21b-237">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="5f21b-237">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5f21b-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f21b-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5f21b-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f21b-239">Entry</span></span> | <span data-ttu-id="5f21b-240">Value</span><span class="sxs-lookup"><span data-stu-id="5f21b-240">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5f21b-241">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f21b-241">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f21b-242">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f21b-243">System-Only</span></span>            | <span data-ttu-id="5f21b-244">False</span><span class="sxs-lookup"><span data-stu-id="5f21b-244">False</span></span>                                                        |
| <span data-ttu-id="5f21b-245">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f21b-245">Is-Single-Valued</span></span>       | <span data-ttu-id="5f21b-246">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-246">True</span></span>                                                         |
| <span data-ttu-id="5f21b-247">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f21b-247">Is Indexed</span></span>             | <span data-ttu-id="5f21b-248">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-248">True</span></span>                                                         |
| <span data-ttu-id="5f21b-249">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f21b-249">In Global Catalog</span></span>      | <span data-ttu-id="5f21b-250">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-250">True</span></span>                                                         |
| <span data-ttu-id="5f21b-251">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f21b-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f21b-252">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f21b-252">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5f21b-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f21b-253">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f21b-254">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-255">Search-Flags</span></span>           | <span data-ttu-id="5f21b-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-256">0x00000001</span></span>                                                   |
| <span data-ttu-id="5f21b-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-257">System-Flags</span></span>           | <span data-ttu-id="5f21b-258">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5f21b-258">0x00000012</span></span>                                                   |
| <span data-ttu-id="5f21b-259">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f21b-259">Classes used in</span></span>        | [<span data-ttu-id="5f21b-260">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="5f21b-260">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5f21b-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f21b-261">Windows Server 2012</span></span>



| <span data-ttu-id="5f21b-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f21b-262">Entry</span></span> | <span data-ttu-id="5f21b-263">Value</span><span class="sxs-lookup"><span data-stu-id="5f21b-263">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5f21b-264">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="5f21b-264">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f21b-265">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5f21b-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f21b-266">System-Only</span></span>            | <span data-ttu-id="5f21b-267">False</span><span class="sxs-lookup"><span data-stu-id="5f21b-267">False</span></span>                                                        |
| <span data-ttu-id="5f21b-268">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="5f21b-268">Is-Single-Valued</span></span>       | <span data-ttu-id="5f21b-269">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-269">True</span></span>                                                         |
| <span data-ttu-id="5f21b-270">Está indexado</span><span class="sxs-lookup"><span data-stu-id="5f21b-270">Is Indexed</span></span>             | <span data-ttu-id="5f21b-271">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-271">True</span></span>                                                         |
| <span data-ttu-id="5f21b-272">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="5f21b-272">In Global Catalog</span></span>      | <span data-ttu-id="5f21b-273">True</span><span class="sxs-lookup"><span data-stu-id="5f21b-273">True</span></span>                                                         |
| <span data-ttu-id="5f21b-274">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="5f21b-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f21b-275">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f21b-275">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5f21b-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f21b-276">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f21b-277">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5f21b-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-278">Search-Flags</span></span>           | <span data-ttu-id="5f21b-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f21b-279">0x00000001</span></span>                                                   |
| <span data-ttu-id="5f21b-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f21b-280">System-Flags</span></span>           | <span data-ttu-id="5f21b-281">0x00000012</span><span class="sxs-lookup"><span data-stu-id="5f21b-281">0x00000012</span></span>                                                   |
| <span data-ttu-id="5f21b-282">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="5f21b-282">Classes used in</span></span>        | [<span data-ttu-id="5f21b-283">**Entidad de seguridad**</span><span class="sxs-lookup"><span data-stu-id="5f21b-283">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 






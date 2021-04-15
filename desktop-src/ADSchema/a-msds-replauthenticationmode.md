---
title: atributo MS-DS-REPL-Authentication-Mode
description: El atributo MS-DS-REPL-Authentication-Mode se usa para especificar el método de autenticación que se utiliza para autenticar a los asociados de replicación.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-REPL-Authentication-Mode
- Esquema de AD del atributo msDS-ReplAuthenticationMode
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494020"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a><span data-ttu-id="c7bf7-105">atributo MS-DS-REPL-Authentication-Mode</span><span class="sxs-lookup"><span data-stu-id="c7bf7-105">ms-DS-Repl-Authentication-Mode attribute</span></span>

<span data-ttu-id="c7bf7-106">El atributo **MS-DS-REPL-Authentication-Mode** se usa para especificar el método de autenticación que se utiliza para autenticar a los asociados de replicación.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-106">The **ms-DS-Repl-Authentication-Mode** attribute is used to specify which authentication method is used to authenticate replication partners.</span></span> <span data-ttu-id="c7bf7-107">Este atributo se aplica a la partición de configuración de una instancia de ADAM.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-107">This attribute applies to the configuration partition of an ADAM instance.</span></span>

<span data-ttu-id="c7bf7-108">Los valores siguientes son los valores posibles para este atributo.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-108">The following values are the possible values for this attribute.</span></span>

| <span data-ttu-id="c7bf7-109">Value</span><span class="sxs-lookup"><span data-stu-id="c7bf7-109">Value</span></span>        | <span data-ttu-id="c7bf7-110">Método de autenticación</span><span class="sxs-lookup"><span data-stu-id="c7bf7-110">Authentication method</span></span>                          | <span data-ttu-id="c7bf7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7bf7-111">Description</span></span>                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7bf7-112">0</span><span class="sxs-lookup"><span data-stu-id="c7bf7-112">0</span></span><br/> | <span data-ttu-id="c7bf7-113">Paso negociado</span><span class="sxs-lookup"><span data-stu-id="c7bf7-113">Negotiated pass-through</span></span><br/>             | <span data-ttu-id="c7bf7-114">Todas las instancias de ADAM del conjunto de configuración usan el mismo nombre de cuenta y la misma contraseña que la cuenta de servicio de ADAM.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-114">All ADAM instances in the configuration set use an identical account name and password as the ADAM service account.</span></span><br/>                                                 |
| <span data-ttu-id="c7bf7-115">1</span><span class="sxs-lookup"><span data-stu-id="c7bf7-115">1</span></span><br/> | <span data-ttu-id="c7bf7-116">Negotiated</span><span class="sxs-lookup"><span data-stu-id="c7bf7-116">Negotiated</span></span><br/>                          | <span data-ttu-id="c7bf7-117">Primero se intenta la autenticación Kerberos (utilizando SPN).</span><span class="sxs-lookup"><span data-stu-id="c7bf7-117">Kerberos authentication (using SPNs) is attempted first.</span></span> <span data-ttu-id="c7bf7-118">Si se produce un error en Kerberos, se intenta la autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-118">If Kerberos fails, NTLM authentication is attempted.</span></span> <span data-ttu-id="c7bf7-119">Si se produce un error en NTLM, las instancias de ADAM no se replicarán.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-119">If NTLM fails, the ADAM instances will not replicate.</span></span><br/> |
| <span data-ttu-id="c7bf7-120">2</span><span class="sxs-lookup"><span data-stu-id="c7bf7-120">2</span></span><br/> | <span data-ttu-id="c7bf7-121">Autenticación mutua con Kerberos</span><span class="sxs-lookup"><span data-stu-id="c7bf7-121">Mutual authentication with Kerberos</span></span><br/> | <span data-ttu-id="c7bf7-122">Autenticación con Kerberos, que usa nombres principales de servicio (SPN) obligatoriamente.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-122">Kerberos authentication, using service principal names (SPNs), is required.</span></span> <span data-ttu-id="c7bf7-123">Si se produce un error en la autenticación Kerberos, no se replicarán las instancias de ADAM.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-123">If Kerberos authentication fails, the ADAM instances will not replicate.</span></span><br/>                |



 

<span data-ttu-id="c7bf7-124">La tabla siguiente contiene los identificadores de programación para los valores de este atributo.</span><span class="sxs-lookup"><span data-stu-id="c7bf7-124">The following table contains the programmatic identifiers for the values of this attribute.</span></span>

| <span data-ttu-id="c7bf7-125">Value</span><span class="sxs-lookup"><span data-stu-id="c7bf7-125">Value</span></span>        | <span data-ttu-id="c7bf7-126">Identifier (desde ntdsapi. h)</span><span class="sxs-lookup"><span data-stu-id="c7bf7-126">Identifier (from Ntdsapi.h)</span></span>                                               |
|--------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c7bf7-127">0</span><span class="sxs-lookup"><span data-stu-id="c7bf7-127">0</span></span><br/> | <span data-ttu-id="c7bf7-128">**modo de autenticación de REPL de ADAM \_ \_ \_ \_ negociar \_ paso \_ a través**</span><span class="sxs-lookup"><span data-stu-id="c7bf7-128">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE\_PASS\_THROUGH**</span></span><br/> |
| <span data-ttu-id="c7bf7-129">1</span><span class="sxs-lookup"><span data-stu-id="c7bf7-129">1</span></span><br/> | <span data-ttu-id="c7bf7-130">**modo de autenticación de REPL de ADAM \_ \_ \_ \_ Negotiate**</span><span class="sxs-lookup"><span data-stu-id="c7bf7-130">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE**</span></span><br/>                |
| <span data-ttu-id="c7bf7-131">2</span><span class="sxs-lookup"><span data-stu-id="c7bf7-131">2</span></span><br/> | <span data-ttu-id="c7bf7-132">**modo de autenticación de replicación de ADAM, se \_ \_ \_ \_ \_ requiere autenticación mutua \_**</span><span class="sxs-lookup"><span data-stu-id="c7bf7-132">**ADAM\_REPL\_AUTHENTICATION\_MODE\_MUTUAL\_AUTH\_REQUIRED**</span></span><br/>   |



 



| <span data-ttu-id="c7bf7-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7bf7-133">Entry</span></span> | <span data-ttu-id="c7bf7-134">Value</span><span class="sxs-lookup"><span data-stu-id="c7bf7-134">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c7bf7-135">CN</span><span class="sxs-lookup"><span data-stu-id="c7bf7-135">CN</span></span>                | <span data-ttu-id="c7bf7-136">MS-DS-REPL-autenticación-modo</span><span class="sxs-lookup"><span data-stu-id="c7bf7-136">ms-DS-Repl-Authentication-Mode</span></span>       |
| <span data-ttu-id="c7bf7-137">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="c7bf7-137">Ldap-Display-Name</span></span> | <span data-ttu-id="c7bf7-138">msDS-ReplAuthenticationMode</span><span class="sxs-lookup"><span data-stu-id="c7bf7-138">msDS-ReplAuthenticationMode</span></span>          |
| <span data-ttu-id="c7bf7-139">Tamaño</span><span class="sxs-lookup"><span data-stu-id="c7bf7-139">Size</span></span>              | \-                                   |
| <span data-ttu-id="c7bf7-140">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="c7bf7-140">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c7bf7-141">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="c7bf7-141">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c7bf7-142">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c7bf7-142">Attribute-Id</span></span>      | <span data-ttu-id="c7bf7-143">1.2.840.113556.1.4.1861</span><span class="sxs-lookup"><span data-stu-id="c7bf7-143">1.2.840.113556.1.4.1861</span></span>              |
| <span data-ttu-id="c7bf7-144">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c7bf7-144">System-Id-Guid</span></span>    | <span data-ttu-id="c7bf7-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span><span class="sxs-lookup"><span data-stu-id="c7bf7-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span></span> |
| <span data-ttu-id="c7bf7-146">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7bf7-146">Syntax</span></span>            | [<span data-ttu-id="c7bf7-147">**Enumeración**</span><span class="sxs-lookup"><span data-stu-id="c7bf7-147">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c7bf7-148">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="c7bf7-148">Implementations</span></span>

-   [<span data-ttu-id="c7bf7-149">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c7bf7-149">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="c7bf7-150">ADAM</span><span class="sxs-lookup"><span data-stu-id="c7bf7-150">ADAM</span></span>



| <span data-ttu-id="c7bf7-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7bf7-151">Entry</span></span> | <span data-ttu-id="c7bf7-152">Value</span><span class="sxs-lookup"><span data-stu-id="c7bf7-152">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="c7bf7-153">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="c7bf7-153">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c7bf7-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7bf7-154">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="c7bf7-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7bf7-155">System-Only</span></span>            | <span data-ttu-id="c7bf7-156">False</span><span class="sxs-lookup"><span data-stu-id="c7bf7-156">False</span></span>                                               |
| <span data-ttu-id="c7bf7-157">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="c7bf7-157">Is-Single-Valued</span></span>       | <span data-ttu-id="c7bf7-158">True</span><span class="sxs-lookup"><span data-stu-id="c7bf7-158">True</span></span>                                                |
| <span data-ttu-id="c7bf7-159">Está indexado</span><span class="sxs-lookup"><span data-stu-id="c7bf7-159">Is Indexed</span></span>             | <span data-ttu-id="c7bf7-160">False</span><span class="sxs-lookup"><span data-stu-id="c7bf7-160">False</span></span>                                               |
| <span data-ttu-id="c7bf7-161">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7bf7-161">In Global Catalog</span></span>      | <span data-ttu-id="c7bf7-162">False</span><span class="sxs-lookup"><span data-stu-id="c7bf7-162">False</span></span>                                               |
| <span data-ttu-id="c7bf7-163">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="c7bf7-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7bf7-164">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c7bf7-164">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="c7bf7-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7bf7-165">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="c7bf7-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7bf7-166">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="c7bf7-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7bf7-167">Search-Flags</span></span>           | <span data-ttu-id="c7bf7-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7bf7-168">0x00000000</span></span>                                          |
| <span data-ttu-id="c7bf7-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7bf7-169">System-Flags</span></span>           | <span data-ttu-id="c7bf7-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7bf7-170">0x00000010</span></span>                                          |
| <span data-ttu-id="c7bf7-171">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="c7bf7-171">Classes used in</span></span>        | [<span data-ttu-id="c7bf7-172">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="c7bf7-172">**Configuration**</span></span>](c-configuration.md)<br/> |



 

 






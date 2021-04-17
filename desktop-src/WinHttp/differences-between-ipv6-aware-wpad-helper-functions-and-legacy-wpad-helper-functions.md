---
title: IPv6-Aware y funciones auxiliares de WPAD heredadas
description: Diferencias entre las funciones auxiliares de WPAD IPv6-Aware y las funciones auxiliares de WPAD heredadas
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716647"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a><span data-ttu-id="bb416-103">IPv6-Aware y funciones auxiliares de WPAD heredadas</span><span class="sxs-lookup"><span data-stu-id="bb416-103">IPv6-Aware and Legacy WPAD helper functions</span></span>

<span data-ttu-id="bb416-104">En las tablas siguientes se explican las diferencias entre las nuevas funciones auxiliares de WPAD y las funciones auxiliares de WPAD heredadas.</span><span class="sxs-lookup"><span data-stu-id="bb416-104">The following tables explain the differences between the new WPAD helper functions and the legacy WPAD helper functions.</span></span> <span data-ttu-id="bb416-105">Las nuevas funciones se marcan con un asterisco.</span><span class="sxs-lookup"><span data-stu-id="bb416-105">The new functions are marked with an asterisk.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bb416-106">Functions</span><span class="sxs-lookup"><span data-stu-id="bb416-106">Functions</span></span></th>
<th><span data-ttu-id="bb416-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb416-107">Input</span></span></th>
<th><span data-ttu-id="bb416-108">Output</span><span class="sxs-lookup"><span data-stu-id="bb416-108">Output</span></span></th>
<th><span data-ttu-id="bb416-109">Motivo del cambio</span><span class="sxs-lookup"><span data-stu-id="bb416-109">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb416-110">dnsResolve</span><span class="sxs-lookup"><span data-stu-id="bb416-110">dnsResolve</span></span></td>
<td><span data-ttu-id="bb416-111">Host</span><span class="sxs-lookup"><span data-stu-id="bb416-111">Host</span></span></td>
<td><span data-ttu-id="bb416-112">Dirección IPv4</span><span class="sxs-lookup"><span data-stu-id="bb416-112">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="bb416-113">La función ex devolverá una lista de IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="bb416-113">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="bb416-114">Necesario porque las direcciones IPv6 o IPv4 pueden tener varias direcciones de unidifusión para una sola interfaz. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="bb416-114">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb416-115">dnsResolveEx\*</span><span class="sxs-lookup"><span data-stu-id="bb416-115">dnsResolveEx\*</span></span></td>
<td><span data-ttu-id="bb416-116">Host</span><span class="sxs-lookup"><span data-stu-id="bb416-116">Host</span></span></td>
<td><span data-ttu-id="bb416-117">Lista de direcciones IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="bb416-117">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bb416-118">Functions</span><span class="sxs-lookup"><span data-stu-id="bb416-118">Functions</span></span></th>
<th><span data-ttu-id="bb416-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb416-119">Input</span></span></th>
<th><span data-ttu-id="bb416-120">Output</span><span class="sxs-lookup"><span data-stu-id="bb416-120">Output</span></span></th>
<th><span data-ttu-id="bb416-121">Motivo del cambio</span><span class="sxs-lookup"><span data-stu-id="bb416-121">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb416-122">isResolveable</span><span class="sxs-lookup"><span data-stu-id="bb416-122">isResolveable</span></span></td>
<td><span data-ttu-id="bb416-123">Host IPv4</span><span class="sxs-lookup"><span data-stu-id="bb416-123">IPv4 host</span></span></td>
<td><span data-ttu-id="bb416-124">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="bb416-124">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="bb416-125">La función ex devolverá TRUE si un host se puede resolver en una dirección IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="bb416-125">The Ex function will return TRUE if a host can resolve to an IPv6 or IPv4 address.</span></span> <span data-ttu-id="bb416-126">La función heredada solo devuelve TRUE si el host se resuelve en una dirección IPv4. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="bb416-126">The legacy function only returns TRUE if the host resolves to an IPv4 address.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb416-127">isResolveableEx\*</span><span class="sxs-lookup"><span data-stu-id="bb416-127">isResolveableEx\*</span></span></td>
<td><span data-ttu-id="bb416-128">Host IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="bb416-128">IPv6/IPv4 host</span></span></td>
<td><span data-ttu-id="bb416-129">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="bb416-129">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bb416-130">Functions</span><span class="sxs-lookup"><span data-stu-id="bb416-130">Functions</span></span></th>
<th><span data-ttu-id="bb416-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb416-131">Input</span></span></th>
<th><span data-ttu-id="bb416-132">Output</span><span class="sxs-lookup"><span data-stu-id="bb416-132">Output</span></span></th>
<th><span data-ttu-id="bb416-133">Motivo del cambio</span><span class="sxs-lookup"><span data-stu-id="bb416-133">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb416-134">myIPAddress</span><span class="sxs-lookup"><span data-stu-id="bb416-134">myIPAddress</span></span></td>
<td><span data-ttu-id="bb416-135">ninguno</span><span class="sxs-lookup"><span data-stu-id="bb416-135">none</span></span></td>
<td><span data-ttu-id="bb416-136">Dirección IPv4</span><span class="sxs-lookup"><span data-stu-id="bb416-136">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="bb416-137">La función ex devolverá una lista de IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="bb416-137">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="bb416-138">Necesario porque las direcciones IPv6 o IPv4 pueden tener varias direcciones de unidifusión para una sola interfaz $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="bb416-138">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface ${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb416-139">myIPAddressEx\*</span><span class="sxs-lookup"><span data-stu-id="bb416-139">myIPAddressEx\*</span></span></td>
<td><span data-ttu-id="bb416-140">ninguno</span><span class="sxs-lookup"><span data-stu-id="bb416-140">none</span></span></td>
<td><span data-ttu-id="bb416-141">Lista de direcciones IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="bb416-141">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bb416-142">Functions</span><span class="sxs-lookup"><span data-stu-id="bb416-142">Functions</span></span></th>
<th><span data-ttu-id="bb416-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb416-143">Input</span></span></th>
<th><span data-ttu-id="bb416-144">Output</span><span class="sxs-lookup"><span data-stu-id="bb416-144">Output</span></span></th>
<th><span data-ttu-id="bb416-145">Motivo del cambio</span><span class="sxs-lookup"><span data-stu-id="bb416-145">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb416-146">isInNet</span><span class="sxs-lookup"><span data-stu-id="bb416-146">isInNet</span></span></td>
<td><span data-ttu-id="bb416-147">Host, patrón de dirección IP separada por puntos, máscara de dirección IP</span><span class="sxs-lookup"><span data-stu-id="bb416-147">Host, Dot separated IP address pattern, IP address Mask</span></span></td>
<td><span data-ttu-id="bb416-148">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="bb416-148">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="bb416-149">Proporcione una manera independiente de la versión de IP para buscar si una dirección IP se encuentra en una subred determinada.</span><span class="sxs-lookup"><span data-stu-id="bb416-149">Provide an IP version agnostic way to find if an IP address is in a given subnet.</span></span> <span data-ttu-id="bb416-150">Además, la notación de máscara de IPv4 está en desuso. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="bb416-150">Also, the mask notation in IPv4 is deprecated.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb416-151">isInNetEx\*</span><span class="sxs-lookup"><span data-stu-id="bb416-151">isInNetEx\*</span></span></td>
<td><span data-ttu-id="bb416-152">Prefijo IP de dirección IP</span><span class="sxs-lookup"><span data-stu-id="bb416-152">IP Address IP Prefix</span></span></td>
<td><span data-ttu-id="bb416-153">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="bb416-153">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



| <span data-ttu-id="bb416-154">Functions</span><span class="sxs-lookup"><span data-stu-id="bb416-154">Functions</span></span>           | <span data-ttu-id="bb416-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb416-155">Input</span></span>                       | <span data-ttu-id="bb416-156">Output</span><span class="sxs-lookup"><span data-stu-id="bb416-156">Output</span></span>                             | <span data-ttu-id="bb416-157">Motivo del cambio</span><span class="sxs-lookup"><span data-stu-id="bb416-157">Reason for Change</span></span>                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb416-158">sortIPAddressList\*</span><span class="sxs-lookup"><span data-stu-id="bb416-158">sortIPAddressList\*</span></span> | <span data-ttu-id="bb416-159">Lista de direcciones IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="bb416-159">List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="bb416-160">Lista ordenada de direcciones IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="bb416-160">Sorted List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="bb416-161">No hay ninguna función heredada equivalente porque las funciones heredadas solo devolvían una única dirección IPv4, por lo que no era necesario ordenar.</span><span class="sxs-lookup"><span data-stu-id="bb416-161">There is no counterpart legacy function because legacy functions only returned a single IPv4 address, therefore there was no need to sort .</span></span> |



 



| <span data-ttu-id="bb416-162">Functions</span><span class="sxs-lookup"><span data-stu-id="bb416-162">Functions</span></span>          | <span data-ttu-id="bb416-163">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb416-163">Input</span></span> | <span data-ttu-id="bb416-164">Output</span><span class="sxs-lookup"><span data-stu-id="bb416-164">Output</span></span>                     | <span data-ttu-id="bb416-165">Motivo del cambio</span><span class="sxs-lookup"><span data-stu-id="bb416-165">Reason for Change</span></span>                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb416-166">getClientVersion\*</span><span class="sxs-lookup"><span data-stu-id="bb416-166">getClientVersion\*</span></span> | <span data-ttu-id="bb416-167">ninguno</span><span class="sxs-lookup"><span data-stu-id="bb416-167">none</span></span>  | <span data-ttu-id="bb416-168">Número de versión del motor WPAD</span><span class="sxs-lookup"><span data-stu-id="bb416-168">WPAD engine version number</span></span> | <span data-ttu-id="bb416-169">Actualmente, esta función devuelve la versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="bb416-169">Currently this function returns version 1.0.</span></span> <span data-ttu-id="bb416-170">Hemos agregado esta función para permitir que los administradores de ti actualicen su WPAD para trabajar con versiones diferentes del motor WPAD sin causar interrupciones en su implementación existente.</span><span class="sxs-lookup"><span data-stu-id="bb416-170">We added this function to allow IT administrators to update their WPAD to work with different versions of the WPAD engine without causing breaks to their existent deployment.</span></span> |



 

> [!Note]  
> <span data-ttu-id="bb416-171">Esta funcionalidad requiere Windows Internet Explorer 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="bb416-171">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 




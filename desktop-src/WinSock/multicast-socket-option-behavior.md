---
description: En esta página se describe el comportamiento de las opciones de socket de multidifusión en función de los distintos Estados de configuración de opciones de socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamiento de la opción de socket de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082116"
---
# <a name="multicast-socket-option-behavior"></a><span data-ttu-id="7aac9-103">Comportamiento de la opción de socket de multidifusión</span><span class="sxs-lookup"><span data-stu-id="7aac9-103">Multicast Socket Option Behavior</span></span>

<span data-ttu-id="7aac9-104">En esta página se describe el comportamiento de las opciones de socket de multidifusión en función de los distintos Estados de configuración de opciones de socket.</span><span class="sxs-lookup"><span data-stu-id="7aac9-104">This page describes the behavior of multicast socket options based on various socket option settings states.</span></span>

<span data-ttu-id="7aac9-105">Por ejemplo, en esta página se describe el comportamiento cuando \_ \_ se establece la opción de socket de pertenencia de origen de adición \_ de IP en un socket para el que ya se ha establecido la opción de pertenencia a un origen de código IP \_ \_ \_ con el par de grupo/origen especificado en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-105">For example, this page describes the behavior when the IP\_ADD\_SOURCE\_MEMBERSHIP socket option is set on a socket for which the IP\_ADD\_SOURCE\_MEMBERSHIP option has already been set with the specified group/source pair on the same network interface.</span></span> <span data-ttu-id="7aac9-106">Se permite llamar a \_ \_ la pertenencia al origen de la adición de IP \_ en el mismo grupo en una interfaz de red diferente.</span><span class="sxs-lookup"><span data-stu-id="7aac9-106">It is permitted to call IP\_ADD\_SOURCE\_MEMBERSHIP on the same group on a different network interface.</span></span>

<span data-ttu-id="7aac9-107">Esta página ayuda a diseñar y solucionar problemas de aplicaciones de multidifusión de Windows Sockets correctamente.</span><span class="sxs-lookup"><span data-stu-id="7aac9-107">This page assists in properly designing and troubleshooting Windows Sockets multicast applications.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7aac9-108">Opción de socket inicial</span><span class="sxs-lookup"><span data-stu-id="7aac9-108">Initial socket option</span></span></th>
<th><span data-ttu-id="7aac9-109">Opción de socket subsiguiente en conflicto</span><span class="sxs-lookup"><span data-stu-id="7aac9-109">Conflicting subsequent socket option</span></span></th>
<th><span data-ttu-id="7aac9-110">Error devuelto</span><span class="sxs-lookup"><span data-stu-id="7aac9-110">Error returned</span></span></th>
<th><span data-ttu-id="7aac9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7aac9-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="7aac9-112">IP_ADD_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7aac9-112">IP_ADD_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7aac9-113">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-113">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-114">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="7aac9-114">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="7aac9-115">No llame a IP_ADD_MEMBERSHIP con el mismo grupo más de una vez en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-115">Do not call IP_ADD_MEMBERSHIP with the same group more than once on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aac9-116">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-116">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-117">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="7aac9-117">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="7aac9-118">No llame a IP_ADD_SOURCE_MEMBERSHIP con el mismo grupo previamente llamado con IP_ADD_MEMBERSHIP en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-118">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group previously called with IP_ADD_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7aac9-119">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-119">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-120">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="7aac9-120">WSAEINVAL</span></span></td>
<td><span data-ttu-id="7aac9-121">En su lugar, use IP_BLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="7aac9-121">Use IP_BLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7aac9-122">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="7aac9-122">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="7aac9-123">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="7aac9-123">WSAEINVAL</span></span></td>
<td><span data-ttu-id="7aac9-124">Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-124">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7aac9-125">IP_DROP_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-125">IP_DROP_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-126">Cualquier llamada posterior en el mismo grupo o grupo/origen</span><span class="sxs-lookup"><span data-stu-id="7aac9-126">Any subsequent call on the same group or group/source pair</span></span></td>
<td><span data-ttu-id="7aac9-127">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="7aac9-127">WSAEINVAL</span></span></td>
<td><span data-ttu-id="7aac9-128">La realización de llamadas a opciones de socket en un par de grupo o grupo/origen no se encuentra actualmente en la lista de inclusión (debido a la eliminación de la pertenencia, o de otro modo) produce un error.</span><span class="sxs-lookup"><span data-stu-id="7aac9-128">Making socket option calls on a group or group/source pair not currently in the inclusion list (due to dropping membership, or otherwise) results in an error.</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="7aac9-129">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7aac9-129">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7aac9-130">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-130">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-131">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="7aac9-131">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="7aac9-132">No llame a IP_ADD_MEMBERSHIP con el mismo grupo previamente llamado con IP_ADD_SOURCE_MEMBERSHIP en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-132">Do not call IP_ADD_MEMBERSHIP with the same group previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aac9-133">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-133">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-134">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="7aac9-134">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="7aac9-135">No llame a IP_ADD_SOURCE_MEMBERSHIP con el mismo par de grupo/origen llamado previamente con IP_ADD_SOURCE_MEMBERSHIP en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-135">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group/source pair previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7aac9-136">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="7aac9-136">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="7aac9-137">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="7aac9-137">WSAEINVAL</span></span></td>
<td><span data-ttu-id="7aac9-138">Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-138">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7aac9-139">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7aac9-139">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7aac9-140">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="7aac9-140">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="7aac9-141">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="7aac9-141">WSAEINVAL</span></span></td>
<td><span data-ttu-id="7aac9-142">Devuelve un error al intentar desbloquear un par de grupo/origen que no se ha bloqueado previamente en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-142">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aac9-143">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-143">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-144">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="7aac9-144">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="7aac9-145">Devuelve un error al intentar quitar un par de grupo/origen que no está en la lista de inclusión de la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-145">Returns an error when attempting to drop a group/source pair that is not in the inclusion list on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="7aac9-146">IP_BLOCK_SOURCE $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="7aac9-146">IP_BLOCK_SOURCE${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7aac9-147">IP_BLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="7aac9-147">IP_BLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="7aac9-148">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="7aac9-148">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="7aac9-149">Devuelve un error al intentar bloquear un par de grupo/origen que ya está bloqueado en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-149">Returns an error when attempting to block a group/source pair that is already blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aac9-150">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-150">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-151">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="7aac9-151">WSAEINVAL</span></span></td>
<td><span data-ttu-id="7aac9-152">En su lugar, use IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="7aac9-152">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7aac9-153">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="7aac9-153">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="7aac9-154">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="7aac9-154">WSAEINVAL</span></span></td>
<td><span data-ttu-id="7aac9-155">En su lugar, use IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="7aac9-155">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7aac9-156">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="7aac9-156">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="7aac9-157">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="7aac9-157">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="7aac9-158">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="7aac9-158">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="7aac9-159">Devuelve un error al intentar desbloquear un par de grupo/origen que no está en la lista de bloqueados en la misma interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7aac9-159">Returns an error when attempting to unblock a group/source pair that is not in the blocked list on the same network interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




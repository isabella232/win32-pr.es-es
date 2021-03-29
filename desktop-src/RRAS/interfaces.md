---
title: Interfaces RAS
description: Una interfaz representa una red a la que se puede tener acceso a través de un adaptador de LAN o WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103904318"
---
# <a name="ras-interfaces"></a><span data-ttu-id="ad63a-103">Interfaces RAS</span><span class="sxs-lookup"><span data-stu-id="ad63a-103">RAS interfaces</span></span>

<span data-ttu-id="ad63a-104">Una interfaz representa una red a la que se puede tener acceso a través de un adaptador de LAN o WAN.</span><span class="sxs-lookup"><span data-stu-id="ad63a-104">An interface represents a network that can be reached over a LAN or WAN adapter.</span></span> <span data-ttu-id="ad63a-105">Cada interfaz tiene un identificador único en el enrutador.</span><span class="sxs-lookup"><span data-stu-id="ad63a-105">Each interface has a unique identifier on the router.</span></span> <span data-ttu-id="ad63a-106">Las interfaces que están activas tienen un adaptador que proporciona conectividad a la red que representan.</span><span class="sxs-lookup"><span data-stu-id="ad63a-106">Interfaces that are active have an adapter that is providing connectivity to the network they represent.</span></span> <span data-ttu-id="ad63a-107">Las interfaces que están inactivas no tienen un adaptador que proporcione conectividad, a menos que un administrador deshabilite la interfaz después de que ya tenga un adaptador.</span><span class="sxs-lookup"><span data-stu-id="ad63a-107">Interfaces that are inactive do not have an adapter providing connectivity, unless an administrator disabled the interface after it already had an adapter.</span></span>

<span data-ttu-id="ad63a-108">El enrutamiento de un paquete a una red representada por una interfaz hará que el enrutador asigne un adaptador para esa interfaz y establezca una conexión WAN a la red remota.</span><span class="sxs-lookup"><span data-stu-id="ad63a-108">Routing a packet to a network represented by an interface will cause the router to allocate an adapter for that interface, and establish a WAN connection to the remote network.</span></span> <span data-ttu-id="ad63a-109">La asignación de un adaptador a una interfaz se conoce como *enlace*.</span><span class="sxs-lookup"><span data-stu-id="ad63a-109">Allocating an adapter to an interface is referred to as *binding*.</span></span>

<span data-ttu-id="ad63a-110">Las interfaces son objetos administrables.</span><span class="sxs-lookup"><span data-stu-id="ad63a-110">Interfaces are manageable objects.</span></span> <span data-ttu-id="ad63a-111">Cada interfaz aparece como una fila en la tabla de la interfaz de la MIB de SNMP adecuada.</span><span class="sxs-lookup"><span data-stu-id="ad63a-111">Each interface appears as a row in the Interface Table of the appropriate SNMP MIB.</span></span>
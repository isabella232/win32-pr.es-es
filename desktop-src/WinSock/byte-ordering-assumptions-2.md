---
description: Sockaddr estructuras y suposiciones de orden de bytes en Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Suposiciones de orden de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705659"
---
# <a name="byte-ordering-assumptions"></a><span data-ttu-id="2302a-103">Suposiciones de orden de bytes</span><span class="sxs-lookup"><span data-stu-id="2302a-103">Byte Ordering Assumptions</span></span>

<span data-ttu-id="2302a-104">Un proveedor de servicios debe tratar todos los componentes de [**sockaddr**](sockaddr-2.md) exclusivos del parámetro de la familia de direcciones como si estuvieran en el orden de bytes de la red, y el parámetro de la familia de direcciones como en el orden de bytes del equipo local.</span><span class="sxs-lookup"><span data-stu-id="2302a-104">A service provider should treat all [**sockaddr**](sockaddr-2.md) components exclusive of the address family parameter as if they are in the network byte order, and the address family parameter as in the local computer's byte order.</span></span> <span data-ttu-id="2302a-105">Es responsabilidad de la aplicación Winsock asegurarse de que las direcciones contenidas en las estructuras **sockaddr** están organizadas correctamente.</span><span class="sxs-lookup"><span data-stu-id="2302a-105">It is the Winsock application's responsibility to make sure that addresses contained in **sockaddr** structures are properly arranged.</span></span> <span data-ttu-id="2302a-106">La API de Winsock proporciona varias rutinas de conversión para simplificar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="2302a-106">The Winsock API provides a number of conversion routines to simplify this task.</span></span> <span data-ttu-id="2302a-107">Actualmente, estas rutinas comprenden la conversión entre el orden de bytes natural del host local y el orden de bytes de red big-endian o Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="2302a-107">Currently these routines understand conversion between the local host's natural byte order and either big-Endian or little-Endian network byte ordering.</span></span> <span data-ttu-id="2302a-108">La arquitectura de Winsock puede admitir otros esquemas de ordenación de bytes en el futuro.</span><span class="sxs-lookup"><span data-stu-id="2302a-108">The Winsock architecture can support other byte ordering schemes in the future.</span></span>

 

 




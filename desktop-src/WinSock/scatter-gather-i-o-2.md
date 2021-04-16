---
description: Las funciones WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg y WSASendTo toman una matriz de búferes de la aplicación como parámetros de entrada y se pueden usar para la e/s de dispersión y recopilación (o vectoriales).
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: E/s de dispersión y recopilación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706185"
---
# <a name="scattergather-io"></a><span data-ttu-id="6b9d0-103">E/s de dispersión y recopilación</span><span class="sxs-lookup"><span data-stu-id="6b9d0-103">Scatter/Gather I/O</span></span>

<span data-ttu-id="6b9d0-104">Las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)y [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) toman una matriz de búferes de aplicación como parámetros de entrada y se pueden usar para la e/s de dispersión y recopilación (o vector).</span><span class="sxs-lookup"><span data-stu-id="6b9d0-104">The [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) functions all take an array of application buffers as input parameters and can be used for scatter/gather (or vectored) I/O.</span></span> <span data-ttu-id="6b9d0-105">Esto puede ser muy útil en las instancias en las que las partes de cada mensaje que se transmiten se componen de uno o varios componentes de encabezado de longitud fija además del cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b9d0-105">This can be very useful in instances where portions of each message being transmitted consist of one or more fixed-length header components in addition to the message body.</span></span> <span data-ttu-id="6b9d0-106">Estos componentes de encabezado no se deben concatenar por la aplicación en un solo búfer contiguo antes del envío.</span><span class="sxs-lookup"><span data-stu-id="6b9d0-106">Such header components need not be concatenated by the application into a single contiguous buffer prior to sending.</span></span> <span data-ttu-id="6b9d0-107">Del mismo modo, al recibir, los componentes del encabezado se pueden dividir automáticamente en búferes independientes, lo que se mantiene por sí mismo en el cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b9d0-107">Likewise on receiving, the header components can be automatically split off into separate buffers, leaving the message body by itself.</span></span>

<span data-ttu-id="6b9d0-108">Al recibir en varios búferes, la finalización se produce cuando los datos llegan de la red, independientemente de si se usan todos los búferes proporcionados.</span><span class="sxs-lookup"><span data-stu-id="6b9d0-108">When receiving into multiple buffers, completion occurs as data arrives from the network, regardless of whether all the supplied buffers are utilized.</span></span>

 

 

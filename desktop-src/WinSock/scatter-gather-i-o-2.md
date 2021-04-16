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
# <a name="scattergather-io"></a>E/s de dispersión y recopilación

Las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)y [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) toman una matriz de búferes de aplicación como parámetros de entrada y se pueden usar para la e/s de dispersión y recopilación (o vector). Esto puede ser muy útil en las instancias en las que las partes de cada mensaje que se transmiten se componen de uno o varios componentes de encabezado de longitud fija además del cuerpo del mensaje. Estos componentes de encabezado no se deben concatenar por la aplicación en un solo búfer contiguo antes del envío. Del mismo modo, al recibir, los componentes del encabezado se pueden dividir automáticamente en búferes independientes, lo que se mantiene por sí mismo en el cuerpo del mensaje.

Al recibir en varios búferes, la finalización se produce cuando los datos llegan de la red, independientemente de si se usan todos los búferes proporcionados.

 

 

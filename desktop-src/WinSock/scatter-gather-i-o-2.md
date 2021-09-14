---
description: Las funciones WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg y WSASendTo toman una matriz de búferes de aplicación como parámetros de entrada y se pueden usar para la E/S de dispersión/recopilación (o vectorización).
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: E/S de dispersión/recopilación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063969"
---
# <a name="scattergather-io"></a>E/S de dispersión/recopilación

Las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)y [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) toman una matriz de búferes de aplicación como parámetros de entrada y se pueden usar para la dispersión o recopilación (o vectorización) de E/S. Esto puede ser muy útil en instancias en las que las partes de cada mensaje que se transmiten constan de uno o varios componentes de encabezado de longitud fija además del cuerpo del mensaje. La aplicación no debe concatenar estos componentes de encabezado en un solo búfer contiguo antes del envío. Del mismo modo, al recibir, los componentes de encabezado se pueden dividir automáticamente en búferes independientes, dejando el cuerpo del mensaje por sí mismo.

Cuando se recibe en varios búferes, la finalización se produce a medida que llegan datos de la red, independientemente de si se usan todos los búferes proporcionados.

 

 

---
description: Las funciones WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg y WSASendTo toman una matriz de búferes de aplicación como parámetros de entrada y se pueden usar para la dispersión y recopilación (o vectorización) de E/S.
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: E/S de dispersión/recopilación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4dc580065655c2d69485a49cd41919345c566c32ec2ff9cd1055383853c7438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794685"
---
# <a name="scattergather-io"></a>E/S de dispersión/recopilación

Las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)y [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) toman una matriz de búferes de aplicación como parámetros de entrada y se pueden usar para la dispersión y recopilación (o vectorización) de E/S. Esto puede ser muy útil en instancias en las que las partes de cada mensaje que se transmiten constan de uno o varios componentes de encabezado de longitud fija además del cuerpo del mensaje. La aplicación no debe concatenar estos componentes de encabezado en un solo búfer contiguo antes de enviarlos. Del mismo modo, al recibir, los componentes de encabezado se pueden dividir automáticamente en búferes independientes, dejando el cuerpo del mensaje por sí mismo.

Al recibir en varios búferes, la finalización se produce cuando llegan datos de la red, independientemente de si se usan todos los búferes proporcionados.

 

 

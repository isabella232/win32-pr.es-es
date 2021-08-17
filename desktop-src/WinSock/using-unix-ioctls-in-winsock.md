---
description: El comando SIOCGIFCONF proporcionado por la mayoría de las implementaciones UNIX se admite en forma de funciones WSAIoctl y WSPIoctl con el comando SIO \_ GET \_ INTERFACE \_ LIST. Este comando devuelve la lista de interfaces configuradas y sus parámetros.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Uso UNIX Ioctls en Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da517adb6480a1bd20100a3d9a6d0896f544c1b541ce547a0f76e5c88aa24210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558867"
---
# <a name="using-unix-ioctls-in-winsock"></a>Uso UNIX Ioctls en Winsock

El comando **SIOCGIFCONF** proporcionado por la mayoría de las implementaciones UNIX se admite en forma de funciones [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) y [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) con el comando **SIO \_ GET INTERFACE \_ \_ LIST**. Este comando devuelve la lista de interfaces configuradas y sus parámetros.

> [!Note]  
> La compatibilidad con este comando es obligatoria para los Windows de servicio TCP/IP compatibles con Sockets 2.

 

El parámetro *lpvOutBuffer* apunta al búfer en el que [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) y [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) almacenan la información sobre las interfaces. El número de interfaces (número de estructuras devueltas en *lpvOutBuffer)* se puede determinar en función de la longitud real del búfer de salida devuelto en *lpcbBytesReturned.*

 

 

---
description: El comando SIOCGIFCONF proporcionado por la mayoría de las implementaciones de UNIX es compatible con la forma de las funciones WSAIoctl y WSPIoctl con el comando SIO \_ Get \_ interface \_ List. Este comando devuelve la lista de interfaces configuradas y sus parámetros.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Usar ioctl de UNIX en Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697256"
---
# <a name="using-unix-ioctls-in-winsock"></a>Usar ioctl de UNIX en Winsock

El comando **SIOCGIFCONF** proporcionado por la mayoría de las implementaciones de Unix es compatible con la forma de las funciones [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) y [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) con el comando **SiO \_ Get \_ interface \_ List**. Este comando devuelve la lista de interfaces configuradas y sus parámetros.

> [!Note]  
> La compatibilidad de este comando es obligatoria para los proveedores de servicios TCP/IP compatibles con Windows Sockets 2.

 

El parámetro *lpvOutBuffer* apunta al búfer en el que [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) y [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) almacenan la información sobre las interfaces. El número de interfaces (el número de estructuras devueltas en *lpvOutBuffer*) se puede determinar en función de la longitud real del búfer de salida devuelto en *lpcbBytesReturned*.

 

 

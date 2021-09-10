---
title: Obtención de las funcionalidades del controlador
description: Obtención de las funcionalidades del controlador
ms.assetid: 761886db-b2e5-449c-b526-6e992cc1b42f
keywords:
- nids,drivers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b9f4d54e80dc589a4c730ef891d8f0bd132e52
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371162"
---
# <a name="getting-the-driver-capabilities"></a>Obtención de las funcionalidades del controlador

En el ejemplo siguiente se [**usagetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) [**ygetGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) para determinar si los servicios de Emergencia están disponibles y si hay un puerto conectado a uno de los puertos.


```C++
JOYINFO joyinfo; 
UINT wNumDevs, wDeviceID; 
BOOL bDev1Attached, bDev2Attached; 
 
    if((wNumDevs = joyGetNumDevs()) == 0) 
        return ERR_NODRIVER; 
    bDev1Attached = joyGetPos(JOYSTICKID1,&joyinfo) != JOYERR_UNPLUGGED; 
    bDev2Attached = wNumDevs == 2 && joyGetPos(JOYSTICKID2,&joyinfo) != 
        JOYERR_UNPLUGGED; 
    if(bDev1Attached || bDev2Attached)   // decide which joystick to use 
        wDeviceID = bDev1Attached ? JOYSTICKID1 : JOYSTICKID2; 
    else 
        return ERR_NODEVICE; 

```



 

 
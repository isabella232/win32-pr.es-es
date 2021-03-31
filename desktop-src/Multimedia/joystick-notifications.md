---
title: Notificaciones de joystick
description: Notificaciones de joystick
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- joysticks, notificaciones
- joysticks, mensajes
- joysticks capturados
- joysticks desconectados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077712"
---
# <a name="joystick-notifications"></a>Notificaciones de joystick

Puede capturar mensajes de joystick directos para enviarlos a una función mediante la función [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) . Solo una aplicación a la vez puede capturar mensajes de un joystick, pero puede consultar el joystick desde otra aplicación mediante la función [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) o [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

> [!Note]  
> Un mensaje de joystick puede no llegar a la aplicación que capturó el joystick si una segunda aplicación utiliza **joyGetPos** o **joyGetPosEx** para consultar el joystick aproximadamente al mismo tiempo que se envía el mensaje. En este caso, la segunda aplicación podría interceptar el mensaje.

 

Si desea capturar mensajes de dos joysticks conectados al sistema, utilice [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) dos veces, una para cada joystick. La ventana recibe mensajes independientes y distintos para cada dispositivo.

Puede liberar un joystick capturado mediante la función [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) . Si una aplicación no libera el joystick antes de finalizar, el joystick se liberará automáticamente poco después de que se destruya la ventana de captura.

No se puede capturar un joystick desconectado. La función **joySetCapture** devuelve JOYERR \_ unenchufado si el dispositivo especificado está desconectado.

 

 
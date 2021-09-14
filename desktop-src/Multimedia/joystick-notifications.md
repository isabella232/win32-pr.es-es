---
title: Notificaciones de notificación de notificación
description: Notificaciones de notificación de notificación
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- así como notificaciones
- y, por último, mensajes
- capturó los contrabandos
- interruptores desconectados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246194"
---
# <a name="joystick-notifications"></a>Notificaciones de notificación de notificación

Puede capturar mensajes de mensajes de mensajes de mensajes directos que se enviarán a una función mediante la [**función soapSetCapture.**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) Solo una aplicación a la vez puede capturar mensajes de un grupo, pero puede consultar el objeto desde otra aplicación mediante la [**funcióngetGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) [**ogetPosEx.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex)

> [!Note]  
> Un mensaje de sms puede no llegar a la aplicación que capturó el paquete si una segunda aplicación **usagetPos** **ogetGetPosEx** para consultar el paquete aproximadamente al mismo tiempo que se envía el mensaje. En este caso, la segunda aplicación podría interceptar el mensaje.

 

Si desea capturar mensajes de dos dispositivos conectados al sistema, use el método [**de captura de**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) datos de dos veces, una vez para cada uno de ellos. La ventana recibe mensajes independientes y distintos para cada dispositivo.

Puede liberar un objeto capture mediante la [**función de releaseCapture.**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) Si una aplicación no libera el yerba antes de finalizar, este se libera automáticamente poco después de que se destruye la ventana de captura.

No se puede capturar un interruptor desconectado. La **funciónvoluciónsetCapture** devuelve \_ ELECONJUNTO DE TOR SI el dispositivo especificado está desconectado.

 

 
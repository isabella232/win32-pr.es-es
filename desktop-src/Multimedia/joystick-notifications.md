---
title: Notificaciones de notificación de notificación
description: Notificaciones de notificación de notificación
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- y, por último, notificaciones
- sms, mensajes
- capturó los contrabandos
- adaptadores desconectados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86666645a4589d1ecd638b81541aab2954839ca08889ef567b69f4abda17d211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140336"
---
# <a name="joystick-notifications"></a>Notificaciones de notificación de notificación

Puede capturar mensajes de mensajes de mensajes directos que se enviarán a una función mediante la [**función fuesetCapture.**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) Solo una aplicación a la vez puede capturar mensajes de un país, pero puede consultar el objeto desde otra aplicación mediante la [**funcióngetGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) [**ogetPosEx.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex)

> [!Note]  
> Un mensaje de mensaje de mensaje no puede llegar a la aplicación que capturó el objeto si una segunda aplicación usa **fuepoGetPos** **ogetPosEx** para consultar el destino aproximadamente al mismo tiempo que se envía el mensaje. En este caso, la segunda aplicación podría interceptar el mensaje.

 

Si desea capturar mensajes de dos velocidades conectadas al sistema, use [**hasta dos veces,**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) una vez para cada uno. La ventana recibe mensajes independientes y distintos para cada dispositivo.

Puede liberar un objeto capture mediante la [**función de releaseCapture.**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) Si una aplicación no libera el objeto antes de finalizar, se libera automáticamente poco después de que se destruya la ventana de captura.

No se puede capturar un resalte desconectado. La **funciónnchSetCapture** devuelve UNPLUGGED de DRAGERR \_ si el dispositivo especificado está desconectado.

 

 
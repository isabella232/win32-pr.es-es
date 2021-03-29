---
title: Notificaciones de Event-Based
description: Notificaciones de Event-Based
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- joysticks, notificaciones
- joysticks, mensajes
- joysticks, notificaciones basadas en eventos
- joysticks, umbral de movimiento
- notificaciones de joystick basadas en eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789999"
---
# <a name="event-based-notifications"></a>Notificaciones de Event-Based

Puede pedir al sistema que envíe mensajes de joystick a una aplicación cada vez que la posición del eje del joystick cambie con un valor mayor que el *umbral de movimiento* del dispositivo. El umbral de movimiento es la distancia a la que se debe mover el joystick antes de que se envíe un mensaje de cambio de posición de joystick a una ventana que haya capturado el dispositivo. Para obtener más información, [**consulte \_ mm JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), mm [**\_ JOY2MOVE**](mm-joy2move.md)o [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).

El umbral es inicialmente cero. Puede establecer el umbral de movimiento mediante la función [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) . Puede recuperar la frecuencia de sondeo mínima del joystick mediante la función [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .

 

 
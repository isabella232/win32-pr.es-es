---
title: Event-Based notificaciones
description: Event-Based notificaciones
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- y, por último, notificaciones
- sms, mensajes
- y notificaciones basadas en eventos
- eras, umbral de movimiento
- notificaciones de notificación basadas en eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372229"
---
# <a name="event-based-notifications"></a>Event-Based notificaciones

Puede pedir al sistema que envíe mensajes de mensajes de mensaje a una aplicación cada vez que cambie la posición de un eje de eje de axis por un valor mayor que el umbral *de* movimiento del dispositivo. El umbral de movimiento es la distancia a la que se debe mover el coche antes de que se envíe un mensaje de cambio de posición a una ventana que ha capturado el dispositivo. Para obtener más información, [**vea \_ MMMOV1MOVE,**](mm-joy1move.md) [**MM \_ MMMUT1ZMOVE,**](mm-joy1zmove.md) [**MM MM \_ MMMUT2MOVE**](mm-joy2move.md)o [**\_ MMMUT2ZMOVE**](mm-joy2zmove.md).

El umbral es inicialmente cero. Puede establecer el umbral de movimiento mediante la [**función fuesetThreshold.**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) Puede recuperar la frecuencia de sondeo mínima del intervalo mediante la [**funcióngetDevCaps.**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)

 

 
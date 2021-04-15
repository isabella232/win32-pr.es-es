---
title: Mensajes de notificación de joystick
description: Mensajes de notificación de joystick
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- joysticks, notificaciones
- joysticks, mensajes
- joysticks, posición
- joysticks, botones
- Mensajes de MM_JOY1
- Mensajes de MM_JOY2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676131"
---
# <a name="joystick-notification-messages"></a>Mensajes de notificación de joystick

Los mensajes de joystick notifican a la aplicación que un joystick ha cambiado de posición o que uno de sus botones ha cambiado de estado. Los mensajes que comienzan con MM \_ JOY1 se envían a la función si la aplicación solicita entradas del joystick mediante el identificador JOYSTICKID1 y \_ se envían mensajes JOY2 de mm si la aplicación solicita entradas del joystick mediante el identificador JOYSTICKID2.

Los mensajes de la tabla siguiente identifican el estado de los botones del joystick:



| Message                                         | Descripción                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**MM \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md) | Se presionó un botón en el joystick JOYSTICKID1.              |
| [**MM \_ JOY1BUTTONUP**](mm-joy1buttonup.md)     | Se ha lanzado un botón en el joystick JOYSTICKID1.             |
| [**MM \_ JOY1MOVE**](mm-joy1move.md)             | El joystick JOYSTICKID1 ha cambiado la posición en la dirección x o y. |
| [**MM \_ JOY1ZMOVE**](mm-joy1zmove.md)           | El joystick JOYSTICKID1 ha cambiado la posición en la dirección z.       |
| [**MM \_ JOY2BUTTONDOWN**](mm-joy2buttondown.md) | Se presionó un botón en el joystick JOYSTICKID2.              |
| [**MM \_ JOY2BUTTONUP**](mm-joy2buttonup.md)     | Se ha lanzado un botón en el joystick JOYSTICKID2.             |
| [**MM \_ JOY2MOVE**](mm-joy2move.md)             | El joystick JOYSTICKID2 ha cambiado la posición en la dirección x o y  |
| [**MM \_ JOY2ZMOVE**](mm-joy2zmove.md)           | El joystick JOYSTICKID2 ha cambiado la posición en la dirección z.       |



 

Todos los mensajes informan de los botones inexistentes como liberados.

 

 





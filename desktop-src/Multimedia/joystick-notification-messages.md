---
title: Mensajes de notificación de notificación de notificaciones de notificaciones
description: Mensajes de notificación de notificación de notificaciones de notificaciones
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- y, por último, notificaciones
- sms, mensajes
- ', posición'
- controles, botones
- MM_JOY1 mensajes
- MM_JOY2 mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246206"
---
# <a name="joystick-notification-messages"></a>Mensajes de notificación de notificación de notificaciones de notificaciones

Los mensajes de texto notifican a la aplicación que un móvil ha cambiado de posición o que uno de sus botones ha cambiado de estado. Los mensajes que comienzan por MM SOAP1 se envían a la función si la aplicación solicita la entrada del dispositivo mediante el identificador DEID1 y se envían mensajes MMIJO2 si la aplicación solicita la entrada del objeto mediante el identificador \_ \_ DEID2.

Los mensajes de la tabla siguiente identifican el estado de los botones de botones de botones:



| Message                                         | Descripción                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**MM \_ MM MM1BUTTONDOWN**](mm-joy1buttondown.md) | Se ha presionado un botón en el botón CTRLID1.              |
| [**MM \_ MM MM1BUTTONUP**](mm-joy1buttonup.md)     | Se ha publicado un botón en el botón DEID1.             |
| [**MM \_ MM MM1MOVE**](mm-joy1move.md)             | Se cambió la posición de la posición en dirección x o y. |
| [**MM \_ MM1ZMOVE**](mm-joy1zmove.md)           | Se cambió la posición de la dirección Z en Sentido Z.       |
| [**MM \_ MM MM2BUTTONDOWN**](mm-joy2buttondown.md) | Se ha presionado un botón en el botón CTRLID2.              |
| [**MM \_ MM MM2BUTTONUP**](mm-joy2buttonup.md)     | Se ha publicado un botón en el botón DEID2.             |
| [**MM \_ MM MM2MOVE**](mm-joy2move.md)             | Se cambió la posición en dirección x o y de Sentido del sentido de la izquierda a izquierda  |
| [**MM \_ MM2ZMOVE**](mm-joy2zmove.md)           | Se cambió la posición de la dirección Z en Sentido Z.       |



 

Todos los mensajes informan de botones inexistentes como liberados.

 

 





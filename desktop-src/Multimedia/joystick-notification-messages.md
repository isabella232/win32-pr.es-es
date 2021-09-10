---
title: Mensajes de notificación de notificación de notificaciones de notificación
description: Mensajes de notificación de notificación de notificaciones de notificación
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- así como notificaciones
- y, por último, mensajes
- ', posición'
- así como botones
- MM_JOY1 mensajes
- MM_JOY2 mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372283"
---
# <a name="joystick-notification-messages"></a>Mensajes de notificación de notificación de notificaciones de notificación

Los mensajes de texto notifican a la aplicación que un ha cambiado de posición o que uno de sus botones ha cambiado de estado. Los mensajes que comienzan por MM SOAP1 se envían a la función si la aplicación solicita la entrada del objeto mediante el identificador DESID1 y los mensajes MMIJO2 se envían si la aplicación solicita la entrada desde el panel mediante el identificador \_ \_ SOAPID2.

Los mensajes de la tabla siguiente identifican el estado de los botones de botones de botones de botones:



| Message                                         | Descripción                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [**\_MMBUTTON1BUTTONDOWN**](mm-joy1buttondown.md) | Se ha presionado un botón en el botón CTRLID1.              |
| [**MM \_ MMMIENTO1BUTTONUP**](mm-joy1buttonup.md)     | Se ha publicado un botón en el botón DESID1.             |
| [**MM \_ MM1MOVE**](mm-joy1move.md)             | Se cambió la posición de la dirección X o Y de La izquierda a izquierda. |
| [**\_MMMUT1ZMOVE**](mm-joy1zmove.md)           | Se cambió la posición de la dirección Z de La 1.       |
| [**\_MMIJO2BUTTONDOWN**](mm-joy2buttondown.md) | Se ha presionado un botón en el botón CTRLID2.              |
| [**\_MMIJO2BUTTONUP**](mm-joy2buttonup.md)     | Se ha publicado un botón en el botón DESID2.             |
| [**\_MMIJO2MOVE**](mm-joy2move.md)             | Se cambió la posición de Desuso DEID2 en la dirección x o y  |
| [**\_MMIJO2ZMOVE**](mm-joy2zmove.md)           | Se cambió la posición en la dirección Z.       |



 

Todos los mensajes informan de botones inexistentes como publicados.

 

 





---
description: El MSP de conferencia IP implementa varias interfaces específicas del proveedor para el control de participantes. Estas interfaces se exponen en el objeto de llamada, si este MSP está asociado a la llamada.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: IPConf MSP Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d740ffad9cbb10df64599914234a1b6db97f3829e70d055958290ae55935ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061053"
---
# <a name="ipconf-msp-interfaces"></a>IPConf MSP Interfaces

\[Las interfaces MSP de IPConf no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El MSP de conferencia IP implementa varias interfaces específicas del proveedor para el control de participantes. Estas interfaces se exponen en el objeto de llamada, si este MSP está asociado a la llamada.

Las [**interfaces ITParticipantEvent**](itparticipantevent.md) [**e IEnumParticipant**](ienumparticipant.md) son objetos independientes y se enumeran aquí por comodidad de referencia.



| Interfaz                                            | Descripción                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMulticastControl**](imulticastcontrol.md)       | Permite que una aplicación establezca y obtenga el modo de bucle recuperación [**(MULTICAST \_ LOOPBACK \_ MODE)**](multicast-loopback-mode.md)para un objeto de conferencia de multidifusión. |
| [**ITParticipant**](itparticipant.md)               | Permite que una aplicación recupere información sobre los participantes de la conferencia y obtenga punteros a las secuencias asociadas a esos participantes.             |
| [**ITParticipantControl**](itparticipantcontrol.md) | Permite que una aplicación recupere punteros a los participantes en una conferencia.                                                                           |
| [**ITParticipantEvent**](itparticipantevent.md)     | Permite que una aplicación recupere información de eventos relativa a un participante de la conferencia.                                                                  |
| [**IEnumParticipant**](ienumparticipant.md)         | Enumera [**ITParticipant.**](itparticipant.md)                                                                                                        |



 

 

 




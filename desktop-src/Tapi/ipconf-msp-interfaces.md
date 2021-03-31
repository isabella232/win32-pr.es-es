---
description: El MSP de conferencias IP implementa varias interfaces específicas del proveedor para el control del participante. Estas interfaces se exponen en el objeto de llamada si este MSP está asociado a la llamada.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Interfaces de IPConf MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155889"
---
# <a name="ipconf-msp-interfaces"></a>Interfaces de IPConf MSP

\[ Las interfaces IPConf MSP no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El MSP de conferencias IP implementa varias interfaces específicas del proveedor para el control del participante. Estas interfaces se exponen en el objeto de llamada si este MSP está asociado a la llamada.

Las interfaces [**ITParticipantEvent**](itparticipantevent.md) y [**IEnumParticipant**](ienumparticipant.md) son objetos independientes y se enumeran aquí para mayor comodidad de referencia.



| Interfaz                                            | Descripción                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMulticastControl**](imulticastcontrol.md)       | Permite a una aplicación establecer y obtener el modo de bucle invertido ( [**\_ \_ modo de bucle invertido de multidifusión**](multicast-loopback-mode.md)) para un objeto de conferencia de multidifusión. |
| [**ITParticipant**](itparticipant.md)               | Permite a una aplicación recuperar información sobre los participantes de la Conferencia y obtener punteros a las secuencias asociadas a esos participantes.             |
| [**ITParticipantControl**](itparticipantcontrol.md) | Permite que una aplicación recupere punteros a los participantes de una conferencia.                                                                           |
| [**ITParticipantEvent**](itparticipantevent.md)     | Permite que una aplicación recupere información de eventos relativa a un participante de la Conferencia.                                                                  |
| [**IEnumParticipant**](ienumparticipant.md)         | Enumera [**ITParticipant**](itparticipant.md).                                                                                                        |



 

 

 




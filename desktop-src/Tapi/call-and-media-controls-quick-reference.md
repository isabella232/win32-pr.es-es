---
description: En la tabla siguiente se enumeran las interfaces COM de TAPI versión 3 por Categoría en orden de importancia.
ms.assetid: fafb6d6e-934e-4942-8b90-dacb7ba09752
title: Referencia rápida de los controles de llamada y multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ed3105612205d6d516b8d0c5e4f0a7bf9719b3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689636"
---
# <a name="call-and-media-controls-quick-reference"></a>Referencia rápida de los controles de llamada y multimedia

\[ Las [interfaces IPCONF MSP](ipconf-msp-interfaces.md) no están disponibles para su uso en Windows Vista, windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

En la tabla siguiente se enumeran las interfaces COM de TAPI versión 3 por Categoría en orden de importancia. Las interfaces se agrupan de acuerdo con los cinco objetos básicos de control de llamadas de TAPI 3: TAPI, dirección, terminal, llamada y CallHub. Las interfaces restantes se agrupan de acuerdo con las interfaces de distribución automática de llamadas (ACD), que proporcionan funcionalidad del centro de llamadas. interfaces de enumerador y objetos independientes.



| Agrupaciones de interfaces                                          | Descripción                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaces de objeto TAPI](tapi-object-interfaces.md)         | El objeto TAPI es el objeto principal de TAPI 3.                                                                                                                                                                                                              |
| [Interfaces del objeto Address](address-object-interfaces.md)   | El objeto Address representa una entidad que puede realizar o recibir llamadas. Las interfaces y los métodos asociados permiten a una aplicación obtener y establecer información relacionada con la dirección, por ejemplo, si tiene compatibilidad con el identificador del llamador.                             |
| [Interfaces de objetos de terminal](terminal-object-interfaces.md) | El objeto terminal representa el receptor o el origen en la terminación o punto de origen de una llamada. Las interfaces y los métodos asociados permiten a una aplicación obtener y establecer información relacionada con el terminal, como, por ejemplo, si está actualmente en uso. |
| [Llamar a interfaces de objeto](call-object-interfaces.md)         | El objeto Call representa una llamada y se crea cuando se produce una llamada. Las interfaces y los métodos asociados obtienen y establecen información relacionada con la llamada, como el estado de la llamada actual.                                                           |
| [Interfaces de objetos de teléfono](phone-object-interfaces.md)       | El objeto Phone es la entidad que representa el dispositivo de teléfono real y todos sus controles.                                                                                                                                                             |
| [Interfaces de IPConf MSP](ipconf-msp-interfaces.md)           | El MSP de conferencias IP implementa varias interfaces para el control de participantes que se exponen en el objeto de llamada.                                                                                                                                          |
| [Interfaces del objeto CallHub](callhub-object-interfaces.md)   | El objeto CallHub representa una vista de terceros de una llamada de varias entidades. Las interfaces y los métodos asociados obtienen y establecen información relativa a la llamada, como, por ejemplo, si el centro de llamadas está activo.                                                          |
| [Interfaces de enumerador](enumerator-interfaces.md)           | Interfaces de enumerador estándar de COM.                                                                                                                                                                                                                         |
| [Interfaces de eventos](./event-interfaces.md)            | Las interfaces de eventos también se muestran con sus objetos o agrupaciones de funciones.                                                                                                                                                                                |
| [Objetos independientes](stand-alone-objects.md)               | Los distintos objetos independientes de TAPI 3 proporcionan interfaces y métodos para operaciones como telefonía asistida o control de eventos.                                                                                                                    |



 

 

 

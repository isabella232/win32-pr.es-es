---
description: En la tabla siguiente se enumeran las interfaces COM de TAPI versión 3 por categoría en orden de importancia.
ms.assetid: fafb6d6e-934e-4942-8b90-dacb7ba09752
title: Referencia rápida de los controles de llamadas y medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9985f88997e454a05838f0dec499d9036fb114e3e89ea543619c8359d1a03d8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948267"
---
# <a name="call-and-media-controls-quick-reference"></a>Referencia rápida de los controles de llamadas y medios

\[Las [interfaces MSP de IPConf](ipconf-msp-interfaces.md) no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

En la tabla siguiente se enumeran las interfaces COM de TAPI versión 3 por categoría en orden de importancia. Las interfaces se agrupan según los cinco objetos de control de llamadas básicos de TAPI 3: TAPI, Address, Terminal, Call y CallHub. Las interfaces restantes se agrupan según las interfaces de distribución automática de llamadas (ACD), que proporcionan funcionalidad de centro de llamadas. interfaces de enumerador y objetos independientes.



| Agrupaciones de interfaz                                          | Descripción                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaces de objetos TAPI](tapi-object-interfaces.md)         | El objeto TAPI es el objeto principal de TAPI 3.                                                                                                                                                                                                              |
| [Interfaces de objeto de dirección](address-object-interfaces.md)   | El objeto Address representa una entidad que puede realizar o recibir llamadas. Las interfaces y los métodos asociados permiten a una aplicación obtener y establecer información sobre la dirección, por ejemplo, si tiene compatibilidad con el identificador de autor de la llamada.                             |
| [Interfaces de objetos de terminal](terminal-object-interfaces.md) | El objeto Terminal representa el receptor o el origen en el punto de finalización u origen de una llamada. Las interfaces y métodos asociados permiten a una aplicación obtener y establecer información sobre el terminal, por ejemplo, si está actualmente en uso. |
| [Llamar a interfaces de objeto](call-object-interfaces.md)         | El objeto Call representa una llamada y se crea cuando existe una llamada. Las interfaces y métodos asociados obtienen y establecen información relacionada con la llamada, como el estado de la llamada actual.                                                           |
| [Teléfono Interfaces de objeto](phone-object-interfaces.md)       | El Teléfono es la entidad que representa el dispositivo telefónico real y todos sus controles.                                                                                                                                                             |
| [IPConf MSP Interfaces](ipconf-msp-interfaces.md)           | El MSP de conferencia IP implementa varias interfaces para el control de participantes que se exponen en el objeto de llamada.                                                                                                                                          |
| [Interfaces de objetos CallHub](callhub-object-interfaces.md)   | El objeto CallHub representa una vista de terceros de una llamada a varios usuarios. Las interfaces y métodos asociados obtienen y establecen información relacionada con la llamada, como si el centro de llamadas está activo.                                                          |
| [Interfaces de enumerador](enumerator-interfaces.md)           | Interfaces de enumerador estándar COM.                                                                                                                                                                                                                         |
| [Interfaces de eventos](./event-interfaces.md)            | Las interfaces de eventos también se muestran con sus agrupaciones de objetos o funciones.                                                                                                                                                                                |
| [Objetos independientes](stand-alone-objects.md)               | Los objetos independientes varios de TAPI 3 proporcionan interfaces y métodos para operaciones como la telefonía asistida o el control de eventos.                                                                                                                    |



 

 

 

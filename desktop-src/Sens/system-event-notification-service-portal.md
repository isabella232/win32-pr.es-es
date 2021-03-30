---
description: Supervise las notificaciones de eventos del sistema de los programas que se ejecutan en equipos móviles para determinar el ancho de banda y la latencia de conexión de red. Escriba aplicaciones optimizadas para la informática móvil y LAN de alta latencia.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Servicio de notificación de eventos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002661"
---
# <a name="system-event-notification-service"></a>Servicio de notificación de eventos del sistema

## <a name="purpose"></a>Propósito

Las aplicaciones diseñadas para su uso por parte de usuarios móviles requieren un conjunto único de funciones de conectividad y notificaciones. En el pasado, las aplicaciones individuales eran necesarias para implementar estas características internamente. El servicio de notificación de eventos del sistema (SENS) ahora proporciona estas funcionalidades en el sistema operativo, creando una interfaz de notificación y conectividad uniforme para las aplicaciones. El uso de los desarrolladores de SENS puede determinar el ancho de banda de conexión y la información de latencia dentro de su aplicación y optimizar el funcionamiento de la aplicación en función de esas condiciones.

## <a name="where-applicable"></a>Donde sea aplicable

Las funciones de conectividad y las notificaciones de SENS son útiles para las aplicaciones escritas para equipos móviles o equipos conectados a redes de área local de latencia alta.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Este documento está destinado a los desarrolladores de software que desarrollan aplicaciones para la informática móvil y redes de área local de latencia alta. En este documento se proporciona una referencia completa de todas las partes del servicio de notificación de eventos del sistema, incluido el objeto SENS y los métodos auxiliares.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Requiere Microsoft Windows XP o posterior. Para obtener información acerca de los sistemas operativos necesarios para usar una interfaz o función determinada, consulte la sección de requisitos de la documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                              | Descripción                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Información general](about-system-event-notification-service.md)<br/> | Información general sobre el servicio de notificación de eventos del sistema.<br/>               |
| [Referencia](sens-reference.md)<br/>                         | Documentación de los métodos e interfaces del servicio de notificación de eventos del sistema.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IEventSubscription**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 

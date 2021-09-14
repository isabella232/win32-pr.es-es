---
description: El servicio de notificación de eventos del sistema permite a las aplicaciones móviles recibir notificaciones de eventos del sistema que SUPERVISA SENS. Cuando se produce el evento solicitado, SENS notifica a la aplicación.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notificaciones (Servicio de notificación de eventos del sistema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073577"
---
# <a name="notifications-system-event-notification-service"></a>Notificaciones (Servicio de notificación de eventos del sistema)

El servicio de notificación de eventos del sistema permite a las aplicaciones móviles recibir notificaciones de eventos del sistema que SUPERVISA SENS. Cuando se produce el evento solicitado, SENS notifica a la aplicación.

SENS puede notificar a las aplicaciones sobre tres clases de eventos del sistema:

-   Eventos de red TCP/IP, como el estado de una conexión de red TCP/IP o la calidad de la conexión.
-   Eventos de inicio de sesión de usuario.
-   Eventos de batería y alimentación de CA.

Por ejemplo, una aplicación puede suscribirse a cualquiera de los siguientes eventos del sistema:

-   Establecimiento de conectividad de red
-   Notificación cuando se puede alcanzar un destino especificado dentro de los parámetros de calidad de conexión (QOC) especificados
-   El equipo ha cambiado a la energía de la batería.
-   El porcentaje de energía restante de la batería está dentro de un parámetro especificado.
-   Se producen eventos programados mediante Synchronization Manager

**Windows Server 2008 R2 y Windows 7:** El suscriptor tiene un máximo de 3 minutos para responder a una notificación en las [**interfaces ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) e [**ISensLogon2.**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) Después de 3 minutos, SENS cancela la llamada a los suscriptores y desbloquea el subproceso de notificación. Si se requiere una operación larga para responder a la notificación, vuelva de **ISensLogon** o **ISensLogon2** lo antes posible y abra otro subproceso para su procesamiento.

 

 




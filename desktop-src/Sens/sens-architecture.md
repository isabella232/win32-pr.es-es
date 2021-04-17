---
description: El servicio de notificación de eventos del sistema funciona con el sistema de eventos COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Arquitectura de SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668306"
---
# <a name="sens-architecture"></a>Arquitectura de SENS

El servicio de notificación de eventos del sistema funciona con el sistema de eventos COM+. SENS es un publicador de eventos para las clases de eventos que supervisa: eventos de red, Inicio de sesión y energía/batería. La aplicación que recibe una notificación se denomina suscriptor de eventos.

Cuando una aplicación se suscribe para recibir notificaciones, también puede especificar filtros asociados a los eventos suscritos. SENS y los eventos COM+ usan los filtros para determinar más cuando se debe notificar a la aplicación.

Las notificaciones son asincrónicas, por lo que no es necesario que la aplicación que recibe la notificación esté activa cuando se envía la notificación. Cuando una aplicación se suscribe para recibir notificaciones, puede especificar si se debe activar cuando se produce el evento o cuando se le notifica posteriormente cuando está activo.

La suscripción solo puede ser transitoria y válida hasta que la aplicación deje de ejecutarse, o bien puede ser persistente y válida hasta que la aplicación se quite del sistema.

Un almacén de datos de eventos COM+ contiene información sobre el publicador de eventos (SENS), los suscriptores de eventos y los filtros. SENS también Predefine una interfaz de salida para cada clase de evento en una biblioteca de tipos.



| Clase de evento    | GUID                          | Interfaz    |
|----------------|-------------------------------|--------------|
| Eventos de red | red de SENSGUID \_ EVENTCLASS \_ | ISensNetwork |
| Eventos de inicio de sesión   | Inicio de sesión de SENSGUID \_ EVENTCLASS \_   | ISensLogon   |
| Eventos de energía   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

Para recibir notificaciones de cualquiera de estos eventos, la aplicación debe hacer dos cosas:

-   Suscríbase a los eventos de SENS que le interesen. Para suscribirse a un evento, use las interfaces **IEventSubscription** y **IEVENTSYSTEM** en eventos com+. Debe proporcionar un identificador para las clases de eventos y el identificador del publicador SENS, SENSGUID \_ Publisher. Las suscripciones se encuentran en un nivel de evento, por lo que la aplicación de suscripción también debe especificar qué eventos de la clase son de interés. Cada evento corresponde a un método de la interfaz correspondiente a su clase de eventos.
-   Cree un objeto de receptor con una implementación para cada interfaz que controla. Vea [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)y [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) para obtener más información acerca de estas interfaces y los eventos que se admiten en cada una de ellas.

Cuando se produce uno de los eventos supervisados, SENS procesa cada suscripción con cualquier filtro asociado y notifica a los suscriptores a través del sistema de eventos COM+.

 

 




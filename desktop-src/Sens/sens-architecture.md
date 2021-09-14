---
description: El servicio de notificación de eventos del sistema funciona con el sistema de eventos COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Arquitectura de SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073578"
---
# <a name="sens-architecture"></a>Arquitectura de SENS

El servicio de notificación de eventos del sistema funciona con el sistema de eventos COM+. SENS es un publicador de eventos para las clases de eventos que supervisa: eventos de red, inicio de sesión y alimentación/batería. La aplicación que recibe una notificación se denomina suscriptor de eventos.

Cuando una aplicación se suscribe para recibir notificaciones, también puede especificar filtros asociados a los eventos suscritos. Los eventos SENS y COM+ usan los filtros para determinar aún más cuándo se debe notificar a la aplicación.

Las notificaciones son asincrónicas, por lo que la aplicación que recibe la notificación no tiene que estar activa cuando se envía la notificación. Cuando una aplicación se suscribe para recibir notificaciones, puede especificar si se debe activar cuando se produce el evento o si se notifica más adelante cuando está activa.

La suscripción solo puede ser transitoria y válida hasta que la aplicación deje de ejecutarse, o puede ser persistente y válida hasta que la aplicación se quite del sistema.

Un almacén de datos de eventos COM+ contiene información sobre el publicador de eventos (SENS), los suscriptores de eventos y los filtros. SENS también predefine una interfaz saliente para cada clase de eventos en una biblioteca de tipos.



| Clase de evento    | GUID                          | Interfaz    |
|----------------|-------------------------------|--------------|
| Eventos de red | SENSGUID \_ EVENTCLASS \_ NETWORK | ISensNetwork |
| Eventos de inicio de sesión   | SENSGUID \_ EVENTCLASS \_ LOGON   | ISensLogon   |
| Eventos de energía   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

Para recibir notificaciones de cualquiera de estos eventos, la aplicación debe hacer dos cosas:

-   Suscríbase a los eventos SENS que le interesen. Para suscribirse a un evento, use las interfaces **IEventSubscription** **e IEventSystem** en eventos COM+. Debe proporcionar un identificador para las clases de eventos y el identificador del publicador SENS, SENSGUID \_ PUBLISHER. Las suscripciones se encuentran en un nivel por evento, por lo que la aplicación de suscripción también debe especificar qué eventos dentro de la clase son de interés. Cada evento corresponde a un método de la interfaz correspondiente a su clase de eventos.
-   Cree un objeto receptor con una implementación para cada interfaz que controle. Vea [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)e [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) para obtener más información sobre estas interfaces y los eventos admitidos en cada una de ellas.

Cuando se produce uno de los eventos supervisados, SENS procesa cada suscripción con los filtros asociados y notifica a los suscriptores a través del sistema de eventos COM+.

 

 




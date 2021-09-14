---
title: Información general sobre eventos de UI Automation
description: La notificación Automatización de la interfaz de usuario eventos de Microsoft es una característica clave para las tecnologías de asistencia, como lectores de pantalla y lupas de pantalla.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- Automatización de la interfaz de usuario,información general sobre eventos
- Automatización de la interfaz de usuario,categorías de eventos
- Automatización de la interfaz de usuario,notificaciones de eventos
- notificaciones de eventos
- events,categories
- events,event notifications
- Eventos de cambio de propiedad
- Eventos de acción de elemento
- Eventos de cambio de estructura
- Eventos de cambio de escritorio global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070523"
---
# <a name="ui-automation-events-overview"></a>Información general sobre eventos de UI Automation

La notificación Automatización de la interfaz de usuario eventos de Microsoft es una característica clave para las tecnologías de asistencia, como lectores de pantalla y lupas de pantalla. Estos Automatización de la interfaz de usuario realiza un seguimiento de los eventos que los proveedores de Automatización de la interfaz de usuario genera cuando sucede algo en la interfaz de usuario y usan la información para notificar a los usuarios finales.

La eficacias se mejora gracias a que las aplicaciones proveedoras son capaces de generar los eventos de manera selectiva (en función de si hay clientes suscritos a esos eventos) o de no generarlos en absoluto (si no hay clientes a la escucha de eventos).

Los eventos de Automatización de la interfaz de usuario pueden clasificarse de la siguiente manera.



| Categoría de eventos        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cambio de propiedad       | Se genera cuando cambia una propiedad Automatización de la interfaz de usuario elemento o patrón de control. Por ejemplo, si un cliente necesita supervisar un control de casilla de aplicación, puede registrarse para escuchar un evento de cambio de propiedad en la propiedad [**IUIAutomationTogglePattern::CurrentToggleState.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) Cuando el control de casilla se activa o desactiva, el proveedor genera el evento y el cliente puede actuar según sea necesario. |
| Acción de elemento        | Se produce cuando un cambio en la interfaz de usuario es el resultado de una actividad de programación o usuario final, por ejemplo, cuando se hace clic en un botón o se invoca mediante [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).                                                                                                                                                                                                                                                     |
| Cambio de estructura      | Se genera cuando cambia la estructura del Automatización de la interfaz de usuario de datos. La estructura cambia cuando se hacen visibles, ocultan o quitan elementos nuevos de la interfaz de usuario en el escritorio.                                                                                                                                                                                                                                                                                                              |
| Cambio de escritorio global | Se genera cuando se producen acciones de interés global para el cliente, por ejemplo, cuando el foco cambia de un elemento a otro o cuando se cierra una ventana.                                                                                                                                                                                                                                                                                                                      |
| Notification          | Se genera cuando una aplicación llama a [**la función UiaRaiseNotificationEvent.**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indica el tipo de notificación.                                                                                                                                                                                                                                                 |



 

Algunos eventos no implican necesariamente un cambio en el estado de la UI. Por ejemplo, si el usuario ficha a un campo de entrada de texto y, a continuación, hace clic en un botón para actualizar el campo, se genera un evento [**\_ \_ TextChangedEventId de UIA,**](uiauto-event-ids.md) incluso si el usuario no ha cambiado realmente el texto. Al procesar un evento, puede ser necesario que la aplicación cliente compruebe si realmente se ha producido un cambio antes de realizar cualquier acción.

Los siguientes eventos se pueden generar incluso si no cambia el estado de la UI.

-   [**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (dependiendo de la propiedad que haya cambiado)
-   [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)
-   [**Selección de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md)
-   [**Texto de UIA \_ \_ TextChangedEventId**](uiauto-event-ids.md)

Para obtener una descripción de todos Automatización de la interfaz de usuario eventos, vea [Identificadores de eventos](uiauto-event-ids.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suscribirse a Automatización de la interfaz de usuario eventos](uiauto-eventsforclients.md)
</dt> </dl>

 

 
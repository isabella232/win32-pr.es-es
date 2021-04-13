---
title: Información general sobre eventos de UI Automation
description: La notificación de eventos de automatización de la interfaz de usuario de Microsoft es una característica clave para las tecnologías de asistencia, como los lectores de pantalla y los ampliadores de pantalla.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- Automatización de la interfaz de usuario, información general sobre eventos
- Automatización de la interfaz de usuario, categorías de eventos
- Automatización de la interfaz de usuario, notificaciones de eventos
- notificaciones de eventos
- eventos, categorías
- eventos, notificaciones de eventos
- Eventos de cambio de propiedad
- Eventos de acción de elemento
- Eventos de cambio de estructura
- Eventos de cambio de escritorio global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359020"
---
# <a name="ui-automation-events-overview"></a>Información general sobre eventos de UI Automation

La notificación de eventos de automatización de la interfaz de usuario de Microsoft es una característica clave para las tecnologías de asistencia, como los lectores de pantalla y los ampliadores de pantalla. Estos clientes de automatización de la interfaz de usuario realizan el seguimiento de los eventos generados por los proveedores de UI Automation cuando sucede algo en la interfaz de usuario y usan la información para notificar a los usuarios finales.

La eficacias se mejora gracias a que las aplicaciones proveedoras son capaces de generar los eventos de manera selectiva (en función de si hay clientes suscritos a esos eventos) o de no generarlos en absoluto (si no hay clientes a la escucha de eventos).

Los eventos de Automatización de la interfaz de usuario pueden clasificarse de la siguiente manera.



| Categoría de eventos        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cambio de propiedad       | Se genera cuando cambia una propiedad en el patrón de control o elemento de automatización de la interfaz de usuario. Por ejemplo, si un cliente necesita supervisar un control de casilla de la aplicación, se puede registrar para escuchar un evento de cambio de propiedad en la propiedad [**IUIAutomationTogglePattern:: CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) . Cuando el control de casilla se activa o desactiva, el proveedor genera el evento y el cliente puede actuar según sea necesario. |
| Acción de elemento        | Se genera cuando se produce un cambio en la interfaz de usuario de la actividad de usuario final o de programación, por ejemplo, cuando se hace clic en un botón o se invoca a través de [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).                                                                                                                                                                                                                                                     |
| Cambio de estructura      | Se genera cuando cambia la estructura del árbol de automatización de la interfaz de usuario. La estructura cambia cuando se hacen visibles, ocultan o quitan elementos nuevos de la interfaz de usuario en el escritorio.                                                                                                                                                                                                                                                                                                              |
| Cambio de escritorio global | Se genera cuando se producen acciones de interés global para el cliente, por ejemplo, cuando el foco cambia de un elemento a otro o cuando se cierra una ventana.                                                                                                                                                                                                                                                                                                                      |
| notificación          | Se genera cuando una aplicación llama a la función [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) . [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indica el tipo de notificación.                                                                                                                                                                                                                                                 |



 

Algunos eventos no implican necesariamente un cambio en el estado de la UI. Por ejemplo, si el usuario realiza una pestaña en un campo de entrada de texto y, a continuación, hace clic en un botón para actualizar el campo, se genera un evento de [**\_ \_ TextChangedEventId de texto UIA**](uiauto-event-ids.md) , aunque el usuario no haya cambiado realmente el texto. Al procesar un evento, puede ser necesario que la aplicación cliente compruebe si realmente se ha producido un cambio antes de realizar cualquier acción.

Los siguientes eventos se pueden generar incluso si no cambia el estado de la UI.

-   [**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (dependiendo de la propiedad que ha cambiado)
-   [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)
-   [**\_InvalidatedEventId de selección de UIA \_**](uiauto-event-ids.md)
-   [**\_TextChangedEventId de texto de UIA \_**](uiauto-event-ids.md)

Para obtener una descripción de todos los eventos de automatización de la interfaz de usuario, vea [identificadores de eventos](uiauto-event-ids.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suscribirse a eventos de UI Automation](uiauto-eventsforclients.md)
</dt> </dl>

 

 
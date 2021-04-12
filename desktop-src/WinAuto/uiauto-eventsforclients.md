---
title: Suscribirse a eventos de UI Automation
description: La automatización de la interfaz de usuario de Microsoft permite a los clientes suscribirse a eventos de interés. Esta funcionalidad mejora el rendimiento al eliminar la necesidad de sondear continuamente los elementos de la interfaz de usuario del sistema para ver si ha cambiado la información, la estructura o el estado.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- clientes, eventos de UI Automation
- clientes, eventos para la automatización de la interfaz de usuario
- Automatización de la interfaz de usuario, eventos para clientes
- Automatización de la interfaz de usuario, eventos de cliente
- Automatización de la interfaz de usuario, suscribirse a eventos
- Automatización de la interfaz de usuario, métodos de suscripción
- Automatización de la interfaz de usuario, ejemplos de código
- Automatización de la interfaz de usuario, ejemplos
- Automatización de la interfaz de usuario, ejemplos
- suscribirse a eventos de automatización de la interfaz de usuario
- eventos, suscripción de UI Automation
- Ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a89df1b9d2afc401e07b6cd77d1307d912f11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357193"
---
# <a name="subscribing-to-ui-automation-events"></a>Suscribirse a eventos de UI Automation

La automatización de la interfaz de usuario de Microsoft permite a los clientes suscribirse a eventos de interés. Esta funcionalidad mejora el rendimiento al eliminar la necesidad de sondear continuamente los elementos de la interfaz de usuario del sistema para ver si ha cambiado la información, la estructura o el estado.

La eficacia también mejora gracias a la capacidad para realizar escuchas de eventos que solo se encuentran dentro de un ámbito definido. Por ejemplo, un cliente puede escuchar los cambios de selección en un elemento de una lista, en la propia lista o en todo un cuadro de diálogo.

> [!Note]  
> No asuma que un proveedor de automatización de la interfaz de usuario genera todos los posibles eventos. Por ejemplo, no todos los cambios de propiedad hacen que los proveedores de proxy estándar generen eventos para los controles de Windows Forms y Microsoft Win32.

 

Para obtener una vista más amplia de los eventos de automatización de la interfaz de usuario, consulte [UI Automation Events Overview](uiauto-eventsoverview.md).

> [!Note]  
> Antes de implementar un controlador de eventos, debe estar familiarizado con los problemas de subprocesamiento descritos en Descripción de los [problemas de subprocesos](uiauto-threading.md).

 

En este tema se incluyen las siguientes secciones.

-   [Registrar controladores de eventos](#registering-event-handlers)
-   [Ejemplos](#examples)
-   [Temas relacionados](#related-topics)

## <a name="registering-event-handlers"></a>Registrar controladores de eventos

Las aplicaciones cliente se suscriben a eventos de un tipo determinado mediante el registro de un controlador de eventos, mediante uno de los siguientes métodos [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) .



| Método de suscripción                                                                                                                                                                                                | Tipo de evento       | Interfaz de devolución de llamada                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Cambio de foco     | [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Cambio de propiedad  | [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Cambio de estructura | [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | notificación     | [**IUIAutomationNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Otros eventos     | [**IUIAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Cuando un cliente agrega un controlador de eventos para todos los descendientes ([**\_ descendientes de TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)), la automatización de la interfaz de usuario solo agrega un controlador para la raíz del subárbol y el controlador realiza escuchas en todos los descendientes. La automatización de la interfaz de usuario no agrega controladores de eventos de forma recursiva.

Cuando un cliente llama al método [**IUIAutomation:: RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) , la automatización de la interfaz de usuario quita todos los controladores de eventos del proceso del cliente.

Para recibir y controlar eventos, implemente un objeto de control de eventos que exponga una interfaz de devolución de llamada y debe registrar el objeto llamando a un método de registro de eventos como [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler). La interfaz de devolución de llamada tiene un único método; La automatización de la interfaz de usuario llama a este método cuando se procesa el evento.

Al apagar o cuando los eventos de UI Automation ya no son de interés para la aplicación, los clientes de automatización de la interfaz de usuario deben llamar a uno o varios de los siguientes métodos de [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) .

> [!Note]  
> Un cliente de UI Automation no debe utilizar varios subprocesos para agregar o quitar controladores de eventos. Un comportamiento inesperado puede producirse si se agrega o se quita un controlador de eventos mientras se agrega o quita otro en el mismo proceso de cliente.

 



| Método                                                                                                | Descripción                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Anula el registro de un controlador de eventos que se registró mediante [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler).                                                                                                                                  |
| [**RemoveFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Anula el registro de un controlador de eventos que se registró mediante [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler).                                                                                                                              |
| [**RemovePropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Anula el registro de un controlador de eventos que se registró mediante [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray). |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Anula el registro de un controlador de eventos que se registró mediante [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler).                                                                                                                      |
| [**RemoveNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Anula el registro de un controlador de eventos que Weas registrado con [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler).                                                                                                                            |
| [**RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Anula el registro de todos los controladores de eventos registrados.                                                                                                                                                                                                                                      |



 

Es posible que se entregue un evento en un controlador de eventos después de que se haya anulado la suscripción del controlador, si el evento se recibe simultáneamente con la solicitud para cancelar la suscripción al evento. El procedimiento recomendado es seguir el estándar del modelo de objetos componentes (COM) y evitar destruir el objeto del controlador de eventos hasta que su recuento de referencias llegue a cero. La destrucción de un controlador de eventos inmediatamente después de cancelar la suscripción de los eventos puede producir una infracción de acceso si se entrega un evento tarde.

## <a name="examples"></a>Ejemplos

Para ver ejemplos de código que muestran cómo controlar eventos de automatización de la interfaz de usuario, consulte [cómo implementar controladores de eventos](uiauto-howto-implement-event-handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Descripción de los problemas de subprocesos](uiauto-threading.md)
</dt> </dl>

 

 





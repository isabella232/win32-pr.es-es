---
title: Suscribirse a Automatización de la interfaz de usuario eventos
description: Microsoft Automatización de la interfaz de usuario permite a los clientes suscribirse a eventos de interés. Esta funcionalidad mejora el rendimiento al eliminar la necesidad de sondear continuamente los elementos de la interfaz de usuario del sistema para ver si ha cambiado alguna información, estructura o estado.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- clients,Automatización de la interfaz de usuario eventos
- clients,events for Automatización de la interfaz de usuario
- Automatización de la interfaz de usuario,events para clientes
- Automatización de la interfaz de usuario,eventos de cliente
- Automatización de la interfaz de usuario, suscribirse a eventos
- Automatización de la interfaz de usuario,métodos de suscripción
- Automatización de la interfaz de usuario,ejemplos de código
- Automatización de la interfaz de usuario,examples
- Automatización de la interfaz de usuario,samples
- suscribirse a eventos de automatización de la interfaz de usuario
- events,Automatización de la interfaz de usuario suscripción
- Ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e8dd4cb2d810ad8423c1fa4f75020a9489ceb72acbe1483cb439e943b5676
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505305"
---
# <a name="subscribing-to-ui-automation-events"></a>Suscribirse a Automatización de la interfaz de usuario eventos

Microsoft Automatización de la interfaz de usuario permite a los clientes suscribirse a eventos de interés. Esta funcionalidad mejora el rendimiento al eliminar la necesidad de sondear continuamente los elementos de la interfaz de usuario del sistema para ver si ha cambiado alguna información, estructura o estado.

La eficacia también mejora gracias a la capacidad para realizar escuchas de eventos que solo se encuentran dentro de un ámbito definido. Por ejemplo, un cliente puede escuchar los cambios de selección en un elemento de una lista, en la propia lista o en un cuadro de diálogo completo.

> [!Note]  
> No suponga que un proveedor de Automatización de la interfaz de usuario genera todos los eventos posibles. Por ejemplo, no todos los cambios de propiedad hacen que los proveedores de proxy estándar deban generar eventos para Windows Forms y controles de Microsoft Win32.

 

Para obtener una vista más amplia de Automatización de la interfaz de usuario eventos, [vea información general sobre Automatización de la interfaz de usuario eventos.](uiauto-eventsoverview.md)

> [!Note]  
> Antes de implementar un controlador de eventos, debe estar familiarizado con los problemas de subprocesos descritos en Descripción de los [problemas de subprocesamiento.](uiauto-threading.md)

 

En este tema se incluyen las siguientes secciones.

-   [Registro de controladores de eventos](#registering-event-handlers)
-   [Ejemplos](#examples)
-   [Temas relacionados](#related-topics)

## <a name="registering-event-handlers"></a>Registro de controladores de eventos

Las aplicaciones cliente se suscriben a eventos de un tipo determinado mediante el registro de un controlador de eventos, mediante uno de los métodos [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) siguientes.



| Método de suscripción                                                                                                                                                                                                | Tipo de evento       | Interfaz de devolución de llamada                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Cambio de foco     | [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Cambio de propiedad  | [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Cambio de estructura | [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | Notificación     | [**IUIAutomationNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Otros eventos     | [**IUIAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Cuando un cliente agrega un controlador de eventos para todos los [**\_ descendientes (Descendientes de TreeScope),**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)Automatización de la interfaz de usuario agrega solo un controlador para la raíz del subárver y el controlador escucha en todos los descendientes. Automatización de la interfaz de usuario no agrega controladores de eventos de forma recursiva.

Cuando un cliente llama al método [**IUIAutomation::RemoveAllEventHandlers,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) Automatización de la interfaz de usuario quita todos los controladores de eventos del proceso de cliente.

Para recibir y controlar eventos, implemente un objeto de control de eventos que exponga una interfaz de devolución de llamada y debe registrar el objeto llamando a un método de registro de eventos como [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler). La interfaz de devolución de llamada tiene un único método; Automatización de la interfaz de usuario llama a este método cuando se procesa el evento.

Al cerrar o cuando los Automatización de la interfaz de usuario ya no son de interés para la aplicación, Automatización de la interfaz de usuario clientes deben llamar a uno o varios de los métodos [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) siguientes.

> [!Note]  
> Un Automatización de la interfaz de usuario cliente no debe usar varios subprocesos para agregar o quitar controladores de eventos. Un comportamiento inesperado puede producirse si se agrega o quita un controlador de eventos mientras se agrega o quita otro en el mismo proceso de cliente.

 



| Método                                                                                                | Descripción                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Anula el registro de un controlador de eventos que se registró mediante [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler).                                                                                                                                  |
| [**RemoveFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Anula el registro de un controlador de eventos que se registró mediante [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler).                                                                                                                              |
| [**RemovePropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Anula el registro de un controlador de eventos registrado mediante [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray). |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Anula el registro de un controlador de eventos que se registró mediante [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler).                                                                                                                      |
| [**RemoveNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Anula el registro de un controlador de eventos registrado mediante [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler).                                                                                                                            |
| [**RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Anula el registro de todos los controladores de eventos registrados.                                                                                                                                                                                                                                      |



 

Es posible que un evento se entregue a un controlador de eventos después de cancelar la suscripción del controlador, si el evento se recibe simultáneamente con la solicitud para cancelar la suscripción del evento. El procedimiento recomendado es seguir el estándar modelo de objetos componentes (COM) y evitar destruir el objeto de controlador de eventos hasta que su recuento de referencias haya alcanzado cero. Destruir un controlador de eventos inmediatamente después de cancelar la suscripción de eventos puede producir una infracción de acceso si un evento se entrega tarde.

## <a name="examples"></a>Ejemplos

Para obtener ejemplos de código que muestran cómo controlar Automatización de la interfaz de usuario eventos, vea [How to Implement Event Handlers](uiauto-howto-implement-event-handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Descripción de los problemas de subprocesamiento](uiauto-threading.md)
</dt> </dl>

 

 





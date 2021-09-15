---
title: Invocar patrón de control
description: Describe las directrices y convenciones para implementar IInvokeProvider, incluida la información sobre los métodos.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Invoke
- Automatización de la interfaz de usuario,Invoke control pattern
- Automatización de la interfaz de usuario,IInvokeProvider
- IInvokeProvider
- implementar patrones Automatización de la interfaz de usuario de control Invoke
- Invocar patrones de control
- patrones de control,IInvokeProvider
- patrones de control, implementar Automatización de la interfaz de usuario Invoke
- patrones de control,Invoke
- interfaces,IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567249"
---
# <a name="invoke-control-pattern"></a>Invocar patrón de control

Describe las directrices y convenciones para implementar [**IInvokeProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)incluida la información sobre los métodos. El **patrón de** control Invoke se usa para admitir controles que no mantienen el estado cuando se activan, sino que inician o realizan una única acción inequívoca.

Los controles que mantienen el estado, como las casillas y los botones de radio, deben implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) e [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectivamente. Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IInvokeProvider**](#required-members-for-iinvokeprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Invoke,** tenga en cuenta las siguientes directrices y convenciones:

-   Los controles [**implementan IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) si el mismo comportamiento no se expone a través de otro proveedor de patrones de control. Por ejemplo, si el método [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) de un control realiza la misma acción que el método [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) o [**Collapse,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) el control no debe implementar **IInvokeProvider**.
-   Generalmente, la invocación de un control se realiza con un clic, un doble clic, presionando la tecla ENTRAR, usando un método abreviado de teclado predefinido o alguna combinación alternativa de pulsaciones de teclas.
-   El **evento Invoke** ([**UIA Invoke \_ \_ InvokedEventId**](uiauto-event-ids.md)) se genera en un control que se ha activado (como respuesta a un control que lleva a cabo su acción asociada). Si es posible, se debe generar el evento después de que el control haya completado la acción y haya hecho la devolución sin bloquearse. El **evento Invoke** (**UIA Invoke \_ \_ InvokedEventId**) debe generarse antes de atender la solicitud **Invoke** en los escenarios siguientes:
    -   No es posible ni práctico esperar hasta que se complete la acción.
    -   La acción requiere la interacción del usuario.
    -   La acción requiere mucho tiempo y provocará que el cliente que llama se bloquee durante un tiempo considerable.
-   Si invocar el control tiene efectos secundarios significativos, estos se deben exponer a través de la **propiedad HelpText.** Por ejemplo, aunque [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) no está asociado a la selección, **Invoke** puede hacer que se seleccione otro control.
-   Los efectos de mantener el puntero (o pasar el mouse sobre) generalmente no constituyen un **evento Invocado.** Sin embargo, los controles que realizan una acción (en lugar de provocar un efecto visual) basados en el estado del puntero deben admitir el patrón de control **Invoke.**
    > [!Note]  
    > Esta implementación se considera un problema de accesibilidad si el control solo se puede invocar como resultado de un efecto secundario relacionado con el mouse.

     

-   La invocación de un control es diferente de la selección de un elemento. No obstante, dependiendo del control, su invocación puede provocar que el elemento se seleccione como un efecto secundario. Por ejemplo, al invocar un Microsoft Word de lista de documentos en la carpeta Mis documentos, se selecciona el elemento y se abre el documento.
-   Un elemento puede desaparecer del árbol de Automatización de la interfaz de usuario microsoft inmediatamente después de ser invocado. La solicitud de información del elemento que proporciona la devolución de llamada de evento puede producir un error como resultado. La solución recomendada es la captura previa de la información almacenada en caché.
-   Los controles pueden implementar varios patrones de control. Por ejemplo, el control **Color de** relleno de la barra Microsoft Excel herramientas implementa los patrones de control Invoke y [ExpandCollapse.](uiauto-implementingexpandcollapse.md) El patrón de control ExpandCollapse expone el menú y el patrón de control **Invoke** rellena la selección activa con el color elegido.

## <a name="required-members-for-iinvokeprovider"></a>Miembros necesarios para **IInvokeProvider**

El método siguiente es necesario para implementar la [**interfaz IInvokeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)



| Miembros requeridos                                | Tipo de miembro | Notas                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Invocar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | Método      | **Invoke** es una llamada asincrónica y debe devolverse inmediatamente sin bloqueo.<br/> Este comportamiento es especialmente importante para los controles que, directa o indirectamente, inician un cuadro de diálogo modal cuando se invocan. Cualquier cliente de Automatización de la interfaz de usuario que haya provocado que el evento permanezca bloqueado hasta que se cierre el cuadro de diálogo modal. <br/> |



 

Este patrón de control no tiene eventos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[**Invoke \_ InvokeEventId de UIA \_**](uiauto-event-ids.md)
</dt> </dl>

 

 






---
title: Window (patrón de control)
description: Describe las directrices y convenciones para implementar IWindowProvider, incluida información sobre propiedades, métodos y eventos. El patrón de control window admite controles que proporcionan la funcionalidad fundamental basada en ventanas dentro de una interfaz gráfica de usuario tradicional.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control window
- Automatización de la interfaz de usuario, patrón de control window
- Automatización de la interfaz de usuario, IWindowProvider
- IWindowProvider
- implementar patrones de control de ventana de automatización de la interfaz de usuario
- Patrones de control de ventanas
- patrones de control, IWindowProvider
- patrones de control, implementar la ventana de automatización de la interfaz de usuario
- patrones de control, ventana
- interfaces, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357708"
---
# <a name="window-control-pattern"></a>Window (patrón de control)

Describe las directrices y convenciones para implementar [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), incluida información sobre propiedades, métodos y eventos. El patrón de control **Window** admite controles que proporcionan la funcionalidad fundamental basada en ventanas dentro de una interfaz gráfica de usuario tradicional.

Entre los ejemplos de controles que deben implementar este patrón de control se incluyen las ventanas de aplicación de nivel superior, las ventanas secundarias de interfaz de múltiples documentos (MDI), los controles de panel de división de tamaño ajustable, los cuadros de diálogo modales y las ventanas de ayuda de globo. Para obtener ejemplos de controles que implementan este patrón de control, vea [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IWindowProvider**](#required-members-for-iwindowprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Window** , tenga en cuenta las siguientes directrices y convenciones:

-   Para admitir la capacidad de modificar el tamaño de la ventana y la posición de la pantalla mediante la automatización de la interfaz de usuario de Microsoft, un control debe implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) además de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Normalmente, los controles que contienen barras de título y elementos de barra de título que permiten que el control se mueva, cambie de tamaño, se maximice, se minimice o se cierren, por lo general, para implementar [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Los controles como los elementos emergentes de información sobre herramientas y las listas desplegables de menús o cuadros combinados no implementan normalmente [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Las ventanas de ayuda de globo se diferencian de los elementos emergentes de información sobre herramientas básicos por el aprovisionamiento de un botón de **cierre** de tipo ventana.
-   El modo de pantalla completa no es compatible con [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) , ya que es específico de la característica de una aplicación y no es un comportamiento de ventana típico.

## <a name="required-members-for-iwindowprovider"></a>Miembros requeridos para **IWindowProvider**

Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) .



| Miembros requeridos                                                                            | Tipo de miembro | Notas                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**WindowInteractionState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | Propiedad    | No se garantiza que sea **WindowInteractionState \_ ReadyForUserInteraction** |
| [**IsModal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | Propiedad    | None                                                                        |
| [**IsTopmost**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | Propiedad    | None                                                                        |
| [**CanMaximize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | Propiedad    | None                                                                        |
| [**CanMinimize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | Propiedad    | None                                                                        |
| [**WindowVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | Propiedad    | None                                                                        |
| [**Cercanos**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | Método      | None                                                                        |
| [**SetVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | Método      | None                                                                        |
| [**WaitForInputIdle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | Método      | None                                                                        |
| [**Ventana de UIA \_ \_ WindowClosedEventId**](uiauto-event-ids.md) | Evento       | None                                                                        |
| [**Ventana de UIA \_ \_ WindowOpenedEventId**](uiauto-event-ids.md) | Evento       | None                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Asignación de patrones de controles para clientes de UI Automation](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





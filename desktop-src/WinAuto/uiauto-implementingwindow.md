---
title: Patrón de control de ventana
description: Describe directrices y convenciones para implementar IWindowProvider, incluida información sobre propiedades, métodos y eventos. El patrón de control Ventana admite controles que proporcionan funcionalidad básica basada en ventanas dentro de una GUI tradicional.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Automatización de la interfaz de usuario,implementing Window control pattern
- Automatización de la interfaz de usuario,patrón de control De ventana
- Automatización de la interfaz de usuario,IWindowProvider
- IWindowProvider
- implementación de Automatización de la interfaz de usuario de control de ventana
- Patrones de control de ventana
- patrones de control, IWindowProvider
- patrones de control, implementar Automatización de la interfaz de usuario ventana
- patrones de control,Ventana
- interfaces,IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242361"
---
# <a name="window-control-pattern"></a>Patrón de control de ventana

Describe directrices y convenciones para implementar [**IWindowProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)incluida información sobre propiedades, métodos y eventos. El **patrón de** control Ventana admite controles que proporcionan funcionalidad básica basada en ventanas dentro de una GUI tradicional.

Algunos ejemplos de controles que deben implementar este patrón de control son las ventanas de aplicación de nivel superior, las ventanas secundarias de la interfaz de múltiples documentos (MDI), los controles de panel dividido que se pueden cambiar de tamaño, los diálogos modales y las ventanas de ayuda de globo. Para obtener ejemplos de controles que implementan este patrón de control, vea [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IWindowProvider**](#required-members-for-iwindowprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Ventana,** tenga en cuenta las siguientes directrices y convenciones:

-   Para admitir la capacidad de modificar el tamaño de la ventana y la posición de la pantalla mediante Microsoft Automatización de la interfaz de usuario, un control debe implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) además de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Los controles que contienen barras de título y elementos de barra de título que permiten mover, cambiar el tamaño, maximizar, minimizar o cerrar el control suelen ser necesarios para implementar [**IWindowProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)
-   Los controles como los elementos emergentes de información sobre herramientas y los menús desplegables de cuadro combinado o menú no suelen implementar [**IWindowProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)
-   Las ventanas de ayuda de globo se diferencian de los elementos emergentes básicos de la información sobre herramientas mediante el aprovisionamiento de un botón Cerrar parecido a **una** ventana.
-   El modo de pantalla completa no es compatible con [**IWindowProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) ya que es específico de la característica de una aplicación y no es un comportamiento típico de la ventana.

## <a name="required-members-for-iwindowprovider"></a>Miembros necesarios para **IWindowProvider**

Las siguientes propiedades, métodos y eventos son necesarios para implementar la [**interfaz IWindowProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)



| Miembros requeridos                                                                            | Tipo de miembro | Notas                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**WindowInteractionState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | Propiedad    | No se garantiza que sea **WindowInteractionState \_ ReadyForUserInteraction** |
| [**IsModal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | Propiedad    | None                                                                        |
| [**IsTopmost**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | Propiedad    | None                                                                        |
| [**CanMaximize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | Propiedad    | None                                                                        |
| [**CanMinimize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | Propiedad    | None                                                                        |
| [**WindowVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | Propiedad    | None                                                                        |
| [**Cerca**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | Método      | None                                                                        |
| [**SetVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | Método      | None                                                                        |
| [**WaitForInputIdle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | Método      | None                                                                        |
| [**Ventana de \_ \_ UIAClosedEventId**](uiauto-event-ids.md) | Evento       | None                                                                        |
| [**Ventana de \_ \_ UIAOpenedEventId**](uiauto-event-ids.md) | Evento       | None                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Asignación de patrones de controles para clientes de UI Automation](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





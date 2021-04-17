---
title: Patrón de control SelectionItem
description: Describe las directrices y convenciones para implementar ISelectionItemProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control SelectionItem
- Automatización de la interfaz de usuario, patrón de control SelectionItem
- Automatización de la interfaz de usuario, ISelectionItemProvider
- ISelectionItemProvider
- implementación de patrones de control SelectionItem de UI Automation
- Patrones de control de SelectionItem
- patrones de control, ISelectionItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario SelectionItem
- patrones de control, SelectionItem
- interfaces, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704581"
---
# <a name="selectionitem-control-pattern"></a>Patrón de control SelectionItem

Describe las directrices y convenciones para implementar [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), incluida información sobre propiedades, métodos y eventos. El patrón de control **SelectionItem** se usa para admitir controles que actúan como elementos secundarios individuales seleccionables de controles de contenedor que implementan [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).

Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **ISelectionItemProvider**](#required-members-for-iselectionitemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **SelectionItem** , tenga en cuenta las siguientes directrices y convenciones:

-   Los controles de selección única que administran los controles secundarios que implementan [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como el control deslizante de **resolución de pantalla** del cuadro de diálogo **propiedades de pantalla** para Windows, deben implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); sus elementos secundarios deben implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) y [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

## <a name="required-members-for-iselectionitemprovider"></a>Miembros requeridos para **ISelectionItemProvider**

Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) .



| Miembros requeridos                                                                                                                        | Tipo de miembro | Notas |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | Método      | None  |
| [**IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | Propiedad    | None  |
| [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | Método      | None  |
| [**Seleccionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | Método      | None  |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | Propiedad    | None  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)         | Evento       | None  |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) | Evento       | None  |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         | Evento       | None  |



 

Si el resultado de una [**selección**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), un [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)o un [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) es un elemento seleccionado único, se debe producir un evento **ElementSelected** ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)); de lo contrario, genere los eventos **ElementAddedToSelection** ([**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)) o **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) según corresponda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





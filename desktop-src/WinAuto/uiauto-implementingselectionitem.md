---
title: Patrón de control SelectionItem
description: Describe directrices y convenciones para implementar ISelectionItemProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control SelectionItem
- Automatización de la interfaz de usuario,patrón de control SelectionItem
- Automatización de la interfaz de usuario,ISelectionItemProvider
- ISelectionItemProvider
- implementación de Automatización de la interfaz de usuario de control SelectionItem
- Patrones de control SelectionItem
- patrones de control,ISelectionItemProvider
- patrones de control, implementar Automatización de la interfaz de usuario SelectionItem
- patrones de control,SelectionItem
- interfaces,ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070482"
---
# <a name="selectionitem-control-pattern"></a>Patrón de control SelectionItem

Describe directrices y convenciones para implementar [**ISelectionItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)incluida información sobre propiedades, métodos y eventos. El patrón de control **SelectionItem** se usa para admitir controles que actúan como elementos secundarios individuales y seleccionables de controles de contenedor que implementan [**ISelectionProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)

Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y Sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ISelectionItemProvider**](#required-members-for-iselectionitemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **SelectionItem,** tenga en cuenta las siguientes directrices y convenciones:

-   Los controles de selección única que administran controles secundarios que implementan  [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como el control deslizante Resolución de pantalla del cuadro de diálogo **Propiedades de pantalla** para Windows, deben implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); sus elementos secundarios deben implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) [**e ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

## <a name="required-members-for-iselectionitemprovider"></a>Miembros necesarios para **ISelectionItemProvider**

Las siguientes propiedades, métodos y eventos son necesarios para implementar la [**interfaz ISelectionItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)



| Miembros requeridos                                                                                                                        | Tipo de miembro | Notas |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | Método      | None  |
| [**IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | Propiedad.    | None  |
| [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | Método      | None  |
| [**Seleccionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | Método      | None  |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | Propiedad.    | None  |
| [**Elemento \_ SelectionItem \_ de UIAAddedToSelectionEventId**](uiauto-event-ids.md)         | Evento       | None  |
| [**Elemento \_ SelectionItem de \_ UIARemovedFromSelectionEventId**](uiauto-event-ids.md) | Evento       | None  |
| [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)                         | Evento       | None  |



 

Si el resultado de [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)o [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) es un elemento seleccionado único, se debe generar un evento **ElementSelected** ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)); de lo contrario, se deben generar eventos **ElementAddedToSelection** ([**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)) o **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId)**](uiauto-event-ids.md)según corresponda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





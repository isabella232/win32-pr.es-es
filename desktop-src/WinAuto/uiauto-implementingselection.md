---
title: Selection (patrón de control)
description: Describe las directrices y convenciones para implementar ISelectionProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Selection
- UI Automation, Selection (patrón de control)
- Automatización de la interfaz de usuario, ISelectionProvider
- ISelectionProvider
- implementar patrones de control de selección de UI Automation
- Patrones de control de selección
- patrones de control, ISelectionProvider
- patrones de control, implementar la selección de automatización de la interfaz de usuario
- patrones de control, selección
- interfaces, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075781"
---
# <a name="selection-control-pattern"></a>Selection (patrón de control)

Describe las directrices y convenciones para implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), incluida información sobre propiedades, métodos y eventos. El patrón de control **Selection** se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios seleccionables. Los elementos secundarios de este elemento deben implementar [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Selection** , tenga en cuenta las siguientes directrices y convenciones:

-   Los controles que implementan [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) permiten la selección de uno o varios elementos secundarios. Por ejemplo, los cuadros de lista, las vistas de lista y las vistas de árbol admiten varias selecciones, mientras que los cuadros combinados, los controles deslizantes y los grupos de botones de radio admiten la selección única.
-   Los controles que tienen un intervalo mínimo, máximo y continuo, como el control deslizante de **volumen** de un reproductor multimedia, deben implementar [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en lugar de [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).
-   Los controles de selección única que administran los controles secundarios que implementan [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como el control deslizante de **resolución de pantalla** del cuadro de diálogo Propiedades de **pantalla** para Windows, o el control de selección **selector de colores** de Microsoft Word (vea la imagen siguiente), deben implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); sus elementos secundarios deben implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) y [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

    ![imagen que muestra un ejemplo de asignación de cadena de muestrario de colores](images/uia-valuepattern-colorpicker.jpg)

-   Los menús no admiten el patrón de control **Selection** . Si está trabajando con elementos de menú que incluyen tanto gráficos como texto (como los elementos del **Panel de vista previa** en el menú **Ver** de Microsoft Outlook) y necesita transmitir el estado, debe implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).

## <a name="required-members-for-iselectionprovider"></a>Miembros requeridos para **ISelectionProvider**

Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .



| Miembros requeridos                                                                                | Tipo de miembro | Notas                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Propiedad    | None                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Propiedad    | None                                                                        |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Método      | None                                                                        |
| [**\_InvalidatedEventId de selección de UIA \_**](uiauto-event-ids.md) | Evento       | Genera este evento cuando una selección de un contenedor ha cambiado significativamente. |



 

Las propiedades [**ISelectionProvider:: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) y [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) pueden ser dinámicas. Por ejemplo, es posible que el estado inicial de un control no tenga elementos seleccionados de forma predeterminada, lo que indica que **IsSelectionRequired** es false. Sin embargo, cuando se haya seleccionado un elemento, el control siempre debe tener al menos un elemento seleccionado. Del mismo modo, en raras ocasiones, un control podría permitir la selección de varios elementos en la inicialización pero solo permitir posteriormente la realización de selecciones únicas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control SelectionItem](uiauto-implementingselectionitem.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





---
title: Patrón de control de selección
description: Describe directrices y convenciones para implementar ISelectionProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Selección
- Automatización de la interfaz de usuario,Patrón de control Selección
- Automatización de la interfaz de usuario,ISelectionProvider
- ISelectionProvider
- implementar patrones de control Automatización de la interfaz de usuario selección de datos
- Patrones de control de selección
- patrones de control,ISelectionProvider
- patrones de control, implementar Automatización de la interfaz de usuario selección
- patrones de control,Selección
- interfaces,ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d0578dcdcfa9d381272afaa474338a54caa1f4b17989f2461f9aec5086bc18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098325"
---
# <a name="selection-control-pattern"></a>Patrón de control de selección

Describe directrices y convenciones para implementar [**ISelectionProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)incluida información sobre propiedades, métodos y eventos. El **patrón de** control Selección se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios seleccionables. Los elementos secundarios de este elemento deben implementar [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Selección,** tenga en cuenta las siguientes directrices y convenciones:

-   Los controles que [**implementan ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) permiten seleccionar uno o varios elementos secundarios. Por ejemplo, los cuadros de lista, las vistas de lista y las vistas de árbol admiten varias selecciones, mientras que los cuadros combinados, los controles deslizantes y los grupos de botones de radio admiten una selección única.
-   Los controles que tienen un intervalo mínimo,  máximo e continuo, como el control deslizante Volumen de un reproductor multimedia, deben implementar [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en lugar de [**ISelectionProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)
-   Los controles de selección única que administran controles secundarios que implementan  [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como el control  deslizante Resolución de pantalla del cuadro de diálogo **Propiedades de pantalla** para Windows o el control de selección Selector de colores de Microsoft Word (vea la imagen siguiente), deben implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); sus elementos secundarios deben implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) [**e ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

    ![imagen que muestra un ejemplo de asignación de cadenas de muestra de color](images/uia-valuepattern-colorpicker.jpg)

-   Los menús no admiten el **patrón de** control Selección. Si está trabajando con elementos de menú que  incluyen gráficos  y texto (como los elementos del panel vista previa del menú Ver de Microsoft Outlook) y necesita transmitir el estado, debe implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).

## <a name="required-members-for-iselectionprovider"></a>Miembros necesarios para **ISelectionProvider**

Las siguientes propiedades, métodos y eventos son necesarios para implementar la [**interfaz ISelectionProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)



| Miembros requeridos                                                                                | Tipo de miembro | Notas                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Propiedad    | Ninguno                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Propiedad    | Ninguno                                                                        |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Método      | Ninguno                                                                        |
| [**UIA \_ Selection \_ InvalidtedEventId**](uiauto-event-ids.md) | Evento       | Generar este evento cuando una selección de un contenedor ha cambiado significativamente. |



 

Las [**propiedades ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) y [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) pueden ser dinámicas. Por ejemplo, el estado inicial de un control podría no tener ningún elemento seleccionado de forma predeterminada, lo que indica que **IsSelectionRequired** es false. Sin embargo, cuando se haya seleccionado un elemento, el control siempre debe tener al menos un elemento seleccionado. Del mismo modo, en raras ocasiones, un control podría permitir la selección de varios elementos en la inicialización pero solo permitir posteriormente la realización de selecciones únicas.

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

 

 





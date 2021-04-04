---
title: Patrón de control ExpandCollapse
description: Describe las directrices y convenciones para implementar IExpandCollapseProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control ExpandCollapse
- Automatización de la interfaz de usuario, patrón de control ExpandCollapse
- Automatización de la interfaz de usuario, IExpandCollapseProvider
- IExpandCollapseProvider
- implementación de patrones de control ExpandCollapse de UI Automation
- Patrones de control de ExpandCollapse
- patrones de control, IExpandCollapseProvider
- patrones de control, implementar la automatización de la interfaz de usuario ExpandCollapse
- patrones de control, ExpandCollapse
- interfaces, IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bd28ddcc201dcff0a4811a1eb8e04670f93091
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075486"
---
# <a name="expandcollapse-control-pattern"></a>Patrón de control ExpandCollapse

Describe las directrices y convenciones para implementar [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), incluida información sobre propiedades, métodos y eventos. El patrón de control **ExpandCollapse** se usa para admitir controles que se expanden visualmente para mostrar más contenido y se contraen para ocultar el contenido.

Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IExpandCollapseProvider**](#required-members-for-iexpandcollapseprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **ExpandCollapse** , tenga en cuenta las siguientes directrices y convenciones:

-   Los controles agregados, creados con objetos secundarios que proporcionan la interfaz de usuario con la funcionalidad de expandir o contraer, deben admitir el patrón de control **ExpandCollapse** , mientras que sus elementos secundarios no lo admiten. Por ejemplo, un control de cuadro combinado se crea con una combinación de controles de cuadro de lista, botón y edición, pero solo es el cuadro combinado primario que debe admitir el patrón de control **ExpandCollapse** .
    > [!Note]  
    > Una excepción es el control de menú, que es un agregado de objetos de elemento de menú individuales. Los objetos de elemento de menú pueden admitir el patrón de control **ExpandCollapse** , pero el control de menú primario no puede. Se aplica una excepción similar a los controles de árbol y elemento de árbol.

     

-   Cuando [**IExpandCollapseProvider:: ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) de un control se establece en **ExpandCollapseState \_ LeafNode**, cualquier funcionalidad **ExpandCollapse** está actualmente inactiva para el control y la única información que se puede obtener mediante este patrón de control es el **ExpandCollapseState**. Si posteriormente se agregan objetos secundarios, se activa la funcionalidad **ExpandCollapseState** Changes y **ExpandCollapse** .
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) solo hace referencia a la visibilidad de los objetos secundarios inmediatos; no hace referencia a la visibilidad de todos los objetos descendientes.
-   La funcionalidad [**IExpandCollapseProvider:: Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) y [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) es específica del control. A continuación se muestran ejemplos de este comportamiento.
    -   El menú personal de Office puede ser un elemento de menú de tres Estados ("expandido", "contraído" y "PartiallyExpanded") donde el control especifica el estado que se debe adoptar cuando se llama a [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) o [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) .
    -   La llamada a [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) en un elemento de árbol puede mostrar todos los descendientes o solo los secundarios inmediatos.
    -   Si llamar a [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) o [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) en un control mantiene el estado de sus descendientes, se debe enviar un evento de cambio de visibilidad, no un evento de cambio de estado. Si el control primario no mantiene el estado de sus descendientes cuando se contraen, el control puede destruir todos los descendientes que ya no están visibles y generar un evento destruido; o bien, puede cambiar el [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) de cada descendiente y generar un evento de cambio de visibilidad.
-   Para garantizar la navegación, es deseable que un objeto esté en el árbol de automatización de la interfaz de usuario de Microsoft (con el estado de visibilidad adecuado), independientemente de sus [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)primarios. Si los descendientes se generan a petición, solo pueden aparecer en el árbol de automatización de la interfaz de usuario después de mostrarse por primera vez o solo mientras estén visibles.

## <a name="required-members-for-iexpandcollapseprovider"></a>Miembros requeridos para **IExpandCollapseProvider**

Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) .



| Miembros requeridos                                                                                    | Tipo de miembro | Notas                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Propiedad    | None                                                                   |
| [**Expanda**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Método      | None                                                                   |
| [**Contraer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Método      | None                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Evento       | Este control no tiene ningún evento asociado; Use este controlador de eventos genéricos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





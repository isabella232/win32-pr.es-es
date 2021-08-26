---
title: Patrón de control ExpandCollapse
description: Describe directrices y convenciones para implementar IExpandCollapseProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control ExpandCollapse
- Automatización de la interfaz de usuario,patrón de control ExpandCollapse
- Automatización de la interfaz de usuario,IExpandCollapseProvider
- IExpandCollapseProvider
- implementación de Automatización de la interfaz de usuario de control ExpandCollapse
- Patrones de control ExpandCollapse
- patrones de control,IExpandCollapseProvider
- patrones de control, implementar Automatización de la interfaz de usuario ExpandCollapse
- patrones de control,ExpandCollapse
- interfaces,IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7fa1461110a7fcdee83b8b3c20c15653e7bd5740187b89337620f5410b2bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998045"
---
# <a name="expandcollapse-control-pattern"></a>Patrón de control ExpandCollapse

Describe directrices y convenciones para implementar [**IExpandCollapseProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)incluida información sobre propiedades, métodos y eventos. El patrón de control **ExpandCollapse** se usa para admitir controles que se expanden visualmente para mostrar más contenido y contraer para ocultar el contenido.

Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y Sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IExpandCollapseProvider**](#required-members-for-iexpandcollapseprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **ExpandCollapse,** tenga en cuenta las siguientes directrices y convenciones:

-   Los controles agregados, creados con objetos secundarios que proporcionan a la interfaz de usuario la funcionalidad de expansión o contención, deben admitir el patrón de control **ExpandCollapse,** mientras que sus elementos secundarios no. Por ejemplo, un control de cuadro combinado se crea con una combinación de controles de cuadro de lista, botón y edición, pero es solo el cuadro combinado primario el que debe admitir el patrón de control **ExpandCollapse.**
    > [!Note]  
    > Una excepción es el control de menú, que es un agregado de objetos de elemento de menú individuales. Los objetos de elemento de menú pueden admitir el patrón de control **ExpandCollapse,** pero el control de menú primario no. Se aplica una excepción similar a los controles de árbol y elemento de árbol.

     

-   Cuando [**IExpandCollapseProvider::ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) de un control se establece en **ExpandCollapseState \_ LeafNode**, cualquier funcionalidad **de ExpandCollapse** está inactiva actualmente para el control y la única información que se puede obtener con este patrón de control **es ExpandCollapseState.** Si posteriormente se agregan objetos secundarios, **la funcionalidad ExpandCollapseState** cambia y **expandCollapse** se activa.
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) solo hace referencia a la visibilidad de objetos secundarios inmediatos; no hace referencia a la visibilidad de todos los objetos descendientes.
-   [**La funcionalidad IExpandCollapseProvider::Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) y [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) es específica del control. A continuación se muestran ejemplos de este comportamiento.
    -   El Office Personal Menu puede ser un elemento de menú de tres estados ("Expandido", "Contraído" y "PartiallyExpanded") donde el control especifica el estado que se debe adoptar cuando se llama a [**Expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) o Contraer. [](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)
    -   La llamada a [**Expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) en un elemento de árbol puede mostrar todos los descendientes o solo los elementos secundarios inmediatos.
    -   Si al llamar a [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) o [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) en un control se mantiene el estado de sus descendientes, se debe enviar un evento de cambio de visibilidad, no un evento de cambio de estado. Si el control primario no mantiene el estado de sus descendientes cuando se contrae, el control puede destruir todos los descendientes que ya no están visibles y generar un evento destructor. o puede cambiar [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) para cada descendiente y generar un evento de cambio de visibilidad.
-   Para garantizar la navegación, es conveniente que un objeto esté en el árbol de Microsoft Automatización de la interfaz de usuario (con el estado de visibilidad adecuado) independientemente de sus elementos primarios [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate). Si los descendientes se generan a petición, solo pueden aparecer en el árbol de Automatización de la interfaz de usuario después de mostrarse por primera vez o solo mientras estén visibles.

## <a name="required-members-for-iexpandcollapseprovider"></a>Miembros necesarios para **IExpandCollapseProvider**

Las siguientes propiedades, métodos y eventos son necesarios para implementar la [**interfaz IExpandCollapseProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)



| Miembros requeridos                                                                                    | Tipo de miembro | Notas                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Propiedad    | Ninguno                                                                   |
| [**Expanda**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Método      | Ninguno                                                                   |
| [**Contraer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Método      | Ninguno                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Evento       | Este control no tiene eventos asociados; use este controlador de eventos genérico. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





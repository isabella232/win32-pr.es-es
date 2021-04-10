---
title: Patrón de control ScrollItem
description: Describe las directrices y convenciones para implementar IScrollItemProvider, incluida información sobre los métodos.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control ScrollItem
- Automatización de la interfaz de usuario, patrón de control ScrollItem
- Automatización de la interfaz de usuario, IScrollItemProvider
- IScrollItemProvider
- implementación de patrones de control ScrollItem de UI Automation
- Patrones de control de ScrollItem
- patrones de control, IScrollItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario ScrollItem
- patrones de control, ScrollItem
- interfaces, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268913"
---
# <a name="scrollitem-control-pattern"></a>Patrón de control ScrollItem

Describe las directrices y convenciones para implementar [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), incluida información sobre los métodos. El patrón de control **ScrollItem** se usa para admitir controles secundarios individuales de contenedores que implementan [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider). La existencia del patrón de control **ScrollItem** en un control no implica que su contenedor o cualquier antecesor debe implementar el patrón de control **Scroll** .

Cuando el contenedor implementa el patrón de control **Scroll** , el patrón de control **ScrollItem** actúa como un canal de comunicación entre un control secundario y su contenedor para asegurarse de que el contenedor puede cambiar el contenido (o región) actualmente visible dentro de su ventanilla para mostrar el control secundario. Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IScrollItemProvider**](#required-members-for-iscrollitemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **ScrollItem** , tenga en cuenta las siguientes directrices y convenciones:

-   No es necesario que los elementos contenidos en un control [Window](uiauto-supportwindowcontroltype.md) o **Canvas** implementen la interfaz [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) . Sin embargo, como alternativa, deben exponer una ubicación válida para la propiedad [**IUIAutomationElement:: CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (o [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)). Esto permitirá que una aplicación cliente de automatización de la interfaz de usuario de Microsoft use los métodos de patrón de control [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) en el contenedor para mostrar el elemento secundario.

## <a name="required-members-for-iscrollitemprovider"></a>Miembros requeridos para **IScrollItemProvider**

El método siguiente es necesario para implementar la interfaz [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .



| Miembros requeridos                                                    | Tipo de miembro | Notas |
|---------------------------------------------------------------------|-------------|-------|
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | Método      | None  |



 

Este patrón de control no tiene eventos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Selection (patrón de control)](uiauto-implementingselection.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





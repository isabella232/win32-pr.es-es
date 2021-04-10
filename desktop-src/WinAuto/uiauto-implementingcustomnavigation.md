---
title: Patrón de control CustomNavigation
description: Describe las directrices y convenciones para implementar la interfaz ICustomNavigationProvider, incluida la información sobre las propiedades y los métodos.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268722"
---
# <a name="customnavigation-control-pattern"></a>Patrón de control CustomNavigation

Describe las directrices y convenciones para implementar la interfaz **ICustomNavigationProvider** , incluida la información sobre las propiedades y los métodos. El patrón de control **CustomNavigation** se usa para habilitar la navegación personalizada entre controles en estructuras similares a las jerarquías, como elementos de lista, listas con viñetas, listas numeradas y encabezados. Esto permite a los proveedores describir estructuras o definir las relaciones navegables mediante el elemento por sí solo y no solo el control contenedor.

Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **ICustomNavigationProvider**](#required-members-for-icustomnavigationprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el proveedor **CustomNavigation** , tenga en cuenta las siguientes directrices y convenciones:

-   Los valores de propiedad de **PositionInSet**, **SizeOfSet** y **LEVEL** son valores enteros basados en uno.
-   **ICustomNavigationProvider** no proporciona una manipulación activa del control, como mover posiciones, agregar y quitar elementos, o promover y degradar niveles.
-   Los controles que implementan **ICustomNavigationProvider** normalmente tienen una estructura jerárquica, pero pueden omitir los niveles mediante el método **Navigate** . Las propiedades **PositionInSet**, **SizeOfSet** y **LEVEL** son necesarias en el patrón.

## <a name="required-members-for-icustomnavigationprovider"></a>Miembros requeridos para **ICustomNavigationProvider**

Las siguientes propiedades son necesarias para implementar la interfaz **ICustomNavigationProvider** .



| Miembros requeridos                                                                  | Tipo de miembro | Notas                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**CachedLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Propiedad    | Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CachedPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Propiedad    | Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CachedSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Propiedad    | Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Propiedad    | Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Propiedad    | Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Propiedad    | Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**Navegar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Método      | None                                                                                |



 

Este patrón de control no tiene métodos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[ListItem (control)](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[HeaderItem (control)](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[DataItem (control)](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





---
title: Patrón de control CustomNavigation
description: Describe directrices y convenciones para implementar la interfaz ICustomNavigationProvider, incluida información sobre propiedades y métodos.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465503"
---
# <a name="customnavigation-control-pattern"></a>Patrón de control CustomNavigation

Describe directrices y convenciones para implementar la **interfaz ICustomNavigationProvider,** incluida información sobre propiedades y métodos. El patrón de control **CustomNavigation** se usa para habilitar la navegación personalizada entre controles de estructuras similares a la jerarquía, como elementos de lista, listas con viñetas, listas numeradas y encabezados. Esto permite a los proveedores describir estructuras o definir las relaciones navegables usando solo el elemento y no solo el control que lo contiene.

Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ICustomNavigationProvider**](#required-members-for-icustomnavigationprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el **proveedor CustomNavigation,** tenga en cuenta las siguientes directrices y convenciones:

-   Los valores de propiedad **de PositionInSet,** **SizeOfSet** y **Level** son valores enteros basados en uno.
-   **ICustomNavigationProvider** no proporciona la manipulación activa del control, como mover posiciones, agregar y quitar elementos, ni promover y degradar niveles.
-   Los controles que **implementan ICustomNavigationProvider suelen** tener una estructura jerárquica, pero pueden omitir los niveles mediante el **método Navigate.** Las propiedades **PositionInSet**, **SizeOfSet** y **Level** son necesarias en el patrón.

## <a name="required-members-for-icustomnavigationprovider"></a>Miembros necesarios para **ICustomNavigationProvider**

Las siguientes propiedades son necesarias para implementar la **interfaz ICustomNavigationProvider.**



| Miembros requeridos                                                                  | Tipo de miembro | Notas                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**CachedLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Propiedad    | Se encuentra [**en la interfaz IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CachedPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Propiedad    | Se encuentra [**en la interfaz IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CachedSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Propiedad    | Se encuentra [**en la interfaz IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Propiedad    | Se encuentra [**en la interfaz IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Propiedad    | Se encuentra [**en la interfaz IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Propiedad    | Se encuentra [**en la interfaz IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**Navegar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Método      | Ninguno                                                                                |



 

Este patrón de control no tiene métodos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[ListItem Control](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[HeaderItem (Control)](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[DataItem (Control)](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





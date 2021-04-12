---
title: Patrón de control VirtualizedItem
description: Describe las directrices y convenciones para implementar IVirtualizedItemProvider, incluida información sobre propiedades y métodos.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control VirtualizedItem
- Automatización de la interfaz de usuario, patrón de control VirtualizedItem
- Automatización de la interfaz de usuario, IVirtualizedItemProvider
- IVirtualizedItemProvider
- implementación de patrones de control VirtualizedItem de UI Automation
- Patrones de control de VirtualizedItem
- patrones de control, IVirtualizedItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario VirtualizedItem
- patrones de control, VirtualizedItem
- interfaces, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269442"
---
# <a name="virtualizeditem-control-pattern"></a>Patrón de control VirtualizedItem

Describe las directrices y convenciones para implementar [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), incluida información sobre propiedades y métodos. El patrón de control **VirtualizedItem** se usa para admitir elementos virtualizados, que son elementos que se representan mediante elementos de automatización de marcadores de posición en el árbol de automatización de la interfaz de usuario de Microsoft.

Los elementos virtualizados pueden incluir elementos recuperados de un control que admite el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) o un objeto incrustado virtualizado recuperado de un control que admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) . El marcador de posición de un elemento virtualizado podría no tener datos cargados para todas las propiedades de automatización de la interfaz de usuario y puede devolver [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) en respuesta a las consultas de propiedades que no están disponibles. El patrón de control **VirtualizedItem** proporciona un método para obtener un elemento virtual de forma que haya información completa disponible para el elemento, y se puede crear un elemento de automatización completo para el elemento en el árbol de automatización de la interfaz de usuario.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IVirtualizedItemProvider**](#required-members-for-ivirtualizeditemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **VirtualizedItem** , tenga en cuenta las siguientes directrices y convenciones:

-   Cualquier elemento de marcador de posición de automatización de la interfaz de usuario que se pueda virtualizar debe admitir el patrón de control **VirtualizedItem** al exponer la interfaz [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .
-   Cuando se llama a [**IVirtualizedItemProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , el objeto de marcador de posición debe actualizarse con implementaciones completas de sus propiedades y patrones de control.
-   Cuando se llama a [**IVirtualizedItemProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) acview, el proveedor puede cambiar la ventanilla para que el elemento virtualizado se vea en la vista. No es necesario poner el elemento en la vista; sin embargo, los elementos no virtualizados y fuera de la pantalla deben admitir el método [**IScrollItemProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .

## <a name="required-members-for-ivirtualizeditemprovider"></a>Miembros requeridos para **IVirtualizedItemProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .



| Miembros requeridos                                           | Tipo de miembro | Notas |
|------------------------------------------------------------|-------------|-------|
| [**Alcanzar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementar el patrón de control ItemContainer de UI Automation](uiauto-implementingitemcontainer.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Trabajar con elementos virtualizados](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 





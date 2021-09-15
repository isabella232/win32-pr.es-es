---
title: Patrón de control VirtualizedItem
description: Describe directrices y convenciones para implementar IVirtualizedItemProvider, incluida información sobre propiedades y métodos.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control VirtualizedItem
- Automatización de la interfaz de usuario, patrón de control VirtualizedItem
- Automatización de la interfaz de usuario,IVirtualizedItemProvider
- IVirtualizedItemProvider
- implementación de Automatización de la interfaz de usuario de control VirtualizedItem
- Patrones de control VirtualizedItem
- patrones de control,IVirtualizedItemProvider
- patrones de control, implementar Automatización de la interfaz de usuario VirtualizedItem
- patrones de control, VirtualizedItem
- interfaces,IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569729"
---
# <a name="virtualizeditem-control-pattern"></a>Patrón de control VirtualizedItem

Describe directrices y convenciones para implementar [**IVirtualizedItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)incluida información sobre propiedades y métodos. El patrón de control **VirtualizedItem** se usa para admitir elementos virtualizados, que son elementos representados por elementos de automatización de marcadores de posición en el árbol de Automatización de la interfaz de usuario Microsoft.

Los elementos virtualizados pueden incluir elementos recuperados de un control que admite el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) o un objeto incrustado virtualizado recuperado de un control que admite el patrón de [control](uiauto-implementingtextandtextrange.md) Text. Es posible que el marcador de posición de un elemento virtualizado no haya cargado datos para todas las propiedades de Automatización de la interfaz de usuario y que devuelva [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) en respuesta a las consultas de propiedades que no están disponibles. El patrón de control **VirtualizedItem** proporciona un método para realizar un elemento virtual de modo que la información completa esté disponible para el elemento y se pueda crear un elemento de automatización completo para el elemento en el árbol de Automatización de la interfaz de usuario.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IVirtualizedItemProvider**](#required-members-for-ivirtualizeditemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **VirtualizedItem,** tenga en cuenta las siguientes directrices y convenciones:

-   Cualquier Automatización de la interfaz de usuario marcador de posición que se pueda virtualizar debe admitir el patrón de control **VirtualizedItem** mediante la exposición de la [**interfaz IVirtualizedItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)
-   Cuando se llama a [**IVirtualizedItemProvider::Realize,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) el objeto de marcador de posición debe actualizarse con implementaciones completa de sus propiedades y patrones de control.
-   Cuando se llama a [**IVirtualizedItemProvider::Realize,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) el proveedor puede cambiar la ventanilla para que el elemento virtualizado se vea. No es necesario poner el elemento en la vista; Sin embargo, los elementos no virtualizados fuera de la pantalla deben admitir el [**método IScrollItemProvider::ScrollIntoView.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview)

## <a name="required-members-for-ivirtualizeditemprovider"></a>Miembros necesarios para **IVirtualizedItemProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz IVirtualizedItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)



| Miembros requeridos                                           | Tipo de miembro | Notas |
|------------------------------------------------------------|-------------|-------|
| [**Darse cuenta de**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementación del patrón Automatización de la interfaz de usuario control ItemContainer](uiauto-implementingitemcontainer.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Trabajar con elementos virtualizados](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 





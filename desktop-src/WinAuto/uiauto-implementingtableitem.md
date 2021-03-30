---
title: Patrón de control TableItem
description: Describe las directrices y convenciones para implementar ITableItemProvider, incluida información sobre los métodos. El patrón de control TableItem se usa para admitir controles secundarios de contenedores que implementan ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control TableItem
- Automatización de la interfaz de usuario, patrón de control TableItem
- Automatización de la interfaz de usuario, ITableItemProvider
- ITableItemProvider
- implementación de patrones de control TableItem de UI Automation
- Patrones de control de TableItem
- patrones de control, ITableItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario TableItem
- patrones de control, TableItem
- interfaces, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774814"
---
# <a name="tableitem-control-pattern"></a>Patrón de control TableItem

Describe las directrices y convenciones para implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), incluida información sobre los métodos. El patrón de control **TableItem** se usa para admitir controles secundarios de contenedores que implementan [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).

El acceso a la funcionalidad de celda individual se proporciona mediante la implementación simultánea necesaria de [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider). Este patrón de control es análogo a **IGridItemProvider** , con la diferencia de que cualquier control que implemente [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) debe exponer mediante programación la relación entre la celda individual y su información de fila y columna. Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **ITableItemProvider**](#required-members-for-itableitemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **TableItem** , tenga en cuenta las siguientes directrices y convenciones:

-   Para obtener la funcionalidad de elemento de cuadrícula relacionada, vea el [patrón de control GridItem](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Miembros requeridos para **ITableItemProvider**

Los métodos siguientes son necesarios para implementar la interfaz [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) .



| Miembros requeridos                                                               | Tipo de miembro | Notas |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Método      | None  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Método      | None  |



 

Este patrón de control no tiene eventos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Table (patrón de control)](uiauto-implementingtable.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





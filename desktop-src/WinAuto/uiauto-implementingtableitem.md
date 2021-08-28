---
title: Patrón de control TableItem
description: Describe las directrices y convenciones para implementar ITableItemProvider, incluida la información sobre los métodos. El patrón de control TableItem se usa para admitir controles secundarios de contenedores que implementan ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control TableItem
- Automatización de la interfaz de usuario,patrón de control TableItem
- Automatización de la interfaz de usuario,ITableItemProvider
- ITableItemProvider
- implementación de Automatización de la interfaz de usuario de control TableItem
- Patrones de control TableItem
- patrones de control,ITableItemProvider
- patrones de control, implementar Automatización de la interfaz de usuario TableItem
- patrones de control, TableItem
- interfaces,ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babb64114bb761b0b6e93a7cc9c0036cb01bb8946eb813bcd0fc3e821d44a183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098275"
---
# <a name="tableitem-control-pattern"></a>Patrón de control TableItem

Describe las directrices y convenciones para implementar [**ITableItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)incluida la información sobre los métodos. El patrón de control **TableItem** se usa para admitir controles secundarios de contenedores que implementan [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).

La implementación simultánea necesaria de [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)proporciona acceso a la funcionalidad de celda individual. Este patrón de control es análogo a **IGridItemProvider** con la distinción de que cualquier control que implemente [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) debe exponer mediante programación la relación entre la celda individual y su información de fila y columna. Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y Sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ITableItemProvider**](#required-members-for-itableitemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **TableItem,** tenga en cuenta las siguientes directrices y convenciones:

-   Para obtener la funcionalidad de elemento de cuadrícula relacionada, [vea GridItem Control Pattern](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Miembros necesarios para **ITableItemProvider**

Los métodos siguientes son necesarios para implementar la [**interfaz ITableItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)



| Miembros requeridos                                                               | Tipo de miembro | Notas |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Método      | Ninguno  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Método      | Ninguno  |



 

Este patrón de control no tiene eventos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control de tabla](uiauto-implementingtable.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





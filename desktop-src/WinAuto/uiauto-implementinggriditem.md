---
title: GridItem (patrón de control)
description: Describe las directrices y convenciones para implementar IGridItemProvider, incluida información sobre las propiedades. El patrón de control GridItem se usa para admitir controles secundarios individuales de contenedores que implementan IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control GridItem
- Automatización de la interfaz de usuario, modelo de control GridItem
- Automatización de la interfaz de usuario, IGridItemProvider
- IGridItemProvider
- implementar patrones de control GridItem de automatización de la interfaz de usuario
- GridItem (patrones de control)
- patrones de control, IGridItemProvider
- patrones de control, implementación de la automatización de la interfaz de usuario
- patrones de control, GridItem
- interfaces, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775229"
---
# <a name="griditem-control-pattern"></a>GridItem (patrón de control)

Describe las directrices y convenciones para implementar [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), incluida información sobre las propiedades. El patrón de control **GridItem** se usa para admitir controles secundarios individuales de contenedores que implementan [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).

Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IGridItemProvider**](#required-members-for-igriditemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **GridItem** , tenga en cuenta las siguientes directrices y convenciones:

-   Las coordenadas de la cuadrícula son de base, donde la celda superior izquierda tiene las coordenadas (0, 0).
-   Las celdas combinadas informarán de sus propiedades de [**fila**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) y [**columna**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) en función de su celda de anclaje subyacente, tal como se define en el proveedor de automatización de la interfaz de usuario de Microsoft. Normalmente, será la fila o columna superior izquierda.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) no proporciona una manipulación activa de la cuadrícula, como combinar o dividir celdas.
-   Los controles que implementan [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) normalmente se pueden atravesar (es decir, un cliente de automatización de la interfaz de usuario puede moverse a controles adyacentes) con el teclado.

## <a name="required-members-for-igriditemprovider"></a>Miembros requeridos para **IGridItemProvider**

Las siguientes propiedades son necesarias para implementar la interfaz [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) .



| Miembros requeridos                                                  | Tipo de miembro | Notas |
|-------------------------------------------------------------------|-------------|-------|
| [**Row**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | Propiedad    | None  |
| [**Columna**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | Propiedad    | None  |
| [**RowSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | Propiedad    | None  |
| [**ColumnSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | Propiedad    | None  |
| [**ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | Propiedad    | None  |



 

Este patrón de control no tiene métodos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Grid (patrón de control)](uiauto-implementinggrid.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





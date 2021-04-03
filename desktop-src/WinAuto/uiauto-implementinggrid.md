---
title: Grid (patrón de control)
description: Describe las directrices y convenciones para implementar IGridProvider, incluida información sobre propiedades y métodos. El patrón de control Grid se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Grid
- Automatización de la interfaz de usuario, patrón de control Grid
- Automatización de la interfaz de usuario, IGridProvider
- IGridProvider
- implementar patrones de control de cuadrícula de UI Automation
- Patrones de control de cuadrícula
- patrones de control, IGridProvider
- patrones de control, implementar cuadrícula de UI Automation
- patrones de control, cuadrícula
- interfaces, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075485"
---
# <a name="grid-control-pattern"></a>Grid (patrón de control)

Describe las directrices y convenciones para implementar [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), incluida información sobre propiedades y métodos. El patrón de control **Grid** se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.

Los elementos secundarios de este elemento deben implementar [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) y organizarse en un sistema de coordenadas lógico bidimensional que se pueda atravesar por fila y columna. Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IGridProvider**](#required-members-for-igridprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Grid** , tenga en cuenta las siguientes directrices y convenciones:

-   Las coordenadas de la cuadrícula son de base cero con la parte superior izquierda (o la celda superior derecha, según la configuración regional), con las coordenadas (0,0).
-   Si una celda está vacía, todavía debe devolverse un elemento de automatización de la interfaz de usuario de Microsoft para admitir la propiedad [**IGridItemProvider:: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) para esa celda. Esto es posible si el diseño de elementos secundarios de la cuadrícula es similar a una matriz irregular (consulte el ejemplo siguiente).

    ![ejemplo de un control Grid con coordenadas vacías](images/grid.png)

-   Todavía se requiere una cuadrícula con un elemento único para implementar [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) si se considera una cuadrícula lógicamente. El número de elementos secundarios de la cuadrícula es irrelevante.
-   Las filas y columnas ocultas, según la implementación del proveedor, se pueden cargar en el árbol de automatización de la interfaz de usuario y, por tanto, se reflejarán en las propiedades [**IGridProvider:: RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) y [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) . Si las filas y columnas ocultas todavía no se han cargado, no deben contarse.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) no habilita la manipulación activa de una cuadrícula; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) debe implementarse para habilitar esta funcionalidad.
-   Use un [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) para escuchar cambios estructurales o de diseño en la cuadrícula, como las celdas que se han agregado, quitado o combinado.
-   Use un [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) para realizar un seguimiento del recorrido a través de los elementos o las celdas de una cuadrícula.

## <a name="required-members-for-igridprovider"></a>Miembros requeridos para **IGridProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) .



| Miembros requeridos                                        | Tipo de miembro | Notas |
|---------------------------------------------------------|-------------|-------|
| [**Empleado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | Propiedad    | None  |
| [**NúmeroDeColumnas**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | Propiedad    | None  |
| [**GetItem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[GridItem (patrón de control)](uiauto-implementinggriditem.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





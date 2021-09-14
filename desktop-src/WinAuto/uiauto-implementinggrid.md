---
title: Patrón de control de cuadrícula
description: Describe directrices y convenciones para implementar IGridProvider, incluida información sobre propiedades y métodos. El patrón de control Grid se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control Grid
- Automatización de la interfaz de usuario,patrón de control grid
- Automatización de la interfaz de usuario,IGridProvider
- IGridProvider
- implementación de Automatización de la interfaz de usuario de control grid
- Patrones de control de cuadrícula
- patrones de control, IGridProvider
- patrones de control, implementar Automatización de la interfaz de usuario Grid
- patrones de control, Grid
- interfaces,IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070502"
---
# <a name="grid-control-pattern"></a>Patrón de control de cuadrícula

Describe directrices y convenciones para implementar [**IGridProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)incluida información sobre propiedades y métodos. El **patrón de** control Grid se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.

Los elementos secundarios de este elemento deben implementar [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) y organizarse en un sistema de coordenadas lógico bidimensional que se puede recorrer por fila y columna. Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y Sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IGridProvider**](#required-members-for-igridprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Grid,** tenga en cuenta las siguientes directrices y convenciones:

-   Las coordenadas de cuadrícula se basan en cero y la celda superior izquierda (o superior derecha, según la configuración regional) tiene coordenadas (0,0).
-   Si una celda está vacía, se debe devolver un elemento Automatización de la interfaz de usuario microsoft para admitir la propiedad [**IGridItemProvider::ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) para esa celda. Esto es posible si el diseño de elementos secundarios de la cuadrícula es similar a una matriz irregular (consulte el ejemplo siguiente).

    ![ejemplo de un control de cuadrícula con coordenadas vacías](images/grid.png)

-   Una cuadrícula con un solo elemento sigue siendo necesaria para implementar [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) si se considera lógicamente una cuadrícula. El número de elementos secundarios de la cuadrícula es irrelevante.
-   Las filas y columnas ocultas, según la implementación del proveedor, se pueden cargar en el árbol Automatización de la interfaz de usuario y, por tanto, se reflejarán en las propiedades [**IGridProvider::RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) y [**ColumnCount.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) Si las filas y columnas ocultas todavía no se han cargado, no deben contarse.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) no habilita la manipulación activa de una cuadrícula; [**ITransformProvider debe**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) implementarse para habilitar esta funcionalidad.
-   Use [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) para escuchar los cambios estructurales o de diseño en la cuadrícula, como las celdas que se han agregado, quitado o combinado.
-   Use [**IUIAutomationFocusChangedEventHandler para**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) realizar un seguimiento del recorrido a través de los elementos o celdas de una cuadrícula.

## <a name="required-members-for-igridprovider"></a>Miembros necesarios para **IGridProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz IGridProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)



| Miembros requeridos                                        | Tipo de miembro | Notas |
|---------------------------------------------------------|-------------|-------|
| [**RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | Propiedad.    | None  |
| [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | Propiedad.    | None  |
| [**GetItem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control GridItem](uiauto-implementinggriditem.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





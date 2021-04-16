---
title: Table (patrón de control)
description: Describe las directrices y convenciones para implementar ITableProvider, incluida información sobre propiedades y métodos. El patrón de control Table se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Table
- Automatización de la interfaz de usuario, patrón de control Table
- Automatización de la interfaz de usuario, ITableProvider
- ITableProvider
- implementación de patrones de control de tabla de UI Automation
- Patrones de control de tabla
- patrones de control, ITableProvider
- patrones de control, implementar la tabla de automatización de la interfaz de usuario
- patrones de control, tabla
- interfaces, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104556988"
---
# <a name="table-control-pattern"></a>Table (patrón de control)

Describe las directrices y convenciones para implementar [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), incluida información sobre propiedades y métodos. El patrón de control **TABLE** se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.

Los elementos secundarios del elemento contenedor deben implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) y organizarse en un sistema de coordenadas lógico bidimensional que se pueda atravesar por fila y columna. Este patrón de control es análogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , con la diferencia de que cualquier control que implemente [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) también debe exponer una relación de encabezado de columna o fila para cada elemento secundario. Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **ITableProvider**](#required-members-for-itableprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **TABLE** , tenga en cuenta las siguientes directrices y convenciones:

-   El acceso al contenido de celdas individuales se realiza a través de un sistema de coordenadas lógico bidimensional o una matriz que proporciona la implementación simultánea necesaria de [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).
-   Un encabezado de columna o fila puede estar dentro de un objeto de tabla o ser un objeto de encabezado independiente asociado a un objeto de tabla.
-   Los encabezados de fila y columna pueden incluir tanto un encabezado principal como cualquier encabezado auxiliar.
    > [!Note]  
    > Este concepto se vuelve evidente en una hoja de cálculo de Microsoft Excel en la que un usuario ha definido una columna de **nombre** . Esta columna tiene ahora dos encabezados, incluido el encabezado **First Name** definido por el usuario, y la designación alfanumérica para esa columna asignada por la aplicación.

     

-   Vea [patrón de control de cuadrícula](uiauto-implementinggrid.md) para la funcionalidad de cuadrícula relacionada.

    En la imagen siguiente se muestra una tabla con encabezados de columna complejos.

    ![tabla con encabezados de columna complejos](images/uia-valuepattern-colorpicker.jpg)

    En la imagen siguiente se muestra una tabla con una propiedad [**ITableProvider:: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambigua.

    ![tabla con una propiedad RowOrColumnMajor ambigua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Miembros requeridos para **ITableProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) .



| Miembros requeridos                                                   | Tipo de miembro | Notas |
|--------------------------------------------------------------------|-------------|-------|
| [**RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Propiedad    | None  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Método      | None  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control TableItem](uiauto-implementingtableitem.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





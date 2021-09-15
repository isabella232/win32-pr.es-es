---
title: Patrón de control de tabla
description: Describe directrices y convenciones para implementar ITableProvider, incluida información sobre propiedades y métodos. El patrón de control Tabla se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automatización de la interfaz de usuario,implementing Table control pattern
- Automatización de la interfaz de usuario, patrón de control Tabla
- Automatización de la interfaz de usuario,ITableProvider
- ITableProvider
- implementación de Automatización de la interfaz de usuario de control table
- Patrones de control de tabla
- patrones de control, ITableProvider
- patrones de control, implementar Automatización de la interfaz de usuario tabla
- patrones de control, tabla
- interfaces,ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466000"
---
# <a name="table-control-pattern"></a>Patrón de control de tabla

Describe directrices y convenciones para implementar [**ITableProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)incluida información sobre propiedades y métodos. El **patrón de** control Tabla se usa para admitir controles que actúan como contenedores para una colección de elementos secundarios.

Los elementos secundarios del elemento contenedor deben implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) y organizarse en un sistema de coordenadas lógico bidimensional que se puede recorrer por fila y columna. Este patrón de control es análogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) con la distinción de que cualquier control que implemente [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) también debe exponer una relación de encabezado de columna o fila para cada elemento secundario. Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y Sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ITableProvider**](#required-members-for-itableprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Table,** tenga en cuenta las siguientes directrices y convenciones:

-   El acceso al contenido de las celdas individuales se realiza a través de una matriz o sistema de coordenadas lógico bidimensional proporcionado por la implementación simultánea necesaria de [**IGridProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)
-   Un encabezado de columna o fila puede estar dentro de un objeto de tabla o ser un objeto de encabezado independiente asociado a un objeto de tabla.
-   Los encabezados de fila y columna pueden incluir tanto un encabezado principal como cualquier encabezado auxiliar.
    > [!Note]  
    > Este concepto se hace evidente en Microsoft Excel hoja de cálculo donde un usuario ha definido una **columna De nombre.** Esta columna ahora tiene dos encabezados, incluido el encabezado **First name** definido por el usuario y la designación alfanumérica para esa columna asignada por la aplicación.

     

-   Consulte [Grid Control Pattern (Patrón de control de cuadrícula)](uiauto-implementinggrid.md) para ver la funcionalidad de cuadrícula relacionada.

    En la imagen siguiente se muestra una tabla con encabezados de columna complejos.

    ![tabla con encabezados de columna complejos](images/uia-valuepattern-colorpicker.jpg)

    En la imagen siguiente se muestra una tabla con una propiedad [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambigua.

    ![tabla con una propiedad roworcolumnmajor ambigua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Miembros necesarios para **ITableProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz ITableProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)



| Miembros requeridos                                                   | Tipo de miembro | Notas |
|--------------------------------------------------------------------|-------------|-------|
| [**RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Propiedad    | None  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Método      | None  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control TableItem](uiauto-implementingtableitem.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





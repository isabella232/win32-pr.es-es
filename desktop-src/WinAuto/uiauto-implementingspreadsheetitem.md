---
title: Patrón de control SpreadsheetItem
description: Describe las directrices y convenciones para implementar ISpreadsheetItemProvider, incluida información sobre propiedades y métodos.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control SpreadsheetItem
- Automatización de la interfaz de usuario, patrón de control SpreadsheetItem
- Automatización de la interfaz de usuario, ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- implementación del patrón de control SpreadsheetItem de UI Automation
- Patrón de control SpreadsheetItem
- patrones de control, ISpreadsheetItemProvider
- patrones de control, implementar la automatización de la interfaz de usuario SpreadsheetItem
- patrones de control, SpreadsheetItem
- interfaces, ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078240"
---
# <a name="spreadsheetitem-control-pattern"></a>Patrón de control SpreadsheetItem

Describe las directrices y convenciones para implementar [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), incluida información sobre propiedades y métodos. El patrón de control **SpreadsheetItem** se usa para exponer las propiedades de una celda en una hoja de cálculo u otro documento basado en cuadrícula.

El patrón de control **SpreadsheetItem** está estrechamente relacionado con el patrón de control [GridItem](uiauto-implementinggriditem.md) ; los controles que implementan el patrón de control **SpreadsheetItem** también deben implementar el patrón de control GridItem. Los controles también pueden implementar el patrón de control [TableItem](uiauto-implementingtableitem.md) , si es necesario. Para obtener ejemplos de controles que implementan estos patrones de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **ISpreadsheetItemProvider**](#required-members-for-ispreadsheetitemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **SpreadsheetItem** , tenga en cuenta las siguientes directrices y convenciones:

-   Al implementar los métodos [**ISpreadsheetItemProvider:: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) y [**ISpreadsheetItemProvider:: GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) , consulte la documentación de [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Estos métodos devuelven matrices para permitir que los proveedores admitan varias anotaciones en una sola celda.
-   Algunos tipos de anotaciones no requieren una implementación completa de la interfaz [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Por ejemplo, un indicador de error ortográfico sencillo podría representarse si [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) devuelve un identificador de atributo de texto de [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)y tiene [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) devuelve un valor null.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Miembros requeridos para **ISpreadsheetItemProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) .



| Miembros requeridos                                                                         | Tipo de miembro | Notas                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fórmula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Propiedad    | La implementación de una propiedad de [**fórmula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) independiente es necesaria porque la propiedad [Value](value-property.md) de una celda devuelve normalmente el valor calculado de la celda. La propiedad de **fórmula** debe ser **null** si no se ha establecido ninguna fórmula. |
| [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Método      | Devuelve una matriz de proveedores de elementos que hacen referencia a las anotaciones vinculadas a esta celda. Los punteros dentro de la matriz pueden ser null si una anotación no tiene un proveedor vinculado.                                                                                                       |
| [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Método      | Devuelve una matriz de identificadores de tipo de anotación que describen las anotaciones de esta celda. La matriz debe tener el mismo tamaño que la matriz devuelta por [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).                                         |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control de hoja de cálculo](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 
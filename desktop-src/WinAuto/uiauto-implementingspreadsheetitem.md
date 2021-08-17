---
title: Patrón de control SpreadsheetItem
description: Describe directrices y convenciones para implementar ISpreadsheetItemProvider, incluida información sobre propiedades y métodos.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control SpreadsheetItem
- Automatización de la interfaz de usuario,patrón de control SpreadsheetItem
- Automatización de la interfaz de usuario,ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- implementación del Automatización de la interfaz de usuario de control SpreadsheetItem
- Patrón de control SpreadsheetItem
- patrones de control,ISpreadsheetItemProvider
- patrones de control, implementación de Automatización de la interfaz de usuario SpreadsheetItem
- patrones de control,SpreadsheetItem
- interfaces,ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d5feaa32b5fe79635c6acc01e1e0b18b9ba77c382ba3f07c64f7cb3e921b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324375"
---
# <a name="spreadsheetitem-control-pattern"></a>Patrón de control SpreadsheetItem

Describe directrices y convenciones para implementar [**ISpreadsheetItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider)incluida información sobre propiedades y métodos. El patrón de control **SpreadsheetItem** se usa para exponer las propiedades de una celda en una hoja de cálculo u otro documento basado en cuadrícula.

El patrón de control **SpreadsheetItem** está estrechamente relacionado con el patrón de control [GridItem;](uiauto-implementinggriditem.md) Los controles que implementan el patrón de control **SpreadsheetItem** también deben implementar el patrón de control GridItem. Los controles también pueden implementar el patrón de control [TableItem,](uiauto-implementingtableitem.md) si procede. Para obtener ejemplos de controles que implementan estos patrones de control, vea [Tipos de control y Sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ISpreadsheetItemProvider**](#required-members-for-ispreadsheetitemprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **SpreadsheetItem,** tenga en cuenta las siguientes directrices y convenciones:

-   Al implementar los [**métodos ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) e [**ISpreadsheetItemProvider::GetAnnotationTypes,**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) consulte la documentación de [**IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Ambos métodos devuelven matrices para permitir que los proveedores admitan varias anotaciones en una sola celda.
-   Algunos tipos de anotaciones no requieren una implementación completa de la [**interfaz IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Por ejemplo, un indicador de error ortográfico simple podría representarse haciendo que [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) devuelva un identificador de atributo de texto [**de AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)y que [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) devuelva un valor NULL.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Miembros necesarios para **ISpreadsheetItemProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz ISpreadsheetItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider)



| Miembros requeridos                                                                         | Tipo de miembro | Notas                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fórmula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Propiedad    | Es necesario implementar una [**propiedad Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) independiente porque la propiedad [Value](value-property.md) de una celda normalmente devuelve el valor calculado de la celda. La **propiedad Formula** debe ser NULL **si** no se establece ninguna fórmula. |
| [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Método      | Devuelve una matriz de proveedores de elementos que hacen referencia a las anotaciones vinculadas a esta celda. Los punteros dentro de la matriz pueden ser NULL si una anotación no tiene un proveedor vinculado.                                                                                                       |
| [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Método      | Devuelve una matriz de identificadores de tipo de anotación que describen las anotaciones de esta celda. La matriz debe tener el mismo tamaño que la matriz devuelta [**por GetAnnotationObjects.**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects)                                         |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Patrón de control de hoja de cálculo](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 
---
title: Patrón de control de hoja de cálculo
description: Describe las directrices y convenciones para implementar ISpreadsheetProvider, incluida información sobre los métodos.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Automatización de la interfaz de usuario, implementar patrón de control de hoja de cálculo
- UI Automation, patrón de control de hoja de cálculo
- Automatización de la interfaz de usuario, ISpreadsheetProvider
- ISpreadsheetProvider
- implementar el patrón de control de hoja de cálculo UI Automation
- patrón de control de hoja de cálculo
- patrones de control, ISpreadsheetProvider
- patrones de control, implementar la hoja de cálculo de UI Automation
- patrones de control, hoja de cálculo
- interfaces, ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359187"
---
# <a name="spreadsheet-control-pattern"></a>Patrón de control de hoja de cálculo

Describe las directrices y convenciones para implementar [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), incluida información sobre los métodos. Al final del tema se ofrecen vínculos a referencias adicionales. El patrón de control de **hoja de cálculo** se usa para exponer el contenido de una hoja de cálculo u otro documento basado en cuadrícula.

El patrón de control de la **hoja de cálculo** está estrechamente relacionado con el patrón de control [Grid](uiauto-implementinggrid.md) ; los controles que implementan el patrón de control de **hoja de cálculo** también deben implementar el patrón de control Grid. Los controles también pueden implementar el patrón de control [TABLE](uiauto-implementingtable.md) , si procede. Para obtener ejemplos de controles que implementan estos patrones de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control de la **hoja de cálculo** , tenga en cuenta las siguientes directrices y convenciones:

-   Si una hoja de cálculo implementa la interfaz [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , sus celdas deben implementar la interfaz [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .
-   El método [**ISpreadsheetProvider:: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) está diseñado para proporcionar el mismo tipo de navegación que puede proporcionar una aplicación con una característica de **salto a etiqueta** . Muchos programas de hojas de cálculo permiten a las celdas específicas asignarles un nombre descriptivo o una etiqueta. **GetItemByName** permite al cliente buscar una celda en función de su nombre descriptivo. Este método no debe recuperar ninguna celda que contenga el texto del nombre porque los resultados pueden ser muy ambiguos. Si el programa de hoja de cálculo permite que varias celdas de la misma hoja de cálculo tengan el mismo nombre descriptivo o etiqueta, el comportamiento de la automatización de la interfaz de usuario de Microsoft no está definido.

## <a name="required-members-for-ispreadsheetprovider"></a>Miembros requeridos para **ISpreadsheetProvider**

El método siguiente es necesario para implementar la interfaz [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) .



| Miembros requeridos                                                       | Tipo de miembro | Notas |
|------------------------------------------------------------------------|-------------|-------|
| [**GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 
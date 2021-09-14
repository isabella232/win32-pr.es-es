---
title: Patrón de control de hoja de cálculo
description: Describe las directrices y convenciones para implementar ISpreadsheetProvider, incluida la información sobre los métodos.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control de hoja de cálculo
- Automatización de la interfaz de usuario,patrón de control de hoja de cálculo
- Automatización de la interfaz de usuario,ISpreadsheetProvider
- ISpreadsheetProvider
- implementación de un Automatización de la interfaz de usuario de control de hoja de cálculo
- patrón de control de hoja de cálculo
- patrones de control,ISpreadsheetProvider
- patrones de control, implementación de Automatización de la interfaz de usuario hoja de cálculo
- patrones de control, hoja de cálculo
- interfaces,ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070483"
---
# <a name="spreadsheet-control-pattern"></a>Patrón de control de hoja de cálculo

Describe directrices y convenciones para implementar [**ISpreadsheetProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider)incluida información sobre los métodos. Al final del tema se ofrecen vínculos a referencias adicionales. El **patrón de** control Hoja de cálculo se usa para exponer el contenido de una hoja de cálculo u otro documento basado en cuadrícula.

El **patrón de** control Hoja de cálculo está estrechamente relacionado con el patrón [de](uiauto-implementinggrid.md) control Grid. Los controles que implementan el patrón de control **Hoja** de cálculo también deben implementar el patrón de control Grid. Los controles también pueden implementar el [patrón de](uiauto-implementingtable.md) control Table, si procede. Para obtener ejemplos de controles que implementan estos patrones de control, vea [Tipos de control y sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **de hoja** de cálculo, tenga en cuenta las siguientes directrices y convenciones:

-   Si una hoja de cálculo implementa la [**interfaz ISpreadsheetProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) sus celdas deben implementar la [**interfaz ISpreadsheetItemProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider)
-   El [**método ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) está pensado para proporcionar el mismo tipo de navegación que una aplicación podría proporcionar con una característica De salto **a** etiqueta. Muchos programas de hoja de cálculo permiten que a las celdas específicas se les asigne un nombre descriptivo o una etiqueta. **GetItemByName permite** al cliente buscar una celda en función de su nombre descriptivo. Este método no debe recuperar ninguna celda que contenga el texto del nombre porque los resultados pueden ser muy ambiguos. Si el programa de hoja de cálculo permite que varias celdas de la misma hoja de cálculo tengan el mismo nombre descriptivo o etiqueta, el comportamiento Automatización de la interfaz de usuario microsoft es indefinido.

## <a name="required-members-for-ispreadsheetprovider"></a>Miembros necesarios para **ISpreadsheetProvider**

El método siguiente es necesario para implementar la [**interfaz ISpreadsheetProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider)



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

 

 
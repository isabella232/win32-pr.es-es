---
title: Acceso al contenido de la hoja de cálculo
description: En este tema se describe cómo Microsoft Automatización de la interfaz de usuario aplicaciones cliente pueden acceder al contenido de una hoja de cálculo.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- clientes, acceder al contenido de la hoja de cálculo
- clientes, controles basados en texto
- clients,Patrón de control de hoja de cálculo
- clients,SpreadsheetItem control pattern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09d34aeb484da056920a2b77d47ca199e11c00c99832412e9bf007807c49563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052353"
---
# <a name="accessing-spreadsheet-content"></a>Acceso al contenido de la hoja de cálculo

Un control basado en texto que contiene contenido de hoja de cálculo puede permitir que los clientes accedan al contenido mediante la compatibilidad con los patrones de control [Spreadsheet](uiauto-implementingspreadsheet.md) [y SpreadsheetItem.](uiauto-implementingspreadsheetitem.md) En este tema se describe cómo Microsoft Automatización de la interfaz de usuario aplicaciones cliente pueden acceder al contenido de una hoja de cálculo.

Para determinar si un control basado en texto admite los patrones de control [Spreadsheet](uiauto-implementingspreadsheet.md) y [SpreadsheetItem,](uiauto-implementingspreadsheetitem.md) recupere primero la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para el control (vea Obtención de [Automatización de la interfaz de usuario Elements).](uiauto-obtainingelements.md) A continuación, llame al método [**IUIAutomationElement::GetCurrentPattern,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) especificando un identificador de patrón de control de [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) o [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)y una variante que recibe TRUE si el control admite el patrón de control determinado.

Para acceder al contenido de la hoja de cálculo, recupere la interfaz [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) llamando al método [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) y especificando [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) como identificador del patrón de control. A continuación, use el método [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) para obtener la interfaz [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) de un elemento de hoja de cálculo determinado (normalmente una celda). Use las propiedades y los métodos de la interfaz **IUIAutomationSpreadsheetItem** para recuperar la fórmula de la celda y las anotaciones asociadas a la celda. Para obtener más información sobre las anotaciones, vea [Recuperar anotaciones.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 
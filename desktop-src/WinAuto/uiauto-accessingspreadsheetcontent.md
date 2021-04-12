---
title: Acceder al contenido de la hoja de cálculo
description: En este tema se describe cómo las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft pueden acceder al contenido de una hoja de cálculo.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- clientes, acceso al contenido de la hoja de cálculo
- clientes, controles basados en texto
- clients, patrón de control Spreadsheet
- clients, patrón de control SpreadsheetItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31495086614f34aeff378a8565200fa03f2dad62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359339"
---
# <a name="accessing-spreadsheet-content"></a>Acceder al contenido de la hoja de cálculo

Un control basado en texto que contiene el contenido de la hoja de cálculo puede permitir que los clientes tengan acceso al contenido mediante la compatibilidad con los patrones de control de [hoja de cálculo](uiauto-implementingspreadsheet.md) y [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) . En este tema se describe cómo las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft pueden acceder al contenido de una hoja de cálculo.

Para determinar si un control basado en texto admite los patrones de control de [hoja de cálculo](uiauto-implementingspreadsheet.md) y [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) , recupere primero la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para el control (consulte obtención de [elementos de UI Automation](uiauto-obtainingelements.md)). Después, llame al método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , especificando un identificador de patrón de control de [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) o [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)y una variante que reciba true si el control admite el patrón de control determinado.

Para tener acceso al contenido de la hoja de cálculo, recupere la interfaz [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) llamando al método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) y especificando [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) como identificador de patrón de control. A continuación, use el método [**IUIAutomationSpreadsheetPattern:: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) para obtener la interfaz [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) para un elemento de hoja de cálculo determinado (normalmente una celda). Use las propiedades y los métodos de la interfaz **IUIAutomationSpreadsheetItem** para recuperar la fórmula de la celda y las anotaciones asociadas a la celda. Para obtener más información sobre las anotaciones, vea [recuperar anotaciones.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 
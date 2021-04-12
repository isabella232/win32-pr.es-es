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
# <a name="accessing-spreadsheet-content"></a><span data-ttu-id="335e3-107">Acceder al contenido de la hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="335e3-107">Accessing Spreadsheet Content</span></span>

<span data-ttu-id="335e3-108">Un control basado en texto que contiene el contenido de la hoja de cálculo puede permitir que los clientes tengan acceso al contenido mediante la compatibilidad con los patrones de control de [hoja de cálculo](uiauto-implementingspreadsheet.md) y [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="335e3-108">A text-based control that contains spreadsheet content can enable clients to access the content by supporting the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns.</span></span> <span data-ttu-id="335e3-109">En este tema se describe cómo las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft pueden acceder al contenido de una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="335e3-109">This topic describes how Microsoft UI Automation client applications can access the content of a spreadsheet.</span></span>

<span data-ttu-id="335e3-110">Para determinar si un control basado en texto admite los patrones de control de [hoja de cálculo](uiauto-implementingspreadsheet.md) y [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) , recupere primero la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para el control (consulte obtención de [elementos de UI Automation](uiauto-obtainingelements.md)). Después, llame al método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , especificando un identificador de patrón de control de [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) o [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)y una variante que reciba true si el control admite el patrón de control determinado.</span><span class="sxs-lookup"><span data-stu-id="335e3-110">To determine whether a text-based control supports the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns, first retrieve the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the control (see [Obtaining UI Automation Elements](uiauto-obtainingelements.md).) Next, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying a control pattern identifier of [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) or [**UIA\_SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md), and a variant that receives TRUE if the control supports the particular control pattern.</span></span>

<span data-ttu-id="335e3-111">Para tener acceso al contenido de la hoja de cálculo, recupere la interfaz [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) llamando al método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) y especificando [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) como identificador de patrón de control.</span><span class="sxs-lookup"><span data-stu-id="335e3-111">To access the spreadsheet content, retrieve the [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) interface by calling [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method and specifying [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) as the control pattern identifier.</span></span> <span data-ttu-id="335e3-112">A continuación, use el método [**IUIAutomationSpreadsheetPattern:: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) para obtener la interfaz [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) para un elemento de hoja de cálculo determinado (normalmente una celda).</span><span class="sxs-lookup"><span data-stu-id="335e3-112">Next, use the [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) method to get the [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) interface for a particular spreadsheet item (typically a cell).</span></span> <span data-ttu-id="335e3-113">Use las propiedades y los métodos de la interfaz **IUIAutomationSpreadsheetItem** para recuperar la fórmula de la celda y las anotaciones asociadas a la celda.</span><span class="sxs-lookup"><span data-stu-id="335e3-113">Use the properties and methods of the **IUIAutomationSpreadsheetItem** interface to retrieve the formula for the cell, and any annotations associated with the cell.</span></span> <span data-ttu-id="335e3-114">Para obtener más información sobre las anotaciones, vea [recuperar anotaciones.](uiauto-usingtextrangeobjects.md)</span><span class="sxs-lookup"><span data-stu-id="335e3-114">For more information about annotations, see [Retrieving Annotations.](uiauto-usingtextrangeobjects.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="335e3-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="335e3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="335e3-116">Compatibilidad de UI Automation para el contenido textual</span><span class="sxs-lookup"><span data-stu-id="335e3-116">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="335e3-117">Trabajar con controles basados en texto</span><span class="sxs-lookup"><span data-stu-id="335e3-117">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 
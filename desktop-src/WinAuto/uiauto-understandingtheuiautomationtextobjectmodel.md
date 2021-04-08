---
title: Descripción del modelo de objetos de texto de automatización de la interfaz de usuario
description: En este tema se describe cómo las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft tienen acceso al contenido textual de un control basado en texto.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- clientes, Descripción del modelo de objetos de texto de automatización de la interfaz de usuario
- clientes, controles basados en texto
- clientes, intervalos de texto
- clients, patrón de control Text
- clients, patrón de control TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774875"
---
# <a name="understanding-the-ui-automation-text-object-model"></a><span data-ttu-id="f00b4-108">Descripción del modelo de objetos de texto de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f00b4-108">Understanding the UI Automation Text Object Model</span></span>

<span data-ttu-id="f00b4-109">En este tema se describe cómo las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft tienen acceso al contenido textual de un control basado en texto.</span><span class="sxs-lookup"><span data-stu-id="f00b4-109">This topic describes how Microsoft UI Automation client applications access the textual content of a text-based control.</span></span>

-   [<span data-ttu-id="f00b4-110">Modelo de objetos específico del control</span><span class="sxs-lookup"><span data-stu-id="f00b4-110">Control-specific Object Model</span></span>](#control-specific-object-model)
-   [<span data-ttu-id="f00b4-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f00b4-111">Related topics</span></span>](#related-topics)

<span data-ttu-id="f00b4-112">Los controles basados en texto exponen contenido textual a las aplicaciones cliente de automatización de la interfaz de usuario a través de un modelo de objetos de texto simple.</span><span class="sxs-lookup"><span data-stu-id="f00b4-112">Text-based controls expose textual content to UI Automation client applications through a simple text object model.</span></span> <span data-ttu-id="f00b4-113">Las aplicaciones cliente tienen acceso al modelo de objetos de texto a través de las interfaces de patrón de control [Text y TextRange](uiauto-about-text-and-textrange-patterns.md) , incluidos [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) y [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span><span class="sxs-lookup"><span data-stu-id="f00b4-113">Client applications have access to the text object model through the [Text and TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern interfaces, including [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span></span> <span data-ttu-id="f00b4-114">Las aplicaciones cliente pueden utilizar estas interfaces para recuperar contenido textual, atributos de texto y objetos incrustados como tablas e hipervínculos de controles basados en texto.</span><span class="sxs-lookup"><span data-stu-id="f00b4-114">Client applications can use these interfaces to retrieve textual content, text attributes, and embedded objects such as tables and hyperlinks from text-based controls.</span></span>

<span data-ttu-id="f00b4-115">Los tipos de control que admiten el modelo de objetos de texto de automatización de la interfaz de usuario incluyen los tipos de control de [edición](uiauto-supporteditcontroltype.md) y de [documento](uiauto-supportdocumentcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="f00b4-115">Control types that support the UI Automation text object model include the [Edit](uiauto-supporteditcontroltype.md) and [Document](uiauto-supportdocumentcontroltype.md) control types.</span></span> <span data-ttu-id="f00b4-116">Otros tipos de control como la [información sobre herramientas](uiauto-supporttooltipcontroltype.md) y el [texto](uiauto-supporttextcontroltype.md) también podrían admitir el modelo de objetos de texto, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="f00b4-116">Other control types such as [ToolTip](uiauto-supporttooltipcontroltype.md) and [Text](uiauto-supporttextcontroltype.md) might also support the text object model, but they are not required to.</span></span>

> [!Note]  
> <span data-ttu-id="f00b4-117">El modelo de objetos de texto de automatización de la interfaz de usuario no proporciona un medio para insertar o modificar texto.</span><span class="sxs-lookup"><span data-stu-id="f00b4-117">The UI Automation text object model does not provide a means to insert or modify text.</span></span> <span data-ttu-id="f00b4-118">Sin embargo, algunos controles permiten insertar o modificar texto a través de la interfaz [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) o a través de una entrada de teclado directa.</span><span class="sxs-lookup"><span data-stu-id="f00b4-118">However, some controls enable text to be inserted or modified either through the [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) interface, or through direct keyboard input.</span></span>

 

## <a name="control-specific-object-model"></a><span data-ttu-id="f00b4-119">Modelo de objetos específico del control</span><span class="sxs-lookup"><span data-stu-id="f00b4-119">Control-specific Object Model</span></span>

<span data-ttu-id="f00b4-120">Un control basado en texto que implementa su propio Document Object Model (DOM) puede exponer el DOM implementando el patrón de control [ObjectModel](uiauto-implementingobjectmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="f00b4-120">A text-based control that implements its own Document Object Model (DOM) can expose the DOM by implementing the [ObjectModel](uiauto-implementingobjectmodel.md) control pattern.</span></span> <span data-ttu-id="f00b4-121">La exposición del DOM puede proporcionar a las aplicaciones cliente mayor acceso y control sobre el contenido de un control basado en texto.</span><span class="sxs-lookup"><span data-stu-id="f00b4-121">Exposing the DOM can give client applications greater access to, and control over, the content of a text-based control.</span></span>

<span data-ttu-id="f00b4-122">Una aplicación cliente puede detectar si un control basado en texto determinado implementa un DOM mediante la recuperación de la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) del control.</span><span class="sxs-lookup"><span data-stu-id="f00b4-122">A client application can discover whether a particular text-based control implements a DOM by retrieving the control's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="f00b4-123">A continuación, llame al método [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , especificando el identificador de propiedad de [**UIA \_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) y una variante que reciba true si el control implementa un Dom.</span><span class="sxs-lookup"><span data-stu-id="f00b4-123">Then, call the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method, specifying the [**UIA\_IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) property identifier, and a variant that receives TRUE if the control implements a DOM.</span></span>

<span data-ttu-id="f00b4-124">Para acceder al DOM, llame al método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , especificando el identificador de patrón de control [**UIA \_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) y una variable que recibe la interfaz [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) .</span><span class="sxs-lookup"><span data-stu-id="f00b4-124">To access the DOM, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying the [**UIA\_ObjectModelPatternId**](uiauto-controlpattern-ids.md) control pattern identifier and a variable that receives the [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) interface.</span></span> <span data-ttu-id="f00b4-125">Llame al método [**IUIAutomationObjectModelPattern:: GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) para recuperar la interfaz Dom.</span><span class="sxs-lookup"><span data-stu-id="f00b4-125">Call the [**IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) method to retrieve the DOM interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f00b4-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f00b4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f00b4-127">Patrones de control Text y TextRange</span><span class="sxs-lookup"><span data-stu-id="f00b4-127">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="f00b4-128">Compatibilidad de UI Automation para el contenido textual</span><span class="sxs-lookup"><span data-stu-id="f00b4-128">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="f00b4-129">Trabajar con controles basados en texto</span><span class="sxs-lookup"><span data-stu-id="f00b4-129">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 





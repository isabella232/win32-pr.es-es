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
# <a name="understanding-the-ui-automation-text-object-model"></a>Descripción del modelo de objetos de texto de automatización de la interfaz de usuario

En este tema se describe cómo las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft tienen acceso al contenido textual de un control basado en texto.

-   [Modelo de objetos específico del control](#control-specific-object-model)
-   [Temas relacionados](#related-topics)

Los controles basados en texto exponen contenido textual a las aplicaciones cliente de automatización de la interfaz de usuario a través de un modelo de objetos de texto simple. Las aplicaciones cliente tienen acceso al modelo de objetos de texto a través de las interfaces de patrón de control [Text y TextRange](uiauto-about-text-and-textrange-patterns.md) , incluidos [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) y [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange). Las aplicaciones cliente pueden utilizar estas interfaces para recuperar contenido textual, atributos de texto y objetos incrustados como tablas e hipervínculos de controles basados en texto.

Los tipos de control que admiten el modelo de objetos de texto de automatización de la interfaz de usuario incluyen los tipos de control de [edición](uiauto-supporteditcontroltype.md) y de [documento](uiauto-supportdocumentcontroltype.md) . Otros tipos de control como la [información sobre herramientas](uiauto-supporttooltipcontroltype.md) y el [texto](uiauto-supporttextcontroltype.md) también podrían admitir el modelo de objetos de texto, pero no es necesario.

> [!Note]  
> El modelo de objetos de texto de automatización de la interfaz de usuario no proporciona un medio para insertar o modificar texto. Sin embargo, algunos controles permiten insertar o modificar texto a través de la interfaz [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) o a través de una entrada de teclado directa.

 

## <a name="control-specific-object-model"></a>Modelo de objetos específico del control

Un control basado en texto que implementa su propio Document Object Model (DOM) puede exponer el DOM implementando el patrón de control [ObjectModel](uiauto-implementingobjectmodel.md) . La exposición del DOM puede proporcionar a las aplicaciones cliente mayor acceso y control sobre el contenido de un control basado en texto.

Una aplicación cliente puede detectar si un control basado en texto determinado implementa un DOM mediante la recuperación de la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) del control. A continuación, llame al método [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , especificando el identificador de propiedad de [**UIA \_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) y una variante que reciba true si el control implementa un Dom.

Para acceder al DOM, llame al método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , especificando el identificador de patrón de control [**UIA \_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) y una variable que recibe la interfaz [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) . Llame al método [**IUIAutomationObjectModelPattern:: GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) para recuperar la interfaz Dom.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 





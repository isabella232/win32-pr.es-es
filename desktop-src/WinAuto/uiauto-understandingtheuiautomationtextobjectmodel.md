---
title: Descripción del modelo Automatización de la interfaz de usuario objetos de texto
description: En este tema se describe cómo microsoft Automatización de la interfaz de usuario aplicaciones cliente acceden al contenido textual de un control basado en texto.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- clients,understanding Automatización de la interfaz de usuario text object model
- clientes, controles basados en texto
- clients,text ranges
- clients,Text control pattern
- clients,Patrón de control TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359227"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Descripción del modelo Automatización de la interfaz de usuario objetos de texto

En este tema se describe cómo microsoft Automatización de la interfaz de usuario aplicaciones cliente acceden al contenido textual de un control basado en texto.

-   [Modelo de objetos específico del control](#control-specific-object-model)
-   [Temas relacionados](#related-topics)

Los controles basados en texto exponen contenido textual a Automatización de la interfaz de usuario aplicaciones cliente a través de un modelo de objetos de texto simple. Las aplicaciones cliente tienen acceso al modelo de objetos de texto a través de las interfaces de patrón de control Text y [TextRange,](uiauto-about-text-and-textrange-patterns.md) incluidas [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) Las aplicaciones cliente pueden usar estas interfaces para recuperar contenido textual, atributos de texto y objetos incrustados, como tablas e hipervínculos de controles basados en texto.

Los tipos de control que admiten Automatización de la interfaz de usuario de objetos de texto incluyen los tipos de control [Editar](uiauto-supporteditcontroltype.md) [y](uiauto-supportdocumentcontroltype.md) Documento. Otros tipos de control, como [Información sobre herramientas](uiauto-supporttooltipcontroltype.md) y [Texto,](uiauto-supporttextcontroltype.md) también pueden admitir el modelo de objetos de texto, pero no es necesario.

> [!Note]  
> El Automatización de la interfaz de usuario objeto de texto no proporciona un medio para insertar o modificar texto. Sin embargo, algunos controles permiten insertar o modificar texto a través de la interfaz [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) o a través de la entrada de teclado directa.

 

## <a name="control-specific-object-model"></a>Modelo de objetos específico del control

Un control basado en texto que implementa su propio Document Object Model (DOM) puede exponer el DOM implementando el patrón de control [ObjectModel.](uiauto-implementingobjectmodel.md) Exponer dom puede proporcionar a las aplicaciones cliente un mayor acceso y control sobre el contenido de un control basado en texto.

Una aplicación cliente puede detectar si un control basado en texto determinado implementa un DOM recuperando la interfaz [**IUIAutomationElement del**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) control. A continuación, llame al método [**IUIAutomationElement::GetCurrentPropertyValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) especificando el identificador de propiedad [**\_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) de UIA y una variante que recibe TRUE si el control implementa un DOM.

Para tener acceso al DOM, llame al método [**IUIAutomationElement::GetCurrentPattern,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) especificando el identificador del patrón de control [**\_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) de UIA y una variable que recibe la interfaz [**IUIAutomationObjectModelPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) Llame al [**método IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) para recuperar la interfaz DOM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 





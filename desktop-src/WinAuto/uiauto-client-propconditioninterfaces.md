---
title: Interfaces de condición de propiedad para clientes
description: En esta sección se describen las interfaces de condiciones de propiedad para los clientes de automatización de la interfaz de usuario para aplicaciones Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077841"
---
# <a name="property-condition-interfaces-for-clients"></a>Interfaces de condición de propiedad para clientes

En esta sección se describen las interfaces de condiciones de propiedad para los clientes de automatización de la interfaz de usuario para aplicaciones Microsoft Win32.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                                  | Descripción                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Expone propiedades y métodos que las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft pueden usar para recuperar información sobre una condición de propiedad basada en y. <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Representa una condición que puede ser **true** (selecciona todos los elementos) o **false** (no selecciona ningún elemento).<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Esta es la interfaz principal para las condiciones usadas en el filtrado cuando se buscan elementos en el árbol de automatización de la interfaz de usuario.<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Representa una condición que es el valor negativo de otra condición.<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Representa una condición que se compone de varias condiciones, al menos una de las cuales debe ser true.<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Representa una condición basada en un valor de propiedad que se usa para buscar elementos de automatización de la interfaz de usuario.<br/>                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes de UI Automation](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 


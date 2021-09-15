---
title: Interfaces de condición de propiedad para clientes
description: En esta sección se describen las interfaces de condición de propiedad Automatización de la interfaz de usuario clientes para aplicaciones De Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567309"
---
# <a name="property-condition-interfaces-for-clients"></a>Interfaces de condición de propiedad para clientes

En esta sección se describen las interfaces de condición de propiedad Automatización de la interfaz de usuario clientes para aplicaciones De Microsoft Win32.

## <a name="in-this-section"></a>En esta sección



| Interfaz                                                                                  | Descripción                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Expone las propiedades y los métodos que Microsoft Automatización de la interfaz de usuario aplicaciones cliente pueden usar para recuperar información sobre una condición de propiedad basada en AND. <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Representa una condición que puede ser **TRUE** (selecciona todos los elementos) o **FALSE** (no selecciona ningún elemento).<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Esta es la interfaz principal para las condiciones que se usan en el filtrado al buscar elementos en el Automatización de la interfaz de usuario árbol.<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Representa una condición que es el negativo de otra condición.<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Representa una condición que se conste de varias condiciones, al menos una de las cuales debe ser true.<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Representa una condición basada en un valor de propiedad que se usa para buscar Automatización de la interfaz de usuario elementos.<br/>                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario clientes](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 


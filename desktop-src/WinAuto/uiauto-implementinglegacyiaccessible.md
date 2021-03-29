---
title: Patrón de control LegacyIAccessible
description: Describe las directrices y convenciones para usar ILegacyIAccessibleProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control LegacyIAccessible
- Automatización de la interfaz de usuario, patrón de control LegacyIAccessible
- Automatización de la interfaz de usuario, ILegacyIAccessibleProvider
- ILegacyIAccessibleProvider
- implementación de patrones de control LegacyIAccessible de UI Automation
- Patrones de control de LegacyIAccessible
- patrones de control, ILegacyIAccessibleProvider
- patrones de control, implementar la automatización de la interfaz de usuario LegacyIAccessible
- patrones de control, LegacyIAccessible
- interfaces, ILegacyIAccessibleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777712"
---
# <a name="legacyiaccessible-control-pattern"></a>Patrón de control LegacyIAccessible

Describe las directrices y convenciones para usar [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider), incluida información sobre propiedades, métodos y eventos. Microsoft Active Accessibility admite el patrón de control **LegacyIAccessible** en el proxy de automatización de la interfaz de usuario de Microsoft.

Los proveedores de aplicaciones y controles nunca implementan la interfaz [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) .

El patrón de control **LegacyIAccessible** expone la interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) a los clientes de automatización de la interfaz de usuario, permitiéndoles tener acceso a la implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) subyacente para determinados elementos de la interfaz de usuario. Sin embargo, **IUIAutomationLegacyIAccessiblePattern** no admite métodos que están obsoletos o que son redundantes con las características de automatización de la interfaz de usuario.

Este tema contiene las siguientes secciones:

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros del patrón de control **LegacyIAccessible**](#members-of-the-legacyiaccessible-control-pattern)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Ninguna aplicación o control implementa [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider). El marco de automatización de la interfaz de usuario proporciona automáticamente la implementación del proveedor para un servidor nativo de Microsoft Active Accessibility.

El patrón de control **LegacyIAccessible** no está disponible para los controles basados en la automatización de la interfaz de usuario.

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>Miembros del patrón de control **LegacyIAccessible**

Las siguientes propiedades, métodos y eventos son miembros del patrón de control **LegacyIAccessible** . Las notas son para los clientes de automatización de la interfaz de usuario.



| Miembros                                                                        | Tipo de miembro | Notas                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**ChildId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | Propiedad    | Devuelve **CHILDID \_ Self** (0) para un objeto que no es secundario.                                                                                |
| [**DefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | Propiedad    | None                                                                                                                                 |
| [**Descripción**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | Propiedad    | None                                                                                                                                 |
| [**Ayuda**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | Propiedad    | None                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | Propiedad    | None                                                                                                                                 |
| [**Name**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | Propiedad    | None                                                                                                                                 |
| [**Role**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | Propiedad    | Use la función [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar la cadena localizada.                                                    |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | Método      | Recupera un puntero de la interfaz [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) .                                |
| [**Estado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | Propiedad    | Use la función [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar la cadena localizada.                                                  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | Propiedad    | None                                                                                                                                 |
| [**DoDefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | Método      | None                                                                                                                                 |
| [**GetIAccessible**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | Método      | None                                                                                                                                 |
| [**Seleccionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | Método      | La marca de selección es un valor **SELFLAG** de Microsoft Active Accessibility. Para obtener más información, vea [constantes SELFLAG](selflag.md). |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | Método      | None                                                                                                                                 |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





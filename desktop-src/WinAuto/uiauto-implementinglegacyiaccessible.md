---
title: Patrón de control LegacyIAccessible
description: Describe directrices y convenciones para usar ILegacyIAccessibleProvider, incluida información sobre propiedades, métodos y eventos.
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control LegacyIAccessible
- Automatización de la interfaz de usuario,patrón de control LegacyIAccessible
- Automatización de la interfaz de usuario,ILegacyIAccessibleProvider
- ILegacyIAccessibleProvider
- implementación de Automatización de la interfaz de usuario de control LegacyIAccessible
- Patrones de control LegacyIAccessible
- patrones de control, ILegacyIAccessibleProvider
- patrones de control, implementar Automatización de la interfaz de usuario LegacyIAccessible
- patrones de control, LegacyIAccessible
- interfaces,ILegacyIAccessibleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993dcba736be2232ffceb1e6ab0b1dd26b58722b1bb3c26886103229fc7574a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827199"
---
# <a name="legacyiaccessible-control-pattern"></a>Patrón de control LegacyIAccessible

Describe directrices y convenciones para usar [**ILegacyIAccessibleProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)incluida información sobre propiedades, métodos y eventos. El patrón de control **LegacyIAccessible** es compatible con Microsoft Active Accessibility a Microsoft Automatización de la interfaz de usuario Proxy.

Los proveedores de aplicaciones y controles nunca implementan [**la interfaz ILegacyIAccessibleProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)

El patrón de control **LegacyIAccessible** expone la interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) Automatización de la interfaz de usuario clientes, lo que les permite acceder a la implementación [**subyacente de IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para determinados elementos de la interfaz de usuario. Sin embargo, **IUIAutomationLegacyIAccessiblePattern** no admite métodos obsoletos o redundantes con las características Automatización de la interfaz de usuario cliente.

Este tema contiene las siguientes secciones:

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros del patrón de control **LegacyIAccessible**](#members-of-the-legacyiaccessible-control-pattern)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Ninguna aplicación o control implementa [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider). El marco de trabajo de automatización de la interfaz de usuario proporciona automáticamente la implementación del proveedor para un servidor Microsoft Active Accessibility nativo.

El patrón de control **LegacyIAccessible** no está disponible para los controles basados en Automatización de la interfaz de usuario.

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>Miembros del patrón de control **LegacyIAccessible**

Las siguientes propiedades, métodos y eventos son miembros del patrón de control **LegacyIAccessible.** Las notas son para Automatización de la interfaz de usuario cliente.



| Miembros                                                                        | Tipo de miembro | Notas                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**ChildId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | Propiedad    | Devuelve **CHILDID \_ SELF** (0) para un objeto no secundario.                                                                                |
| [**DefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | Propiedad    | Ninguno                                                                                                                                 |
| [**Descripción**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | Propiedad    | Ninguno                                                                                                                                 |
| [**Ayuda**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | Propiedad    | Ninguno                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | Propiedad    | Ninguno                                                                                                                                 |
| [**Nombre**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | Propiedad    | Ninguno                                                                                                                                 |
| [**Role**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | Propiedad    | Use la [**función GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar la cadena localizada.                                                    |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | Método      | Recupera un puntero [**de interfaz IUIAutomationElementArray.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)                                |
| [**Estado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | Propiedad    | Use la [**función GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar la cadena localizada.                                                  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | Propiedad    | Ninguno                                                                                                                                 |
| [**DoDefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | Método      | Ninguno                                                                                                                                 |
| [**GetIAccessible**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | Método      | Ninguno                                                                                                                                 |
| [**Seleccionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | Método      | La marca de selección es Microsoft Active Accessibility **valor SELFANDER.** Para obtener más información, [vea Self CONSTANTs](selflag.md). |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | Método      | Ninguno                                                                                                                                 |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





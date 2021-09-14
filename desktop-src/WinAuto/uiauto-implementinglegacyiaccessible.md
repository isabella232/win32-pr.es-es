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
- patrones de control,ILegacyIAccessibleProvider
- patrones de control, implementar Automatización de la interfaz de usuario LegacyIAccessible
- patrones de control,LegacyIAccessible
- interfaces,ILegacyIAccessibleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070494"
---
# <a name="legacyiaccessible-control-pattern"></a>Patrón de control LegacyIAccessible

Describe directrices y convenciones para usar [**ILegacyIAccessibleProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)incluida información sobre propiedades, métodos y eventos. El patrón de control **LegacyIAccessible** es compatible con el Microsoft Active Accessibility a Microsoft Automatización de la interfaz de usuario Proxy.

Los proveedores de aplicaciones y controles nunca implementan [**la interfaz ILegacyIAccessibleProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)

El patrón de control **LegacyIAccessible** expone la interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) a los clientes de Automatización de la interfaz de usuario, lo que les permite acceder a la implementación subyacente de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para determinados elementos de la interfaz de usuario. Sin embargo, **IUIAutomationLegacyIAccessiblePattern** no admite métodos que están obsoletos o que son redundantes con las Automatización de la interfaz de usuario existentes.

Este tema contiene las siguientes secciones:

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros del patrón de control **LegacyIAccessible**](#members-of-the-legacyiaccessible-control-pattern)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Ninguna aplicación o control implementa [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider). El marco de trabajo de automatización de la interfaz de usuario proporciona automáticamente la implementación del proveedor para un servidor Microsoft Active Accessibility nativo.

El patrón de control **LegacyIAccessible** no está disponible para los controles basados en Automatización de la interfaz de usuario.

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>Miembros del patrón de control **LegacyIAccessible**

Las siguientes propiedades, métodos y eventos son miembros del patrón de control **LegacyIAccessible.** Las notas son para Automatización de la interfaz de usuario cliente.



| Members                                                                        | Tipo de miembro | Notas                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**ChildId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | Propiedad.    | Devuelve **CHILDID \_ SELF** (0) para un objeto no secundario.                                                                                |
| [**DefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | Propiedad.    | None                                                                                                                                 |
| [**Descripción**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | Propiedad.    | None                                                                                                                                 |
| [**Ayuda**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | Propiedad.    | None                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | Propiedad.    | None                                                                                                                                 |
| [**Nombre**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | Propiedad.    | None                                                                                                                                 |
| [**Role**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | Propiedad.    | Use la [**función GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar la cadena localizada.                                                    |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | Método      | Recupera un puntero [**de interfaz IUIAutomationElementArray.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)                                |
| [**Estado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | Propiedad.    | Use la [**función GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar la cadena localizada.                                                  |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | Propiedad.    | None                                                                                                                                 |
| [**DoDefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | Método      | None                                                                                                                                 |
| [**GetIAccessible**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | Método      | None                                                                                                                                 |
| [**Seleccionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | Método      | La marca de selección es Microsoft Active Accessibility **valor SELFRET.** Para obtener más información, [vea SELFRET Constants](selflag.md). |
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

 

 





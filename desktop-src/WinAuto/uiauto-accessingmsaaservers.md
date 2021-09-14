---
title: Acceso a Microsoft Active Accessibility server
description: El Microsoft Active Accessibility proxy Automatización de la interfaz de usuario es un componente de software que permite a los clientes de Microsoft Automatización de la interfaz de usuario interactuar con servidores Microsoft Active Accessibility que implementan la interfaz IAccessible de forma nativa.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Automatización de la interfaz de usuario, acceder a Active Accessibility
- Automatización de la interfaz de usuario,Active Accessibility
- Automatización de la interfaz de usuario proxy
- Automatización de la interfaz de usuario,Automatización de la interfaz de usuario Proxy
- Patrón de control LegacyIAccessible
- Automatización de la interfaz de usuario,patrón de control LegacyIAccessible
- Microsoft Active Accessibility
- Active Accessibility
- clients,accessing Active Accessibility servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070578"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>Acceso a Microsoft Active Accessibility server

El Microsoft Active Accessibility proxy Automatización de la interfaz de usuario es un componente de software que permite a los clientes de Microsoft Automatización de la interfaz de usuario interactuar con servidores Microsoft Active Accessibility que implementan la [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de forma nativa. El proxy admite el patrón de control [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) y proporciona una instancia de la interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para cada Microsoft Active Accessibility servidor detectado. Automatización de la interfaz de usuario los clientes usan los métodos expuestos por **IUIAutomationLegacyIAccessiblePattern** para acceder a las propiedades y los objetos Microsoft Active Accessibility compatibles con el servidor.

Si un elemento Automatización de la interfaz de usuario tiene una implementación de Microsoft Active Accessibility subyacente, un cliente puede obtener un puntero de interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para el elemento pasando el identificador del patrón de control [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) a uno de los métodos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) siguientes:

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**GetCachedPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

La [**interfaz IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) no está disponible para los controles basados en Automatización de la interfaz de usuario.

La [**interfaz IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) permite que Automatización de la interfaz de usuario clientes accedan a la implementación [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) subyacente de un Microsoft Active Accessibility elemento. Sin embargo, la interfaz no admite métodos obsoletos o redundantes con Automatización de la interfaz de usuario características. Por ejemplo, **IUIAutomationLegacyIAccessiblePattern** no tiene un método equivalente a [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque la ubicación actual de un elemento de interfaz de usuario está disponible en la propiedad Automatización de la interfaz de usuario BoundingRectangle.

El [**método IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) permite a un cliente recuperar un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un Automatización de la interfaz de usuario elemento. Lo contrario también es posible mediante los métodos [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) e [**IUIAutomation::ElementFromIAccessibleBuildCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache)

[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) devuelve **NULL** si un objeto proxy de OLEACC.dll o de Automatización de la interfaz de usuario a Microsoft Active Accessibility Bridge proporciona la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Automatización de la interfaz de usuario y Active Accessibility](uiauto-msaa.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





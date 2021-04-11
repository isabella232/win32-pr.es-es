---
title: Acceso a servidores de Microsoft Active Accessibility
description: Microsoft Active Accessibility al proxy de automatización de la interfaz de usuario es un componente de software que permite a los clientes de automatización de la interfaz de usuario de Microsoft interactuar con servidores de Microsoft Active Accessibility que implementan la interfaz IAccessible de forma nativa.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Automatización de la interfaz de usuario, obtener acceso a Active Accessibility
- Automatización de la interfaz de usuario, Active Accessibility
- Proxy de automatización de la interfaz de usuario
- Automatización de la interfaz de usuario, proxy de UI Automation
- Patrón de control LegacyIAccessible
- Automatización de la interfaz de usuario, patrón de control LegacyIAccessible
- Microsoft Active Accessibility
- Active Accessibility
- clientes, acceso a servidores de Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075421"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>Acceso a servidores de Microsoft Active Accessibility

Microsoft Active Accessibility al proxy de automatización de la interfaz de usuario es un componente de software que permite a los clientes de automatización de la interfaz de usuario de Microsoft interactuar con servidores de Microsoft Active Accessibility que implementan la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de forma nativa. El proxy admite el patrón de control [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) y proporciona una instancia de la interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para cada servidor de Microsoft Active Accessibility detectado. Los clientes de automatización de la interfaz de usuario usan los métodos expuestos por **IUIAutomationLegacyIAccessiblePattern** para tener acceso a las propiedades y los objetos de Microsoft Active Accessibility compatibles con el servidor.

Si un elemento de automatización de la interfaz de usuario tiene una implementación subyacente de Microsoft Active Accessibility, un cliente puede obtener un puntero de interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) para el elemento pasando el identificador de patrón de control [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) a uno de los siguientes métodos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) :

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**GetCachedPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

La interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) no está disponible para los controles basados en la automatización de la interfaz de usuario.

La interfaz [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) permite a los clientes de automatización de la interfaz de usuario tener acceso a la implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) subyacente de un elemento de Microsoft Active Accessibility. Sin embargo, la interfaz no admite métodos que son obsoletos o redundantes con las características de automatización de la interfaz de usuario. Por ejemplo, **IUIAutomationLegacyIAccessiblePattern** no tiene un método que sea equivalente a [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque la ubicación actual de un elemento de la interfaz de usuario está disponible desde la propiedad BoundingRectangle de automatización de la interfaz de usuario.

El método [**IUIAutomationLegacyIAccessiblePattern:: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) permite a un cliente recuperar un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un elemento de automatización de la interfaz de usuario. También es posible usar los métodos [**IUIAutomation:: ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) y [**IUIAutomation:: ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .

[**IUIAutomationLegacyIAccessiblePattern:: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) devuelve **null** si un objeto proxy proporciona la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento desde OLEACC.dll o desde la automatización de la interfaz de usuario a Microsoft Active Accessibility Bridge.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Automatización y Active Accessibility de la interfaz de usuario](uiauto-msaa.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





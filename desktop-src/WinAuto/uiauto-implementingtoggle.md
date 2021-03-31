---
title: Alternar patrón de control
description: Describe las directrices y convenciones para implementar IToggleProvider, incluida información sobre propiedades y métodos. El patrón de control Toggle se usa para admitir controles que pueden recorrer un conjunto de Estados y mantener un estado una vez establecido.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Toggle
- Automatización de la interfaz de usuario, alternar patrón de control
- Automatización de la interfaz de usuario, IToggleProvider
- IToggleProvider
- implementar patrones de control de alternancia de la automatización de la interfaz de usuario
- Alternar patrones de control
- patrones de control, IToggleProvider
- patrones de control, alternancia de la automatización de la interfaz de usuario
- patrones de control, alternar
- interfaces, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418515"
---
# <a name="toggle-control-pattern"></a>Alternar patrón de control

Describe las directrices y convenciones para implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), incluida información sobre propiedades y métodos. El patrón de control **Toggle** se usa para admitir controles que pueden recorrer un conjunto de Estados y mantener un estado una vez establecido.

Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IToggleProvider**](#required-members-for-itoggleprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Toggle** , tenga en cuenta las siguientes directrices y convenciones:

-   Los controles que no mantienen el estado cuando se activan, como botones, botones de barra de herramientas e hipervínculos, deben implementar [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) en su lugar.
-   Un control debe recorrer sus Estados de alternancia ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) en el siguiente orden: **ToggleState \_ on**, **ToggleState \_ OFF** y, si se admite, **ToggleState \_ indeterminada**.
-   La **alternancia** no proporciona un método de estado de conjunto debido a problemas relacionados con la configuración directa de una casilla de tres Estados sin recorrer la secuencia [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) adecuada.
-   El control de botón de radio no implementa [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), porque no es capaz de recorrer sus Estados válidos.

## <a name="required-members-for-itoggleprovider"></a>Miembros requeridos para **IToggleProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) .



| Miembros requeridos                                          | Tipo de miembro | Notas |
|-----------------------------------------------------------|-------------|-------|
| [**Alternancia**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | Método      | None  |
| [**ToggleState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | Propiedad    | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





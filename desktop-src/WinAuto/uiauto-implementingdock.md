---
title: Dock (patrón de control)
description: Describe las directrices y convenciones para implementar IDockProvider, incluida información sobre propiedades y métodos. El patrón de control Dock se usa para exponer las propiedades de acoplamiento de un control dentro de un contenedor de acoplamiento.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Dock
- Automatización de la interfaz de usuario, patrón de control Dock
- Automatización de la interfaz de usuario, IDockProvider
- IDockProvider
- implementación de patrones de control Dock de UI Automation
- patrones de control Dock
- patrones de control, IDockProvider
- patrones de control, implementar el Dock de automatización de la interfaz de usuario
- patrones de control, Dock
- interfaces, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903397"
---
# <a name="dock-control-pattern"></a>Dock (patrón de control)

Describe las directrices y convenciones para implementar [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), incluida información sobre propiedades y métodos. El patrón de control **Dock** se usa para exponer las propiedades de acoplamiento de un control dentro de un contenedor de acoplamiento.

Un contenedor de acoplamiento es un control que permite organizar elementos secundarios horizontal y verticalmente, relacionados entre sí. La siguiente imagen muestra un contenedor de acoplamiento con dos elementos secundarios. Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

![captura de pantalla que muestra el contenedor de acoplamiento con dos elementos secundarios acoplados](images/dockxmpl.jpg)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IDockProvider**](#required-members-for-idockprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Dock** , tenga en cuenta las siguientes directrices y convenciones:

-   [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) no expone ninguna propiedad del contenedor de acoplamiento ni propiedades de controles que estén acoplados adyacentes al control actual dentro del contenedor de acoplamiento.
-   Los controles se acoplan de forma relativa entre ellos, según su valor actual de orden Z; cuanto mayor es su ubicación de orden Z, más lejos se colocan del borde especificado del contenedor de acoplamiento.
-   Si se cambia el tamaño del contenedor de acoplamiento, los controles acoplados dentro del contenedor cambiarán de posición y se alinearán con el mismo borde en el que estaban originalmente acoplados. Los controles acoplados también cambiarán de tamaño para rellenar cualquier espacio dentro del contenedor según el comportamiento de acoplamiento de la propiedad [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) . Por ejemplo, si se especifica **DockPosition \_ Top** , los lados izquierdo y derecho del control se expandirán para rellenar el espacio disponible. Si se especifica **DockPosition \_ Fill** , los cuatro lados del control se expandirán para rellenar el espacio disponible.
-   En un sistema de varios monitores, los controles se deben acoplar en el lado izquierdo o derecho del monitor actual. Si no es posible, deben acoplarse en el lado izquierdo del monitor que se encuentre más a la izquierda o en el lado derecho del monitor que se encuentre más a la derecha.

## <a name="required-members-for-idockprovider"></a>Miembros requeridos para **IDockProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) .



| Miembros requeridos                                                | Tipo de miembro | Notas |
|-----------------------------------------------------------------|-------------|-------|
| [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | Propiedad    | None  |
| [**SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 





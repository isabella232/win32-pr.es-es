---
title: Elementos de la interfaz de usuario personalizada
description: Los desarrolladores de servidores diseñan objetos accesibles basándose en la interfaz de usuario de una aplicación.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903226"
---
# <a name="custom-user-interface-elements"></a>Elementos de la interfaz de usuario personalizada

Los desarrolladores de servidores diseñan objetos accesibles basándose en la interfaz de usuario de una aplicación. Dado que [Active Accessibility implementa la interfaz IAccessible en nombre de los elementos de la interfaz de usuario proporcionados por el sistema](appendix-a--supported-user-interface-elements-reference.md) , como cuadros de lista, menús y controles TrackBar, debe implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) solo para los siguientes tipos de elementos de la interfaz de usuario personalizados:

-   Controles personalizados creados mediante el registro de una clase de ventana definida por la aplicación
-   Controles personalizados dibujados directamente en la pantalla que no tienen un **hWnd** asociado
-   Controles personalizados como Microsoft ActiveX y controles Java
-   Controles u objetos de la ventana de cliente de la aplicación que aún no están expuestos

Los menús y controles dibujados por el propietario son accesibles siempre que se sigan las directrices descritas en [accesos directos para exponer elementos de la interfaz de usuario personalizados](shortcuts-for-exposing-custom-user-interface-elements.md). Si sigue estas instrucciones, no es necesario implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los menús y controles dibujados por el propietario.

En la mayoría de los casos, se puede tener acceso a los controles con subclases y subclases porque el sistema controla la funcionalidad básica del control. Sin embargo, si un control superclase o subclase modifica significativamente el comportamiento del control proporcionado por el sistema en el que se basa, debe implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Para obtener más información, vea [exponer controles basados en controles del sistema](exposing-controls-based-on-system-controls.md).

Si una aplicación solo usa elementos de la interfaz de usuario proporcionados por el sistema, no es necesario implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), excepto para su ventana de cliente. Por ejemplo, una aplicación que incluye un editor de texto, no implementado mediante un control de edición, expone líneas de texto como objetos accesibles. Tenga en cuenta que Microsoft Active Accessibility expone automáticamente el texto en los controles de edición y edición enriquecida como una sola cadena de texto en la propiedad [**Value**](value-property.md) del control.

 

 





---
title: Elementos Interfaz de usuario personalizados
description: Los desarrolladores de servidores diseñan objetos accesibles basados en la interfaz de usuario de una aplicación.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174917"
---
# <a name="custom-user-interface-elements"></a>Elementos Interfaz de usuario personalizados

Los desarrolladores de servidores diseñan objetos accesibles basados en la interfaz de usuario de una aplicación. Dado Active Accessibility implementa la interfaz IAccessible en nombre de elementos de interfaz de usuario [proporcionados](appendix-a--supported-user-interface-elements-reference.md) por el sistema, como cuadros de lista, menús y controles de barra de seguimiento, debe implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) solo para los siguientes tipos de elementos de interfaz de usuario personalizados:

-   Controles personalizados creados mediante el registro de una clase de ventana definida por la aplicación
-   Controles personalizados dibujados directamente en la pantalla que no tienen un **HWND asociado**
-   Controles personalizados, como microsoft ActiveX y controles de Java
-   Controles u objetos de la ventana de cliente de la aplicación que aún no están expuestos

Los controles y menús dibujados por el propietario son accesibles siempre que siga las directrices que se deban tratar en Accesos directos para exponer elementos [Interfaz de usuario personalizados.](shortcuts-for-exposing-custom-user-interface-elements.md) Si sigue estas instrucciones, no es necesario implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los menús y controles dibujados por el propietario.

En la mayoría de los casos, se puede acceder a los controles superclases y subclases porque el sistema controla la funcionalidad básica del control. Sin embargo, si un control superclase o subclase modifica significativamente el comportamiento del control proporcionado por el sistema en el que se basa, debe implementar la interfaz [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Para obtener más información, vea [Exponer controles basados en controles del sistema](exposing-controls-based-on-system-controls.md).

Si una aplicación solo usa elementos de interfaz de usuario proporcionados por el sistema, no es necesario implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), excepto su ventana de cliente. Por ejemplo, una aplicación que incluye un editor de texto, no implementado mediante un control de edición, expone líneas de texto como objetos accesibles. Tenga en Microsoft Active Accessibility muestra automáticamente el texto de los controles de edición y [](value-property.md) edición enriquezca como una sola cadena de texto en la propiedad Valor del control .

 

 





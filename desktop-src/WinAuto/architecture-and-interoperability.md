---
title: Arquitectura e interoperabilidad
description: En este tema se describe brevemente la arquitectura de Microsoft Active Accessibility y la automatización de la interfaz de usuario de Microsoft, así como los componentes que permiten la interoperabilidad entre aplicaciones basadas en las dos tecnologías diferentes.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "104149045"
---
# <a name="architecture-and-interoperability"></a>Arquitectura e interoperabilidad

En este tema se describe brevemente la arquitectura de Microsoft Active Accessibility y la automatización de la interfaz de usuario de Microsoft, así como los componentes que permiten la interoperabilidad entre aplicaciones basadas en las dos tecnologías diferentes.

Para obtener más información sobre la interoperabilidad de Microsoft Active Accessibility y UI Automation, vea [Common Infrastructure](common-infrastructure.md).

En este tema se incluyen las siguientes secciones.

-   [Arquitectura de Microsoft Active Accessibility](#microsoft-active-accessibility-architecture)
-   [Arquitectura de UI Automation](#ui-automation-architecture)
-   [Interoperabilidad de Microsoft Active Accessibility y UI Automation](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [La interfaz IAccessibleEx](#the-iaccessibleex-interface)
-   [Temas relacionados](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Arquitectura de Microsoft Active Accessibility

Microsoft Active Accessibility expone información básica sobre controles como el nombre del control, la ubicación en la pantalla y el tipo de control, así como información de estado como la visibilidad y el estado habilitado/deshabilitado. La interfaz de usuario se representa como una jerarquía de objetos accesibles; los cambios y las acciones se representan como WinEvents.

Microsoft Active Accessibility consta de los siguientes componentes:

-   Objeto accesible: elemento lógico de la interfaz de usuario (por ejemplo, un botón) representado por una interfaz del modelo de objetos componentes (COM) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario entero (ChildID).
-   WinEvents: sistema de eventos que permite a los servidores notificar a los clientes cuando cambia un objeto accesible. Para obtener más información, vea [WinEvents](winevents-infrastructure.md).
-   OLEACC.dll: la biblioteca de vínculos dinámicos en tiempo de ejecución que proporciona la API de Microsoft Active Accessibility y el marco de trabajo del sistema de accesibilidad. OLEACC implementa objetos proxy que proporcionan información de accesibilidad predeterminada para los elementos de la interfaz de usuario estándar, incluidos los controles de usuario, los menús de usuario y los controles comunes.

En el caso de Microsoft Active Accessibility, el componente sistema del marco de accesibilidad (OLEACC) ayuda a la comunicación entre las tecnologías de asistencia (herramientas de accesibilidad) y las aplicaciones, como se muestra en la siguiente ilustración.

![Ilustración que muestra cómo las herramientas de accesibilidad interactúan con las aplicaciones](images/msaaarch.gif)

Las aplicaciones (servidores de Microsoft Active Accessibility) proporcionan información de accesibilidad de la interfaz de usuario a las herramientas (clientes de Microsoft Active Accessibility), que interactúan con la interfaz de usuario en nombre de los usuarios. El límite del código es mediante programación y un límite de proceso.

## <a name="ui-automation-architecture"></a>Arquitectura de UI Automation

Con la automatización de la interfaz de usuario, el componente principal de automatización de la interfaz de usuario (UIAutomationCore.dll) se carga en los procesos de las herramientas de accesibilidad y de las aplicaciones. El componente principal administra la comunicación entre procesos, proporciona servicios de nivel superior, como la búsqueda de elementos por valores de propiedad, y habilita la captura masiva o el almacenamiento en caché de propiedades, lo que proporciona un mejor rendimiento que la implementación de Microsoft Active Accessibility.

UI Automation incluye objetos proxy que proporcionan información de la interfaz de usuario sobre elementos de la interfaz de usuario estándar, como controles de usuario, menús de usuario y controles comunes. También incluye servidores proxy que permiten a los clientes de automatización de la interfaz de usuario obtener información de la interfaz de usuario de servidores de Microsoft Active Accessibility.

En la ilustración siguiente se muestran las relaciones entre los diversos compontents de automatización de la interfaz de usuario usados en herramientas de accesibilidad (clientes) y en aplicaciones (proveedores).

![Ilustración en la que se muestra cómo interactúan los componentes de herramientas de accesibilidad con los de las aplicaciones](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Interoperabilidad de Microsoft Active Accessibility y UI Automation

La automatización de la interfaz de usuario a Microsoft Active Accessibility Bridge permite a los clientes de Microsoft Active Accessibility acceder a los proveedores de UI Automation convirtiendo el modelo de objetos de automatización de la interfaz de usuario en un modelo de objetos de Microsoft Active Accessibility. En la ilustración siguiente se muestra el rol del puente de automatización de la interfaz de usuario a Microsoft Active Accessibility.

![Ilustración en la que se muestra cómo funciona automatización de la interfaz de usuario con aplicaciones y herramientas de accesibilidad](images/uiatomsaabridge.gif)

Del mismo modo, el proxy de automatización de Microsoft Active Accessibility a la interfaz de usuario convierte modelos de objetos de servidor basados en Active Accessibility de Microsoft para clientes de automatización de la interfaz de usuario. En la ilustración siguiente se muestra el rol del proxy de automatización de Microsoft Active Accessibility a la interfaz de usuario.

![Ilustración que muestra cómo funciona el proxy de automatización de la interfaz de usuario con aplicaciones y herramientas de accesibilidad](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>La interfaz IAccessibleEx

La interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permite a las aplicaciones o bibliotecas de interfaz de usuario existentes ampliar su modelo de objetos de Microsoft Active Accessibility para admitir la automatización de la interfaz de usuario sin tener que volver a escribir la implementación desde el principio. Con **IAccessibleEx**, solo puede implementar las propiedades de automatización de la interfaz de usuario y los patrones de control adicionales necesarios para describir completamente la interfaz de usuario y su funcionalidad.

Dado que el proxy de automatización de Microsoft Active Accessibility a la interfaz de usuario convierte los modelos de objetos de los servidores de Microsoft Active Accessibility habilitados para [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)como modelos de objetos de automatización de la interfaz de usuario, los clientes de automatización de la interfaz de usuario no necesitan realizar ningún trabajo adicional. La interfaz **IAccessibleEx** también puede permitir que los clientes de Microsoft Active Accessibility en proceso interactúen directamente con los proveedores de automatización de la interfaz de usuario.

Para obtener más información, consulte [la interfaz IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la API de automatización de Windows](windows-automation-api-overview.md)
</dt> <dt>

[La interfaz IAccessibleEx](iaccessibleex.md)
</dt> <dt>

[Consideraciones de seguridad para las tecnologías de asistencia](uiauto-securityoverview.md)
</dt> </dl>

 

 





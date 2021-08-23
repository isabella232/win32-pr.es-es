---
title: Arquitectura e interoperabilidad
description: En este tema se describe brevemente la arquitectura de Microsoft Active Accessibility y Microsoft Automatización de la interfaz de usuario, así como los componentes que permiten la interoperabilidad entre aplicaciones basadas en las dos tecnologías diferentes.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b146fa2d628ff64d2dcf714a1f860bee28c2f0f816e057f6b411e8344462fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053023"
---
# <a name="architecture-and-interoperability"></a>Arquitectura e interoperabilidad

En este tema se describe brevemente la arquitectura de Microsoft Active Accessibility y Microsoft Automatización de la interfaz de usuario, así como los componentes que permiten la interoperabilidad entre aplicaciones basadas en las dos tecnologías diferentes.

Para obtener más información sobre Microsoft Active Accessibility y Automatización de la interfaz de usuario interoperabilidad, vea [Common Infrastructure](common-infrastructure.md).

En este tema se incluyen las siguientes secciones.

-   [Microsoft Active Accessibility arquitectura](#microsoft-active-accessibility-architecture)
-   [Automatización de la interfaz de usuario arquitectura](#ui-automation-architecture)
-   [Microsoft Active Accessibility y Automatización de la interfaz de usuario Interoperability](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [Interfaz IAccessibleEx](#the-iaccessibleex-interface)
-   [Temas relacionados](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Microsoft Active Accessibility arquitectura

Microsoft Active Accessibility muestra información básica sobre controles como el nombre del control, la ubicación en pantalla y el tipo de control, así como información de estado como visibilidad y estado habilitado o deshabilitado. La interfaz de usuario se representa como una jerarquía de objetos accesibles; Los cambios y las acciones se representan como WinEvents.

Microsoft Active Accessibility consta de los siguientes componentes:

-   Objeto accesible: un elemento lógico de la interfaz de usuario (como un botón) representado por una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) y un identificador secundario entero (ChildID).
-   WinEvents: un sistema de eventos que permite a los servidores notificar a los clientes cuando cambia un objeto accesible. Para obtener más información, vea [WinEvents](winevents-infrastructure.md).
-   OLEACC.dll: la biblioteca de vínculos dinámicos en tiempo de ejecución que proporciona la API de Microsoft Active Accessibility y el marco del sistema de accesibilidad. OLEACC implementa objetos proxy que proporcionan información de accesibilidad predeterminada para los elementos de interfaz de usuario estándar, incluidos los controles USER, los menús USER y los controles comunes.

Por Microsoft Active Accessibility, el componente del sistema del marco de accesibilidad (OLEACC) ayuda a la comunicación entre las tecnologías de asistencia (herramientas de accesibilidad) y las aplicaciones, como se muestra en la ilustración siguiente.

![ilustración que muestra cómo interactúan las herramientas de accesibilidad con las aplicaciones](images/msaaarch.gif)

Las aplicaciones (Microsoft Active Accessibility servidor) proporcionan información de accesibilidad de la interfaz de usuario a las herramientas (Microsoft Active Accessibility clientes), que interactúan con la interfaz de usuario en nombre de los usuarios. El límite de código es un límite de proceso y de programación.

## <a name="ui-automation-architecture"></a>Automatización de la interfaz de usuario arquitectura

Con Automatización de la interfaz de usuario, el Automatización de la interfaz de usuario principal (UIAutomationCore.dll) se carga en los procesos de las herramientas de accesibilidad y de las aplicaciones. El componente principal administra la comunicación entre procesos, proporciona servicios de nivel superior, como la búsqueda de elementos por valores de propiedad, y permite la captura masiva o el almacenamiento en caché de propiedades, lo que proporciona un mejor rendimiento que la implementación de Microsoft Active Accessibility.

Automatización de la interfaz de usuario incluye objetos proxy que proporcionan información de interfaz de usuario sobre elementos de interfaz de usuario estándar, como controles USER, menús USER y controles comunes. También incluye servidores proxy que permiten a los clientes Automatización de la interfaz de usuario obtener información de la interfaz de usuario de Microsoft Active Accessibility servidores.

En la ilustración siguiente se muestran las relaciones entre los distintos Automatización de la interfaz de usuario que se usan en las herramientas de accesibilidad (clientes) y en las aplicaciones (proveedores).

![ilustración en la que se muestra cómo interactúan los componentes de las herramientas de accesibilidad con los de las aplicaciones](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Microsoft Active Accessibility y Automatización de la interfaz de usuario interoperabilidad

La Automatización de la interfaz de usuario a Microsoft Active Accessibility Bridge permite a los clientes de Microsoft Active Accessibility acceder a los proveedores de Automatización de la interfaz de usuario mediante la conversión del modelo de objetos Automatización de la interfaz de usuario en un modelo de objetos Microsoft Active Accessibility. En la ilustración siguiente se muestra el rol del puente Automatización de la interfaz de usuario a Microsoft Active Accessibility puente.

![ilustración que muestra cómo funciona la automatización de la interfaz de usuario con aplicaciones y herramientas de accesibilidad](images/uiatomsaabridge.gif)

De forma similar, el proxy Microsoft Active Accessibility a Automatización de la interfaz de usuario convierte los modelos de objetos de servidor basados Microsoft Active Accessibility para Automatización de la interfaz de usuario cliente. En la ilustración siguiente se muestra el rol del proxy Microsoft Active Accessibility a Automatización de la interfaz de usuario proxy.

![ilustración en la que se muestra cómo funciona el proxy de automatización de la interfaz de usuario con aplicaciones y herramientas de accesibilidad](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>La interfaz IAccessibleEx

La [**interfaz IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permite a las aplicaciones o bibliotecas de interfaz de usuario existentes ampliar su modelo de objetos Microsoft Active Accessibility para admitir Automatización de la interfaz de usuario sin volver a escribir la implementación desde cero. Con **IAccessibleEx,** solo puede implementar las propiedades adicionales Automatización de la interfaz de usuario y los patrones de control necesarios para describir completamente la interfaz de usuario y su funcionalidad.

Dado que el proxy Microsoft Active Accessibility a Automatización de la interfaz de usuario traduce los modelos de objetos de los servidores Microsoft Active Accessibility habilitados para [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)como modelos de objetos Automatización de la interfaz de usuario, los clientes de Automatización de la interfaz de usuario no necesitan realizar ningún trabajo adicional. La **interfaz IAccessibleEx** también puede permitir que los clientes en proceso Microsoft Active Accessibility interactúen directamente con Automatización de la interfaz de usuario proveedores.

Para obtener más información, [vea La interfaz IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Introducción a la API de Automation](windows-automation-api-overview.md)
</dt> <dt>

[Interfaz IAccessibleEx](iaccessibleex.md)
</dt> <dt>

[Consideraciones de seguridad para las tecnologías de asistencia](uiauto-securityoverview.md)
</dt> </dl>

 

 





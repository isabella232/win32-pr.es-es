---
title: Comparación de Microsoft Active Accessibility y UI Automation
description: En este tema se resumen las principales diferencias entre Microsoft Active Accessibility y la automatización de la interfaz de usuario.
ms.assetid: ba963e53-6fb8-4bc1-8883-62547f52b0e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c90c4bffd0646aea592e19adc51ca020b2c90d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656373"
---
# <a name="microsoft-active-accessibility-and-ui-automation-compared"></a>Comparación de Microsoft Active Accessibility y UI Automation

La API de automatización de Windows consta de dos tecnologías: Microsoft Active Accessibility y Microsoft UI Automation. Microsoft Active Accessibility es la tecnología de accesibilidad heredada que se presentó como un complemento de plataforma para Windows 95, mientras que la automatización de la interfaz de usuario es una tecnología más reciente y más compatible que supera las limitaciones inherentes a Microsoft Active Accessibility.

En este tema se resumen las principales diferencias entre Microsoft Active Accessibility y la automatización de la interfaz de usuario. Se incluyen las secciones siguientes:

-   [Principios de diseño básicos](#basic-design-principles)
-   [Propiedades y patrones de control](#properties-and-control-patterns)
-   [Roles de MSAA y patrones de control de UI Automation](#msaa-roles-and-ui-automation-control-patterns)
-   [Navegación del modelo de objetos](#object-model-navigation)
-   [Extensibilidad del modelo de objetos](#object-model-extensibility)
-   [Transición desde MSAA](#transitioning-from-msaa)
-   [Elección de Microsoft Active Accessibility, UI Automation o IAccessibleEx](#choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex)
    -   [Nuevas aplicaciones y controles](#new-applications-and-controls)
    -   [Implementaciones existentes de Microsoft Active Accessibility](#existing-microsoft-active-accessibility-implementations)
-   [Temas relacionados](#related-topics)

## <a name="basic-design-principles"></a>Principios de diseño básicos

Aunque Microsoft Active Accessibility y la automatización de la interfaz de usuario son dos tecnologías diferentes, los principios de diseño básicos son similares. El propósito de ambas tecnologías es exponer información enriquecida sobre los elementos de la interfaz de usuario que se usan en las aplicaciones Windows. Los desarrolladores de herramientas de accesibilidad pueden usar esta información para crear software que hace que las aplicaciones que se ejecutan en Windows sean más accesibles para personas con discapacidades visuales, auditivas o de movimiento.

Tanto Microsoft Active Accessibility como la automatización de la interfaz de usuario exponen el modelo de objetos de la interfaz de usuario como un árbol jerárquico, cuya raíz es el escritorio. Microsoft Active Accessibility representa elementos de interfaz de usuario individuales como *objetos accesibles* y la automatización de la interfaz de usuario los representa como *elementos de automatización*. Ambos hacen referencia a la herramienta de accesibilidad o al programa de automatización de software como *cliente*. Sin embargo, Microsoft Active Accessibility hace referencia a la aplicación o control que ofrece la interfaz de usuario para obtener accesibilidad como el *servidor*, mientras que la automatización de la interfaz de usuario hace referencia a esto como *proveedor*.

## <a name="properties-and-control-patterns"></a>Propiedades y patrones de control

Microsoft Active Accessibility ofrece una interfaz única del modelo de objetos componentes (COM) con un conjunto fijo de propiedades pequeño. La automatización de la interfaz de usuario ofrece un conjunto más completo de propiedades, así como un conjunto de interfaces extendidas denominadas *patrones de control* para manipular objetos accesibles de maneras que Microsoft Active Accessibility no puede.

Para obtener más información, vea información general sobre [las propiedades de automatización](uiauto-propertiesoverview.md) de la interfaz de usuario y [patrones de control de UI Automation](uiauto-controlpatternsoverview.md).

## <a name="msaa-roles-and-ui-automation-control-patterns"></a>Roles de MSAA y patrones de control de UI Automation

Microsoft diseñó el modelo de objetos de Microsoft Active Accessibility a la misma hora en que se lanzó Windows 95. El modelo se basa en "roles" definidos hace una década y no se admiten nuevos comportamientos de la interfaz de usuario o se combinan dos o más roles juntos. No hay ningún modelo de objetos de texto, por ejemplo, para ayudar a las tecnologías de asistencia a tratar con contenido web complejo. La automatización de la interfaz de usuario supera estas limitaciones al introducir patrones de control que permiten a los objetos admitir más de un rol, y el patrón de control de [texto](uiauto-implementingtextandtextrange.md) de automatización de la interfaz de usuario ofrece un modelo de objetos de texto completo.

## <a name="object-model-navigation"></a>Navegación del modelo de objetos

Otra limitación de Microsoft Active Accessibility implica navegar por el modelo de objetos. Microsoft Active Accessibility representa la interfaz de usuario como una jerarquía de objetos accesibles. Los clientes navegan desde un objeto accesible a otro utilizando las interfaces y los métodos disponibles en el objeto accesible. Los servidores pueden exponer los elementos secundarios de un objeto accesible con las propiedades de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o con la interfaz estándar [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) com. Los clientes, sin embargo, deben ser capaces de abordar ambos enfoques para cualquier servidor. Esta ambigüedad significa trabajo adicional para implementadores de cliente y modelos de objetos accesibles rotos para implementadores de servidor.

La automatización de la interfaz de usuario representa la interfaz de usuario como un árbol jerárquico de elementos de automatización y proporciona una única interfaz para navegar por el árbol. Los clientes pueden personalizar la vista de los elementos del árbol mediante el ámbito y el filtrado.

## <a name="object-model-extensibility"></a>Extensibilidad del modelo de objetos

Las propiedades y funciones de Microsoft Active Accessibility no se pueden ampliar sin interrumpir ni cambiar la especificación de la interfaz com de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . El resultado es que el nuevo comportamiento del control no se puede exponer a través del modelo de objetos; tiende a ser estático.

Con la automatización de la interfaz de usuario, a medida que se crean nuevos elementos de la interfaz de usuario, los desarrolladores de aplicaciones pueden introducir propiedades personalizadas, patrones de control y eventos para describir los nuevos elementos. Para obtener más información, vea [propiedades personalizadas, eventos y patrones de control](uiauto-custompropertieseventscontrolpatterns.md).

## <a name="transitioning-from-msaa"></a>Transición desde MSAA

El marco de trabajo de la API de automatización de Windows proporciona compatibilidad para la transición de servidores de Microsoft Active Accessibility a proveedores de automatización de la interfaz de usuario. La interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) habilita la compatibilidad con propiedades de automatización de la interfaz de usuario y patrones de control específicos que se van a agregar a los servidores de Microsoft Active Accessibility heredados sin necesidad de volver a escribir toda la implementación. La interfaz **IAccessibleEx** también permite a los clientes de Microsoft Active Accessibility en proceso acceder directamente a las interfaces del proveedor de automatización de la interfaz de usuario, en lugar de a través de las interfaces de cliente de UI Automation. Para obtener más información, consulte [la interfaz IAccessibleEx](iaccessibleex.md).

## <a name="choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex"></a>Elección de Microsoft Active Accessibility, UI Automation o IAccessibleEx

Esta sección le ayuda a determinar qué solución de la API de automatización de Windows se va a usar para implementar un producto de tecnología de asistencia o para hacer que la aplicación sea accesible para los productos de tecnología de asistencia.

### <a name="new-applications-and-controls"></a>Nuevas aplicaciones y controles

Si está desarrollando una nueva aplicación o control, Microsoft recomienda usar la automatización de la interfaz de usuario. Aunque Microsoft Active Accessibility puede ser más fácil de implementar a corto plazo, las limitaciones inherentes a esta tecnología, como el modelo de objetos de caducidad y la imposibilidad de admitir nuevos comportamientos de la interfaz de usuario o de combinar roles, hacen que sea más difícil y costoso a largo plazo. Estas limitaciones se hacen especialmente evidentes al introducir nuevos controles.

El modelo de objetos de automatización de la interfaz de usuario es más fácil de usar y es más flexible que el de Microsoft Active Accessibility. Los elementos de automatización de la interfaz de usuario reflejan la evolución de las interfaces de usuario y los desarrolladores pueden definir patrones, propiedades y eventos personalizados de control de automatización de la interfaz de usuario.

Microsoft Active Accessibility tiende a ejecutarse lentamente para los clientes que se ejecutan fuera de proceso. Para mejorar el rendimiento, los desarrolladores de programas de herramientas de accesibilidad suelen elegir enlazar y ejecutar sus programas en el proceso de la aplicación de destino: un enfoque extremadamente difícil y arriesgado. La automatización de la interfaz de usuario es mucho más fácil de implementar para los clientes fuera de proceso y ofrece un rendimiento y una confiabilidad mucho mejores.

### <a name="existing-microsoft-active-accessibility-implementations"></a>Implementaciones existentes de Microsoft Active Accessibility

Si está actualizando una aplicación o un control existente basado en Microsoft Active Accessibility, considere la posibilidad de agregar compatibilidad para la automatización de la interfaz de usuario mediante la implementación de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . En primer lugar, asegúrese de que la aplicación o el control cumplen los siguientes requisitos:

-   La jerarquía de objetos accesibles de Microsoft Active Accessibility Server de la línea de base debe estar bien organizada y sin errores. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) no puede corregir problemas con jerarquías de objetos accesibles existentes.
-   La implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) debe cumplir la especificación de Microsoft Active Accessibility y la especificación de automatización de la interfaz de usuario. Microsoft proporciona un conjunto de herramientas para validar la compatibilidad con ambas especificaciones. Para obtener más información, vea [herramientas de prueba](testing-tools.md).

Si no se cumple alguno de estos requisitos, considere la posibilidad de implementar la automatización de la interfaz de usuario de forma nativa. Puede mantener las implementaciones heredadas de Microsoft Active Accessibility Server por compatibilidad con versiones anteriores si es necesario. Desde la perspectiva del cliente de automatización de la interfaz de usuario, no hay ninguna diferencia entre los proveedores de automatización de la interfaz de usuario y los servidores de Microsoft Active Accessibility que implementan [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correctamente.

Para obtener más información, consulte [la interfaz IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la API de automatización de Windows](windows-automation-api-overview.md)
</dt> <dt>

[Microsoft Active Accessibility](microsoft-active-accessibility.md)
</dt> <dt>

[Automatización de la interfaz de usuario](entry-uiauto-win32.md)
</dt> <dt>

[La interfaz IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 
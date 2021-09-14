---
title: Microsoft Active Accessibility y Automatización de la interfaz de usuario comparación
description: En este tema se resumen las principales diferencias entre Microsoft Active Accessibility y Automatización de la interfaz de usuario.
ms.assetid: ba963e53-6fb8-4bc1-8883-62547f52b0e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c90c4bffd0646aea592e19adc51ca020b2c90d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070684"
---
# <a name="microsoft-active-accessibility-and-ui-automation-compared"></a>Microsoft Active Accessibility y Automatización de la interfaz de usuario comparación

La WINDOWS Automation API consta de dos tecnologías: Microsoft Active Accessibility y Microsoft Automatización de la interfaz de usuario. Microsoft Active Accessibility es la tecnología de accesibilidad heredada que se introdujo como complemento de plataforma para Windows 95, mientras que Automatización de la interfaz de usuario es una tecnología más reciente y más capaz que supera las limitaciones inherentes a Microsoft Active Accessibility.

En este tema se resumen las principales diferencias entre Microsoft Active Accessibility y Automatización de la interfaz de usuario. Se incluyen las secciones siguientes:

-   [Principios básicos de diseño](#basic-design-principles)
-   [Propiedades y patrones de control](#properties-and-control-patterns)
-   [Roles de MSAA y Automatización de la interfaz de usuario de control de MSAA](#msaa-roles-and-ui-automation-control-patterns)
-   [Navegación del modelo de objetos](#object-model-navigation)
-   [Extensibilidad del modelo de objetos](#object-model-extensibility)
-   [Transición desde MSAA](#transitioning-from-msaa)
-   [Elegir Microsoft Active Accessibility, Automatización de la interfaz de usuario o IAccessibleEx](#choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex)
    -   [Nuevas aplicaciones y controles](#new-applications-and-controls)
    -   [Implementaciones Microsoft Active Accessibility existentes](#existing-microsoft-active-accessibility-implementations)
-   [Temas relacionados](#related-topics)

## <a name="basic-design-principles"></a>Principios básicos de diseño

Aunque Microsoft Active Accessibility y Automatización de la interfaz de usuario son dos tecnologías diferentes, los principios de diseño básicos son similares. El propósito de ambas tecnologías es exponer información completa sobre los elementos de interfaz de usuario usados en Windows aplicaciones. Los desarrolladores de herramientas de accesibilidad pueden usar esta información para crear software que haga que las aplicaciones que se ejecutan en Windows sea más accesible para las personas con discapacidades de visión, audiencia o movimiento.

Tanto Microsoft Active Accessibility como Automatización de la interfaz de usuario el modelo de objetos de interfaz de usuario como un árbol jerárquico, con raíz en el escritorio. Microsoft Active Accessibility representa elementos individuales de la *interfaz* de usuario como objetos accesibles y Automatización de la interfaz de usuario los representa como elementos *de automatización*. Ambos hacen referencia a la herramienta de accesibilidad o al programa de automatización de software como *el cliente*. Sin embargo, Microsoft Active Accessibility hace referencia a la aplicación o control que ofrece la interfaz de usuario para la accesibilidad como servidor *,* mientras que Automatización de la interfaz de usuario hace referencia a esto como *el proveedor*.

## <a name="properties-and-control-patterns"></a>Propiedades y patrones de control

Microsoft Active Accessibility ofrece una única interfaz de Modelo de objetos componentes (COM) con un conjunto fijo y pequeño de propiedades. Automatización de la interfaz de usuario ofrece un conjunto más completo de propiedades, así como un conjunto de interfaces *extendidas denominadas* patrones de control para manipular objetos accesibles de manera que Microsoft Active Accessibility no.

Para obtener más información, [vea Información general Automatización de la interfaz de usuario propiedades y](uiauto-propertiesoverview.md) Automatización de la interfaz de usuario información general sobre patrones de control [.](uiauto-controlpatternsoverview.md)

## <a name="msaa-roles-and-ui-automation-control-patterns"></a>Roles de MSAA y Automatización de la interfaz de usuario de control de MSAA

Microsoft diseñó Microsoft Active Accessibility modelo de objetos al mismo tiempo que Windows 95. El modelo se basa en "roles" definidos hace una década y no se pueden admitir nuevos comportamientos de la interfaz de usuario ni combinar dos o más roles. No hay ningún modelo de objetos de texto, por ejemplo, para ayudar a las tecnologías de asistencia a tratar con contenido web complejo. Automatización de la interfaz de usuario supera estas limitaciones mediante la introducción de patrones de control que permiten que los objetos admitan más de un rol, y el patrón de control Automatización de la interfaz de usuario [Text](uiauto-implementingtextandtextrange.md) ofrece un modelo de objetos de texto completo.

## <a name="object-model-navigation"></a>Navegación del modelo de objetos

Otra limitación de Microsoft Active Accessibility implica navegar por el modelo de objetos. Microsoft Active Accessibility representa la interfaz de usuario como una jerarquía de objetos accesibles. Los clientes navegan de un objeto accesible a otro mediante interfaces y métodos disponibles desde el objeto accesible. Los servidores pueden exponer los secundarios de un objeto accesible con propiedades de la [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o con la interfaz [COM IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) estándar. Sin embargo, los clientes deben ser capaces de tratar ambos enfoques para cualquier servidor. Esta ambigüedad significa un trabajo adicional para los implementadores de cliente y modelos de objetos accesibles rotos para los implementadores de servidor.

Automatización de la interfaz de usuario representa la interfaz de usuario como un árbol jerárquico de elementos de automatización y proporciona una única interfaz para navegar por el árbol. Los clientes pueden personalizar la vista de los elementos del árbol mediante el ámbito y el filtrado.

## <a name="object-model-extensibility"></a>Extensibilidad del modelo de objetos

Microsoft Active Accessibility propiedades y funciones no se pueden extender sin romper o cambiar la especificación de la interfaz COM [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) El resultado es que el nuevo comportamiento del control no se puede exponer a través del modelo de objetos; tiende a ser estático.

Con Automatización de la interfaz de usuario, a medida que se crean nuevos elementos de la interfaz de usuario, los desarrolladores de aplicaciones pueden introducir propiedades personalizadas, patrones de control y eventos para describir los nuevos elementos. Para obtener más información, [vea Custom Properties, Events, and Control Patterns](uiauto-custompropertieseventscontrolpatterns.md).

## <a name="transitioning-from-msaa"></a>Transición desde MSAA

El marco Windows AUTOMATION API proporciona compatibilidad para la transición de servidores de Microsoft Active Accessibility a Automatización de la interfaz de usuario proveedores. La [**interfaz IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permite agregar propiedades de Automatización de la interfaz de usuario y patrones de control específicos a servidores Microsoft Active Accessibility heredados sin necesidad de volver a escribir toda la implementación. La **interfaz IAccessibleEx** también permite que los clientes de Microsoft Active Accessibility en proceso accedan Automatización de la interfaz de usuario interfaces de proveedor directamente, en lugar de Automatización de la interfaz de usuario interfaces de cliente. Para obtener más información, [vea La interfaz IAccessibleEx](iaccessibleex.md).

## <a name="choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex"></a>Elegir Microsoft Active Accessibility, Automatización de la interfaz de usuario o IAccessibleEx

Esta sección le ayuda a determinar qué solución Windows API de Automation que se va a usar para implementar un producto de tecnología de asistencia o para que la aplicación sea accesible para los productos de tecnología de asistencia.

### <a name="new-applications-and-controls"></a>Nuevas aplicaciones y controles

Si está desarrollando una nueva aplicación o control, Microsoft recomienda usar Automatización de la interfaz de usuario. Aunque Microsoft Active Accessibility puede ser más fácil de implementar a corto plazo, las limitaciones inherentes a esta tecnología, como su modelo de objetos de edad y la incapacidad de admitir nuevos comportamientos de interfaz de usuario o roles de combinación, lo hace más difícil y costoso a largo plazo. Estas limitaciones se hacen especialmente evidentes al introducir nuevos controles.

El Automatización de la interfaz de usuario de objetos es más fácil de usar y es más flexible que el de Microsoft Active Accessibility. Los elementos de automatización de la interfaz de usuario reflejan la evolución de las interfaces de usuario, y los desarrolladores pueden definir patrones de control de Automatización de la interfaz de usuario, propiedades y eventos personalizados.

Microsoft Active Accessibility suele ejecutarse lentamente para los clientes que se ejecutan fuera de proceso. Para mejorar el rendimiento, los desarrolladores de programas de herramientas de accesibilidad suelen elegir enlazar y ejecutar sus programas en el proceso de aplicación de destino: un enfoque extremadamente difícil y de riesgo. Automatización de la interfaz de usuario es mucho más fácil de implementar para clientes fuera de proceso y ofrece un rendimiento y una confiabilidad mucho mejores.

### <a name="existing-microsoft-active-accessibility-implementations"></a>Implementaciones Microsoft Active Accessibility existentes

Si va a actualizar una aplicación o control existente basado en Microsoft Active Accessibility, considere la posibilidad de agregar compatibilidad con Automatización de la interfaz de usuario mediante la implementación de la [**interfaz IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) En primer lugar, asegúrese de que la aplicación o el control cumple los siguientes requisitos:

-   La línea Microsoft Active Accessibility jerarquía del servidor de objetos accesibles debe estar bien organizada y libre de errores. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) no puede corregir problemas con jerarquías de objetos accesibles existentes.
-   La [**implementación de IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) debe cumplir con la especificación Microsoft Active Accessibility y la especificación Automatización de la interfaz de usuario datos. Microsoft proporciona un conjunto de herramientas para validar el cumplimiento de ambas especificaciones. Para obtener más información, vea [Herramientas de prueba.](testing-tools.md)

Si no se cumple alguno de estos requisitos, considere la posibilidad de implementar Automatización de la interfaz de usuario de forma nativa. Si es necesario, puede mantener las implementaciones de Microsoft Active Accessibility de servidor heredados por motivos de compatibilidad con versiones anteriores. Desde una Automatización de la interfaz de usuario cliente, no hay ninguna diferencia entre los proveedores de Automatización de la interfaz de usuario y Microsoft Active Accessibility que implementan [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correctamente.

Para obtener más información, [vea La interfaz IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Introducción a la API de Automation](windows-automation-api-overview.md)
</dt> <dt>

[Microsoft Active Accessibility](microsoft-active-accessibility.md)
</dt> <dt>

[Automatización de la interfaz de usuario](entry-uiauto-win32.md)
</dt> <dt>

[La interfaz IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 
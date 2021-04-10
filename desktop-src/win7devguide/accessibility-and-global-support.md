---
title: Accesibilidad y soporte global
description: La plataforma Windows 7 facilita la compilación de soluciones que son accesibles para más usuarios y que cumplen o superan los estándares de cumplimiento de accesibilidad.
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea7f710850f419493c5a8435626d163361c8a03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149490"
---
# <a name="accessibility-and-global-support"></a>Accesibilidad y soporte global

La plataforma Windows 7 facilita la compilación de soluciones que son accesibles para más usuarios y que cumplen o superan los estándares de cumplimiento de accesibilidad. La comunidad de proveedores de tecnología de asistencia (ATV) ahora puede crear soluciones para una amplia variedad de aplicaciones cliente, y los desarrolladores de aplicaciones le resultarán más fáciles de crear y validar interfaces de usuario accesibles.

Windows 7 también facilita la compatibilidad con varios lenguajes globales que en versiones anteriores de Windows. Desde el momento en que un usuario selecciona un idioma y una ubicación, Windows 7 presenta fechas, números, calendarios, intercalaciones y otra información mediante las convenciones culturales que esperan los clientes.

## <a name="windows-automation"></a>Automatización de Windows

Windows 7 ofrece un avanzado nivel de automatización basado en estándares que se extiende para aplicaciones nativas. Se basa en Microsoft Active Accessibility y en la automatización de la interfaz de usuario de Microsoft. También está diseñado para trabajar con estándares de la industria como la web ARIA de W3C (aplicación de Internet enriquecida accesible) y las especificaciones de la *sección 508*.

La automatización de la interfaz de usuario ofrece un rendimiento mejorado al introducir proxies de automatización no administrados más rápidos para los controles de Microsoft Win32 y las aplicaciones heredadas de Microsoft Active Accessibility (*MSAA*), y registros de proxy y eventos de automatización de la interfaz de usuario más rápidos. Las nuevas características de extensibilidad extienden los patrones de control, las propiedades y los eventos personalizados. (Consulte [Windows Automation API: información general](../winauto/windows-automation-api-overview.md)).

## <a name="accessibility-support-tools"></a>Herramientas de soporte técnico de accesibilidad

El comprobador de accesibilidad de la interfaz de usuario es una práctica herramienta de interfaz gráfica de usuario que permite a los desarrolladores y evaluadores comprobar rápidamente si su interfaz de usuario cumple los requisitos de accesibilidad, como *MSAA* (que comprueba las relaciones de elementos primarios secundarios o rectángulos delimitadores) y el acceso mediante programación de automatización de la interfaz de usuario, la generación de eventos, el diseño (Consulte [Comprobador de accesibilidad](https://www.codeplex.com/AccCheck)de la interfaz de usuario).

UIA Verify es un marco de automatización de pruebas que facilita las pruebas manuales y automatizadas de la implementación del proveedor de automatización de la interfaz de usuario de un control o una aplicación. Estas dos nuevas herramientas permiten a los desarrolladores probar la funcionalidad y las implementaciones de accesibilidad en aplicaciones que usan la automatización de la interfaz de usuario o *MSAA* . Ambas herramientas están disponibles a través de [CodePlex](https://www.codeplex.com/), un sitio web que Microsoft ha creado para hospedar proyectos de código abierto y para ofrecer mejor servicio a la comunidad de desarrolladores. (Consulte [UI Automation verify (UIA Verify) Test Automation Framework](https://uiautomationverify.codeplex.com/)).

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Compatibilidad mejorada con la interfaz de usuario multilingüe y servicios lingüísticos

Windows 7 proporciona a los desarrolladores un método estándar para preparar sus aplicaciones para el mercado internacional al ofrecer una compatibilidad mejorada con la interfaz de usuario multilingüe y servicios lingüísticos que pueden usar en sus aplicaciones.

Servicios lingüísticos extendidos es una nueva característica de Windows 7 que permite a los desarrolladores usar el mismo conjunto de API reducido para aprovechar una gran variedad de funciones lingüísticas avanzadas. Mediante el uso de ServicesAPIss lingüísticos extendidos en Windows 7, los desarrolladores pueden detectar automáticamente el idioma de cualquier fragmento de texto Unicode y utilizar esa información para ayudar a mejorar la experiencia del usuario en todo el mundo. Los servicios lingüísticos extendidos también ofrecen compatibilidad con la transliteración integrada que convierte el texto de un sistema de escritura en otro. Por ejemplo, los desarrolladores ahora pueden convertir automáticamente texto entre chino simplificado y tradicional para ayudar a las personas a comunicarse entre sí a través de límites lingüísticos. Mediante el uso de ServicesAPIss lingüísticos extendidos, los desarrolladores podrán usar los servicios lingüísticos extendidos existentes y recoger nuevos servicios en el futuro sin tener que aprender el nuevo código. (Consulte [servicios lingüísticos extendidos](../intl/extended-linguistic-services.md)).

 

 
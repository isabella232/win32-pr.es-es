---
title: Herramientas de pruebas
description: Describe las herramientas para probar la implementación de accesibilidad de la aplicación para asegurarse de que la interfaz de usuario es totalmente accesible para las aplicaciones cliente y para los usuarios que acceden a la aplicación a través del teclado.
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- herramientas de prueba de accesibilidad
- herramientas de pruebas, accesibilidad
- pruebas de accesibilidad
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce653adb2602b8fdd46bebb72d3a7607185ffd84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149582"
---
# <a name="testing-tools"></a>Herramientas de pruebas

El acceso mediante programación y el acceso al teclado son requisitos esenciales para admitir la accesibilidad en la aplicación. Sin el acceso adecuado, muchos usuarios de tecnología de asistencia (AT), como lectores de pantalla y usuarios de teclado en pantalla, no podrán usar la aplicación. Asegúrese de probar exhaustivamente la implementación de accesibilidad de la aplicación para confirmar que proporciona información adecuada sobre los elementos de la interfaz de usuario y de que todos los escenarios de la aplicación se pueden realizar solo con el teclado.

Además de comprobar el acceso mediante programación, algunas de las herramientas pueden ayudarle a evaluar la implementación del acceso del teclado de la aplicación. Sin embargo, las herramientas solas no son suficientes. Es importante comprobar manualmente que todos los escenarios pueden realizarse solo con el teclado.

En el caso de los requisitos de teclado y programación, no hay una herramienta que pueda comprobar la implementación completa. Intente usar una variedad de herramientas para comprobar la implementación y, cuando sea posible, busque usuarios de tecnologías de asistencia, como lectores de pantalla, para usar la interfaz de usuario.

En esta sección se describen las herramientas disponibles para probar Microsoft UI Automation (UIA) y las implementaciones de Microsoft Active Accessibility (MSAA).

## <a name="tools"></a>Herramientas

[Información de accesibilidad](https://accessibilityinsights.io/) : ayuda a los desarrolladores a encontrar y corregir problemas de accesibilidad en sitios web y aplicaciones Windows.

- [Accesibilidad Insights para web](https://accessibilityinsights.io/docs/web/overview) es una extensión para Chrome y [Microsoft Edge Insider](https://www.microsoftedgeinsider.com) que ayuda a los desarrolladores a encontrar y corregir problemas de accesibilidad en sitios y aplicaciones Web. Admite dos escenarios principales:
  - **FASTPASS** : proceso ligero de dos pasos que ayuda a los desarrolladores a identificar problemas de accesibilidad comunes y de alto impacto en menos de cinco minutos.  
  - **Evaluación** : permite a cualquier persona comprobar que un sitio web 100 es compatible con los estándares e instrucciones de accesibilidad. [Accessibility Insights](https://accessibilityinsights.io/) también le permite revisar los elementos, las propiedades, los patrones de control y los eventos de la automatización de la interfaz de usuario (de forma similar a las herramientas heredadas de [inspección](/windows/desktop/winauto/inspect-objects) y [AccEvent](/windows/desktop/winauto/accessible-event-watcher) que se describen en la sección siguiente).

- [Accesibilidad Insights para Windows](https://accessibilityinsights.io/docs/windows/overview) ayuda a los desarrolladores a encontrar y corregir problemas de accesibilidad en aplicaciones de Windows. La herramienta admite tres escenarios principales:
  - La **inspección en directo** permite a los desarrolladores comprobar que un elemento de una aplicación tiene las propiedades de automatización de la interfaz de usuario adecuadas simplemente desplazando el puntero sobre el elemento o estableciendo el foco de teclado en él.
  - **FASTPASS** : proceso ligero de dos pasos que ayuda a los desarrolladores a identificar problemas de accesibilidad comunes y de alto impacto en menos de cinco minutos.
  - La **solución de problemas** le permite diagnosticar y corregir problemas de accesibilidad específicos.

### <a name="legacy-testing-tools"></a>Herramientas de pruebas heredadas

Las siguientes herramientas siguen estando disponibles en el Windows SDK y se documentan aquí para ofrecer soporte técnico continuado, pero se recomienda la transición a [información de accesibilidad](https://accessibilityinsights.io/).

- [**Monitor de eventos accesible**](accessible-event-watcher.md): la herramienta de supervisión de eventos accesibles (AccEvent) examina los datos de accesibilidad para ayudar a validar los elementos de la interfaz de usuario de la aplicación, para asegurarse de que los elementos de la interfaz de usuario generan eventos de Microsoft Active Accessibility y de automatización de la interfaz de usuario adecuados cuando se producen cambios AccEvent se suele usar para depurar problemas y para validar que los controles personalizados y extendidos funcionan correctamente.

- [**Inspeccione**](inspect-objects.md): inspeccionar permite ver los datos de accesibilidad en cualquier elemento de la interfaz de usuario. Es especialmente útil cuando se amplía un control común o se crea un control personalizado, para asegurarse de que las propiedades y los patrones de control se establecen correctamente.

- [**AccScope**](accscope.md): la herramienta AccScope permite a los desarrolladores evaluar visualmente la accesibilidad de su aplicación durante las fases tempranas de diseño y desarrollo. AccScope ayuda a visualizar cómo un lector de pantalla usa la información de automatización de la interfaz de usuario que proporciona una aplicación. Puede mostrar áreas en las que agregar información o soporte técnico a la aplicación puede mejorar su accesibilidad.

- [**Comprobador de accesibilidad de IU**](ui-accessibility-checker.md): la herramienta de comprobación de accesibilidad de la interfaz de usuario (AccChecker) comprueba que se cumplen los requisitos de accesibilidad de la interfaz de usuario. AccChecker incluye comprobaciones de comprobación para la automatización de la interfaz de usuario, Microsoft Active Accessibility y aplicaciones de Internet enriquecidas accesibles (ARIA). Puede proporcionar una comprobación estática que busque errores como nombres que faltan, problemas de árbol y mucho más. Ayuda a comprobar el acceso mediante programación y tiene características avanzadas que permiten automatizar las pruebas de accesibilidad.

- [**Comprobación**](ui-automation-verify.md)de la automatización de la interfaz de usuario: comprobación de UI Automation (UIA Verify) es un marco de pruebas para pruebas manuales y automatizadas de la implementación de la interfaz de usuario de un control o de la aplicación. También puede registrar los resultados de la prueba. Puede integrar la aplicación en el código de prueba y realizar comprobaciones regulares y automatizadas de los escenarios de automatización de la interfaz de usuario. Esta herramienta es útil para comprobar que los cambios en las aplicaciones con características establecidas no tienen nuevos problemas o regresiones en áreas más allá de las nuevas características.

### <a name="obsolete-tools"></a>Herramientas obsoletas

Las herramientas de la **interfaz de usuario** y el **Explorador accesibles** están obsoletas y ya no están disponibles. Use [**inspeccionar**](inspect-objects.md) o [**AccScope**](accscope.md) en su lugar.

## <a name="related-topics"></a>Temas relacionados

- [Centro para desarrolladores de accesibilidad](https://developer.microsoft.com/windows/accessible-apps)
- [Accesibilidad de Microsoft](https://www.microsoft.com/accessibility/)
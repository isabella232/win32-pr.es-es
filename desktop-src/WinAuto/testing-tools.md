---
title: Herramientas de pruebas
description: Describe las herramientas para probar la implementación de accesibilidad de la aplicación para asegurarse de que la interfaz de usuario es totalmente accesible para las aplicaciones cliente y para los usuarios que acceden a la aplicación a través del teclado.
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- herramientas de pruebas de accesibilidad
- herramientas de prueba, accesibilidad
- pruebas de accesibilidad
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce653adb2602b8fdd46bebb72d3a7607185ffd84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567337"
---
# <a name="testing-tools"></a>Herramientas de pruebas

El acceso mediante programación y el acceso con teclado son requisitos críticos para admitir la accesibilidad en la aplicación. Sin el acceso adecuado, muchos usuarios de la tecnología de asistencia (AT), como los lectores de pantalla y los usuarios de teclado en pantalla, no podrían usar la aplicación. Asegúrese de probar exhaustivamente la implementación de accesibilidad de la aplicación para confirmar que proporciona la información adecuada sobre sus elementos de la interfaz de usuario y que todos los escenarios de aplicación se pueden realizar solo con el teclado.

Además de comprobar el acceso mediante programación, algunas de las herramientas pueden ayudarle a evaluar la implementación del acceso mediante teclado de la aplicación. Sin embargo, las herramientas por sí solas no son suficientes. Es importante comprobar manualmente que todos los escenarios se pueden realizar solo con el teclado.

Para los requisitos de teclado y programación, no hay ninguna herramienta que pueda comprobar la implementación completa. Intente usar una variedad de herramientas para comprobar la implementación y, cuando sea posible, buscar usuarios de tecnologías de asistencia, como lectores de pantalla, para usar la interfaz de usuario.

En esta sección se describen las herramientas disponibles para probar las implementaciones Automatización de la interfaz de usuario Microsoft (UIA) y Microsoft Active Accessibility (MSAA).

## <a name="tools"></a>Herramientas

[Accesibilidad Ideas:](https://accessibilityinsights.io/) ayuda a los desarrolladores a encontrar y corregir problemas de accesibilidad tanto en sitios web como Windows aplicaciones.

- [Accessibility Ideas for Web](https://accessibilityinsights.io/docs/web/overview) es una extensión para Chrome y [Microsoft Edge Insider](https://www.microsoftedgeinsider.com) que ayuda a los desarrolladores a encontrar y corregir problemas de accesibilidad en sitios y aplicaciones web. Admite dos escenarios principales:
  - **FastPass:** un proceso ligero de dos pasos que ayuda a los desarrolladores a identificar problemas comunes de accesibilidad de alto impacto en menos de cinco minutos.  
  - **Evaluación:** permite a cualquier persona comprobar que un sitio web cumple al 100 % con las directrices y estándares de accesibilidad. [La Ideas](https://accessibilityinsights.io/) accesibilidad también le permite revisar Automatización de la interfaz de usuario elementos, propiedades, patrones de control y eventos (de forma similar a las herramientas heredadas [Inspect](/windows/desktop/winauto/inspect-objects) y [AccEvent](/windows/desktop/winauto/accessible-event-watcher) que se describen en la sección siguiente).

- [La Ideas Windows](https://accessibilityinsights.io/docs/windows/overview) ayuda a los desarrolladores a encontrar y corregir problemas de accesibilidad en Windows aplicaciones. La herramienta admite tres escenarios principales:
  - **Live Inspect permite** a los desarrolladores comprobar que un elemento de una aplicación tiene las propiedades de Automatización de la interfaz de usuario con solo mantener el puntero sobre el elemento o establecer el foco del teclado en él.
  - **FastPass:** un proceso ligero de dos pasos que ayuda a los desarrolladores a identificar problemas comunes de accesibilidad de alto impacto en menos de cinco minutos.
  - **La solución de** problemas permite diagnosticar y corregir problemas de accesibilidad específicos.

### <a name="legacy-testing-tools"></a>Herramientas de prueba heredadas

Las siguientes herramientas siguen estando disponibles en el SDK de Windows y se documentan aquí para obtener soporte técnico continuo, pero se recomienda realizar la transición a [Accessibility Ideas](https://accessibilityinsights.io/).

- [**Accessible Event Watcher:**](accessible-event-watcher.md)la herramienta Accessible Event Watcher (AccEvent) examina los datos de accesibilidad para ayudar a validar los elementos de la interfaz de usuario de la aplicación, con el fin de asegurarse de que los elementos de la interfaz de usuario producen eventos Microsoft Active Accessibility y Automatización de la interfaz de usuario adecuados cuando se producen cambios en la interfaz de usuario. AccEvent se usa normalmente para depurar problemas y para validar que los controles personalizados y extendidos funcionan correctamente.

- [**Inspeccionar:**](inspect-objects.md)Inspeccionar permite ver los datos de accesibilidad en cualquier elemento de la interfaz de usuario. Resulta especialmente útil, al extender un control común o crear un control personalizado, para asegurarse de que las propiedades y los patrones de control se establecen correctamente.

- [**AccScope:**](accscope.md)la herramienta AccScope permite a los desarrolladores evaluar visualmente la accesibilidad de su aplicación durante las primeras fases de diseño y desarrollo. AccScope ayuda a visualizar cómo un lector de pantalla usa Automatización de la interfaz de usuario información que proporciona una aplicación. Puede mostrar áreas en las que agregar información o soporte técnico a la aplicación puede mejorar su accesibilidad.

- [**Comprobador de accesibilidad de la**](ui-accessibility-checker.md)interfaz de usuario: la herramienta Comprobador de accesibilidad de la interfaz de usuario (AccChecker) comprueba que se cumplen los requisitos clave de accesibilidad de la interfaz de usuario. AccChecker incluye comprobaciones de verificación para Automatización de la interfaz de usuario, Microsoft Active Accessibility y aplicaciones de Internet enriquecciones accesibles (ARIA). Puede proporcionar una comprobación estática en busca de errores, como nombres que faltan, problemas de árbol, etc. Ayuda a comprobar el acceso mediante programación y tiene características avanzadas para admitir la automatización de las pruebas de accesibilidad.

- [**Automatización de la interfaz de usuario Verify:**](ui-automation-verify.md)Automatización de la interfaz de usuario Verify (UIA Verify) es un marco de pruebas para las pruebas manuales y automatizadas de la implementación de un control o aplicación de Automatización de la interfaz de usuario. También puede registrar los resultados de las pruebas. Puede integrar la aplicación en el código de prueba y realizar pruebas periódicas y automatizadas o comprobaciones de acceso Automatización de la interfaz de usuario escenarios. Esta herramienta es útil para comprobar que los cambios en las aplicaciones con características establecidas no tienen nuevos problemas o regresiones en áreas más allá de las nuevas características.

### <a name="obsolete-tools"></a>Herramientas obsoletas

Las **herramientas Accessible Explorer** y UI **Spy** están obsoletas y ya no están disponibles. Use [**Inspect**](inspect-objects.md) o [**AccScope en**](accscope.md) su lugar.

## <a name="related-topics"></a>Temas relacionados

- [Centro para desarrolladores de accesibilidad](https://developer.microsoft.com/windows/accessible-apps)
- [Accesibilidad de Microsoft](https://www.microsoft.com/accessibility/)
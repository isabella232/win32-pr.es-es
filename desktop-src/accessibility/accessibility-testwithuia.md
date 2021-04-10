---
description: Información general sobre cómo usar la automatización de la interfaz de usuario y otras herramientas para probar sus aplicaciones.
title: Pruebas de accesibilidad
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0d589c9b7bd598c0829ff9941ab2facabfaf10d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153478"
---
# <a name="testing-for-accessibility"></a>Pruebas de accesibilidad

El acceso mediante programación y el acceso al teclado son requisitos esenciales para admitir la accesibilidad en la aplicación. Probar la accesibilidad de las aplicaciones de Windows, las herramientas de tecnología de ayuda (AT) y los marcos de interfaz de usuario es fundamental para garantizar una experiencia de usuario correcta para las personas con diversas discapacidades y limitaciones (incluida la visión, el aprendizaje, Dexterity/Mobility y las discapacidades de lenguaje y comunicación) o las que simplemente prefieren usar un teclado.

Sin un acceso adecuado a través de, como los lectores de pantalla y los teclados en pantalla, los usuarios con visión, aprendizaje, Dexterity/Mobility y las discapacidades o limitaciones de lenguaje/comunicación (y los usuarios que solo prefieren usar el teclado) no podrán usar la aplicación.

En esta sección se describen las diversas herramientas que se pueden usar para probar la implementación de accesibilidad de Windows y las aplicaciones Web.

> [!NOTE]
> También es importante realizar pruebas manuales para comprobar el acceso del teclado a la aplicación.

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

- [Inspeccionar](/windows/desktop/winauto/inspect-objects): le permite ver los datos de accesibilidad de cualquier elemento de la interfaz de usuario. Es especialmente útil para garantizar que las propiedades y los patrones de control se establezcan correctamente al extender un control común o crear un control personalizado.
- [Monitor de eventos de acceso (AccEvent)](/windows/desktop/winauto/accessible-event-watcher): examina los datos de accesibilidad para validar los elementos de la interfaz de usuario de la aplicación y asegurarse de que los elementos de la interfaz de usuario generan eventos de Microsoft Active Accessibility y de automatización de la interfaz de usuario adecuados AccEvent se usa normalmente para depurar problemas y para validar que los controles personalizados y extendidos funcionan correctamente.
- [AccScope](/windows/desktop/winauto/accscope): habilita la evaluación visual de la accesibilidad de una aplicación durante las fases tempranas de diseño y desarrollo. AccScope ayuda a visualizar el modo en que un lector de pantalla usa la información de automatización de la interfaz de usuario proporcionada por una aplicación y muestra dónde la adición de información o soporte técnico a la aplicación puede mejorar su accesibilidad.
- [Comprobador de accesibilidad de IU](/windows/desktop/winauto/ui-accessibility-checker): comprueba que se logran los requisitos de accesibilidad de la interfaz de usuario clave en una aplicación. AccChecker incluye comprobaciones de comprobación para la automatización de la interfaz de usuario, Microsoft Active Accessibility y aplicaciones de Internet enriquecidas accesibles (ARIA). Puede proporcionar una comprobación estática de errores como nombres que faltan, problemas de árbol y mucho más. Ayuda a comprobar el acceso mediante programación e incluye características avanzadas para automatizar las pruebas de accesibilidad.
- [Comprobación](/windows/desktop/winauto/ui-automation-verify)de la automatización de la interfaz de usuario: un marco para las pruebas manuales y automatizadas de la implementación de la automatización de la interfaz de usuario en un control o una aplicación (los resultados se pueden registrar). Puede integrar la aplicación en el código de prueba y realizar comprobaciones regulares y automatizadas de los escenarios de automatización de la interfaz de usuario. Esta herramienta es útil para comprobar que los cambios en las aplicaciones con características establecidas no tienen nuevos problemas o regresiones en áreas más allá de las nuevas características.

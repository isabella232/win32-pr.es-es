---
description: Información general sobre cómo usar Automatización de la interfaz de usuario y otras herramientas para probar las aplicaciones.
title: Pruebas de accesibilidad
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0cc1d118c84e2689b6cf329da29bb518a566fb8588c311229be17fcd28825ddc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896585"
---
# <a name="testing-for-accessibility"></a>Pruebas de accesibilidad

El acceso mediante programación y el acceso con teclado son requisitos críticos para admitir la accesibilidad en la aplicación. Probar la accesibilidad de las aplicaciones de Windows, las herramientas de tecnología de asistencia (AT) y los marcos de interfaz de usuario es fundamental para garantizar una experiencia de usuario correcta para las personas con diversas discapacidades y limitaciones (como la visión, el aprendizaje, la movilidad y las discapacidades de lenguaje y comunicación), o aquellos que simplemente prefieren usar un teclado.

Sin el acceso adecuado a través de AT, como lectores de pantalla y teclados en pantalla, los usuarios con visión, aprendizaje, movilidad y discapacidades o limitaciones del lenguaje o la comunicación (y los usuarios que simplemente prefieren usar el teclado) no podrán usar la aplicación.

En esta sección se describen las diversas herramientas que se pueden usar para probar la implementación de accesibilidad de Windows aplicaciones web.

> [!NOTE]
> También es importante realizar pruebas manuales para comprobar el acceso mediante teclado a la aplicación.

## <a name="tools"></a>Herramientas

[Accesibilidad Ideas: ayuda](https://accessibilityinsights.io/) a los desarrolladores a encontrar y corregir problemas de accesibilidad tanto en sitios web como Windows aplicaciones.

- [Accessibility Ideas for Web](https://accessibilityinsights.io/docs/web/overview) es una extensión para Chrome y [Microsoft Edge Insider](https://www.microsoftedgeinsider.com) que ayuda a los desarrolladores a encontrar y corregir problemas de accesibilidad en sitios y aplicaciones web. Admite dos escenarios principales:
  - **FastPass:** un proceso ligero de dos pasos que ayuda a los desarrolladores a identificar problemas comunes de accesibilidad de alto impacto en menos de cinco minutos.  
  - **Evaluación:** permite a cualquier persona comprobar que un sitio web cumple al 100 % con las directrices y estándares de accesibilidad. [La Ideas](https://accessibilityinsights.io/) accesibilidad también le permite revisar Automatización de la interfaz de usuario elementos, propiedades, patrones de control y eventos (de forma similar a las herramientas heredadas [Inspect](/windows/desktop/winauto/inspect-objects) y [AccEvent](/windows/desktop/winauto/accessible-event-watcher) que se describen en la sección siguiente).

- [La Ideas](https://accessibilityinsights.io/docs/windows/overview) Windows ayuda a los desarrolladores a encontrar y corregir problemas de accesibilidad en Windows aplicaciones. La herramienta admite tres escenarios principales:
  - **Live Inspect** permite a los desarrolladores comprobar que un elemento de una aplicación tiene las propiedades de Automatización de la interfaz de usuario con solo mantener el puntero sobre el elemento o establecer el foco del teclado en él.
  - **FastPass:** un proceso ligero de dos pasos que ayuda a los desarrolladores a identificar problemas comunes de accesibilidad de alto impacto en menos de cinco minutos.
  - **La solución de** problemas le permite diagnosticar y corregir problemas de accesibilidad específicos.

### <a name="legacy-testing-tools"></a>Herramientas de prueba heredadas

Las siguientes herramientas siguen estando disponibles en el SDK de Windows y se documentan aquí para obtener soporte técnico continuo, pero se recomienda realizar la transición a [Accessibility Ideas](https://accessibilityinsights.io/).

- [Inspeccionar:](/windows/desktop/winauto/inspect-objects)permite ver los datos de accesibilidad de cualquier elemento de la interfaz de usuario. Resulta especialmente útil para garantizar que las propiedades y los patrones de control se establecen correctamente al extender un control común o crear un control personalizado.
- [Accessible Event Watcher (AccEvent):](/windows/desktop/winauto/accessible-event-watcher)examina los datos de accesibilidad para validar los elementos de la interfaz de usuario de la aplicación y asegurarse de que los elementos de la interfaz de usuario genera eventos Microsoft Active Accessibility y Automatización de la interfaz de usuario adecuados en los eventos de la interfaz de usuario. AccEvent se usa normalmente para depurar problemas y validar que los controles personalizados y extendidos funcionan correctamente.
- [AccScope:](/windows/desktop/winauto/accscope)permite la evaluación visual de la accesibilidad de una aplicación durante las primeras fases de diseño y desarrollo. AccScope ayuda a visualizar cómo un lector de pantalla usa Automatización de la interfaz de usuario información proporcionada por una aplicación y muestra dónde agregar información o soporte técnico a la aplicación puede mejorar su accesibilidad.
- [Comprobador de accesibilidad de la](/windows/desktop/winauto/ui-accessibility-checker)interfaz de usuario: comprueba que se cumplen los requisitos clave de accesibilidad de la interfaz de usuario en una aplicación. AccChecker incluye comprobaciones de verificación para Automatización de la interfaz de usuario, Microsoft Active Accessibility y Aplicaciones de Internet enriquecciones accesibles (ARIA). Puede proporcionar una comprobación estática de errores, como nombres que faltan, problemas de árbol, etc. Ayuda a comprobar el acceso mediante programación e incluye características avanzadas para automatizar las pruebas de accesibilidad.
- [Automatización de la interfaz de usuario Comprobar:](/windows/desktop/winauto/ui-automation-verify)un marco para realizar pruebas manuales y automatizadas de la implementación de Automatización de la interfaz de usuario en un control o aplicación (se pueden registrar los resultados). Puede integrar la aplicación en el código de prueba y realizar pruebas periódicas y automatizadas o comprobaciones de acceso Automatización de la interfaz de usuario escenarios. Esta herramienta es útil para comprobar que los cambios en las aplicaciones con características establecidas no tienen nuevos problemas o regresiones en áreas más allá de las nuevas características.

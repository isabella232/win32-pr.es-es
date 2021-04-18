---
title: 'Herramientas de accesibilidad: AccChecker (comprobador de accesibilidad de IU)'
description: Describe AccChecker (comprobador de accesibilidad de IU), una herramienta para probar la automatización de la interfaz de usuario de una aplicación o la implementación de Microsoft Active Accessibility (MSAA).
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI Accessibility Checker
- AccChecker
- Implementación de automatización de la interfaz de usuario, prueba
- Implementación de UIA, pruebas
- Implementación de Microsoft Active Accessibility, pruebas
- Implementación de MSAA, pruebas
- probar la automatización de la interfaz de usuario
- probar UIA
- probar Microsoft Active Accessibility
- prueba de MSAA
- Herramientas de prueba de UIA
- Herramientas de pruebas de UI Automation
- Herramientas de pruebas de MSAA
- Herramientas de prueba de Microsoft Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "105704905"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>Herramientas de accesibilidad: AccChecker (comprobador de accesibilidad de IU)

**AccChecker** (comprobador de accesibilidad de IU) comprueba que se cumplen los requisitos de accesibilidad de la interfaz de usuario clave en el diseño y la implementación de la automatización de la interfaz de usuario (UIA) o Microsoft Active ACCESSIBILITY (MSAA) independientemente del marco de interfaz de usuario subyacente. **AccChecker** también incluye un conjunto de comprobaciones de accesibilidad Web.

**AccChecker** proporciona los siguientes niveles de funcionalidad:

- Aplicación GUI de Windows que admite pruebas manuales, registro de mensajes y generación de supresiones.
- Una API que se utiliza en marcos de pruebas automatizadas.
- Aplicación de consola que admite la automatización de pruebas no administradas en escenarios donde no se puede usar la API administrada **AccChecker** .

Todos los niveles de funcionalidad de **AccChecker** proporcionan rutinas para comprobar el acceso mediante programación a Microsoft Active Accessibility, generación de eventos mediante programación, diseño de control y navegación mediante el teclado. **AccChecker** también proporciona un servicio básico de transcripción de lector de pantalla.

**AccChecker** se instala con el kit de desarrollo de software (SDK) de Windows. Se encuentra en la \\ carpeta bin \\ < *version* > \\ < *Platform* > \\ AccChecker de la ruta de instalación del SDK.

> [!NOTE]
> **AccChecker** es una herramienta heredada. En su lugar, se recomienda usar [información de accesibilidad](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisitos

Requiere .NET Framework 2,0 o posterior.

**AccChecker** se puede usar para examinar los datos de accesibilidad de los sistemas que no tienen automatización de la interfaz de usuario de Microsoft, pero solo pueden examinar las propiedades de Microsoft Active Accessibility. Para examinar la automatización de la interfaz de usuario, la automatización de la interfaz de usuario debe estar presente en el sistema. Para obtener más información, vea la sección "requirements" de automatización de la [interfaz de usuario](entry-uiauto-win32.md).

**AccChecker** se instala como parte del conjunto general de herramientas en el SDK de Windows, no se distribuye como una descarga independiente de exe. El Windows SDK incluye todas las herramientas relacionadas con la accesibilidad que se documentan en esta sección. [Obtiene el Windows SDK.](https://developer.microsoft.com/) (También hay un archivo de descarga de SDK vinculado desde esa página, si necesita una versión anterior).

## <a name="related-topics"></a>Temas relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Inspeccionar](inspect-objects.md)
- [Herramientas de pruebas](testing-tools.md)
- [UI Automation Verify](ui-automation-verify.md)

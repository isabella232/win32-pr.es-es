---
title: 'Herramientas de accesibilidad: AccChecker (Comprobador de accesibilidad de la interfaz de usuario)'
description: Describe AccChecker (Comprobador de accesibilidad de la interfaz de usuario), una herramienta para probar la implementación de Automatización de la interfaz de usuario o Microsoft Active Accessibility (MSAA) de una aplicación.
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI Accessibility Checker
- AccChecker
- Automatización de la interfaz de usuario implementación, pruebas
- Implementación de UIA, pruebas
- Microsoft Active Accessibility implementación, pruebas
- Implementación de MSAA, pruebas
- pruebas Automatización de la interfaz de usuario
- prueba de UIA
- pruebas Microsoft Active Accessibility
- prueba de MSAA
- Herramientas de prueba de UIA
- Automatización de la interfaz de usuario de pruebas
- Herramientas de prueba de MSAA
- Microsoft Active Accessibility herramientas de pruebas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070592"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>Herramientas de accesibilidad: AccChecker (Comprobador de accesibilidad de la interfaz de usuario)

**AccChecker** (Comprobador de accesibilidad de la interfaz de usuario) comprueba que se cumplen los requisitos clave de accesibilidad de la interfaz de usuario en el diseño y la implementación de Automatización de la interfaz de usuario (UIA) o Microsoft Active Accessibility (MSAA) independientemente del marco de interfaz de usuario subyacente. **AccChecker también** incluye un conjunto de comprobaciones de accesibilidad web.

**AccChecker proporciona** los siguientes niveles de funcionalidad:

- Una Windows GUI que admite pruebas manuales, registro de mensajes y generación de supresión.
- Una API para su uso en marcos de pruebas automatizadas.
- Una aplicación de consola que admite automatizaciones de pruebas no administradas para escenarios en los que no se puede usar la API administrada de **AccChecker.**

Todos los niveles **de funcionalidad accChecker** proporcionan rutinas para comprobar Microsoft Active Accessibility mediante programación, la generación de eventos mediante programación, el diseño del control y la navegación mediante teclado. **AccChecker también proporciona** un servicio básico de transcripción del lector de pantalla.

**AccChecker se** instala con Windows Software Development Kit (SDK). Se encuentra en la carpeta AccChecker de la plataforma de versión \\ \\ <  > \\ <  > \\ bin de la ruta de instalación del SDK.

> [!NOTE]
> **AccChecker es** una herramienta heredada. En su lugar, se [recomienda usar Ideas](https://accessibilityinsights.io/) accesibilidad.

## <a name="requirements"></a>Requisitos

Requiere .NET Framework 2.0 o posterior.

**AccChecker se** puede usar para examinar los datos de accesibilidad en sistemas que no tienen Microsoft Automatización de la interfaz de usuario, pero que solo pueden examinar las Microsoft Active Accessibility de acceso. Para examinar Automatización de la interfaz de usuario, Automatización de la interfaz de usuario debe estar presente en el sistema. Para obtener más información, vea la sección "Requisitos" [de Automatización de la interfaz de usuario](entry-uiauto-win32.md).

**AccChecker** se instala como parte del conjunto general de herramientas en el SDK de Windows, no se distribuye como una descarga de exe independiente. El SDK Windows incluye todas las herramientas relacionadas con la accesibilidad documentadas en esta sección. [Obtenga el SDK Windows.](https://developer.microsoft.com/) (También hay un archivo de descarga del SDK vinculado desde esa página, si necesita una versión anterior).

## <a name="related-topics"></a>Temas relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Inspeccionar](inspect-objects.md)
- [Herramientas de prueba](testing-tools.md)
- [UI Automation Verify](ui-automation-verify.md)

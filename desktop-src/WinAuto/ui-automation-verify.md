---
title: Automatización de la interfaz de usuario verify (UIA Verify)
description: Automatización de la interfaz de usuario Verify (UIA Verify) es un marco de pruebas para las pruebas manuales y automatizadas de la implementación de microsoft o la aplicación de un control de Microsoft Automatización de la interfaz de usuario.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- UI Automation Verify
- Comprobación de UIA
- Automatización de la interfaz de usuario implementación, pruebas
- pruebas Automatización de la interfaz de usuario
- Herramientas de prueba de UIA
- Automatización de la interfaz de usuario herramientas de prueba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070580"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Herramientas de accesibilidad: Automatización de la interfaz de usuario comprobación (comprobación de UIA)

**Automatización de la interfaz de usuario Verify (UIA Verify)** es un marco de pruebas para las pruebas manuales y automatizadas de la implementación de Microsoft Automatización de la interfaz de usuario. La mayor parte de la funcionalidad del marco de pruebas procede de un archivo DLL denominado WUIATestLibrary.dll. Este archivo DLL contiene el código para probar funcionalidades Automatización de la interfaz de usuario y también admite el registro de los resultados de pruebas. Puede integrar la aplicación en el código de prueba y realizar pruebas periódicas y automatizadas o comprobaciones de acceso Automatización de la interfaz de usuario escenarios.

**UIA Verify** se instala con Windows Software Development Kit (SDK). Se encuentra en la carpeta \\ \\ <  > \\ <  > \\ UIAVerify de la plataforma bin version de la ruta de instalación del SDK (VisualUIAVerifyNative.exe).

**UIA Verify** consta de una API denominada biblioteca Automatización de la interfaz de usuario test y una interfaz gráfica de usuario denominada Visual **Automatización de la interfaz de usuario Verify**. Estos se describen en los temas siguientes.

> [!NOTE]
> **Automatización de la interfaz de usuario Verify** es una herramienta heredada. En su [lugar,](https://accessibilityinsights.io/) se recomienda usar Ideas accesibilidad.

## <a name="requirements"></a>Requisitos

Automatización de la interfaz de usuario debe estar presente en el sistema. Para obtener más información, vea la sección "Requisitos" [de Automatización de la interfaz de usuario](entry-uiauto-win32.md).

**UIA Verify** se instala como parte del conjunto general de herramientas del SDK de Windows, no se distribuye como una descarga independiente. El SDK Windows incluye todas las herramientas relacionadas con la accesibilidad que se documentan en esta sección. [Obtenga el SDK Windows.](https://developer.microsoft.com/) (También hay un archivo de descarga del SDK vinculado desde esa página, si necesita una versión anterior).

Para ejecutar **UIA Verify** como herramienta visual, busque VisualUIAVerifyNative.exe en la carpeta \\ bin \\ < *platform* > \\ UIAVerify y ejecutarla (normalmente no tiene que ejecutar como administrador). Para obtener más información, [vea Visual Automatización de la interfaz de usuario Verify](visual-ui-automation-verify.md). Para usar las bibliotecas, vea Automatización de la interfaz de usuario [Test Library](ui-automation-test-library.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Accessible Event Watcher](accessible-event-watcher.md)
</dt> <dt>

[Inspeccionar](inspect-objects.md)
</dt> <dt>

[Herramientas de prueba](testing-tools.md)
</dt> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





---
title: Comprobación de automatización de la interfaz de usuario (comprobar UIA)
description: La comprobación de la automatización de la interfaz de usuario (UIA Verify) es un marco de pruebas para pruebas manuales y automatizadas de la implementación de una aplicación o un control de la automatización de la interfaz de usuario de Microsoft.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- UI Automation Verify
- Comprobar UIA
- Implementación de automatización de la interfaz de usuario, prueba
- probar la automatización de la interfaz de usuario
- Herramientas de prueba de UIA
- Herramientas de pruebas de UI Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420349"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Herramientas de accesibilidad: comprobación de UI Automation (UIA Verify)

La comprobación de la automatización de la **interfaz de usuario (UIA Verify)** es un marco de pruebas para pruebas manuales y automatizadas de la implementación de una aplicación o un control de la automatización de la interfaz de usuario de Microsoft. La mayor parte de la funcionalidad del marco de pruebas procede de un archivo DLL denominado WUIATestLibrary.dll. Este archivo DLL contiene el código para probar la funcionalidad de automatización de la interfaz de usuario específica y también admite el registro de los resultados de pruebas. Puede integrar la aplicación en el código de prueba y realizar comprobaciones regulares y automatizadas de los escenarios de automatización de la interfaz de usuario.

**UIA Verify** se instala con el kit de desarrollo de software (SDK) de Windows. Se encuentra en la \\ carpeta bin \\ < *version* > \\ < *Platform* > \\ UIAVerify de la ruta de instalación de SDK (VisualUIAVerifyNative.exe).

**UIA Verify** consta de una API denominada Biblioteca de pruebas de automatización de la interfaz de usuario y una interfaz de GUI denominada visual **UI Automation Verify**. Se describen en los temas siguientes.

> [!NOTE]
> La comprobación de automatización de la **interfaz de usuario** es una herramienta heredada. En su lugar, se recomienda usar [información de accesibilidad](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisitos

La automatización de la interfaz de usuario debe estar presente en el sistema. Para obtener más información, vea la sección "requirements" de automatización de la [interfaz de usuario](entry-uiauto-win32.md).

**UIA Verify** se instala como parte del conjunto general de herramientas en el Windows SDK, no se distribuye como una descarga independiente. El Windows SDK incluye todas las herramientas relacionadas con la accesibilidad que se documentan en esta sección. [Obtiene el Windows SDK.](https://developer.microsoft.com/) (También hay un archivo de descarga de SDK vinculado desde esa página, si necesita una versión anterior).

Para ejecutar **UIA Verify** como una herramienta visual, busque VisualUIAVerifyNative.exe en la \\ carpeta bin UIAVerify de la \\ < *plataforma* > \\ y ejecútelo (normalmente no tiene que ejecutarse como administrador). Para obtener más información, consulte Comprobación de la automatización de la [interfaz de usuario visual](visual-ui-automation-verify.md). Para usar las bibliotecas, vea [UI Automation test Library](ui-automation-test-library.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Accessible Event Watcher](accessible-event-watcher.md)
</dt> <dt>

[Inspeccionar](inspect-objects.md)
</dt> <dt>

[Herramientas de pruebas](testing-tools.md)
</dt> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





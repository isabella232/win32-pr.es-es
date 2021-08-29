---
title: Registrar componentes
description: Registrar componentes
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58a987bba4ef7767cfc7346730f5f22e2c1eaab8ae3eed76cd33be0ad778902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992305"
---
# <a name="registering-components"></a>Registrar componentes

Cuando se instalan los siguientes tipos de aplicaciones, se debe agregar información de instalación al Registro, normalmente a través de un programa de instalación:

-   Aplicaciones de servidor
-   Aplicaciones de contenedor o servidor
-   Aplicaciones de contenedor que permiten la vinculación a objetos incrustados

Para las tres instancias, registre la información de la biblioteca COM (DLL) y la información específica de la aplicación.

El archivo DLL registra la información de todos sus componentes mediante la exportación de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Use las siguientes funciones para registrar y anular el registro de un componente:

-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegSetValueEx**](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [**RegEnumKeyEx**](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 
---
title: Registrar componentes
description: Registrar componentes
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078409"
---
# <a name="registering-components"></a>Registrar componentes

Cuando se instalan los siguientes tipos de aplicaciones, se debe agregar información de instalación al registro, normalmente a través de un programa de instalación:

-   Aplicaciones de servidor
-   Aplicaciones de contenedor/servidor
-   Aplicaciones contenedoras que permiten la vinculación a objetos incrustados

Para las tres instancias, registre la información de la biblioteca COM (DLL) y la información específica de la aplicación.

El archivo DLL registra la información de todos sus componentes mediante la exportación de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Utilice las siguientes funciones para registrar y anular el registro de un componente:

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

 

 
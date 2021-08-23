---
title: Uso del Administrador de reinicio
description: En las secciones siguientes se describe el uso de la API de Restart Manager.
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- Restart Manager Restart Mgr , using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90826091aa4a3cdf39e0a1f063a211255ec4ef9cf84b06214eb172150ac3b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010003"
---
# <a name="using-restart-manager"></a>Uso del Administrador de reinicio

En las secciones siguientes se describe el uso de la API de Restart Manager. Las aplicaciones y los servicios también deben seguir las [directrices para aplicaciones y servicios](guidelines-for-applications-and-services.md).

## <a name="using-the-microsoft-windows-installer"></a>Uso de Microsoft Windows Installer

Microsoft [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versión 4.0 es el servicio de instalación de aplicaciones de Windows Vista o Windows Server 2008. Las aplicaciones que usan Windows Installer versión 4.0 para la instalación y el mantenimiento usan automáticamente el Administrador de reinicio para reducir los reinicios del sistema. Los instaladores personalizados también se pueden diseñar para llamar a la API de Restart Manager a fin de apagar y reiniciar aplicaciones y servicios directamente para evitar requerir un reinicio del sistema. En los casos en los que un reinicio del sistema es inevitable, los instaladores pueden usar la función [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) o [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) para programarlo de forma que minimice la interrupción para el usuario. Los paquetes Windows instalador interactivo deben implementar una interfaz de usuario que incluya un [cuadro de diálogo MsiRMFilesInUse.](/windows/desktop/Msi/msirmfilesinuse-dialog) Para obtener más información, consulte [Uso del instalador Windows con el Administrador de](/windows/desktop/Msi/using-windows-installer-with-restart-manager) reinicio en la documentación del SDK Windows Installer.

## <a name="using-the-restart-manager-api-with-custom-installers"></a>Uso de la API de Restart Manager con instaladores personalizados

Los instaladores personalizados, o un paquete Windows Installer que contiene acciones personalizadas que provocan un reinicio del sistema, pueden usar la API de Restart Manager para apagar y reiniciar aplicaciones y servicios.

-   Todas las operaciones que se realizan mediante la API de Restart Manager deben estar asociadas a una sesión. Se puede abrir un máximo de 64 sesiones de Restart Manager por sesión de usuario en el sistema al mismo tiempo. El instalador principal se inicia y finaliza la sesión del Administrador de reinicio. Para obtener más información sobre el uso de Restart Manager con un solo instalador, vea [Using Restart Manager with a Primary Installer](using-restart-manager-with-a-primary-installer.md).
-   Si es necesario para la instalación, uno o varios instaladores secundarios se pueden unir a la sesión del Administrador de reinicio y pueden ejecutarse en proceso o fuera de proceso del instalador principal. Los instaladores secundarios requieren que el instalador principal pueda proporcionar la clave de sesión para unirse a una sesión. Para obtener más información y un ejemplo del uso de instaladores secundarios, vea [Using Restart Manager with a Secondary Installer](using-restart-manager-with-a-secondary-installer.md).
-   Los instaladores interactivos deben implementar una interfaz de usuario que incluya un cuadro de diálogo [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) que pueda pedir a los usuarios que cierren aplicaciones y servicios. Para obtener más información, consulte [Uso del instalador Windows con el Administrador de](/windows/desktop/Msi/using-windows-installer-with-restart-manager) reinicio en la documentación del SDK Windows Installer.
-   Los instaladores pueden llamar a la API de Restart Manager para cambiar, cancelar y obtener el estado de la operación de Restart Manager actual. Para obtener más información, vea los temas siguientes: [Obtener](getting-the-status-of-a-restart-manager-operation.md) el estado de una operación del administrador de reinicio y [Cancelar la operación actual del administrador de reinicio](canceling-the-current-restart-manager-operation.md).
-   Los instaladores no deben deshabilitar el redireccionamiento del sistema de archivos antes de llamar a la API de Restart Manager. Es posible que algunos instaladores de 32 bits se ejecuten en Windows de 64 bits no puedan registrar un archivo en el directorio %windir% \\ system32.

 

 
---
title: Uso del administrador de reinicio
description: En las secciones siguientes se describe el uso de la API del administrador de reinicio.
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- Admin. de reinicio del administrador, uso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ac72edb9f2395bbd67236806c3ab3029372cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904763"
---
# <a name="using-restart-manager"></a>Uso del administrador de reinicio

En las secciones siguientes se describe el uso de la API del administrador de reinicio. Las aplicaciones y los servicios también deben seguir las [instrucciones para aplicaciones y servicios](guidelines-for-applications-and-services.md).

## <a name="using-the-microsoft-windows-installer"></a>Usar el Microsoft Windows Installer

La versión [Microsoft Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4,0 es el servicio de instalación de aplicaciones de Windows Vista o windows Server 2008. Las aplicaciones que utilizan la Windows Installer versión 4,0 para la instalación y el mantenimiento usan automáticamente el administrador de reinicio para reducir los reinicios del sistema. Los instaladores personalizados también pueden diseñarse para que llamen a la API del administrador de reinicio para apagar y reiniciar aplicaciones y servicios directamente para evitar que se reinicie el sistema. En los casos en los que no se puede evitar el reinicio del sistema, los instaladores pueden utilizar la función [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) o [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) para programarlos de forma que se minimice la interrupción para el usuario. Los paquetes Windows Installer interactivos deben implementar una interfaz de usuario que incluya un cuadro de diálogo [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) . Para obtener más información, consulte [uso de Windows Installer con el administrador de reinicio](/windows/desktop/Msi/using-windows-installer-with-restart-manager) en la documentación del SDK de Windows Installer.

## <a name="using-the-restart-manager-api-with-custom-installers"></a>Uso de la API del administrador de reinicio con instaladores personalizados

Los instaladores personalizados, o un paquete de Windows Installer que contiene acciones personalizadas que provocan un reinicio del sistema, pueden usar la API del administrador de reinicio para apagar y reiniciar aplicaciones y servicios.

-   Todas las operaciones que se realizan con la API del administrador de reinicio deben estar asociadas a una sesión. Puede haber un máximo de 64 sesiones del administrador de reinicio por sesión de usuario abiertas en el sistema al mismo tiempo. El instalador principal inicia y finaliza la sesión del administrador de reinicio. Para obtener más información acerca del uso del administrador de reinicio con un solo instalador, consulte [uso del administrador de reinicio con un instalador principal](using-restart-manager-with-a-primary-installer.md).
-   Si es necesario para la instalación, uno o varios instaladores secundarios pueden unirse a la sesión del administrador de reinicio y pueden ejecutarse en proceso o fuera de proceso del instalador principal. Los instaladores secundarios requieren que el instalador principal proporcione la clave de sesión para unirse a una sesión. Para obtener más información y un ejemplo del uso de instaladores secundarios, consulte [uso del administrador de reinicio con un instalador secundario](using-restart-manager-with-a-secondary-installer.md).
-   Los instaladores interactivos deben implementar una interfaz de usuario que incluye un cuadro de diálogo [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) que puede pedir a los usuarios que cierren las aplicaciones y los servicios. Para obtener más información, consulte [uso de Windows Installer con el administrador de reinicio](/windows/desktop/Msi/using-windows-installer-with-restart-manager) en la documentación del SDK de Windows Installer.
-   Los instaladores pueden llamar a la API del administrador de reinicio para cambiar, cancelar y obtener el estado de la operación del administrador de reinicio actual. Para obtener más información, vea los temas siguientes: [obtener el estado de una operación del administrador de reinicio](getting-the-status-of-a-restart-manager-operation.md) y [cancelar la operación actual del administrador de reinicio](canceling-the-current-restart-manager-operation.md).
-   Los instaladores no deben deshabilitar la redirección del sistema de archivos antes de llamar a la API del administrador de reinicio. Algunos instaladores de 32 bits que se ejecutan en Windows de 64 bits pueden no poder registrar un archivo en el directorio% WINDIR% \\ system32.

 

 
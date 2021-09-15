---
description: Las aplicaciones que usan Windows Installer 4.0 para la instalación y el mantenimiento en Windows Vista usan automáticamente el Administrador de reinicio para reducir los reinicios del sistema.
ms.assetid: 821739ff-f7a7-4192-ad34-254aa7d74d13
title: Usar Windows instalador con el Administrador de reinicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4160b2241c75ec7305accd1ab4d1295a54fa9f65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473909"
---
# <a name="using-windows-installer-with-restart-manager"></a>Usar Windows instalador con el Administrador de reinicio

Las aplicaciones que usan Windows Installer 4.0 para la instalación y el [](../rstmgr/restart-manager-portal.md) mantenimiento en Windows Vista usan automáticamente el Administrador de reinicio para reducir los reinicios del sistema. El comportamiento predeterminado en Windows Vista es apagar las aplicaciones en lugar de apagar y reiniciar el sistema operativo siempre que sea posible. En los casos en los que un reinicio del sistema es inevitable, los instaladores pueden usar la API [de Restart Manager](../rstmgr/restart-manager-portal.md) para programar reinicios de forma que minimice la interrupción del flujo de trabajo del usuario.

Windows Los desarrolladores del instalador pueden realizar las siguientes acciones para preparar su paquete para trabajar con [el Administrador de reinicio.](../rstmgr/restart-manager-portal.md)

-   Agregue el [cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) al paquete. Si el cuadro de diálogo MsiRMFilesInUse está presente en el paquete, el [](user-interface-levels.md) usuario de Windows Vista que ejecuta una instalación en el nivel de interfaz de usuario de interfaz de usuario completa tiene la opción de cerrar y reiniciar automáticamente las aplicaciones. Un paquete de instalación puede contener información para el cuadro de diálogo MsiRMFilesInUse y el [cuadro de diálogo FilesInUse](filesinuse-dialog.md) . El cuadro de diálogo MsiRMFilesInUse solo se muestra si el paquete está instalado con al menos Windows Installer 4.0 en Windows Vista y, de lo contrario, se omite. Los paquetes existentes que no tienen el cuadro de diálogo MsiRMFilesInUse siguen funcionando mediante el cuadro de diálogo FilesInUse. Se puede usar una transformación de personalización para agregar un cuadro de diálogo MsiRMFilesInUse a los paquetes existentes.

    Los usuarios finales suelen ejecutar instalaciones en el nivel de interfaz de [usuario de interfaz de usuario completa](user-interface-levels.md). Las instalaciones básicas de nivel de interfaz [](../rstmgr/restart-manager-portal.md) de usuario o de interfaz de usuario reducidas dan al usuario la opción de usar el Administrador de reinicio para reducir los reinicios del sistema incluso si el cuadro de diálogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) no está presente. Las instalaciones silenciosas de nivel de interfaz de usuario siempre apagan aplicaciones y servicios, y en Windows Vista, use siempre el Administrador de reinicio.

-   Registre las aplicaciones para un reinicio mediante [**la función RegisterApplicationRestart.**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) Restart Manager solo puede reiniciar las aplicaciones que se han registrado para el reinicio. Restart Manager reinicia las aplicaciones registradas después de la instalación. Si la instalación requiere un reinicio del sistema, restart Manager reinicia la aplicación registrada después del reinicio del sistema.
-   Especifique INSTALLLOGMODE RMFILESINUSE al habilitar un controlador de interfaz de usuario externo con las funciones \_ [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) y [**MsiSetExternalUIRecord.**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) Windows El instalador enviará un mensaje INSTALLMESSAGE RMFILESINUSE para los controladores externos de la interfaz de usuario \_ que [admiten el Administrador de reinicio.](../rstmgr/restart-manager-portal.md) Si ninguna interfaz de usuario registrada o interna controla el mensaje INSTALLMESSAGE RMFILESINUSE, el instalador envía un mensaje INSTALLMESSAGE FILESINUSE para los controladores de interfaz de usuario que admiten el cuadro de diálogo \_ \_ [FilesInUse.](filesinuse-dialog.md) Para obtener más información, vea [Usar el Administrador de reinicio con una interfaz de usuario externa.](using-restart-manager-with-an-external-ui-.md)
-   Las acciones personalizadas pueden agregar recursos que pertenecen a una [sesión de Restart Manager.](../rstmgr/restart-manager-portal.md) La acción personalizada debe secuenciarse antes de [la acción InstallValidate.](installvalidate-action.md) Las acciones personalizadas pueden usar la propiedad [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md) para obtener la clave de sesión y deben llamar a las funciones [**RmJoinSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmjoinsession) y [**RmEndSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmendsession) de la API de Restart Manager. Las acciones personalizadas no pueden quitar los recursos que pertenecen a una sesión de Restart Manager. Las acciones personalizadas no deben intentar apagar ni reiniciar aplicaciones mediante las funciones [**RmShutdown**](/windows/win32/api/restartmanager/nf-restartmanager-rmshutdown), [**RmGetList**](/windows/win32/api/restartmanager/nf-restartmanager-rmgetlist) y [**RmRestart.**](/windows/win32/api/restartmanager/nf-restartmanager-rmrestart)
-   Los autores de paquetes pueden basar una condición en la [tabla LaunchCondition](launchcondition-table.md) en la propiedad [**MsiSystemRebootPending**](msisystemrebootpending.md) para evitar la instalación de su paquete cuando hay pendiente un reinicio del sistema.
-   Los autores y administradores de paquetes pueden controlar la interacción del instalador y el administrador de reinicio de Windows mediante las propiedades [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md), [**MSIDISABLERMRESTART,**](msidisablermrestart.md) [**MSIRMSHUTDOWN**](msirmshutdown.md) y la directiva [DisableAutomaticApplicationShutdown.](disableautomaticapplicationshutdown.md)
-   Las aplicaciones y los servicios deben seguir las instrucciones descritas en la [sección Uso del Administrador](../rstmgr/using-restart-manager.md) de reinicio de la documentación de [Restart](../rstmgr/restart-manager-portal.md) Manager.

 

 

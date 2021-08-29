---
description: Las funciones, tablas y propiedades del instalador de Windows que se enumeran en esta página no son compatibles con Windows Installer&\# 160;3.1 y versiones anteriores.
ms.assetid: fbf75dbe-3fa1-424b-83bb-cfd0b179107c
title: No se admite en Windows Installer 3.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b33334133fafa5e37f8bd7dfe4edfd30962c4e605bf2a675661e9d57aca4184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145588"
---
# <a name="not-supported-in-windows-installer-31"></a>No se admite en Windows Installer 3.1

Las Windows, las tablas y las propiedades del instalador que se enumeran en esta página no son compatibles con Windows Installer 3.1 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admite la característica. Consulte la documentación principal para determinar qué Windows installer es necesaria para una característica determinada. Para obtener información sobre otras versiones Windows Installer, vea [Novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows El instalador 3.1 está disponible para Windows Server 2003, Windows XP o Windows 2000. Para obtener una lista de todas las versiones Windows installer y redistribuibles, vea Versiones publicadas [de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 3.1 y versiones anteriores.

[Funciones del instalador](installer-functions.md)

-   [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)

[Propiedades](properties.md)

-   [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)
-   [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md)
-   [**MSIDISABLERMRESTART**](msidisablermrestart.md)
-   [**MsiLogFileLocation**](msilogfilelocation.md)
-   [**MsiLogging**](msilogging.md)
-   [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
-   [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)
-   [**MSIRMSHUTDOWN**](msirmshutdown.md)
-   [**MsiRunningElevated**](msirunningelevated-.md)
-   [**MsiSystemRebootPending**](msisystemrebootpending.md)
-   [**MsiTabletPC**](msitabletpc.md)
-   [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)

[Propiedades de información de resumen](summary-information-stream-reference.md)

-   La [**propiedad Resumen de recuento de palabras**](word-count-summary.md) tiene nuevos bits de marca para especificar si la instalación del paquete requiere privilegios elevados.

[Directiva del sistema](system-policy.md)

-   [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
-   [DisableLoggingFromPackage](disableloggingfrompackage.md)

[Tablas de base de datos](database-tables.md)

-   [Tabla de métodos abreviados](shortcut-table.md)

    Nuevas columnas: DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL y DescriptionResourceId

[Cuadros de diálogo](dialog-boxes.md)

-   [Cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)

[Atributos de control](control-attributes.md)

-   [ElevationShield](elevationshield-attribute.md)

[ControlEvents](control-events.md)

-   [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)

[Tipos de mensajes de interfaz de usuario externos](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

-   INSTALLLOGMODE \_ RMFILESINUSE

[Windows Instalador en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   **Atributo msidbComponentAttributesDisableRegistryReflection** en [la tabla de componentes](component-table.md)

[Interfaz de Automation](automation-interface.md)

-   Métodos del [ **objeto Installer**](installer-object.md)

    -   [**Installer.AdvertiseProduct**](installer-advertiseproduct.md)
    -   [**Installer.AdvertiseScript**](installer-advertisescript.md)
    -   [**Installer.CreateAdvertiseScript**](installer-createadvertisescript.md)
    -   [**Installer.ProvideAssembly**](installer-provideassembly.md)

-   Propiedades del [ **objeto Installer**](installer-object.md)

    -   [**Installer.PatchFiles**](installer-patchfiles.md)
    -   [**Installer.ProductElevated**](installer-productelevated.md)
    -   [**Installer.ProductInfoFromScript**](installer-productinfofromscript.md)

## <a name="notes"></a>Notas

El servicio Windows Installer debe ejecutarse en Windows Vista para habilitar el uso de la aplicación de revisiones del Administrador de [reinicio,](../rstmgr/restart-manager-portal.md) [*control*](u-gly.md)de cuentas de usuario y Control de cuentas de [usuario (UAC).](user-account-control--uac--patching.md) Para obtener información, vea Usar [Windows instalador](using-windows-installer-with-restart-manager.md) con el Administrador de reinicio y Usar Windows Installer [con UAC](using-windows-installer-with-uac.md) y aplicación de revisiones de control de cuentas [de usuario (UAC).](user-account-control--uac--patching.md)

Windows Installer 3.1 admite Windows File Protection (WFP) y no admite Windows Resource Protection (WRP). WRP en Windows Server 2008 y Windows Vista reemplaza a WFP en Windows Server 2003, Windows XP y Windows 2000. Para obtener información sobre Windows Installer y WFP, vea [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).

 

 

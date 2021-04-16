---
description: Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer&\# 160; 3.1 y versiones anteriores.
ms.assetid: fbf75dbe-3fa1-424b-83bb-cfd0b179107c
title: No se admite en Windows Installer 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a221d80f56c5737cc5ae92a040a005ae42449e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678429"
---
# <a name="not-supported-in-windows-installer-31"></a>No se admite en Windows Installer 3,1

Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer 3,1 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admita la característica. Consulte la documentación principal para determinar qué versión de Windows Installer es necesaria para una característica determinada. Para obtener información sobre otras versiones de Windows Installer, vea [novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 3,1 está disponible para Windows Server 2003, Windows XP o Windows 2000. Para obtener una lista de todas las versiones de Windows Installer y redistribuibles, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 3,1 y versiones anteriores.

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

[Propiedades de información de Resumen](summary-information-stream-reference.md)

-   La [**propiedad de Resumen de recuento de palabras**](word-count-summary.md) tiene nuevos bits de marca para especificar si la instalación del paquete requiere privilegios elevados.

[Directiva del sistema](system-policy.md)

-   [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
-   [DisableLoggingFromPackage](disableloggingfrompackage.md)

[Tablas de base de datos](database-tables.md)

-   [Tabla de acceso directo](shortcut-table.md)

    Nuevas columnas: DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL y DescriptionResourceId

[Cuadros de diálogo](dialog-boxes.md)

-   [Cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)

[Atributos de control](control-attributes.md)

-   [ElevationShield](elevationshield-attribute.md)

[ControlEvents](control-events.md)

-   [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)

[Tipos de mensajes de interfaz de usuario externos](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

-   INSTALLLOGMODE \_ RMFILESINUSE

[Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   atributo **msidbComponentAttributesDisableRegistryReflection** en la [tabla de componentes](component-table.md)

[Interfaz de automatización](automation-interface.md)

-   Métodos del [ **objeto Installer**](installer-object.md)

    -   [**Instalador. AdvertiseProduct**](installer-advertiseproduct.md)
    -   [**Instalador. AdvertiseScript**](installer-advertisescript.md)
    -   [**Instalador. CreateAdvertiseScript**](installer-createadvertisescript.md)
    -   [**Instalador. ProvideAssembly**](installer-provideassembly.md)

-   Propiedades del [ **objeto Installer**](installer-object.md)

    -   [**Instalador. PatchFiles**](installer-patchfiles.md)
    -   [**Instalador. ProductElevated**](installer-productelevated.md)
    -   [**Instalador. ProductInfoFromScript**](installer-productinfofromscript.md)

## <a name="notes"></a>Notas

El servicio de Windows Installer se debe ejecutar en Windows Vista para habilitar el uso del [Administrador de reinicio](../rstmgr/restart-manager-portal.md), el [*control de cuentas de usuario*](u-gly.md)y la revisión de control de cuentas de [usuario (UAC)](user-account-control--uac--patching.md). Para obtener más información, consulte [uso de Windows Installer con el administrador de reinicio](using-windows-installer-with-restart-manager.md) y [uso de Windows Installer con la revisión de UAC](using-windows-installer-with-uac.md) y control de [cuentas de usuario (UAC)](user-account-control--uac--patching.md).

Windows Installer 3,1 es compatible con la protección de archivos de Windows (WFP) y no es compatible con Protección de recursos de Windows (WRP). WRP en Windows Server 2008 y Windows Vista reemplaza WFP en Windows Server 2003, Windows XP y Windows 2000. Para obtener información acerca de Windows Installer y WFP, vea [usar Windows Installer y protección de recursos de Windows](windows-resource-protection-on-windows-vista.md).

 

 

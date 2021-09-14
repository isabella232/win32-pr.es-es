---
description: Las Windows Installer de Windows, tablas y propiedades enumeradas en esta página no son compatibles con Windows Installer&\# 160;4.5 y versiones anteriores.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: No se admite en Windows Installer 4.5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d1d1b3039c4e51c7233f98ee2e41afb308a822
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161475"
---
# <a name="not-supported-in-windows-installer-45"></a>No se admite en Windows Installer 4.5

Las Windows, las tablas y las propiedades del instalador que se enumeran en esta página no son compatibles con Windows Installer 4.5 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admite la característica. Consulte la documentación principal para determinar qué versión Windows installer es necesaria para una característica determinada. Para obtener información sobre otras Windows installer, vea [Novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows El instalador 4.5 está disponible como redistribuible para Windows Server 2008, Windows Vista con Service Pack 1 (SP1), Windows XP con Service Pack 2 (SP2) y versiones posteriores, y Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores. Para obtener una lista completa de todas las versiones Windows Installer y redistribuibles, vea Versiones publicadas [de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 4.5 y versiones anteriores.

[Acciones estándar](standard-actions.md)

-   [MsiConfigureServices](msiconfigureservices-action.md)

[Funciones del instalador](installer-functions.md)

-   [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[Tipos de datos de columna](column-data-types.md)

-   [**FormattedSDDLText**](formattedsddltext.md)

[Propiedades](properties.md)

-   [**MSIFASTINSTALL**](msifastinstall.md)
-   [**MSIINSTALLPERUSER**](msiinstallperuser.md)

[Tablas de base de datos](database-tables.md)

-   [Tabla MsiServiceConfig](msiserviceconfig-table.md)
-   [Tabla MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
-   [Tabla MsiShortcutProperty](msishortcutproperty-table.md)
-   [Tabla MsiLockPermissionsEx](msilockpermissionsex-table.md)

[ControlEvents](control-events.md)

-   [MsiPrint ControlEvent](msiprint-controlevent.md)
-   [MsiLaunchApp ControlEvent](msilaunchapp-controlevent.md)

[Controles](controls.md)

-   [Hyperlink (Control)](hyperlink-control.md)
-   [Compatibilidad del control de](bitmap-control.md) mapa de bits con formatos de archivo de imagen WIC

[Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interfaz de Automation](automation-interface.md)

-   Propiedades del objeto [ **Installer**](installer-object.md)

    -   [**Installer.ClientsEx**](installer-clientsex.md)
    -   [**Installer.ComponentsEx**](installer-componentsex.md)
    -   [**Installer.ComponentPathEx**](installer-componentpathex.md)

-   Propiedades del [ **objeto Component**](components.md)

    -   [**Component.ComponentCode**](component-componentcode.md)
    -   [**Component.UserSID**](component-usersid.md)
    -   [**Component.Context**](component-context.md)

-   Propiedades del [ **objeto cliente**](client.md)

    -   [**Client.ProductCode**](client-productcode.md)
    -   [**Client.ComponentCode**](client-componentcode.md)
    -   [**Client.UserSID**](client-usersid.md)
    -   [**Client.Context**](client-context.md)

-   Propiedades del [**objeto ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo.Path**](componentinfo-path.md)
    -   [**ComponentInfo.State**](componentinfo-state.md)

## <a name="notes"></a>Notas

Windows El instalador 4.5 no admite algunas características que permiten instalar un único paquete de instalación en el contexto de instalación por equipo o por usuario. Para obtener más información, vea [Single Package Authoring](single-package-authoring.md).

Windows El instalador 4.5 no admite algunas opciones de configuración de servicios que pueden permitir que un paquete personalice los [servicios](../services/services.md) en un equipo. Para obtener más información, vea [Using Services Configuration](using-services-configuration.md).

Windows El instalador 4.5 no admite algunas características que permiten al instalador de Windows proteger nuevas cuentas, servicios [Windows,](../services/services.md)archivos, carpetas y claves del Registro. Para obtener información, vea [Securing Resources](securing-resources-.md).

Windows El instalador 4.5 no admite algunas características que permiten a la instalación enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de clave para el componente. Para obtener más información, [vea Enumerar componentes](enumerating-components-.md).

 

 

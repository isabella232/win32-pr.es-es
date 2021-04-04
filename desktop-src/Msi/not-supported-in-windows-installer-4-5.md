---
description: Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer&\# 160; 4.5 y versiones anteriores.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: No se admite en Windows Installer 4,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d1d1b3039c4e51c7233f98ee2e41afb308a822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811815"
---
# <a name="not-supported-in-windows-installer-45"></a>No se admite en Windows Installer 4,5

Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer 4,5 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admita la característica. Consulte la documentación principal para determinar qué versión de Windows Installer es necesaria para una característica determinada. Para obtener información sobre otras versiones de Windows Installer, vea [novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 4,5 está disponible como paquete redistribuible para Windows Server 2008, Windows Vista con Service Pack 1 (SP1), Windows XP con Service Pack 2 (SP2) y versiones posteriores, y Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores. Para obtener una lista completa de todas las versiones de Windows Installer y redistribuibles, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 4,5 y versiones anteriores.

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

-   [MsiPrint ControlEvent,](msiprint-controlevent.md)
-   [MsiLaunchApp ControlEvent,](msilaunchapp-controlevent.md)

[Controles](controls.md)

-   [Control de hipervínculo](hyperlink-control.md)
-   Compatibilidad del [control de mapa de bits](bitmap-control.md) con los formatos de archivo de imagen WIC

[Evaluadores de coherencia interna-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interfaz de automatización](automation-interface.md)

-   Propiedades del [ **objeto Installer**](installer-object.md)

    -   [**Instalador. ClientsEx**](installer-clientsex.md)
    -   [**Instalador. ComponentsEx**](installer-componentsex.md)
    -   [**Instalador. ComponentPathEx**](installer-componentpathex.md)

-   Propiedades del [ **objeto de componente**](components.md)

    -   [**Componente. ComponentCode**](component-componentcode.md)
    -   [**Componente. UserSID**](component-usersid.md)
    -   [**Componente. Context**](component-context.md)

-   Propiedades del [ **objeto de cliente**](client.md)

    -   [**Client. ProductCode**](client-productcode.md)
    -   [**Client. ComponentCode**](client-componentcode.md)
    -   [**Client. UserSID**](client-usersid.md)
    -   [**Client. Context**](client-context.md)

-   Propiedades del objeto [**ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo. Path**](componentinfo-path.md)
    -   [**ComponentInfo. State**](componentinfo-state.md)

## <a name="notes"></a>Notas

Windows Installer 4,5 no admite algunas características que permiten instalar un único paquete de instalación en el contexto de instalación por equipo o por usuario. Para obtener más información, vea [creación de un solo paquete](single-package-authoring.md).

Windows Installer 4,5 no admite algunas opciones de configuración de servicios que pueden habilitar un paquete para personalizar los [servicios](../services/services.md) de un equipo. Para obtener más información, consulte uso de la [configuración de servicios](using-services-configuration.md).

Windows Installer 4,5 no admite algunas características que permiten al Windows Installer proteger nuevas cuentas, [servicios](../services/services.md)de Windows, archivos, carpetas y claves del registro. Para obtener más información, consulte [protección de recursos](securing-resources-.md).

Windows Installer 4,5 no admite algunas características que permiten que la instalación Enumere todos los componentes instalados en el equipo y obtenga la ruta de acceso de la clave del componente. Para obtener más información, vea [enumerar componentes](enumerating-components-.md).

 

 

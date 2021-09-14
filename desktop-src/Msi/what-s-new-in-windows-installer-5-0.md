---
description: La información de este tema identifica las adiciones y los cambios que están disponibles en Windows Installer&\# 160;5.0.
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: Novedades de Windows Installer 5.0
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: ae7986cec60341127ab00ad08a3032aad80209bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069584"
---
# <a name="whats-new-in-windows-installer-50"></a>Novedades de Windows Installer 5.0

La información de este tema identifica las adiciones y los cambios que están disponibles en Windows Installer 5.0.

Windows El instalador 5.0 se incluye con las siguientes versiones de Windows:

* Cliente: Windows 7 y todas las versiones posteriores.
* Servidor: Windows Server 2008 R2 y todas las versiones posteriores.

> [!NOTE]
> No hay ningún redistribuible para Windows Installer 5.0. Para obtener una lista de redistribuibles disponibles para versiones anteriores de Windows Installer, [vea Windows Installer Redistributables](windows-installer-redistributables.md). Para obtener una lista completa de las Windows del instalador, vea [Versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

Esta página se proporciona como guía de la documentación. Debe consultar la sección Requisitos de las páginas de referencia principales para determinar los requisitos reales del sistema operativo. Las partes del Windows que no están vinculadas a desde esta página pueden estar disponibles en otra versión del Windows instalador. Para obtener información sobre otras Windows installer, vea [Novedades de Windows Installer](what-s-new-in-windows-installer.md).

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

[Propiedades de información de resumen](summary-information-stream-reference.md)

-   El [**Resumen de plantilla tiene**](template-summary.md) nuevos valores para indicar que la base de datos es compatible con Windows RT o la plataforma Arm64.

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

[Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interfaz de Automation](automation-interface.md)

-   Propiedades del objeto [ **Installer**](installer-object.md)

    -   [**Installer.ClientsEx**](installer-clientsex.md)
    -   [**Installer.ComponentsEx**](installer-componentsex.md)
    -   [**Installer.ComponentPathEx**](installer-componentpathex.md)

-   Propiedades del objeto [ **Components**](components.md)

    -   [**Components.ComponentCode**](component-componentcode.md)
    -   [**Components.UserSID**](component-usersid.md)
    -   [**Components.Context**](component-context.md)

-   Propiedades del [ **objeto de cliente**](client.md)

    -   [**Client.ProductCode**](client-productcode.md)
    -   [**Client.ComponentCode**](client-componentcode.md)
    -   [**Client.UserSID**](client-usersid.md)
    -   [**Client.Context**](client-context.md)

-   Propiedades del [**objeto ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo.Path**](componentinfo-path.md)
    -   [**ComponentInfo.State**](componentinfo-state.md)

## <a name="notes"></a>Notas

Los desarrolladores de instalación pueden usar Windows Installer 5.0 para crear un único paquete de instalación capaz de instalar la aplicación por máquina o por usuario. Para obtener más información, vea [Single Package Authoring](single-package-authoring.md). El evaluador de coherencia [interno ICE105](ice-105.md) comprueba que el paquete se ha escrito para instalarse en un contexto por usuario. Una aplicación capaz de instalar, actualizar, ejecutar y quitar por un usuario estándar sin elevación se denomina Per-User aplicación (PUA). Una PUA puede proporcionar una mejor experiencia de usuario, minimizar los efectos en el sistema y otros usuarios del equipo, y reserva la solicitud de UAC a situaciones que realmente requieren la elevación de los privilegios del usuario. Las características de creación de paquete único de Windows Installer 5.0 pueden facilitar el desarrollo de Per-User aplicaciones.

Las opciones de configuración de servicios permiten que Windows instalador personalizado para personalizar [los servicios](../services/services.md) en un equipo. Para obtener más información, vea [Using Services Configuration](using-services-configuration.md).

A partir de Windows Installer 5.0, un paquete del instalador de Windows es capaz de proteger nuevas cuentas, servicios de [Windows,](../services/services.md)archivos, carpetas y claves del Registro. La [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) puede especificar un descriptor de seguridad que deniegue permisos, especifique la herencia de permisos de un recurso primario o especifique los permisos de una nueva cuenta. Para obtener información, vea [Securing Resources](securing-resources-.md).

Windows El instalador 5.0 puede enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de la clave para el componente. Para obtener más información, [vea Enumerar componentes](enumerating-components-.md).

Windows El instalador 5.0 que se ejecuta Windows Server 2012 o Windows 8 admite la instalación de aplicaciones aprobadas en Windows RT. No Windows instalar un paquete, revisión o transformación del instalador de aplicaciones que no haya sido firmado por Microsoft en Windows RT. La [**propiedad Resumen de plantilla**](template-summary.md) indica la plataforma que es compatible con la base de datos de instalación y debe incluir el valor para Windows RT.

Windows El instalador 5.0 que se ejecuta Windows 10 en procesadores Arm64 admite la instalación de aplicaciones compiladas específicamente para la plataforma Arm64.  La [**propiedad Resumen de**](template-summary.md) plantilla de estos paquetes debe incluir el valor Arm64. 

 

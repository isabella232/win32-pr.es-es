---
description: Las funciones, las tablas y las propiedades del instalador de Windows enumeradas en esta página no son compatibles con Windows Installer&\# 160;4.0 y versiones anteriores.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: No se admite en Windows Installer 4.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444040fca716b6bd64c8598d2d2e36013fe19cc62971483507756a66f3e961bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558805"
---
# <a name="not-supported-in-windows-installer-40"></a>No se admite en Windows Installer 4.0

Las Windows, las tablas y las propiedades del instalador que aparecen en esta página no son compatibles con Windows Installer 4.0 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admite la característica. Consulte la documentación principal para determinar qué Windows installer es necesaria para una característica determinada. Para obtener información sobre otras versiones Windows Installer, vea [Novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows El instalador 4.0 está disponible para Microsoft Windows Server 2008 y Windows Vista. Para obtener una lista completa de todas las versiones Windows Installer y redistribuibles, vea Versiones publicadas [de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 4.0 y versiones anteriores.

[Funciones del instalador](installer-functions.md)

-   [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[Propiedades](properties.md)

-   [**MSIDISABLEEEUI**](msidisableeeui.md)
-   [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)

[Tablas de base de datos](database-tables.md)

-   [Tabla MsiEmbeddedChainer](msiembeddedchainer-table.md)
-   [Tabla MsiEmbeddedUI](msiembeddedui-table.md)
-   [Tabla MsiPackageCertificate](msipackagecertificate-table.md)
-   [Tabla de componentes](component-table.md)
- **msidbComponentAttributesUninstallOnSupersedence**  
    **msidbComponentAttributesShared**  
    
-   [CustomAction](customaction-table.md) Columna ExtendedType  
    

[Opción de desinstalación de revisiones de acción personalizada](custom-action-patch-uninstall-option.md)



[MsiTransformView\<PatchGUID\>](msitransformview.md)  

**msidbCustomActionTypePatchUninstall**  


[Directiva del sistema](system-policy.md)

-   [DisableSharedComponent](disablesharedcomponent.md)
-   [MsiDisableEmbeddedUI](msidisableembeddedui.md)

Prototipos de función de devolución de llamada

-   *EmbeddedUIHandler*
-   *InitializeEmbeddedUI*
-   *ShutdownEmbeddedUI*

[Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)

-   [ICE92 comprueba](ice92.md) que ningún componente tiene los atributos **msidbComponentAttributesPermanent** y **msidbComponentAttributesUninstallOnSupersedence.**

## <a name="notes"></a>Notas

Windows El instalador 4.0 no puede realizar [varias instalaciones de paquetes mediante](multiple-package-installations.md) el procesamiento de [*transacciones*](t-gly.md).

Con Windows Installer 4.0 o versiones anteriores del instalador, se pueden producir errores en las actualizaciones pequeñas y secundarias cuando se usa la directiva [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) o la propiedad [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) porque la actualización quita un componente.

Una interfaz de usuario personalizada no se puede incrustar en el paquete Windows Installer mediante el método descrito en [Uso de una interfaz de usuario insertada](using-an-embedded-ui.md).

 

 




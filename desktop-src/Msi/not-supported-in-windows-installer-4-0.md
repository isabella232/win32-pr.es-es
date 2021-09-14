---
description: Las funciones, las tablas y las propiedades del instalador de Windows enumeradas en esta página no son compatibles con Windows Installer&\# 160;4.0 y versiones anteriores.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: No se admite en Windows Installer 4.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4307422c71976057948759078dc321e38dc543b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161474"
---
# <a name="not-supported-in-windows-installer-40"></a>No se admite en Windows Installer 4.0

Las Windows, las tablas y las propiedades del instalador que se enumeran en esta página no son compatibles con Windows Installer 4.0 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admite la característica. Consulte la documentación principal para determinar qué versión Windows installer es necesaria para una característica determinada. Para obtener información sobre otras Windows installer, vea [Novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows El instalador 4.0 está disponible para Microsoft Windows Server 2008 y Windows Vista. Para obtener una lista completa de todas las versiones Windows installer y redistribuibles, vea Versiones publicadas [de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 4.0 y versiones anteriores.

[Funciones del instalador](installer-functions.md)

-   [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[Propiedades](properties.md)

-   [**MSIDISABLEEEUI**](msidisableeeui.md)
-   [**MSIUNINSTALLSUPERSEDCOMPONENTS**](msiuninstallsupersededcomponents.md)

[Tablas de base de datos](database-tables.md)

-   [Tabla MsiEmbeddedChainer](msiembeddedchainer-table.md)
-   [Tabla MsiEmbeddedUI](msiembeddedui-table.md)
-   [Tabla MsiPackageCertificate](msipackagecertificate-table.md)
-   [Tabla de componentes](component-table.md)
- **msidbComponentAttributesUninstallOnSupersedence**  
    **msidbComponentAttributesShared**  
    
-   [CustomAction](customaction-table.md) Columna ExtendedType  
    

[Opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md)



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

No se puede incrustar una interfaz de usuario personalizada en el paquete Windows Installer mediante el método descrito en [Uso de una interfaz de usuario insertada](using-an-embedded-ui.md).

 

 




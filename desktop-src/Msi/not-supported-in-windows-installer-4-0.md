---
description: Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer&\# 160; 4.0 y versiones anteriores.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: No se admite en Windows Installer 4,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4307422c71976057948759078dc321e38dc543b7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105678669"
---
# <a name="not-supported-in-windows-installer-40"></a>No se admite en Windows Installer 4,0

Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer 4,0 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admita la característica. Consulte la documentación principal para determinar qué versión de Windows Installer es necesaria para una característica determinada. Para obtener información sobre otras versiones de Windows Installer, vea [novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 4,0 está disponible para Microsoft Windows Server 2008 y Windows Vista. Para obtener una lista completa de todas las versiones de Windows Installer y redistribuibles, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 4,0 y versiones anteriores.

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

[Evaluadores de coherencia interna-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) comprueba que ningún componente tiene los atributos **msidbComponentAttributesPermanent** y **msidbComponentAttributesUninstallOnSupersedence** .

## <a name="notes"></a>Notas

Windows Installer 4,0 no puede realizar [varias instalaciones de paquetes](multiple-package-installations.md) mediante el [*procesamiento de transacciones*](t-gly.md).

Con Windows Installer 4,0 o versiones anteriores del programa de instalación, se puede producir un error en las actualizaciones pequeñas y las actualizaciones secundarias cuando se usa la directiva [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) o la propiedad [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) porque la actualización quita un componente.

Una interfaz de usuario personalizada no se puede incrustar en el paquete de Windows Installer mediante el método descrito en [usar una interfaz de usuario incrustada](using-an-embedded-ui.md).

 

 




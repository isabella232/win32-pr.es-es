---
description: Las funciones, las tablas y las propiedades del instalador de Windows enumeradas en esta página no son compatibles con Windows Installer&\# 160;2.0 y versiones anteriores.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: No se admite en Windows Installer 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ee09133af9ef611a93c2511d7b130b2175561b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161477"
---
# <a name="not-supported-in-windows-installer-20"></a>No se admite en Windows Installer 2.0

Las Windows, las tablas y las propiedades del instalador que se enumeran en esta página no son compatibles con Windows Installer 2.0 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admite la característica. Consulte la documentación principal para determinar qué versión Windows installer es necesaria para una característica determinada. Para obtener información sobre otras Windows installer, vea [Novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows El instalador 2.0 se puede ejecutar en Microsoft Windows 2000, Microsoft Windows XP o Windows Server 2003. Para obtener una lista de todas las versiones Windows Installer, vea [Versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 2.0 y versiones anteriores.

[Funciones del instalador](installer-functions.md)

-   [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
-   [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
-   [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
-   [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
-   [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
-   [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
-   [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
-   [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
-   [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
-   [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
-   [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
-   [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
-   [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
-   [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
-   [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
-   [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa)
-   [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
-   [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
-   [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
-   [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
-   [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

[Windows Estructuras del instalador](installer-structures.md)

-   [**MSIPATCHSEQUENCEINFO**](/windows/win32/api/msi/ns-msi-msipatchsequenceinfoa)

[Tablas de base de datos](database-tables.md)

-   [MsiPatchCertificate](msipatchcertificate-table.md)
-   [MsiPatchSequence](msipatchsequence-table.md)
-   [MsiPatchMetadata](msipatchmetadata-table.md)

[Propiedades](properties.md)

-   [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**MsiPatchRemovalList**](msipatchremovallist.md)
-   [**MsiUISourceResOnly**](msiuisourceresonly.md)
-   [**MsiUIHideCancel**](msiuihidecancel.md)
-   [**MsiUIProgressOnly**](msiuiprogressonly.md)

[Directiva del sistema](system-policy.md)

-   [DisableLUAPatching](disableluapatching.md)
-   [DisablePatchUninstall](disablepatchuninstall.md)
-   [DisableFlyWeightPatching](disableflyweightpatching.md)
-   [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md)
-   [MaxPatchCacheSize](maxpatchcachesize.md)

[Códigos de error](error-codes.md)

-   ELIMINACIÓN \_ DE \_ REVISIÓN \_ DE ERRORES NO ADMITIDA
-   REVISIÓN \_ DESCONOCIDA DE \_ ERROR
-   REVISIÓN \_ \_ DE ERRORES SIN \_ SECUENCIA
-   NO \_ SE PUEDE ELIMINAR LA \_ \_ REVISIÓN DE ERRORES
-   ERROR \_ XML DE \_ REVISIÓN NO \_ VÁLIDO
-   PRODUCTO \_ ANUNCIADO ADMINISTRADO POR \_ REVISIÓN DE \_ \_ ERRORES

Modos de registro

-   [**INSTALLLOGMODE \_ LOGONLYONERROR**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Interfaz de Automation](automation-interface.md)

-   Propiedades del [ **objeto Product**](product-object.md)

    -   [**Product.UserSid**](product-usersid.md)
    -   [**Product.Sources**](product-sources.md)
    -   [**Product.MediaDisks**](product-mediadisks.md)
    -   [**Product.FeatureState**](product-featurestate.md)
    -   [**Product.Context**](product-context.md)
    -   [**Product.InstallProperty**](product-installproperty.md)
    -   [**Product.ProductCode**](product-productcode.md)
    -   [**Product.ComponentState**](product-componentstate.md)
    -   [**Product.State**](product-state.md)
    -   [**Product.SourceListInfo**](product-sourcelistinfo.md)

-   Métodos del [ **objeto Product**](product-object.md)

    -   [**Product.SourceListForceResolution**](product-sourcelistforceresolution.md)
    -   [**Product.SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)
    -   [**Product.SourceListClearAll**](product-sourcelistclearall.md)
    -   [**Product.SourceListClearSource**](product-sourcelistclearsource.md)
    -   [**Product.SourceListAddSource**](product-sourcelistaddsource.md)
    -   [**Product.SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)

-   Propiedades del [ **objeto Patch**](patch-object.md)

    -   [**Patch.UserSid**](patch-usersid.md)
    -   [**Patch.State**](patch-state.md)
    -   [**Patch.Sources**](patch-sources.md)
    -   [**Patch.SourceListInfo**](patch-sourcelistinfo.md)
    -   [**Patch.ProductCode**](patch-productcode.md)
    -   [**Patch.PatchProperty**](patch-patchproperty.md)
    -   [**Patch.PatchCode**](patch-patchcode.md)
    -   [**Patch.MediaDisks**](patch-mediadisks.md)
    -   [**Patch.Context**](patch-context.md)

-   Métodos del [ **objeto Patch**](patch-object.md)

    -   [**Patch.SourceListForceResolution**](patch-sourcelistforceresolution.md)
    -   [**Patch.SourceListClearAll**](patch-sourcelistclearall.md)
    -   [**Patch.SourceListClearSource**](patch-sourcelistclearsource.md)
    -   [**Patch.SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch.SourceListAddSource**](patch-sourcelistaddsource.md)
    -   [**Patch.SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)

-   Propiedades del objeto [ **Installer**](installer-object.md)

    -   [**Installer.ProductsEx**](installer-productsex.md)
    -   [**Installer.ProductInfo**](installer-productinfo.md)
    -   [**Installer.PatchesEx**](installer-patchesex.md)

-   Métodos del [ **objeto Installer**](installer-object.md)

    -   [**Installer.ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**Installer.ApplyPatch**](installer-applypatch.md)
    -   [**Installer.RemovePatches**](installer-removepatches.md)
    -   [**Installer.ExtractPatchXMLData**](installer-extractpatchxmldata.md)

Las siguientes características tampoco se admiten en Windows Installer versión 2.0.2600. Windows La versión del instalador 2.0.2600 se publicó con Windows XP y Windows 2000 Server. Las características están disponibles a partir de Windows Installer versión 2.0.3790 publicada con Windows Server 2003. Para obtener una lista de todas las versiones Windows Installer, vea [Versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

[Funciones del instalador](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   INSTANCIA DE MSIADVERTISEOPTIONS \_
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Interfaz de Automation](automation-interface.md)

-   Métodos del [ **objeto Installer**](installer-object.md)

    -   [**Installer.ApplyPatch**](installer-applypatch.md)
    -   [**Installer.ProductInfo**](installer-productinfo.md)

[Propiedades](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[Opciones de ejecución de In-Script acción personalizada](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[Códigos de error](error-codes.md)

-   [ERROR \_ DE INSTALACIÓN REMOTA \_ \_ PROHIBIDA](error-codes.md)

[Directivas de máquina](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [Transformaciones Directiva segura](transformssecure-policy.md)

[Opciones de línea de comandos](command-line-options.md)

-   [/c](command-line-options.md)
-   [/n](command-line-options.md)
-   [/Lx](command-line-options.md)

[Atributos de control](control-attributes.md)

-   **ImageHandle** se quitó

## <a name="notes"></a>Notas

Las [opciones de configuración Command-Line](standard-installer-command-line-options.md) instalador estándar no son compatibles con Windows Installer 2.0. En su lugar, use Windows de [línea de comandos del instalador de .](command-line-options.md)

Cuando Windows Installer 2.0 instala un paquete de revisión, omite la información de las tablas [MsiPatchSequence](msipatchsequence-table.md) [o MsiPatchMetadata.](msipatchmetadata-table.md) Las versiones posteriores del instalador Windows pueden usar la información de estas tablas para mejorar la secuenciación, eliminación y optimización de revisiones. Para obtener información sobre la funcionalidad de aplicación de revisiones mejorada en Windows Installer, vea [Aplicación de revisiones.](patching.md)

Windows El instalador 2.0 [](uninstallable-patches.md) no admite revisiones desinstalables y el único método para quitar revisiones concretas de una aplicación es desinstalar toda la aplicación con revisión y, a continuación, volver a instalarla sin volver a aplicar ninguna revisión que se quite.

Windows El instalador 2.0 no admite la secuenciación de revisiones e instala revisiones en el orden en que se proporcionan al sistema al instalar [varias revisiones](installing-multiple-patches.md).

Windows El instalador 2.0 no admite el uso de la aplicación de revisiones de control de cuentas de usuario [(UAC)](user-account-control--uac--patching.md) para habilitar las revisiones firmadas digitalmente que pueden aplicar los usuarios que no son administradores.

Windows El instalador 2.0 no admite la [optimización de revisiones](patch-optimization.md). La aplicación de revisiones puede tardar mucho más tiempo que con versiones posteriores Windows Installer que solo actualiza los archivos afectados por la revisión.

Windows El instalador 2.0 no admite el uso [de Windows instalador para inventariar productos y revisiones.](inventory-products-and-patches-.md)

Windows Installer 2.0 no admite la recuperación y modificación de la información de la lista de origen para las aplicaciones y revisiones de Windows Installer instaladas en el sistema para todos los usuarios. Las versiones posteriores de Windows Installer permiten a los administradores administrar las listas de origen y las propiedades de la lista de origen para los orígenes de red, dirección URL y medios. Las versiones posteriores permiten a los administradores administrar listas de origen desde un proceso externo. Para obtener más información, vea [Administrar orígenes de instalación.](managing-installation-sources.md)

Windows El instalador 2.0 no admite la instalación de varias instancias de productos o revisiones sin un paquete de instalación independiente para cada instancia. Más Windows versiones del instalador pueden instalar varias instancias de un producto mediante transformaciones de código de producto y un paquete de .msi o una revisión. Para obtener [información, vea Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md)( Instalación de varias instancias de productos y revisiones).

A partir Windows XP con Service Pack 2 (SP2), Windows Installer puede usar los protocolos HTTP, HTTPS y FILE. El instalador no admite los protocolos FTP y GOPHER.

 

 




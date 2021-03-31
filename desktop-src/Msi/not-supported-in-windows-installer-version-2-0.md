---
description: Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer&\# 160; 2.0 y versiones anteriores.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: No se admite en Windows Installer 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ee09133af9ef611a93c2511d7b130b2175561b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913258"
---
# <a name="not-supported-in-windows-installer-20"></a>No se admite en Windows Installer 2,0

Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer 2,0 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admita la característica. Consulte la documentación principal para determinar qué versión de Windows Installer es necesaria para una característica determinada. Para obtener información sobre otras versiones de Windows Installer, vea [novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 2,0 se puede ejecutar en Microsoft Windows 2000, Microsoft Windows XP o Windows Server 2003. Para obtener una lista de todas las versiones de Windows Installer, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 2,0 y versiones anteriores.

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

[Windows Installer estructuras](installer-structures.md)

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

-   \_no se \_ admite la eliminación de la revisión de errores \_
-   ERROR \_ de \_ revisión desconocida
-   ERROR de \_ revisión \_ sin \_ secuencia
-   no \_ se \_ permite la eliminación de la revisión de errores \_
-   ERROR \_ de \_ revisión \_ XML no válida
-   producto de revisión de errores \_ \_ administrado \_ anunciada \_

Modos de registro

-   [**INSTALLLOGMODE \_ LOGONLYONERROR**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Interfaz de automatización](automation-interface.md)

-   Propiedades del [ **objeto Product**](product-object.md)

    -   [**Producto. UserSid**](product-usersid.md)
    -   [**Product. sources**](product-sources.md)
    -   [**Producto. MediaDisks**](product-mediadisks.md)
    -   [**Producto. FeatureState**](product-featurestate.md)
    -   [**Product. Context**](product-context.md)
    -   [**Producto. InstallProperty**](product-installproperty.md)
    -   [**Product. ProductCode**](product-productcode.md)
    -   [**Producto. ComponentState**](product-componentstate.md)
    -   [**Product. State**](product-state.md)
    -   [**Producto. SourceListInfo**](product-sourcelistinfo.md)

-   Métodos de [ **objeto Product**](product-object.md)

    -   [**Producto. SourceListForceResolution**](product-sourcelistforceresolution.md)
    -   [**Producto. SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)
    -   [**Producto. SourceListClearAll**](product-sourcelistclearall.md)
    -   [**Producto. SourceListClearSource**](product-sourcelistclearsource.md)
    -   [**Producto. SourceListAddSource**](product-sourcelistaddsource.md)
    -   [**Producto. SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)

-   Propiedades del [ **objeto patch**](patch-object.md)

    -   [**Patch. UserSid**](patch-usersid.md)
    -   [**Patch. State**](patch-state.md)
    -   [**Patch. sources**](patch-sources.md)
    -   [**Patch. SourceListInfo**](patch-sourcelistinfo.md)
    -   [**Patch. ProductCode**](patch-productcode.md)
    -   [**Patch. PatchProperty**](patch-patchproperty.md)
    -   [**Patch. PatchCode**](patch-patchcode.md)
    -   [**Patch. MediaDisks**](patch-mediadisks.md)
    -   [**Patch. Context**](patch-context.md)

-   Métodos del [ **objeto patch**](patch-object.md)

    -   [**Patch. SourceListForceResolution**](patch-sourcelistforceresolution.md)
    -   [**Patch. SourceListClearAll**](patch-sourcelistclearall.md)
    -   [**Patch. SourceListClearSource**](patch-sourcelistclearsource.md)
    -   [**Patch. SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch. SourceListAddSource**](patch-sourcelistaddsource.md)
    -   [**Patch. SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)

-   Propiedades del [ **objeto Installer**](installer-object.md)

    -   [**Instalador. ProductsEx**](installer-productsex.md)
    -   [**Instalador. ProductInfo**](installer-productinfo.md)
    -   [**Instalador. PatchesEx**](installer-patchesex.md)

-   Métodos del [ **objeto Installer**](installer-object.md)

    -   [**Instalador. ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**Instalador. ApplyPatch**](installer-applypatch.md)
    -   [**Instalador. RemovePatches**](installer-removepatches.md)
    -   [**Instalador. ExtractPatchXMLData**](installer-extractpatchxmldata.md)

También se admiten las siguientes características en Windows Installer versión 2.0.2600. Windows Installer versión 2.0.2600 se lanzó con Windows XP y Windows 2000 Server. Las características están disponibles a partir de Windows Installer versión 2.0.3790 publicada con Windows Server 2003. Para obtener una lista de todas las versiones de Windows Installer, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

[Funciones del instalador](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   instancia de MSIADVERTISEOPTIONS \_
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Interfaz de automatización](automation-interface.md)

-   Métodos del [ **objeto Installer**](installer-object.md)

    -   [**Instalador. ApplyPatch**](installer-applypatch.md)
    -   [**Instalador. ProductInfo**](installer-productinfo.md)

[Propiedades](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[Opciones de ejecución de la acción personalizada In-Script](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[Códigos de error](error-codes.md)

-   [ERROR al \_ instalar el \_ remoto \_ prohibido](error-codes.md)

[Directivas de equipo](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [Directiva TransformsSecure](transformssecure-policy.md)

[Opciones de la línea de comandos](command-line-options.md)

-   [/c](command-line-options.md)
-   [/n](command-line-options.md)
-   [/Lx](command-line-options.md)

[Atributos de control](control-attributes.md)

-   Se quitó **ImageHandle**

## <a name="notes"></a>Notas

El [instalador estándar Command-Line opciones](standard-installer-command-line-options.md) no se admiten en Windows Installer 2,0. En su lugar, use las [Opciones de línea de comandos de](command-line-options.md)Windows Installer.

Cuando Windows Installer 2,0 instala un paquete de revisión, omite la información de las tablas [MsiPatchSequence](msipatchsequence-table.md) o [MsiPatchMetadata](msipatchmetadata-table.md) . Las versiones posteriores del Windows Installer pueden utilizar la información de estas tablas para mejorar la secuenciación, la eliminación y la optimización de las revisiones. Para obtener información acerca de la funcionalidad de revisión mejorada en Windows Installer, consulte [revisión](patching.md).

Windows Installer 2,0 no admite [revisiones desinstalables](uninstallable-patches.md) y el único método para quitar revisiones concretas de una aplicación es desinstalar toda la aplicación con revisión y, a continuación, volver a instalar sin volver a aplicar las revisiones que se van a quitar.

Windows Installer 2,0 no admite la secuenciación de revisiones e instala revisiones en el orden en que se proporcionan al sistema al [instalar varias revisiones](installing-multiple-patches.md).

Windows Installer 2,0 no admite el uso de la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) para habilitar revisiones firmadas digitalmente que pueden ser aplicadas por usuarios que no son administradores.

Windows Installer 2,0 no admite la [optimización de revisiones](patch-optimization.md). La revisión puede tardar mucho más tiempo que con versiones posteriores Windows Installer que solo actualizan los archivos afectados por la revisión.

Windows Installer 2,0 no admite el [uso de Windows Installer para inventariar productos y revisiones](inventory-products-and-patches-.md).

Windows Installer 2,0 no admite la recuperación y modificación de la información de la lista de origen para las aplicaciones Windows Installer y las revisiones instaladas en el sistema para todos los usuarios. Las versiones posteriores de Windows Installer permiten a los administradores administrar las listas de origen y las propiedades de la lista de origen de los orígenes de red, URL y multimedia. Las versiones posteriores permiten a los administradores administrar las listas de origen desde un proceso externo. Para obtener más información, consulte [administrar orígenes de instalación](managing-installation-sources.md).

Windows Installer 2,0 no admite la instalación de varias instancias de productos o revisiones sin un paquete de instalación independiente para cada instancia. Versiones posteriores Windows Installer pueden instalar varias instancias de un producto mediante el uso de transformaciones de código de producto y un paquete. msi o una revisión. Para obtener información [, consulte Instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md).

A partir de Windows XP con Service Pack 2 (SP2), Windows Installer puede usar los protocolos HTTP, HTTPS y FILE. El instalador no admite los protocolos FTP y GOPHER.

 

 




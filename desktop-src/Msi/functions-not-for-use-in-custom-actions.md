---
description: Nunca se debe llamar a las siguientes funciones de base de datos desde una acción personalizada.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Funciones que no se usan en acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667790"
---
# <a name="functions-not-for-use-in-custom-actions"></a>Funciones que no se usan en acciones personalizadas

Nunca se debe llamar a las siguientes [funciones de base de datos](database-functions.md) desde una acción personalizada.

-   [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

Nunca se debe llamar a las siguientes [funciones de instalador](installer-function-reference.md) desde una acción personalizada.

-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

Nunca se debe llamar a las siguientes [funciones de instalador](installer-function-reference.md) desde una acción personalizada si al hacerlo se inicia otra instalación. Pueden llamarse desde una acción personalizada que no inicia otra instalación.

-   [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

Una acción personalizada nunca debe generar un nuevo subproceso que use funciones de Windows Installer para cambiar el estado de la característica, el estado del componente o para enviar mensajes desde un evento de control. Si intenta hacerlo, se producirá un error en la instalación.

 

 




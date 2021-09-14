---
description: Para reproducir el paquete de revisión de ejemplo, necesita una herramienta de software capaz de crear y editar un Windows de revisión del instalador.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Crear un archivo de propiedades de creación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158735"
---
# <a name="creating-a-patch-creation-properties-file"></a>Crear un archivo de propiedades de creación de revisiones

Para reproducir el paquete de revisión de ejemplo, necesita una herramienta de software capaz de crear y editar un Windows de revisión del instalador. Hay varias herramientas de creación de paquetes de revisión disponibles de proveedores de software independientes. En el ejemplo que se describe en las secciones siguientes se usa un editor de base de datos Windows Installer llamado Orca para crear un archivo de propiedades de creación de revisiones (extensión .csv). El archivo .msp se puede usar con las utilidades [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) para generar un paquete de revisión Windows Installer (extensión .msp). Orca, Msimsp.exe y Patchwiz.dll se proporcionan en Windows SDK Components for Windows Installer Developers (Componentes Windows SDK para [Windows Installer).](platform-sdk-components-for-windows-installer-developers.md)

También se proporciona un archivo de propiedades de creación de revisiones en blanco, template.asín. Realice una copia de template.fax y cambie el nombre de esta copia MNP2000.copie. Use Orca u otro editor de bases de datos para escribir los datos siguientes en la tabla Properties de MNP2000.oracle. La tabla Propiedades contiene la configuración global del paquete de revisión.

[Propiedades de tabla](properties-table-patchwiz-dll-.md)



| Nombre                               | Value                                  |
|------------------------------------|----------------------------------------|
| AllowProductCodeMismatches         | 1                                      |
| AllowProductVersionMajorMismatches | 1                                      |
| ApiPatchingSymbolFlags             | 0x00000000                             |
| DontRemoveTempFolderWhenFinished   | 1                                      |
| IncludeWholeFilesOnly              | 0                                      |
| ListOfPatchGUIDsToReplace          |                                        |
| ListOfTargetProductCodes           | \*                                     |
| PatchGUID                          | {5406B219-A1AC-4BC4-8695-72292C8195AC} |
| PatchOutputPath                    | c: \\ output.msp                         |
| PatchSourceList                    | PatchSourceList                        |



 

Use el editor de bases de datos para escribir los datos siguientes en la tabla ImageFamilies de MNP2000.oracle. La tabla ImageFamilies contiene información que se va a agregar a la [tabla Media durante](media-table.md) la aplicación de revisiones.

[Tabla ImageFamilies](imagefamilies-table-patchwiz-dll-.md)



| Familia  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| MNPapps | MNPSrcPropName   | 2           | 1000              |            |             |



 

Escriba los datos siguientes en la tabla UpgradedImages de MNP2000.uu. La tabla UpgradedImages contiene información sobre la imagen actualizada que creó en [Planning a Small Update Patch](planning-a-small-update-patch.md).

[Tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md)



| Upgraded   | MsiPath                                           | PatchMsiPath | SymbolPaths | Familia  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ corregido | C: Nota \\ Actualización \_ de la \\ revisión del instalador \\ \\MNP2000.msi |              |             | MNPapps |



 

Escriba los datos siguientes en la tabla TargetImages de MNP2000. La tabla TargetImages contiene información sobre la imagen de destino.

[Tabla TargetImages](targetimages-table-patchwiz-dll-.md)



| Destino     | MsiPath                                         | SymbolPaths | Upgraded   | Pedido | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| Error \_ de MNP | C: Nota \\ Destino \_ de \\ revisión del instalador \\ \\MNP2000.msi |             | MNP \_ corregido | 1     |                      | 0                     |



 

Para el paquete de revisión de ejemplo, deje en blanco las tablas siguientes en MNP2000.blank.

[Tabla UpgradedFiles \_ OptionalData](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[Tabla FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md)

[TargetFiles \_ OptionalData Table](targetfiles-optionaldata-table-patchwiz-dll-.md)

[Tabla ExternalFiles](externalfiles-table-patchwiz-dll-.md)

[Tabla UpgradedFilesToIgnore](upgradedfilestoignore-table-patchwiz-dll-.md)

[Continuar](generating-a-patch-package.md)

 

 




---
description: Para reproducir el paquete de revisión de ejemplo, necesita una herramienta de software capaz de crear y editar un paquete de revisión de Windows Installer.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Crear un archivo de propiedades de creación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669926"
---
# <a name="creating-a-patch-creation-properties-file"></a>Crear un archivo de propiedades de creación de revisiones

Para reproducir el paquete de revisión de ejemplo, necesita una herramienta de software capaz de crear y editar un paquete de revisión de Windows Installer. Hay disponibles varias herramientas de creación de paquetes de revisiones de fabricantes de software independientes. En el ejemplo que se describe en las secciones siguientes se usa un editor de base de datos de Windows Installer denominado orca para crear un archivo de propiedades de creación de revisiones (extensión. PCP). El archivo. PCP se puede usar con las utilidades [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) para generar un paquete de revisión de Windows Installer (extensión. msp). Orca, Msimsp.exe y Patchwiz.dll se proporcionan en los [componentes Windows SDK para los programadores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

También se proporciona un archivo de propiedades de creación de revisiones en blanco, template. PCP, con el SDK. Haga una copia de template. PCP y cambie el nombre de esta copia MNP2000. PCP. Use Orca u otro editor de bases de datos para especificar los datos siguientes en la tabla de propiedades de MNP2000. PCP. La tabla de propiedades contiene la configuración global del paquete de revisión.

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
| PatchOutputPath                    | c: \\ salida. MSP                         |
| PatchSourceList                    | PatchSourceList                        |



 

Use el editor de base de datos para escribir los siguientes datos en la tabla ImageFamilies de MNP2000. PCP. La tabla ImageFamilies contiene información que se va a agregar a la [tabla de medios](media-table.md) durante la revisión.

[Tabla ImageFamilies](imagefamilies-table-patchwiz-dll-.md)



| Familia  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| MNPapps | MNPSrcPropName   | 2           | 1000              |            |             |



 

Escriba los datos siguientes en la tabla UpgradedImages de MNP2000. PCP. La tabla UpgradedImages contiene información sobre la imagen actualizada que ha creado en la sección [planeación de una pequeña revisión de actualización](planning-a-small-update-patch.md).

[Tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md)



| Upgraded   | Rutamsi                                           | PatchMsiPath | SymbolPaths | Familia  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ fijo | C: \\ Nota \_ revisión del instalador \\ \\ actualizada \\MNP2000.msi |              |             | MNPapps |



 

Escriba los datos siguientes en la tabla TargetImages de MNP2000. PCP. La tabla TargetImages contiene información sobre la imagen de destino.

[Tabla TargetImages](targetimages-table-patchwiz-dll-.md)



| Destino     | Rutamsi                                         | SymbolPaths | Upgraded   | Pedido | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| Error de MNP \_ | C: \\ tenga en cuenta el \_ destino de revisión del instalador \\ \\ \\MNP2000.msi |             | MNP \_ fijo | 1     |                      | 0                     |



 

En el paquete de revisión de ejemplo, deje en blanco las siguientes tablas en MNP2000. PCP.

[\_Tabla OptionalData UpgradedFiles](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[Tabla FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md)

[\_Tabla OptionalData TargetFiles](targetfiles-optionaldata-table-patchwiz-dll-.md)

[Tabla ExternalFiles](externalfiles-table-patchwiz-dll-.md)

[Tabla UpgradedFilesToIgnore](upgradedfilestoignore-table-patchwiz-dll-.md)

[Continuar](generating-a-patch-package.md)

 

 




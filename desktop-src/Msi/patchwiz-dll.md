---
description: Para generar un paquete de revisión, se recomienda usar una herramienta de creación de revisiones como Msimsp.exe y Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279327"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Para generar un paquete de revisión, se recomienda usar una herramienta de creación de revisiones como [Msimsp.exe](msimsp-exe.md) y Patchwiz.dll. Patchwiz.dll versión 4,0 es compatible con los paquetes y las revisiones que se crearon con versiones anteriores de la Patchwiz.dll. La herramienta Patchwiz.dll solo está disponible en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).

Patchwiz.dll versión 4,0 tiene una nueva función, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), que extiende la funcionalidad de [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md). Estas funciones toman un archivo de propiedades de creación de revisiones (archivo. PCP) y generan un [paquete de revisión](patch-packages.md)del instalador.

El archivo. PCP es un archivo de base de datos binario con el mismo formato que una base de datos de Windows Installer (archivo. msi), pero con un esquema de base de datos diferente. Por lo tanto, se puede crear un archivo. PCP con las mismas herramientas que se usan para una base de datos del instalador.

Puede crear un archivo. PCP mediante un editor de tablas como [Orca.exe](orca-exe.md) para escribir información en la base de datos en blanco. el PCP proporcionado con el Windows Installer SDK, template. PCP. Para obtener más información, vea [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md).

Las tablas de base de datos siguientes son necesarias en cada archivo. PCP:

-   [Tabla de propiedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Tabla ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Tabla UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [Tabla TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

Las tablas de base de datos siguientes son opcionales:

-   [UpgradedFiles \_ OptionalData (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabla FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [TargetFiles \_ OptionalData (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabla ExternalFiles (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Tabla UpgradedFilesToIgnore (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

La tabla siguiente es necesaria en los archivos. PCP que tienen un valor de MinimumRequiredMsiVersion igual a 300 en la tabla de [propiedades](properties-table-patchwiz-dll-.md) .

-   [Tabla PatchMetadata (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> La tabla es opcional si MinimumRequiredMsiVersion no es igual a 300.

 

La versión de Patchwiz.dll publicada con Windows Installer 3,0 puede generar automáticamente información de secuenciación de revisiones y agregarla a la [tabla MsiPatchSequence](msipatchsequence-table.md) de una nueva revisión. La [tabla PatchSequence](patchsequence-table--patchwiz-dll-.md) se puede usar para agregar manualmente la información de secuenciación de revisiones a la tabla MsiPatchSequence. Para obtener más información, vea [generar información de secuencia de revisión](generating-patch-sequence-information---patchwiz-dll-.md).

A partir de Patchwiz.dll versión 2,0, puede aumentar la velocidad de la creación posterior de revisiones mediante el [almacenamiento en caché de la información de revisión (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).

El uso de símbolos públicos para los archivos binarios de imagen de destino y actualización puede reducir el tamaño de las revisiones binarias en aproximadamente una mitad. Para obtener más información, vea [usar símbolos para reducir el tamaño de las revisiones binarias](using-symbols-to-reduce-binary-patch-size.md).

Puede especificar que se conserven que se sobrescriban determinadas regiones del archivo de destino durante la revisión y que se retenga la información de esas regiones. Para obtener más información, consulte [aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




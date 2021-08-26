---
description: Para generar un paquete de revisión, se recomienda usar una herramienta de creación de revisiones, como Msimsp.exe y Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de7a099a95eb6b42341b7f440f15fadb42e6a5ea8bbf69ff4d61b1fcaa28d21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129175"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Para generar un paquete de revisión, se recomienda usar una herramienta de creación de revisiones, comoMsimsp.exe[ y ](msimsp-exe.md) Patchwiz.dll. Patchwiz.dll versión 4.0 es compatible con paquetes y revisiones que se crearon con versiones anteriores del Patchwiz.dll. La herramienta Patchwiz.dll solo está disponible en los componentes del SDK de Windows [para desarrolladores Windows installer .](platform-sdk-components-for-windows-installer-developers.md)

Patchwiz.dll versión 4.0 tiene una nueva función, [UiCreatePatchPackageEx (Patchwiz.dll),](uicreatepatchpackageex--patchwiz-dll-.md)que amplía la funcionalidad de [UiCreatePatchPackage (Patchwiz.dll).](uicreatepatchpackage-patchwiz-dll-.md) Estas funciones toman un archivo de propiedades de creación de revisiones (archivo .debian) y generan un paquete [de revisión del instalador](patch-packages.md).

El archivo .jpeg es un archivo de base de datos binario con el mismo formato que una base de datos Windows Installer (.msi archivo), pero con un esquema de base de datos diferente. Por lo tanto, se puede crear un archivo .debian con las mismas herramientas que se usan para una base de datos del instalador.

Puede crear un archivo .debian mediante un editor de tablas, como [Orca.exe,](orca-exe.md) para escribir información en la base de datos .installer en blanco proporcionada con el SDK del instalador de Windows, Template.debian. Para obtener más información, vea [A Small Update Patching Example](a-small-update-patching-example.md).

Las siguientes tablas de base de datos son necesarias en cada archivo .csv:

-   [Tabla de propiedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Tabla ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Tabla UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [Tabla TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

Las siguientes tablas de base de datos son opcionales:

-   [Tabla UpgradedFiles \_ OptionalData (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabla FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [TargetFiles \_ OptionalData Table (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabla ExternalFiles (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Tabla UpgradedFilesToIgnore (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

La tabla siguiente es necesaria en los archivos .uu. que tienen un Valor MínimoRequiredMsiVersion igual a 300 en la [tabla](properties-table-patchwiz-dll-.md) Propiedades.

-   [Tabla PatchMetadata (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> La tabla es opcional si MinimumRequiredMsiVersion no es igual a 300.

 

La versión de Patchwiz.dll publicada con Windows Installer 3.0 puede generar automáticamente información de secuenciación de revisiones y agregarla a la tabla [MsiPatchSequence](msipatchsequence-table.md) de una nueva revisión. La [tabla PatchSequence se](patchsequence-table--patchwiz-dll-.md) puede usar para agregar manualmente información de secuenciación de revisiones a la tabla MsiPatchSequence. Para obtener más información, vea [Generar información de secuencia de revisión.](generating-patch-sequence-information---patchwiz-dll-.md)

A partir Patchwiz.dll versión 2.0, puede aumentar la velocidad de la posterior creación de revisiones mediante el almacenamiento en caché de información de revisión [(Patchwiz.dll).](patch-information-caching-patchwiz-dll-.md)

El uso de símbolos públicos para los archivos binarios de imagen de destino y actualización puede reducir los tamaños de revisión binaria en aproximadamente la mitad. Para obtener más información, [vea Usar símbolos para reducir el tamaño de revisión binaria.](using-symbols-to-reduce-binary-patch-size.md)

Puede especificar que determinadas regiones del archivo de destino no se sobrescriban durante la aplicación de revisiones y que se conserve la información de esas regiones. Para obtener más información, vea [Aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




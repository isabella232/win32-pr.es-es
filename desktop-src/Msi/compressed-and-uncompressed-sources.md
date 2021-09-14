---
description: Los autores de paquetes pueden reducir el tamaño de sus paquetes de instalación comprimiendo los archivos de origen e incluyéndolos en archivos de archivo. La imagen de archivo de origen se puede comprimir, descomprimir o una combinación de ambos tipos.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Orígenes comprimidos y sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dc706a73d52f1dac35c917bd6c178a543ab300
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158824"
---
# <a name="compressed-and-uncompressed-sources"></a>Orígenes comprimidos y sin comprimir

Los autores de paquetes pueden reducir el tamaño de sus paquetes de instalación comprimiendo los archivos de origen e incluyéndolos en archivos [de archivo .](cabinet-files.md) La imagen de archivo de origen se puede comprimir, descomprimir o una combinación de ambos tipos.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Orígenes comprimidos
</dt> <dd>

Un origen que consta completamente de archivos comprimidos debe incluir el bit de marca comprimida en la [**propiedad Resumen de recuento de**](word-count-summary.md) palabras. Los archivos de origen comprimidos deben almacenarse en archivos archivados ubicados en un flujo de datos dentro del archivo .msi o en un archivo de archivado independiente ubicado en la raíz del árbol de origen. Todos los gabinetes del origen deben aparecer en la [tabla Media](media-table.md).

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Orígenes sin comprimir
</dt> <dd>

Un origen que consta completamente de archivos de origen sin comprimir debe omitir el bit de marca comprimida de la [**propiedad Resumen de recuento de**](word-count-summary.md) palabras. Todos los archivos sin comprimir del origen deben existir en el árbol de origen especificado por la [tabla Directory](directory-table.md).

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Orígenes mixtos 
</dt> <dd>

Para mezclar archivos de código fuente comprimidos y [](word-count-summary.md) sin comprimir en el mismo paquete, invalide el valor predeterminado de la propiedad Resumen de recuento de palabras estableciendo las marcas de bits msidbFileAttributesCompressed o msidbFileAttributesNoncompressed en archivos concretos. Estas marcas de bits se establecen [](file-table.md) en la columna Atributos de la tabla Archivo si el estado de compresión del archivo no coincide con el valor predeterminado especificado por la propiedad Resumen de recuento [**de palabras.**](word-count-summary.md)

Por ejemplo, si la [**propiedad Resumen de recuento**](word-count-summary.md) de palabras tiene el conjunto de bits de marca comprimido, todos los archivos se tratan como comprimidos en un gabinete. Los archivos sin comprimir del origen deben incluir msidbFileAttributesNoncompressed en la columna Attributes de la [tabla File](file-table.md). Los archivos sin comprimir deben encontrarse en la raíz del árbol de origen.

Si la [**propiedad Resumen de**](word-count-summary.md) recuento de palabras tiene establecida la marca sin comprimir, los archivos se tratan como sin comprimir de forma predeterminada y los archivos comprimidos deben incluir msidbFileAttributesCompressed en la columna Atributos de la tabla Archivo. Todos los archivos comprimidos deben almacenarse en archivos archivados ubicados en un flujo de datos dentro del archivo .msi o en un archivo de archivado independiente ubicado en la raíz del árbol de origen.

Para obtener más información, [vea Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

</dd> </dl>

 

 




---
description: Los autores de paquetes pueden reducir el tamaño de los paquetes de instalación mediante la compresión de los archivos de origen y su inclusión en los archivos. cab. La imagen del archivo de origen se puede comprimir, descomprimir o una mezcla de ambos tipos.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Orígenes comprimidos y sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dc706a73d52f1dac35c917bd6c178a543ab300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001390"
---
# <a name="compressed-and-uncompressed-sources"></a>Orígenes comprimidos y sin comprimir

Los autores de paquetes pueden reducir el tamaño de los paquetes de instalación mediante la compresión de los archivos de origen y su inclusión en [los archivos. cab](cabinet-files.md). La imagen del archivo de origen se puede comprimir, descomprimir o una mezcla de ambos tipos.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Orígenes comprimidos
</dt> <dd>

Un origen compuesto por completo de archivos comprimidos debe incluir el bit de marca comprimido en la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) . Los archivos de código fuente comprimidos deben almacenarse en archivos contenedores ubicados en una secuencia de datos dentro del archivo. msi o en un archivo. cab independiente ubicado en la raíz del árbol de origen. Todos los contenedores del origen deben aparecer en la [tabla de medios](media-table.md).

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Orígenes sin comprimir
</dt> <dd>

Un origen compuesto por completo de archivos de código fuente sin comprimir debe omitir el bit de marca comprimido de la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) . Todos los archivos sin comprimir en el origen deben existir en el árbol de origen especificado por la [tabla de directorio](directory-table.md).

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Orígenes mixtos 
</dt> <dd>

Para mezclar archivos de código fuente comprimidos y sin comprimir en el mismo paquete, invalide el valor predeterminado de la propiedad [**Resumen de recuento de palabras**](word-count-summary.md) estableciendo las marcas de bits MsidbFileAttributesCompressed o msidbFileAttributesNoncompressed en archivos concretos. Estas marcas de bits se establecen en la columna Attributes de la [tabla File](file-table.md) si el estado de compresión del archivo no coincide con el valor predeterminado especificado por la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) .

Por ejemplo, si la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) tiene establecido el bit de marca comprimido, todos los archivos se tratan como comprimidos en un archivo. cab. Los archivos sin comprimir en el origen deben incluir msidbFileAttributesNoncompressed en la columna Attributes de la [tabla File](file-table.md). Los archivos sin comprimir deben estar ubicados en la raíz del árbol de origen.

Si la propiedad [**Resumen de recuento de palabras**](word-count-summary.md) tiene establecida la marca sin comprimir, los archivos se tratan como sin comprimir de forma predeterminada y los archivos comprimidos deben incluir msidbFileAttributesCompressed en la columna atributos de la tabla archivo. Todos los archivos comprimidos deben almacenarse en archivos contenedores ubicados en una secuencia de datos dentro del archivo. msi o en un archivo. cab independiente ubicado en la raíz del árbol de origen.

Para obtener más información, consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).

</dd> </dl>

 

 




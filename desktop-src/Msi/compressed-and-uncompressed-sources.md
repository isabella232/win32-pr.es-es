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
# <a name="compressed-and-uncompressed-sources"></a><span data-ttu-id="dea2b-104">Orígenes comprimidos y sin comprimir</span><span class="sxs-lookup"><span data-stu-id="dea2b-104">Compressed and Uncompressed Sources</span></span>

<span data-ttu-id="dea2b-105">Los autores de paquetes pueden reducir el tamaño de los paquetes de instalación mediante la compresión de los archivos de origen y su inclusión en [los archivos. cab](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="dea2b-105">Package authors can reduce the size of their installation packages by compressing the source files and including them in [cabinet files](cabinet-files.md).</span></span> <span data-ttu-id="dea2b-106">La imagen del archivo de origen se puede comprimir, descomprimir o una mezcla de ambos tipos.</span><span class="sxs-lookup"><span data-stu-id="dea2b-106">The source file image can be compressed, uncompressed, or a mixture of both types.</span></span>

<dl> <dt>

<span data-ttu-id="dea2b-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Orígenes comprimidos</span><span class="sxs-lookup"><span data-stu-id="dea2b-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Compressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="dea2b-108">Un origen compuesto por completo de archivos comprimidos debe incluir el bit de marca comprimido en la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="dea2b-108">A source consisting entirely of compressed files should include the compressed flag bit in the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="dea2b-109">Los archivos de código fuente comprimidos deben almacenarse en archivos contenedores ubicados en una secuencia de datos dentro del archivo. msi o en un archivo. cab independiente ubicado en la raíz del árbol de origen.</span><span class="sxs-lookup"><span data-stu-id="dea2b-109">The compressed source files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span> <span data-ttu-id="dea2b-110">Todos los contenedores del origen deben aparecer en la [tabla de medios](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="dea2b-110">All of the cabinets in the source must be listed in the [Media table](media-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="dea2b-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Orígenes sin comprimir</span><span class="sxs-lookup"><span data-stu-id="dea2b-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Uncompressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="dea2b-112">Un origen compuesto por completo de archivos de código fuente sin comprimir debe omitir el bit de marca comprimido de la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="dea2b-112">A source consisting entirely of uncompressed source files should omit the compressed flag bit from the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="dea2b-113">Todos los archivos sin comprimir en el origen deben existir en el árbol de origen especificado por la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="dea2b-113">All of the uncompressed files in the source must exist in the source tree specified by the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="dea2b-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Orígenes mixtos</span><span class="sxs-lookup"><span data-stu-id="dea2b-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Mixed Sources</span></span> 
</dt> <dd>

<span data-ttu-id="dea2b-115">Para mezclar archivos de código fuente comprimidos y sin comprimir en el mismo paquete, invalide el valor predeterminado de la propiedad [**Resumen de recuento de palabras**](word-count-summary.md) estableciendo las marcas de bits MsidbFileAttributesCompressed o msidbFileAttributesNoncompressed en archivos concretos.</span><span class="sxs-lookup"><span data-stu-id="dea2b-115">To mix compressed and uncompressed source files in the same package, override the [**Word Count Summary**](word-count-summary.md) property default by setting the msidbFileAttributesCompressed or msidbFileAttributesNoncompressed bit flags on particular files.</span></span> <span data-ttu-id="dea2b-116">Estas marcas de bits se establecen en la columna Attributes de la [tabla File](file-table.md) si el estado de compresión del archivo no coincide con el valor predeterminado especificado por la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="dea2b-116">These bit flags are set in the Attributes column of the [File table](file-table.md) if the compression state of the file does not match the default specified by the [**Word Count Summary**](word-count-summary.md) property.</span></span>

<span data-ttu-id="dea2b-117">Por ejemplo, si la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) tiene establecido el bit de marca comprimido, todos los archivos se tratan como comprimidos en un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="dea2b-117">For example, if the [**Word Count Summary**](word-count-summary.md) property has the compressed flag bit set, all files are treated as compressed into a cabinet.</span></span> <span data-ttu-id="dea2b-118">Los archivos sin comprimir en el origen deben incluir msidbFileAttributesNoncompressed en la columna Attributes de la [tabla File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="dea2b-118">Any uncompressed files in the source must include msidbFileAttributesNoncompressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="dea2b-119">Los archivos sin comprimir deben estar ubicados en la raíz del árbol de origen.</span><span class="sxs-lookup"><span data-stu-id="dea2b-119">The uncompressed files must be located at the root of the source tree.</span></span>

<span data-ttu-id="dea2b-120">Si la propiedad [**Resumen de recuento de palabras**](word-count-summary.md) tiene establecida la marca sin comprimir, los archivos se tratan como sin comprimir de forma predeterminada y los archivos comprimidos deben incluir msidbFileAttributesCompressed en la columna atributos de la tabla archivo.</span><span class="sxs-lookup"><span data-stu-id="dea2b-120">If the [**Word Count Summary**](word-count-summary.md) property has the uncompressed flag set, files are treated as uncompressed by default and any compressed files must include msidbFileAttributesCompressed in the Attributes column of the File table.</span></span> <span data-ttu-id="dea2b-121">Todos los archivos comprimidos deben almacenarse en archivos contenedores ubicados en una secuencia de datos dentro del archivo. msi o en un archivo. cab independiente ubicado en la raíz del árbol de origen.</span><span class="sxs-lookup"><span data-stu-id="dea2b-121">All of the compressed files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span>

<span data-ttu-id="dea2b-122">Para obtener más información, consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="dea2b-122">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

</dd> </dl>

 

 




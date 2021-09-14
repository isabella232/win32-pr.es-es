---
description: Una familia de imágenes es un grupo de una o varias imágenes actualizadas de un producto que se han actualizado a la versión más reciente.
ms.assetid: 06a77b35-b593-47e6-9083-46a6b65b7481
title: Tabla ImageFamilies (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ece99e3c42626eb2155f16f2198703dc31b682
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074449"
---
# <a name="imagefamilies-table-patchwizdll"></a>Tabla ImageFamilies (Patchwiz.dll)

Una familia de imágenes es un grupo de una o varias imágenes actualizadas de un producto que se han actualizado a la versión más reciente. Cada imagen actualizada solo puede pertenecer a una familia. Las imágenes actualizadas que pertenecen a una familia de imágenes comparten uno o varios archivos. Cada familia de imágenes tiene su propio archivo de archivador en el archivo .msp que contiene las revisiones binarias y los nuevos archivos necesarios para actualizar las diferencias entre los archivos de destino y los actualizados. El archivo archivador no replica las revisiones binarias y los nuevos archivos usados por los archivos compartidos.

Se requiere una tabla ImageFamilies que contenga al menos un registro en cada base de datos de creación de revisiones (archivo .csv). La función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) usa esta tabla.

La tabla ImageFamilies contiene la información de aplicación de revisiones que se va a agregar a la [tabla Media](media-table.md). Una revisión agrega una entrada a la tabla Media. Cada registro de las tablas ImageFamilies hace referencia a un grupo de imágenes de producto relacionadas que se han actualizado a la versión más reciente del producto.

La tabla ImageFamilies tiene las columnas siguientes. Se puede usar un valor NULL en las columnas MediaSrcPropName, MediaDiskId y FileSequenceStart si la revisión se aplica con Windows Installer y Patchwiz.dll versión 2.0.



| Columna            | Tipo    | Clave | Nullable |
|-------------------|---------|-----|----------|
| Familia            | text    | Y   | N        |
| MediaSrcPropName  | text    |     | Y        |
| MediaDiskId       | integer |     | Y        |
| FileSequenceStart | integer |     | Y        |
| DiskPrompt        | text    |     | Y        |
| VolumeLabel       | text    |     | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia
</dt> <dd>

El valor especificado en este campo es un identificador para un grupo de imágenes de producto relacionadas que se han actualizado a la versión más reciente del producto. Limitado a un total de 8 caracteres alfanuméricos o caracteres de subrayado. El instalador inserta un flujo de archivador en Windows archivo de revisión del instalador (archivo .msp) para cada familia de la tabla. El archivador contiene las revisiones binarias y los nuevos archivos necesarios para actualizar una imagen de destino en una imagen actualizada del producto. El instalador prefida el nombre de familia con CAB de PCW para generar el nombre de secuencia del gabinete que escribe en el campo Gabinete de la nueva entrada \_ \_ de la [tabla](media-table.md) Multimedia.

</dd> <dt>

<span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>MediaSrcPropName
</dt> <dd>

Valor especificado en el campo Origen de la nueva [entrada de la tabla Media](media-table.md) de la imagen actualizada. Este campo solo puede ser NULL si usa la versión 2.0 de Patchwiz.dll y si MinimumRequiredMsiVersion de la tabla Properties [(Patchwiz.dll)](properties-table-patchwiz-dll-.md) está establecido en 200.

</dd> <dt>

<span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>MediaDiskId
</dt> <dd>

El instalador escribe este valor en el campo DiskId del nuevo [registro de tabla Multimedia.](media-table.md) El valor de DiskID debe ser mayor que cualquier DiskID actual en el paquete de destino. El límite de MediaDiskId es 32767. Este campo solo puede ser NULL si usa la versión 2.0 de Patchwiz.dll y si MinimumRequiredMsiVersion de la tabla Properties [(Patchwiz.dll)](properties-table-patchwiz-dll-.md) está establecido en 200.

</dd> <dt>

<span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>FileSequenceStart
</dt> <dd>

Este campo es el número de secuencia del archivo de inicio. Este mismo número de secuencia de archivo no debe existir en dos revisiones para el mismo producto. Para garantizar esto, el valor de este campo debe ser mayor que todos los números de secuencia usados en revisiones anteriores o en el paquete de instalación original. El número de secuencia más grande de una revisión se puede determinar agregando el número total de entradas del archivo de archivador de revisiones al número fileSequenceStart de esa revisión. Una manera de determinar esto es mirar el archivo .ddf generado por [Patchwiz.dll](patchwiz-dll.md) durante la creación de la revisión. El límite de FileSequenceStart es 32767. Este campo solo puede ser NULL si usa la versión 2.0 de Patchwiz.dll y si MinimumRequiredMsiVersion de la tabla Properties [(Patchwiz.dll)](properties-table-patchwiz-dll-.md) está establecido en 200.

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

El instalador escribe este valor en el campo DiskPrompt del nuevo [registro de tabla Multimedia.](media-table.md)

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

El instalador escribe este valor en el campo VolumeLabel del nuevo registro Multimedia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La revisión agrega el nombre del gabinete en el archivo .msp al campo Gabinete del nuevo registro agregado a la [tabla Media](media-table.md). Dado que es un gabinete incrustado, el nombre tiene como prefijo un carácter \# ''. La revisión agrega una propiedad al campo Origen del nuevo registro en la tabla Media. No dos revisiones pueden tener la misma propiedad de origen.

Los archivos que se comparten dentro de la familia de imágenes deben tener la misma clave de tabla de archivos en cada imagen actualizada de la familia. Las claves de tabla de archivos compartidas entre las imágenes actualizadas deben representar el mismo archivo y ser idénticas en todas las imágenes actualizadas. La clave de tabla de archivos es el valor especificado en la columna Archivo de la [tabla Archivo](file-table.md).

El límite de MediaDiskId y FileSequenceStart es 32767. Para aumentar este límite, exporte la tabla ImageFamilies a un archivo .idt conMsidb.exey cambie el tipo de columna de i2 a i4, o de I2 a I4 y, a continuación, vuelva a importar el archivo .idt [ en ](msidb-exe.md) la base de datos .oracle. Las transformaciones y revisiones no se pueden crear entre dos paquetes que tienen tipos de columna diferentes.

 

 




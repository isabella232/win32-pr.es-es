---
description: Una familia de imágenes es un grupo de una o varias imágenes actualizadas de un producto que se han actualizado a la versión más reciente.
ms.assetid: 06a77b35-b593-47e6-9083-46a6b65b7481
title: Tabla ImageFamilies (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ece99e3c42626eb2155f16f2198703dc31b682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001435"
---
# <a name="imagefamilies-table-patchwizdll"></a>Tabla ImageFamilies (Patchwiz.dll)

Una familia de imágenes es un grupo de una o varias imágenes actualizadas de un producto que se han actualizado a la versión más reciente. Cada imagen actualizada solo puede pertenecer a una familia. Las imágenes actualizadas que pertenecen a una familia de imágenes comparten uno o varios archivos. Cada familia de imágenes tiene su propio archivo. cab en el archivo. MSP que contiene las revisiones binarias y los nuevos archivos necesarios para actualizar las diferencias entre los archivos de destino y los actualizados. El archivo. cab no Replica las revisiones binarias y los nuevos archivos usados por los archivos compartidos.

Se requiere una tabla ImageFamilies que contenga al menos un registro en cada base de datos de creación de revisiones (archivo. PCP). La función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) usa esta tabla.

La tabla ImageFamilies contiene la información de revisión que se va a agregar a la [tabla de medios](media-table.md). Una revisión agrega una entrada a la tabla de medios. Cada registro de las tablas de ImageFamilies hace referencia a un grupo de imágenes de producto relacionadas que se han actualizado a la versión más reciente del producto.

La tabla ImageFamilies tiene las columnas siguientes. Se puede utilizar un valor null en las columnas MediaSrcPropName, MediaDiskId y FileSequenceStart si la revisión se aplica con Windows Installer y Patchwiz.dll versión 2,0.



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

El valor especificado en este campo es un identificador de un grupo de imágenes de producto relacionadas que se han actualizado a la versión más reciente del producto. Limitado a un total de 8 caracteres alfanuméricos o de subrayado. El instalador inserta una secuencia de archivos. cab en el archivo de revisión de Windows Installer (archivo. msp) de cada familia de la tabla. El archivo. cab contiene las revisiones binarias y los nuevos archivos necesarios para actualizar una imagen de destino en una imagen actualizada del producto. El instalador precede el nombre de familia con el \_ archivo CAB \_ de PCW para generar el nombre de flujo del archivador que entra en el campo del archivo. cab de la nueva entrada de la [tabla de medios](media-table.md) .

</dd> <dt>

<span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>MediaSrcPropName
</dt> <dd>

Valor especificado en el campo de origen de la nueva entrada de [tabla de medios](media-table.md) de la imagen actualizada. Este campo solo puede ser null si usa la versión 2,0 de Patchwiz.dll y si MinimumRequiredMsiVersion en la tabla de [propiedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md) está establecido en 200.

</dd> <dt>

<span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>MediaDiskId
</dt> <dd>

El instalador especifica este valor en el campo dipatine del nuevo registro de la [tabla de medios](media-table.md) . El valor del dipatine debe ser mayor que el del paquete de destino actual. El límite de MediaDiskId es 32767. Este campo solo puede ser null si usa la versión 2,0 de Patchwiz.dll y si MinimumRequiredMsiVersion en la tabla de [propiedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md) está establecido en 200.

</dd> <dt>

<span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>FileSequenceStart
</dt> <dd>

Este campo es el número de secuencia del archivo de inicio. Este mismo número de secuencia de archivo no debe existir en dos revisiones para el mismo producto. Para garantizar esto, el valor de este campo debe ser mayor que todos los números de secuencia usados en revisiones anteriores o en el paquete de instalación original. El número de secuencia más alto de una revisión puede determinarse agregando el número total de entradas del archivo. cab de la revisión al número FileSequenceStart de esa revisión. Una manera de determinar esto es examinar el archivo. DDF generado por [Patchwiz.dll](patchwiz-dll.md) durante la creación de la revisión. El límite de FileSequenceStart es 32767. Este campo solo puede ser null si usa la versión 2,0 de Patchwiz.dll y si MinimumRequiredMsiVersion en la tabla de [propiedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md) está establecido en 200.

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

El instalador especifica este valor en el campo DiskPrompt del nuevo registro de la [tabla de medios](media-table.md) .

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

El instalador especifica este valor en el campo VolumeLabel del nuevo registro multimedia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La revisión agrega el nombre del archivador en el archivo. MSP al campo Cabinet del nuevo registro agregado a la tabla de [medios](media-table.md). Dado que es un archivo. cab incrustado, el nombre tiene como prefijo un \# carácter ' '. La revisión agrega una propiedad al campo de origen del nuevo registro en la tabla de medios. Dos revisiones no pueden tener la misma propiedad Source.

Los archivos que se comparten dentro de la familia de imágenes deben tener la misma clave de tabla de archivo en cada imagen actualizada de la familia. Todas las claves de tabla de archivos compartidas entre las imágenes actualizadas deben representar el mismo archivo y deben ser idénticas en todas las imágenes actualizadas. La clave de la tabla de archivos es el valor especificado en la columna archivo de la [tabla archivo](file-table.md).

El límite de MediaDiskId y FileSequenceStart es 32767. Para aumentar este límite, exporte la tabla ImageFamilies a un archivo. IDT con [Msidb.exe](msidb-exe.md) y cambie el tipo de columna de i2 a I4, o de i2 a I4, y, a continuación, importe el archivo. IDT de nuevo a la base de datos. PCP. Las transformaciones y revisiones no se pueden crear entre dos paquetes que tienen tipos de columna diferentes.

 

 




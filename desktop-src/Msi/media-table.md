---
description: En la tabla de medios se describe el conjunto de discos que componen el medio de origen para la instalación.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Tabla de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361850"
---
# <a name="media-table"></a>Tabla de medios

En la tabla de medios se describe el conjunto de discos que componen el medio de origen para la instalación.

La tabla de medios contiene las columnas que se muestran en la tabla siguiente.



| Columna       | Tipo                     | Clave | Nullable |
|--------------|--------------------------|-----|----------|
| Detectaron       | [Entero](integer.md)   | Y   | N        |
| LastSequence | [Entero](integer.md)   | N   | N        |
| DiskPrompt   | [Texto](text.md)         | N   | Y        |
| Archiva      | [Archiva](cabinet.md)   | N   | Y        |
| VolumeLabel  | [Texto](text.md)         | N   | Y        |
| Source       | [Propiedad](property.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>Detectaron
</dt> <dd>

Determina el criterio de ordenación de la tabla. Este número debe ser igual o mayor que 1.

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

Número de secuencia de archivo para el último archivo de este medio. Los números de la columna LastSequence especifican qué archivos de la tabla de [archivos](file-table.md) se encuentran en un disco de origen determinado. Cada disco de origen contiene todos los archivos con números de secuencia (como se muestra en la columna secuencia de la tabla de archivos) menores o iguales que el valor de la columna LastSequence, y mayor que el valor LastSequence del disco anterior (o mayor que 0, para la primera entrada de la tabla de medios). Este número no debe ser negativo; el límite máximo es de 32767 archivos. Para obtener más información sobre cómo crear un paquete de Windows Installer con más archivos, vea [crear un paquete de gran tamaño](authoring-a-large-package.md).

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

El nombre del disco, que suele ser el texto visible impreso en el disco. Este texto traducible se usa para preguntar al usuario cuando es necesario insertar este disco.

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Archiva
</dt> <dd>

El nombre del archivo. cab si algunos o todos los archivos almacenados en el medio se comprimen en un archivo. cab. Si no se usan contenedores, esta columna debe estar en blanco. El nombre del archivo. cab debe utilizar la sintaxis del tipo de datos del [archivo. cab](cabinet.md) . Windows Installer requiere siempre un origen válido para reparar los archivos incluidos en los archivos. cab insertados. Cuando Windows Installer instala un paquete que contiene un archivo. cab incrustado, el sistema puede guardar una copia del archivo. cab. Esta copia no se puede usar para reparar el archivo. cab. Para conservar espacio en disco, use archivos. cab externos en lugar de archivos. cab incrustados.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Etiqueta atribuida al volumen. Esta es la etiqueta de volumen devuelta por la función [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) . Si la propiedad [**SourceDir**](sourcedir.md) hace referencia a un volumen extraíble (disquete o CD-ROM), esta etiqueta de volumen se usa para comprobar que el disco adecuado se encuentra en la unidad antes de intentar instalar archivos. La entrada de esta columna debe coincidir con la etiqueta de volumen del medio físico.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuentes
</dt> <dd>

Este campo solo se usa en la revisión y, de lo contrario, se deja en blanco. Una transformación de revisión puede escribir aquí una propiedad que es la ubicación del archivo. cab que contiene los archivos de revisión o los nuevos archivos agregados por la revisión. Se debe especificar un origen diferente para estos archivos porque el origen del paquete de revisión se puede almacenar por separado del origen del producto. Si el campo del archivo. cab está vacío, el instalador omite el valor de esta columna. Si este campo está vacío, el instalador usa el valor de la propiedad [**SourceDir**](sourcedir.md) como origen del archivo. cab.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el nombre del archivo. cab está precedido por un signo de número ( \# ), los archivos que hacen referencia a este registro de tabla multimedia se empaquetan en un archivo. cab que se almacena en la base de datos como una secuencia independiente.

Para obtener más información sobre cómo agregar archivadores a las tablas de archivos y las tablas de medios, consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).

Windows Installer requiere que el archivo. msi esté en el primer disco de medios extraíbles (CD, DVD o disquete) usado para la instalación del producto.

**Determinar el SourceMode**

La propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) determina el modo de origen de la instalación actual. Si esta propiedad se establece en 2 o 3, se supone la instalación de un archivo. cab. En este modo, se supone que los archivos. cab existen en el directorio indicado por la propiedad [**SourceDir**](sourcedir.md) . Si el valor de tipo de origen es 0 o 1, se supone que todos los archivos de código fuente existen en el árbol cuya raíz se indica mediante la propiedad **SourceDir** .

Tenga en cuenta que esto solo se aplica a los archivos de la tabla de archivos que no tienen los bits comprimidos o sin comprimir establecidos en la columna atributos. Estos bits invalidan el valor de la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) al determinar si un archivo determinado está comprimido o descomprimido.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE35](ice35.md)  
[ICE58](ice58.md)  
[ICE71](ice71.md)  
[ICE81](ice81.md)  
</dl>

 

 

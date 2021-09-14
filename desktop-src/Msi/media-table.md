---
description: En la tabla Multimedia se describe el conjunto de discos que forma el medio de origen para la instalación.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Tabla multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071910"
---
# <a name="media-table"></a>Tabla multimedia

En la tabla Multimedia se describe el conjunto de discos que forma el medio de origen para la instalación.

La tabla Media contiene las columnas que se muestran en la tabla siguiente.



| Columna       | Tipo                     | Clave | Nullable |
|--------------|--------------------------|-----|----------|
| DiskId       | [Entero](integer.md)   | Y   | N        |
| LastSequence | [Entero](integer.md)   | N   | N        |
| DiskPrompt   | [Texto](text.md)         | N   | Y        |
| Gabinete      | [Gabinete](cabinet.md)   | N   | Y        |
| VolumeLabel  | [Texto](text.md)         | N   | Y        |
| Source       | [Propiedad](property.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId
</dt> <dd>

Determina el criterio de ordenación de la tabla. Este número debe ser igual o mayor que 1.

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

Número de secuencia de archivo para el último archivo de este medio. Los números de la columna LastSequence especifican cuáles de los archivos de la [tabla File](file-table.md) se encuentran en un disco de origen determinado. Cada disco de origen contiene todos los archivos con números de secuencia (como se muestra en la columna Secuencia de la tabla File) menor o igual que el valor de la columna LastSequence y mayor que el valor LastSequence del disco anterior (o mayor que 0, para la primera entrada de la tabla Media). Este número debe ser no negativo; el límite máximo es de 32767 archivos. Para obtener más información sobre cómo crear un paquete Windows Installer con más archivos, vea [Creación de un paquete grande.](authoring-a-large-package.md)

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

Nombre del disco, que suele ser el texto visible impreso en el disco. Este texto localizable se usa para preguntar al usuario cuándo es necesario insertar este disco.

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Gabinete
</dt> <dd>

Nombre del gabinete si algunos o todos los archivos almacenados en los medios se comprimen en un archivo de archivador. Si no se usa ningún gabinete, esta columna debe estar en blanco. El nombre del gabinete debe usar la sintaxis del tipo de datos [Cabinet.](cabinet.md) Windows El instalador siempre requiere un origen válido para reparar los archivos incluidos en los archivos de archivador insertados. Cuando Windows instalador instala un paquete que contiene un archivo de archivador incrustado, el sistema puede guardar una copia del archivo de archivador. Esta copia no se puede usar para reparar el archivo de archivador. Para ahorrar espacio en disco, use archivos de archivador externos en lugar de archivos de archivador incrustados.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Etiqueta atribuida al volumen. Esta es la etiqueta de volumen devuelta por la [**función GetVolumeInformation.**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) Si la [**propiedad SourceDir**](sourcedir.md) hace referencia a un volumen extraíble (disquete o CD-ROM), esta etiqueta de volumen se usa para comprobar que el disco adecuado está en la unidad antes de intentar instalar archivos. La entrada de esta columna debe coincidir con la etiqueta de volumen del medio físico.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuente
</dt> <dd>

Este campo solo se usa mediante la aplicación de revisiones y, de lo contrario, se deja en blanco. Una transformación de revisión puede escribir aquí una propiedad que sea la ubicación del archivo de archivador que contiene los archivos de revisión o los nuevos archivos agregados por la revisión. Es necesario especificar un origen diferente para estos archivos porque el origen del paquete de revisión se puede almacenar independientemente del origen del producto. Si el campo Gabinete está vacío, el instalador omite el valor de esta columna. Si este campo está vacío, el instalador usa el valor de la [**propiedad SourceDir**](sourcedir.md) como origen del archivador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el nombre del gabinete va precedido de un signo de número ( ), los archivos que hacen referencia a este registro de tabla multimedia se empaquetan en un archivo de archivador que se almacena en la base de datos como una \# secuencia independiente.

Para obtener más información sobre cómo agregar archivadores a las tablas File y Media, vea [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

Windows El instalador requiere que el .msi esté en el primer disco de medios extraíbles (CD, DVD o disquete) usados para la instalación del producto.

**Determinar sourceMode**

La [**propiedad Resumen de recuento de**](word-count-summary.md) palabras determina el modo de origen de la instalación actual. Si esta propiedad se establece en 2 o 3, se supone que hay una instalación de gabinete. En este modo, se supone que los archivos de archivador existen en el directorio indicado por la [**propiedad SourceDir.**](sourcedir.md) Si el valor de Tipo de origen es 0 o 1, se supone que todos los archivos de origen existen en el árbol cuya raíz se indica mediante la **propiedad SourceDir.**

Tenga en cuenta que esto solo se aplica a los archivos de la tabla File que no tienen los bits comprimidos o sin comprimir establecidos en la columna attributes. Estos bits invalidan el valor de la propiedad [**Resumen de recuento**](word-count-summary.md) de palabras al determinar si un archivo determinado está comprimido o descomprimido.

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

 

 

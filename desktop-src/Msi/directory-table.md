---
description: La tabla Directory especifica el diseño del directorio para el producto. Cada fila de la tabla indica un directorio tanto en el origen como en el destino.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabla de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158574"
---
# <a name="directory-table"></a>Tabla de directorios

La tabla Directory especifica el diseño del directorio para el producto. Cada fila de la tabla indica un directorio tanto en el origen como en el destino.

La tabla Directory tiene las columnas siguientes.



| Columna            | Tipo                         | Clave | Nullable |
|-------------------|------------------------------|-----|----------|
| Directorio         | [Identificador](identifier.md) | Y   | N        |
| Elemento primario \_ del directorio | [Identificador](identifier.md) | N   | Y        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directorio
</dt> <dd>

La columna Directorio contiene un identificador único para una ruta de acceso de directorio o directorio. Esta columna puede contener el nombre de una propiedad que se establece en la ruta de acceso completa de un directorio de destino. Si esta columna contiene una propiedad, el directorio de destino toma el nombre especificado en la columna DefaultDir y toma el directorio primario especificado en la columna Directory \_ Parent.

El directorio de origen siempre toma el nombre especificado en la columna DefaultDir y toma el directorio primario especificado en la columna Directory \_ Parent.

Si la columna Directory Parent es null o igual que el valor de la columna Directory, la columna \_ Directory representa un directorio de destino raíz. Solo se puede especificar un directorio raíz en la tabla Directory.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Elemento primario \_ del directorio
</dt> <dd>

Esta columna es una referencia al directorio primario del directorio. Un registro que tiene una columna Directory Parent igual a NULL o igual a \_ la columna Directory representa un directorio raíz. La ruta de acceso completa del directorio primario se resuelve por referencia en la columna Directory Parent (Primario del directorio) es una \_ clave externa en la columna Directory . Por ejemplo, si una carpeta tiene un directorio primario denominado PDIR, el directorio primario de PDIR se da en la columna Directory Parent de la fila con PDIR en la \_ columna Directory .

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

La columna DefaultDir contiene el nombre del directorio (localizable) en el directorio primario. De forma predeterminada, este es el nombre de los directorios de origen y de destino. Para especificar nombres de directorio de origen y de destino diferentes, separe los nombres de destino y de origen con dos puntos como se muestra a continuación: \[ targetname \] : \[ sourcename \] .

Si el valor de la columna Directory Parent es NULL o es igual a la columna Directory, la columna DefaultDir especifica el nombre de un \_ directorio de origen raíz.

Para un directorio de origen no raíz, un punto (.) especificado en la columna DefaultDir para el nombre del directorio de origen o el nombre del directorio de destino indica que el directorio debe estar ubicado en su directorio primario sin un subdirectorio.

Los nombres de directorio de esta columna pueden tener el formato de pares de nombre de archivo largo \| de nombre de archivo cortos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cada registro de la tabla representa un directorio en las imágenes de origen y de destino. La tabla Directory debe especificar un único directorio raíz con un valor de columna Directory igual a la [**propiedad TARGETDIR.**](targetdir.md)

Para una [instalación administrativa,](administrative-installation.md)instale la imagen administrativa en el directorio raíz denominado TARGETDIR y use los nombres de directorio de origen para resolver los directorios de destino.

Tenga en cuenta que el instalador establece una serie de propiedades [estándar en](properties.md) las rutas de acceso de carpeta del sistema. Consulte la [Referencia de propiedades](property-reference.md) para obtener una lista de las propiedades que se establecen en carpetas del sistema.

La resolución de directorios se realiza durante [la acción CostFinalize](costfinalize-action.md) y se realiza de la manera siguiente:

### <a name="root-destination-directory"></a>Directorio de destino raíz

Solo puede haber un único directorio de destino raíz. Para especificar el directorio de destino raíz, establezca la columna Directory en la [**propiedad TARGETDIR**](targetdir.md) y la columna DefaultDir en [**la propiedad SourceDir.**](sourcedir.md) Si se define la propiedad **TARGETDIR,** el directorio de destino se resuelve en el valor de la propiedad. Si la **propiedad TARGETDIR** no está definida, se usa [**la propiedad ROOTDRIVE**](rootdrive.md) para resolver la ruta de acceso.

### <a name="root-source-directory"></a>Directorio de origen raíz

El valor de la columna DefaultDir para la entrada del directorio raíz debe establecerse en la [**propiedad SourceDir.**](sourcedir.md)

### <a name="non-root-destination-directories"></a>Directorios de destino no raíz

El valor directory de un directorio no raíz también se interpreta como el nombre de una propiedad que define la ubicación del destino. Si se define la propiedad , el directorio de destino se resuelve en el valor de la propiedad. Si no se define la propiedad , el directorio de destino se resuelve en un subdirectorio debajo del directorio de destino resuelto para la entrada Directory \_ Parent. El valor DefaultDir define el nombre del subdirectorio.

### <a name="non-root-source-directories"></a>Directorios de origen no raíz

El directorio de origen de un directorio no raíz se resuelve en un subdirectorio del directorio de origen resuelto para la entrada Directory \_ Parent. De nuevo, el valor DefaultDir define el nombre del subdirectorio.

### <a name="short-or-long-file-names"></a>Nombres de archivo cortos o largos

Al resolver directorios de destino, se usan los nombres de archivo cortos especificados en la columna DefaultDir si se establece la propiedad [**SHORTFILENAMES**](shortfilenames.md) o el volumen en el que se encuentra el directorio no admite nombres de archivo largos. De lo contrario, se usa el nombre de archivo long.

Tenga en cuenta que cuando los directorios se resuelven durante la [](properties.md) acción CostFinalize, las claves de la tabla Directory se convierten en propiedades establecidas en rutas de acceso de directorio.

[CreateFolder Table](createfolder-table.md)

Para crear carpetas vacías durante una instalación, vea [CreateFolder Table](createfolder-table.md).

[Uso de la tabla de directorios](using-the-directory-table.md)

Para obtener más información sobre la tabla Directory, incluidos ejemplos, vea [Using the Directory Table](using-the-directory-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE56](ice56.md)  
[ICE57](ice57.md)  
[ICE64](ice64.md)  
[ICE88](ice88.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 




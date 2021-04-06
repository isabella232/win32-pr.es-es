---
description: La tabla de directorios especifica el diseño del directorio para el producto. Cada fila de la tabla indica un directorio tanto en el origen como en el destino.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabla de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002272"
---
# <a name="directory-table"></a>Tabla de directorio

La tabla de directorios especifica el diseño del directorio para el producto. Cada fila de la tabla indica un directorio tanto en el origen como en el destino.

La tabla de directorio tiene las columnas siguientes.



| Columna            | Tipo                         | Clave | Nullable |
|-------------------|------------------------------|-----|----------|
| Directorio         | [Identificador](identifier.md) | Y   | N        |
| Directorio \_ primario | [Identificador](identifier.md) | N   | Y        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Active
</dt> <dd>

La columna de directorio contiene un identificador único para un directorio o ruta de acceso de directorio. Esta columna puede contener el nombre de una propiedad que se establece en la ruta de acceso completa de un directorio de destino. Si esta columna contiene una propiedad, el directorio de destino toma el nombre especificado en la columna DefaultDir y toma el directorio primario especificado en la \_ columna principal del directorio.

El directorio de origen siempre toma el nombre especificado en la columna DefaultDir y toma el directorio primario especificado en la \_ columna principal del directorio.

Si la \_ columna principal del directorio es null o igual al valor de la columna Directory, la columna Directory representa un directorio de destino raíz. Solo se puede especificar un directorio raíz en la tabla de directorios.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directorio \_ primario
</dt> <dd>

Esta columna es una referencia al directorio principal del directorio. Un registro que tiene una \_ columna principal de directorio igual a NULL o igual que la columna de directorio representa un directorio raíz. La ruta de acceso completa del directorio principal se resuelve por referencia en la \_ columna principal del directorio es una clave externa en la columna directorio. Por ejemplo, si una carpeta tiene un directorio principal denominado PDIR, el directorio principal de PDIR se proporciona en la \_ columna principal de directorio de la fila con PDIR en la columna directorio.

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

La columna DefaultDir contiene el nombre del directorio (localizable) en el directorio principal. De forma predeterminada, es el nombre de los directorios de origen y de destino. Para especificar los nombres de directorio de origen y de destino diferentes, separe los nombres de origen y de destino con un signo de dos puntos de la manera siguiente: \[ targetName \] : \[ SourceName \] .

Si el valor de la \_ columna principal del directorio es null o es igual a la columna de directorio, la columna DefaultDir especifica el nombre de un directorio de origen raíz.

Para un directorio de origen no raíz, un punto (.) especificado en la columna DefaultDir para el nombre del directorio de origen o el nombre del directorio de destino indica que el directorio debe estar ubicado en el directorio primario sin un subdirectorio.

Los nombres de directorio de esta columna se pueden formatear como pares de nombre de archivo corto de nombre de archivo \| .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cada registro de la tabla representa un directorio en las imágenes de origen y de destino. La tabla de directorio debe especificar un único directorio raíz con un valor de columna de directorio igual a la propiedad [**targetDir**](targetdir.md) .

Para una [instalación administrativa](administrative-installation.md), instale la imagen administrativa en el directorio raíz denominado targetdir y use los nombres de directorio de origen para resolver los directorios de destino.

Nota el instalador establece varias propiedades estándar en [las](properties.md) rutas de acceso a las carpetas del sistema. Vea la [referencia](property-reference.md) de propiedades para obtener una lista de las propiedades que se establecen en carpetas del sistema.

La resolución de directorios se realiza durante la [acción CostFinalize](costfinalize-action.md) y se realiza de la siguiente manera:

### <a name="root-destination-directory"></a>Directorio de destino raíz

Solo puede haber un único directorio de destino de raíz. Para especificar el directorio raíz de destino, establezca la columna directorio en la propiedad [**targetDir**](targetdir.md) y la columna DefaultDir en la propiedad [**SourceDir**](sourcedir.md) . Si se define la propiedad **targetDir** , el directorio de destino se resuelve en el valor de la propiedad. Si la propiedad **targetDir** es undefined, la propiedad [**ROOTDRIVE**](rootdrive.md) se utiliza para resolver la ruta de acceso.

### <a name="root-source-directory"></a>Directorio de origen raíz

El valor de la columna DefaultDir para la entrada de directorio raíz debe establecerse en la propiedad [**SourceDir**](sourcedir.md) .

### <a name="non-root-destination-directories"></a>Directorios de destino no raíz

El valor del directorio de un directorio no raíz también se interpreta como el nombre de una propiedad que define la ubicación del destino. Si se define la propiedad, el directorio de destino se resuelve en el valor de la propiedad. Si no se define la propiedad, el directorio de destino se resuelve en un subdirectorio bajo el directorio de destino resuelto para la \_ entrada principal del directorio. El valor de DefaultDir define el nombre del subdirectorio.

### <a name="non-root-source-directories"></a>Directorios de origen no raíz

El directorio de origen de un directorio no raíz se resuelve en un subdirectorio del directorio de origen resuelto para la \_ entrada principal del directorio. De nuevo, el valor de DefaultDir define el nombre del subdirectorio.

### <a name="short-or-long-file-names"></a>Nombres de archivo cortos o largos

Al resolver directorios de destino, se usan los nombres cortos de archivo especificados en la columna DefaultDir si se establece la propiedad [**SHORTFILENAMES**](shortfilenames.md) o el volumen en el que se encuentra el directorio no admite nombres de archivo largos. De lo contrario, se usa el nombre de archivo largo.

Tenga en cuenta que cuando se resuelven los directorios durante la acción CostFinalize, las claves de la tabla de directorio se convierten en [propiedades](properties.md) establecidas en rutas de acceso de directorio.

[CreateFolder (tabla)](createfolder-table.md)

Para crear carpetas vacías durante una instalación, vea [CreateFolder Table](createfolder-table.md).

[Usar la tabla de directorio](using-the-directory-table.md)

Para obtener más información acerca de la tabla de directorios, incluidos ejemplos, consulte [uso de la tabla de directorios](using-the-directory-table.md).

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

 

 




---
description: Esta tabla contiene una lista de archivos que se mueven o copian desde un directorio de origen especificado a un directorio de destino especificado.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Tabla MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818579"
---
# <a name="movefile-table"></a>Tabla MoveFile

Esta tabla contiene una lista de archivos que se mueven o copian desde un directorio de origen especificado a un directorio de destino especificado.

La tabla MoveFile tiene las columnas siguientes.



| Columna       | Tipo                         | Clave | Nullable |
|--------------|------------------------------|-----|----------|
| FileKey      | [Identificador](identifier.md) | Y   | N        |
| Componente\_  | [Identificador](identifier.md) | N   | N        |
| SourceName   | [Texto](text.md)             | N   | Y        |
| DestName     | [Nombre de archivo](filename.md)     | N   | Y        |
| Carpetadeorigen | [Identificador](identifier.md) | N   | Y        |
| DestFolder   | [Identificador](identifier.md) | N   | N        |
| Opciones      | [Entero](integer.md)       | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Clave principal que identifica de forma única un registro MoveFile determinado.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la [tabla de componentes](component-table.md). Si el componente al que hace referencia esta clave no está seleccionado para la instalación o la eliminación, no se realiza ninguna acción en esta entrada MoveFile.

</dd> <dt>

<span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName
</dt> <dd>

Esta columna contiene el nombre traducible de los archivos de origen que se van a copiar o copiar. Esta columna puede dejarse en blanco. Vea la descripción de la columna Carpetadeorigen. Este campo debe contener un nombre de archivo largo y puede contener caracteres comodín ( \* y?).

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

Esta columna contiene el nombre traducible que se va a asignar al archivo original una vez que se ha copiado o copiado. Si este campo está en blanco, el archivo de destino recibe el mismo nombre que el archivo de origen.

</dd> <dt>

<span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>Carpetadeorigen
</dt> <dd>

Esta columna contiene el nombre de una propiedad que tiene un valor que se resuelve en la ruta de acceso completa al directorio de origen. Si la columna SourceName se deja en blanco, se supone que la propiedad denominada en la columna Carpetadeorigen contiene la ruta de acceso completa al archivo de código fuente (incluido el nombre de archivo).

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

Nombre de una propiedad cuyo valor se resuelve en la ruta de acceso completa al directorio de destino.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opciones
</dt> <dd>

Valor entero que especifica el modo de funcionamiento.



| Constante                     | Hexadecimal | Decimal | Significado               |
|------------------------------|-------------|---------|-----------------------|
| (ninguno)                       | 0x000       | 0       | Copie el archivo de código fuente. |
| **msidbMoveFileOptionsMove** | 0x001       | 1       | Mueva el archivo de código fuente. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si \* se escribe un carácter comodín "" en la columna SourceName de la tabla MoveFile y se especifica un nombre de archivo de destino en la columna DestName, todos los archivos que se han copiado o copiado conservan los nombres en los orígenes.

La [acción MoveFiles](movefiles-action.md)procesa esta tabla.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE85](ice85.md)  
</dl>

 

 




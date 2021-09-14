---
description: Esta tabla contiene una lista de archivos que se van a mover o copiar de un directorio de origen especificado a un directorio de destino especificado.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Tabla MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261092"
---
# <a name="movefile-table"></a>Tabla MoveFile

Esta tabla contiene una lista de archivos que se van a mover o copiar de un directorio de origen especificado a un directorio de destino especificado.

La tabla MoveFile tiene las columnas siguientes.



| Columna       | Tipo                         | Clave | Nullable |
|--------------|------------------------------|-----|----------|
| FileKey      | [Identificador](identifier.md) | Y   | N        |
| Componente\_  | [Identificador](identifier.md) | N   | N        |
| SourceName   | [Texto](text.md)             | N   | Y        |
| DestName     | [Nombre de archivo](filename.md)     | N   | Y        |
| SourceFolder | [Identificador](identifier.md) | N   | Y        |
| DestFolder   | [Identificador](identifier.md) | N   | N        |
| Opciones      | [Entero](integer.md)       | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Clave principal que identifica de forma única un registro MoveFile determinado.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la [tabla Component](component-table.md). Si el componente al que hace referencia esta clave no está seleccionado para la instalación o eliminación, no se toma ninguna acción en esta entrada MoveFile.

</dd> <dt>

<span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName
</dt> <dd>

Esta columna contiene el nombre localizable de los archivos de origen que se van a mover o copiar. Es posible que esta columna se haya dejado en blanco. Consulte la descripción de la columna SourceFolder. Este campo debe contener un nombre de archivo largo y puede contener caracteres comodín ( \* y ?).

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

Esta columna contiene el nombre localizable que se va a proporcionar al archivo original después de moverlo o copiarlo. Si este campo está en blanco, el archivo de destino tiene el mismo nombre que el archivo de origen.

</dd> <dt>

<span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder
</dt> <dd>

Esta columna contiene el nombre de una propiedad que tiene un valor que se resuelve en la ruta de acceso completa al directorio de origen. Si la columna SourceName se deja en blanco, se supone que la propiedad denominada en la columna SourceFolder contiene la ruta de acceso completa al propio archivo de origen (incluido el nombre de archivo).

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
| (ninguno)                       | 0x000       | 0       | Copie el archivo de origen. |
| **msidbMoveFileOptionsMove** | 0x001       | 1       | Mueva el archivo de origen. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si se especifica un carácter comodín " " en la columna SourceName de la tabla MoveFile y se especifica un nombre de archivo de destino en la columna DestName, todos los archivos movidos o copiados conservan los nombres de los \* orígenes.

Esta tabla se procesa mediante la [acción MoveFiles](movefiles-action.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE85](ice85.md)  
</dl>

 

 




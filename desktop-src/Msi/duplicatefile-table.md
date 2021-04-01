---
description: La tabla DuplicateFile contiene una lista de archivos que se van a duplicar, ya sea en un directorio diferente al del archivo original o en el mismo directorio, pero con un nombre diferente. El archivo original debe ser un archivo instalado por la acción InstallFiles.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Tabla DuplicateFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082783"
---
# <a name="duplicatefile-table"></a>Tabla DuplicateFile

La tabla DuplicateFile contiene una lista de archivos que se van a duplicar, ya sea en un directorio diferente al del archivo original o en el mismo directorio, pero con un nombre diferente. El archivo original debe ser un archivo instalado por la [acción InstallFiles](installfiles-action.md).

La tabla DuplicateFile tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| FileKey     | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |
| Archivo\_      | [Identificador](identifier.md) | N   | N        |
| DestName    | [Nombre de archivo](filename.md)     | N   | Y        |
| DestFolder  | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Una clave principal, un token no localizado, que identifica un registro DuplicateFile único.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Una clave externa a la primera columna de la [tabla de componentes](component-table.md). Si el componente identificado por la clave no está seleccionado para la instalación o la eliminación, no se realiza ninguna acción en este registro DuplicateFile.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

Clave externa en la [tabla de archivos](file-table.md) que representa el archivo original que se va a duplicar.

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

Nombre traducible que se va a asignar al archivo duplicado. Si este campo está en blanco, el archivo de destino recibe el mismo nombre que el archivo original.

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

Nombre de una propiedad que es la ruta de acceso completa a la que se va a copiar el archivo duplicado. Si este directorio es el mismo que el directorio que contiene el archivo original y el nombre del archivo duplicado propuesto es el mismo que el original, no se realiza ninguna acción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La tabla se procesa mediante la [acción DuplicateFiles](duplicatefiles-action.md) y la [acción RemoveDuplicateFiles](removeduplicatefiles-action.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
</dl>

 

 




---
description: La tabla RemoveFile contiene una lista de archivos que la acción RemoveFiles va a quitar. Establecer la columna FileName de esta tabla en Null admite la eliminación de carpetas vacías.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Tabla RemoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cf63e9b7616eb033a696da2ad29cb4310e6dc0dc56279ef465c3c549cb5437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082605"
---
# <a name="removefile-table"></a>Tabla RemoveFile

La tabla RemoveFile contiene una lista de archivos que la acción [RemoveFiles](removefiles-action.md)va a quitar. Establecer la columna FileName de esta tabla en Null admite la eliminación de carpetas vacías.

La tabla RemoveFile tiene las columnas siguientes.



| Columna      | Tipo                                     | Clave | Nullable |
|-------------|------------------------------------------|-----|----------|
| FileKey     | [Identificador](identifier.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md)             | N   | N        |
| FileName    | [WildCardFilename](wildcardfilename.md) | N   | Y        |
| DirProperty | [Identificador](identifier.md)             | N   | N        |
| InstallMode | [Entero](integer.md)                   | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Clave principal usada para identificar esta entrada de tabla concreta.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa de la primera columna de la [tabla Component](component-table.md). Este campo hace referencia al componente que controla el archivo que se va a quitar.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nombre
</dt> <dd>

Esta columna contiene el nombre localizable del archivo que se va a quitar. Si esta columna es NULL, se quitará la carpeta especificada si está vacía. Todos los archivos que coincidan con el carácter comodín se quitarán del directorio especificado.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nombre de una propiedad cuyo valor se supone que se resuelve en la ruta de acceso completa a la carpeta del archivo que se va a quitar. La propiedad puede ser el nombre de un directorio de la tabla [Directory](directory-table.md), una propiedad establecida por la tabla [AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa.

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode
</dt> <dd>

Debe ser uno de los siguientes valores:



| Constante                                | Hexadecimal | Decimal | Descripción                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbRemoveFileInstallModeOnInstall** | 0x001       | 1       | Quite solo cuando se instale el componente asociado (msiInstallStateLocal o msiInstallStateSource). |
| **msidbRemoveFileInstallModeOnRemove**  | 0x002       | 2       | Quitar solo cuando se quita el componente asociado (msiInstallStateAbsent).                           |
| **msidbRemoveFileInstallModeOnBoth**    | 0x003       | 3       | Quite en cualquiera de los casos anteriores.                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las referencias de archivo de esta tabla se procesan mediante la [acción RemoveFiles](removefiles-action.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE64](ice64.md)  
</dl>

 

 




---
description: La tabla RemoveFile contiene una lista de archivos que se van a quitar mediante la acción RemoveFiles. La configuración de la columna FileName de esta tabla en NULL admite la eliminación de carpetas vacías.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Tabla RemoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911333"
---
# <a name="removefile-table"></a>Tabla RemoveFile

La tabla RemoveFile contiene una lista de archivos que se van a quitar mediante la [acción RemoveFiles](removefiles-action.md). La configuración de la columna FileName de esta tabla en NULL admite la eliminación de carpetas vacías.

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

Clave principal usada para identificar esta entrada de tabla determinada.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa la primera columna de la [tabla de componentes](component-table.md). Este campo hace referencia al componente que controla el archivo que se va a quitar.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión
</dt> <dd>

Esta columna contiene el nombre traducible del archivo que se va a quitar. Si esta columna es null, se quitará la carpeta especificada si está vacía. Todos los archivos que coinciden con el carácter comodín se quitarán del directorio especificado.

</dd> <dt>

<span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty
</dt> <dd>

Nombre de una propiedad cuyo valor se supone que se va a resolver como la ruta de acceso completa a la carpeta del archivo que se va a quitar. La propiedad puede ser el nombre de un directorio en la [tabla del directorio](directory-table.md), una propiedad establecida por la [tabla AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa.

</dd> <dt>

<span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode
</dt> <dd>

Debe ser uno de los valores siguientes.



| Constante                                | Hexadecimal | Decimal | Descripción                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| **msidbRemoveFileInstallModeOnInstall** | 0x001       | 1       | Quitar solo cuando se está instalando el componente asociado (msiInstallStateLocal o msiInstallStateSource). |
| **msidbRemoveFileInstallModeOnRemove**  | 0x002       | 2       | Quitar solo cuando se quita el componente asociado (msiInstallStateAbsent).                           |
| **msidbRemoveFileInstallModeOnBoth**    | 0x003       | 3       | Quítelo en cualquiera de los casos anteriores.                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [acción RemoveFiles](removefiles-action.md)procesa las referencias de archivo en esta tabla.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE64](ice64.md)  
</dl>

 

 




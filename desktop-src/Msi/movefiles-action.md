---
description: La acción MoveFiles busca los archivos existentes en el equipo del usuario y los mueve o copia en una nueva ubicación.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Acción MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8581cd19569109c0f7697b5dfebf33e91b33da9ba84d15caf424242e4e21ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945049"
---
# <a name="movefiles-action"></a>Acción MoveFiles

La acción MoveFiles busca los archivos existentes en el equipo del usuario y los mueve o copia en una nueva ubicación. La acción MoveFiles consulta la tabla [MoveFile](movefile-table.md) y mueve los archivos especificados allí si se especifica que el componente vinculado a las entradas se instale localmente o se ejecute desde el origen.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MoveFiles debe ir después de [la acción InstallValidate](installvalidate-action.md) y antes de [la acción InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                  |
|-------|---------------------------------------------|
| \[1\] | Identificador del archivo movido.                   |
| \[6\] | Tamaño del archivo instalado en bytes.            |
| \[9\] | Identificador del directorio que contiene el archivo movido. |



 

## <a name="remarks"></a>Comentarios

La tabla MoveFiles contiene una columna denominada "options" que especifica los archivos de origen que se van a mover o copiar. Se elimina un archivo de origen movido después de copiarlo en una nueva ubicación. Para obtener la sintaxis exacta, vea la [tabla MoveFile](movefile-table.md).

Las columnas SourceFolder y DestFolder de la tabla MoveFile son nombres de propiedad cuyos valores se espera que se resuelvan en rutas de acceso completas. Estas propiedades pueden ser cualquiera de las entradas de directorio de la tabla [Directory,](directory-table.md) cualquier propiedad de carpeta predefinida [**(FavoritesFolder**](favoritesfolder.md), por ejemplo) o una propiedad establecida por cualquier entrada de la [tabla AppSearch.](appsearch-table.md) Estas propiedades pueden contener una ruta de acceso completa que contiene el nombre de archivo de un archivo específico. Por ejemplo, se puede crear la tabla AppSearch para buscar un archivo determinado y establecer una propiedad en la ruta de acceso completa a ese archivo. En este ejemplo, la columna SourceName de la tabla MoveFile se puede dejar en blanco para indicar que el valor de la propiedad SourceFolder contiene una ruta de acceso de archivo completa. El punto y coma es el delimitador de lista para transformaciones, orígenes y revisiones y no debe usarse en nombres de archivo o rutas de acceso.

La acción MoveFiles no actúa sobre las entradas de la tabla MoveFile en las que la propiedad SourceFolder o DestFolder no se evalúa como una ruta de acceso completa.

La acción MoveFiles intenta mover o copiar todos los archivos del directorio de origen que coincidan con el nombre especificado en la columna SourceName de la tabla MoveFiles. El nombre de la columna SourceName puede incluir o \* ? caracteres comodín que permiten mover o copiar un grupo de archivos. Por ejemplo, la columna SourceName puede contener una entrada de ".xls" y la acción MoveFiles mueve o copia cada libro Microsoft Excel desde el directorio de origen al \* destino.

El nombre que se va a dar al archivo de destino se puede especificar en la columna DestName de la tabla MoveFile. El nombre del archivo de destino conserva el nombre del archivo de origen si esta columna se deja en blanco.

Si se especifica un carácter comodín " " en la columna SourceName de la tabla MoveFile y se especifica un nombre de archivo de destino en la \* columna DestName, todos los archivos movidos o copiados conservan los nombres de los orígenes. [](movefile-table.md)

Los archivos que se mueven o copian mediante la acción MoveFiles no se eliminan cuando se desinstala el producto.

 

 




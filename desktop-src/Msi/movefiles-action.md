---
description: La acción MoveFiles busca los archivos existentes en el equipo del usuario y mueve o copia esos archivos en una nueva ubicación.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Acción MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913482"
---
# <a name="movefiles-action"></a>Acción MoveFiles

La acción MoveFiles busca los archivos existentes en el equipo del usuario y mueve o copia esos archivos en una nueva ubicación. La acción MoveFiles consulta la [tabla MoveFile](movefile-table.md) y mueve los archivos especificados allí si el componente vinculado a las entradas se especifica para que se instale localmente o se ejecute desde el origen.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MoveFiles debe aparecer después de la acción [InstallValidate](installvalidate-action.md) y antes de la acción [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                  |
|-------|---------------------------------------------|
| \[1\] | Identificador del archivo que se ha pasado.                   |
| \[6\] | Tamaño del archivo instalado en bytes.            |
| \[9\] | Identificador del directorio que contiene el archivo que se ha cambiado. |



 

## <a name="remarks"></a>Observaciones

La tabla MoveFiles contiene una columna denominada "Options" que especifica los archivos de origen que se van a copiar o copiar. Un archivo de origen que se ha despasado se elimina una vez copiado en una nueva ubicación. Para ver la sintaxis exacta, vea la [tabla MoveFile](movefile-table.md).

Las columnas Carpetadeorigen y DestFolder de la tabla MoveFile son nombres de propiedad cuyos valores se espera que se resuelvan en rutas de acceso completas. Estas propiedades pueden ser cualquiera de las entradas de directorio de la tabla de [directorio](directory-table.md) , cualquier propiedad de carpeta predefinida ([**FavoritesFolder**](favoritesfolder.md), por ejemplo) o una propiedad establecida por cualquier entrada de la tabla [AppSearch](appsearch-table.md) . Estas propiedades pueden contener una ruta de acceso completa que contenga el nombre de archivo a un archivo específico. Por ejemplo, se puede crear la tabla AppSearch para buscar un archivo determinado y establecer una propiedad en la ruta de acceso completa a ese archivo. En este ejemplo, la columna SourceName de la tabla MoveFile puede dejarse en blanco para indicar que el valor de la propiedad Carpetadeorigen contiene una ruta de acceso completa al archivo. El punto y coma es el delimitador de lista para las transformaciones, los orígenes y las revisiones, y no debe usarse en los nombres de archivo o rutas de acceso.

La acción MoveFiles no actúa sobre las entradas de la tabla MoveFile en las que la propiedad Carpetadeorigen o DestFolder no se evalúa como una ruta de acceso completa.

La acción MoveFiles intenta trasladar o copiar todos los archivos del directorio de origen que coinciden con el nombre dado en la columna SourceName de la tabla MoveFiles. El nombre de la columna SourceName puede incluir \* o? caracteres comodín que permiten que un grupo de archivos se muevan o se copien. Por ejemplo, la columna SourceName puede contener una entrada de " \* . xls" y la acción MoveFiles mueve o copia cada libro de Microsoft Excel del directorio de origen al de destino.

El nombre que se va a asignar al archivo de destino se puede especificar en la columna DestName de la tabla MoveFile. El nombre de archivo de destino conserva el nombre del archivo de código fuente si esta columna se deja en blanco.

Si \* se escribe un carácter comodín "" en la columna SourceName de la [tabla MoveFile](movefile-table.md) y se especifica un nombre de archivo de destino en la columna DestName, todos los archivos que se han copiado o copiado conservan los nombres en los orígenes.

Los archivos que se mueven o copian mediante la acción MoveFiles no se eliminan cuando se desinstala el producto.

 

 




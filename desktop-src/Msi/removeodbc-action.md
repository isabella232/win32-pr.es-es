---
description: La acción RemoveODBC quita los orígenes de datos, traductores y controladores enumerados para su eliminación durante la instalación.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Acción RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6619bc5b8a18cff2ee33dbe45261764c682953bad75a17cb9d6e93cbe487147b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580435"
---
# <a name="removeodbc-action"></a>Acción RemoveODBC

La acción RemoveODBC quita los orígenes de datos, traductores y controladores enumerados para su eliminación durante la instalación. Esta acción consulta la [tabla ODBCDataSource,](odbcdatasource-table.md)la tabla [ODBCTranslator](odbctranslator-table.md)y la tabla [ODBCDriver](odbcdriver-table.md) para cada origen de datos, traductor o controlador programado para su eliminación.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

Para cada controlador instalado.



| Campo | Descripción de los datos de acción               |
|-------|------------------------------------------|
| \[1\] | Descripción del controlador. Clave del controlador ODBC. |
| \[2\] | Componentid                              |



 

Para cada traductor instalado.



| Campo | Descripción de los datos de acción               |
|-------|------------------------------------------|
| \[1\] | Descripción del controlador. Clave del controlador ODBC. |
| \[2\] | Componentid                              |



 

Para cada origen de datos instalado.



| Campo | Descripción de los datos de acción                              |
|-------|---------------------------------------------------------|
| \[1\] | Descripción del controlador. Clave del controlador ODBC.                |
| \[2\] | Componentid                                             |
| \[3\] | Registro: SQL \_ REMOVE \_ DSN o SQL \_ REMOVE SYS \_ \_ DSN |



 

## <a name="remarks"></a>Comentarios

Si el recuento de uso de ODBC y el recuento de uso de archivos se convierten en cero, se quita el archivo. El registro depende de los recuentos de uso de ODBC y la eliminación de archivos se basa en los recuentos de referencias de claves dll compartidas.

 

 




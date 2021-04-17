---
description: La acción RemoveODBC quita los orígenes de datos, los traductores y los controladores que se muestran para su eliminación durante la instalación.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Acción RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667469"
---
# <a name="removeodbc-action"></a>Acción RemoveODBC

La acción RemoveODBC quita los orígenes de datos, los traductores y los controladores que se muestran para su eliminación durante la instalación. Esta acción consulta la tabla [ODBCDataSource](odbcdatasource-table.md), la [tabla ODBCTranslator](odbctranslator-table.md)y la tabla [ODBCDriver](odbcdriver-table.md) para cada origen de datos, traductor o controlador programados para su eliminación.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

Para cada controlador instalado.



| Campo | Descripción de los datos de acción               |
|-------|------------------------------------------|
| \[1\] | Descripción del controlador. La clave del controlador ODBC. |
| \[2\] | ComponentId                              |



 

Para cada traductor instalado.



| Campo | Descripción de los datos de acción               |
|-------|------------------------------------------|
| \[1\] | Descripción del controlador. La clave del controlador ODBC. |
| \[2\] | ComponentId                              |



 

Para cada origen de datos instalado.



| Campo | Descripción de los datos de acción                              |
|-------|---------------------------------------------------------|
| \[1\] | Descripción del controlador. La clave del controlador ODBC.                |
| \[2\] | ComponentId                                             |
| \[3\] | Registro: SQL \_ Remove \_ DSN o SQL \_ Remove \_ Sys \_ DSN |



 

## <a name="remarks"></a>Observaciones

Si el recuento de uso de ODBC y el recuento de uso de archivo se vuelven cero, se quita el archivo. El registro depende de los recuentos de uso de ODBC y la eliminación de archivos se basa en recuentos de referencias clave de dll compartidas.

 

 




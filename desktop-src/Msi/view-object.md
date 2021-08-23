---
description: El objeto View representa un conjunto de resultados obtenido al procesar una consulta mediante el método OpenView del objeto Database.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Ver objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f5025df952ce6e3c5ce43bf3dcb93748a241702b8c4e2f52cd9d0fd00103dc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145278"
---
# <a name="view-object"></a>Ver objeto

El **objeto View** representa un conjunto de resultados obtenido al procesar una consulta mediante el método [**OpenView**](database-openview.md) del [**objeto Database.**](database-object.md) Antes de que se puedan transferir datos, la consulta debe ejecutarse mediante el método [**Execute**](view-execute.md) y pasarle todos los parámetros reemplazables designados dentro de la SQL consulta. La consulta se puede ejecutar de nuevo, con parámetros diferentes si es necesario, pero solo después de liberar el conjunto de resultados mediante la captura de todos los registros o mediante una llamada [**al método Close.**](view-close.md)

## <a name="members"></a>Miembros

El **objeto View** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto View** tiene estos métodos.



| Método                            | Descripción                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cerrar**](view-close.md)       | Finaliza la ejecución de consultas y libera los recursos de base de datos.<br/>                                                                                                          |
| [**Ejecutar**](view-execute.md)   | Usa el token de signo de interrogación para representar parámetros en una SQL consulta. Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.<br/> |
| [**traer**](view-fetch.md)       | Devuelve un [**objeto Record**](record-object.md) que contiene los datos de columna solicitados si hay más filas disponibles en el conjunto de resultados; de lo contrario, devuelve null.<br/>      |
| [**GetError**](view-geterror.md) | Devuelve el error de validación y el nombre de columna para los que se produjo el error.<br/>                                                                                           |
| [**Modificar**](view-modify.md)     | Modifica una fila de base de datos con un [**objeto Record**](record-object.md) modificado obtenido por el [**método Fetch.**](view-fetch.md)<br/>                                   |



 

### <a name="properties"></a>Propiedades

El **objeto View** tiene estas propiedades.



| Propiedad                                         | Descripción                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**ColumnInfo**](view-columninfo.md)<br/> | Devuelve un [**objeto Record**](record-object.md) que contiene la información solicitada sobre cada columna del conjunto de resultados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView se define como \_ 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





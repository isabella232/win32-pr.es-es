---
description: El objeto de vista representa un conjunto de resultados obtenido al procesar una consulta mediante el método OpenView del objeto de base de datos.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Objeto de vista
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
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680432"
---
# <a name="view-object"></a>Objeto de vista

El objeto de **vista** representa un conjunto de resultados obtenido al procesar una consulta mediante el método [**OpenView**](database-openview.md) del objeto de [**base de datos**](database-object.md) . Antes de transferir los datos, se debe ejecutar la consulta mediante el método [**Execute**](view-execute.md) , pasando todos los parámetros reemplazables designados en la cadena de consulta SQL. La consulta se puede volver a ejecutar, con parámetros diferentes, si es necesario, pero solo después de liberar el conjunto de resultados mediante la captura de todos los registros o mediante una llamada al método [**Close**](view-close.md) .

## <a name="members"></a>Miembros

El objeto de **vista** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **vista** tiene estos métodos.



| Método                            | Descripción                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cercanos**](view-close.md)       | Finaliza la ejecución de la consulta y libera los recursos de la base de datos.<br/>                                                                                                          |
| [**Ejecut**](view-execute.md)   | Utiliza el token de signo de interrogación para representar los parámetros de una consulta SQL. Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.<br/> |
| [**Recopila**](view-fetch.md)       | Devuelve un objeto de [**registro**](record-object.md) que contiene los datos de la columna solicitada si hay más filas disponibles en el conjunto de resultados; de lo contrario, devuelve NULL.<br/>      |
| [**GetError**](view-geterror.md) | Devuelve el error de validación y el nombre de columna para los que se produjo el error.<br/>                                                                                           |
| [**Modificar**](view-modify.md)     | Modifica una fila de base de datos con un objeto de [**registro**](record-object.md) modificado obtenido por el método [**Fetch**](view-fetch.md) .<br/>                                   |



 

### <a name="properties"></a>Propiedades

El objeto de **vista** tiene estas propiedades.



| Propiedad                                         | Descripción                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**ColumnInfo**](view-columninfo.md)<br/> | Devuelve un objeto de [**registro**](record-object.md) que contiene la información solicitada sobre cada columna del conjunto de resultados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView se define como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





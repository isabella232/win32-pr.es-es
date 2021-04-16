---
description: El objeto de base de datos tiene acceso a una base de datos del instalador.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Objeto de base de datos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671681"
---
# <a name="database-object"></a>Objeto de base de datos

El objeto de **base de datos** tiene acceso a una base de datos del instalador.

El objeto de **base de datos** se libera cuando se saca del ámbito o cuando la variable de objeto asociada a él está establecida en NULL. Se debe llamar al método [**commit**](database-commit.md) antes de liberar el objeto de **base de datos** para escribir todos los cambios persistentes. Si no se llama al método **commit** , el instalador realiza una reversión implícita al destruir el objeto.

El cliente puede utilizar el siguiente procedimiento para el acceso a los datos.

**Para consultar la secuenciación de API**

1.  Obtenga un objeto de **base de datos** mediante una llamada a los objetos [**OpenDatabase**](installer-opendatabase.md) o [**Installer**](installer-object.md) .
2.  Inicie una consulta con una cadena SQL llamando al método [**OpenView**](database-openview.md) del objeto de **base de datos** .
3.  Establezca los parámetros de consulta en un objeto de [**registro**](record-object.md) y ejecute la consulta de base de datos llamando al método [**Execute**](view-execute.md) del objeto [**View**](view-object.md) . Esto genera un resultado que se puede capturar o actualizar.
4.  Llame a el método [**Fetch**](view-fetch.md) del objeto de [**vista**](view-object.md) varias veces para devolver los objetos de [**registro**](record-object.md) .
5.  Actualice las filas de la base de datos de un objeto de [**registro**](record-object.md) obtenido por el método [**Fetch**](view-fetch.md) con el método [**Modify**](view-modify.md) del objeto [**View**](view-object.md) .
6.  Libere la consulta y los registros no capturados llamando al método [**Close**](view-close.md) del objeto [**View**](view-object.md) .
7.  Conservar cualquier actualización de la base de datos llamando al método [**commit**](database-commit.md) del objeto de **base de datos** .

## <a name="members"></a>Miembros

El objeto de **base de datos** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **base de datos** tiene estos métodos.



| Método                                                                    | Descripción                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyTransform**](database-applytransform.md)                         | Aplica la transformación a esta base de datos.<br/>                                                                                                                        |
| [**Promete**](database-commit.md)                                         | Finaliza el formulario persistente de la base de datos.<br/>                                                                                                                 |
| [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) | Crea y rellena la secuencia de información de Resumen de un archivo de transformación existente.<br/>                                                                            |
| [**EnableUIPreview**](database-enableuipreview.md)                       | Facilita la creación de cuadros de diálogo y cartelera al proporcionar la compatibilidad necesaria para ver los cuadros de diálogo de la interfaz de usuario almacenados en la base de datos del instalador.<br/> |
| [**Exportación**](database-export.md)                                         | Copia la estructura y los datos de una tabla especificada en un archivo de almacenamiento de texto.<br/>                                                                                   |
| [**GenerateTransform**](database-generatetransform.md)                   | Crea una transformación.<br/>                                                                                                                                           |
| [**Importar**](database-import.md)                                         | Importa una tabla de base de datos de un archivo de almacenamiento de texto.<br/>                                                                                                             |
| [**Sin**](database-merge.md)                                           | Combina la base de datos de referencia con la base de datos base.<br/>                                                                                                          |
| [**AbrirVista**](database-openview.md)                                     | Devuelve un objeto de [**vista**](view-object.md) que representa la consulta especificada por una cadena SQL.<br/>                                                                 |



 

### <a name="properties"></a>Propiedades

El objeto de **base de datos** tiene estas propiedades.



| Propiedad                                                                               | Descripción                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DatabaseState**](database-databasestate.md)<br/>                             | Devuelve el estado de persistencia de la base de datos.<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | Devuelve un objeto de [**registro**](record-object.md) que contiene el nombre de la tabla y los nombres de columna (que comprenden las claves principales).<br/>                        |
| [**SummaryInformation (objeto de base de datos)**](database-summaryinformation.md)<br/> | Devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede utilizar para examinar, actualizar y agregar propiedades a la secuencia de información de resumen.<br/> |
| [**TablePersistent**](database-tablepersistent.md)<br/>                         | Devuelve el estado de persistencia de la tabla.<br/>                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





---
description: El objeto Base de datos tiene acceso a una base de datos del instalador.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158637"
---
# <a name="database-object"></a>Objeto de base de datos

El objeto **Base de** datos tiene acceso a una base de datos del instalador.

El **objeto Database** se libera cuando se sale del ámbito o cuando la variable de objeto asociada a él se establece en null. Se [**debe llamar al**](database-commit.md) método Commit antes de liberar el objeto **Database** para escribir todos los cambios persistentes. Si no se llama al método **Commit,** el instalador realiza una reversión implícita tras la destrucción de objetos.

El cliente puede usar el siguiente procedimiento para el acceso a datos.

**Para consultar la secuenciación de API**

1.  Obtenga un **objeto Database** mediante una llamada [**a OpenDatabase**](installer-opendatabase.md) o [**al objeto Installer.**](installer-object.md)
2.  Inicie una consulta mediante una cadena SQL mediante una llamada al [**método OpenView**](database-openview.md) del **objeto Database.**
3.  Establezca parámetros de consulta en un [**objeto Record**](record-object.md) y ejecute la consulta de base de datos mediante una llamada al [**método Execute**](view-execute.md) del [**objeto View.**](view-object.md) Esto genera un resultado que se puede capturar o actualizar.
4.  Llame al [**método Fetch**](view-fetch.md) del [**objeto View**](view-object.md) repetidamente para devolver [**objetos Record.**](record-object.md)
5.  Actualice las filas de base de [**datos de un objeto Record**](record-object.md) obtenidas por el método [**Fetch**](view-fetch.md) mediante el [**método Modify**](view-modify.md) del [**objeto View.**](view-object.md)
6.  Libere la consulta y los registros sin captura llamando al [**método Close**](view-close.md) del [**objeto View.**](view-object.md)
7.  Conserve las actualizaciones de base de datos llamando al [**método Commit**](database-commit.md) del **objeto Database.**

## <a name="members"></a>Members

El **objeto Database** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Database** tiene estos métodos.



| Método                                                                    | Descripción                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyTransform**](database-applytransform.md)                         | Aplica la transformación a esta base de datos.<br/>                                                                                                                        |
| [**Commit**](database-commit.md)                                         | Completa la forma persistente de la base de datos.<br/>                                                                                                                 |
| [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) | Crea y rellena el flujo de información de resumen de un archivo de transformación existente.<br/>                                                                            |
| [**EnableUIPreview**](database-enableuipreview.md)                       | Facilita la creación de cuadros de diálogo y paneles de diálogo proporcionando la compatibilidad necesaria para ver los cuadros de diálogo de la interfaz de usuario almacenados en la base de datos del instalador.<br/> |
| [**Exportación**](database-export.md)                                         | Copia la estructura y los datos de una tabla especificada en un archivo de archivo de texto.<br/>                                                                                   |
| [**GenerateTransform**](database-generatetransform.md)                   | Crea una transformación.<br/>                                                                                                                                           |
| [**Importar**](database-import.md)                                         | Importa una tabla de base de datos desde un archivo de archivo de texto.<br/>                                                                                                             |
| [**Combinar**](database-merge.md)                                           | Combina la base de datos de referencia con la base de datos base.<br/>                                                                                                          |
| [**Openview**](database-openview.md)                                     | Devuelve un [**objeto View**](view-object.md) que representa la consulta especificada por una SQL cadena.<br/>                                                                 |



 

### <a name="properties"></a>Propiedades

El **objeto Database** tiene estas propiedades.



| Propiedad.                                                                               | Descripción                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DatabaseState**](database-databasestate.md)<br/>                             | Devuelve el estado de persistencia de la base de datos.<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | Devuelve un [**objeto Record**](record-object.md) que contiene el nombre de la tabla y los nombres de columna (que comprende las claves principales).<br/>                        |
| [**SummaryInformation (objeto de base de datos)**](database-summaryinformation.md)<br/> | Devuelve un [**objeto SummaryInfo**](summaryinfo-object.md) que se puede usar para examinar, actualizar y agregar propiedades al flujo de información de resumen.<br/> |
| [**TablePersistent**](database-tablepersistent.md)<br/>                         | Devuelve el estado de persistencia de la tabla.<br/>                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





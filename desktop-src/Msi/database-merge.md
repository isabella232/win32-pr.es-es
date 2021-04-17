---
description: El método Merge del objeto Database combina la base de datos de referencia con la base de datos base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653773"
---
# <a name="databasemerge-method"></a>Database. Merge (método)

El método **Merge** del objeto [**Database**](database-object.md) combina la base de datos de referencia con la base de datos base.

## <a name="syntax"></a>Sintaxis


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*reference* 
</dt> <dd>

Objeto de [**base de datos**](database-object.md) necesario que se va a combinar en la base de datos.

</dd> <dt>

*errorTable* 
</dt> <dd>

Nombre opcional de una tabla que contiene los nombres de las tablas que contienen conflictos de combinación, el número de filas en conflicto dentro de la tabla y una referencia a la tabla con el conflicto de combinación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) y el método **Merge** del objeto [**Database**](database-object.md) no se pueden usar para combinar un módulo incluido en un paquete de instalación. No se deben usar para fusionar mediante combinación [módulos de combinación](merge-modules.md) en un paquete de Windows Installer. Para incluir un módulo de combinación en un paquete de instalación, los autores de paquetes de instalación deben seguir las instrucciones descritas en el tema [aplicar módulos de combinación](applying-merge-modules.md) .

El método **Merge** no copia en la base de datos de destino [los archivos. cab](cabinet-files.md) incrustados o las [transformaciones incrustadas](embedded-transforms.md) de la base de datos de referencia. Los flujos de datos incrustados que se enumeran en la tabla [binaria](binary-table.md) o la [tabla de iconos](icon-table.md) se copian de la base de datos de referencia en la base de datos de destino. Los almacenamientos insertados en la base de datos de referencia no se copian en la base de datos de destino.

Si no se proporciona ninguna tabla, el mensaje de error general proporciona el número de tablas que contienen conflictos de combinación. Se puede pasar cualquier tabla, pero todas las demás columnas deben admitir valores NULL porque la operación para actualizar la [tabla de errores](error-table.md) produce un error si una columna no admite valores NULL. También se puede pasar una tabla recién creada porque el método **Merge** crea automáticamente las columnas que utiliza si se encuentran conflictos de combinación. Se utilizan dos columnas para presentar conflictos de combinación. La primera columna es el nombre de la tabla y la columna de clave principal. La segunda columna es el número de filas de la tabla que tienen errores de combinación.

Si las tablas con el mismo nombre en ambas bases de datos no coinciden en el número de claves principales, los tipos de columna, el número de columnas o los nombres de columna, se produce un error en el método **Merge** y se envía un mensaje de error que indica lo que ocurrió.

Para que la tabla de errores permanezca, el controlador de errores debe confirmar la base de datos a la que pertenece la tabla de errores. Sin embargo, esta confirmación debe realizarse después de usar la tercera columna para obtener las referencias a las tablas en las que se produjeron conflictos de combinación.

Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 





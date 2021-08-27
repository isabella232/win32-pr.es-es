---
description: El método Merge del objeto Database combina la base de datos de referencia con la base de datos base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Método Database.Merge
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
ms.openlocfilehash: 4fad74e1647413b66ebc6910e739750699f4e641c961eff59ecaacbf1e7a41f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074995"
---
# <a name="databasemerge-method"></a>Método Database.Merge

El **método Merge** del objeto [**Database**](database-object.md) combina la base de datos de referencia con la base de datos base.

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

Objeto Database [**necesario que**](database-object.md) se va a combinar en la base de datos.

</dd> <dt>

*errorTable* 
</dt> <dd>

Nombre opcional de una tabla que contiene los nombres de las tablas que contienen conflictos de combinación, el número de filas en conflicto dentro de la tabla y una referencia a la tabla con el conflicto de combinación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La [**función MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) y el **método Merge** del objeto [**Database**](database-object.md) no se pueden usar para combinar un módulo incluido en un paquete de instalación. No deben usarse para combinar módulos [de mezcla](merge-modules.md) en un paquete Windows Installer. Para incluir un módulo de combinación en un paquete de instalación, los autores de los paquetes de instalación deben seguir las instrucciones que se describen en el tema Aplicar módulos [de mezcla.](applying-merge-modules.md)

El **método Merge** no copia los archivos de [archivador](cabinet-files.md) incrustados ni las [transformaciones incrustadas](embedded-transforms.md) de la base de datos de referencia en la base de datos de destino. Los flujos de datos incrustados que [](icon-table.md) aparecen en [la tabla](binary-table.md) binaria o en la tabla de iconos se copian de la base de datos de referencia a la base de datos de destino. Los almacenamientos incrustados en la base de datos de referencia no se copian en la base de datos de destino.

Si no se proporciona ninguna tabla, el mensaje de error general proporciona el número de tablas que contienen conflictos de combinación. Se puede pasar cualquier tabla, pero todas las demás columnas deben ser que aceptan valores NULL porque se produce un error en la operación para actualizar la tabla [de errores](error-table.md) si una columna no acepta valores NULL. También se puede pasar una tabla recién creada porque el método **Merge** crea automáticamente las columnas que usa si se encuentran conflictos de combinación. Se usan dos columnas para presentar conflictos de combinación. La primera columna es el nombre de la tabla y la columna de clave principal. La segunda columna es el número de filas de esa tabla que tienen errores de combinación.

Si las tablas con el mismo nombre en ambas bases de datos no coinciden en el número de claves principales, los tipos de columna, el número de columnas o los nombres de columna, se produce un error en el método **Merge** y se publica un mensaje de error que indica lo que ha ocurrido.

Para que la tabla Error permanezca, el controlador de errores debe confirmar la base de datos a la que pertenece la tabla Error. Sin embargo, esta confirmación debe realizarse después de usar la tercera columna para obtener las referencias a las tablas en las que se produjeron conflictos de combinación.

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 





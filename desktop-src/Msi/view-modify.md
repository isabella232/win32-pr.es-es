---
description: El método Modify del objeto View modifica una fila de base de datos con un objeto record modificado obtenido por el método Fetch.
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: View. Modify (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Modify
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4dc97f2e3b5f85d472cfcbfad6017ce4e051e4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653729"
---
# <a name="viewmodify-method"></a>View. Modify (método)

El método **Modify** del objeto [**View**](view-object.md) modifica una fila de base de datos con un objeto [**Record**](record-object.md) modificado obtenido por el método [**Fetch**](view-fetch.md) .

## <a name="syntax"></a>Sintaxis


```JScript
View.Modify(
  action,
  record
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*action* 
</dt> <dd>

Acción necesaria que se va a realizar en la fila de la base de datos. Esta acción es una de las que se muestran en la tabla siguiente.



| Nombre de acción                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiViewModifySeek**</dt> <dt>: 1</dt> </dl>                                            | Actualiza la información del registro proporcionado sin cambiar la posición en el conjunto de resultados y sin afectar a las operaciones de captura posteriores. Después, el registro se puede usar para la actualización, eliminación y actualización posteriores. Todas las columnas de clave principal de la tabla deben estar en la consulta y el registro debe tener al menos tantos campos como consulta. Seek no se puede usar con consultas multitable. Vea la sección Comentarios. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiViewModifyRefresh**</dt> <dt>0</dt> </dl>                                 | Actualiza la información del registro. Debe llamar primero al método [**Fetch**](view-fetch.md) con el mismo registro. Se produce un error en una fila eliminada. Funciona con registros de lectura y escritura y de solo lectura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiViewModifyInsert**</dt> <dt>1</dt> </dl>                                     | Inserta un registro. Produce un error si existe una fila con las mismas claves principales. Produce un error con una base de datos de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiViewModifyUpdate**</dt> <dt>2</dt> </dl>                                     | Actualiza un registro existente. Solo claves no principales. Debe llamar primero al método [**Fetch**](view-fetch.md) con el mismo registro. Produce un error con un registro eliminado. Solo funciona con registros de lectura y escritura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiViewModifyAssign**</dt> <dt>3</dt> </dl>                                     | Escribe los datos actuales del cursor en una fila de la tabla. Actualiza el registro si las claves principales coinciden con una fila existente e inserta si no coinciden. Produce un error con una base de datos de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiViewModifyReplace**</dt> <dt>4</dt> </dl>                                 | Actualiza o elimina e inserta un registro en una tabla. Debe llamar primero al método [**Fetch**](view-fetch.md) con el mismo registro. Actualiza el registro si no se modifican las claves principales. Elimina la fila antigua e inserta nuevas si han cambiado las claves principales. Produce un error con una base de datos de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiViewModifyMerge**</dt> <dt>5</dt> </dl>                                         | Inserta o valida un registro en una tabla. Inserta si las claves principales no coinciden con ninguna fila y se validan si hay una coincidencia. Se produce un error si el registro no coincide con los datos de la tabla. Se produce un error si hay un registro con una clave duplicada que no es idéntica. Solo funciona con registros de lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiViewModifyDelete**</dt> <dt>6</dt> </dl>                                     | Quita una fila de la tabla. Debe llamar primero al método [**Fetch**](view-fetch.md) con el mismo registro. Se produce un error si se ha eliminado la fila. Solo funciona con registros de lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiViewModifyInsertTemporary**</dt> <dt>7</dt> </dl> | Inserta un registro temporal. La información no es persistente. Produce un error si existe una fila con la misma clave principal. Solo funciona con registros de lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiViewModifyValidate**</dt> <dt>8</dt> </dl>                             | Valida un registro. No se valida entre combinaciones. Debe llamar primero al método [**Fetch**](view-fetch.md) con el mismo registro. Obtiene los errores de validación con el método [**GetError**](view-geterror.md) . Funciona con registros de lectura y escritura y de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiViewModifyValidateNew**</dt> <dt>9</dt> </dl>                 | Valida un nuevo registro. No se valida entre combinaciones. Comprueba si hay claves duplicadas. Obtiene los errores de validación mediante una llamada al método [**GetError**](view-geterror.md) . Requiere llamar al método [**MsiDatabase. OpenView**](database-openview.md) con un valor de modificación. Funciona con registros de lectura y escritura y de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiViewModifyValidateField**</dt> <dt>10</dt> </dl>        | Valida los campos de un registro capturado o nuevo. Puede validar uno o más campos de un registro incompleto. Obtiene los errores de validación mediante una llamada al método [**GetError**](view-geterror.md) . Funciona con registros de lectura y escritura y de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiViewModifyValidateDelete**</dt> <dt>11</dt> </dl>    | Valida un registro que se eliminará más adelante. Debe llamar primero al método [**Fetch**](view-fetch.md) con el mismo registro. Se produce un error si otra fila hace referencia a las claves principales de esta fila. La validación no comprueba la existencia de las claves principales de esta fila en las propiedades o cadenas. No comprueba si una columna es una clave externa para varias tablas. Obtener errores de validación mediante una llamada al método [**GetError**](view-geterror.md) . Funciona con registros de lectura y escritura y de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Obligatorio. Objeto de [**registro**](record-object.md) obtenido por el método de [**captura**](view-fetch.md) con datos de campo modificados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se debe llamar a este método después del método [**Execute**](view-execute.md) .

Para ejecutar cualquier instrucción SQL, se debe crear una vista. Sin embargo, una vista que no crea un conjunto de resultados, como CREATE TABLE o INSERT INTO, no se puede usar con el método **Modify** para actualizar las tablas a través de la vista.

Los valores msiViewModifyValidate, msiViewModifyValidateNew, msiViewModifyValidateField y msiViewModifyValidateDelete del método **Modify** no realizan actualizaciones reales; se aseguran de que los datos del registro sean válidos. El uso de estas acciones requiere que la base de datos contenga una [ \_ tabla de validación](-validation-table.md) .

No se puede capturar un registro que contenga datos binarios de una base de datos y, a continuación, utilizar ese registro para insertar los datos en una base de datos completamente diferente. Para trasladar datos binarios de una base de datos a otra, debe exportar los datos a un archivo y, a continuación, importarlos en la nueva base de datos mediante el método [**SetStream**](record-setstream.md) del objeto de [**registro**](record-object.md) . Esto garantiza que cada base de datos tiene su propia copia de los datos binarios.

> [!Note]  
> Las acciones personalizadas solo pueden agregar, modificar o quitar filas, columnas o tablas temporales de una base de datos. Las acciones personalizadas no pueden modificar los datos persistentes en una base de datos, como los datos que forman parte de la base de datos almacenada en el disco. Para obtener más información, vea [obtener acceso a la sesión del instalador actual desde una acción personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md).

 

Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView se define como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 





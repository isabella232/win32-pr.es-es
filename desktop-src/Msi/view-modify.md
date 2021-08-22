---
description: El método Modify del objeto View modifica una fila de base de datos con un objeto Record modificado obtenido por el método Fetch.
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: View.Modify (método)
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
ms.openlocfilehash: e4149afb638c01b31d51c45f5d55c6f43fe50b4a85b77c25b4f6a5e0ed5993fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498865"
---
# <a name="viewmodify-method"></a>View.Modify (método)

El **método Modify** del objeto [**View**](view-object.md) modifica una fila de base de datos con un objeto [**Record**](record-object.md) modificado obtenido por el [**método Fetch.**](view-fetch.md)

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

Acción necesaria que se debe realizar en la fila de la base de datos. Esta acción es una de las que se muestran en la tabla siguiente.



| Nombre de acción                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiViewModifySeek**</dt> <dt>–1</dt> </dl>                                            | Actualiza la información del registro proporcionado sin cambiar la posición en el conjunto de resultados y sin afectar a las operaciones de captura posteriores. A continuación, el registro se puede usar para las actualizaciones, eliminaciones y actualizaciones posteriores. Todas las columnas de clave principal de la tabla deben estar en la consulta y el registro debe tener al menos tantos campos como la consulta. La búsqueda no se puede usar con consultas multitabla. Consulte los comentarios. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiViewModifyRefresh**</dt> <dt>0</dt> </dl>                                 | Actualiza la información del registro. Primero debe llamar al [**método Fetch**](view-fetch.md) con el mismo registro. Se produce un error en una fila eliminada. Funciona con registros de lectura y escritura y de solo lectura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiViewModifyInsert**</dt> <dt>1</dt> </dl>                                     | Inserta un registro. Se produce un error si existe una fila con las mismas claves principales. Se produce un error con una base de datos de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiViewModifyUpdate**</dt> <dt>2</dt> </dl>                                     | Actualiza un registro existente. Solo claves no principales. Primero debe llamar al [**método Fetch**](view-fetch.md) con el mismo registro. Se produce un error con un registro eliminado. Solo funciona con registros de lectura y escritura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiViewModifyAssign**</dt> <dt>3</dt> </dl>                                     | Escribe los datos actuales del cursor en una fila de tabla. Actualiza el registro si las claves principales coinciden con una fila existente e inserta si no coinciden. Se produce un error con una base de datos de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiViewModifyReplace**</dt> <dt>4</dt> </dl>                                 | Actualiza o elimina e inserta un registro en una tabla. Primero debe llamar al [**método Fetch**](view-fetch.md) con el mismo registro. Actualiza el registro si las claves principales no han cambiado. Elimina la fila anterior e inserta new si las claves principales han cambiado. Se produce un error con una base de datos de solo lectura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiViewModifyMerge**</dt> <dt>5</dt> </dl>                                         | Inserta o valida un registro en una tabla. Inserta si las claves principales no coinciden con ninguna fila y valida si hay una coincidencia. Se produce un error si el registro no coincide con los datos de la tabla. Se produce un error si hay un registro con una clave duplicada que no es idéntica. Solo funciona con registros de lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiViewModifyDelete**</dt> <dt>6</dt> </dl>                                     | Quita una fila de la tabla. Primero debe llamar al [**método Fetch**](view-fetch.md) con el mismo registro. Se produce un error si se ha eliminado la fila. Solo funciona con registros de lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiViewModifyInsertTemporary**</dt> <dt>7</dt> </dl> | Inserta un registro temporal. La información no es persistente. Se produce un error si existe una fila con la misma clave principal. Solo funciona con registros de lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiViewModifyValidate**</dt> <dt>8</dt> </dl>                             | Valida un registro. No valida entre combinaciones. Primero debe llamar al [**método Fetch**](view-fetch.md) con el mismo registro. Obtenga errores de validación con [**el método GetError.**](view-geterror.md) Funciona con registros de solo lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiViewModifyValidateNew**</dt> <dt>9</dt> </dl>                 | Valida un nuevo registro. No valida entre combinaciones. Comprueba si hay claves duplicadas. Obtiene errores de validación llamando al [**método GetError.**](view-geterror.md) Requiere llamar [**al método MsiDatabase.OpenView**](database-openview.md) con un valor modify. Funciona con registros de solo lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiViewModifyValidateField**</dt> <dt>10</dt> </dl>        | Valida los campos de un registro nuevo o capturado. Puede validar uno o varios campos de un registro incompleto. Obtiene errores de validación llamando al [**método GetError.**](view-geterror.md) Funciona con registros de solo lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiViewModifyValidateDelete**</dt> <dt>11</dt> </dl>    | Valida un registro que se eliminará más adelante. Primero debe llamar al [**método Fetch**](view-fetch.md) con el mismo registro. Se produce un error si otra fila hace referencia a las claves principales de esta fila. La validación no comprueba la existencia de las claves principales de esta fila en propiedades o cadenas. No comprueba si una columna es una clave externa para varias tablas. Obtenga errores de validación llamando al [**método GetError.**](view-geterror.md) Funciona con registros de solo lectura y escritura. Este modo no se puede usar con una vista que contenga combinaciones.<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Obligatorio. [**Objeto**](record-object.md) de registro obtenido por el [**método Fetch**](view-fetch.md) con datos de campo modificados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se debe llamar a este método después del [**método Execute.**](view-execute.md)

Para ejecutar cualquier instrucción SQL, se debe crear una vista. Sin embargo, una vista que no crea un conjunto de resultados, como CREATE TABLE o INSERT INTO, no se puede usar con el método **Modify** para actualizar tablas a través de la vista.

Los valores msiViewModifyValidate, msiViewModifyValidateNew, msiViewModifyValidateField y msiViewModifyValidateDelete del método **Modify** no realizan actualizaciones reales; garantizan que los datos del registro son válidos. El uso de estas acciones requiere que la base de datos contenga una [ \_ tabla Validation](-validation-table.md) .

No se puede capturar un registro que contenga datos binarios de una base de datos y, a continuación, usar ese registro para insertar los datos en una base de datos completamente diferente. Para mover datos binarios de una base de datos a otra, debe exportar los datos a un archivo y, a continuación, importarlos en la nueva base de datos mediante el [**método SetStream**](record-setstream.md) del [**objeto Record.**](record-object.md) Esto garantiza que cada base de datos tenga su propia copia de los datos binarios.

> [!Note]  
> Las acciones personalizadas solo pueden agregar, modificar o quitar filas, columnas o tablas temporales de una base de datos. Las acciones personalizadas no pueden modificar datos persistentes en una base de datos, como los datos que forman parte de la base de datos almacenada en disco. Para obtener más información, vea [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md).

 

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView se define como \_ 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 





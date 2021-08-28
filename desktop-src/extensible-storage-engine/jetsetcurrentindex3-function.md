---
description: 'Más información sobre: JetSetCurrentIndex3 (Función)'
title: Función JetSetCurrentIndex3
TOCTitle: JetSetCurrentIndex3 Function
ms:assetid: 50050bd3-4b74-4be7-985c-754ced8aded1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269244(v=EXCHG.10)
ms:contentKeyID: 32765546
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex3A
- JetSetCurrentIndex3W
- JetSetCurrentIndex3
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36aadb42cdf942c802a65f92b5c450535575793b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986658"
---
# <a name="jetsetcurrentindex3-function"></a>Función JetSetCurrentIndex3


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetcurrentindex3-function"></a>Función JetSetCurrentIndex3

La **función JetSetCurrentIndex3** se usa para establecer el índice actual de un cursor. El índice actual de un cursor define qué registros de una tabla son visibles para ese cursor y el orden en el que aparecen seleccionando el conjunto de entradas de índice que se van a usar para exponer esos registros.

```cpp
    JET_ERR JET_API JetSetCurrentIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*szIndexName*

Nombre del índice que se va a seleccionar para el cursor.

Si este parámetro es NULL o una cadena vacía, se seleccionará el índice clúster. Si se define un índice principal para la tabla, ese índice se seleccionará porque es el mismo que el índice clúster. Si no se define ningún índice principal para la tabla, se seleccionará el índice secuencial. El índice secuencial no tiene ninguna definición de índice. Consulte [JetCreateIndex](./jetcreateindex-function.md) para obtener más información.

Si *pindexid* no es NULL, se omitirá el nombre del índice y el índice se seleccionará mediante su identificador de índice.

*grbit*

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitMoveFirst</p> | <p>Esta opción indica que el cursor debe colocarse en la primera entrada del índice especificado. Si se selecciona el índice clúster (índice principal o secuencial) y el índice actual es un índice secundario, JET_bitMoveFirst se supone. Si se selecciona el índice actual, esta opción se omite y no se realiza ningún cambio en la posición del cursor.</p> | 
| <p>JET_bitNoMove</p> | <p>Esta opción indica que el cursor debe colocarse en la entrada de índice del nuevo índice que corresponde al registro asociado a la entrada de índice en la posición actual del cursor en el índice antiguo.</p><p>Si la definición del nuevo índice contiene al menos una columna de clave con varios valores, la entrada del índice de destino es ambigua. En este caso, la <em>itagSequence</em> especificada se usa para seleccionar qué valor múltiple de la columna de clave multivalor más importante se usa para colocar el cursor. Solo es necesario pasar una sola <em>itagSequence</em> incluso en el caso de varias columnas de clave multivalor porque el motor solo expande todos los valores de la columna de clave multivalor más importante. Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex para</a> obtener más detalles.</p><p>Si JET_bitMoveFirst se especifica, se omite esta opción.</p><p>Si se selecciona el índice actual, esta opción se omite y no se realiza ningún cambio en la posición del cursor. Cuando este parámetro no está presente, se supone que su valor JET_bitMoveFirst.</p> | 



*itagSequence*

Número de secuencia del valor de columna multivalor que se usará para colocar el cursor en el nuevo índice.

Este parámetro solo se usa junto con JET_bitNoMove. Consulte la descripción de esta opción para obtener más detalles.

Cuando este parámetro no está presente o está establecido en cero, se supone que su valor es 1.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ningún valor para la primera columna de clave multivalor en la definición del nuevo índice que se corresponda con el número de secuencia especificado.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidIndexId</p> | <p>El contenido del identificador de índice no era válido o ha expirado y debe actualizarse. Esto puede ocurrir para <strong>JetSetCurrentIndex3</strong> cuando:</p><ul><li><p>pindexid- cbStruct no tiene el tamaño esperado &gt; (Windows Server 2003 y versiones posteriores).</p></li><li><p>El motor se ha apagado desde que se ha obtenido el identificador de índice.</p></li><li><p>Se han cerrado todos los cursores que hacen referencia a la tabla que contiene el índice correspondiente al identificador de índice y el motor ha expulsado la definición de ese índice de la caché de esquemas.</p></li><li><p>El identificador de índice se usa con un cursor abierto en la tabla incorrecta.</p></li><li><p>El índice se ha eliminado o aún no está visible para la sesión.</p></li></ul> | 
| <p>JET_errInvalidName</p> | <p>Uno de los nombres de objeto especificados no era válido. Todos los nombres de objeto deben cumplir el mismo conjunto de reglas. Estas reglas son:</p><ul><li><p>Los nombres de objeto deben estar compuestos de caracteres ASCII.</p></li><li><p>Los nombres de objeto deben tener al menos un carácter de longitud.</p></li><li><p>Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</p></li><li><p>Es posible que los nombres de objeto no comiencen por un espacio.</p></li><li><p>Los nombres de objeto no pueden contener caracteres de control ASCII (0x00 a 0x1F).</p></li><li><p>Los nombres de objeto no pueden contener un carácter de signo de exclamación (!), punto (.), corchete izquierdo ([) o corchete derecho (]).</p></li><li><p>Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si lo hubiera) para el nombre del objeto. Esto significa de hecho que los nombres de objeto tampoco pueden contener un espacio.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir <strong>para JetSetCurrentIndex3</strong> cuando <em>pindexid</em> no es NULL y pindexid- cbStruct no tiene el tamaño esperado (Windows XP y versiones &gt; anteriores).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ninguna entrada de índice en el nuevo índice que se corresponda con el registro asociado a la entrada de índice en la posición actual del cursor en el índice antiguo.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errOutOfCursors</p> | <p>El motor ha agotado su grupo de recursos usados para abrir cursores. El número máximo de cursores que se pueden abrir en cualquier momento se controla mediante <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>. Consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter para</a> obtener más información. Esto puede ocurrir para <strong>JetSetCurrentIndex3</strong> cuando se ha seleccionado un índice secundario y el motor no puede abrir un cursor interno para usar ese índice.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, el índice actual del cursor se establece en el índice solicitado. Ahora se pueden buscar entradas de índice mediante [JetSeek](./jetseek-function.md) según la definición de índice del índice solicitado. Las entradas de índice también se pueden enumerar [mediante JetMove](./jetmove-function.md) en el orden especificado por esa definición de índice. La posición actual del cursor se establece en la primera entrada de índice del índice (JET_bitMoveFirst) o en una entrada de índice específica que está relacionada con la posición actual del cursor en el índice antiguo (JET_bitNoMove). No se producirá ningún cambio en el estado de la base de datos.

En caso de error, el índice actual y la posición actual del cursor se encuentran en un estado indefinido. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Si la sugerencia de identificador de índice está obsoleta, la API simplemente produce un error. En este caso, no hay ninguna reserva en el nombre de texto del índice como se podría esperar. El autor de la llamada de la API debe realizar manualmente esta reserva.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetSetCurrentIndex3W</strong> (Unicode) y <strong>JetSetCurrentIndex3A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetSeek](./jetseek-function.md)

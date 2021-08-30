---
description: 'Más información sobre: JetRenameColumn (Función)'
title: JetRenameColumn (Función)
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b48e83416951f30f2c395273438d4c71b482636c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985758"
---
# <a name="jetrenamecolumn-function"></a>JetRenameColumn (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetrenamecolumn-function"></a>JetRenameColumn (Función)

La **función JetRenameColumn** se puede usar para cambiar el nombre de una columna existente en una tabla.

**Windows XP:****JetRenameColumn** se introduce en Windows XP.  

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*szName*

Nombre actual de la columna cuyo nombre se va a cambiar.

*szNameNew*

Nuevo nombre de la columna cuyo nombre se va a cambiar.

*grbit*

Este parámetro debe ser 0.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Esta columna especificada no existe para esta tabla.</p> | 
| <p>JET_errInvalidName</p> | <p>Uno de los nombres de objeto especificados no era válido. Todos los nombres de objeto deben cumplir el mismo conjunto de reglas. Estas reglas son:</p><ul><li><p>Los nombres de objeto deben estar compuestos por caracteres ASCII.</p></li><li><p>Los nombres de objeto deben tener al menos un carácter de longitud.</p></li><li><p>Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</p></li><li><p>Es posible que los nombres de objeto no comiencen por un espacio: los nombres de objeto pueden no contener caracteres de control ASCII (0x00 a 0x1F).</p></li><li><p>Los nombres de objeto no pueden contener un signo de exclamación (!), punto (.), corchete de apertura ([) o carácter de corchete derecho (]).</p></li><li><p>Una vez validado, solo se usará la parte de la cadena hasta el primer espacio (si hay alguno) para el nombre del objeto. Esto significa que los nombres de objeto tampoco pueden contener un espacio.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetRenameColumn</strong> cuando:</p><ul><li><p><em>szName</em> es NULL.</p></li><li><p><em>szNameNew</em> es NULL.</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInTransaction</p> | <p>Esta operación solo se puede realizar cuando la sesión no está actualmente dentro de una transacción.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransReadOnly</p> | <p>No se puede realizar una actualización en el ámbito de una transacción de solo lectura. Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 



Si se ejecuta correctamente, el nombre de la columna especificada en la tabla asociada al cursor cambia permanentemente al nuevo nombre. También se actualizarán los índices que hacen referencia a esa columna.

En caso de error, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

La operación de cambio de nombre de columna no es habitual porque, a diferencia de otras operaciones de esquema, no se lleva a cabo como una transacción. Cuando se cambia el nombre de una columna de una tabla determinada en una sesión, cualquier otra sesión que use esa tabla verá el cambio inmediatamente, incluso si se encuentran en una transacción que impediría que esa sesión vea cualquier otro cambio realizado por la sesión que realiza la operación de cambio de nombre.

El identificador de columna de una columna no se ve afectado por la operación de cambio de nombre.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetRenameColumnW</strong> (Unicode) y <strong>JetRenameColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)

---
description: 'Más información sobre: JetSetColumnDefaultValue (Función)'
title: JetSetColumnDefaultValue (Función)
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b4c624e985cbbef41d3e2a96133af97de6ea250e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887257"
---
# <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue (Función)

La **función JetSetColumnDefaultValue** se puede usar para cambiar el valor predeterminado de una columna existente.

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*Dbid*

Base de datos que se va a usar para esta llamada.

*szTableName*

Nombre de la tabla que contiene la columna que se verá afectada.

*szColumnName*

Nombre de la columna cuyo valor predeterminado se va a cambiar.

*pvData*

Búfer de entrada que contiene el nuevo valor predeterminado.

*cbData*

Tamaño del búfer de entrada que contiene el nuevo valor predeterminado.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores ese, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Igual que JET_errNullInvalid.</p> | 
| <p>JET_errColumnInUse</p> | <p>Esta columna especificada está actualmente en uso por un índice.</p><p><strong>JetSetColumnDefaultValue</strong> no puede cambiar el valor predeterminado de una columna a la que se hace referencia en la definición de un índice. Esto se debe a que, al hacerlo, podría cambiar el contenido del índice.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Esta columna especificada no existe para esta tabla.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>El identificador de base de datos especificado no era válido.</p> | 
| <p>JET_errInvalidName</p> | <p>Uno de los nombres de objeto especificados no era válido. Todos los nombres de objeto deben cumplir el mismo conjunto de reglas. Estas reglas son:</p><ul><li><p>Los nombres de objeto deben estar compuestos de caracteres ASCII.</p></li><li><p>Los nombres de objeto deben tener al menos un carácter de longitud.</p></li><li><p>Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</p></li><li><p>Es posible que los nombres de objeto no comiencen por un espacio.</p></li><li><p>Los nombres de objeto no pueden contener caracteres de control ASCII (0x00 a 0x1F).</p></li><li><p>Los nombres de objeto no pueden contener un carácter de signo de exclamación (!), punto (.), corchete izquierdo ([) o corchete derecho (]).</p></li><li><p>Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si lo hubiera) para el nombre del objeto. Esto significa que los nombres de objeto tampoco pueden contener un espacio.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errNullInvalid</p> | <p>No se pudo establecer la columna en NULL. Esto sucede para <strong>JetSetColumnDefaultValue</strong> cuando:</p><ul><li><p><em>cbData</em> es cero.</p></li><li><p><strong>pvData</strong> es NULL.</p></li></ul><p>Por lo tanto, no es posible establecer el valor predeterminado de una columna (atrás) en NULL o en un valor de longitud cero.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Esta tabla especificada no existe para esta base de datos.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTableInUse</p> | <p>Otra sesión está utilizando esta tabla especificada.</p><p><strong>JetSetColumnDefaultValue</strong> requiere acceso exclusivo a una tabla para cambiar el valor predeterminado de la columna para las versiones anteriores a Windows Server 2003.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransReadOnly</p> | <p>No es posible intentar una actualización cuando se encuentra dentro del ámbito de una transacción de solo lectura. Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errWriteConflict</p> | <p>Otra sesión ha bloqueado previamente el registro para la actualización. Se producirá un error en la actualización intentada por esta sesión.</p> | 



Si se ejecuta correctamente, el valor predeterminado de la columna especificada en la tabla especificada de la base de datos determinada se cambia permanentemente al nuevo valor predeterminado.

En caso de error, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

No es posible cambiar el valor predeterminado de una columna en una tabla de plantillas.

El motor de base de datos truncará de forma silenciosa el valor predeterminado de una columna a 255 bytes para columnas de texto largo y binarias largas.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetSetColumnDefaultValueW</strong> (Unicode) y <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)

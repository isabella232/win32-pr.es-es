---
description: 'Más información sobre: JetGetCurrentIndex (Función)'
title: JetGetCurrentIndex (Función)
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f41114c74643d7165bc16363af3d1777828003b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964252"
---
# <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex (Función)

La **función JetGetCurrentIndex** determina el nombre del índice actual de un cursor determinado. Este nombre también se usa para volver a seleccionar posteriormente ese índice como índice actual mediante [JetSetCurrentIndex](./jetsetcurrentindex-function.md). También se puede usar para detectar las propiedades de ese índice [mediante JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*szIndexName*

Búfer de salida que recibe el nombre del índice actual del cursor.

*cchIndexName*

Tamaño máximo en caracteres del búfer de salida.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir el nombre de índice completo.</p><p>El búfer de salida se ha rellenado con la mayor parte del nombre del índice que cabría. Si el búfer de salida tiene al menos un carácter de longitud, la cadena de ese búfer de salida finalizará en null.</p><p><strong>Nota  </strong> Este error no se devolverá si cchIndexName es cero. Consulte la sección Comentarios para obtener más información.</p> | 



Si se ejecuta correctamente, el nombre del índice actual del cursor especificado se devolverá en el búfer de salida. Si JET_wrnBufferTruncated se devuelve, el búfer de salida contendrá la mayor parte del nombre del índice que cabe en el espacio proporcionado. Si el búfer de salida tiene al menos un carácter de longitud, la cadena devuelta en ese búfer finalizará en null. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, el estado del búfer de salida será indefinido. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Si no hay ningún índice actual para el cursor, se devolverá una cadena vacía. Esto puede ocurrir cuando el cursor está en el índice clúster de la tabla y no se ha definido ningún índice principal. Este índice se conoce como índice secuencial de la tabla y no tiene ninguna definición. En cualquier caso, al establecer el índice actual en una cadena vacía mediante [JetSetCurrentIndex,](./jetsetcurrentindex-function.md) se seleccionará el índice clúster independientemente de la presencia de una definición de índice principal.

Hay un error importante en esta función que está presente en todas las versiones. Si el búfer de salida es demasiado pequeño para recibir el nombre de índice completo y el búfer de salida tiene al menos un carácter de longitud, JET_wrnBufferTruncated no se devolverá. JET_errSuccess se devolverá en su lugar. Para evitar este problema, el búfer de salida siempre debe tener al menos JET_cbNameMost + 1 (65) caracteres de longitud.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetGetCurrentIndexW</strong> (Unicode) y <strong>JetGetCurrentIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)

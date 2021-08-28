---
description: 'Más información sobre: JetRegisterCallback (Función)'
title: Función JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdc87805539619ff644afbd295bfa7f1ac76f075
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482791"
---
# <a name="jetregistercallback-function"></a>Función JetRegisterCallback


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetregistercallback-function"></a>Función JetRegisterCallback

La **función JetRegisterCallback permite** a la aplicación configurar el motor de base de datos para emitir notificaciones a la aplicación para eventos específicos. Estas notificaciones están asociadas a una tabla específica y permanecen en vigor solo hasta que la instancia que contiene la tabla se cierre mediante [JetTerm](./jetterm-function.md).

**Windows XP: JetRegisterCallback** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*cbtyp*

Máscara de bits formada por las razones de devolución de llamada por las que la aplicación desea recibir notificaciones.

Para crear esta máscara de bits, simplemente o juntos motivos de devolución de llamada válidos de [la enumeración JET_CBTYP](./jet-cbtyp.md) bits.

*pCallback*

Puntero de función a la función de devolución de llamada de la aplicación.

*pvContext*

Especifica un puntero de contexto que se va a dar a la función de devolución de llamada para la aplicación.

*phCallbackId*

Devuelve un identificador que se puede usar más adelante para cancelar el registro de la función de devolución de llamada dada [mediante JetUnregisterCallback](./jetunregistercallback-function.md).

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. <strong>JetRegisterCallback</strong> devolverá este error cuando:</p><ul><li><p><em>cbtyp</em> es cero,</p></li><li><p><em>pCallback</em> es NULL.</p></li><li><p><em>phCallbackId</em> es NULL.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, la devolución de llamada especificada se registrará por los motivos de devolución de llamada especificados con la tabla asociada al cursor especificado. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, la devolución de llamada no se registrará. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Comentarios

Este método proporciona un medio para que la aplicación asocie devoluciones de llamada volátiles a una tabla de una base de datos. Si la aplicación desea asociar devoluciones de llamada persistentes a una tabla de la base de datos, debe pasar la devolución de llamada a [JET_TABLECREATE](./jet-tablecreate-structure.md) mediante [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetTerm](./jetterm-function.md)  
[JetUnregisterCallback](./jetunregistercallback-function.md)

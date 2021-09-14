---
description: 'Más información sobre: JetResetTableSequential (Función)'
title: JetResetTableSequential (Función)
TOCTitle: JetResetTableSequential Function
ms:assetid: 5fe9daf2-5ef1-46d6-b0c3-ef92fb57d8bb
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269261(v=EXCHG.10)
ms:contentKeyID: 32765563
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 356fdcbf21dd3b08948936556b40f983ec1ac888
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126962763"
---
# <a name="jetresettablesequential-function"></a>JetResetTableSequential (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetresettablesequential-function"></a>JetResetTableSequential (Función)

La **función JetResetTableSequential** notifica al motor de base de datos que la aplicación ya no está analizando todo el índice actual que contiene un cursor determinado. Esta llamada invierte una notificación enviada por [JetSetTableSequential.](./jetsettablesequential-function.md)

**Windows XP:****JetResetTableSequential** se introdujo en Windows XP.   

```cpp
    JET_ERR JET_API JetResetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores ese, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, el índice actual del cursor ya no está optimizado para un examen secuencial de todo el índice. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, no se producirá ningún cambio en la configuración del cursor. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Es seguro realizar esta llamada en un cursor que no se haya configurado previamente mediante una llamada a [JetSetTableSequential](./jetsettablesequential-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetTableSequential](./jetsettablesequential-function.md)  
[JetStopService](./jetstopservice-function.md)

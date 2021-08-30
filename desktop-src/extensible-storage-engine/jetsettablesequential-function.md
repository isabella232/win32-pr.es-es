---
description: 'Más información sobre: JetSetTableSequential (Función)'
title: JetSetTableSequential (Función)
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9286cc9ffc07f9b03bf6cfa84add8ba5b031fe97
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983318"
---
# <a name="jetsettablesequential-function"></a>JetSetTableSequential (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsettablesequential-function"></a>JetSetTableSequential (Función)

La **función JetSetTableSequential** notifica al motor de base de datos que la aplicación está analizando todo el índice actual que contiene un cursor determinado. Por lo tanto, los métodos que se usan para acceder a los datos de índice se ajustarán para que este escenario sea lo más rápido posible.

**Windows XP:****JetSetTableSequential** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetSetTableSequential(
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

Grupo de bits que especifican cero o más de las siguientes opciones.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitPrereadForward</p> | <p>Esta opción se usa para indexar en la dirección hacia delante.</p><p><strong>Windows 7:</strong><strong>JET_bitPrereadForward</strong> se introdujo en Windows 7.  </p> | 
| <p>JET_bitPrereadBackward</p> | <p>Esta opción se usa para indexar en dirección hacia atrás.</p><p><strong>Windows 7:</strong><strong>JET_bitPrereadBackward</strong> se introdujo en Windows 7.  </p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión se ha puesto en modo de espera como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión encontró un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque todavía no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si esta función se realiza correctamente, el índice actual del cursor se optimiza para un examen secuencial de todo el índice. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, no se producirá ningún cambio en la configuración del cursor. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Si la aplicación necesita examinar eficazmente un subconjunto conocido de un índice, también se realiza una optimización similar siempre que se establece un intervalo de índices [mediante JetSetIndexRange](./jetsetindexrange-function.md). Esta optimización solo está disponible en Windows XP y versiones posteriores.

Si la aplicación necesita examinar eficazmente un subconjunto desconocido de un índice, no se debe realizar ninguna acción. El motor puede detectar automáticamente el comportamiento del examen y capturará los datos con antelación. Sin embargo, este comportamiento no es tan agresivo.

Esta optimización hará que el examen del índice principal sea eficaz y hará que el examen solo sea eficaz de los datos de entrada de índice en un índice secundario. No hará que el examen de un índice secundario al recuperar los datos del registro sea eficaz. Esto se debe a que el motor no realiza una lectura adelantada en los datos de registro.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)

---
description: 'Más información sobre: JetSetLS (Función)'
title: Función JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c94e5dc01d2aff69b699894f88287122cb9530cf
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984288"
---
# <a name="jetsetls-function"></a>Función JetSetLS


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetls-function"></a>Función JetSetLS

La **función JetSetLS permite** a la aplicación asociar un identificador de contexto conocido como Storage local con un cursor o la tabla asociada a ese cursor. La aplicación puede usar este identificador de contexto para almacenar datos auxiliares asociados a un cursor o tabla. Más adelante se notifica a la aplicación mediante una devolución de llamada en tiempo de ejecución cuando se debe liberar el identificador de contexto. Esto permite asociar el estado asignado dinámicamente a un cursor o tabla.

**Windows XP:****JetSetLS** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*ls*

Identificador de contexto que se va a asociar al cursor o a la tabla.

Cuando JET_bitLSReset se especifica , el valor real de este parámetro se omite y JET_LSNil se usa.

*grbit*

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>Esta opción indica que el identificador de contexto debe asociarse al cursor especificado.</p><p>Si no JET_bitLSCursor ni JET_bitLSTable se especifica , JET_bitLSCursor se presupone.</p><p>No es posible usar esta opción con JET_bitLSTable. Se producirá un error en la operación JET_errInvalidgrbit si se intenta.</p> | 
| <p>JET_bitLSReset</p> | <p>Esta opción indica que se debe omitir el identificador de contexto especificado y que el identificador de contexto del objeto elegido se debe restablecer a JET_LSNil.</p><p>Es importante tener en cuenta que esta acción no dará lugar a una devolución de llamada para limpiar el valor anterior del identificador de contexto para el objeto elegido. Se puede lograr una limpieza adecuada del identificador de contexto anterior <a href="gg269234(v=exchg.10).md">mediante JetGetLS</a> con JET_bitLSReset. Consulte <a href="gg269234(v=exchg.10).md">JetGetLS para</a> obtener más información.</p> | 
| <p>JET_bitLSTable</p> | <p>Esta opción indica que el identificador de contexto debe asociarse a la tabla asociada al cursor especificado.</p><p>No es posible usar esta opción con JET_bitLSCursor. Se producirá un error en la operación JET_errInvalidgrbit si se intenta.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una de las opciones solicitadas no era válida, se usaba incorrectamente o no se implementaba. Esto puede ocurrir para <strong>JetSetLS</strong> cuando JET_bitLSCursor y JET_bitLSTable se especifican.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errLSAlreadySet</p> | <p>El identificador de contexto dado no se pudo asociar al objeto solicitado porque ya tenía asociado un identificador de contexto.</p> | 
| <p>JET_errLSCallbackNotSpecified</p> | <p>El identificador de contexto especificado no se pudo asociar al objeto solicitado porque la devolución de llamada en tiempo de ejecución no se ha configurado para la instancia asociada a la sesión.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se realiza correctamente, el identificador de contexto especificado se asoció correctamente al objeto solicitado. No se producirá ningún cambio en el estado de la base de datos.

En caso de error, no se ha producido ningún cambio en el estado del objeto solicitado. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

La configuración Storage local para un cursor o tabla debe considerarse una caché volátil. La aplicación debe intentar primero recuperar el identificador de contexto mediante [JetGetLS.](./jetgetls-function.md) Si no se establece el valor (es decir, es JET_LSNil), la aplicación debe crear un nuevo contexto y cargarlo en la memoria caché mediante **JetSetLS.** La aplicación puede purgar la memoria caché mediante una llamada a [JetGetLS](./jetgetls-function.md) con JET_bitLSReset. Si el motor de base de datos purga la memoria caché, se generará una devolución de llamada en tiempo de ejecución para dar a la aplicación la oportunidad de limpiar ese contexto. El tipo de devolución de llamada se JET_cbtypFreeCursorLS para un identificador de contexto asociado a un cursor y JET_cbtypFreeTableLS para un identificador de contexto asociado a una tabla. En cualquier caso, el identificador de contexto se pasará como pvArg1. Consulte [JET_CALLBACK](./jet-callback-callback-function.md) para obtener más información.

La devolución de llamada en tiempo de ejecución debe configurarse correctamente para la instancia asociada a la sesión especificada antes de que se pueda usar Storage local. Esta devolución de llamada se puede establecer [mediante JetSetSystemParameter](./jetsetsystemparameter-function.md) [con JET_paramRuntimeCallback](./callback-parameters.md). Consulte [JetSetSystemParameter](./jetsetsystemparameter-function.md) y [JET_paramRuntimeCallback](./callback-parameters.md) parámetros del sistema para obtener más información.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)

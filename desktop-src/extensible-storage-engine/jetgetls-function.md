---
description: 'Más información sobre: JetGetLS (Función)'
title: JetGetLS (Función)
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9eb6eed0bbec7be0acd377fa3b34d1b91a8b3fed
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982548"
---
# <a name="jetgetls-function"></a>JetGetLS (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetls-function"></a>JetGetLS (Función)

La **función JetGetLS** permite a la aplicación recuperar el identificador de contexto conocido como Storage local asociado a un cursor o a la tabla asociada a ese cursor. Este identificador de contexto se debe haber establecido previamente mediante [JetSetLS.](./jetsetls-function.md) **JetGetLS también** se puede usar para capturar simultáneamente el identificador de contexto actual de un cursor o tabla y restablecer ese identificador de contexto.

**Windows XP: JetGetLS** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*pls*

Búfer de salida que recibe el identificador de contexto asociado actualmente al cursor o la tabla.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>Indica que se debe recuperar el identificador de contexto asociado al cursor especificado.</p><p>Si no JET_bitLSCursor ni JET_bitLSTable se especifica , JET_bitLSCursor se presupone.</p><p>Esta opción no se puede usar con JET_bitLSTable. La operación producirá un error JET_errInvalidgrbit si se intenta.</p> | 
| <p>JET_bitLSTable</p> | <p>Indica que se debe recuperar el identificador de contexto asociado a la tabla que contiene el cursor especificado. No es posible usar esta opción con JET_bitLSCursor. La operación producirá un error JET_errInvalidgrbit si se intenta.</p> | 
| <p>JET_bitLSReset</p> | <p>Indica que el identificador de contexto del objeto elegido se debe restablecer a JET_LSNil. El valor actual del identificador de contexto se devuelve en el búfer de salida.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una de las opciones solicitadas no era válida, se usaba de forma no válida o no se implementaba.</p><p>Esto puede ocurrir para <strong>JetGetLS</strong> cuando se JET_bitLSCursor y JET_bitLSTable se establecen.</p> | 
| <p>JET_errLSNotSet</p> | <p>No se pudo devolver el identificador de contexto porque no hay ningún identificador de contexto asociado actualmente al objeto solicitado.</p><p><strong>Nota  </strong> Este error no se devuelve si JET_bitLSReset se especifica pero no se ha asociado ningún identificador de contexto con el objeto solicitado.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se realiza correctamente, el identificador de contexto se recuperó correctamente del objeto solicitado. Si JET_bitLSReset especificado, ese identificador de contexto también se quitó correctamente del objeto . No se producirá ningún cambio en el estado de la base de datos.

En caso de error, no se ha producido ningún cambio en el estado del objeto solicitado. No se producirá ningún cambio en el estado de la base de datos.

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
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)

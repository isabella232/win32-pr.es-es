---
description: 'Más información sobre: JetOSSnapshotEnd (Función)'
title: Función JetOSSnapshotEnd
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 890114147950d74dcf2c9004a34cc2c0ab30f61c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471741"
---
# <a name="jetossnapshotend-function"></a>Función JetOSSnapshotEnd


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshotend-function"></a>Función JetOSSnapshotEnd

La **función JetOSSnapshotEnd** notifica al motor que la sesión de instantáneas finalizó.

**Windows Vista:****JetOSSnapshotEnd** se introdujo en Windows Vista:.  

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*grbit*

Opciones de esta llamada. Este parámetro puede tener una combinación de los siguientes valores.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>0</p> | <p>Final correcto de la sesión de instantánea.</p> | 
| <p>JET_bitAbortSnapshot</p> | <p>Sesión de instantánea anulada.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Una de las opciones solicitadas no es válida, se usa incorrectamente o no se implementa.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Ya hay una sesión de instantánea en curso. Esto no está permitido.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>El identificador de la sesión de instantánea no es válido.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>La sesión de instantánea tenía un tiempo de espera interno antes de que se produjese esta llamada. Como resultado, las operaciones de E/S han vuelto a la normalidad antes de que se realizara esta llamada.</p> | 



Si esta función se realiza correctamente, se completará una sesión de instantáneas y se reanudará el comportamiento normal del motor. Más adelante se puede iniciar una nueva sesión de instantáneas.

Si se produce un error en esta función, JET_errOSSnapshotTimeOut el código devuelto y finaliza la sesión de instantánea actual, pero la inmovilización de las E/S durante el período de instantánea no se respeta internamente. Para todos los demás errores, no se cambiará el estado de la sesión de instantánea.

#### <a name="remarks"></a>Comentarios

Se llama a esta función solo si se llamó [a JetOSSnapshotThaw](./jetossnapshotthaw-function.md) con JET_bitContinueAfterThaw.

La sesión de instantánea debe completarse para que se lleve a cabo la comprobación de instantáneas y el truncamiento del registro. Las entradas del registro de eventos se generarán para los distintos pasos de la instantánea.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de ejecución](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)

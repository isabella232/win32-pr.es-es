---
description: 'Más información sobre: JetOSSnapshotEnd (Función)'
title: JetOSSnapshotEnd (Función)
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
ms.openlocfilehash: b57528899b8d78ecee31f6dd54c2ac8decece383
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170334"
---
# <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd (Función)

La **función JetOSSnapshotEnd** notifica al motor que la sesión de instantánea ha finalizado.

**Windows Vista:****JetOSSnapshotEnd** se presenta en Windows Vista:.  

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

Opciones para esta llamada. Este parámetro puede tener una combinación de los valores siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>0</p> | <p>Final correcto de la sesión de instantáneas.</p> | 
| <p>JET_bitAbortSnapshot</p> | <p>Se anuló la sesión de instantánea.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Una de las opciones solicitadas no es válida, se usa incorrectamente o no se implementa.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Ya hay una sesión de instantánea en curso. Esto no está permitido.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>El identificador de la sesión de instantánea no es válido.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>La sesión de instantánea tenía un tiempo de espera interno antes de que se produjese esta llamada. Como resultado, las operaciones de E/S regresaron a la normalidad antes de realizar esta llamada.</p> | 



Si esta función se realiza correctamente, se completará una sesión de instantáneas y se reanudará el comportamiento normal del motor. Más adelante se puede iniciar una nueva sesión de instantáneas.

Si se produce un error en esta función, JET_errOSSnapshotTimeOut devuelve el código devuelto y finaliza la sesión de instantánea actual, pero la inmovilización de las E/S durante el período de instantánea no se respeta internamente. Para todos los demás errores, no se cambiará el estado de la sesión de instantánea.

#### <a name="remarks"></a>Observaciones

Solo se llama a esta función si se llamó [a JetOSSnapshotThaw](./jetossnapshotthaw-function.md) con JET_bitContinueAfterThaw.

La sesión de instantánea debe completarse para que se lleve a cabo la comprobación de la instantánea y el truncamiento del registro. Las entradas del registro de eventos se generarán para los distintos pasos de la instantánea.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de datos](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)

---
description: 'Más información sobre: JetOSSnapshotTruncateLog (Función)'
title: JetOSSnapshotTruncateLog (Función)
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da8e76b1c735f6249f1d7e3893acd1db1743b65
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985868"
---
# <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog (Función)

La **función JetOSSnapshotTruncateLog** habilita el truncamiento del registro para todas las instancias que forman parte de la sesión de instantáneas.

**Windows Vista:****JetOSSnapshotTruncateLog** se introdujo en Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*grbit*

Opciones de esta llamada. Este parámetro puede tener una combinación de los siguientes valores.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitAllDatabasesSnapshot</p> | <p>Todas las bases de datos están conectadas para que el motor de almacenamiento pueda calcular y realizar el truncamiento del registro.</p> | 
| <p>0 (cero)</p> | <p>No se producirá ningún truncamiento.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>El <em>parámetro grbit</em> no es válido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>La sesión de instantánea no está en el estado en el que se puede producir un truncamiento. Las posibles causas son:</p><ul><li><p>la llamada se realiza después de que se haya transcurrido el tiempo de espera de la sesión de instantáneas.</p></li><li><p>la sesión se especificó como una instantánea de copia</p></li></ul> | 



Si se ejecuta correctamente, los archivos de registro de una o todas las instancias de la sesión de instantáneas se truncarán, si es posible.

#### <a name="remarks"></a>Observaciones

Solo se debe llamar a esta función si la instantánea se creó con la JET_bitContinueAfterThaw predeterminada. De lo contrario, la sesión de instantánea habría finalizado después de la [llamada a JetOSSnapshotThaw.](./jetossnapshotthaw-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de instalación](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)

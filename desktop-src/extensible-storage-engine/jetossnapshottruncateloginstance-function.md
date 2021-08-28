---
description: 'Más información sobre: JetOSSnapshotTruncateLogInstance (Función)'
title: JetOSSnapshotTruncateLogInstance (Función)
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0986633a450052431dfcef1426488dddc0417d33
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988448"
---
# <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance (Función)

La **función JetOSSnapshotTruncateLogInstance** trunca el registro de una instancia especificada durante una sesión de instantánea.

**Windows Vista:****JetOSSnapshotTruncateLogInstance** se introdujo en Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*Ejemplo*

Instancia de que se usará para esta llamada.

*grbit*

Opciones de esta llamada. Este parámetro puede tener una combinación de los siguientes valores.

*grbit* puede ser uno de los siguientes valores:


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
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>La sesión de instantánea no está en el estado en el que se puede producir un truncamiento. Las posibles causas son:</p><ul><li><p>La llamada se completa después de que se haya completado el tiempo de espera de la sesión de instantánea.</p></li><li><p>La sesión se especificó como una instantánea de copia.</p></li></ul> | 



Si esta función se realiza correctamente, los archivos de registro de una o todas las instancias que forman parte de la sesión de instantáneas se truncarán, si es posible.

#### <a name="remarks"></a>Observaciones

Solo se debe llamar a esta función si la instantánea se creó con la JET_bitContinueAfterThaw predeterminada. De lo contrario, la sesión de instantánea finaliza después de la llamada [a JetOSSnapshotThaw](./jetossnapshotthaw-function.md).

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

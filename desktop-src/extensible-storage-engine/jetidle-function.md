---
description: 'Más información sobre: JetIdle (Función)'
title: JetIdle (Función)
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73a1fa613bd5dda8d64572b376b0e1fa792e56fb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471371"
---
# <a name="jetidle-function"></a>JetIdle (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetidle-function"></a>JetIdle (Función)

La **función JetIdle** está en desuso y solo se debe usar con fines de prueba. **JetIdle se puede** usar para realizar tareas de limpieza inactivas o comprobar el estado del almacén de versiones en ESE.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se usará para esta llamada.

*grbit*

Un grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de los bits siguientes:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIdleCompact</p> | <p>Desencadena la limpieza del almacén de versiones.</p> | 
| <p>JET_bitIdleFlushBuffers</p> | <p>Reservado para uso futuro. Si se especifica esta marca, la API devolverá JET_errInvalidgrbit.</p> | 
| <p>JET_bitIdleStatus</p> | <p>Devuelve JET_wrnIdleFull si el almacén de versiones está más de la mitad lleno.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un <em>parámetro grbit</em> que se proporcionó a la API no era válido.</p> | 



Si esta función se realiza correctamente, se desencadenará la operación adecuada o se mostrará un código de error que indica la cantidad de almacenamiento de versiones en función del *grbit* proporcionado.

Si se produce un error en esta función, la operación solicitada no se habrá completado correctamente.

#### <a name="remarks"></a>Comentarios

El almacén de versiones mantiene el mecanismo de aislamiento de instantáneas de ESE. Si el almacén de versiones está más de la mitad lleno, el programa podría cerrar transacciones de ejecución larga. Si una transacción de ejecución larga agota el almacén de versiones, ESE dejará de permitir operaciones de escritura en la base de datos.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)

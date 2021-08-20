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
ms.openlocfilehash: 2bf8d45144c990da16cd91899c70c05f8689dc799ee556b6e2e46762f01c3361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117891131"
---
# <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog (Función)

La **función JetOSSnapshotTruncateLog** habilita el truncamiento del registro para todas las instancias que forman parte de la sesión de instantáneas.

**Windows Vista:****JetOSSnapshotTruncateLog** se presenta en Windows Vista.  

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

Opciones para esta llamada. Este parámetro puede tener una combinación de los valores siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitAllDatabasesSnapshot</p></td>
<td><p>Todas las bases de datos están conectadas para que el motor de almacenamiento pueda calcular y realizar el truncamiento del registro.</p></td>
</tr>
<tr class="even">
<td><p>0 (cero)</p></td>
<td><p>No se producirá ningún truncamiento.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>El <em>parámetro grbit</em> no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>La sesión de instantánea no está en el estado en el que se puede producir un truncamiento. Las posibles causas son:</p>
<ul>
<li><p>La llamada se realiza después de que se haya transcurrido el tiempo de espera de la sesión de instantáneas.</p></li>
<li><p>la sesión se especificó como una instantánea de copia</p></li>
</ul></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, los archivos de registro de una o todas las instancias de la sesión de instantánea se truncarán, si es posible.

#### <a name="remarks"></a>Comentarios

Solo se debe llamar a esta función si la instantánea se creó con la JET_bitContinueAfterThaw predeterminada. De lo contrario, la sesión de instantáneas habría finalizado después [de la llamada a JetOSSnapshotThaw.](./jetossnapshotthaw-function.md)

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de ejecución](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)

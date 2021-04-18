---
description: 'Más información acerca de: JetStopService (función)'
title: Función JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715295"
---
# <a name="jetstopservice-function"></a>Función JetStopService


_**Se aplica a:** Windows | Windows Server_

## <a name="jetstopservice-function"></a>Función JetStopService

La función **JetStopService** prepara una instancia para la terminación.

**JetStopService** es la llamada heredada cuando solo se permite una instancia. En este caso, la única instancia activa es aquella en la que se está preparando la terminación.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No está claro qué instancia se debe preparar para la finalización cuando se usa <strong>JetStopService</strong> con el modo de varias instancias.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, se prepara para una finalización futura. Entre los pasos necesarios para preparar una terminación se incluyen los siguientes:

  - Detenga la desfragmentación con conexión si se está ejecutando.

  - Iniciar una limpieza del almacén de versiones.

  - Reduzca la profundidad del punto de control iniciando el vaciado de las páginas desfasadas en el administrador de búfer.

  - Evite las llamadas futuras a la mayoría de las funciones para esa instancia.

Si se produce un error en esta función, no se realizará ninguno de los pasos para preparar la finalización de una instancia, por lo que no se producirá ningún cambio en el estado de la instancia.

#### <a name="remarks"></a>Observaciones

Esta función reduce el trabajo que tendrá que hacer la instancia cuando termine, pero no finalizará la instancia. Como resultado, esta función es simplemente una optimización y no es obligatoria para su uso. Tenga en cuenta que la cantidad de trabajo realizado en preparación fue inferior en Windows 2000 y Windows XP. Una vez que la función se ejecuta correctamente, las funciones de llamada que ya no se permiten devolverán JET_errClientRequestToStopJetService. Las funciones que todavía se permiten después de esta llamada son: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) y [JetResetSessionContext](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)

---
description: 'Más información acerca de: JetGetThreadStats (función)'
title: JetGetThreadStats función)
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705451"
---
# <a name="jetgetthreadstats-function"></a>JetGetThreadStats función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetthreadstats-function"></a>JetGetThreadStats función)

La función **JetGetThreadStats** recupera información de rendimiento del motor de base de datos para el subproceso actual. Se pueden usar varias llamadas para recopilar estadísticas que reflejen la actividad del motor de base de datos en este subproceso entre esas llamadas.

**Windows Vista:**  **JetGetThreadStats** se presentó en Windows Vista.

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parámetros

*pvResult*

Búfer de salida que recibe los datos de las estadísticas del subproceso. El búfer contiene una estructura de [JET_THREADSTATS](./jet-threadstats-structure.md) después de una llamada correcta.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>No se pudo realizar la operación porque el búfer de salida proporcionado era demasiado pequeño para contener los datos solicitados. La función <strong>JetGetThreadStats</strong> devolverá este error cuando el búfer de salida sea demasiado pequeño para contener la versión más pequeña de la estructura <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> compatible con el motor de base de datos.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el búfer de salida contendrá una estructura [JET_THREADSTATS](./jet-threadstats-structure.md) que contiene las estadísticas del motor de base de datos para el subproceso actual.

En caso de error, el estado del búfer de salida es indefinido.

#### <a name="remarks"></a>Observaciones

La información proporcionada por dos llamadas consecutivas de esta API está pensada para calcular el gasto de cualquier otra operación del motor de base de datos en el subproceso actual. Por lo general, esto se realiza tomando antes y después de leer las estadísticas y restar el recuento después del recuento anterior para obtener el número neto de operaciones realizadas.

Por ejemplo, una aplicación podría llamar a **JetGetThreadStats** una vez para obtener una lectura inicial de las estadísticas para el subproceso actual. Después, podría llamar a la función [JetMove](./jetmove-function.md) con el parámetro *cRow* establecido en JET_MoveNext para moverse a la entrada de índice siguiente en un índice. A continuación, podría llamar a **JetGetThreadStats** de nuevo para obtener otra lectura de las estadísticas del subproceso. A continuación, podría restar el contador cPageReferenced de la segunda lectura del primer. El resultado sería el número de páginas de base de datos a las que hace referencia el motor de base de datos para realizar la operación [JetMove](./jetmove-function.md) .

Las estadísticas de cada subproceso se acumulan durante la vigencia de ese subproceso. Las estadísticas se restablecen si el archivo DLL del motor de base de datos se descarga del proceso de host.

La estructura de [JET_THREADSTATS](./jet-threadstats-structure.md) probablemente se expandirá en el futuro para contener más estadísticas. Las nuevas estadísticas se agregarán al final de la estructura y se pueden recuperar con un mayor tamaño del búfer de salida. La presencia de estadísticas adicionales se puede inferir con un valor de cbStruct mayor.

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
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
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
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)

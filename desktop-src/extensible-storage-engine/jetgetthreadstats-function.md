---
description: 'Más información sobre: JetGetThreadStats (Función)'
title: JetGetThreadStats (Función)
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
ms.openlocfilehash: 87f3bed1dcd9fd43a67c96cbcb53d2496a976afa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474091"
---
# <a name="jetgetthreadstats-function"></a>JetGetThreadStats (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetthreadstats-function"></a>JetGetThreadStats (Función)

La **función JetGetThreadStats** recupera información de rendimiento del motor de base de datos para el subproceso actual. Se pueden usar varias llamadas para recopilar estadísticas que reflejen la actividad del motor de base de datos en este subproceso entre esas llamadas.

**Windows Vista:****JetGetThreadStats** se introdujo en Windows Vista.  

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parámetros

*pvResult*

Búfer de salida que recibe los datos de estadísticas del subproceso. El búfer contiene una [estructura JET_THREADSTATS](./jet-threadstats-structure.md) después de una llamada correcta.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Error en la operación porque el búfer de salida proporcionado era demasiado pequeño para contener los datos solicitados. La <strong>función JetGetThreadStats</strong> devolverá este error cuando el búfer de salida sea demasiado pequeño para contener la versión más pequeña de la estructura <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> compatible con el motor de base de datos.</p> | 



Si se ejecuta correctamente, el búfer de salida contendrá [una JET_THREADSTATS](./jet-threadstats-structure.md) que contiene estadísticas del motor de base de datos para el subproceso actual.

En caso de error, el estado del búfer de salida es indefinido.

#### <a name="remarks"></a>Comentarios

La información proporcionada por dos llamadas consecutivas de esta API está pensada para usarse para calcular el gasto de cualquier otra operación del motor de base de datos en el subproceso actual. Por lo general, esto se hace tomando un antes y después de leer las estadísticas y restando el recuento posterior del recuento anterior para obtener el recuento neto de operaciones realizadas.

Por ejemplo, una aplicación podría llamar a **JetGetThreadStats** una vez para obtener una lectura inicial de las estadísticas del subproceso actual. A continuación, podría llamar a la función [JetMove](./jetmove-function.md) con el parámetro *cRow* establecido en JET_MoveNext pasar a la siguiente entrada de índice en un índice. A continuación, podría llamar **a JetGetThreadStats** de nuevo para obtener otra lectura de las estadísticas del subproceso. A continuación, podría restar el contador cPageReferenced de la segunda lectura de la primera. El resultado sería el número de páginas de base de datos a las que hace referencia el motor de base de datos para realizar la [operación JetMove.](./jetmove-function.md)

Las estadísticas de cada subproceso se acumulan durante la vigencia de ese subproceso. Las estadísticas se restablecen si el archivo DLL del motor de base de datos se descarga del proceso de host.

La [JET_THREADSTATS](./jet-threadstats-structure.md) estructura se expandirá probablemente en el futuro para contener más estadísticas. Se agregarán nuevas estadísticas al final de la estructura y se pueden recuperar con un mayor tamaño de búfer de salida. La presencia de estadísticas adicionales se puede deducir mediante un valor cbStruct mayor.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)

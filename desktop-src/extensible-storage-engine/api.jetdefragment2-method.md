---
description: 'Más información sobre: API. JetDefragment2 (método)'
title: Método API. JetDefragment2
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715048"
---
# <a name="apijetdefragment2-method"></a>Método API. JetDefragment2

Inicia y detiene las tareas de desfragmentación de bases de datos que mejora la organización de datos en una base de datos.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar para la llamada.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de datos que se va a desfragmentar.

<!-- end list -->

  - tableName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Parámetro sin usar. La desfragmentación se realiza para toda la base de datos descrita por el identificador de base de datos especificado.

<!-- end list -->

  - paso  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Al iniciar una tarea de desfragmentación con conexión, este parámetro establece el número máximo de pasos de desfragmentación. Al detener una tarea de desfragmentación con conexión, este parámetro se establece en el número de pasos realizados.

<!-- end list -->

  - segundos  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Al iniciar una tarea de desfragmentación con conexión, este parámetro establece el tiempo máximo para la desfragmentación. Al detener una tarea de desfragmentación en línea, este búfer de salida se establece en el período de tiempo utilizado para la desfragmentación.

<!-- end list -->

  - devolución de llamada  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)  
    
    Función de devolución de llamada que usa Defrag para notificar el progreso.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. DefragGrbit](./defraggrbit-enumeration.md)  
    
    Opciones de desfragmentación.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Código de advertencia.  

## <a name="remarks"></a>Observaciones

La devolución de llamada pasada a JetDefragment2 se puede ejecutar de forma asincrónica. El GC no sabe que el código no administrado tiene una referencia a la devolución de llamada, por lo que es importante asegurarse de que la devolución de llamada no se recopila.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

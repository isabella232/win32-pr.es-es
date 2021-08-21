---
description: Más información sobre el método Api.JetEnumerateColumns
title: Método Api.JetEnumerateColumns
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 713b02835aa063e888a2385df9bd8abdff9af1300a2e9885c06e995f2b814bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042713"
---
# <a name="apijetenumeratecolumns-method"></a>Método Api.JetEnumerateColumns

Recupera eficazmente un conjunto de columnas y sus valores del registro actual de un cursor o del búfer de copia de ese cursor. Las columnas y los valores recuperados se pueden restringir mediante una lista de id. de columna, números de itagSequence y otras características. Esta API de recuperación de columnas es única en que devuelve información en memoria asignada dinámicamente que se obtiene mediante una devolución de llamada compatible con el reasignación proporcionada por el usuario. Esta nueva flexibilidad permite la recuperación eficaz de datos de columna con características específicas (como el tamaño y la multiplicidad) que el autor de la llamada desconoce. Esto elimina la necesidad de usar los modos de detección de JetRetrieveColumn para determinar esas características con el fin de configurar una llamada final a JetRetrieveColumn que recupere correctamente los datos deseados.

Esta API no es conforme a CLS. 

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor del que se recuperarán los datos.

<!-- end list -->

  - numColumnids  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Números de JET_ENUMCOLUMNIDS.

<!-- end list -->

  - columnids  
    Tipo: \[\]  
    
    Matriz opcional de id. de columna, cada uno con una matriz opcional de números de itagSequence que se va a enumerar.

<!-- end list -->

  - numColumnValues  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Devuelve el número de valores de columna recuperados.

<!-- end list -->

  - columnValues  
    Tipo: \[\]  
    
    Devuelve los valores de columna enumerados.

<!-- end list -->

  - allocator  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    Devolución de llamada usada para asignar memoria.

<!-- end list -->

  - allocatorContext  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Contexto para la devolución de llamada de asignación.

<!-- end list -->

  - maxDataSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Establece un límite en la cantidad de datos que se devolverán de una columna de texto largo o binario largo. Este parámetro se puede usar para evitar la enumeración de un valor de columna extremadamente grande.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)  
    
    Recuperar opciones.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Una advertencia o un éxito.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

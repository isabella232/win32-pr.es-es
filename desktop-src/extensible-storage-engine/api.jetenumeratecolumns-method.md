---
description: 'Más información sobre: API. JetEnumerateColumns (método)'
title: Método API. JetEnumerateColumns
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
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082052"
---
# <a name="apijetenumeratecolumns-method"></a>Método API. JetEnumerateColumns

Recupera eficazmente un conjunto de columnas y sus valores del registro actual de un cursor o del búfer de copia de ese cursor. Las columnas y los valores recuperados se pueden restringir por una lista de identificadores de columna, números de itagSequence y otras características. Esta API de recuperación de columnas es única, ya que devuelve información en memoria asignada dinámicamente que se obtiene mediante una devolución de llamada compatible con realloc proporcionada por el usuario. Esta nueva flexibilidad permite la recuperación eficaz de datos de columna con características específicas (como el tamaño y la multiplicidad) que son desconocidas para el autor de la llamada. Esto elimina la necesidad de usar los modos de detección de JetRetrieveColumn para determinar esas características a fin de configurar una llamada final a JetRetrieveColumn que recupere correctamente los datos deseados.

Esta API no es conforme a CLS. 

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor del que se van a recuperar datos.

<!-- end list -->

  - numColumnids  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número de JET_ENUMCOLUMNIDS.

<!-- end list -->

  - columnids  
    Automáticamente \[\]  
    
    Una matriz opcional de identificadores de columna, cada uno con una matriz opcional de números itagSequence para enumerar.

<!-- end list -->

  - numColumnValues  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Devuelve el número de valores de columna recuperados.

<!-- end list -->

  - columnValues  
    Automáticamente \[\]  
    
    Devuelve los valores de columna enumerados.

<!-- end list -->

  - allocator  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    Devolución de llamada usada para asignar memoria.

<!-- end list -->

  - allocatorContext  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contexto para la devolución de llamada de asignación.

<!-- end list -->

  - maxDataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Establece un límite en la cantidad de datos que se van a devolver de una columna de texto largo o binario largo. Este parámetro se puede utilizar para evitar la enumeración de un valor de columna extremadamente grande.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)  
    
    Opciones de recuperación.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
ADVERTENCIA o éxito.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

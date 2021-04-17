---
description: 'Más información sobre: API. JetOpenTempTable (método)'
title: Método API. JetOpenTempTable
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa41ce62b8bc2d7f2429acb5de809ad0be44a609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697725"
---
# <a name="apijetopentemptable-method"></a>Método API. JetOpenTempTable

Crea una tabla temporal con un índice único. Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex. Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil. También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial. Vea también [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md). [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - columnas  
    Automáticamente \[\]  
    
    Definiciones de columna para las columnas creadas en la tabla temporal.

<!-- end list -->

  - numColumns  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número de definiciones de columna.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)  
    
    Opciones de creación de tablas.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Devuelve el ID. de la tabla temporal. Al cerrar este TABLEID con [JetCloseTable (JET_SESID, JET_TABLEID),](./api.jetclosetable-method.md) se liberan los recursos asociados a la tabla temporal.

<!-- end list -->

  - columnids  
    Automáticamente \[\]  
    
    Búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal. Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: Método Api.JetEscrowUpdate'
title: Método Api.JetEscrowUpdate
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec5ddbedb921b89ef1b3c6e5bc48284da72407e8374bd6f0bb2de51c39c087e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042673"
---
# <a name="apijetescrowupdate-method"></a>Método Api.JetEscrowUpdate

Realiza una operación de suma atómica en una columna. Esta función permite que varias sesiones actualicen el mismo registro simultáneamente sin conflictos. Vea también [EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32).](./api.escrowupdate-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará. La sesión debe estar en una transacción.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se actualizará.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columna que se actualizará. Debe ser una columna que se pueda custodiar.

<!-- end list -->

  - delta  
    Tipo: \[\]  
    
    Búfer que contiene el complemento.

<!-- end list -->

  - deltaSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño del complemento.

<!-- end list -->

  - previousValue  
    Tipo: \[\]  
    
    Búfer de salida que recibirá el valor actual de la columna. Este búfer puede ser NULL.

<!-- end list -->

  - previousValueLength  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño del búfer previousValue.

<!-- end list -->

  - actualPreviousValueLength  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Devuelve el tamaño real de previousValue.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)  
    
    Opciones de actualización de custodia.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

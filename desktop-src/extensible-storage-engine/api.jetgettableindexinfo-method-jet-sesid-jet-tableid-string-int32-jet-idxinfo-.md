---
description: 'Más información sobre: método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)'
title: Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100742
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc9c3432e34f36d13b2a12880118f2b5c36a8ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001372"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-int32-jet_idxinfo"></a>Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)

Recupera información acerca de los índices de una tabla.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As Integer, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As Integer
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out int result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabla de la que se va a recuperar información de índice.

<!-- end list -->

  - IndexName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    El nombre del índice.

<!-- end list -->

  - resultado  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Se rellena con información acerca de los índices de la tabla.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)  
    
    Tipo de información que se va a recuperar.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga JetGetTableIndexInfo](./api.jetgettableindexinfo-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

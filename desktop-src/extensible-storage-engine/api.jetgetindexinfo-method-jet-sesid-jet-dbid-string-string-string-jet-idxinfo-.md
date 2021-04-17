---
description: 'Más información sobre: método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, cadena, JET_IdxInfo)'
title: Método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, cadena, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100769
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eed2ba4a3f578dda966b2b4530f26de25089681e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696310"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-string-jet_idxinfo"></a>Método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, cadena, JET_IdxInfo)

Recupera información acerca de los índices de una tabla.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de datos que se va a usar.

<!-- end list -->

  - tablename  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nombre de la tabla sobre la que se va a recuperar información de índice.

<!-- end list -->

  - IndexName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nombre del índice del que se va a recuperar información.

<!-- end list -->

  - resultado  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Se rellena con información acerca de los índices de la tabla.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)  
    
    Tipo de información que se va a recuperar.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga JetGetIndexInfo](./api.jetgetindexinfo-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

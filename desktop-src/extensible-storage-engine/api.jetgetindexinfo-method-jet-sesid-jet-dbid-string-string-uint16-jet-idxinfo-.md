---
description: 'Más información sobre: Método Api.JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)'
title: Método Api.JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100771
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd6b8833a235049b0079dfd0d436b859f836cb7f5f98d9d21afc131437b642e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085312"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-uint16-jet_idxinfo"></a>Método Api.JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)

Recupera información sobre los índices de una tabla.

Esta API no es conforme a CLS. 

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de datos que se usará.

<!-- end list -->

  - tablename  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre de la tabla sobre la que se recuperará la información de índice.

<!-- end list -->

  - indexname  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre del índice sobre el que se recuperará información.

<!-- end list -->

  - resultado  
    Tipo: [System.UInt16](/dotnet/api/system.uint16)  
    
    Rellenado con información sobre los índices de la tabla.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)  
    
    Tipo de información que se recuperará.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetGetIndexInfo](./api.jetgetindexinfo-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: API. JetCreateTable (método)'
title: Método API. JetCreateTable
TOCTitle: 'JetCreateTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetable(v=EXCHG.10)
ms:contentKeyID: 55100676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8025e35746d921fda3b601d289a9b361aefefb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497158"
---
# <a name="apijetcreatetable-method"></a>Método API. JetCreateTable

Cree una tabla vacía. La tabla recién creada se abre exclusivamente.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetCreateTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String, _
    pages As Integer, _
    density As Integer, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As String
Dim pages As Integer
Dim density As Integer
Dim tableid As JET_TABLEIDApi.JetCreateTable(sesid, dbid, _
    table, pages, density, tableid)
```

``` csharp
public static void JetCreateTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table,
    int pages,
    int density,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de datos en la que se va a crear la tabla.

<!-- end list -->

  - table  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    El objeto de la tabla que se va a crear.

<!-- end list -->

  - páginas  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número inicial de páginas de la tabla.

<!-- end list -->

  - densidad  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Densidad predeterminada de la tabla. Se usa al realizar inserciones secuenciales.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Devuelve el ID. de la nueva tabla.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

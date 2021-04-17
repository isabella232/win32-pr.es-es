---
description: 'Más información sobre: Constructor de tablas'
title: Constructor de tablas
TOCTitle: 'Table constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.table(v=EXCHG.10)
ms:contentKeyID: 55104142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8987e643253791e5315dd07b7b20a40dee66cf9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696588"
---
# <a name="table-constructor"></a>Constructor de tablas

Inicializa una nueva instancia de la clase Table. La tabla se abre desde la base de datos especificada.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    name As String, _
    grbit As OpenTableGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim name As String
Dim grbit As OpenTableGrbit

Dim instance As New Table(sesid, dbid, _
    name, grbit)
```

``` csharp
public Table(
    JET_SESID sesid,
    JET_DBID dbid,
    string name,
    OpenTableGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de datos en la que se va a abrir la tabla.

<!-- end list -->

  - name  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nombre de la tabla.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)  
    
    Opciones de JetOpenTable.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Table (clase)](./table-class.md)

[Miembros de tabla](./table-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

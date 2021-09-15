---
description: Más información sobre el método Api.JetCreateDatabase2
title: Método Api.JetCreateDatabase2
TOCTitle: 'JetCreateDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase2(v=EXCHG.10)
ms:contentKeyID: 55100671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8293a7c98451b0fd8bc46fbc13dde6b477a0ad09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567733"
---
# <a name="apijetcreatedatabase2-method"></a>Método Api.JetCreateDatabase2

Crea y adjunta un archivo de base de datos con un tamaño máximo de base de datos especificado.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetCreateDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase2(sesid, database, _
    maxPages, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - database  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Ruta de acceso al archivo de base de datos que se creará.

<!-- end list -->

  - maxPages  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño máximo, en páginas de base de datos, de la base de datos. Pasar 0 significa que no hay ningún máximo aplicado.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Devuelve el dbid de la nueva base de datos.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)  
    
    Opciones de creación de bases de datos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

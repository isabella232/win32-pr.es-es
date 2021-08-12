---
description: Más información sobre el método Api.JetGrowDatabase
title: Método Api.JetGrowDatabase
TOCTitle: 'JetGrowDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgrowdatabase(v=EXCHG.10)
ms:contentKeyID: 55100754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80652f60e7c7bf8afad3e3dd6bc36d1998dc64b989c307e130ec9d664a7949f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118271919"
---
# <a name="apijetgrowdatabase-method"></a>Método Api.JetGrowDatabase

Extiende el tamaño de una base de datos que está abierta actualmente.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGrowDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetGrowDatabase(sesid, dbid, _
    desiredPages, actualPages)
```

``` csharp
public static void JetGrowDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de datos que se debe aumentar.

<!-- end list -->

  - desiredPages  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño deseado de la base de datos, en páginas.

<!-- end list -->

  - actualPages  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño de la base de datos, en páginas, después de la llamada.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

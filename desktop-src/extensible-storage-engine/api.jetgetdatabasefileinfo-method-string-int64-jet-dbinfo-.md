---
description: 'Más información sobre: Método Api.JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)'
title: Método Api.JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int64@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100700
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba9426e53be08001940802a7bcc66e45fc71e8883252ce9d5a3b529e9a8c82c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983425"
---
# <a name="apijetgetdatabasefileinfo-method-string-int64-jet_dbinfo"></a>Método Api.JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)

Recupera cierta información sobre la base de datos especificada.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Long, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Long
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out long value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a>Parámetros

  - databaseName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre de archivo de la base de datos.

<!-- end list -->

  - value  
    Tipo: [System.Int64](/dotnet/api/system.int64)  
    
    Valor que se va a recuperar.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)  
    
    Datos específicos que se recuperarán.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetGetDatabaseFileInfo](./api.jetgetdatabasefileinfo-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

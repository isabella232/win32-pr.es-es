---
description: 'Más información sobre: Método Api.JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)'
title: Método Api.JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,Microsoft.Isam.Esent.Interop.JET_DBINFOMISC@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d72711314312c843d9e456a5194cb6133b4f491f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270071"
---
# <a name="apijetgetdatabasefileinfo-method-string-jet_dbinfomisc-jet_dbinfo"></a>Método Api.JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)

Recupera cierta información sobre la base de datos especificada.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef dbinfomisc As JET_DBINFOMISC, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim dbinfomisc As JET_DBINFOMISC
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    dbinfomisc, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out JET_DBINFOMISC dbinfomisc,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a>Parámetros

  - databaseName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre de archivo de la base de datos.

<!-- end list -->

  - dbinfomisc  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)  
    
    Valor que se va a recuperar.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)  
    
    Datos específicos que se recuperarán.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetGetDatabaseFileInfo](./api.jetgetdatabasefileinfo-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

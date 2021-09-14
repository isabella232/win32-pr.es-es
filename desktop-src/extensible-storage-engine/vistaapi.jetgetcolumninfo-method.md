---
description: Más información sobre el método VistaApi.JetGetColumnInfo
title: Método VistaApi.JetGetColumnInfo (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'JetGetColumnInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55104283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ae090fa5279b9ec60a3be88b4ebda393322b1f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126882609"
---
# <a name="vistaapijetgetcolumninfo-method"></a>Método VistaApi.JetGetColumnInfo

Recupera información sobre una columna de una tabla.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnid As JET_COLUMNID
Dim columnbase As JET_COLUMNBASEVistaApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnid, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    JET_COLUMNID columnid,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de datos que contiene la tabla.

<!-- end list -->

  - tablename  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre de la tabla que contiene la columna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Identificador de la columna.

<!-- end list -->

  - base de columna  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)  
    
    Rellenado con información sobre las columnas de la tabla.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[VistaApi (clase)](./vistaapi-class.md)

[Miembros de VistaApi](./vistaapi-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)

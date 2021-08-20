---
description: 'Más información sobre: Método Api.JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)'
title: Método Api.JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, String, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100745
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a742aaa8ee6bd8c296f0a6aa912a9a4ca8f4ed48cf560e77ce469a13a2712fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117615"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-string-jet_tblinfo"></a>Método Api.JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)

Recupera varios fragmentos de información sobre una tabla de una base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As String
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabla sobre la que se recuperará información.

<!-- end list -->

  - resultado  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Información recuperada.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)  
    
    Tipo de información que se recuperará.

## <a name="remarks"></a>Comentarios

Esta sobrecarga se usa con [Name](./jet-tblinfo-enumeration.md) y [TemplateTableName.](./jet-tblinfo-enumeration.md)

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de JetGetTableInfo](./api.jetgettableinfo-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: Más información sobre el método Api.GetColumnDictionary
title: Método Api.GetColumnDictionary
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab359c5b8b163ce67f576f35250dd521eb14472
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575193"
---
# <a name="apigetcolumndictionary-method"></a>Método Api.GetColumnDictionary

Crea un diccionario que asigna nombres de columna a sus id. de columna.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesid que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabla para la que se recuperará la información.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Collections.Generic.IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\>  
Diccionario que asigna nombres de columna a los id. de columna.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: Método Api.MakeKey (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)'
title: Método Api.MakeKey (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.Text.Encoding,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100830
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5f4fa9dfd848ff6aef858533501891e08ef8972
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361268"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-string-encoding-makekeygrbit"></a>Método Api.MakeKey (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)

Construye una clave de búsqueda que [jetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) y [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As String, _
    encoding As Encoding, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As String
Dim encoding As Encoding
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    encoding, grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string data,
    Encoding encoding,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor en el que se creará la clave.

<!-- end list -->

  - datos  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Datos de columna para la columna de clave actual del índice actual.

<!-- end list -->

  - encoding  
    Tipo: [System.Text.Encoding](/dotnet/api/system.text.encoding)  
    
    Codificación utilizada para convertir la cadena.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)  
    
    Opciones clave.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de MakeKey](./api.makekey-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

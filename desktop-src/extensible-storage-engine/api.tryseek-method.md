---
description: 'Más información sobre: API. TrySeek (método)'
title: Método API. TrySeek
TOCTitle: 'TrySeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryseek(v=EXCHG.10)
ms:contentKeyID: 55100941
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46472c59c14bd515e744a7ccfa908752783d27fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907777"
---
# <a name="apitryseek-method"></a>Método API. TrySeek

Coloca de forma eficaz un cursor en una entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada. Una clave de búsqueda se debe haber construido previamente mediante JetMakeKey.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function TrySeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As Boolean

returnValue = Api.TrySeek(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se va a colocar.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. SeekGrbit](./seekgrbit-enumeration.md)  
    
    Opción de búsqueda.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True si se encontró un registro que coincide con los criterios.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

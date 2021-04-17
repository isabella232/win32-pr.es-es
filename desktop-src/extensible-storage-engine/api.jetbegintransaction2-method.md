---
description: 'Más información sobre: API. JetBeginTransaction2 (método)'
title: Método API. JetBeginTransaction2
TOCTitle: 'JetBeginTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction2(v=EXCHG.10)
ms:contentKeyID: 55107226
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d41652c4688bd736ac5f5164ca9b487a24edf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539730"
---
# <a name="apijetbegintransaction2-method"></a>Método API. JetBeginTransaction2

Hace que una sesión escriba una transacción o cree un nuevo punto de retorno en una transacción existente.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetBeginTransaction2 ( _
    sesid As JET_SESID, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As BeginTransactionGrbitApi.JetBeginTransaction2(sesid, _
    grbit)
```

``` csharp
public static void JetBeginTransaction2(
    JET_SESID sesid,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión para la que se va a iniciar la transacción.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)  
    
    Opciones de transacción.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

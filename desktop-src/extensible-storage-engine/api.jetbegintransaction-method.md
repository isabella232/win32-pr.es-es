---
description: 'Más información sobre: Método Api.JetBeginTransaction'
title: Método Api.JetBeginTransaction
TOCTitle: 'JetBeginTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction(v=EXCHG.10)
ms:contentKeyID: 55107225
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b8812df332734ee109ea52820346e433e747751
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569872"
---
# <a name="apijetbegintransaction-method"></a>Método Api.JetBeginTransaction

Hace que una sesión escriba una transacción o cree un nuevo punto de guardado en una transacción existente.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetBeginTransaction ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetBeginTransaction(sesid)
```

``` csharp
public static void JetBeginTransaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión para la que se inicia la transacción.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: Conversión implícita de sesión (sesión a JET_SESID)'
title: Conversión implícita de sesión (sesión a JET_SESID)
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 512bc457a84ad1d1b170ac9d31cb04e36d8a05d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580060"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a>Conversión implícita de sesión (sesión a JET_SESID)

Operador de conversión implícita de una sesión a una JET_SESID. Esto permite usar una sesión con las API que esperan un JET_SESID.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a>Parámetros

  - hora de sesión  
    Tipo: [Microsoft.Isam.Esent.Interop.Session](./session-class.md)  
    
    Sesión que se convertirá.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
El JET_SESID de la sesión.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de sesión](./session-class.md)

[Miembros de sesión](./session-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

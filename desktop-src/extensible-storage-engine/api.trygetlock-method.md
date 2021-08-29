---
description: 'Más información sobre: Método Api.TryGetLock'
title: Método Api.TryGetLock
TOCTitle: 'TryGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trygetlock(v=EXCHG.10)
ms:contentKeyID: 55100934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6a8d4ac8b5b81b1238e7847846a1e95122bc53cf8912d591acb221d666d6e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738585"
---
# <a name="apitrygetlock-method"></a>Método Api.TryGetLock

Reservar explícitamente la capacidad de actualizar una fila, escribir bloqueo o impedir explícitamente que cualquier otra sesión actualice una fila, el bloqueo de lectura. Normalmente, los bloqueos de escritura de fila se adquieren implícitamente como resultado de la actualización de filas. Normalmente, los bloqueos de lectura no son necesarios debido al control de versiones de los registros. Sin embargo, en algunos casos, es posible que una transacción desee bloquear explícitamente una fila para aplicar la serialización o asegurarse de que una operación posterior se realizará correctamente.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function TryGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbit
Dim returnValue As Boolean

returnValue = Api.TryGetLock(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TryGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se usará. Se adquirirá un bloqueo en el registro actual.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)  
    
    Opciones de bloqueo, úsese esta opción para especificar qué tipo de bloqueo se va a obtener.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True si se obtuvo el bloqueo; de lo contrario, false. Se produce una excepción si se encuentra un error inesperado.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

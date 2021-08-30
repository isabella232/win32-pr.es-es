---
description: Más información sobre el método Api.JetSetLS
title: Método Api.JetSetLS
TOCTitle: 'JetSetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetls(v=EXCHG.10)
ms:contentKeyID: 55100808
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94c6b8dfe425576b7340f637a3f9942a25aeb28391adbdf3417b65afe0e0e84b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977585"
---
# <a name="apijetsetls-method"></a>Método Api.JetSetLS

Permite que la aplicación asocie un identificador de contexto conocido como Storage local con un cursor o la tabla asociada a ese cursor. La aplicación puede usar este identificador de contexto para almacenar datos auxiliares asociados a un cursor o tabla. Más adelante se notifica a la aplicación mediante una devolución de llamada en tiempo de ejecución cuando se debe liberar el identificador de contexto. Esto permite asociar el estado asignado dinámicamente a un cursor o tabla.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetSetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetSetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetSetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se usará.

<!-- end list -->

  - ls  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)  
    
    Identificador de contexto que se va a asociar a la sesión o al cursor.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)  
    
    Establecer opciones.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: JET_DBINFOMISC.dbstate'
title: JET_DBINFOMISC.dbstate, propiedad
TOCTitle: 'dbstate property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.dbstate(v=EXCHG.10)
ms:contentKeyID: 39513341
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.dbstate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_dbstate
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.dbstate
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fece25cfd46154168216d197c114fa2f688855d10556aeeb925d9ba970ad9c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980425"
---
# <a name="jet_dbinfomiscdbstate-property"></a>JET_DBINFOMISC.dbstate, propiedad

Obtiene el estado coherente o incoherente de la base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property dbstate As JET_dbstate
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_dbstate

value = instance.dbstate
```

``` csharp
public JET_dbstate dbstate { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.Isam.Esent.Interop.JET_dbstate](./jet-dbstate-enumeration.md)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_DBINFOMISC clase](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC miembros](./jet-dbinfomisc-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

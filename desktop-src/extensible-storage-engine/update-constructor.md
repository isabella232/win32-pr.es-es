---
description: 'Más información sobre: Constructor de actualización'
title: Constructor de actualización
TOCTitle: 'Update constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.update(v=EXCHG.10)
ms:contentKeyID: 55104189
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.Update
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 58c42652ec9a6e8ece773338b9ef669833061ad2e25f29a54ded3d1c5d5cb6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978255"
---
# <a name="update-constructor"></a>Constructor de actualización

Inicializa una nueva instancia de la clase Update. Esto inicia automáticamente una actualización. La actualización se cancelará si no se guarda explícitamente.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prep

Dim instance As New Update(sesid, tableid, _
    prep)
```

``` csharp
public Update(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión para la que se inicia la transacción.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tableid para el que se prepara la actualización.

<!-- end list -->

  - Preparación  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)  
    
    Tipo de actualización.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Actualizar clase](./update-class.md)

[Actualizar miembros](./update-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

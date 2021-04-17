---
description: 'Más información acerca de: constructor de actualizaciones'
title: Actualizar constructor
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
ms.openlocfilehash: 841403523e0cae7c71fb8fa0861c1d400a26a726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652969"
---
# <a name="update-constructor"></a>Actualizar constructor

Inicializa una nueva instancia de la clase Update. Esto inicia automáticamente una actualización. La actualización se cancelará si no se guarda explícitamente.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión para la que se va a iniciar la transacción.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    TABLEID para el que se va a preparar la actualización.

<!-- end list -->

  - porcentaje  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_prep](./jet-prep-enumeration.md)  
    
    Tipo de actualización.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Update (clase)](./update-class.md)

[Actualizar miembros](./update-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

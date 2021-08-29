---
description: 'Más información sobre: JET_RETRIEVECOLUMN.pvData'
title: JET_RETRIEVECOLUMN.pvData, propiedad
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_pvData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a791bfa6fa44b4a24387c42bac66bdf453c130ec68039119620c2a782731b39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890405"
---
# <a name="jet_retrievecolumnpvdata-property"></a>JET_RETRIEVECOLUMN.pvData, propiedad

Obtiene o establece el búfer que almacenará los datos que se recuperan de la columna.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvData As Byte()
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Byte()

value = instance.pvData

instance.pvData = value
```

``` csharp
public byte[] pvData { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: \[\]  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_RETRIEVECOLUMN clase](./jet-retrievecolumn-class.md)

[JET_RETRIEVECOLUMN miembros](./jet-retrievecolumn-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

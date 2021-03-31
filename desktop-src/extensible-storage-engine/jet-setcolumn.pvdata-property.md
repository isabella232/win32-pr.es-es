---
description: 'Más información acerca de: propiedad JET_SETCOLUMN. pvData'
title: Propiedad JET_SETCOLUMN. pvData
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103932
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_pvData
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47170dd68749b13f0c6a3bc818f0a2fb775e77b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809020"
---
# <a name="jet_setcolumnpvdata-property"></a>Propiedad JET_SETCOLUMN. pvData

Obtiene o establece un puntero a los datos que se van a establecer.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property pvData As Byte()
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Byte()

value = instance.pvData

instance.pvData = value
```

``` csharp
public byte[] pvData { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Automáticamente \[\]  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_SETCOLUMN (clase)](./jet-setcolumn-class.md)

[Miembros de JET_SETCOLUMN](./jet-setcolumn-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

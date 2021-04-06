---
description: 'Más información acerca de: JET_SETCOLUMN. err (propiedad)'
title: JET_SETCOLUMN. err (propiedad)
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.err(v=EXCHG.10)
ms:contentKeyID: 55107684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_err
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_err
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afb84b4b8cbeda5f5686e953dd6e7b51e9bacbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001011"
---
# <a name="jet_setcolumnerr-property"></a>JET_SETCOLUMN. err (propiedad)

Obtiene el código de error o la advertencia devuelta por la operación de conjunto de columnas.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_SETCOLUMN (clase)](./jet-setcolumn-class.md)

[Miembros de JET_SETCOLUMN](./jet-setcolumn-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

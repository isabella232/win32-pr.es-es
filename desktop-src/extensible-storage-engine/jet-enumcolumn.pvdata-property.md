---
description: 'Más información sobre: JET_ENUMCOLUMN.pvData'
title: JET_ENUMCOLUMN.pvData, propiedad
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df79d838277a849c99ea49af2a8ca12e77cb3667d4750b141f0b9247b46b9232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254698"
---
# <a name="jet_enumcolumnpvdata-property"></a>JET_ENUMCOLUMN.pvData, propiedad

Obtiene el valor enumerado para la columna. Este miembro solo se usa si [err](./jet-enumcolumn.err-property.md) es igual a [ColumnSingleValue.](./jet-wrn-enumeration.md) Esto apunta a la memoria asignada con la devolución de llamada del asignador de JET_PFNREALLOC pasada [a](./jet-pfnrealloc-delegate.md) [JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, , \[ \] JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit).](./api.jetenumeratecolumns-method.md) No olvide liberar la memoria cuando haya terminado.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.IntPtr](/dotnet/api/system.intptr)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMN clase](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN miembros](./jet-enumcolumn-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

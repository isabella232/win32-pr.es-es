---
description: Más información sobre el método ColumnValue.ToString
title: Método ColumnValue.ToString
TOCTitle: 'ToString method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnValue.ToString
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.tostring(v=EXCHG.10)
ms:contentKeyID: 55101194
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.ToString
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ad8618fb9fe3486ca15b0883002f40cd29a2193
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466326"
---
# <a name="columnvaluetostring-method"></a>Método ColumnValue.ToString

Devuelve un [objeto String](/dotnet/api/system.string) que representa el [valor columnValue actual.](./columnvalue-class.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public MustOverride Function ToString As String
'Usage
Dim instance As ColumnValue
Dim returnValue As String

returnValue = instance.ToString()
```

``` csharp
public abstract string ToString()
```

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.String](/dotnet/api/system.string)  
Cadena [que](/dotnet/api/system.string) representa el valor [ColumnValue actual.](./columnvalue-class.md)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[ColumnValue (clase)](./columnvalue-class.md)

[Miembros ColumnValue](./columnvalue-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

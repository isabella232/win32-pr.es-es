---
description: Más información sobre el método FloatColumnValue.GetValueFromBytes
title: Método FloatColumnValue.GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103242
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 329ab0fb3a6d26173623ae8bb3d78506c17b6d1e0b2b7f33f13893b3877d3e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968785"
---
# <a name="floatcolumnvaluegetvaluefrombytes-method"></a>Método FloatColumnValue.GetValueFromBytes

Dados los datos recuperados de ESENT, descodifique los datos y establezca el valor en el objeto ColumnValue.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Parámetros

  - value  
    Tipo: \[\]  
    
    Matriz de bytes.

<!-- end list -->

  - startIndex  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Posición inicial dentro de los bytes.

<!-- end list -->

  - recuento  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de bytes que se van a descodificar.

<!-- end list -->

  - err  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Error devuelto de ESENT.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase FloatColumnValue](./floatcolumnvalue-class.md)

[Miembros FloatColumnValue](./floatcolumnvalue-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: Más información sobre el método Int16ColumnValue.GetValueFromBytes
title: Método Int16ColumnValue.GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int16ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int16columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103359
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int16ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int16ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1464dd417607024f377c1c9af0cd3d56cfa5d9f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465416"
---
# <a name="int16columnvaluegetvaluefrombytes-method"></a>Método Int16ColumnValue.GetValueFromBytes

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

  - count  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número de bytes que se van a descodificar.

<!-- end list -->

  - err  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Error devuelto de ESENT.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Int16ColumnValue (clase)](./int16columnvalue-class.md)

[Miembros Int16ColumnValue](./int16columnvalue-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

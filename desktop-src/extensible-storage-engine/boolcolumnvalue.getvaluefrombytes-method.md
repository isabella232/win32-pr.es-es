---
description: Más información sobre el método BoolColumnValue.GetValueFromBytes
title: Método BoolColumnValue.GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.boolcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55100913
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44fddd0e9eee1ce593b5ac8cb7cb2ca0efcabb2d48e7e614f1ed2d100ad38c8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670075"
---
# <a name="boolcolumnvaluegetvaluefrombytes-method"></a>Método BoolColumnValue.GetValueFromBytes

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

[Clase BoolColumnValue](./boolcolumnvalue-class.md)

[Miembros BoolColumnValue](./boolcolumnvalue-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

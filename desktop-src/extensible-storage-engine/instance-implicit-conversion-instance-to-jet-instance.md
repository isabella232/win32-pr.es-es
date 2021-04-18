---
description: Más información acerca de la conversión implícita de instancias (instancia a JET_INSTANCE)
title: Conversión implícita de instancia (instancia a JET_INSTANCE)
TOCTitle: Implicit conversion (Instance to JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.op_Implicit(Microsoft.Isam.Esent.Interop.Instance)~Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55103290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
- Microsoft.Isam.Esent.Interop.Instance.op_Implicit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7dbac9f0b5736970cf51aef9e99f2877cfd488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720452"
---
# <a name="instance-implicit-conversion-instance-to-jet_instance"></a>Conversión implícita de instancia (instancia a JET_INSTANCE)

Proporcionar la conversión implícita de un objeto de instancia a una estructura de JET_INSTANCE. Esto se hace para que se pueda usar una instancia en cualquier lugar en el que se requiera JET_INSTANCE.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    instance As Instance _
) As JET_INSTANCE
'Usage
Dim input As Instance
Dim output As JET_INSTANCE

output = CType(input, JET_INSTANCE)
```

``` csharp
public static implicit operator JET_INSTANCE (
    Instance instance
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft. ISAM. esent. Interop. Instance](./instance-class.md)  
    
    La instancia de que se convertirá.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
JET_INSTANCE encapsulado por la instancia de.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de instancia](./instance-class.md)

[Miembros de instancia](./instance-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

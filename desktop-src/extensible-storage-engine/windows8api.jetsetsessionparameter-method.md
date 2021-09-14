---
description: Más información sobre el método Windows8Api.JetSetSessionParameter
title: Método Windows8Api.JetSetSessionParameter (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'JetSetSessionParameter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetsessionparameter(v=EXCHG.10)
ms:contentKeyID: 55104461
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b73331c765e1f8026b39c28dde5268417601663c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263564"
---
# <a name="windows8apijetsetsessionparameter-method"></a>Método Windows8Api.JetSetSessionParameter

Establece un parámetro en el estado de sesión proporcionado, que se usa durante la vigencia de esta sesión o hasta que se restablezca.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetSetSessionParameter ( _
    sesid As JET_SESID, _
    sesparamid As JET_sesparam, _
    data As Byte(), _
    dataSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim sesparamid As JET_sesparam
Dim data As Byte()
Dim dataSize As IntegerWindows8Api.JetSetSessionParameter(sesid, _
    sesparamid, data, dataSize)
```

``` csharp
public static void JetSetSessionParameter(
    JET_SESID sesid,
    JET_sesparam sesparamid,
    byte[] data,
    int dataSize
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión en la que se establece el parámetro.

<!-- end list -->

  - sesparamid  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)  
    
    Identificador del parámetro de sesión que se establecerá.

<!-- end list -->

  - datos  
    Tipo: \[\]  
    
    Datos que se establecerán en este parámetro de sesión.

<!-- end list -->

  - dataSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño de los datos proporcionados.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase Windows8Api](./windows8api-class.md)

[Miembros de Windows8Api](./windows8api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)

---
description: 'Más información sobre: JET_PFNREALLOC delegado'
title: JET_PFNREALLOC delegado
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965632"
---
# <a name="jet_pfnrealloc-delegate"></a>JET_PFNREALLOC delegado

Devolución de llamada usada por JetEnumerateColumns para asignar memoria para sus búferes de salida.

Esta API no es conforme a CLS. 

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a>Parámetros

  - context  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Contexto dado a JetEnumerateColumns.

<!-- end list -->

  - memoria  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Si es distinto de cero, puntero a un bloque de memoria asignado previamente por esta devolución de llamada.

<!-- end list -->

  - requestedSize  
    Tipo: [System.UInt32](/dotnet/api/system.uint32)  
    
    Nuevo tamaño del bloque de memoria (en bytes). Si es 0 y se especifica un bloque de memoria, se liberará ese bloque de memoria.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
Puntero a la memoria recién asignada. Si no se pudo asignar memoria, [se debe](/dotnet/api/system.intptr.zero) devolver Cero.  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

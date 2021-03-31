---
description: 'Más información sobre: clase EsentInvalidBufferSizeException'
title: Clase EsentInvalidBufferSizeException
TOCTitle: EsentInvalidBufferSizeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidbuffersizeexception(v=EXCHG.10)
ms:contentKeyID: 55101912
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0dc693135124ba5d2979fa0f1a7ff80fcca27600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910570"
---
# <a name="esentinvalidbuffersizeexception-class"></a>Clase EsentInvalidBufferSizeException

Clase base para JET_err. Excepciones InvalidBufferSize.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentInvalidBufferSizeException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidBufferSizeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentInvalidBufferSizeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidBufferSizeException : EsentStateException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentInvalidBufferSizeException](./esentinvalidbuffersizeexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

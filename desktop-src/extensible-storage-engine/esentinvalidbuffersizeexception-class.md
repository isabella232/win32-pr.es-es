---
description: 'Más información sobre: Clase EsentInvalidBufferSizeException'
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
ms.openlocfilehash: 6f3a8119eb774d86058d7fbf5f5ae6b96adecb9f2b3dc7214b6f41bef51dfb0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668743"
---
# <a name="esentinvalidbuffersizeexception-class"></a>Clase EsentInvalidBufferSizeException

Clase base para JET_err. Excepciones InvalidBufferSize.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

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

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: Clase EsentInvalidOperationException'
title: Clase EsentInvalidOperationException
TOCTitle: EsentInvalidOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102007
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02a4c7015c48171a69b1acb5fd8be2964a5f4ac9f661cd3d963541f000a97a4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020015"
---
# <a name="esentinvalidoperationexception-class"></a>Clase EsentInvalidOperationException

Clase base para JET_err. Excepciones invalidOperation.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentInvalidOperationException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidOperationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidOperationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidOperationException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentInvalidOperationException](./esentinvalidoperationexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

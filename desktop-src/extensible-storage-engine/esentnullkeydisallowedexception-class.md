---
description: 'Más información sobre: Clase EsentNullKeyDisallowedException'
title: Clase EsentNullKeyDisallowedException
TOCTitle: EsentNullKeyDisallowedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnullkeydisallowedexception(v=EXCHG.10)
ms:contentKeyID: 55102391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d66b9ec2193835e4b9a0f791a4f981fa18ff70399d6ba59cda2f7975a06e7d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119040153"
---
# <a name="esentnullkeydisallowedexception-class"></a>Clase EsentNullKeyDisallowedException

Clase base para JET_err. Excepciones NullKeyDisallowed.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNullKeyDisallowedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNullKeyDisallowedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNullKeyDisallowedException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentNullKeyDisallowedException](./esentnullkeydisallowedexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: clase EsentAlreadyPreparedException'
title: Clase EsentAlreadyPreparedException
TOCTitle: EsentAlreadyPreparedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAlreadyPreparedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentalreadypreparedexception(v=EXCHG.10)
ms:contentKeyID: 55101013
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAlreadyPreparedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAlreadyPreparedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 357220b36cbb25528cf99e524a6e0cf2eb4f97e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104081966"
---
# <a name="esentalreadypreparedexception-class"></a>Clase EsentAlreadyPreparedException

Clase base para JET_err. Excepciones AlreadyPrepared.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentAlreadyPreparedException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAlreadyPreparedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentAlreadyPreparedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAlreadyPreparedException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentAlreadyPreparedException](./esentalreadypreparedexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

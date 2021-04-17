---
description: 'Más información sobre: clase EsentPartiallyAttachedDBException'
title: Clase EsentPartiallyAttachedDBException
TOCTitle: EsentPartiallyAttachedDBException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpartiallyattacheddbexception(v=EXCHG.10)
ms:contentKeyID: 55107313
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96ff15d9a2becb937c88f6e0bec689e68ddc39d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677925"
---
# <a name="esentpartiallyattacheddbexception-class"></a>Clase EsentPartiallyAttachedDBException

Clase base para JET_err. Excepciones PartiallyAttachedDB.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentPartiallyAttachedDBException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPartiallyAttachedDBException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentPartiallyAttachedDBException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPartiallyAttachedDBException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentPartiallyAttachedDBException](./esentpartiallyattacheddbexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

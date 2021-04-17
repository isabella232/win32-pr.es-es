---
description: 'Más información sobre: clase EsentTooManyInstancesException'
title: Clase EsentTooManyInstancesException
TOCTitle: EsentTooManyInstancesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyinstancesexception(v=EXCHG.10)
ms:contentKeyID: 55103084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecd20f6a05a17d4bd21623732a4e716e82c9b1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716691"
---
# <a name="esenttoomanyinstancesexception-class"></a>Clase EsentTooManyInstancesException

Clase base para JET_err. Excepciones TooManyInstances.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentQuotaException](./esentquotaexception-class.md)  
              Microsoft. ISAM. esent. Interop. EsentTooManyInstancesException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyInstancesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyInstancesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyInstancesException : EsentQuotaException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentTooManyInstancesException](./esenttoomanyinstancesexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

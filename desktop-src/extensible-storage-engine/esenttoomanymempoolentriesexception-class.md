---
description: 'Más información sobre: clase EsentTooManyMempoolEntriesException'
title: Clase EsentTooManyMempoolEntriesException
TOCTitle: EsentTooManyMempoolEntriesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanymempoolentriesexception(v=EXCHG.10)
ms:contentKeyID: 55103097
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 454abe6d19fedb2f318696b80d166f181e19fb0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688398"
---
# <a name="esenttoomanymempoolentriesexception-class"></a>Clase EsentTooManyMempoolEntriesException

Clase base para JET_err. Excepciones TooManyMempoolEntries.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMemoryException](./esentmemoryexception-class.md)  
              Microsoft. ISAM. esent. Interop. EsentTooManyMempoolEntriesException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyMempoolEntriesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyMempoolEntriesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyMempoolEntriesException : EsentMemoryException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentTooManyMempoolEntriesException](./esenttoomanymempoolentriesexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

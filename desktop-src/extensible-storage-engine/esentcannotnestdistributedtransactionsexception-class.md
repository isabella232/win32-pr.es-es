---
description: 'Más información sobre: Clase EsentCannotNestDistributedTransactionsException'
title: Clase EsentCannotNestDistributedTransactionsException
TOCTitle: EsentCannotNestDistributedTransactionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotnestdistributedtransactionsexception(v=EXCHG.10)
ms:contentKeyID: 55101211
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 732b0995f75bb02174325489554aff2ece18a7f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241275"
---
# <a name="esentcannotnestdistributedtransactionsexception-class"></a>Clase EsentCannotNestDistributedTransactionsException

Clase base para JET_err. Excepciones de CannotNestDistributedTransactions.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotNestDistributedTransactionsException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentCannotNestDistributedTransactionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotNestDistributedTransactionsException : EsentObsoleteException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentCannotNestDistributedTransactionsException](./esentcannotnestdistributedtransactionsexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: Clase EsentNotInTransactionException'
title: Clase EsentNotInTransactionException
TOCTitle: EsentNotInTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotintransactionexception(v=EXCHG.10)
ms:contentKeyID: 55107294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1630ecc3cea33af09c0c81be69beb9a852609f32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569813"
---
# <a name="esentnotintransactionexception-class"></a>Clase EsentNotInTransactionException

Clase base para JET_err. Excepciones NotInTransaction.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentNotInTransactionException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInTransactionException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNotInTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInTransactionException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentNotInTransactionException](./esentnotintransactionexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

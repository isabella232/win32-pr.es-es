---
description: 'Más información sobre: Clase EsentTermInProgressException'
title: Clase EsentTermInProgressException
TOCTitle: EsentTermInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTermInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentterminprogressexception(v=EXCHG.10)
ms:contentKeyID: 55103042
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTermInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTermInProgressException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81a6675976e8ff92ad1338c888b7deebf02cd6af04b3905923ea18c95128a5cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834776"
---
# <a name="esentterminprogressexception-class"></a>Clase EsentTermInProgressException

Clase base para JET_err. Excepciones de TermInProgress.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentTermInProgressException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTermInProgressException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentTermInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTermInProgressException : EsentOperationException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentTermInProgressException](./esentterminprogressexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

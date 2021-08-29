---
description: 'Más información sobre: Clase EsentTooManyOpenDatabasesException'
title: Clase EsentTooManyOpenDatabasesException
TOCTitle: EsentTooManyOpenDatabasesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopendatabasesexception(v=EXCHG.10)
ms:contentKeyID: 55103102
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 038eedfc26e3174d639507c2b0bfa315e483ff8b9e7e6b485ba3d18bf592b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119113648"
---
# <a name="esenttoomanyopendatabasesexception-class"></a>Clase EsentTooManyOpenDatabasesException

Clase base para JET_err. Excepciones de TooManyOpenDatabases.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenDatabasesException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentTooManyOpenDatabasesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenDatabasesException : EsentObsoleteException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentTooManyOpenDatabasesException](./esenttoomanyopendatabasesexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

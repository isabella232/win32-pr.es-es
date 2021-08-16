---
description: 'Más información sobre: Clase EsentErrorException'
title: Clase EsentErrorException
TOCTitle: EsentErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101648
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f3890248063740f7c1078da54495ddffb97c93179ee929a629803d53b69b964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118779294"
---
# <a name="esenterrorexception-class"></a>Clase EsentErrorException

Clase base para excepciones de error de ESENT.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      Microsoft.Isam.Esent.Interop.EsentErrorException  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException](./esentcannotlogduringrecoveryredoexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentPreviousVersionException](./esentpreviousversionexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException](./esentversionstoreentrytoobigexception-class.md)  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public Class EsentErrorException _
    Inherits EsentException
'Usage
Dim instance As EsentErrorException
```

``` csharp
[SerializableAttribute]
public class EsentErrorException : EsentException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentErrorException](./esenterrorexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

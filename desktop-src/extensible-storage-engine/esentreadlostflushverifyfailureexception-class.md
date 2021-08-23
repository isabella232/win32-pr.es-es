---
description: 'Más información sobre: Clase EsentReadLostFlushVerifyFailureException'
title: Clase EsentReadLostFlushVerifyFailureException
TOCTitle: EsentReadLostFlushVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadlostflushverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102493
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92e2b4dd0f7d2e27041f801842cf73c353a3ce4f8eba2ce8d8ce7421d342421f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782135"
---
# <a name="esentreadlostflushverifyfailureexception-class"></a>Clase EsentReadLostFlushVerifyFailureException

Clase base para JET_err. Excepciones readLostFlushVerifyFailure.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadLostFlushVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadLostFlushVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadLostFlushVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentReadLostFlushVerifyFailureException](./esentreadlostflushverifyfailureexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

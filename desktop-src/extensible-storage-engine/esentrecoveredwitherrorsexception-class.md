---
description: 'Más información sobre: Clase EsentRecoveredWithErrorsException'
title: Clase EsentRecoveredWithErrorsException
TOCTitle: EsentRecoveredWithErrorsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveredwitherrorsexception(v=EXCHG.10)
ms:contentKeyID: 55102545
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd90328b3b592232e1f87f4fe568022443be8b77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566501"
---
# <a name="esentrecoveredwitherrorsexception-class"></a>Clase EsentRecoveredWithErrorsException

Clase base para JET_err. Excepciones RecoveredWithErrors.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveredWithErrorsException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecoveredWithErrorsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveredWithErrorsException : EsentStateException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentRecoveredWithErrorsException](./esentrecoveredwitherrorsexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

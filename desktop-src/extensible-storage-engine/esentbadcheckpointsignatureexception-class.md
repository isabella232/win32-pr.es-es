---
description: 'Más información sobre: clase EsentBadCheckpointSignatureException'
title: Clase EsentBadCheckpointSignatureException
TOCTitle: EsentBadCheckpointSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadcheckpointsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55101053
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96ddfa89c1fdf6a4b7727a00f736bbcc1c1c925e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678337"
---
# <a name="esentbadcheckpointsignatureexception-class"></a>Clase EsentBadCheckpointSignatureException

Clase base para JET_err. Excepciones BadCheckpointSignature.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentBadCheckpointSignatureException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadCheckpointSignatureException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentBadCheckpointSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadCheckpointSignatureException : EsentInconsistentException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentBadCheckpointSignatureException](./esentbadcheckpointsignatureexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

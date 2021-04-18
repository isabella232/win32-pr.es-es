---
description: 'Más información sobre: clase EsentLSAlreadySetException'
title: Clase EsentLSAlreadySetException
TOCTitle: EsentLSAlreadySetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlsalreadysetexception(v=EXCHG.10)
ms:contentKeyID: 55102175
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7757740a6c07d6fedaa8b17c7a84755ade4de59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716694"
---
# <a name="esentlsalreadysetexception-class"></a>Clase EsentLSAlreadySetException

Clase base para JET_err. Excepciones LSAlreadySet.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentLSAlreadySetException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLSAlreadySetException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentLSAlreadySetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLSAlreadySetException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentLSAlreadySetException](./esentlsalreadysetexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

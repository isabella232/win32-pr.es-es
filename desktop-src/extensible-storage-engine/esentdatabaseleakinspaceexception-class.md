---
description: 'Más información sobre: clase EsentDatabaseLeakInSpaceException'
title: Clase EsentDatabaseLeakInSpaceException
TOCTitle: EsentDatabaseLeakInSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseleakinspaceexception(v=EXCHG.10)
ms:contentKeyID: 55101407
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51c011fb1cf3c1dc7ebcade5d88dc2cbce66351b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542819"
---
# <a name="esentdatabaseleakinspaceexception-class"></a>Clase EsentDatabaseLeakInSpaceException

Clase base para JET_err. Excepciones DatabaseLeakInSpace.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDatabaseLeakInSpaceException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseLeakInSpaceException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseLeakInSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseLeakInSpaceException : EsentStateException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentDatabaseLeakInSpaceException](./esentdatabaseleakinspaceexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

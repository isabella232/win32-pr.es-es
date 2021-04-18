---
description: 'Más información sobre: clase EsentSessionInUseException'
title: Clase EsentSessionInUseException
TOCTitle: EsentSessionInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioninuseexception(v=EXCHG.10)
ms:contentKeyID: 55102709
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b956d88e1a8c59f23bedc25fadcacd234841572b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720550"
---
# <a name="esentsessioninuseexception-class"></a>Clase EsentSessionInUseException

Clase base para JET_err. Excepciones SessionInUse.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentSessionInUseException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionInUseException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentSessionInUseException](./esentsessioninuseexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: clase EsentDisabledFunctionalityException'
title: Clase EsentDisabledFunctionalityException
TOCTitle: EsentDisabledFunctionalityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdisabledfunctionalityexception(v=EXCHG.10)
ms:contentKeyID: 55101615
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ec4458b1306f11240f2090403dcc6ae4c7db07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002993"
---
# <a name="esentdisabledfunctionalityexception-class"></a>Clase EsentDisabledFunctionalityException

Clase base para JET_err. Excepciones DisabledFunctionality.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDisabledFunctionalityException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDisabledFunctionalityException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDisabledFunctionalityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDisabledFunctionalityException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentDisabledFunctionalityException](./esentdisabledfunctionalityexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

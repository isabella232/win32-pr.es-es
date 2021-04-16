---
description: 'Más información sobre: clase EsentDDLNotInheritableException'
title: Clase EsentDDLNotInheritableException
TOCTitle: EsentDDLNotInheritableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentddlnotinheritableexception(v=EXCHG.10)
ms:contentKeyID: 55101474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c2a1d4b715bab34d33c12678dcd6808e119921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706014"
---
# <a name="esentddlnotinheritableexception-class"></a>Clase EsentDDLNotInheritableException

Clase base para JET_err. Excepciones DDLNotInheritable.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDDLNotInheritableException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDDLNotInheritableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDDLNotInheritableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDDLNotInheritableException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentDDLNotInheritableException](./esentddlnotinheritableexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

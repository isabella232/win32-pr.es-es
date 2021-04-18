---
description: 'Más información sobre: clase EsentObjectDuplicateException'
title: Clase EsentObjectDuplicateException
TOCTitle: EsentObjectDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobjectduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 25af4c5ca5654ed769a61afa19ad3afe8732ac54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707061"
---
# <a name="esentobjectduplicateexception-class"></a>Clase EsentObjectDuplicateException

Clase base para JET_err. Excepciones ObjectDuplicate.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentObjectDuplicateException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentObjectDuplicateException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentObjectDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentObjectDuplicateException : EsentObsoleteException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentObjectDuplicateException](./esentobjectduplicateexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

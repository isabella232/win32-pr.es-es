---
description: 'Más información sobre: clase EsentResourceException'
title: Clase EsentResourceException
TOCTitle: EsentResourceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResourceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102627
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResourceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7d4964bb4ed9c1305652d9425170bd934c9274e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277462"
---
# <a name="esentresourceexception-class"></a>Clase EsentResourceException

Clase base para las excepciones de recursos.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentResourceException  
            [Microsoft. ISAM. esent. Interop. EsentDiskException](./esentdiskexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMemoryException](./esentmemoryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentQuotaException](./esentquotaexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTaskDroppedException](./esenttaskdroppedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyIOException](./esenttoomanyioexception-class.md)  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentResourceException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentResourceException
```

``` csharp
[SerializableAttribute]
public abstract class EsentResourceException : EsentOperationException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentResourceException](./esentresourceexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

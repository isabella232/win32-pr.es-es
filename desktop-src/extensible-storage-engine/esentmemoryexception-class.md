---
description: 'Más información sobre: Clase EsentMemoryException'
title: Clase EsentMemoryException
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063597"
---
# <a name="esentmemoryexception-class"></a>Clase EsentMemoryException

Clase base para excepciones memory.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMemoryException  
              

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentMemoryException](./esentmemoryexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMemoryException  
              [Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException](./esentoutofbuffersexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException](./esentoutofcursorsexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException](./esentoutoffilehandlesexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException](./esentoutofmemoryexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException](./esentoutofsessionsexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException](./esentoutofthreadsexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException](./esenttoomanymempoolentriesexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException](./esenttoomanyopenindexesexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentTooManySortsException](./esenttoomanysortsexception-class.md)
---
description: 'Más información sobre: clase EsentQuotaException'
title: Clase EsentQuotaException
TOCTitle: EsentQuotaException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQuotaException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102495
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53b108a4d55553788a6c2d316f93f4f8efc76035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707059"
---
# <a name="esentquotaexception-class"></a>Clase EsentQuotaException

Clase base para las excepciones de cuota.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentQuotaException  
              [Microsoft. ISAM. esent. Interop. EsentOutOfDatabaseSpaceException](./esentoutofdatabasespaceexception-class.md)  
              [Microsoft. ISAM. esent. Interop. EsentTooManyInstancesException](./esenttoomanyinstancesexception-class.md)  
              [Microsoft. ISAM. esent. Interop. EsentTooManyOpenTablesException](./esenttoomanyopentablesexception-class.md)  
              [Microsoft. ISAM. esent. Interop. EsentVersionStoreOutOfMemoryException](./esentversionstoreoutofmemoryexception-class.md)  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentQuotaException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentQuotaException
```

``` csharp
[SerializableAttribute]
public abstract class EsentQuotaException : EsentResourceException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentQuotaException](./esentquotaexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

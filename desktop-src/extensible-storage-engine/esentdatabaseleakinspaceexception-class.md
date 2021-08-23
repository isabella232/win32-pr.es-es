---
description: 'Más información sobre: Clase EsentDatabaseLeakInSpaceException'
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
ms.openlocfilehash: cb8d79eb302665293532f3e2adf946162f6cb880d2ab79b84d8fa9bebd3f0f43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605321"
---
# <a name="esentdatabaseleakinspaceexception-class"></a>Clase EsentDatabaseLeakInSpaceException

Clase base para JET_err. Excepciones databaseLeakInSpace.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

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

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

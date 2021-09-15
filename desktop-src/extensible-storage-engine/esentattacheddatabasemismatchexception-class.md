---
description: 'Más información sobre: Clase EsentAttachedDatabaseMismatchException'
title: Clase EsentAttachedDatabaseMismatchException
TOCTitle: EsentAttachedDatabaseMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentattacheddatabasemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101019
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fca9c0dcb7526df0373cbf26099a8ca810ab3eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359189"
---
# <a name="esentattacheddatabasemismatchexception-class"></a>Clase EsentAttachedDatabaseMismatchException

Clase base para JET_err. Excepciones AttachedDatabaseMismatch.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAttachedDatabaseMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentAttachedDatabaseMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAttachedDatabaseMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentAttachedDatabaseMismatchException](./esentattacheddatabasemismatchexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

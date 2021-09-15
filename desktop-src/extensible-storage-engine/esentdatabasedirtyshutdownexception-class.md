---
description: 'Más información sobre: Clase EsentDatabaseDirtyShutdownException'
title: Clase EsentDatabaseDirtyShutdownException
TOCTitle: EsentDatabaseDirtyShutdownException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasedirtyshutdownexception(v=EXCHG.10)
ms:contentKeyID: 55101339
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7fcb7a3dffd5626bcf8bfc926103951747ee07e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580093"
---
# <a name="esentdatabasedirtyshutdownexception-class"></a>Clase EsentDatabaseDirtyShutdownException

Clase base para JET_err. DatabaseDirtyShutdown exceptions.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseDirtyShutdownException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseDirtyShutdownException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseDirtyShutdownException : EsentInconsistentException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentDatabaseDirtyShutdownException](./esentdatabasedirtyshutdownexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: Clase EsentOSSnapshotTimeOutException'
title: Clase EsentOSSnapshotTimeOutException
TOCTitle: EsentOSSnapshotTimeOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentossnapshottimeoutexception(v=EXCHG.10)
ms:contentKeyID: 55102393
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ee86c466c827211072f8345f05af2c1df5bf721
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966008"
---
# <a name="esentossnapshottimeoutexception-class"></a>Clase EsentOSSnapshotTimeOutException

Clase base para JET_err. Excepciones de OSSnapshotTimeOut.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOSSnapshotTimeOutException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentOSSnapshotTimeOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOSSnapshotTimeOutException : EsentOperationException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentOSSnapshotTimeOutException](./esentossnapshottimeoutexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

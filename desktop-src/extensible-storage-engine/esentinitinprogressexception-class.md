---
description: 'Más información sobre: Clase EsentInitInProgressException'
title: Clase EsentInitInProgressException
TOCTitle: EsentInitInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInitInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinitinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55101813
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInitInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInitInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b035465e575dd94f68b38cf72f8771c24add49d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172473"
---
# <a name="esentinitinprogressexception-class"></a>Clase EsentInitInProgressException

Clase base para JET_err. Excepciones de InitInProgress.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentInitInProgressException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInitInProgressException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentInitInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInitInProgressException : EsentOperationException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentInitInProgressException](./esentinitinprogressexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

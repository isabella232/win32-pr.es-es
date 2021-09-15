---
description: 'Más información sobre: Clase EsentRecordTooBigForBackwardCompatibilityException'
title: Clase EsentRecordTooBigForBackwardCompatibilityException
TOCTitle: EsentRecordTooBigForBackwardCompatibilityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordtoobigforbackwardcompatibilityexception(v=EXCHG.10)
ms:contentKeyID: 55102602
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3d56e87678daf465f3f303d649e8c554fbb0c21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467237"
---
# <a name="esentrecordtoobigforbackwardcompatibilityexception-class"></a>Clase EsentRecordTooBigForBackwardCompatibilityException

Clase base para JET_err. Excepciones recordTooBigForBackwardCompatibility.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordTooBigForBackwardCompatibilityException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordTooBigForBackwardCompatibilityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordTooBigForBackwardCompatibilityException : EsentStateException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentRecordTooBigForBackwardCompatibilityException](./esentrecordtoobigforbackwardcompatibilityexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

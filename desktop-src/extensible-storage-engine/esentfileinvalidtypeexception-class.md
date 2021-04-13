---
description: 'Más información sobre: clase EsentFileInvalidTypeException'
title: Clase EsentFileInvalidTypeException
TOCTitle: EsentFileInvalidTypeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileinvalidtypeexception(v=EXCHG.10)
ms:contentKeyID: 55107272
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c2bf5cf30cb45734613fcabc446834085d5bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361431"
---
# <a name="esentfileinvalidtypeexception-class"></a>Clase EsentFileInvalidTypeException

Clase base para JET_err. Excepciones FileInvalidType.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentFileInvalidTypeException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileInvalidTypeException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentFileInvalidTypeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileInvalidTypeException : EsentInconsistentException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentFileInvalidTypeException](./esentfileinvalidtypeexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

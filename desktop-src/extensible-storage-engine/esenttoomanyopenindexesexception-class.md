---
description: 'Más información sobre: Clase EsentTooManyOpenIndexesException'
title: Clase EsentTooManyOpenIndexesException
TOCTitle: EsentTooManyOpenIndexesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopenindexesexception(v=EXCHG.10)
ms:contentKeyID: 55103106
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 681f9a8ec67b9b9c82babcc3814833a1a3dbb0d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360484"
---
# <a name="esenttoomanyopenindexesexception-class"></a>Clase EsentTooManyOpenIndexesException

Clase base para JET_err. TooManyOpenIndexes excepciones.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMemoryException](./esentmemoryexception-class.md)  
              Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenIndexesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyOpenIndexesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenIndexesException : EsentMemoryException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentTooManyOpenIndexesException](./esenttoomanyopenindexesexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

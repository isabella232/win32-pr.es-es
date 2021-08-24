---
description: 'Más información sobre: Clase EsentIndexTuplesNonUniqueOnlyException'
title: Clase EsentIndexTuplesNonUniqueOnlyException
TOCTitle: EsentIndexTuplesNonUniqueOnlyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindextuplesnonuniqueonlyexception(v=EXCHG.10)
ms:contentKeyID: 55101858
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9d71ea99dfb3625c89b58f610a81a272d81d17390f34c4bff5eceb517d3324a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784015"
---
# <a name="esentindextuplesnonuniqueonlyexception-class"></a>Clase EsentIndexTuplesNonUniqueOnlyException

Clase base para JET_err. IndexTuplesNonUniqueOnly exceptions.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexTuplesNonUniqueOnlyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentIndexTuplesNonUniqueOnlyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexTuplesNonUniqueOnlyException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentIndexTuplesNonUniqueOnlyException](./esentindextuplesnonuniqueonlyexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

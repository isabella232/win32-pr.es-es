---
description: 'Más información sobre: Clase EsentFragmentationException'
title: Clase EsentFragmentationException
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2db8934cfdbfb58b44d3de14c13c72bc7d5ce5afa4f5b2bdfaec0a05926469af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838725"
---
# <a name="esentfragmentationexception-class"></a>Clase EsentFragmentationException

Clase base para excepciones de fragmentación.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentFragmentationException  
            

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentFragmentationException](./esentfragmentationexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentFragmentationException  
            [Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchException](./esentlogsectorsizemismatchexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException](./esentlogsequenceendexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException](./esentoutofautoincrementvaluesexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException](./esentoutofdbtimevaluesexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException](./esentoutoflongvalueidsexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException](./esentoutofobjectidsexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException](./esentoutofsequentialindexvaluesexception-class.md)
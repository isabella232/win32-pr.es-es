---
description: 'Más información sobre: clase EsentFragmentationException'
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
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721255"
---
# <a name="esentfragmentationexception-class"></a>Clase EsentFragmentationException

Clase base para las excepciones de fragmentación.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentFragmentationException  
            

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

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

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentFragmentationException  
            [Microsoft. ISAM. esent. Interop. EsentLogSectorSizeMismatchException](./esentlogsectorsizemismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogSequenceEndDatabasesConsistentException](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException](./esentlogsequenceendexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfAutoincrementValuesException](./esentoutofautoincrementvaluesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfDbtimeValuesException](./esentoutofdbtimevaluesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfLongValueIDsException](./esentoutoflongvalueidsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfObjectIDsException](./esentoutofobjectidsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfSequentialIndexValuesException](./esentoutofsequentialindexvaluesexception-class.md)
---
description: 'Más información sobre: Clase EsentPrimaryIndexCorruptedException'
title: Clase EsentPrimaryIndexCorruptedException
TOCTitle: EsentPrimaryIndexCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentprimaryindexcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102484
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 712d8d4ad906316ab8be71f8a0404fb27710fdb4e232fb3e0dc3d5e29a4b3c59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971315"
---
# <a name="esentprimaryindexcorruptedexception-class"></a>Clase EsentPrimaryIndexCorruptedException

Clase base para JET_err. Excepciones PrimaryIndexCorrupted.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPrimaryIndexCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentPrimaryIndexCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPrimaryIndexCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentPrimaryIndexCorruptedException](./esentprimaryindexcorruptedexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

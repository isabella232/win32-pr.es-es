---
description: 'Más información sobre: clase EsentNTSystemCallFailedException'
title: Clase EsentNTSystemCallFailedException
TOCTitle: EsentNTSystemCallFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentntsystemcallfailedexception(v=EXCHG.10)
ms:contentKeyID: 55102309
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87ebb646a4746b86343772ff7fa509a2b99f0965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279570"
---
# <a name="esentntsystemcallfailedexception-class"></a>Clase EsentNTSystemCallFailedException

Clase base para JET_err. Excepciones NTSystemCallFailed.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentNTSystemCallFailedException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNTSystemCallFailedException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentNTSystemCallFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNTSystemCallFailedException : EsentOperationException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentNTSystemCallFailedException](./esentntsystemcallfailedexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

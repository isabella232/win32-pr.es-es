---
description: 'Más información sobre: Clase EsentInvalidLanguageIdException'
title: Clase EsentInvalidLanguageIdException
TOCTitle: EsentInvalidLanguageIdException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLanguageIdException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlanguageidexception(v=EXCHG.10)
ms:contentKeyID: 55107279
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLanguageIdException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLanguageIdException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3dbd9caf74554d2616efbbe16a4aa43a7f05bde10d74f157ccaa57fe5076610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118265802"
---
# <a name="esentinvalidlanguageidexception-class"></a>Clase EsentInvalidLanguageIdException

Clase base para JET_err. Excepciones invalidLanguageId.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentInvalidLanguageIdException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLanguageIdException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidLanguageIdException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLanguageIdException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentInvalidLanguageIdException](./esentinvalidlanguageidexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

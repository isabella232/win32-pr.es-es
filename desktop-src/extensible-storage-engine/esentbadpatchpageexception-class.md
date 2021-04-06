---
description: 'Más información sobre: clase EsentBadPatchPageException'
title: Clase EsentBadPatchPageException
TOCTitle: EsentBadPatchPageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadPatchPageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadpatchpageexception(v=EXCHG.10)
ms:contentKeyID: 55101149
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadPatchPageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadPatchPageException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b29602e327718dab63c402d075b3a7bf5695604a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817486"
---
# <a name="esentbadpatchpageexception-class"></a>Clase EsentBadPatchPageException

Clase base para JET_err. Excepciones BadPatchPage.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentBadPatchPageException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadPatchPageException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentBadPatchPageException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadPatchPageException : EsentObsoleteException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentBadPatchPageException](./esentbadpatchpageexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

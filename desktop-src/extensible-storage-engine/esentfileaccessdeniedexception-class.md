---
description: 'Más información sobre: Clase EsentFileAccessDeniedException'
title: Clase EsentFileAccessDeniedException
TOCTitle: EsentFileAccessDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileaccessdeniedexception(v=EXCHG.10)
ms:contentKeyID: 55101658
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afb92cc5fad314763ef2d679035b727f38b8305a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174681"
---
# <a name="esentfileaccessdeniedexception-class"></a>Clase EsentFileAccessDeniedException

Clase base para JET_err. Excepciones FileAccessDenied.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentIOException](./esentioexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileAccessDeniedException _
    Inherits EsentIOException
'Usage
Dim instance As EsentFileAccessDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileAccessDeniedException : EsentIOException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentFileAccessDeniedException](./esentfileaccessdeniedexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

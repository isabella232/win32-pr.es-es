---
description: 'Más información sobre: Clase de instancia'
title: Clase de instancia
TOCTitle: Instance class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance(v=EXCHG.10)
ms:contentKeyID: 55103260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be11bc87b1a7969b1c0ddca6640979be0aadae3715a4c2e825ca470ee7932ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731755"
---
# <a name="instance-class"></a>Clase de instancia

Clase que encapsula un [JET_INSTANCE](./jet-instance-structure.md) en un objeto descartable. La instancia debe cerrarse en último lugar y cerrar la instancia libera todos los demás recursos de la instancia.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Runtime.ConstrainedExecution.CriticalFinalizerObject](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [System.Runtime.InteropServices.SafeHandle](/dotnet/api/system.runtime.interopservices.safehandle)  
      [Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        Microsoft.Isam.Esent.Interop.Instance  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Class Instance _
    Inherits SafeHandleZeroOrMinusOneIsInvalid
'Usage
Dim instance As Instance
```

``` csharp
public class Instance : SafeHandleZeroOrMinusOneIsInvalid
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de instancia](./instance-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

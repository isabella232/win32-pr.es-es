---
description: 'Más información sobre: Propiedad InstanceParameters.PreferredVerPages'
title: Propiedad InstanceParameters.PreferredVerPages
TOCTitle: 'PreferredVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.preferredverpages(v=EXCHG.10)
ms:contentKeyID: 55103322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PreferredVerPages
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54287a87a1707df87f5be653456d3ed652ab58a56e20c61ee057858d8ea0b702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255866"
---
# <a name="instanceparameterspreferredverpages-property"></a>Propiedad InstanceParameters.PreferredVerPages

Obtiene o establece el número preferido de páginas de almacén de versiones reservadas para esta instancia. Si el tamaño del almacén de versiones supera este umbral, cualquier información que solo se utilice para tareas en segundo plano opcionales, como reclamar el espacio eliminado en la base de datos, se sacrificará en su lugar para conservar espacio para la información transaccional.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property PreferredVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PreferredVerPages

instance.PreferredVerPages = value
```

``` csharp
public int PreferredVerPages { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

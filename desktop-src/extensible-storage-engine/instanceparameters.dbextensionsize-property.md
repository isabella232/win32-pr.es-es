---
description: 'Más información sobre: InstanceParameters. DbExtensionSize (propiedad)'
title: Propiedad InstanceParameters. DbExtensionSize
TOCTitle: 'DbExtensionSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.dbextensionsize(v=EXCHG.10)
ms:contentKeyID: 55107443
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_DbExtensionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_DbExtensionSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 402c37ca649a9e9ff70435c8a8ef58f79376842b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715541"
---
# <a name="instanceparametersdbextensionsize-property"></a>Propiedad InstanceParameters. DbExtensionSize

Obtiene o establece el número de páginas que se agregan a un archivo de base de datos cada vez que necesita crecer para alojar más datos.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property DbExtensionSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.DbExtensionSize

instance.DbExtensionSize = value
```

``` csharp
public int DbExtensionSize { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

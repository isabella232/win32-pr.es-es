---
description: 'Más información sobre: Propiedad InstanceParameters.NoInformationEvent'
title: Propiedad InstanceParameters.NoInformationEvent
TOCTitle: 'NoInformationEvent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.NoInformationEvent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.noinformationevent(v=EXCHG.10)
ms:contentKeyID: 55103564
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.NoInformationEvent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_NoInformationEvent
- Microsoft.Isam.Esent.Interop.InstanceParameters.NoInformationEvent
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_NoInformationEvent
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0e9b933dc477011c1835da5b95fc6ed11902827
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567673"
---
# <a name="instanceparametersnoinformationevent-property"></a>Propiedad InstanceParameters.NoInformationEvent

Obtiene o establece un valor que indica si se suprimirán los mensajes del registro de eventos informativos que normalmente generaría el motor de base de datos.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property NoInformationEvent As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.NoInformationEvent

instance.NoInformationEvent = value
```

``` csharp
public bool NoInformationEvent { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

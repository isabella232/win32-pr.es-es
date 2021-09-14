---
description: 'Más información sobre: estructura JET_INSTANCE datos'
title: JET_INSTANCE estructura
TOCTitle: JET_INSTANCE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance(v=EXCHG.10)
ms:contentKeyID: 39510997
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a676c0815ba20b725da0216a7c9a145c1c1cfd68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965707"
---
# <a name="jet_instance-structure"></a>JET_INSTANCE estructura

Un JET_INSTANCE contiene un identificador para la instancia de la base de datos que se usará para las llamadas a la API jet.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Structure JET_INSTANCE _
    Implements IEquatable(Of JET_INSTANCE), IFormattable
'Usage
Dim instance As JET_INSTANCE
```

``` csharp
public struct JET_INSTANCE : IEquatable<JET_INSTANCE>, 
    IFormattable
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_INSTANCE miembros](./jet-instance-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

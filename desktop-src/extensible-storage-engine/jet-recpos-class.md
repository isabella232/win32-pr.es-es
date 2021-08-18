---
description: 'Más información sobre: JET_RECPOS clase'
title: JET_RECPOS clase
TOCTitle: JET_RECPOS class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_RECPOS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recpos(v=EXCHG.10)
ms:contentKeyID: 55103839
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECPOS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECPOS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c25fd9cb9af531f134627ffcc54cd9fa5d37a33b340c53129a83c6538b33b1f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107524"
---
# <a name="jet_recpos-class"></a>JET_RECPOS clase

Representa una posición fraccionera dentro de un índice. JetGotoPosition y JetGetRecordPosition lo usan.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  Microsoft.Isam.Esent.Interop.JET_RECPOS  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_RECPOS _
    Implements IContentEquatable(Of JET_RECPOS), IDeepCloneable(Of JET_RECPOS)
'Usage
Dim instance As JET_RECPOS
```

``` csharp
[SerializableAttribute]
public sealed class JET_RECPOS : IContentEquatable<JET_RECPOS>, 
    IDeepCloneable<JET_RECPOS>
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_RECPOS miembros](./jet-recpos-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

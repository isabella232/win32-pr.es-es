---
description: 'Más información sobre: JET_CONDITIONALCOLUMN clase'
title: JET_CONDITIONALCOLUMN clase
TOCTitle: JET_CONDITIONALCOLUMN class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn(v=EXCHG.10)
ms:contentKeyID: 55107506
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23b116ce88b24702711d74f610c208a72c44addf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126883044"
---
# <a name="jet_conditionalcolumn-class"></a>JET_CONDITIONALCOLUMN clase

Define cómo se realiza la indexación condicional para un índice determinado. Un índice condicional contiene una entrada de índice solo para las filas que coinciden con la condición especificada. Sin embargo, la columna condicional no forma parte de la clave del índice, solo controla la presencia de la entrada de índice.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_CONDITIONALCOLUMN _
    Implements IContentEquatable(Of JET_CONDITIONALCOLUMN), IDeepCloneable(Of JET_CONDITIONALCOLUMN)
'Usage
Dim instance As JET_CONDITIONALCOLUMN
```

``` csharp
[SerializableAttribute]
public sealed class JET_CONDITIONALCOLUMN : IContentEquatable<JET_CONDITIONALCOLUMN>, 
    IDeepCloneable<JET_CONDITIONALCOLUMN>
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_CONDITIONALCOLUMN miembros](./jet-conditionalcolumn-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Más información sobre: JET_BKINFO estructura'
title: JET_BKINFO estructura
TOCTitle: JET_BKINFO structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo(v=EXCHG.10)
ms:contentKeyID: 39511166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e7e309704bce5ba0d4cba82494205cb92a0d904ef258a335d4858e337bcd884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118767362"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO estructura

Contiene una colección de datos sobre un evento de copia de seguridad específico.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKINFO _
    Implements IEquatable(Of JET_BKINFO), INullableJetStruct
'Usage
Dim instance As JET_BKINFO
```

``` csharp
[SerializableAttribute]
public struct JET_BKINFO : IEquatable<JET_BKINFO>, 
    INullableJetStruct
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_BKINFO miembros](./jet-bkinfo-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

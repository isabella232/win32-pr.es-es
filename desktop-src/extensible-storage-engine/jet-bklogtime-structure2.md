---
description: 'Más información acerca de: estructura de JET_BKLOGTIME'
title: Estructura de JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime(v=EXCHG.10)
ms:contentKeyID: 39512194
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b718254082095592f097097500d2690be320dd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155032"
---
# <a name="jet_bklogtime-structure"></a>Estructura de JET_BKLOGTIME

Describe la fecha y hora en que se realizó una copia de seguridad.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKLOGTIME _
    Implements IEquatable(Of JET_BKLOGTIME), IJET_LOGTIME,  _
    INullableJetStruct
'Usage
Dim instance As JET_BKLOGTIME
```

``` csharp
[SerializableAttribute]
public struct JET_BKLOGTIME : IEquatable<JET_BKLOGTIME>, 
    IJET_LOGTIME, INullableJetStruct
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de JET_BKLOGTIME](./jet-bklogtime-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

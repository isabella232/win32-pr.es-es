---
description: 'Más información acerca de: estructura de JET_LOGTIME'
title: Estructura de JET_LOGTIME
TOCTitle: JET_LOGTIME structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LOGTIME
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime(v=EXCHG.10)
ms:contentKeyID: 39510198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617911c8f9f0246a836de11d9530536bf9c6e6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697828"
---
# <a name="jet_logtime-structure"></a>Estructura de JET_LOGTIME

Describe una fecha y hora.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_LOGTIME _
    Implements IEquatable(Of JET_LOGTIME), IJET_LOGTIME,  _
    INullableJetStruct
'Usage
Dim instance As JET_LOGTIME
```

``` csharp
[SerializableAttribute]
public struct JET_LOGTIME : IEquatable<JET_LOGTIME>, 
    IJET_LOGTIME, INullableJetStruct
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de JET_LOGTIME](./jet-logtime-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

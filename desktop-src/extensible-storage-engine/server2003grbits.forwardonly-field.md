---
description: Más información sobre el campo Server2003Grbits.ForwardOnly
title: Campo Server2003Grbits.ForwardOnly (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f98dca3e85eb5ad3c57ef1203971078035c7191ca3e5358dba701dcd870f8480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603845"
---
# <a name="server2003grbitsforwardonly-field"></a>Campo Server2003Grbits.ForwardOnly

Esta opción solicita que la tabla temporal solo se cree si el administrador de tablas temporales puede usar la implementación optimizada para los resultados de consulta intermedios. Si alguna característica de la tabla temporal impediría el uso de esta optimización, se producirá un error en la operación JET_errCannotMaterializeForwardOnlySort. Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas. Consulte [Único](./temptablegrbit-enumeration.md) para obtener más información.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Server2003Grbits (clase)](./server2003grbits-class.md)

[Miembros server2003Grbits](./server2003grbits-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

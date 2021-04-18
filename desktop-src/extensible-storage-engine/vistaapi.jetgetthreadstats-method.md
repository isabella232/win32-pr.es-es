---
description: 'Más información sobre: VistaApi. JetGetThreadStats (método)'
title: Método VistaApi. JetGetThreadStats (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705997"
---
# <a name="vistaapijetgetthreadstats-method"></a>VistaApi. JetGetThreadStats, método

Recupera información de rendimiento del motor de base de datos para el subproceso actual. Se pueden usar varias llamadas para recopilar estadísticas que reflejen la actividad del motor de base de datos en este subproceso entre esas llamadas.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a>Parámetros

  - threadstats  
    Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Devuelve los datos de las estadísticas del subproceso.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase VistaApi](./vistaapi-class.md)

[Miembros de VistaApi](./vistaapi-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)

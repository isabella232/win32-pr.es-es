---
description: 'Más información sobre: Conversions. LCMapFlagsFromCompareOptions (método)'
title: Método Conversions. LCMapFlagsFromCompareOptions
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715415"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a>Método Conversions. LCMapFlagsFromCompareOptions

Asigne a la opción CompareOptions los marcadores de LCMapString. Se omiten las opciones desconocidas.

Esta API no es conforme a CLS. 

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a>Parámetros

  - compareOptions  
    Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
    
    Opciones que se van a convertir.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. UInt32](/dotnet/api/system.uint32)  
Marcas de LCMapString que coinciden con las opciones de comparación. Se omiten las opciones no admitidas.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Conversions (clase)](./conversions-class.md)

[Miembros de conversiones](./conversions-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: Más información sobre el método Conversions.LCMapFlagsFromCompareOptions
title: Método Conversions.LCMapFlagsFromCompareOptions
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
ms.openlocfilehash: a13d74b94e6d0a3dcc74e43460a57126b3e9c8c7dd92e67409426374ea6ceaf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042303"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a>Método Conversions.LCMapFlagsFromCompareOptions

Proporcionar CompareOptions y convertirlos en marcas de LCMapString. Se omiten las opciones desconocidas.

Esta API no es conforme a CLS. 

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)  
    
    Opciones que se convertirán.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.UInt32](/dotnet/api/system.uint32)  
Las marcas LCMapString que coinciden con las opciones de comparación. Se omiten las opciones no admitidas.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Conversions](./conversions-class.md)

[Miembros de conversiones](./conversions-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

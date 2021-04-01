---
description: 'Más información sobre: Conversions. CompareOptionsFromLCMapFlags (método)'
title: Método Conversions. CompareOptionsFromLCMapFlags
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275726"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>Método Conversions. CompareOptionsFromLCMapFlags

Las marcas especificadas para LCMapFlags, las convierten en opciones de comparación. Se omiten las opciones desconocidas.

Esta API no es conforme a CLS. 

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a>Parámetros

  - lcmapFlags  
    Tipo: [System. UInt32](/dotnet/api/system.uint32)  
    
    Las marcas de LCMapString.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
CompareOptions que describe las marcas (conocidas).  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Conversions (clase)](./conversions-class.md)

[Miembros de conversiones](./conversions-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

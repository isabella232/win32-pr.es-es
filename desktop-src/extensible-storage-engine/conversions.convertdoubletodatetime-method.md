---
description: 'Más información sobre: Conversions. ConvertDoubleToDateTime (método)'
title: Método Conversions. ConvertDoubleToDateTime
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697468"
---
# <a name="conversionsconvertdoubletodatetime-method"></a>Método Conversions. ConvertDoubleToDateTime

Convierte un valor Double (formato de fecha y hora de OA) en un valor DateTime. A diferencia de DateTime. FromOADate, esto no inicia excepciones.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a>Parámetros

  - d  
    Tipo: [System. Double](/dotnet/api/system.double)  
    
    Valor Double.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. DateTime](/dotnet/api/system.datetime)  
Un valor de fecha y hora.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Conversions (clase)](./conversions-class.md)

[Miembros de conversiones](./conversions-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

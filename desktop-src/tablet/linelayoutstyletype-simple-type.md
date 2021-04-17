---
description: Define los valores válidos para el atributo de estilo del elemento LineLayout.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Tipo simple de LineLayoutStyleType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697756"
---
# <a name="linelayoutstyletype-simple-type"></a>Tipo simple de LineLayoutStyleType

Define los valores válidos para el atributo de **estilo** del [elemento LineLayout](linelayout-element.md).

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **LineLayoutStyleType** es una cadena restringida por el siguiente patrón:

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>Observaciones

Los valores válidos para el atributo de **estilo** del [elemento LineLayout](linelayout-element.md) son:

-   None
-   Sólido
-   Guión
-   Punto
-   DashDot
-   DashDotDot
-   Doble

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 





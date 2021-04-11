---
description: Define el tipo que contiene los valores válidos para el atributo de tipo para el elemento margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Tipo simple de MarginTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278850"
---
# <a name="margintypetype-simple-type"></a>Tipo simple de MarginTypeType

Define el tipo que contiene los valores válidos para el atributo de **tipo** para el [elemento margin](margin-element.md).

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **MarginTypeType** es una **cadena** restringida por el siguiente patrón:

-   `Left|Right`

## <a name="remarks"></a>Observaciones

Los valores válidos para el atributo **Type** del [elemento margin](margin-element.md) son "left" y "Right".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 





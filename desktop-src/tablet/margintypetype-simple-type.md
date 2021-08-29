---
description: Define el tipo que contiene valores válidos para el atributo Type para el elemento Margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Tipo simple MarginTypeType
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
ms.openlocfilehash: b1996b99729e177f7012db097644807a2bf7052f231e089052d5244b20d016ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031693"
---
# <a name="margintypetype-simple-type"></a>Tipo simple MarginTypeType

Define el tipo que contiene valores válidos para el **atributo Type** para el [elemento Margin](margin-element.md).

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

El **tipo simple MarginTypeType** es una **cadena** que está restringida por el siguiente patrón:

-   `Left|Right`

## <a name="remarks"></a>Comentarios

Los valores válidos para **el atributo Type** para el elemento [Margin](margin-element.md) son "Left" y "Right".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 





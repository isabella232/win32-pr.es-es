---
title: Tipo complejo MapType
description: Define una lista de pares nombre-valor.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- EventLog de tipo complejo MapType
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 162676ab5d017c8fa6d6d280a07d1e4500e77cc79e0eacf25e23d5f20c0b3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120923"
---
# <a name="maptype-complex-type"></a>Tipo complejo MapType

Define una lista de pares nombre-valor.

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                          | Tipo                                                                 | Descripción                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Bits**](eventmanifestschema-bitmap-maptype-element.md)     | [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)     | Define una lista de pares nombre-valor que asignan valores de bits y valores de cadena.<br/>     |
| [**valueMap**](eventmanifestschema-valuemap-maptype-element.md) | [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md) | Define una lista de pares nombre-valor que asignan valores enteros y valores de cadena.<br/> |



## <a name="remarks"></a>Comentarios

Normalmente, se crean mapas para proporcionar valores de cadena enumerados para los datos de eventos.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo especificar un mapa de valores y un mapa de bits.


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 






---
description: Contiene un hexBinary de 1 byte que se usa para diferenciar entre las NIC realizadas por el mismo IHV.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: elemento type (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 234b30883df463d7c336ce7d270e574d41a5cabe9924c327a35ff1a31ee65632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797506"
---
# <a name="type-ouiheader-element"></a>elemento type (OUIHeader)

El elemento type (OUIHeader) contiene un elemento hexBinary de 1 byte que se usa para diferenciar entre las NIC realizadas por el mismo IHV.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="type">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) define el elemento .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 





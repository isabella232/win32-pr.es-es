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
ms.openlocfilehash: 12637e5a70409166e5a31aa0fc98f4df1b9f6945
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074179"
---
# <a name="type-ouiheader-element"></a>elemento type (OUIHeader)

El elemento type (OUIHeader) contiene un elemento hexBinary de 1 byte que se usa para diferenciar entre las NIC realizadas por el mismo IHV.

Windows XP con SP3 y la API de LAN inalámbrica **para Windows XP con SP2:** No se admite este elemento.

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



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 





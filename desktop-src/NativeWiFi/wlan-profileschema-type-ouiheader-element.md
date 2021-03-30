---
description: Contiene un hexBinary de 1 byte que se usa para diferenciar entre las NIC realizadas por el mismo IHV.
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: Elemento Type (OUIHeader)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910646"
---
# <a name="type-ouiheader-element"></a>Elemento Type (OUIHeader)

El elemento Type (OUIHeader) contiene un hexBinary de 1 byte que se usa para diferenciar entre las NIC realizadas por el mismo IHV.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.

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

El elemento se define mediante el elemento [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 





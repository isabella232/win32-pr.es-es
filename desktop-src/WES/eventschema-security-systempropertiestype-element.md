---
title: Elemento Security (SystemPropertiesType)
description: Identifica el usuario que registró el evento.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Elemento de seguridad EventLog
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20aef5465b8790bdba92c50181c0550ca5989c29d66fd53b9ec7ed0f760a2129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588291"
---
# <a name="security-systempropertiestype-element"></a>Elemento Security (SystemPropertiesType)

Identifica el usuario que registró el evento.

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

El tipo complejo **SystemPropertiesType** define el [**elemento Security.**](eventschema-systempropertiestype-complextype.md)

## <a name="attributes"></a>Atributos



| Nombre   | Tipo   | Descripción                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | string | Identificador de seguridad (SID) del usuario en forma de cadena.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 






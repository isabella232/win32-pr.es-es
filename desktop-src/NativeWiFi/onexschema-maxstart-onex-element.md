---
description: Especifica el número máximo de mensajes EAPOL-Start enviados.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Elemento maxStart (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7c50945b8de53b6d058556e3b5c995d3ec17bfdc8f8d55ec3dc2e6e56089b2a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800765"
---
# <a name="maxstart-onex-element"></a>Elemento maxStart (OneX)

El elemento maxStart (OneX) especifica el número máximo de EAPOL-Start mensajes enviados. Una vez enviado el número máximo EAPOL-Start mensajes, el cliente asume que no hay ningún autenticador presente en la red.

Este elemento es opcional. Cuando maxStart no se especifica en un perfil, se usa un valor de 3 mensajes.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento maxStart** se define mediante el [**elemento OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 





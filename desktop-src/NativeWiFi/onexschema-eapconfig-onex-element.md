---
description: especifica la configuración de EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Elemento EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 539f30d6730ec0735006f9dd3812322468ce71c7b0fbd90610b6cd589e0d60bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684885"
---
# <a name="eapconfig-onex-element"></a>Elemento EAPConfig (OneX)

El **elemento EAPConfig** (OneX) especifica la configuración de EAPHost.

A diferencia de la mayoría de los elementos del esquema de perfil 802.1X, este elemento está en el espacio de `https://www.microsoft.com/provisioning/EapHostConfig` nombres . Sus elementos secundarios se definen en el [esquema eaphostconfig](../eaphost/eaphostconfigschema-schema.md). El [**elemento EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) es un elemento secundario del **elemento EAPConfig.**

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El **elemento EAPConfig** se define mediante el [**elemento OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



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

 

 

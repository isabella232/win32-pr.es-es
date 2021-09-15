---
title: Tipo complejo BaseEapMethodConfig
description: Obtenga información sobre el tipo complejo BaseEapMethodConfig. Este tipo es un elemento de marcador de posición para la configuración del método.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- Tipo complejo BaseEapMethodConfig EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568884"
---
# <a name="baseeapmethodconfig-complex-type"></a>Tipo complejo BaseEapMethodConfig

El **tipo complejo BaseEapMethodConfig** es un elemento de marcador de posición para la configuración del método.

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Observaciones

El método EAP realiza la validación del esquema en el contenido del **elemento BaseEapMethodConfig.**

## <a name="requirements"></a>Requisitos



| Role | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Remoto<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[esquema baseeapmethodconfig](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 






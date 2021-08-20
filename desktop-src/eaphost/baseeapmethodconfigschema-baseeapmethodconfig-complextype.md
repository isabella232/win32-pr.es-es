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
ms.openlocfilehash: 8decb1746391c1337440eb475a8a8face3f8b7466b73015db48e3991841a3c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086780"
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

## <a name="remarks"></a>Comentarios

El método EAP realiza la validación del esquema en el contenido del **elemento BaseEapMethodConfig.**

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[esquema baseeapmethodconfig](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 






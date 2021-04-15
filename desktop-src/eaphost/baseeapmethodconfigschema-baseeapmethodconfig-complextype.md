---
title: Tipo complejo de BaseEapMethodConfig
description: Obtenga información sobre el tipo complejo de BaseEapMethodConfig. Este tipo es un elemento de marcador de posición para la configuración del método.
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
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421429"
---
# <a name="baseeapmethodconfig-complex-type"></a>Tipo complejo de BaseEapMethodConfig

El tipo complejo de **BaseEapMethodConfig** es un elemento de marcador de posición para la configuración del método.

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

El método EAP realiza la validación del esquema en el contenido del elemento **BaseEapMethodConfig** .

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapmethodconfig](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 






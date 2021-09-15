---
title: Elemento EapType (propiedades de usuario base)
description: Obtenga información sobre el elemento EapType. Este elemento captura la configuración específica del método dentro del elemento Eap. | Elemento EapType (propiedades de usuario base)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
keywords:
- EapType, elemento EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568844"
---
# <a name="eaptype-element-base-user-properties"></a>Elemento EapType (propiedades de usuario base)

El **elemento EapType** captura la configuración específica del método dentro del elemento Eap.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Observaciones

El **elemento EapType** es abstracto; cada método debe definir y usar un elemento derivado en los documentos de instancia.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|-------------------------------------|------------------------------------------------------|
| Remoto<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[esquema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






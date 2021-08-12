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
ms.openlocfilehash: 7d9cb6afe13b8c0060b26edbf5add618c776518b3b03e5abdc1f9131dbbcabde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275538"
---
# <a name="eaptype-element-base-user-properties"></a>Elemento EapType (propiedades de usuario base)

El **elemento EapType** captura la configuración específica del método dentro del elemento Eap.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Comentarios

El **elemento EapType** es abstracto; cada método debe definir y usar un elemento derivado en los documentos de instancia.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima admitida del sistema operativo |
|-------------------------------------|------------------------------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Server<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[esquema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






---
title: Elemento EapType (propiedad de conexión de esquema v1)
description: Obtenga información sobre el elemento EapType. Este elemento captura la configuración específica del método dentro del elemento Eap. | Elemento EapType (propiedad de conexión de esquema v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
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
ms.openlocfilehash: 3f2681e5682ad98ab5f4185174996920315d8c3b81dde8ba69d13ca178904ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498791"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>Elemento EapType (propiedad de conexión de esquema v1)

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
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1 Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 






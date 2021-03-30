---
title: Elemento EapType (propiedad de conexión del esquema V1)
description: Obtenga información sobre el elemento EapType. Este elemento captura la configuración específica del método dentro del elemento EAP. | Elemento EapType (propiedad de conexión del esquema V1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- Elemento EapType EAPHost
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
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820570"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>Elemento EapType (propiedad de conexión del esquema V1)

El elemento **EapType** captura la configuración específica del método dentro del elemento EAP.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Observaciones

El elemento **EapType** es abstracto; cada método debe definir y usar un elemento derivado en los documentos de instancia.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 






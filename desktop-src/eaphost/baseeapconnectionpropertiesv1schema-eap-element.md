---
title: Elemento Eap (propiedades de conexión)
description: Obtenga información sobre el elemento Eap. Este elemento captura el tipo de método seleccionado y la configuración específica del método. | Elemento Eap (propiedades de conexión)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
keywords:
- Eap, elemento EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7750bdb9a5f3c2d6c187b0f765eeb9d7ad88c015403719c16d0b683637b10027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086949"
---
# <a name="eap-element-connection-properties"></a>Elemento Eap (propiedades de conexión)

El **elemento Eap** captura el tipo de método seleccionado y la configuración específica del método.

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Comentarios

El método puede definir los elementos constituyentes dentro del **elemento Eap.** El método también realiza la validación del esquema en los elementos de **Eap**.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1 Schema](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 






---
description: Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1X para la autenticación de puertos.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Elemento OneXEnforced (security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bcaa8604fb8b813417299725133e9c6e51f7d7510b540cf8495ff9009b9d1c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798445"
---
# <a name="onexenforced-security-element"></a>Elemento OneXEnforced (security)

El **elemento OneXEnforced** (security) especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1X para la autenticación de puertos. Cuando **OneXEnforced es** TRUE, el servicio de configuración automática debe usar 802.1X para la autenticación de puertos. Cuando **OneXEnforced** es FALSE, el servicio de configuración automática intentará usar 802.1X para la autenticación de puerto, pero el servicio no volverá a ninguna autenticación si se produce un error en la autenticación 802.1X por cualquier motivo.

Este elemento es opcional. El valor predeterminado es FALSE.

Este elemento solo tiene un valor significativo si [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) es TRUE. Si **OneXEnabled** es FALSE, se omite el valor de este elemento.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

El **elemento OneXEnforced** se define mediante el [**elemento de**](lan-profileschema-security-msm-element.md) seguridad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Seguridad**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 





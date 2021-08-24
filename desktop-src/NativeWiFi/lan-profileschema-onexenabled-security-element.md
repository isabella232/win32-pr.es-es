---
description: Especifica si el servicio de configuración automática para redes cableadas intentará la autenticación de puerto mediante 802.1X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Elemento OneXEnabled (security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aaaf5344078e4c8da2e5ee2118eed84563ebeb4daa8aebd700a29630b2fe4301
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801095"
---
# <a name="onexenabled-security-element"></a>Elemento OneXEnabled (security)

El **elemento OneXEnabled** (seguridad) especifica si el servicio de configuración automática para redes cableadas intentará la autenticación de puerto mediante 802.1X. Cuando **OneXEnabled** es FALSE, el servicio de configuración automática nunca usa 802.1X para la autenticación de puertos. Cuando **OneXEnabled** es TRUE, el servicio de configuración automática intenta la autenticación de puerto mediante 802.1X.

Este elemento es opcional. El valor predeterminado es TRUE. Cuando **No se especifica OneXEnabled** en un perfil, se puede usar 802.1X para la autenticación de puertos.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

El **elemento OneXEnabled** se define mediante el [**elemento de**](lan-profileschema-security-msm-element.md) seguridad .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Seguridad**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 





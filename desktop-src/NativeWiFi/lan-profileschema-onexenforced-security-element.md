---
description: Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1 X para la autenticación de puertos.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Elemento OneXEnforced (Security)
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
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678133"
---
# <a name="onexenforced-security-element"></a>Elemento OneXEnforced (Security)

El elemento **OneXEnforced** (Security) especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1 x para la autenticación de puertos. Cuando **OneXEnforced** es true, el servicio de configuración automática debe usar 802.1 x para la autenticación de puertos. Cuando **OneXEnforced** es false, el servicio de configuración automática intentará usar 802.1 x para la autenticación de puerto, pero el servicio revertirá a ninguna autenticación si se produce un error en la autenticación 802.1 x por cualquier motivo.

Este elemento es opcional. El valor predeterminado es FALSE.

Este elemento solo tiene un valor significativo si [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) es true. Si **OneXEnabled** es false, se omite el valor de este elemento.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

El elemento **OneXEnforced** se define mediante el elemento [**Security**](lan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**bursátil**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 





---
description: Especifica si el servicio de configuración automática de redes cableadas intentará la autenticación del puerto mediante 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Elemento OneXEnabled (Security)
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
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277729"
---
# <a name="onexenabled-security-element"></a>Elemento OneXEnabled (Security)

El elemento **OneXEnabled** (Security) especifica si el servicio de configuración automática de redes cableadas intentará la autenticación del puerto mediante 802.1 x. Cuando **OneXEnabled** es false, el servicio de configuración automática nunca usa 802.1 x para la autenticación de puertos. Cuando **OneXEnabled** es true, el servicio de configuración automática intenta la autenticación del puerto mediante 802.1 x.

Este elemento es opcional. El valor predeterminado es TRUE. Cuando **OneXEnabled** no se especifica en un perfil, se puede usar 802.1 x para la autenticación de puertos.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

El elemento **OneXEnabled** se define mediante el elemento [**Security**](lan-profileschema-security-msm-element.md) .

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

 

 





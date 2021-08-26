---
title: Elemento UserCert (EapType)
description: Hace referencia al hash SHA-1 del certificado que se debe usar para la autenticación.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- Elemento UserCert EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef25a43bf13b1cfb1e4b03f78f5772567b3bfb92f1c31bb810da7882a4d3e1c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067235"
---
# <a name="usercert-eaptype-element"></a>Elemento UserCert (EapType)

El **elemento UserCert (EapType)** hace referencia al hash SHA-1 del certificado que se debe usar para la autenticación.

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

El **elemento UserCert** se define mediante el [**elemento EapType.**](eaptlsuserpropertiesv1schema-eaptype-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 






---
title: Elemento InnerEapOptional (EapType)
description: Obtenga información sobre el elemento InnerEapOptional (EapType). Este elemento indica si se debe realizar el acceso GUEST.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Elemento INNEREapOptional EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 372163b39ea788b5c03bd25aedcc44aee172d58080fb94e3333a029a514962a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404595"
---
# <a name="innereapoptional-eaptype-element"></a>Elemento InnerEapOptional (EapType)

El **elemento InnerEapOptional (EapType)** indica si se debe realizar el acceso GUEST.

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

El elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) define el elemento **InnerEapOptional.**

## <a name="remarks"></a>Comentarios

Si el **elemento InnerEapOptional** es TRUE, el elemento [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) debe estar presente y describir el método interno y su configuración. si es FALSE, PEAP realizará el acceso GUEST. El **elemento InnerEapOptional** es opcional.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 






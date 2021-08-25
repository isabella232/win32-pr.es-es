---
title: Elemento RequireCryptoBinding (EapType)
description: Indica si se debe autenticar con servidores que admiten el enlace criptográfico.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Elemento RequireCryptoBinding EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c4f4169e6ac0af123085795374b06de854b261b5f22004bd726ad47488bc11d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067225"
---
# <a name="requirecryptobinding-eaptype-element"></a>Elemento RequireCryptoBinding (EapType)

El **elemento RequireCryptoBinding (EapType)** indica si se debe autenticar con servidores que admiten el enlace criptográfico.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

El **elemento RequireCryptoBinding** se define mediante [**el elemento EapType.**](mspeapconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Comentarios

Si el **elemento RequireCryptoBinding** es TRUE, PEAP se autenticará con servidores que no admiten cryptobinding; si es FALSE, PEAP solo se autenticará con servidores que admitan el enlace criptográfico. El **elemento RequireCryptoBinding** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



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

 

 






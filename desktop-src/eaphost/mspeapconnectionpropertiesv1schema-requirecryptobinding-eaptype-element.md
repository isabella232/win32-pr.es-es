---
title: Elemento RequireCryptoBinding (EapType)
description: Indica si se va a autenticar con servidores que admiten cryptobinding.
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
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422526"
---
# <a name="requirecryptobinding-eaptype-element"></a>Elemento RequireCryptoBinding (EapType)

El elemento **RequireCryptoBinding (EapType)** indica si se va a autenticar con servidores que admiten cryptobinding.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

El elemento **RequireCryptoBinding** se define mediante el elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Observaciones

Si el elemento **RequireCryptoBinding** es true, PEAP se autenticará con servidores que no admitan cryptobinding; Si es FALSE, PEAP solo se autenticará con servidores que admitan cryptobinding. El elemento **RequireCryptoBinding** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 






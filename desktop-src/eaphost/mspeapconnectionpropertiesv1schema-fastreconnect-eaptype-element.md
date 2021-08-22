---
title: Elemento FastReconnect (EapType)
description: Obtenga información sobre el elemento FastReconnect (EapType). Este elemento indica si se debe realizar una reconexión rápida.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Elemento FastReconnect EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bda956d698ebefef956e85557c6d940baa02f6bcc9ef7cca0081fd668107e18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119238725"
---
# <a name="fastreconnect-eaptype-element"></a>Elemento FastReconnect (EapType)

El **elemento FastReconnect (EapType)** indica si se debe realizar una reconexión rápida.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

El **elemento FastReconnect** se define mediante el [**elemento EapType.**](mspeapconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Observaciones

Si el **elemento FastReconnect** es TRUE, PEAP intenta realizar una reconexión rápida. si es FALSE, PEAP realiza la autenticación completa. El **elemento FastReconnect** es opcional.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Server<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



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

 

 






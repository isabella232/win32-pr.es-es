---
title: Elemento UseWinLogonCredentials (EapType)
description: Obtenga información sobre el elemento UseWinLogonCredentials (EapType). Este elemento controla el uso de credenciales de winlogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Elemento EAPHost de UseWinLogonCredentials
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a407c505139562a155e5aa9d7ed57fed5d15077cf5d035ea8bb7bbe0e177363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086196"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Elemento UseWinLogonCredentials (EapType)

El **elemento UseWinLogonCredentials (EapType)** controla el uso de las credenciales de winlogin.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

El elemento [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) define el elemento **UseWinLogonCredentials.**

## <a name="remarks"></a>Comentarios

Si es TRUE, eap MS-CHAPv2 obtener las credenciales de winlogon. Si es FALSE, eap MS-CHAPv2 obtener las credenciales del usuario. El **elemento UseWinLogonCredentials (EapType)** es opcional.

## <a name="requirements"></a>Requisitos



| Rol | Versiones mínimas del sistema operativo admitidas |
|------|-------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 






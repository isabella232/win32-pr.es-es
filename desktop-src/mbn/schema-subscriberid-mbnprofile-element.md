---
description: Identifica el identificador único del perfil.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Elemento SubscriberID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475863"
---
# <a name="subscriberid-mbnprofile-element"></a>Elemento SubscriberID (MBNProfile)

El **elemento SubscriberID (MBNProfile)** identifica el identificador único del perfil.

En el caso de una red GSM, debe contener el IMSI (Identidad internacional del suscriptor móvil) de la SIM y, en el caso de los dispositivos CDMA, debe contener el valor MIN (número de identificación móvil) del dispositivo.

El elemento es una cadena numérica con una longitud máxima de 15 dígitos.

El elemento es obligatorio.

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

El **elemento SubscriberID** se define mediante el [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 





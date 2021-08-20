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
ms.openlocfilehash: 42290b0a80e85b2fdd1c794aced78571e939010b0e260bf1bdeba15f221cc103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065889"
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



| Requisito | Valor |
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

 

 





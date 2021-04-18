---
description: Identifica el identificador único del perfil.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: SubscriberID (MBNProfile), elemento
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542182"
---
# <a name="subscriberid-mbnprofile-element"></a>SubscriberID (MBNProfile), elemento

El elemento **SubscriberID (MBNProfile)** identifica el identificador único del perfil.

En el caso de una red GSM, debe contener la IMSI (identidad del suscriptor móvil internacional) de la tarjeta SIM y los dispositivos CDMA deben contener el número mínimo de identificación móvil del dispositivo.

El elemento es una cadena numérica con una longitud máxima de 15 dígitos.

El elemento es obligatorio.

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

El elemento **SubscriberID** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
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

 

 





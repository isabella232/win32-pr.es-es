---
title: AcceptServerName
description: Indica si el nombre del servidor se valida con la cadena de nombre especificada en el elemento ServerNames (ServerValidationParameters). | AcceptServerName
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1562d0de8d47e901d7e9815f44e1cf4f283c6bc7488f3a9476531d35bb9d3598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948165"
---
# <a name="acceptservername"></a>AcceptServerName

El **elemento AcceptServerName (EapType)** indica si el nombre del servidor se valida con la cadena de nombre especificada en el elemento [**ServerNames (ServerValidationParameters).**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

El elemento [**eapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) define el elemento .

## <a name="remarks"></a>Comentarios

El **elemento AcceptServerName** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Eaptlsconnectionpropertiesv1 Schema Elements](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**AcceptServerName (EapType)**](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 






---
description: Indica si se usa la autenticación 802.1 X.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: Elemento useOneX (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678013"
---
# <a name="useonex-authencryption-element"></a>Elemento useOneX (authEncryption)

El elemento useOneX (authEncryption) indica si se usa la autenticación 802.1 X.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

El elemento se define mediante el elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **useOneX** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**authEncryption (seguridad)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 





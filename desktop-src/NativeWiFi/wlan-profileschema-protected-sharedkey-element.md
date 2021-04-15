---
description: Indica si una clave compartida está cifrada.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: Elemento Protected (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677331"
---
# <a name="protected-sharedkey-element"></a>Elemento Protected (sharedKey)

El elemento Protected (sharedKey) indica si una clave compartida está cifrada.

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

El elemento se define mediante el elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Observaciones

En Windows Vista y Windows Server 2008, **Protected** siempre tiene el valor true si el perfil se recuperó del almacén de perfiles (por ejemplo, mediante una llamada a [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).

En el caso de los perfiles pensados para usarse en Windows XP con Service Pack 3 (SP3) o la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2), **Protected** debe tener un valor de false.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **protegido** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

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

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**sharedKey (seguridad)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 





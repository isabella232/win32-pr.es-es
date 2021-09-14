---
description: Indica si una clave compartida está cifrada.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: elemento protected (sharedKey)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272172"
---
# <a name="protected-sharedkey-element"></a>elemento protected (sharedKey)

El elemento protected (sharedKey) indica si se cifra una clave compartida.

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

El elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) define el elemento .

## <a name="remarks"></a>Observaciones

Para Windows Vista y Windows Server 2008, **protected** siempre tiene un valor de TRUE si el perfil se recuperó del almacén de perfiles (por ejemplo, mediante una llamada a [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).

Para los perfiles diseñados para su uso en Windows XP con Service Pack 3 (SP3) o wireless LAN API para Windows XP con Service Pack 2 (SP2), **protected** debe tener un valor de FALSE.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan **el elemento** protegido, vea Ejemplos de [perfil inalámbrico](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**sharedKey (seguridad)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 





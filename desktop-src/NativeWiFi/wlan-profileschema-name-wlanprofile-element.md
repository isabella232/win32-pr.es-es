---
description: Contiene el nombre de un perfil de LAN inalámbrica.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: elemento name (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245451"
---
# <a name="name-wlanprofile-element"></a>elemento name (WLANProfile)

El elemento name (WLANProfile) contiene el nombre de un perfil de LAN inalámbrica.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

El **elemento name** se define mediante el elemento [**WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="remarks"></a>Observaciones

Los nombres distinguen mayúsculas de minúsculas.

Para Windows XP con Service Pack 3 (SP3) y wireless LAN API para Windows XP con Service Pack 2 (SP2), el elemento name se omite cuando el perfil se guarda en el almacén de perfiles. El nombre del perfil se deriva del SSID de la red. Para los perfiles de red de infraestructura, el nombre del perfil es el SSID de la red. Para los perfiles de red ad hoc, el nombre del perfil es el SSID de la red ad hoc seguido de `-adhoc` . No se muestran los caracteres de escape XML, como &, . Evite el uso de caracteres de escape XML en nombres SSID para perfiles implementados en Windows XP con SP3 o API de LAN inalámbrica para Windows XP con SP2.

Para cualquier perfil de red pensado para su uso solo en Windows Vista o Windows Server 2008, el nombre puede ser cualquier cadena.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento name,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 





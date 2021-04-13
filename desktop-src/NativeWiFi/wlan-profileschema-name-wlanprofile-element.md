---
description: Contiene el nombre de un perfil de LAN inalámbrica.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: nombre (WLANProfile) (elemento)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543742"
---
# <a name="name-wlanprofile-element"></a>nombre (WLANProfile) (elemento)

El elemento Name (WLANProfile) contiene el nombre de un perfil de LAN inalámbrica.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

El elemento **Name** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Observaciones

Los nombres distinguen mayúsculas de minúsculas.

En Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2), el elemento Name se omite cuando el perfil se guarda en el almacén de perfiles. El nombre del perfil se deriva del SSID de la red. En el caso de los perfiles de red de infraestructura, el nombre del perfil es el SSID de la red. En el caso de los perfiles de red ad hoc, el nombre del perfil es el SSID de la red ad hoc seguido de `-adhoc` . No se muestran los caracteres de escape XML, como &. Evite usar caracteres de escape XML en nombres SSID para los perfiles implementados en Windows XP con SP3 o la API de LAN inalámbrica para Windows XP con SP2.

En el caso de cualquier perfil de red diseñado para usarse solo en Windows Vista o Windows Server 2008, el nombre puede ser cualquier cadena.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **Name** , vea [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 





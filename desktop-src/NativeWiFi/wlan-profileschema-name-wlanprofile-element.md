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
ms.openlocfilehash: 6a6d19c043f7cc2e42ca8221e98b05e4afe7628b143bd572465f00e1d3652275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984118"
---
# <a name="name-wlanprofile-element"></a>elemento name (WLANProfile)

El elemento name (WLANProfile) contiene el nombre de un perfil de LAN inalámbrica.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

El **elemento name** se define mediante el elemento [**WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="remarks"></a>Comentarios

Los nombres distinguen mayúsculas de minúsculas.

Para Windows XP con Service Pack 3 (SP3) e WIRELESS LAN API para Windows XP con Service Pack 2 (SP2), el elemento name se omite cuando el perfil se guarda en el almacén de perfiles. El nombre del perfil se deriva del SSID de la red. Para los perfiles de red de infraestructura, el nombre del perfil es el SSID de la red. Para los perfiles de red ad hoc, el nombre del perfil es el SSID de la red ad hoc seguido de `-adhoc` . Los caracteres de escape XML, &, no se muestran. Evite el uso de caracteres de escape XML en nombres SSID para perfiles implementados en Windows XP con SP3 o API de LAN inalámbrica para Windows XP con SP2.

Para cualquier perfil de red diseñado para su uso solo en Windows Vista o Windows Server 2008, el nombre puede ser cualquier cadena.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento name,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 





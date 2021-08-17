---
description: Especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Elemento userBasedVirtualLan (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9272f61e7efeaf90ba68b1577af9b0062e507984372f7f09ebdbfc15e4ac6fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064975"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>Elemento userBasedVirtualLan (singleSignOn)

El elemento userBasedVirtualLan (singleSignOn) especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario. Algunos dispositivos de servidor de acceso de red (NAS) cambian la VLAN después de que un usuario se autentique. Cuando userBasedVirtualLan es TRUE, el NAS puede cambiar la VLAN de un dispositivo después de que un usuario se autentique.

Este elemento es opcional. Cuando no se especifica userBasedVirtualLan en un perfil, se usa un valor FALSE.

**Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

El **elemento userBasedVirtualLan** se define mediante el [**elemento singleSignOn.**](onexschema-singlesignon-onex-element.md)

## <a name="remarks"></a>Comentarios

Este parámetro se puede establecer en la línea de comandos mediante el **comando netsh wlan set profileparameter.** Para obtener más información, [vea Netsh Commands for Wireless Local Area Network (wlan) (Comandos de Netsh para redes inalámbricas de área local [wlan]).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 

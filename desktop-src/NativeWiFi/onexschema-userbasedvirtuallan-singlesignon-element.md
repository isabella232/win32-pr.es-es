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
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154577"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>Elemento userBasedVirtualLan (singleSignOn)

El elemento userBasedVirtualLan (singleSignOn) especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario. Algunos dispositivos del servidor de acceso a la red (NAS) cambian la VLAN después de que un usuario se autentique. Cuando userBasedVirtualLan es TRUE, el NAS puede cambiar la VLAN de un dispositivo después de que un usuario se autentique.

Este elemento es opcional. Cuando userBasedVirtualLan no se especifica en un perfil, se usa un valor FALSE.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

El elemento **userBasedVirtualLan** se define mediante el elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

## <a name="remarks"></a>Observaciones

Este parámetro se puede establecer en la línea de comandos mediante el comando **netsh wlan set ProfileParameter** Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 

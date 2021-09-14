---
description: Especifica, en segundos, el retraso máximo antes de que se produce un error en el intento de conexión de inicio de sesión único.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Elemento maxDelay (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169438"
---
# <a name="maxdelay-singlesignon-element"></a>Elemento maxDelay (singleSignOn)

El elemento maxDelay (singleSignOn) especifica, en segundos, el retraso máximo antes de que se produce un error en el intento de conexión de inicio de sesión único.

Este elemento es opcional. Cuando maxDelay no se especifica en un perfil, se usa un valor de 10 segundos.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento maxDelay** se define mediante el [**elemento singleSignOn.**](onexschema-singlesignon-onex-element.md)

## <a name="remarks"></a>Observaciones

Este parámetro se puede establecer en la línea de comandos mediante el **comando netsh wlan set profileparameter.** Para obtener más información, [vea Netsh Commands for Wireless Local Area Network (wlan) (Comandos netsh para redes inalámbricas de área local [wlan]).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



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

 

 

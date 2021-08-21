---
description: Especifica el protocolo de autenticación que se usará para activar un contexto de Protocolo de datos de paquetes (PDP).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Elemento AuthProtocol (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 65b944b2966c9b5cac307f6f8efe6af2f42a1ffa5b4f2f400074caa0efe9f84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975264"
---
# <a name="authprotocol-contexttype-element"></a>Elemento AuthProtocol (contextType)

El **elemento AuthProtocol (contextType)** especifica el protocolo de autenticación que se usará para activar un contexto de Protocolo de datos de paquetes (PDP).

El elemento puede tener uno de los valores siguientes.

| Value      | Significado                                                                 |
|------------|-------------------------------------------------------------------------|
| "NONE"     | Sin protocolo de autenticación.                                             |
| "PAP"      | Autenticación de contraseña sin cifrar.                                    |
| "CHAP"     | Protocolo de autenticación de desafío de protocolo de enlace (CHAP).                      |
|  MsCHAPV2" | Use el protocolo de autenticación de desafío (CHAP) v2.0 de Microsoft. |



 

Este elemento es opcional y solo se usa para perfiles GSM. Si no se especifica el elemento y el perfil es para un dispositivo GSM, el servicio banda ancha móvil usará **"NONE".**

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El **elemento AuthProtocol** se define mediante el [**tipo complejo contextType.**](schema-contexttype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Contexto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 





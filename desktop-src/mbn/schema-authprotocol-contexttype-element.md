---
description: Especifica el protocolo de autenticación que se va a utilizar para activar un contexto del Protocolo de datos de paquetes (PDP).
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
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686754"
---
# <a name="authprotocol-contexttype-element"></a>Elemento AuthProtocol (contextType)

El elemento **AuthProtocol (contextType)** especifica el protocolo de autenticación que se va a utilizar para activar un contexto del Protocolo de datos de paquetes (PDP).

El elemento puede tener uno de los valores siguientes.

| Value      | Significado                                                                 |
|------------|-------------------------------------------------------------------------|
| NINGUNA     | No hay ningún protocolo de autenticación.                                             |
| Papanicolau      | Autenticación de contraseña no cifrada.                                    |
| CHAPV2     | Protocolo de autenticación por desafío mutuo (CHAP).                      |
|  MsCHAPV2 | Use el protocolo de autenticación por desafío mutuo (CHAP) v 2.0 de Microsoft. |



 

Este elemento es opcional y solo se usa para los perfiles de GSM. Si no se especifica el elemento y el perfil es para un dispositivo GSM, el servicio de banda ancha móvil usará **"none"**.

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

El elemento **AuthProtocol** se define mediante el tipo complejo de [**contextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
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

 

 





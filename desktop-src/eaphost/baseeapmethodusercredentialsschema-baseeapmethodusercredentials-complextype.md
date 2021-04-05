---
title: Tipo complejo de BaseEapMethodUserCredentials
description: Obtenga información sobre el tipo complejo de BaseEapMethodUserCredentials. Este tipo es un elemento de marcador de posición para los datos de credenciales de método.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Tipo complejo BaseEapMethodUserCredentials EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793785"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Tipo complejo de BaseEapMethodUserCredentials

El tipo complejo de **BaseEapMethodUserCredentials** es un elemento de marcador de posición para los datos de credenciales de método.

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Observaciones

El método EAP realiza la validación del esquema en el contenido de **BaseEapMethodUserCredentials**.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 






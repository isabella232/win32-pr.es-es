---
title: Tipo complejo BaseEapMethodUserCredentials
description: Obtenga información sobre el tipo complejo BaseEapMethodUserCredentials. Este tipo es un elemento de marcador de posición para los datos de credenciales de método.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Tipo complejo EAPHost de BaseEapMethodUserCredentials
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568860"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Tipo complejo BaseEapMethodUserCredentials

El **tipo complejo BaseEapMethodUserCredentials** es un elemento de marcador de posición para los datos de credenciales de método.

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



| Role | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Remoto<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[baseeapmethodusercredentials Schema](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 






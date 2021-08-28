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
ms.openlocfilehash: 8102f095ca7d4b1ada6db3c21fbe55e73a98ed6d06d2d6b99032f1a21a344527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094425"
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

## <a name="remarks"></a>Comentarios

El método EAP realiza la validación del esquema en el contenido de **BaseEapMethodUserCredentials**.

## <a name="requirements"></a>Requisitos



| Rol | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Cliente<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[baseeapmethodusercredentials Schema](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 






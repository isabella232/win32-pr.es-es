---
title: Elemento EapHostConfig
description: Contiene el elemento EapMethod y el elemento Config o ConfigBlob. Los elementos Config y ConfigBlob no se pueden usar simultáneamente.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- EapHostConfig, elemento EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c34ddd1607a59c0425f7ec789bedb4981a05983ead276a14308fbf6aaadf26de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274869"
---
# <a name="eaphostconfig-element"></a>Elemento EapHostConfig

El **elemento EapHostConfig** contiene el [**elemento EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) y [**el elemento Config**](eaphostconfigschema-config-eaphostconfig-element.md) [**o ConfigBlob.**](eaphostconfigschema-configblob-eaphostconfig-element.md)

Los [**elementos Config**](eaphostconfigschema-config-eaphostconfig-element.md) y [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) no se pueden usar simultáneamente.

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                    | Tipo                                                                                     | Descripción                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Config**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**BaseEapMethodConfig**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | Se usa cuando la configuración del método está en formato de texto XML en lugar de un blob binario.<br/>       |
| [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | Se usa cuando la configuración del método está en formato blob binario en lugar de en formato de texto de cadena.<br/> |
| [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                       | Identifica el método al que se hace referencia. <br/>                                                 |



## <a name="remarks"></a>Comentarios

El **elemento processContents** permite futuras mejoras en el esquema. El **elemento processContents** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 






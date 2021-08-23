---
description: Contiene la configuración de seguridad de las redes cableadas.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Elemento Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f66021f61536e8c8f09663e9ec2513b11d1ec87829f5c100b48cbf15d98cdd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685065"
---
# <a name="security-msm-element-lan_policy"></a>Elemento Security (MSM) (LAN_policy)

El elemento de seguridad (MSM) contiene la configuración de seguridad para redes cableadas. Este elemento es opcional.

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
                type="boolean"
             />
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

El **elemento** de seguridad se define mediante el [**elemento MSM.**](lan-profileschema-msm-lanprofile-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                 | Tipo    | Descripción                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Especifica si el servicio de configuración automática para redes cableadas intentará la autenticación de puerto mediante 802.1X. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1X para la autenticación de puertos. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Msm**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MSM (LANProfile)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 





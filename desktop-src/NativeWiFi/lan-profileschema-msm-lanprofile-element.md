---
description: Contiene la configuración del módulo específico del medio (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Elemento MSM (LANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071570"
---
# <a name="msm-lanprofile-element"></a>Elemento MSM (LANProfile)

El elemento MSM (LANProfile) contiene la configuración del módulo específico del medio (MSM).

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
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

El **elemento MSM** se define mediante el [**elemento LANProfile.**](lan-profileschema-lanprofile-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                 | Tipo    | Descripción                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Especifica si el servicio de configuración automática para redes cableadas intentará la autenticación de puerto mediante 802.1X.<br/>       |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1X para la autenticación de puertos. <br/> |
| [**Seguridad**](lan-profileschema-security-msm-element.md)              |         | Contiene la configuración de seguridad. <br/>                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**LANProfile**](lan-profileschema-lanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**LANProfile**](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 





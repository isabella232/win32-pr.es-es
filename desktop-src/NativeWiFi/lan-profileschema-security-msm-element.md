---
description: Contiene la configuración de seguridad para redes cableadas.
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
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105678857"
---
# <a name="security-msm-element-lan_policy"></a>Elemento Security (MSM) (LAN_policy)

El elemento de seguridad (MSM) contiene la configuración de seguridad de las redes cableadas. Este elemento es opcional.

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

El elemento de **seguridad** se define mediante el elemento [**MSM**](lan-profileschema-msm-lanprofile-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                 | Tipo    | Descripción                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Especifica si el servicio de configuración automática de redes cableadas intentará la autenticación del puerto mediante 802.1 X. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1 X para la autenticación de puertos. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MSM**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MSM (LANProfile)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 





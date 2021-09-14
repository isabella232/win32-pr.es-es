---
description: Especifica el par de autenticación y cifrado que se usará para este perfil.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Elemento authEncryption (seguridad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245576"
---
# <a name="authencryption-security-element"></a>Elemento authEncryption (seguridad)

El elemento authEncryption (seguridad) especifica el par de autenticación y cifrado que se usará para este perfil.

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="encryption">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="none"
                         />
                        <xs:enumeration
                            value="WEP"
                         />
                        <xs:enumeration
                            value="TKIP"
                         />
                        <xs:enumeration
                            value="AES"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
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

El elemento de seguridad define [**el**](wlan-profileschema-security-msm-element.md) elemento .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo                                                              | Descripción                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Autenticación**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Especifica el método de autenticación que se debe usar para conectarse a la LAN inalámbrica.<br/> |
| [**Cifrado**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Establece el cifrado de datos que se usará para conectarse a la LAN inalámbrica.<br/>                       |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica si se usa 802.1X.<br/>                                                     |



## <a name="remarks"></a>Observaciones

El [**elemento FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) se puede insertar como elemento secundario del **elemento authEncryption.**

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento authEncryption,** vea [Ejemplos de perfil inalámbrico](wireless-profile-samples.md). Para ver un perfil de ejemplo que usa el [**elemento FIPSMode,**](wlan-profileschema-fipsmode-authencryption-element.md) vea [Ejemplo de perfil de FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de perfil inalámbrico](wireless-profile-samples.md)
</dt> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Seguridad**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 

---
description: Contiene información de clave compartida.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: elemento sharedKey (security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 41677a57a51a98e5b9773ff3dda5b6f5084839c8e03f264567f9621f34ec4eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912715"
---
# <a name="sharedkey-security-element"></a>elemento sharedKey (security)

El elemento sharedKey (security) contiene información de clave compartida. Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="keyType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="networkKey"
                         />
                        <xs:enumeration
                            value="passPhrase"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
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



| Elemento                                                                 | Tipo                                                              | Descripción                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md) | [string](/dotnet/api/system.string)   | Contiene la clave de red o frase de contraseña.<br/>                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | Tipo de clave.<br/>                                                                                                                                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)     | [boolean](/dotnet/api/system.boolean) | Indica si la clave está cifrada.<br/> Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** Este elemento debe tener un valor false.<br/> |



## <a name="remarks"></a>Comentarios

Para Windows Vista y Windows Server 2008, los datos asociados al elemento **sharedKey** se cifran antes de guardarse en el almacén de perfiles.

Para Windows XP con SP3 y LAN API inalámbrica para Windows XP con SP2, los datos no se cifran.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **sharedKey,** vea [Ejemplo](non-broadcast-profile-sample.md)de perfil que no es de difusión, Ejemplo de perfil [wpa-personal](wpa-personal-profile-sample.md)y Ejemplo de perfil [wpa2-personal](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Seguridad**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 

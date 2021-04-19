---
description: Contiene información de claves compartidas.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: Elemento sharedKey (Security)
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
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677991"
---
# <a name="sharedkey-security-element"></a>Elemento sharedKey (Security)

El elemento sharedKey (Security) contiene información de claves compartidas. Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.

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

El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                 | Tipo                                                              | Descripción                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md) | [string](/dotnet/api/system.string)   | Contiene la clave o frase de contraseña de la red.<br/>                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | Tipo de clave.<br/>                                                                                                                                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)     | [boolean](/dotnet/api/system.boolean) | Indica si la clave está cifrada.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento debe tener un valor de FALSE.<br/> |



## <a name="remarks"></a>Observaciones

En Windows Vista y Windows Server 2008, los datos asociados con el elemento **sharedKey** se cifran antes de guardarse en el almacén de perfiles.

En el caso de Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2, los datos no se cifran.

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **sharedKey** , vea ejemplo [de perfil sin difusión](non-broadcast-profile-sample.md), ejemplo de perfil [de WPA-Personal](wpa-personal-profile-sample.md)y [ejemplo de perfil WPA2-Personal](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**bursátil**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**seguridad (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 

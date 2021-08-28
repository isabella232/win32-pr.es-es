---
description: Contiene varias configuraciones para proveedores de hardware independientes.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Elemento IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1cfcd9ee463ef91d04d0bebbeac800d48da32fdd777edc2a08ccf0051410160d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799925"
---
# <a name="ihv-wlanprofile-element"></a>Elemento IHV (WLANProfile)

El elemento IHV (WLANProfile) contiene varias configuraciones para proveedores de hardware independientes. Si un perfil incluye la configuración de seguridad de IHV, invalida cualquier seguridad definida por Microsoft.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
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

El elemento se define mediante el [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectividad**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Contiene la configuración de conectividad relacionada con IHV.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Contiene un hexBinary de 3 bytes que identifica la IHV.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifica el IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**Seguridad**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Contiene la configuración de seguridad específica de IHV. La configuración de seguridad de Microsoft y la configuración de seguridad de IHV son mutuamente excluyentes. El perfil completo no es válido si ambas opciones de seguridad están presentes.<br/>                                                                                                                                                                                            |
| [**tipo**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Contiene un hexBinary de 1 byte que se usa para diferenciar las NIC por el mismo IHV.<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | Especifica el origen de la configuración de seguridad 802.1X utilizada por un componente de seguridad de IHV. Cuando [**useMSOneX es**](wlan-profileschema-usemsonex-ihv-element.md) true, los componentes de seguridad de IHV usan la configuración 802.1X definida por Microsoft. Cuando **useMSOneX es** false, los componentes de seguridad de IHV usan la configuración 802.1X proporcionada por el proveedor. De forma predeterminada, **useMSOneX** es false. Este elemento es opcional.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 

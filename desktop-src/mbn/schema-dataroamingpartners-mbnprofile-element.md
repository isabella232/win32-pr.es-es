---
description: Especifica la lista de proveedores de red preferidos en el momento de la itinerancia.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Elemento DataRoamingPartners (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168145"
---
# <a name="dataroamingpartners-mbnprofile-element"></a>Elemento DataRoamingPartners (MBNProfile)

El **elemento DataRoamingPartners (MBNProfile)** especifica la lista de proveedores de red preferidos en el momento de la itinerancia.

El servicio banda ancha móvil usa este elemento para seleccionar la red preferida durante la itinerancia.

El elemento tiene el siguiente elemento secundario que se debe definir al menos una vez, pero se puede definir varias veces.

-   [**Proveedor**](schema-provider-dataroamingpartners-element.md)

Este elemento puede tener un máximo de una aparición.

Este elemento es opcional.

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El **elemento DataRoamingPartners** se define mediante el [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                         | Tipo                                                    | Descripción                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [**Proveedor**](schema-provider-dataroamingpartners-element.md) | [**providerType**](schema-providertype-complextype.md) | Nombre e identificador de proveedor de una red de telefonía móvil.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 





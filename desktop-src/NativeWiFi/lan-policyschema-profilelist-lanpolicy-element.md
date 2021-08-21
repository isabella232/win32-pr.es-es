---
description: 'Elemento profileList (LANPolicy): contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo.'
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: elemento profileList (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 25582be51d3206c17076c702bb159f13b012d5964a10cc4ebd7908459447fcc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801125"
---
# <a name="profilelist-lanpolicy-element"></a>elemento profileList (LANPolicy)

El elemento profileList (LANPolicy) contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo. Los perfiles deben basarse en el esquema de [ \_ perfil LAN](lan-profileschema-schema.md), con un elemento raíz de [**LANProfile**](lan-profileschema-lanprofile-element.md). Se omitirán los perfiles basados en cualquier otro esquema.

Cuando [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) se establece en FALSE, este elemento no debe estar presente en un perfil de directiva LAN. Cuando **enableAutoConfig** se establece en TRUE, se requiere este elemento.

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El **elemento profileList** se define mediante el [**elemento LANPolicy.**](lan-policyschema-lanpolicy-element.md)

## <a name="remarks"></a>Comentarios

Este elemento debe contener exactamente un perfil de red. Si se especifica más de un perfil en la directiva, solo se aplicará la primera red.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 





---
description: 'Elemento profileList (LANPolicy): contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo.'
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Elemento profileList (LANPolicy)
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
ms.openlocfilehash: 5d18ebc99f48bf72599afe750863d684b8158608
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090783"
---
# <a name="profilelist-lanpolicy-element"></a>elemento profileList (LANPolicy)

El elemento profileList (LANPolicy) contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo. Los perfiles deben basarse en el esquema de [ \_ perfil de LAN](lan-profileschema-schema.md), con un elemento raíz de [**LANProfile**](lan-profileschema-lanprofile-element.md). Se omitirán los perfiles basados en cualquier otro esquema.

Cuando [**enableAutoConfig se**](lan-policyschema-enableautoconfig-globalflags-element.md) establece en FALSE, este elemento no debe estar presente en un perfil de directiva LAN. Cuando **enableAutoConfig se** establece en TRUE, se requiere este elemento.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 





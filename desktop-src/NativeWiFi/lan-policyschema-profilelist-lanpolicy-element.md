---
description: Contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: profileList (LANPolicy), elemento
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
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667937"
---
# <a name="profilelist-lanpolicy-element"></a>profileList (LANPolicy), elemento

El elemento profileList (LANPolicy) contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo. Los perfiles deben basarse en [el \_ esquema de Perfil de LAN](lan-profileschema-schema.md), con un elemento raíz de [**LANProfile**](lan-profileschema-lanprofile-element.md). Los perfiles basados en cualquier otro esquema se omitirán.

Cuando [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) se establece en false, este elemento no debe estar presente en un perfil de directiva de LAN. Cuando **enableAutoConfig** se establece en true, este elemento es obligatorio.

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

El elemento **profileList** se define mediante el elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .

## <a name="remarks"></a>Observaciones

Este elemento debe contener exactamente un perfil de red. Si se especifica más de un perfil en la Directiva, solo se aplicará la primera red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



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

 

 





---
description: Contiene la configuración global para la configuración automática de redes cableadas.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Elemento Indicadores_globales (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277733"
---
# <a name="globalflags-lanpolicy-element"></a>Elemento Indicadores_globales (LANPolicy)

El elemento Indicadores_globales (LANPolicy) contiene la configuración global para la configuración automática de redes cableadas.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
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

El elemento **indicadores_globales** se define mediante el elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Tipo    | Descripción                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean | Especifica si los equipos usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1 X).<br/> |



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

 

 





---
description: Contiene una directiva de LAN cableada.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Elemento LANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687930"
---
# <a name="lanpolicy-element"></a>Elemento LANPolicy

El elemento LANPolicy contiene una directiva de LAN cableada. Este elemento es el elemento raíz único para un perfil de directiva de red cableada.

El espacio de nombres de destino para el elemento **LANPolicy** es `https://www.microsoft.com/networking/LAN/policy/v1` .

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
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
            <xs:element name="profileList"
                minOccurs="0"
            >
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

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Tipo                                                     | Descripción                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**denominación**](lan-policyschema-description-lanpolicy-element.md)             | [**nameType**](lan-policyschema-nametype-simpletype.md) | Contiene la descripción de una directiva de LAN cableada. <br/>                                                                                                                          |
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean                                                  | Especifica si los equipos usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1 X).<br/> |
| [**Indicadores**](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | Contiene la configuración global para la configuración automática de redes cableadas. <br/>                                                                                          |
| [**name**](lan-policyschema-name-lanpolicy-element.md)                           | [**nameType**](lan-policyschema-nametype-simpletype.md) | Contiene el nombre de una directiva de LAN cableada. <br/>                                                                                                                                 |
| [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | Contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo. <br/>                                                                                                |



## <a name="remarks"></a>Observaciones

Para ver la lista de elementos secundarios en una estructura similar a un árbol, [vea \_ elementos de esquema de directiva de LAN](lan-policyschema-elements.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





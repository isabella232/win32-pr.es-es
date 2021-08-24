---
description: Contiene una directiva LAN cableada.
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
ms.openlocfilehash: 468e9fb0500c4a514b7b0a9dddea023f0851b9f7ba783504548f2285810ffffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780185"
---
# <a name="lanpolicy-element"></a>Elemento LANPolicy

El elemento LANPolicy contiene una directiva LAN cableada. Este elemento es el elemento raíz único para un perfil de directiva de red cableada.

El espacio de nombres de destino **para el elemento LANPolicy** es `https://www.microsoft.com/networking/LAN/policy/v1` .

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
| [**Descripción**](lan-policyschema-description-lanpolicy-element.md)             | [**nameType**](lan-policyschema-nametype-simpletype.md) | Contiene la descripción de una directiva DE LAN cableada. <br/>                                                                                                                          |
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean                                                  | Especifica si las máquinas usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1X).<br/> |
| [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | Contiene la configuración global para la configuración automática de redes cableadas. <br/>                                                                                          |
| [**Nombre**](lan-policyschema-name-lanpolicy-element.md)                           | [**nameType**](lan-policyschema-nametype-simpletype.md) | Contiene el nombre de una directiva DE LAN cableada. <br/>                                                                                                                                 |
| [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | Contiene una lista de perfiles que se aplicarán en el nivel de dominio o equipo. <br/>                                                                                                |



## <a name="remarks"></a>Comentarios

Para ver la lista de elementos secundarios en una estructura similar a un árbol, vea Elementos de esquema de [ \_ directiva LAN](lan-policyschema-elements.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





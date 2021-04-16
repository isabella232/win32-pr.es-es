---
description: Contiene la configuración global del módulo de configuración automática (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Elemento Indicadores_globales (WLANPolicy)
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
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546814"
---
# <a name="globalflags-wlanpolicy-element"></a>Elemento Indicadores_globales (WLANPolicy)

El elemento Indicadores_globales (WLANPolicy) contiene la configuración global para el módulo de configuración automática (ACM). Este elemento es obligatorio.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:element name="showDeniedNetwork"
                type="boolean"
             />
            <xs:element name="allowEveryoneToCreateAllUserProfiles"
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

El elemento **indicadores_globales** se define mediante el elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                    | Tipo    | Descripción                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean | Especifica si un usuario puede crear un perfil de todos los usuarios. <br/>                                                               |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean | Especifica si los equipos usan el servicio de configuración automática (AutoConfig) integrado para administrar las conexiones inalámbricas. <br/> |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean | Especifica si las redes denegadas aparecen en el Asistente para **conectarse a una red** . <br/>                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 





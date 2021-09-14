---
description: Contiene la configuración global del módulo de configuración automática (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Elemento globalFlags (WLANPolicy)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161189"
---
# <a name="globalflags-wlanpolicy-element"></a>Elemento globalFlags (WLANPolicy)

El elemento globalFlags (WLANPolicy) contiene la configuración global del módulo de configuración automática (ACM). Este elemento es obligatorio.

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

El **elemento globalFlags** se define mediante el [**elemento WLANPolicy.**](wlan-policyschema-wlanpolicy-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                    | Tipo    | Descripción                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean | Especifica si un usuario puede crear un perfil de todo el usuario. <br/>                                                               |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean | Especifica si las máquinas usan el servicio de configuración automática integrado (AutoConfig) para administrar conexiones inalámbricas. <br/> |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean | Especifica si las redes denegadas aparecen en el **Conectar a un Asistente para** redes. <br/>                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 





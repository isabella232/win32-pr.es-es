---
description: Especifica la configuración de EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Elemento EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667142"
---
# <a name="eapconfig-onex-element"></a>Elemento EAPConfig (OneX)

El elemento **EAPConfig** (Onex) especifica la configuración de EAPHost.

A diferencia de la mayoría de los elementos del esquema de perfil 802.1 X, este elemento se encuentra en el `https://www.microsoft.com/provisioning/EapHostConfig` espacio de nombres. Sus elementos secundarios se definen en el [esquema eaphostconfig](../eaphost/eaphostconfigschema-schema.md). El elemento [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) es un elemento secundario del elemento **EAPConfig** .

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento **EAPConfig** se define mediante el elemento [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**Onex-**](onexschema-onex-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Onex-**](onexschema-onex-element.md)
</dt> </dl>

 

 

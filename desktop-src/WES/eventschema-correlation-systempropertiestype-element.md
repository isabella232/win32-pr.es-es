---
title: Elemento Correlation (SystemPropertiesType)
description: Identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Elemento Correlation EventLog
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242607"
---
# <a name="correlation-systempropertiestype-element"></a>Elemento Correlation (SystemPropertiesType)

Identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

El tipo complejo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) define el elemento **Correlation.**

## <a name="attributes"></a>Atributos



| Nombre              | Tipo                                                | Descripción                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de actividad        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica la actividad actual. Los eventos que se publican con este identificador forman parte de la misma actividad.<br/>                              |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica la actividad a la que se ha transferido el control. A continuación, los eventos relacionados tendrían este identificador como identificador activityID.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 






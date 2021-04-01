---
title: Elemento Correlation (SystemPropertiesType)
description: Los identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Elemento de correlación EventLog
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996841"
---
# <a name="correlation-systempropertiestype-element"></a>Elemento Correlation (SystemPropertiesType)

Los identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.

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

El elemento de **correlación** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nombre              | Tipo                                                | Descripción                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de actividad        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica la actividad actual. Los eventos que se publican con este identificador forman parte de la misma actividad.<br/>                              |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica la actividad a la que se transfirió el control. Los eventos relacionados tendrían este identificador como su identificador ActivityID.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





